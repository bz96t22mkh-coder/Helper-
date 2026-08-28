# Module 12 — Meme-Coin Token & Tokenomics Analysis

**Est. length:** 3 days (6 hours).
**Prerequisite:** Modules 3, 10–11. **Feeds into:** Module 13 (security builds directly on contract/ownership checks here), Module 15 (framework's validation stage).

---

## 1. What You Need to Learn

How to analyze a meme coin's fundamentals *before* considering a trade: market cap, FDV, supply, liquidity, volume (review/application of Module 3), holder distribution, top/developer/insider wallets, wallet concentration, token ownership, liquidity providers, liquidity lock/burn, contract ownership and permissions, trading activity and buy/sell behavior, token age, and community/narrative/social growth (application of Module 11).

## 2. Why It Matters

This is the analytical core of "validation" in your six-step pipeline (Module 10 §6). A token can have a perfect chart and a viral narrative and still be catastrophically unsafe to buy because of what's underneath — this module teaches you to see that.

## 3. Market Cap, FDV, Supply, Liquidity, Volume — Applied

You built the underlying concepts in Module 3 — market capitalization, fully diluted valuation, circulating vs. max supply, liquidity, and volume. Here, the goal is to apply each of them specifically to the meme-coin context, where they tend to interact in ways that are more extreme, and more dangerous if missed, than in more established markets.

**Market cap and liquidity, always computed together,** is the single habit most likely to save you from a specific, common meme-coin trap. Market cap tells you the *notional* value of the entire token supply at the current price; liquidity tells you how much capital is actually sitting in the trading pool available to absorb buys and sells without moving price sharply. A token can display an eye-catching $10 million market cap while its liquidity pool holds only $20,000 — meaning the "market cap" is almost entirely theoretical, since anyone trying to actually sell a meaningful position would crash the price long before realizing anything close to that valuation. This is a common, deliberately exploited pattern: a small amount of real capital, combined with a token's supply math, can produce a market-cap figure that looks impressive on a screener while the underlying market is dangerously thin (Module 3 §5 covers the mechanics of why thin liquidity amplifies price moves in both directions). Flagging any token where liquidity is a small fraction of stated market cap should be an automatic, unconditional habit, not a judgment call you make case by case.

**FDV versus market cap** turns on a fact that's specific to how most meme coins are launched: the overwhelming majority mint 100% of their total supply at launch, with no team allocation and no vesting schedule held back for later release. When that's true, fully diluted valuation and market cap are the same number, because there's no additional locked supply waiting to enter circulation — so the FDV-vs-market-cap gap that matters so much for many other crypto projects (where a large team/investor allocation unlocks gradually and can flood the market later) simply doesn't apply. But not every meme coin follows this pattern — some do allocate a team or insider portion on a vesting schedule, exactly like more conventional token launches — and when that's the case, the question changes from "is there a gap" to "exactly when does that locked supply unlock, and how large is it relative to current liquidity?" A team unlock hitting the market on a specific future date is a known, checkable event that can crash price on its own, independent of anything else happening with the project, which is precisely the kind of fact your Module 15 framework needs on the calendar before it happens, not after.

**Volume relative to liquidity and token age** is where the two prior checks combine into an actual diagnostic question. A token that's only three days old showing daily trading volume that's several multiples of its entire liquidity pool size is doing something unusual — that ratio doesn't happen by accident in a market with only organic participants, because normally a liquidity pool that small would only support that much volume by having price swing wildly on every trade. There are exactly two realistic explanations: the token is going genuinely, explosively viral, with a wave of new participants each buying and pushing volume far beyond what the pool's size would predict, or the volume is heavily wash-traded — an entity trading with itself or coordinated wallets purely to manufacture the appearance of interest (Module 3 §6 introduces the concept; Module 13 §4 covers it as a deliberate manipulation pattern). Market cap, liquidity, and volume numbers alone cannot tell these two explanations apart — a wash-traded token and a genuinely viral one can produce an identical volume-to-liquidity ratio. Telling them apart requires looking *underneath* the aggregate numbers to the wallet-level behavior generating them, which is exactly what Section 4's holder and wallet analysis is for.

## 4. Holder & Wallet Analysis

**Holder distribution** — the percentage of total token supply held by the top 10, top 20, and top 50 wallets, visible directly on the block explorer or through a visualization tool like Bubblemaps — is one of the most direct measurements of concentration risk you can take. The underlying logic is simple: if a handful of wallets control a large share of supply, then a single decision by one of those wallets (or a small coordinated group of them) can move price dramatically regardless of what every other, smaller holder does. A token where the top 10 wallets hold 15% of supply behaves very differently under stress than one where they hold 70% — in the second case, the token's price is effectively hostage to the intentions of a handful of addresses you can't see inside, and "the community is bullish" says very little about whether that concentrated group is about to sell.

**The developer/deployer wallet** — the address that actually deployed the token's contract and, typically, created the initial liquidity pool — deserves individual scrutiny beyond the aggregate concentration number, because this specific wallet usually has more information and more structural power than any other holder. Check its current holdings (has it kept its original allocation, or already reduced it?), its full transaction history (has it sold off significant amounts already, and if so, when relative to price action?), and whether it retains any special privileges baked into the contract itself — a question Section 5 develops in full. A developer wallet that's already sold down a large share of its holdings while the token's public narrative is still "the team is fully committed" is a direct, checkable contradiction worth weighting heavily.

**Insider and early wallets** — addresses that acquired a large position very early, either before public trading opened or heavily concentrated in the first few minutes after it did — are visible by looking directly at a token's earliest transactions on the block explorer, and they matter because early access at a de facto lower cost basis creates an asymmetric incentive to sell into whatever demand shows up later. A single early wallet isn't necessarily a red flag on its own — someone has to be first — but a *cluster* of wallets that are all similar in size, all created around the same time, and all entering in the same narrow window is a strong signal of intentional bundling: supply distributed across multiple addresses specifically to obscure how concentrated the real ownership actually is. Modules 13 and 14 build directly on this observation, using Bubblemaps-style cluster visualization to make bundled wallets visible even when their addresses look unrelated on the surface.

**Wallet concentration over time** matters as much as any single snapshot, because concentration is a trend, not a fixed fact, and the direction of that trend tells you something a snapshot alone cannot. Concentration that's *decreasing* over time — the top holders' share of supply shrinking as new, independent buyers enter — is consistent with organic distribution and a genuinely growing holder base. Concentration that's *increasing* — insiders quietly accumulating a larger share even as headline holder counts grow — is consistent with a small group positioning to control the token's price action more tightly, often ahead of a coordinated sell. Checking the same holder-distribution numbers again a few days or a week after your first look, rather than relying on a single point-in-time read, is a small habit that catches this.

**Liquidity providers** — whoever supplied the capital sitting in the DEX trading pool — matter because of one specific, binary question: is that liquidity **locked** (committed via a smart contract for a fixed time period, mechanically impossible to withdraw early no matter who wants to), **burned** (the LP tokens representing ownership of the pool sent to a dead address that no one controls, making withdrawal permanently impossible for anyone), or **neither** — meaning the deployer retains the ability to withdraw some or all of that liquidity at will, whenever they choose? This third state is the direct mechanical precondition for the most common and most devastating meme-coin scam, the rug pull, which Module 13 covers in full: if the liquidity can be pulled, at some point it may be, and everyone still holding the token at that moment is left with an asset that can no longer be sold for anything close to its prior price. Checking LP lock/burn status is not one item among many equally weighted checks — it is close to a precondition for considering a token investable at all.

## 5. Contract Ownership & Permissions

**Contract ownership** is the first and most structural question: has ownership of the token's smart contract been **renounced** — meaning no one, including the original deployer, retains the ability to call the contract's privileged functions anymore, ever — or is ownership still actively held by a wallet? Renunciation is a one-way, on-chain, publicly verifiable action; you're not taking anyone's word for it, you're checking the contract's own state directly. A contract still owned by a live wallet isn't automatically a scam — plenty of legitimate projects retain ownership temporarily for operational reasons — but it does mean every privileged capability described below is still a live possibility for as long as that ownership persists, which makes the *specific permissions* that ownership grants the next, non-optional thing to check.

**Contract permissions to check specifically** break down into three categories, each with a distinct failure mode. **Mint authority** is the ability to create new tokens out of thin air after launch — if an owner retains this and exercises it, the total supply increases without warning, diluting every existing holder's share and, in the worst cases, letting the owner mint a huge new batch and dump it directly into the market. **Freeze/blacklist authority** is the ability for the contract owner to block specific wallets from selling their tokens at all — this is the exact mechanism behind a "honeypot" (developed further in Module 13 §3): buying works normally, drawing in buyers, but selling is silently restricted for everyone except a pre-approved list, typically the deployer's own wallets. **Fee/tax modification authority** is the ability to change the buy or sell tax percentage after launch, sometimes with no upper limit — an owner can leave the tax at a normal 2-3% while accumulating trust, then suddenly set the sell tax to 99%, which doesn't technically prevent anyone from selling but makes doing so financially pointless, trapping holders' capital just as effectively as an outright freeze. Each of these three permissions being *present and not renounced* is a specific, material, checkable risk — not a vague "this could theoretically be bad," but a concrete capability sitting in the contract's code right now that you can verify directly, which is exactly why Module 13 turns this section into a hard, no-exceptions checklist item rather than a soft consideration.

## 6. Trading Activity, Age & Community/Narrative Synthesis

- **Trading/buy-sell behavior:** the ratio and pattern of buy vs. sell transactions over time, and whether large sells are coming from top/insider wallets specifically (visible on the explorer) — distinguishing broad organic distribution from a small number of large holders exiting into retail buying.
- **Age of token:** newer tokens carry categorically higher risk (less time for the community/liquidity/contract behavior to prove out) but also the potential for the earliest, largest moves — age is a risk-and-opportunity dial, not a pass/fail filter by itself.
- **Community, narrative, social growth:** apply Module 11's tools directly here — genuine, diversifying engagement growth vs. manufactured/bot-driven growth, and whether the token's narrative fits a currently strong sector theme (Module 9).

## 7. Practical Exercises

- Take one real, currently-active meme coin (ideally one from your Module 10 discovery log) and produce a complete token-analysis writeup covering every item in §3–6: market cap, liquidity, FDV, top-10/20 holder %, developer wallet behavior, LP lock/burn status, contract ownership/permissions, buy/sell pattern, age, and a brief community/narrative note.
- Do the same for a second token, and compare: which one shows a materially safer fundamental profile, independent of chart appearance?

## 8. Drills

- **Red-flag count drill:** given a hypothetical token's full data profile (concentration %, LP status, contract permissions), count how many of the "hard" red flags from §4–5 are present.
- **FDV-parity drill:** given hypothetical circulating and max supply numbers, determine whether FDV materially exceeds market cap and what that would imply.

## 9. Real-World Applications

- This writeup format becomes the standard "Token Analysis" section of your Module 16 meme-coin research journal, and a mandatory gate before Module 15's trade-setup stage.

## 10. Challenges

- Find one real token that looks appealing on its chart/narrative but fails badly on at least 2 of this module's fundamental checks, and write exactly why you would reject it despite the attractive chart.

## 11. Assessments

**Baseline (Day 50):** Before instruction, what would you currently check about a meme coin before buying it, beyond "the chart looks good"?

**Exit (Day 52):** Produce a complete token-analysis writeup on a real, currently-active meme coin, covering every item in §3–6, and correctly identify whether it passes or fails a first-pass fundamental screen, with reasoning.

## 12. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | Judges tokens by chart/narrative alone, unaware of holder/contract risk |
| Developing | Knows the checklist items but produces incomplete or shallow writeups |
| Competent | Produces a complete, accurate token-analysis writeup unprompted |
| Advanced | Spots a hidden red flag (e.g., unrenounced mint authority) that a chart gives no hint of |
| Highly Proficient | Runs this analysis quickly and reliably as a standard pre-trade habit |
| Mastery | Could teach someone else to see through an attractive chart to real fundamental risk |

You need **Competent** to move to Module 13.

---

## 13. Day-by-Day Training Plan

### Day 50 — Market Cap, FDV, Supply, Liquidity, Volume Applied to Meme Coins (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 10 | Write what you'd currently check before buying a meme coin (Section 11). |
| Lesson | 30 | Read §3: market cap/liquidity/FDV/volume applied specifically to meme coins. |
| Practical | 60 | Pick one real trending token and compute market cap, liquidity, FDV, and volume-to-liquidity ratio; flag anything disproportionate. |
| Review/journal | 20 | Explain, from memory, why "100% circulating at launch" changes the FDV question. |

### Day 51 — Holder/Wallet Analysis, Liquidity Lock, Contract Permissions (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's liquidity/FDV findings. |
| Lesson | 40 | Read §4–5: holder distribution, dev/insider wallets, LP lock/burn, contract ownership/permissions. |
| Practical | 50 | On the same token, check top-10/20 holder %, developer wallet history, LP lock/burn status, and contract ownership/permissions using your Module 2 tools (explorer + RugCheck/GoPlus). |
| Review/journal | 20 | Do the Section 8 red-flag count drill using today's real findings. |

### Day 52 — Trading Behavior, Age, Community Synthesis & Exit Assessment (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's red-flag count. |
| Lesson | 20 | Read §6: buy/sell behavior, token age, community/narrative synthesis. |
| Practical | 40 | Complete the full writeup for today's token, adding buy/sell pattern, age, and community/narrative notes (using Module 11 tools). |
| Exit assessment | 40 | Produce a complete second writeup (Section 11 exit task) on a fresh token, live. |
| Reflection | 10 | Write the Section 10 challenge answer. |

**If below Competent:** Day 53 repeats the full writeup on a fresh token with closer feedback on whichever section (holder analysis, contract permissions, etc.) was weakest. **If Competent+:** move to Module 13 — Meme-Coin Security & Scam Detection.
