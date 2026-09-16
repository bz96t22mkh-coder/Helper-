# Module 1 — Crypto Fundamentals & Ecosystem

**Est. length:** 6 days (12 hours). Extend only if the Day 6 exit check shows real gaps — this is foundation, not filler.
**Prerequisite:** ICT Futures course (done). **Feeds into:** every later module — you cannot analyze BTC/ETH or vet a meme coin if you're shaky on what a wallet, a block, or a DEX actually is.

---

## 1. What You Need to Learn

What cryptocurrency is; Bitcoin; Ethereum; altcoins; stablecoins; coins vs. tokens; blockchain; smart contracts; decentralization; Layer 1 vs. Layer 2; gas; wallets; private keys; seed phrases; CEX vs. DEX; and, zooming out, how the Bitcoin ecosystem, Ethereum ecosystem, Solana/other-L1 ecosystems, liquidity pools, market makers, bridges, stablecoins, and DeFi all connect — i.e., how capital actually moves through crypto.

## 2. Why It Matters

You already know how to trade. You don't yet know what you're trading, where it lives, or how it moves between wallets/exchanges/chains. Skipping this because "I've traded futures for months" is how people get their meme-coin wallet drained in Module 10+ — this module is what makes the security training in Module 13 click mechanically, not just as a checklist.

## 3. Foundational Concepts

**Cryptocurrency** is a digital asset whose ownership record is secured by cryptography and kept on a distributed ledger — a database copied across thousands of independent computers — rather than a single bank's or broker's private system. When you "own" 0.1 BTC, what exists is an entry on a public ledger saying an address controls it, plus a private key proving you can move it. Nobody at a company updates your balance; the network agrees on the ledger's state collectively, by protocol rules. This is the biggest conceptual shift from futures trading: there, a clearinghouse and broker are the source of truth for your position; in crypto, *the blockchain itself* is — no company can alter, freeze, or reverse a confirmed transaction. That power comes with no "call support and reverse the trade" safety net, a theme you'll meet again in wallet security (Module 2) and scam detection (Module 13).

**Blockchain** is the data structure that makes this possible. Transactions are grouped into blocks; each block contains a cryptographic "hash" of the previous one, so altering any historical block breaks every hash after it — visibly, to anyone checking. Thousands of independent "nodes" each keep a full copy of the chain and verify every new block against the network's rules before accepting it. To secretly rewrite history, an attacker would need to out-compute (Bitcoin's proof-of-work) or out-stake (Ethereum's proof-of-stake) the majority of the honest network at once — a cost scaling into the billions. That combination of transparency and cost-to-cheat is what "trustless" means: you trust that rewriting the ledger is too costly and impractical, not a company's honesty — why on-chain data (Module 8, Module 14) counts as verifiable fact here, while a social-media claim doesn't.

**Decentralization**, despite how it's marketed, is a spectrum, not a yes/no property, and where a network sits on it has real trading consequences. Bitcoin runs on tens of thousands of independently-operated nodes with no company controlling its direction; Ethereum is similarly broad. Many newer "Layer 1" chains run on far fewer validators, often influenced by the founding team. Most meme-coin *tokens* you'll research later are, practically, controlled by a handful of wallets — the deployer and early insiders — regardless of the underlying chain's decentralization. That distinction, blockchain decentralization versus token ownership, is one you'll apply directly in Modules 12–13: a meme coin on a decentralized chain like Solana can still be almost entirely controlled by one wallet.

**Coins versus tokens** sounds pedantic until you realize almost everything you'll trade as a meme-coin trader is a token, not a coin. A *coin* — Bitcoin, Ether, Solana's SOL — is the native asset of its own blockchain: what validators/miners are paid in, and what you pay gas with. A *token* has no blockchain or validators of its own — it's code (a smart contract, §4) deployed on top of someone else's chain, following a shared standard so wallets and exchanges know how to display and move it. An ERC-20 token lives on Ethereum's rails; an SPL token on Solana's. A token inherits the *security* of its chain (an SPL token can't be double-spent any more easily than SOL itself) but does **not** inherit its decentralization of *ownership or control* — that's set entirely by the token's own contract and supply, which you'll learn to investigate starting in Module 12.

## 4. Beginner Concepts

**Bitcoin (BTC)**, launched in 2009, was designed to do one thing well: be a scarce, verifiable, censorship-resistant store of value and settlement network. Its supply is hard-capped at 21 million coins, written into the protocol, and its scripting language is deliberately limited — not built to run arbitrary programs. That's a design choice: simplicity is what has let Bitcoin run for over a decade with an unmatched security record and the deepest, most battle-tested decentralization of any blockchain. "Digital gold" points at the same idea — a scarce asset that's hard to debase or seize, not a platform for building applications.

**Ethereum (ETH)** took the opposite bet: instead of optimizing for simplicity and scarcity, it built a general-purpose computing platform into the blockchain itself, via **smart contracts** — programs that live on-chain and execute exactly as written, with no company able to intervene. That one decision makes almost everything else in this course possible: smart contracts are how tokens (including every meme coin) get created, how decentralized exchanges match trades without a company running an order book, how lending protocols let you borrow against crypto collateral, and how NFTs and countless other applications exist at all. Ethereum trades some of Bitcoin's radical simplicity for this programmability, becoming the foundational layer for most of what people mean by "crypto" beyond Bitcoin.

**Altcoins** is the catch-all term for every cryptocurrency that isn't Bitcoin — everything from major platforms like ETH and SOL through mid-sized utility tokens to brand-new meme coins with no stated purpose beyond a joke and a community. Treating "altcoin" as one uniform risk category is a mistake this course trains you out of immediately: ETH and a two-hour-old meme coin are both technically "altcoins," but they couldn't be more different in liquidity, risk, or the analysis that applies (Module 10 §5).

**Stablecoins** — USDT (Tether), USDC (Circle), DAI, and others — are tokens engineered to hold a steady value, almost always pegged to one US dollar. USDT and USDC hold real-world reserves roughly matching circulation; DAI uses over-collateralization — users lock a surplus of other crypto into a smart contract, with algorithmic mechanisms keeping the peg instead of a bank-held reserve. This is meaningfully more battle-tested than an uncollateralized design relying on market confidence alone (the kind behind TerraUSD/UST's 2022 collapse). Stablecoins are the "cash" layer of crypto: you hold one to sit out of the market, and a meme coin's "$50,000 in liquidity" pool is often paired against a stablecoin (or ETH/SOL) rather than the meme coin alone.

**Smart contracts**, introduced above, deserve one more point: because the code runs exactly as deployed, whoever controls what gets deployed controls the rules permanently, unless the creator built in an ability to change things later (an "admin function" or "owner privilege"). A contract with no such backdoor is trustworthy in that nobody, including its creator, can secretly change how it behaves. One that *does* retain owner privileges (minting new tokens, freezing wallets, changing fees) concentrates real power in whoever holds that key — the mechanism behind several scam patterns in Module 13. Checking whether a contract retains these privileges is a factual exercise you'll practice starting in Module 12.

**Layer 1 (L1)** is a base, independent blockchain — Bitcoin, Ethereum, and Solana are each their own, with their own validators and security guarantees. **Layer 2 (L2)** networks — Arbitrum, Base, and Optimism are the most prominent, built on Ethereum — process transactions more cheaply and quickly than the L1 alone, periodically committing a compressed record of activity back to it, inheriting its security rather than building an independent trust model. A huge amount of everyday crypto activity now happens on L2s because L1 fees, especially on Ethereum during busy periods, can be prohibitively expensive for small transactions.

**Gas** is the fee paid to the network for processing a transaction, priced in the chain's native coin — ETH on Ethereum, SOL on Solana. Gas functions like an auction for limited block space, so costs rise sharply when many people transact at once. A hot token launch on Ethereum can spike gas network-wide as everyone buys in the same few minutes — understanding this mechanically is part of trading meme coins competently.

**A wallet** is software (sometimes paired with hardware) that generates and stores your **private keys** and signs transactions, proving to the network you authorized a transfer. The common mental model — "my wallet holds my coins" — is technically wrong: your balance is a fact recorded on the blockchain, not a number in the app. The wallet's real job is narrower: it holds the secret that lets you prove ownership and authorize movement of that balance. Lose the app but keep the key material, and you can recover access from any compatible wallet; lose the key material with no backup, and the funds are permanently unreachable by anyone — including you.

**Private keys and seed phrases** are the practical form key material takes. The private key is the secret number that mathematically controls an address; a **seed phrase** — typically 12 or 24 words, generated in a standardized way — is a human-typeable backup from which every private key in that wallet can be regenerated. This is the most operationally important fact in this module: **whoever possesses your seed phrase has complete, irreversible control of every asset it protects, with no company, court, or support line able to undo a transfer made with it.** There is no password-reset flow, because there is no central party to reset it with. Every wallet-security practice in Module 2, and every phishing/drainer pattern in Module 13, exists because of this one property. Claude will never ask you for a seed phrase or private key, under any circumstance — and neither should any legitimate wallet support channel, ever, after initial setup.

**CEX (centralized exchange)** and **DEX (decentralized exchange)** are the two fundamentally different ways to trade crypto, mapping onto the trust-model distinction from §3. A CEX — Luno, VALR, Binance, Kraken — is a company: you deposit funds into their custody, and they match buyers and sellers on an internal order book, trusting their solvency and honesty as you would a futures broker. A DEX — Uniswap, Raydium, Jupiter — isn't a company holding your funds; it's a smart contract letting you swap tokens directly from your own wallet, using the liquidity-pool mechanism (§5) instead of an order book. Nobody at a DEX can freeze your account, but nobody can reverse a mistake or refund a scam either. Only a CEX can convert ZAR into crypto (gated by KYC, Module 2) or hold funds a court order could freeze; only a DEX lets you swap a token the moment it launches, with no listing process — why meme-coin trading, from Module 10, happens almost entirely on DEXs.

## 5. Intermediate Concepts

**How the Bitcoin ecosystem fits together** starts with the base layer: a deliberately slow, roughly ten-minute-per-block network optimized for final, irreversible settlement over speed. Around it sit exchanges, providing the fiat on/off-ramp most people use to acquire and sell BTC; the Lightning Network, a Layer 2 built for small, fast, cheap payments without touching the base layer each time; and, more recently, custodians and ETFs giving investors exposure to BTC without managing private keys. Notice what's missing: Bitcoin has essentially no native "DeFi" layer of lending, exchanges, or yield products — not an oversight, but the direct consequence of the simplicity-over-programmability choice from §4.

**How the Ethereum ecosystem fits together** looks structurally different because of Ethereum's programmability. The base layer settles transactions and secures the system; Layer 2s like Arbitrum, Base, and Optimism handle everyday cheap activity while periodically checkpointing back to it; DEXs like Uniswap let anyone swap tokens without a company order book; lending protocols like Aave let people borrow and lend peer-to-pool; major stablecoins like USDC and DAI circulate primarily here; and on top sit the tokens themselves — from serious utility projects to, historically, a large share of meme coins, though that's shifted (see below). Every layer depends on Ethereum's base-layer security, even when activity happens on an L2 or inside a token's own contract.

**How the Solana ecosystem fits together** matters disproportionately for your meme-coin specialization because of Solana's technical profile: sub-second blocks and fees measured in fractions of a cent, versus Ethereum's slower, pricier base layer. On top sit DEXs like Raydium and Orca, and — critically for later modules — launch platforms built for creating tokens quickly and cheaply, the mechanism behind most new meme-coin activity today. This is direct cause and effect: when creating and trading a token costs fractions of a cent and settles in under a second, a different scale and speed of speculative token creation becomes viable than on a slower, pricier chain. You'll spend a great deal of time here from Module 10.

**Liquidity pools** are the mechanism that makes DEX trading possible without an order book, and understanding them now helps Module 3's market mechanics and Module 13's scam detection land more easily. A DEX pool holds a reserve of two assets — say, a meme-coin token and SOL — supplied by liquidity providers, pricing trades off the changing ratio between reserves as people buy and sell (an "automated market maker," or AMM). Trading against a *small* pool moves price far more than against a large one, since your trade itself shifts the ratio — this is **slippage**, the key fact behind why meme coins are so volatile and why a rug pull (Module 13) is possible at all: whoever supplied the liquidity can often withdraw it, collapsing the price toward zero in one action.

**Market makers**, broadly, are whoever provides the continuous buy/sell liquidity that keeps prices from gapping between what a buyer will pay and a seller will accept — on a CEX, often a dedicated trading firm running automated quotes; on a DEX, the liquidity pool itself, with providers collectively acting as market maker.

**Bridges** move an asset — or, more precisely, a representation of it — from one blockchain to another, since a coin native to one chain can't exist on another's ledger. This usually works by locking the original asset on its home chain and minting a "wrapped" version on the destination chain. As a documented pattern, not scaremongering: bridges, concentrating large amounts of locked value behind a narrow piece of code, have historically been among the most frequently and severely hacked components in crypto — a real, checkable risk whenever a strategy or token depends on bridged assets.

**DeFi (decentralized finance)** is the umbrella term for lending, borrowing, trading, and yield-generating protocols built as smart contracts rather than run by banks or brokerages — Aave and Uniswap are both DeFi protocols, in the lending and trading categories respectively. You don't need deep DeFi expertise for this course's BTC/ETH/meme-coin focus, but recognizing the term will come up again in Module 8's on-chain data and Module 9's narrative work.

## 6. Advanced Concepts

**Trust-model differences** between CEXs and DEXs matter because neither is categorically "safer" — they carry different risk profiles professional traders manage rather than avoid. On a CEX you're exposed to counterparty risk: the company could be mismanaged, insolvent, hacked, or fraudulent (FTX is the reference case — a company that appeared reputable but was misusing customer funds). On a DEX or in self-custody, you eliminate that counterparty risk but take on smart-contract risk (an exploitable bug) and, more commonly, operational-security risk (a phishing site, a malicious approval, a lost seed phrase). The right stance isn't "DEXs are safer" or "CEXs are safer" — it's knowing which risks you're accepting and managing each deliberately.

**Why the degree of decentralization matters to a trader**, concretely, comes down to a fact from §3: a token whose ownership and contract control are highly concentrated in a small number of wallets can have its liquidity withdrawn or supply altered unilaterally, at any moment — regardless of how healthy the chart looked a minute before. It's a specific, checkable input you'll weigh on every meme-coin decision from Module 12 onward, using real on-chain data rather than a gut feeling about "legitimacy."

**The custody spectrum** runs from a CEX's custodial wallet (most convenient, most counterparty risk) through its "earn"/staking products (still its custody, regardless of yield) to a self-custody hot wallet — a browser extension or app like MetaMask or Phantom, keys on an internet-connected device — and finally a hardware wallet, where the key is generated and stored offline, never touching an internet-connected computer even when signing. This trades convenience for security fairly linearly: hacks and phishing risk fall toward hardware custody, usability falls with it. Serious traders use more than one tier — a hot wallet for active trading, colder storage for anything held longer-term — and you'll set this up in Module 2.

**Why capital "rotates"** through the crypto market in a fairly predictable sequence is a pattern you'll use directly in cycles and narratives (Module 9). Stablecoins function as the system's parking spot — cash on the sidelines, ready to deploy without leaving crypto. As risk appetite rises, capital has historically flowed first into Bitcoin (the largest, most "trusted" asset), then Ethereum and other large-caps, then smaller altcoins, and finally meme coins at the riskiest edge — reversing as risk appetite falls. This is a general tendency to weigh as evidence, not a law — telling "this is playing out" from "I'm assuming it must be" is the evidence-based judgment this course trains.

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
