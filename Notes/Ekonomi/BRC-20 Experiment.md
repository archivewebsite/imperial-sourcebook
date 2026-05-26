# BRC-20 Experiment

## This document should be regarded as the definitive brc-20 white paper and will remain unaltered. For latest documentation and updates in the future, please refer to the following link.

[Documentation | Layer1 Foundationlayer1.gitbook.io](https://layer1.gitbook.io/layer1-foundation/protocols/brc-20/documentation)

---

This is just a fun experimental standard demonstrating that you can create off-chain balance states with inscriptions. It by no means should be considered THE standard for fungibility on bitcoin with ordinals, as I believe there are almost certainly better design choices and optimization improvements to be made. Consequently, this is an extremely dynamic experiment, and I strongly discourage any financial decisions to be made on the basis of it's design. I do, however, encourage the bitcoin community to tinker with standard designs and optimizations until a general consensus on best practices is met (or to decide that this is a bad idea altogether!).

 [![Logo](https://domo-2.gitbook.io/brc-20-experiment/~gitbook/imageurl=https%3A%2F%2Fmythbtc.xyz%2Fwp-content%2Fuploads%2F2023%2F02%2Fcentaur-logo-1-300x300.png&width=20&dpr=3&quality=100&sign=1d538d8e&sv=2) What are BRC-20 tokens on Bitcoin | Myth BTCMyth BTC](https://mythbtc.xyz/brc-20-token-standard-bitcoin/)

Must read summary of the experiment thus far. by [https://twitter.com/mythbtc](https://twitter.com/mythbtc)

Would also like to mention that the taproot enabled concept of issuing assets on the bitcoin blockchain is not novel, and Taro is unequivocally a better solution.

[Taproot Assets | Builder's Guidedocs.lightning.engineering](https://docs.lightning.engineering/the-lightning-network/taro)

## Idea

Experiment to see if ordinal theory can facilitate fungibility on bitcoin

- Create a brc-20 with the deploy function
- Mint an amount of brc-20's with the mint function
- Transfer an amount of brc-20's with the transfer function.

brc-20 balance state can be found by aggregating all of these function's activity together.

- Deployments initialize the brc-20. Do not affect state
- Mints provide a balance to **only the first owner** of the mint function inscription
- Transfers deduct from the senders balance and add to the receivers balance, **only upon the first transfer** of the transfer function. (1. Inscribe transfer function to senders address 2. **sender** **transfer's transfer function**)
![Drawing](https://domo-2.gitbook.io/brc-20-experiment/~gitbook/imageurl=https%3A%2F%2F2938770315-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FHkbayUy5sgqqrW99ijVE%252Fuploads%252FMjaQfwxzBGLOqYzxJ16N%252Ffile.excalidraw.svg%3Falt%3Dmedia%26token%3D103cb5e2-18f9-4ed5-a638-a9e188a64f4b&width=768&dpr=3&quality=100&sign=91bcb786&sv=2)

## Front end

Dune dashboard was meant for demo purposes only and is already broken/obsolete. Will keep live to demonstrate the logic required to determine state.

 [![Logo](https://domo-2.gitbook.io/brc-20-experiment/~gitbook/imageurl=https%3A%2F%2Fdune.com%2Fassets%2Fapple-touch-icon.png&width=20&dpr=3&quality=100&sign=9989061a&sv=2) ordinals brc-20 experiment | DuneDune](https://dune.com/domo/ordinals-brc-20-experiment)

In the meantime some marketplaces are inscription services are working on a functioning indexer. I will list solutions as they come online

- [https://unisat.io/brc20](https://unisat.io/brc20) (full balance state and explorer functionality)
- [https://unisat.io/searchq=&type=brc20&p=1](https://unisat.io/searchq=&type=brc20&p=1) (no state, search functionality only)
- [https://github.com/Next-DAO/brc20\_indexer](https://github.com/Next-DAO/brc20_indexer) (no state, ordi search functionality only)
- [https://brc-20.io/](https://brc-20.io/) (no state, list of coins only)

## How to

### Getting a balance

You can either deploy your own or mint from existing deployments bitcoin punks style

1. (**Optional: Only do if you want to create your own brc-20. If not go to step 2**) Inscribe the deploy function to you ordinal compatible wallet with the desired brc-20 parameters set.
2. Inscribe the mint function to your ordinal compatible wallet. Make sure the ticker matches either a) the brc-20 you deployed in step 1, or b) any brc-20 that has yet to reach its fully diluted supply. Also if the brc-20 has a mint limit, make sure not to surpass this. **Careful if using inscription service. Some tools inscribe to themselves first then forward it to the customer (thus the intermediate inscription service owned address keeps the balance)**

### Transferring a balance

1. Inscribe the transfer function to your ordinal compatible wallet. Make sure the transfer function inscription information is valid before inscribing. **Careful if using inscription service. Some tools inscribe to themselves first then forward it to the customer (thus because the intermediate inscription service owned address has no balance and the transfer function is wasted). Some ordinal wallets generate a different address each time, make sure to send to the address that holds the balance.**
2. Once received, (and if valid) send the inscription to the desired destination to transfer the balance.

#### What is valid

A valid transfer function is required to transfer a balance. Validity can be determined by the following:

- Valid transfer functions are ones where the amount stated in the inscription does not exceed **Available balance** when inscribed.
- **Available balance** defined as: \[**Overall balance**\] - \[valid/active transfer function inscriptions in wallet (**Transferable balance**)\]. If there are no valid/active transfer functions held by an address **Available balance** and **Overall balance** are equivalent.
- Example: A wallet holds an **Overall balance** of 1000 "ordi", and. The holder then inscribes a transfer function of 700 "ordi". Once the inscription is confirmed, the following is true: **Overall balance** = 1000, **Available balance** = 300, **Transferable balance** = 700. If in the next block, the user tried to inscribe a transfer function of 500 "ordi", this would not be valid as the maximum amount that can be inscribed is 300 (**Available balance**).
- If multiple transfer functions are inscribed in the same block, validity is determined by the order the were confirmed in the block.

#### Redundancies

- If a user changes their mind and no longer wishes to transfer their transfer function, and wants to restore their **Available balance** to the **Overall balance** (invalidate **Transferable balance**), the user must simply transfer the transfer function inscription to themselves.
![Drawing](https://domo-2.gitbook.io/brc-20-experiment/~gitbook/imageurl=https%3A%2F%2F2938770315-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FHkbayUy5sgqqrW99ijVE%252Fuploads%252Fh3tU2BtBBecH8bKWzmpZ%252Ffile.excalidraw.svg%3Falt%3Dmedia%26token%3D8cbf6af7-a7ef-4386-86fa-2a3e61c62376&width=768&dpr=3&quality=100&sign=c85c1c1f&sv=2)

(LEFT) The transfer of 700 "ordi" from sender to receiver (RIGHT) The restoration of overall balance via a self transfer of 700 "ordi". Only the balances marked in red are represented by inscriptions.

### Notes

- Do not send inscriptions to non ordinal compatible wallet taproot addresses
- It is unlikely that balances will be safely tradable using existing marketplace infrastructure. **Under no circumstances does the transfer of a mint function result in a balance change.**
- Each transfer inscription can only be used once
- The first deployment of a ticker is the only one that has claim to the ticker. Tickers are not case sensitive (DOGE = doge).
- If two events occur in the same block, prioritization is assigned via order they were confirmed in the block. (first to last).
- Minting transfer inscription to yourself first is necessary to avoid others spending your balance
- For public brc-20 mints the bitcoin punks /.sats names 'first is first' approach is adopted
- The mint function and the second step of the transfer function are the only events that cause changes in balances
- The first mint to exceed the maximum supply will receive the fraction that is valid. (ex. 21,000,000 maximum supply, 20,999,242 circulating supply, and 1000 mint inscription = 758 balance state applied)
- Mint function inscriptions do not have a padding requirement
- No valid action can occur via the spending of an ordinal via transaction fee. If it occurs during the inscription process then the resulting inscription is ignored. If it occurs during the second phase of the transfer process, the balance is returned to the senders available balance.
- Number of decimals cannot exceed 18 (default)
- Standard limited to uint128
- Maximum supply cannot exceed uint64\_max

## Operations

As I mentioned above, this is just my fun experimental standard design. I welcome anyone to improve upon the design, rules, or compression issues it poses. For traceability json {} are required, as well as the minimum required information to satisfy one of the functions.

### Deploy brc-20

**ordi used for demo purposes in the docs. It has already reached its max supply.**

```
{
  "p": "brc-20",
  "op": "deploy",
  "tick": "ordi",
  "max": "21000000",
  "lim": "1000"
}
```

Key

Required

Description

p

Yes

Protocol: Helps other systems identify and process brc-20 events

op

Yes

Operation: Type of event (Deploy, Mint, Transfer)

tick

Yes

Ticker: 4 letter identifier of the brc-20

max

Yes

Max supply: set max supply of the brc-20

lim

No

Mint limit: If letting users mint to themsleves, limit per ordinal

dec

No

Decimals: set decimal precision, default to 18

### Mint brc-20

**Careful if using inscription service. Some tools inscribe to themselves first then forward it to the customer (thus the intermediate inscription service owned address keeps the balance)**

```
{
  "p": "brc-20",
  "op": "mint",
  "tick": "ordi",
  "amt": "1000"
}
```

Key

Required

Description

p

Yes

Protocol: Helps other systems identify and process brc-20 events

op

Yes

Operation: Type of event (Deploy, Mint, Transfer)

tick

Yes

Ticker: 4 letter identifier of the brc-20

amt

Yes

Amount to mint: States the amount of the brc-20 to mint. Has to be less than "lim" above if stated

### Transfer brc-20

**Careful if using inscription service. Some tools inscribe to themselves first then forward it to the customer (thus because the intermediate inscription service owned address has no balance and the transfer function is wasted). Some ordinal wallets generate a different address each time, make sure to send to the address that holds the balance.**

```
{
  "p": "brc-20",
  "op": "transfer",
  "tick": "ordi",
  "amt": "100"
}
```

Key

Required

Description

p

Yes

Protocol: Helps other systems identify and process brc-20 events

op

Yes

Operation: Type of event (Deploy, Mint, Transfer)

tick

Yes

Ticker: 4 letter identifier of the brc-20

amt

Yes

Amount to transfer: States the amount of the brc-20 to transfer.

~~to~~

~~No~~

~~Address to send to: States the receiving address. If left blank logic will presume that the receiver of the transfer is correct.~~

~~fee~~

~~No~~

~~Transfer fee: For tracking without taproot data purposes only~~

***fee and to keys were for demo indexing purposes only. Inclusions have no effect on the function nor do they invalidate it.

Last updated
