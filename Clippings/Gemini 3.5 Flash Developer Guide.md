![Image](https://pbs.twimg.com/media/HIslZpOa4AIbkcS?format=jpg&name=large)

[Gemini 3.5 Flash](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/#gemini-3-5-flash) is **generally available (GA)**, stable, and ready for scaled production use. As our most intelligent Flash model, it delivers sustained frontier performance in agentic execution, coding, and long-horizon tasks at scale.

This guide contains an overview of improvements, API changes, and migration guidance for Gemini 3.5 Flash.

## New model

Gemini 3.5 Flash: Our most intelligent model for sustained frontier performance in agentic and coding tasks.

Model ID: gemini-3.5-flash

Gemini 3.5 Flash supports the 1M token context window, 65k max output tokens, thinking, and the same set of tools and platform features as Gemini 3 Flash. [Computer Use](https://ai.google.dev/gemini-api/docs/computer-use) is not supported at this moment.

For complete specs, see the [models overview](https://ai.google.dev/gemini-api/docs/models/gemini-3.5-flash). For pricing, see the [pricing page](https://ai.google.dev/gemini-api/docs/pricing#gemini-3.5-flash).

## Quickstart

Install the latest Google Gen AI SDK:

```bash
pip install -U google-genai
```

All code examples in this guide use the [Interactions API](https://ai.google.dev/gemini-api/docs/interactions). The Interactions API is the new standard primitive for building with Gemini, recommended for all new projects. It is optimized for agentic workflows, server-side state management, and complex multi-modal, multi-turn conversations. The [GenerateContent API](https://ai.google.dev/gemini-api/docs/whats-new-gemini-3.5) is also supported; the same configuration options and recommendations apply.

```python
# Interactions API
from google import genai

client = genai.Client()

interaction = client.interactions.create(
    model="gemini-3.5-flash",
    input="Explain how parallel agentic execution works in three sentences."
)
print(interaction.output_text)
```

```python
# Generate Content API
from google import genai

client = genai.Client()

response = client.models.generate_content(
   model="gemini-3.5-flash",
   contents="How does AI work?",
)
print(response.text)
```

## What's new

- **Sustained frontier performance:** Our most intelligent Flash model, optimized for agentic and coding tasks at scale.
- **Agentic execution:** Sub-agent deployment, problem solving, and rapid agentic loops at scale.
- **Coding:** Iterative coding cycles, rapid exploration, and prototyping to test alternate paths and dynamically explore solutions.
- **Long horizon:** Multi-step workflows and tool use at scale.
- **Thought preservation:** The model maintains intermediate reasoning across multi-turn conversations automatically. No API changes needed.
- **New default effort level:** Default thinking effort changed from high to medium. See New default effort level for details.
- **Improved** **low** **thinking:** low is now significantly improved for code and agentic tasks that require fewer steps, offering strong quality at lower latency and cost.
- **GA release:** Stable model for scaled production use.

## Behavioral changes

New default effort level: medium

The default thinking effort is now **medium**, changed from high in Gemini 3 Flash Preview. medium yields very good results across a wide range of tasks while being faster and more cost-efficient. For complex problems, high encourages the model to think more deeply.

![Image](https://pbs.twimg.com/media/HIso9qfbQAAIV2v?format=jpg&name=large)

To override the default, set thinking\_level in your config:

```python
from google import genai

client = genai.Client()

interaction = client.interactions.create(
    model="gemini-3.5-flash",
    input="Prove that the square root of 2 is irrational.",
    generation_config={"thinking_level": "high"},
)
print(interaction.output_text)
```

Tip: Start with medium, it provides the best quality for the vast majority of tasks. Try low for a faster, cheaper experience with strong quality. Switch to high for complex reasoning, hard math, or difficult coding challenges. Use minimal to optimize for speed in simple queries.

Thought preservation

The model maintains intermediate reasoning across multi-turn conversations automatically. When present in the conversation history, reasoning context carries forward, which improves performance on complex multi-step tasks like iterative debugging and code refactoring. No API changes needed:

- **Interactions API**: Thoughts are already preserved automatically. No change in behavior.
- **GenerateContent API**: Beginning with Gemini 3.5 Flash, the model uses reasoning context from all previous turns when thought signatures are present in the conversation history. To enable this, pass the full, unmodified conversation history (including [thought signatures](https://ai.google.dev/gemini-api/docs/thought-signatures)) in contents. The SDKs handle this automatically.

## Parameter updates and best practices in Gemini 3.x

The following apply to **all Gemini 3.x models**, including Gemini 3.5 Flash.

- **temperature****,** **top\_p****,** **top\_k**: we strongly recommend not changing the default values. Gemini 3's reasoning capabilities are optimized for the default settings.
- Use thinking\_level instead of thinking\_budget.
- **Function calling response matching**: id, name, and response count must match the preceding calls.
- **Multimodal function responses**: include multimodal content inside the function response, not outside it.
- **Inline instructions in function responses**: append to the function response text, not as separate parts.
- **Reduce unnecessary tool calls**: Use lower thinking levels or experiment with system instructions to reduce tool calls in agentic workflows.

See the sections below for how to update your code.

Sampling parameters (no longer recommended)

temperature, top\_p, and top\_k are no longer recommended for all Gemini 3.x models. Gemini 3's reasoning capabilities are optimized for the default settings. **Remove these parameters from all requests.**

```python
# ⚠️ Remove these parameters (not recommended)
generation_config = {
    "temperature": 0.7,
    "top_p": 0.9,
    "top_k": 40,
}
```

To ensure determinism, we recommend defining a system instruction with explicit rules for your specific use case.

**thinking\_budget** **(no longer recommended)**

The raw numeric thinking\_budget parameter is no longer recommended across all Gemini 3.x models. Use the thinking\_level string enum instead.

```python
# ⚠️ Before (not recommended)
generation_config = {
    "thinking": {"thinking_budget": 7500},
}

# ✅ After
generation_config = {
    "thinking": {"thinking_level": "medium"},
}
```

Available values: minimal, low, medium (default), and high.

Function calling: strict response matching

The Interactions API already errors on mismatched function responses. The GenerateContent API does not yet error, but mismatched responses cause the model to return empty responses with finish\_reason: STOP in most cases. Always follow these conventions:

![Image](https://pbs.twimg.com/media/HIsqKpybEAAvnbQ?format=jpg&name=large)

```python
# ✅ Include matching call_id and name in the function_result
final_interaction = client.interactions.create(
    model="gemini-3.5-flash",
    previous_interaction_id=interaction.id,
    tools=[my_tool],
    input=[{
        "type": "function_result",
        "name": fc_step.name,
        "call_id": fc_step.id,
        "result": [{"type": "text", "text": json.dumps(result)}],
    }],
)
```

**Multimodal function responses**

We often see clients provide images outside function response. This can lead to unexpected model behavior (e.g. thought leakage) and result in lower quality outputs. Follow the recommendation in [Multimodal Function Responses API docs](https://ai.google.dev/gemini-api/docs/interactions/function-calling?example=meeting#multimodal) instead and include multimodal content in the function response parts that you send to the model. The model can process this multimodal content in its next turn to produce a more informed response.

```python
# ✅ Include multimodal content in the function response
final_interaction = client.interactions.create(
    model="gemini-3.5-flash",
    previous_interaction_id=interaction.id,
    input=[
        {
            "type": "function_result",
            "name": tool_call.name,
            "call_id": tool_call.id,
            "result": [
                {"type": "text", "text": "instrument.jpg"},
                {
                    "type": "image",
                    "mime_type": "image/jpeg",
                    "data": base64_image_data,
                },
            ],
        }
    ],
)
```

Inline instructions in function responses

We often see clients provide additional instructions along with function responses as subsequent Parts. This can lead to unexpected model behavior (e.g. thought leakage) and result in lower quality outputs. Instead, append any extra instructions to the end of the function response text separated by two newlines.

```python
# ✅ Append inline instructions to the end of the function response separated by two newlines
result_text = f"{json.dumps(result)}\n\n<your inline instructions>"

final_interaction = client.interactions.create(
    model="gemini-3.5-flash",
    previous_interaction_id=interaction.id,
    tools=[my_tool],
    input=[
        {
            "type": "function_result",
            "name": fc_step.name,
            "call_id": fc_step.id,
            "result": [{"type": "text", "text": result_text}],
        }
    ],
)
```

Reducing unnecessary tool calls

If you experience an overuse of tool calls, two techniques help minimize them:

1. **Start by reducing the thinking level** (medium, low, or minimal): Higher thinking levels encourage the model to use more tools to explore and verify, so lowering the level can reduce tool calls.
2. **Add a system instruction:** If overuse persists after adjusting the thinking level, consider a prompt that restricts tool usage. For example:

You have a limited action budget of <n> tool calls. Use them efficiently.

## Migration checklist

Note: **Automate this migration with a coding agent.** If you use a coding agent that supports skills (like Antigravity), install the [Gemini Interactions API skill](https://ai.google.dev/gemini-api/docs/coding-agents#gemini-interactions-api) and run:

```bash
/gemini-interactions-api migrate my app to Gemini 3.5 Flash
```

**We strongly recommend updating to** **google-genai** **SDK v2.0.0 or later.** This version introduces breaking changes to the Interactions API. See the [breaking changes migration guide](https://ai.google.dev/gemini-api/docs/interactions-breaking-changes-may-2026) for details.

## Migrate from Gemini 3 Flash Preview

- Update model name: gemini-3-flash-preview → gemini-3.5-flash
- Review pricing. Gemini 3.5 Flash is more expensive than Gemini 3 Flash Preview. See the [pricing page](https://ai.google.dev/gemini-api/docs/pricing#gemini-3.5-flash) for details.
- Remove temperature, top\_p, top\_k from your config (no longer recommended).
- Replace thinking\_budget with thinking\_level.
- Add id and matching name to all FunctionResponse parts.
- Test your prompts. Default effort changed from high → medium; verify quality, speed, and cost.
- Thought preservation is now on by default. Reasoning context carries forward across turns, which improves performance but may increase token usage.
- Reduce unnecessary tool calls: start by reducing the thinking level (medium, low, or minimal); add a system instruction to constrain tool usage if overuse persists.
- [Computer Use](https://ai.google.dev/gemini-api/docs/computer-use) is not supported in Gemini 3.5 Flash at this moment. For Computer Use workloads, continue using Gemini 3 Flash Preview.

## Migrate from Gemini 2.5

All of the above, plus:

- Simplify prompts. If you used chain-of-thought prompt engineering to force reasoning, try thinking\_level: "medium" or "high" with simpler prompts instead.
- Test PDF and media workloads. If you relied on specific behavior for dense document parsing, test the media\_resolution\_high setting to ensure continued accuracy. Migrating to Gemini 3 defaults may also increase token usage for PDFs but decrease it for video; if requests exceed the context window, explicitly reduce the media\_resolution. See the [media resolution](https://ai.google.dev/gemini-api/docs/interactions/media-resolution) docs for details.
- Leverage [combined tool use](https://ai.google.dev/gemini-api/docs/interactions/tool-combination). Google Search, URL context, code execution, and custom functions can be used in the same request.
- If using multimodal function responses, move multimodal content inside function response parts, not alongside them.
- If using inline instructions with function responses, append them to the function response text separated by two newlines, not as separate parts.
- Image segmentation is not supported in Gemini 3.x. For segmentation workloads, continue using Gemini 2.5 Flash with thinking off, or [Gemini Robotics-ER 1.6](https://ai.google.dev/gemini-api/docs/robotics-overview).

## Gemini 3 family features

Gemini 3.5 Flash inherits all Gemini 3 family capabilities except Computer Use. Features introduced in Gemini 3 that carry forward:

- [Thinking](https://ai.google.dev/gemini-api/docs/interactions/thinking)**:** Encrypted reasoning context preserved across API calls. Automatic in the Interactions API; implicit in GenerateContent.
- [Structured outputs with tools](https://ai.google.dev/gemini-api/docs/interactions/structured-output)**:** Combine JSON mode with built-in tools (Search, URL context, code execution, function calling).
- [Multimodal function responses](https://ai.google.dev/gemini-api/docs/interactions/function-calling#multimodal)**:** Return images, audio, and other media in function call results.
- [Code execution with images](https://ai.google.dev/gemini-api/docs/interactions/code-execution#images)**:** Execute code that processes and generates images.
- [Combined tool use](https://ai.google.dev/gemini-api/docs/interactions/tool-combination)**:** Use built-in tools and custom function calling in the same request.

## Next steps

- Read more about the Gemini 3 family in the [Gemini 3 developer guide](https://ai.google.dev/gemini-api/docs/gemini-3)
- Learn more about prompt design strategies in the [prompt engineering guide](https://ai.google.dev/gemini-api/docs/prompting-strategies).
- Get started with the [Gemini 3 Cookbook](https://github.com/google-gemini/cookbook)
- Learn about [Gemini API optimization and inference](https://ai.google.dev/gemini-api/docs/optimization)