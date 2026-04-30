## [AI Advances](https://ai.gopubby.com/?source=post_page---publication_nav-3fe99b2acc4-cf12d0125238---------------------------------------)

[![AI Advances](https://miro.medium.com/v2/resize:fill:76:76/1*R8zEd59FDf0l8Re94ImV0Q.png)](https://ai.gopubby.com/?source=post_page---post_publication_sidebar-3fe99b2acc4-cf12d0125238---------------------------------------)

Democratizing access to artificial intelligence

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*xzmsE3WRtGUIGrDMMkVOXA.jpeg)

Image source: stock.adobe.com \[Licensed\]

### Not a Medium member? Read this article for free here: Link

### TL;DR

> Document parsers struggle with extracting complex layouts common in real-world documents, such as tables having merged cells, cross-page breaks, and misplaced text. Moreover, a large part of the information lies in charts/graphs or figures, which require accurate extraction. This article walks you through a parser that extracts all multimodal data from documents with accurate layout preservation. It demonstrates how you can use it as a reusable Python package that works with multiple model providers.

Accurate extraction of content from documents is critical for AI applications. For instance, while processing a **purchase order for generating a sales draft using AI**, an AI agent or an LLM first needs to accurately understand the purchase order content with the exact layout.

A misaligned table header can make the LLM read the wrong quantity, which will result in wrong price calculation. Similarly, a missed line item due to a cross-page table break can cause the LLM to skip a product entirely.

And we have seen this happening quite often in our **generative AI project** ([**GAIK**](https://gaik.ai/)), in which we build AI applications with enterprise documents, using our **open-source generative AI toolkit** (see GAIK’s GitHub repository [**here**](https://github.com/GAIK-project/gaik-toolkit/tree/main)).

Many customer documents, such as purchase orders or bills of materials, contain messy tables. As an example, see the following 2 pages of a purchase order (content changed for privacy reasons while preserving the layout).

![](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*98M5hOaQZ57D5yNdc9xU8w.png)

There is a text between the table header and row data. Of course, this is not the right place to add this text. It could have been added to some other place before or after the table. But it is quite common to expect such structures from customer documents. This text is also unnecessarily repeated in other places in the same table.

The table continues on multiple pages with row data partially written across pages. For instance, the first page contains partial data for the third item (030), followed by the table footer, and page header and title (repeated) on the next page.

Specialized parsers, such as **PyMuPDF, PyMuPDF4LLM**, or **Docling**, do not accurately extract this table structure.

I addressed this issue in my following articles:

## [How to Extract Everything from Documents Using AI](https://medium.com/data-science-collective/how-i-enhanced-doclings-image-interpretation-capabilities-641ce017bce5?source=post_page-----cf12d0125238---------------------------------------)

### I created a vision-enhanced document parser and RAG chunker

medium.com

## [Building a Generic Knowledge Extraction AI Framework for Organization-Specific Use Cases](https://medium.com/data-science-collective/building-a-generic-knowledge-extraction-ai-framework-for-organization-specific-use-cases-cbb52ce93e48?source=post_page-----cf12d0125238---------------------------------------)

### Allowing non-technical users to specify requirements in plain language, automatically generate schemas, and extract…

medium.com

Even these two parsers do not correctly extract such messy table layouts. See the following extraction snapshots.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*EvixioqnKTP4nqy7YJzhtA.png)

Partial view of the table extracted by Docling+LLM parser (image by author)

![](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*UlE8ACL9Dh9YnKr7sobgog.png)

Partial view of the table extracted by GAIK’s Vision+ parser using vision LLM (image by author)

The fix ultimately turned out to be much simpler than I expected.

It was all about using the right prompts. Just a different way of asking the AI models what you want.

Earlier this month, [LlamaIndex](https://www.llamaindex.ai/) published the document parsing prompts they used in their [benchmark study](https://arxiv.org/abs/2604.08538), and those prompts changed everything.

Here’s the proof. The same purchase order that failed every other parser we tried:

![](https://miro.medium.com/v2/resize:fit:1334/format:webp/1*YjNFJn0MNM4Gzkqu38nEDA.png)

Partial view (converted to HTML for better readability) of the purchase order table extracted by GAIK’s multimodal parser with gemini-3.1-flash-lite-preview model with reasoning effort set to low (image by author)

> In this article, we will create a multimodal parser to accurately extract/parse the content from documents with messy layouts.

The multimodal parser allows the user to select a provider and a model (**OpenAI, Anthropic, or Google**) with several other options to evaluate parsing quality for their use case.

The source code of the multimodal parser with detailed guidelines and documentation can be found at the following link in the GAIK toolkit’s GitHub repository: [**multimodal\_parser**](https://github.com/GAIK-project/gaik-toolkit/tree/main/implementation_layer/src/gaik/software_components/parsers/multimodal_parser). It requires API credentials for at least one provider (**OpenAI, Azure, or Google Vertex AI**).

## It Was All About Some Specific Prompts

Earlier this month, [**LlamaIndex**](https://www.llamaindex.ai/) launched an open-source framework ([**ParseBench**](https://github.com/run-llama/ParseBench)) for benchmarking how well document parsers convert PDFs into output that AI agents can actually use. They tested 14 different methods: general-purpose vision LLMs, specialized parsers, and their own LlamaParse.

Their benchmark results are published in the following study:

## [ParseBench: A Document Parsing Benchmark for AI Agents](https://arxiv.org/abs/2604.08538?source=post_page-----cf12d0125238---------------------------------------)

### AI agents are changing the requirements for document parsing. What matters is semantic correctness: parsed output must…

arxiv.org

These results show that the agentic parsing (such as their own [LlamaParse](https://developers.llamaindex.ai/llamaparse/)) and LLM-based parsing (such as with Gemini 3 Flash) outperform specialized document parsers.

![](https://miro.medium.com/v2/resize:fit:1304/format:webp/1*yswYR2uojKubWHiKX1TK6w.png)

Agentic and VLM-based parsing outperform specialized parsers. Image source: https://www.llamaindex.ai/blog/parsebench

I was curious to know how they got the LLM-based parsing to work so well. So I went through the actual research paper.

I expected some clever architectural trick. A fine-tuned model, or a multi-step pipeline with verification loops.

Instead, I found some specific prompts. The prompts that we had never thought to use.

## What is Special About These Prompts?

When you ask an LLM to output a table as Markdown (the default for most parsers), it doesn’t preserve the layout of merged cells and multi-level headers correctly. For instance, a purchase order with a two-row header that spans multiple columns becomes flat and ambiguous.

LlamaIndex’s proposed prompts extract a table with HTML `colspan` and `rowspan` attributes, which encode the full structure. The prompts ask the LLM to convert tables to HTML format (`<table>`, `<tr>`, `<th>`, `<td>`), and use `colspan` and `rowspan` attributes to preserve merged cells and hierarchical headers.

Similarly, for charts or graphs, the LLM is asked to convert them to tables using flat combined column headers so that the row of each data cell contains all its labels.

The paper proposes to use a shared system prompt for OpenAI and Claude models. For Google models, the user prompt is a bit different.

Here are LlamaParse’s proposed system and user prompts for OpenAI and Claude models that we will be using for building a reusable multimodal parser package.

```c
OPENAI_CLAUDE_SYSTEM_PROMPT = """You are a document parser. Your task is to convert document PDFs into clean, well-structured Markdown.

Guidelines:
- Preserve the document structure, including headings, paragraphs, lists, and tables.
- Convert tables to HTML using \`<table>\`, \`<tr>\`, \`<th>\`, and \`<td>\`.
- For existing tables in the document, use \`colspan\` and \`rowspan\` attributes to preserve merged cells and hierarchical headers.
- For charts or graphs converted into tables, use flat combined column headers (for example, "Primary 2015" instead of separate header rows) so that each data cell's row contains all of its labels.
- Describe images and figures briefly in square brackets, for example: \`[Figure: description]\`.
- Preserve any code blocks with appropriate syntax highlighting.
- Maintain reading order: left to right, top to bottom for Western documents.
- Do not add commentary or explanations. Output only the parsed content.

Additionally, wrap each layout element in a \`<div>\` tag with:
- \`data-bbox="[x1, y1, x2, y2]"\` for the bounding box in normalized 0-1000 coordinates, where x is horizontal (left edge = 0, right edge = 1000) and y is vertical (top = 0, bottom = 1000). \`x1, y1\` is the top-left corner and \`x2, y2\` is the bottom-right corner.
- \`data-label="<category>"\` where category is one of: \`Caption\`, \`Footnote\`, \`Formula\`, \`List-item\`, \`Page-footer\`, \`Page-header\`, \`Picture\`, \`Section-header\`, \`Table\`, \`Text\`, \`Title\`.

Place elements in reading order. Every piece of content must be inside exactly one \`<div>\` wrapper."""

OPENAI_CLAUDE_USER_PROMPT = """The attached PDF is read from the input folder next to this script.

Parse the full document and output its content as clean markdown, with each layout element wrapped in a <div data-bbox="[x1,y1,x2,y2]" data-label="Category"> tag. Use HTML tables for any tabular data. For charts and graphs, use flat combined column headers. Output ONLY the parsed content with div wrappers and no explanations.
"""
```

Google’s Gemini models use the same prompts, with the only difference that the `data-bbox` format is changed to their native coordinate order.

For Gemini models, the following system and user prompts are used:

```c
GOOGLE_SYSTEM_PROMPT = """You are a document parser. Your task is to convert document PDFs into clean, well-structured Markdown.

Guidelines:
- Preserve the document structure, including headings, paragraphs, lists, and tables.
- Convert tables to HTML using \`<table>\`, \`<tr>\`, \`<th>\`, and \`<td>\`.
- For existing tables in the document, use \`colspan\` and \`rowspan\` attributes to preserve merged cells and hierarchical headers.
- For charts or graphs converted into tables, use flat combined column headers (for example, "Primary 2015" instead of separate header rows) so that each data cell's row contains all of its labels.
- Describe images and figures briefly in square brackets, for example: \`[Figure: description]\`.
- Preserve any code blocks with appropriate syntax highlighting.
- Maintain reading order: left to right, top to bottom for Western documents.
- Do not add commentary or explanations. Output only the parsed content.

Additionally, wrap each layout element in a \`<div>\` tag with:
- \`data-bbox="[y_min, x_min, y_max, x_max]"\` for the bounding box in normalized 0-1000 coordinates where x is horizontal (left edge = 0, right edge = 1000) and y is vertical (top = 0, bottom = 1000). The order is \`[y_min, x_min, y_max, x_max]\`.
- \`data-label="<category>"\` where category is one of: \`Caption\`, \`Footnote\`, \`Formula\`, \`List-item\`, \`Page-footer\`, \`Page-header\`, \`Picture\`, \`Section-header\`, \`Table\`, \`Text\`, \`Title\`.

Place elements in reading order. Every piece of content must be inside exactly one \`<div>\` wrapper."""

GOOGLE_USER_PROMPT = """Parse this document page and output its content as clean markdown, with each layout element wrapped in a <div data-bbox="[y_min,x_min,y_max,x_max]" data-label="Category"> tag.
Use HTML tables for any tabular data. For charts/graphs, use flat combined column headers. Output ONLY the parsed content with div wrappers, no explanations.
"""
```

> Instead of Markdown tables that do not accurately represent merged cells, and messy real-world tables, the prompt asks for HTML tables with `colspan ` and `rowspan`. Every layout element gets a bounding box in normalized coordinates. This means downstream code can reconstruct the spatial layout of the page without depending on the original PDF renderer.

The Google prompts use a different bounding-box coordinate order (\[`y_min, x_min, y_max, x_max`\]) because that matches what Gemini models produce natively.

The parsing prompts are defined in GitHub’s `prompts.py` script.

## Multimodal Parser for Accurate Parsing

I packaged a parsing pipeline using the above-mentioned prompts into a Python class that reads a PDF document and lets the user select a provider and model (**OpenAI, Anthropic, or Google**) with several other options.

The full code structure is in the [**GitHub repository**](https://github.com/GAIK-project/gaik-toolkit/tree/main/implementation_layer/src/gaik/software_components/parsers/multimodal_parser). The complete implementation of the `MultimodalParser ` class is in `multimodal_parser.py`.

The `MultimodalParser` has just one method, `parse()`, that orchestrates the whole pipeline.

```c
parser = MultimodalParser(
    model_provider="google",
    model="gemini-3.1-flash-lite-preview",
    reasoning_effort="low",
    merge_table=True,
    create_html=True,
)
result = parser.parse("document.pdf")
```

A few parameters worth understanding:

- `reasoning_effort` — model’s thinking budget: `"low"`, `"medium"`, or `"high"`. Higher effort can improve accuracy on complex layouts, but is slower and costlier.
- `merge_table` — when `True`, appends an instruction to the user prompt telling the model to combine tables split across pages.
- `additional_instructions` — additional instructions appended to the user prompt for domain-specific rules.
- `create_html` — when `True`, renders the cleaned markdown into an HTML document.

The `parse()` method starts by reading the PDF as raw bytes and encoding it as a base64 string, so that it can be embedded in a JSON API payload and sent to the selected LLM with the aforementioned provider-specific prompts.

It then builds the right message structure based on the selected provider, because OpenAI, Claude, and Google each expect their content to be formatted differently.

After the LLM API call, the model returns its raw response, which is a combination of markdown text and `<div>` wrappers containing bounding box coordinates for every layout element on the page. A cleanup process removes any code block fences that the model may have wrapped the output in. Another method extracts the actual content from those `<div>` wrappers in the form of clean markdown.

If the option `create_html=True`, the clean markdown is converted into a styled HTML document that you can open directly in a browser to visually inspect the extraction.

**Every call returns a** `**UsageRecord**` **alongside the parsed content, which provides the details of token consumption and the associated cost.**

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*Sz0nQlFOr6vf9xDPQgvC5w.png)

The pipeline of the multimodal parser(image by author)

## How to Use It

The multimodal parser has been created as a reusable software component of our [GAIK project’s open-source generative AI toolkit](https://github.com/GAIK-project/gaik-toolkit/tree/main). This software component can be installed as a standalone Python package as follows:

```c
pip install "gaik[multimodal-parser]"
```

Here is a minimal example using `gemini-3.1-flash-lite-preview` with low reasoning efforts to parse the same purchase order. This example saves the parsing output in raw markdown, clean markdown, and an HTML format.

See a detailed example with token consumption and price calculation at [this link](https://github.com/GAIK-project/gaik-toolkit/blob/main/implementation_layer/examples/software_components/parsers/demo_multimodal_parser.py).

```c
from pathlib import Path
from dotenv import load_dotenv
from gaik.software_components.parsers.multimodal_parser import MultimodalParser

load_dotenv()

OUTPUT_DIR = Path(__file__).parent / "output"

def save_result(result, prefix: str) -> None:
    """Save parse results to the output directory."""
    OUTPUT_DIR.mkdir(parents=True, exist_ok=True)

    raw_path = OUTPUT_DIR / f"{prefix}_raw.md"
    raw_path.write_text(result.raw_markdown, encoding="utf-8")

    clean_path = OUTPUT_DIR / f"{prefix}_clean.md"
    clean_path.write_text(result.clean_markdown, encoding="utf-8")

    print(f"Saved: {raw_path}")
    print(f"Saved: {clean_path}")

    if result.html is not None:
        html_path = OUTPUT_DIR / f"{prefix}_clean.html"
        html_path.write_text(result.html, encoding="utf-8")
        print(f"Saved: {html_path}")

parser = MultimodalParser(
    model_provider="google",
    model="gemini-3.1-flash-lite-preview",
    reasoning_effort="low",
    merge_table=True,
    create_html=True,
)
result = parser.parse("sample_PO.pdf")
save_result(result, "output_google")
```

The output for the same purchase order, correctly merged and structured, is shown above (HTML format).

Here are a few more input-output examples.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*mkMoYkT4Km9wNCostLzSKg.png)

A table with a complex layout (image by author)

![](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*eWfor1ZdvVGZYCqSEp64OA.png)

The table parsed by gemini-3.1-flash-lite-preview with reasoning effort ‘low’ (image by author)

![](https://miro.medium.com/v2/resize:fit:1302/format:webp/1*v8h8WA_dSMRofyrx2_n7ww.png)

An example document having two charts (image by author)

![](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*nR-dQGTec7t03HCbeMoYog.png)

The two charts parsed by gemini-3.1-flash-lite-preview with reasoning effort ‘low’ (image by author)

## Observations & Final Thoughts

Even the smaller models, such as `gemini-3.1-flash-lite-preview` and `gpt-5.4-mini`, with `reasoning_effort ` set to low, extracted the messy purchase order accurately. It was all about using the right prompts.

==It should be noted that this parsing is useful where accuracy is more important than speed, and a fast or real-time response is not required. For instance, in purchase order processing, accurate parsing for accurate price calculation is more important than speed.==

Increasing the reasoning effort drastically increases the processing time and the cost. Bigger models, such as `gpt-5.4` with reasoning effort set to `high`, become awfully slow. Therefore, a “ `high` ” reasoning, especially for bigger models, should be used only for documents with highly complex layouts.

With respect to cost and speed, `gemini-3.1-flash-lite-preview` stands out as the best choice.

The `additional_instructions ` parameter can be used to supply use-case-specific parsing instructions. For instance, for legal documents, it can be set as “ *Preserve footnote numbering exactly as it appears in the source*.”

***I would be interested to know what document parsing problems you encounter. Can they be solved with this parsing method?***
