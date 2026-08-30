# Module 1 — Crypto Fundamentals & Ecosystem

**Est. length:** 6 days (12 hours). Extend only if the Day 6 exit check shows real gaps — this is foundation, not filler.
**Prerequisite:** ICT Futures course (done). **Feeds into:** every later module — you cannot analyze BTC/ETH or vet a meme coin if you're shaky on what a wallet, a block, or a DEX actually is.

---

## 1. What You Need to Learn

What cryptocurrency is; Bitcoin; Ethereum; altcoins; stablecoins; coins vs. tokens; blockchain; smart contracts; decentralization; Layer 1 vs. Layer 2; gas; wallets; private keys; seed phrases; CEX vs. DEX; and, zooming out, how the Bitcoin ecosystem, Ethereum ecosystem, Solana/other-L1 ecosystems, liquidity pools, market makers, bridges, stablecoins, and DeFi all connect — i.e., how capital actually moves through crypto.

## 2. Why It Matters

You already know how to trade. You don't yet know what you're trading, where it lives, or how it moves between wallets/exchanges/chains. Skipping this because "I've traded futures for months" is exactly how people get their meme-coin wallet drained in Module 10+ — this module is what makes the security training in Module 13 make sense mechanically, not just as a checklist to memorize.

## 3. Foundational Concepts

**Cryptocurrency**, at its core, is a digital asset whose ownership record is secured by cryptography and kept on a distributed ledger — a database copied across thousands of independent computers — rather than sitting inside a single bank's or broker's private system. When you "own" 0.1 BTC, what actually exists is an entry on a public ledger saying that a particular cryptographic address controls 0.1 BTC, and a private key that lets you prove you're the one who can move it. Nobody at a company flips a switch to update your balance; the network of computers running the software agrees on the ledger's state collectively, using rules baked into the protocol. This is the single biggest conceptual shift coming from futures trading: in futures, a clearinghouse and a broker are the source of truth for your position. In crypto, for anything you hold in your own wallet, *the blockchain itself* is the source of truth, and no company can unilaterally alter it, freeze it, or reverse a transaction once it's confirmed. That's powerful, but it also means there's no "call support and reverse the trade" safety net — a theme that will come back constantly, especially once you reach wallet security in Module 2 and scam detection in Module 13.

**Blockchain** is the specific data structure that makes this possible. Transactions are grouped into batches called blocks; each new block contains a cryptographic fingerprint (a "hash") of the previous block, so the blocks form a chain where altering any historical block would break every hash after it — visibly, immediately, to anyone checking. Thousands of independent computers ("nodes") each keep their own full copy of this chain and independently verify every new block against the network's rules before accepting it. To secretly rewrite history, an attacker would need to out-compute (Bitcoin's proof-of-work) or out-stake (Ethereum's proof-of-stake) the majority of the entire honest network simultaneously — a cost that scales into the billions of dollars for BTC and ETH. That combination of transparency (anyone can inspect the whole ledger) and this "cost to cheat" is what people mean when they call blockchains "trustless": you don't have to trust a specific company's honesty, you have to trust that rewriting the ledger is economically and computationally infeasible. Keep this firmly in mind for later — it's exactly why on-chain data (Module 8, Module 14) is treated as verifiable fact in this course, while a claim on social media is not.

**Decentralization**, despite how it's marketed, is a spectrum rather than a yes/no property, and where a given network sits on that spectrum has real trading consequences. Bitcoin runs on tens of thousands of independently-operated full nodes with no single company controlling the software's direction in practice; Ethereum is similarly broad, with a large, geographically distributed set of validators. Many newer "Layer 1" blockchains, by contrast, run on a much smaller number of validators, often chosen or heavily influenced by the founding team. And the vast majority of individual meme-coin *tokens* you'll research later in this course are, practically speaking, controlled by a tiny handful of wallets — the deployer, a handful of early insiders — regardless of how decentralized the underlying chain they're built on happens to be. This distinction between "how decentralized is the blockchain" and "how decentralized is this specific token's ownership and control" is one you will apply directly and repeatedly once you reach the security and tokenomics work in Modules 12–13: a meme coin built on a highly decentralized chain like Solana can still be almost entirely controlled by one wallet.

**Coins versus tokens** is a distinction that sounds pedantic until you realize almost everything you'll trade as a meme-coin trader is a token, not a coin, and the difference changes what risks apply. A *coin* — Bitcoin, Ether, Solana's SOL — is the native asset of its own independent blockchain: it's what validators/miners are paid in, and it's what you pay network fees ("gas," covered below) with on that chain. A *token*, by contrast, is an asset that doesn't have its own blockchain or its own validators at all — it's a piece of code (a smart contract, covered in §4) deployed *on top of* someone else's blockchain, following a shared technical standard so that wallets and exchanges know how to display and move it. An ERC-20 token lives on Ethereum's rails; an SPL token lives on Solana's rails. This matters practically because a token inherits the *security* of its underlying chain (an SPL token can't be double-spent any more easily than SOL itself can) but does **not** inherit the underlying chain's decentralization of *ownership or control* — that's determined entirely by how the token's own contract and supply were set up, which is exactly what you'll learn to investigate starting in Module 12.

## 4. Beginner Concepts

**Bitcoin (BTC)**, launched in 2009, was designed to do one thing extremely well: be a scarce, verifiable, censorship-resistant store of value and settlement network, and nothing more ambitious than that. Its supply is hard-capped at 21 million coins, written into the protocol itself, and its scripting language is deliberately limited — it was not built to run arbitrary programs. This is a design choice, not a limitation someone forgot to fix: simplicity is precisely what has let Bitcoin run for over a decade with an unmatched security record and the deepest, most battle-tested decentralization of any blockchain. When people call BTC "digital gold," they're pointing at this same idea — a scarce asset whose main value proposition is being hard to debase and hard to seize, not a platform for building applications.

**Ethereum (ETH)** took the opposite bet: instead of optimizing purely for simplicity and scarcity, it built a general-purpose computing platform into the blockchain itself, via **smart contracts** — small programs that live on-chain and execute exactly as written whenever someone interacts with them, with no company in the loop to intervene. That one design decision is what makes almost everything else in this course possible: smart contracts are how tokens (including every meme coin) get created, how decentralized exchanges match trades without a company running an order book, how lending protocols let you borrow against crypto collateral, and how NFTs and countless other applications exist at all. Ethereum sacrifices some of Bitcoin's radical simplicity for this programmability, and in exchange became the foundational layer for the vast majority of what people mean today when they say "crypto" beyond Bitcoin itself.

**Altcoins** is simply the catch-all term for every cryptocurrency that isn't Bitcoin — it spans an enormous range, from major, well-established platforms like ETH and SOL, down through mid-sized utility tokens with real products, all the way to brand-new meme coins with no stated purpose beyond a joke and a community. Treating "altcoin" as one uniform risk category is a mistake this course will train you out of immediately: ETH and a two-hour-old meme coin are both technically "altcoins," but they could not be more different in liquidity, risk, or the kind of analysis that applies to them (a distinction fully developed in Module 10 §5).

**Stablecoins** — USDT (Tether), USDC (Circle), DAI, and others — are tokens engineered to hold a steady value, almost always pegged to one US dollar. USDT and USDC do this by holding real-world reserves (cash and cash-equivalents) roughly matching the tokens in circulation; DAI does it by over-collateralization — users lock a surplus of other crypto assets into a smart contract, with algorithmic mechanisms (stability fees, automated liquidations) keeping the peg rather than a bank-held dollar reserve. This is a meaningfully different — and generally more battle-tested — design than the "algorithmic stablecoin" label sometimes gets used for: it's not the same category as an uncollateralized, seigniorage-style design (the kind behind TerraUSD/UST's 2022 collapse), which relies on market confidence alone with no hard collateral backing it at all. Functionally, stablecoins are the "cash" layer of the crypto economy: when you want to sit out of the market without converting back to your bank account, you hold a stablecoin; when a meme coin's liquidity pool is described as "$50,000 in liquidity," that pool is very often paired against a stablecoin (or against ETH/SOL) rather than sitting as a pool of the meme coin alone. You'll rely on this constantly once you reach market mechanics in Module 3.

**Smart contracts**, introduced above, deserve one more precise point: because the code runs exactly as deployed, whoever controls what gets deployed controls the rules — permanently, unless the contract's creator specifically built in an ability to change things later (an "admin function" or "owner privilege"). A contract with no such backdoor is trustworthy in the sense that nobody, including its creator, can secretly change how it behaves. A contract that *does* retain owner privileges (the ability to mint new tokens, freeze wallets, or change fees) concentrates real power in whoever holds that admin key — which is precisely the mechanism behind several of the scam patterns you'll learn to detect in Module 13. Reading whether a contract retains these privileges is a checkable, factual exercise, not a guess — you'll practice it directly starting in Module 12.

**Layer 1 (L1)** refers to a base, independent blockchain — Bitcoin, Ethereum, and Solana are each their own L1, with their own validators and their own security guarantees. **Layer 2 (L2)** networks — Arbitrum, Base, and Optimism are the most prominent examples built on Ethereum — process transactions more cheaply and quickly than the underlying L1 could alone, while still periodically committing a compressed record of their activity back to the L1, inheriting its security rather than building an independent, from-scratch trust model. The practical effect for you as a trader is that a huge amount of everyday crypto activity (swaps, DeFi use, smaller transfers) now happens on L2s specifically because L1 transaction fees, especially on Ethereum during busy periods, can be prohibitively expensive for small transactions.

**Gas** is the fee paid to the network for processing a transaction, priced in the chain's native coin — ETH on Ethereum, SOL on Solana. Gas isn't a fixed price list; it functions like an auction for limited block space, so gas costs rise sharply when many people are trying to transact at once. This is directly relevant to your meme-coin work ahead: a hot new token launch on Ethereum can spike gas fees network-wide as everyone tries to buy in the same few minutes, and understanding this mechanically (rather than being surprised by it) is part of trading meme coins competently rather than naively.

**A wallet** is software (sometimes paired with dedicated hardware) that generates and stores your **private keys** and uses them to digitally sign transactions, proving to the network that you authorized a given transfer. This is worth internalizing precisely because the common mental model — "my wallet holds my coins" — is technically wrong in a way that matters: your balance is a fact recorded on the blockchain itself, not a number stored inside the wallet app. The wallet's actual job is narrower and more important than "storage": it holds the cryptographic secret that lets you prove ownership and authorize movement of that balance. Lose the wallet app but keep the key material, and you can fully recover access from any compatible wallet software; lose the key material with no backup, and the funds are provably, permanently unreachable by anyone — including you.

**Private keys and seed phrases** are the practical form that key material takes. The private key is the actual secret number that mathematically controls a given address; a **seed phrase** — typically 12 or 24 specific words, generated in a specific standardized way — is a human-typeable backup from which every private key in that wallet can be regenerated. This single fact is the most operationally important thing in this entire module: **whoever possesses your seed phrase has complete, irreversible control of every asset it protects, with no company, court, or support line able to undo a transfer made with it.** There is no password-reset flow, because there is no central party to reset it with. Every wallet-security practice you'll learn in Module 2, and every phishing/drainer pattern you'll learn to recognize in Module 13, exists because of this one property. Claude will never ask you for a seed phrase or private key, under any circumstance, for any reason — and neither should any legitimate wallet support channel, ever, after initial setup.

**CEX (centralized exchange)** and **DEX (decentralized exchange)** represent the two fundamentally different ways to trade crypto, and the difference maps directly onto the trust-model distinction from §3. A CEX — Luno, VALR, Binance, Kraken — is a company: you deposit funds into their custody, and they maintain an internal order book matching buyers and sellers, functioning much like a traditional brokerage. You're trusting that company's solvency, security, and honesty, exactly as you'd trust a broker holding your futures margin. A DEX — Uniswap, Raydium, Jupiter — is not a company holding your funds at all; it's a smart contract that lets you swap one token for another directly from your own self-custody wallet, using the liquidity-pool mechanism (fully explained in §5) instead of a company-run order book. Nobody at a DEX can freeze your account, but nobody at a DEX can reverse a mistake or refund a scam either — the trade-offs run in both directions, and professional traders understand both models rather than treating one as simply "safer." In concrete terms: only a CEX can convert your ZAR into crypto in the first place (the fiat on/off-ramp, gated by the KYC process covered in Module 2) or hold funds in a way a court order could freeze; only a DEX can let you swap a token the moment it launches, with no listing process, company approval, or waiting period — which is exactly why meme-coin trading, starting in Module 10, happens almost entirely on DEXs.

## 5. Intermediate Concepts

**How the Bitcoin ecosystem fits together** starts with the base layer itself: a deliberately slow, roughly ten-minute-per-block network optimized for final, irreversible settlement rather than speed. Around that base layer sit exchanges, which provide the fiat on-ramp and off-ramp most people actually use to acquire and sell BTC; the Lightning Network, a Layer 2 built specifically to make small, fast, cheap Bitcoin payments practical without touching the base layer for every transaction; and, more recently, custodians and exchange-traded funds that give institutional and retail investors exposure to BTC without directly managing private keys themselves. Notice what's conspicuously absent from this picture: Bitcoin has essentially no native "DeFi" layer of lending protocols, decentralized exchanges, or yield products, and that's not an oversight — it's the direct consequence of the simplicity-over-programmability design choice covered in §4.

**How the Ethereum ecosystem fits together** looks structurally different specifically because of Ethereum's programmability. The base layer settles final transactions and secures the whole system; Layer 2 networks like Arbitrum, Base, and Optimism handle the bulk of everyday cheap activity while periodically checkpointing back to the base layer; decentralized exchanges like Uniswap let anyone swap tokens without a company running the order book; lending protocols like Aave let people borrow and lend crypto assets peer-to-pool rather than peer-to-bank; major stablecoins like USDC and DAI live and circulate primarily in this ecosystem; and on top of all of that sit the tokens themselves — everything from serious utility projects to, historically, a large share of meme coins, though that center of gravity has shifted (see below). Every layer here ultimately depends on Ethereum's base-layer security, even when the actual activity happens on an L2 or inside a token's own smart contract.

**How the Solana ecosystem fits together** matters disproportionately for your meme-coin specialization specifically because of Solana's technical profile: sub-second blocks and transaction fees measured in fractions of a cent, versus Ethereum's comparatively slower and pricier base layer. On top of this fast, cheap base layer sit decentralized exchanges like Raydium and Orca, and — critically for your later modules — launch platforms built specifically for creating new tokens quickly and cheaply, the mechanism behind the overwhelming majority of new meme-coin activity today. This is a direct, mechanical cause-and-effect relationship, not a trend that happened by coincidence: when creating a token and trading it costs fractions of a cent and settles in under a second, a completely different scale and speed of speculative token creation becomes viable than would ever be economical on a slower, pricier base layer. You will spend a great deal of time inside this specific ecosystem starting in Module 10.

**Liquidity pools** are the mechanism that makes DEX trading possible without a company-run order book, and understanding them precisely now will make Module 3's market-mechanics work and Module 13's scam-detection work land far more easily later. Instead of matching a specific buyer to a specific seller, a DEX pool holds a reserve of two assets — say, a meme-coin token and SOL — supplied by liquidity providers, and prices trades algorithmically based on the changing ratio between those two reserves as people buy and sell (this pricing mechanism is called an "automated market maker," or AMM). The practical consequence is that trading against a *small* pool moves the price far more than trading against a large one, because your trade itself changes the ratio significantly — this effect is called **slippage**, and it is the single most important mechanical fact behind why meme coins are so volatile, why an early buyer's small purchase can spike a price so dramatically, and why a rug pull (Module 13) is even possible in the first place: whoever supplied the pool's liquidity can, in many cases, withdraw it, collapsing the price toward zero in one action.

**Market makers**, in the broader sense, are whoever or whatever provides that continuous buy/sell liquidity so trading can happen without huge price gaps between what a buyer wants to pay and a seller wants to receive — on a CEX this might be a dedicated trading firm running automated quotes on the order book; on a DEX, the liquidity pool itself plays this role, with the liquidity providers effectively acting as the market maker collectively.

**Bridges** are protocols or services that move an asset — or, more precisely, a representation of that asset — from one blockchain to another, since a coin native to one chain can't natively exist on a different chain's ledger. Practically, this usually works by locking the original asset on its home chain and minting a corresponding "wrapped" version on the destination chain. It's worth stating plainly, not as scaremongering but as an documented pattern: bridges, because they concentrate large amounts of locked value behind a relatively narrow piece of code, have historically been among the most frequently and severely hacked components in all of crypto. That's a real, checkable risk factor to weigh whenever a strategy or a token depends on bridged assets.

**DeFi (decentralized finance)** is the umbrella term for the whole category of lending, borrowing, trading, and yield-generating protocols built as smart contracts rather than run by banks or brokerages — Aave and Uniswap are both DeFi protocols, in the lending and trading categories respectively. You don't need deep DeFi expertise for this course's BTC/ETH/meme-coin focus, but recognizing the term and roughly where a given protocol fits will come up repeatedly, especially in Module 8's on-chain data and Module 9's narrative work.

## 6. Advanced Concepts

**Trust-model differences** between CEXs and DEXs are worth stating explicitly, because the honest answer is that neither is categorically "safer" — they carry genuinely different risk profiles that professional traders manage differently rather than avoid. On a CEX, you are exposed to counterparty risk: the company could be mismanaged, insolvent, hacked, or outright fraudulent, and your funds are only as safe as that company's operations and honesty (the collapse of the exchange FTX is the reference case study here — a company that appeared reputable and was, in fact, misusing customer funds). On a DEX or in self-custody, you eliminate that specific counterparty risk but take on smart-contract risk (the code itself could contain an exploitable bug) and, more commonly in practice, personal operational-security risk (a phishing site, a malicious approval, a lost seed phrase). The right professional stance is not "DEXs are safer" or "CEXs are safer" — it's understanding which specific risks you're accepting at any given moment and managing each of them deliberately.

**Why the degree of decentralization matters to a trader, concretely, and not just as an ideological talking point**, comes down to a simple mechanical fact you introduced yourself to in §3: a token whose ownership and contract control are highly concentrated in a small number of wallets can have its liquidity withdrawn or its supply altered unilaterally, at any moment, by whoever holds that control — regardless of how healthy the chart looks a minute before it happens. This isn't an abstract risk to note and move past; it is a specific, checkable, and quantifiable input you will weigh on every single meme-coin decision from Module 12 onward, using real on-chain data rather than a gut feeling about how "legitimate" a project seems.

**The custody spectrum**, laid out end to end, runs from a CEX's custodial wallet (most convenient, most counterparty risk) through a CEX's own "earn" or staking products (still fundamentally their custody, regardless of the yield being offered) to a self-custody hot wallet — a browser extension or mobile app like MetaMask or Phantom, where you hold the keys but they exist on an internet-connected device — and finally to a self-custody hardware wallet, where the private key is generated and stored on a dedicated offline device that never exposes the key to an internet-connected computer even when signing a transaction. Moving along this spectrum trades convenience for security in a fairly linear way: hacks and phishing risk fall as you move toward hardware custody, while everyday usability falls at the same time. Serious traders typically use more than one tier deliberately — a hot wallet for active, smaller-value trading activity, and colder storage for anything they intend to hold rather than actively trade — and you'll set up this same layered approach yourself in Module 2.

**Why capital "rotates"** through the crypto market in a fairly predictable general sequence is a pattern you will use directly once you reach cycles and narratives in Module 9, so it's worth planting the seed here. Stablecoins function as the system's parking spot — cash sitting on the sidelines, ready to deploy without leaving the crypto ecosystem entirely. As risk appetite rises, capital has historically tended to flow first into Bitcoin (as the largest, most liquid, most "trusted" asset), then into Ethereum and other large-cap assets, then further out into smaller altcoins, and finally, at the riskiest and most speculative edge of that spectrum, into meme coins — with the entire sequence reversing as risk appetite falls and capital retreats back toward stablecoins and BTC. This is a general historical tendency to weigh as evidence, not a mechanical law that repeats identically every cycle — and learning to tell the difference between "this tendency is currently playing out" and "I'm assuming it must be happening" is exactly the kind of evidence-based judgment this whole course is built to train.

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
