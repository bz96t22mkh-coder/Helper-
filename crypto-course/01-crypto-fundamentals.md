# Module 1 — Crypto Fundamentals & Ecosystem

**Est. length:** 6 days (12 hours). Extend only if the Day 6 exit check shows real gaps — this is foundation, not filler.
**Prerequisite:** ICT Futures course (done). **Feeds into:** every later module — you cannot analyze BTC/ETH or vet a meme coin if you're shaky on what a wallet, a block, or a DEX actually is.

---

## 1. What You Need to Learn

What cryptocurrency is; Bitcoin; Ethereum; altcoins; stablecoins; coins vs. tokens; blockchain; smart contracts; decentralization; Layer 1 vs. Layer 2; gas; transactions; wallets; private keys; seed phrases; CEX vs. DEX; and, zooming out, how the Bitcoin ecosystem, Ethereum ecosystem, Solana/other-L1 ecosystems, liquidity pools, market makers, bridges, stablecoins, and DeFi all connect — i.e., how capital actually moves through crypto.

## 2. Why It Matters

You already know how to trade. You don't yet know what you're trading, where it lives, or how it moves between wallets/exchanges/chains. Skipping this because "I've traded futures for months" is exactly how people get their meme-coin wallet drained in Module 10+ — this module is what makes the security training in Module 13 make sense mechanically, not just as a checklist to memorize.

## 3. Foundational Concepts

- **Cryptocurrency** is a digital asset secured by cryptography and recorded on a distributed ledger (a blockchain) instead of a central bank/broker's database. No single party can unilaterally edit the ledger.
- **Blockchain**: a chain of blocks, each containing a batch of transactions, each block cryptographically linked to the previous one (via a hash), replicated across thousands of independent computers (nodes). To rewrite history you'd need to out-compute/out-stake the entire honest network — that's what makes it "trustless."
- **Decentralization** is a spectrum, not a binary. Bitcoin (~15,000+ full nodes) and Ethereum are highly decentralized; many "Layer 1" chains and nearly all meme coins are far more centralized in practice (small validator sets, a handful of wallets holding most tokens) — this matters enormously once you get to Module 13.
- **Coins vs. tokens:** a *coin* (BTC, ETH, SOL) is the native asset of its own blockchain, used to pay that chain's transaction fees. A *token* is an asset built *on top of* someone else's blockchain using a smart-contract standard (e.g., an ERC-20 token on Ethereum, an SPL token on Solana) — it doesn't have its own chain or validators. Nearly every meme coin you will research is a **token**, not a coin.

## 4. Beginner Concepts

- **Bitcoin (BTC):** the first cryptocurrency (2009), a fixed-supply (21M cap), simple, deliberately non-programmable "digital gold" / settlement asset. No smart contracts in the general sense.
- **Ethereum (ETH):** a programmable blockchain — smart contracts (self-executing code with rules coded in) let anyone build tokens, DEXs, lending protocols, NFTs, and (relevantly for you) meme coins on top of it.
- **Altcoins:** everything that isn't BTC — includes major L1s (ETH, SOL, etc.), utility tokens, and meme coins.
- **Stablecoins** (USDT, USDC, DAI): tokens designed to hold ~$1 value, usually backed by real-dollar reserves (USDT/USDC) or over-collateralized crypto (DAI). They're your "cash" inside crypto — most trading pairs and meme-coin liquidity pools are priced against a stablecoin or against ETH/SOL.
- **Smart contract:** code deployed on a blockchain that runs exactly as written, with no ability for one party to change the rules after the fact (unless the contract itself was coded with an admin backdoor — a huge red flag you'll learn to check for in Module 13).
- **Layer 1 (L1):** a base blockchain (Bitcoin, Ethereum, Solana). **Layer 2 (L2):** a network built on top of an L1 to make it cheaper/faster (Arbitrum, Base, Optimism sit on Ethereum) while still settling back to the L1 for security.
- **Gas:** the fee paid to the network to process a transaction, denominated in the chain's native coin (ETH for Ethereum, SOL for Solana). Gas spikes when the network is busy — directly relevant to meme-coin launches, which cause exactly that.
- **Wallet:** software (or hardware) that holds your **private keys** and lets you sign transactions. A wallet does not "store coins" the way a physical wallet stores cash — your balance lives on the blockchain; the wallet just proves you control it.
- **Private key / seed phrase:** the private key is the actual cryptographic secret that controls your funds. The **seed phrase** (12–24 words) is a human-readable backup that can regenerate every private key in that wallet. **Whoever has your seed phrase has your funds — permanently, irreversibly, with no customer support to call.** Claude will never ask for either.
- **CEX (centralized exchange):** a company (Luno, VALR, Binance, Kraken) that holds custody of your funds and matches buyers/sellers on an internal order book — like a broker. **DEX (decentralized exchange):** a smart contract (Uniswap, Raydium, Jupiter) that lets you swap tokens directly from your own wallet, with no company holding your funds, using liquidity pools instead of an order book.

## 5. Intermediate Concepts

- **How the Bitcoin ecosystem fits together:** BTC base layer (slow, ~10 min blocks, final settlement) → exchanges (fiat on/off-ramp) → Lightning Network (a Layer 2 for fast/cheap payments) → custodians/ETFs (institutional access). BTC has almost no on-chain "DeFi" — it's intentionally simple.
- **How the Ethereum ecosystem fits together:** ETH base layer → L2s (Arbitrum, Base, Optimism — cheaper execution) → DEXs (Uniswap) → lending protocols (Aave) → stablecoins (USDC/DAI live here) → NFTs and tokens (including most meme coins historically, though Solana now dominates meme-coin volume). Everything ultimately settles back to Ethereum's base layer for security.
- **How the Solana ecosystem fits together (you'll need this heavily for meme coins):** SOL base layer (fast, sub-second blocks, cheap fees) → DEXs (Raydium, Orca, Pump.fun-style launch platforms) → this low-fee, high-speed environment is *why* the majority of active meme-coin launches and trading now happen on Solana rather than Ethereum.
- **Liquidity pools:** instead of matching a buyer to a seller (order book), a DEX pool holds two assets (e.g., TOKEN + SOL) supplied by liquidity providers; price is set algorithmically by the ratio of the two assets in the pool (an "automated market maker" / AMM). Trading against a thin pool causes large **slippage** — the price you actually get moves against you as your trade size eats into the pool. This is *the* central mechanic behind meme-coin volatility and rug pulls (Module 13).
- **Market makers:** entities (on CEXs) or algorithms/pools (on DEXs) that provide continuous buy/sell liquidity so trades can execute without huge price gaps.
- **Bridges:** protocols/services that move an asset (or a wrapped representation of it) from one chain to another. Bridges are historically one of the most-hacked parts of crypto — a fact, not a scare tactic.
- **DeFi (decentralized finance):** the umbrella term for lending, borrowing, trading, and yield protocols built from smart contracts instead of banks/brokers.

## 6. Advanced Concepts

- **Trust model differences:** on a CEX, you trust a company (counterparty risk — see FTX). On a DEX/self-custody wallet, you trust code and yourself (smart-contract risk + your own operational security). Neither is strictly "safer" — they carry *different* risks, and professional traders manage both.
- **Why decentralization degree matters to a trader, not just an ideologue:** a highly centralized token (few holders, mutable contract, unlocked admin functions) can have its liquidity pulled or its supply changed by one wallet at any time — this is a trading-relevant risk factor you will price into every meme-coin decision, not an abstract philosophical point.
- **The custody spectrum in practice:** CEX custodial wallet → CEX-hosted "Earn"/staking (still their custody) → self-custody hot wallet (browser extension, e.g. MetaMask/Phantom) → self-custody hardware wallet (private key never touches an internet-connected device). Your risk of hacks/phishing decreases as you move right; your convenience decreases too. You'll set up more than one tier in Module 2.
- **Why capital "rotates":** stablecoins are the parking spot; capital flows stablecoin → BTC → ETH/large-caps → altcoins → meme coins as risk appetite rises, and reverses under stress. You'll use this rotation logic directly in Module 9 (cycles/narratives).

## 7. Practical Exercises

- **Draw the money map:** starting from "I get paid in ZAR," sketch (on paper or in notes) every hop needed to end up holding SOL in a self-custody wallet — bank → CEX (fiat on-ramp) → buy SOL → withdraw to self-custody wallet. Label each hop with what kind of custody/risk it carries.
- **Coin-or-token quiz (self-check):** for BTC, ETH, SOL, USDT, and one meme coin you've heard of (e.g., DOGE, or whatever's trending — don't trade it, just classify it), write down: coin or token? Which chain does it live on/settle to?
- **CEX vs. DEX comparison table:** list 3 things you'd only be able to do on a CEX and 3 you'd only be able to do on a DEX.

## 8. Drills

- **Terminology flashcards:** write your own 1-sentence definitions (no copy-paste) for: blockchain, smart contract, gas, private key, seed phrase, L1, L2, stablecoin, liquidity pool, bridge — then re-explain each out loud in under 15 seconds, Feynman-style, from memory.
- **"Explain it to past-you" drill:** explain why a seed phrase is *not* like a bank password (no reset, no support line, fully bearer-instrument) in 2–3 sentences, as if to someone who's never touched crypto.

## 9. Real-World Applications

- Everything in Module 2 (choosing a CEX, setting up a wallet) only makes sense once you can explain *why* each step exists — you're not following instructions blindly, you understand the custody model behind each click.
- Every meme-coin safety check in Module 13 ("check if the contract has an admin function," "check liquidity pool lock") is a direct application of §6's centralization/trust-model concepts.

## 10. Challenges

- Without looking anything up, explain to yourself why Bitcoin doesn't have "DeFi" the way Ethereum does, and why that's a deliberate design choice, not a missing feature.
- Pick one real meme coin currently trending (research only, don't trade) and identify: what chain is it on, is it a coin or a token, and what DEX would you need to swap it on?

## 11. Assessments

**Baseline (Day 1, before instruction):** Without looking anything up, write 3–5 sentences on what you currently believe cryptocurrency is and how buying/selling it works. This isn't graded — it's so you (and Claude) can see what's already correct vs. what needs correcting.

**Exit (Day 6):** Explain, from memory, in under 5 minutes total: (1) the difference between a coin and a token, with one real example of each; (2) what a private key/seed phrase actually is and why no one — including Claude — should ever ask for it; (3) the difference between a CEX and a DEX, including one thing only each can do; (4) how the Bitcoin, Ethereum, and Solana ecosystems each fit together at a high level. Send your explanation for evaluation.

## 12. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | Confuses coins/tokens, CEX/DEX, or thinks a wallet "stores" crypto like a bank account |
| Developing | Gets definitions right with prompting, still shaky on ecosystem connections |
| Competent | Explains all Day 6 exit points correctly, unprompted, with correct examples |
| Advanced | Can correctly classify an unfamiliar asset (coin/token, which chain, custody implications) on sight |
| Highly Proficient | Applies ecosystem/custody reasoning automatically when evaluating new tools/platforms in later modules |
| Mastery | Could onboard someone else from zero safely, including explaining *why* each safety rule exists |

You need **Competent** to move to Module 2.

---

## 13. Day-by-Day Training Plan

### Day 1 — What Exactly Is Cryptocurrency? (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline check | 15 | Write your Section 11 baseline (what you currently believe crypto is). |
| Lesson | 40 | Read §3–4 above: cryptocurrency, blockchain, decentralization, coins vs. tokens, BTC, ETH, altcoins, stablecoins, smart contracts. |
| Practical: money map | 25 | Do the Section 7 "money map" exercise (ZAR → CEX → self-custody wallet), labeling custody type at each hop. |
| Practical: coin-or-token quiz | 20 | Classify BTC, ETH, SOL, USDT, and one meme coin (Section 7). |
| Review/journal | 20 | Write 5 flashcard definitions (Section 8) from memory, no notes. |

**Today's objective:** replace "crypto is confusing" with a correct mental model of what it actually is.
**What you must record:** baseline paragraph, money map, coin/token quiz answers, 5 definitions.
**Mastery check:** can you explain, out loud, why Bitcoin and a meme-coin token are fundamentally different kinds of assets?
**After today you should be able to:** correctly use the words coin, token, blockchain, and decentralization without mixing them up.

### Day 2 — Wallets, Keys, and Custody (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall-test yesterday's 5 definitions from memory before checking. |
| Lesson | 40 | Read §4–6: wallets, private keys, seed phrases, CEX vs. DEX, custody spectrum (custodial → hot self-custody → hardware). |
| Exercise | 30 | Write, in your own words, exactly what would happen (step by step) if you lost your seed phrase, and separately, if someone else obtained it. |
| Exercise | 20 | List 3 things only a CEX can do and 3 things only a DEX can do (Section 7). |
| Review/journal | 20 | Explain "a wallet doesn't store your coins" to an imagined beginner in 3 sentences. |

**Today's objective:** internalize that custody = risk model, before you ever touch real funds in Module 2.
**What you must record:** the "lost seed phrase" scenario writeup, CEX/DEX list, custody explanation.
**Mastery check:** can you state, without hesitation, why Claude will never ask for your seed phrase?
**After today you should be able to:** correctly explain the custody spectrum and why each tier trades convenience for security.

### Day 3 — Smart Contracts, Gas, L1 vs. L2 (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall-test the custody spectrum from memory. |
| Lesson | 40 | Read §4–5: smart contracts, gas, L1 vs. L2, liquidity pools/AMMs basics. |
| Exercise | 30 | Explain in your own words how an AMM sets price using pool ratios (no formula needed yet — the concept) and why a thin pool causes bad slippage. |
| Exercise | 20 | List 2 L2s and explain, in one sentence each, why they exist (cheaper/faster than the L1 they settle to). |
| Review/journal | 20 | Write the one-sentence version of "what is gas and why does it spike." |

**Today's objective:** understand the mechanical "why" behind meme-coin volatility before you ever look at a meme-coin chart.
**What you must record:** AMM/slippage explanation, L2 list, gas explanation.
**Mastery check:** can you explain why a $50 buy on a $2,000 liquidity pool moves price dramatically, but the same $50 buy on a $2,000,000 pool barely moves it?
**After today you should be able to:** connect "thin liquidity" to "high volatility" as cause and effect, not just as a vibe.

### Day 4 — The Bitcoin & Ethereum Ecosystems (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall-test gas/AMM/slippage from Day 3. |
| Lesson | 45 | Read §5: how the Bitcoin ecosystem fits together (base layer, Lightning, custodians), how the Ethereum ecosystem fits together (base layer, L2s, DEXs, lending, stablecoins, tokens). |
| Exercise | 30 | Draw (text or diagram) the Bitcoin ecosystem map and the Ethereum ecosystem map, each showing at least 4 layers/components and how money/assets move between them. |
| Review/journal | 35 | Write 4–5 sentences comparing why Bitcoin deliberately has no DeFi layer while Ethereum was built specifically to support one. |

**Today's objective:** see BTC and ETH not as "two coins" but as two different kinds of systems with different design philosophies.
**What you must record:** both ecosystem maps, the BTC-vs-ETH design-philosophy writeup.
**Mastery check:** can you explain what problem Ethereum's smart contracts solve that Bitcoin's design intentionally avoids?
**After today you should be able to:** explain both ecosystems to someone else without notes.

### Day 5 — The Solana Ecosystem, DeFi, Bridges & Stablecoins (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall-test the BTC/ETH ecosystem maps. |
| Lesson | 40 | Read §5–6: Solana ecosystem, why meme coins concentrate there, DeFi umbrella, bridges and bridge risk, stablecoins as crypto's "cash." |
| Exercise | 30 | Draw the Solana ecosystem map (base layer, DEXs/launch platforms, why fees/speed matter for meme coins). |
| Exercise | 20 | Write 3 sentences on why bridges are historically high-risk, using the trust-model concept from §6. |
| Review/journal | 20 | Explain, in 2–3 sentences, why a stablecoin is the "parking spot" capital rotates through. |

**Today's objective:** understand *why* Solana is where most meme-coin activity happens — you'll live in this ecosystem from Module 10 onward.
**What you must record:** Solana ecosystem map, bridge-risk writeup, stablecoin-rotation writeup.
**Mastery check:** can you explain, unprompted, why low fees + fast blocks on Solana specifically enable the meme-coin launch pattern?
**After today you should be able to:** explain all three major ecosystems (BTC, ETH, SOL) and how capital/assets move within and between them.

### Day 6 — Exit Assessment & Integration (2h)

| Segment | Min | What to do |
|---|---|---|
| Warm-up recall | 10 | Quick recall-dump of all three ecosystem maps. |
| Exit assessment | 50 | Complete the Section 11 exit task in full: coin vs. token with examples; private key/seed phrase explanation; CEX vs. DEX with one unique capability each; all three ecosystems at a high level. Write it out or describe how you'd say it. |
| Evaluation | — | Sent for scoring against the Section 12 mastery table: repeat, extend, or progress to Module 2. |
| Challenge task | 30 | Do the Section 10 challenge: classify one real trending meme coin (chain, coin/token, which DEX) — research only, no trade. |
| Reflection | 30 | Write what's still fuzzy, if anything, and what clicked hardest today. |

**Today's objective:** prove you can operate with correct crypto fundamentals without hand-holding before touching real money or real tools.
**What you must record:** full exit-assessment answers, the meme-coin classification, your reflection.
**Mastery check:** Competent-level performance on all 4 exit-assessment points.
**After today you should be able to:** move into Module 2 (real exchange/wallet setup) understanding exactly what you're doing and why, at every step.

**If exit assessment lands below Competent:** Day 7 repeats the weakest 1–2 concepts with a fresh example and a harder self-test before moving on. **If Competent+:** move to Module 2.
