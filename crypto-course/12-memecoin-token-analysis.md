# Module 12 — Meme-Coin Token & Tokenomics Analysis

**Est. length:** 3 days (6 hours).
**Prerequisite:** Modules 3, 10–11. **Feeds into:** Module 13 (security builds directly on contract/ownership checks here), Module 15 (framework's validation stage).

---

## 1. What You Need to Learn

How to analyze a meme coin's fundamentals *before* considering a trade: market cap, FDV, supply, liquidity, volume (review/application of Module 3), holder distribution, top/developer/insider wallets, wallet concentration, token ownership, liquidity providers, liquidity lock/burn, contract ownership and permissions, trading activity and buy/sell behavior, token age, and community/narrative/social growth (application of Module 11).

## 2. Why It Matters

This is the analytical core of "validation" in your six-step pipeline (Module 10 §6). A token can have a perfect chart and a viral narrative and still be catastrophically unsafe to buy because of what's underneath — this module teaches you to see that.

## 3. Market Cap, FDV, Supply, Liquidity, Volume — Applied

You built the underlying concepts in Module 3 — market capitalization, fully diluted valuation, circulating vs. max supply, liquidity, and volume. Here, apply each to the meme-coin context, where they interact in ways more extreme, and more dangerous if missed, than in established markets.

**Market cap and liquidity, always computed together,** is the single habit most likely to save you from a common meme-coin trap. Market cap tells you the *notional* value of the entire supply at the current price; liquidity tells you how much capital sits in the trading pool to absorb buys and sells without moving price sharply. A token can display an eye-catching $10 million market cap while its liquidity pool holds only $20,000 — the "market cap" is almost entirely theoretical, since selling a meaningful position would crash the price long before realizing that valuation. This is a common, deliberately exploited pattern: a small amount of real capital, combined with a token's supply math, can produce a market-cap figure that looks impressive while the underlying market is dangerously thin (Module 3 §5 covers why). Flag any token where liquidity is a small fraction of stated market cap automatically — it's not a case-by-case judgment call.

**FDV versus market cap** turns on a fact specific to how most meme coins are launched: the overwhelming majority mint 100% of their total supply at launch, with no team allocation or vesting schedule held back for later release. When that's true, FDV and market cap are the same number, since no additional locked supply is waiting to enter circulation — the FDV-vs-market-cap gap that matters for other crypto projects (where a large team/investor allocation unlocks gradually and can flood the market later) simply doesn't apply. But not every meme coin follows this pattern: some allocate a team or insider portion on a vesting schedule, like more conventional launches. When that's the case, the question changes from "is there a gap" to "when does that locked supply unlock, and how large is it relative to current liquidity?" A team unlock landing on a specific date is a known, checkable event that can crash price on its own — the fact your Module 15 framework needs on the calendar.

**Volume relative to liquidity and token age** is where the two prior checks combine into a diagnostic question. A token only three days old showing daily volume several multiples of its entire liquidity pool is doing something unusual — that ratio doesn't happen by accident with only organic participants, since a pool that small would otherwise need wild price swings to support that volume. There are two realistic explanations: the token is going explosively viral, with new participants pushing volume far beyond what the pool's size predicts, or the volume is heavily wash-traded — an entity trading with itself or coordinated wallets purely to manufacture the appearance of interest (Module 3 §6 introduces the concept; Module 13 §4 covers it as a manipulation pattern). Market cap, liquidity, and volume alone cannot tell these explanations apart — a wash-traded token and a genuinely viral one can produce an identical ratio. Telling them apart means looking *underneath* the aggregate numbers to wallet-level behavior — what Section 4's analysis is for.

## 4. Holder & Wallet Analysis

**Holder distribution** — the percentage of total supply held by the top 10, top 20, and top 50 wallets, visible on the block explorer or a tool like Bubblemaps — is one of the most direct measurements of concentration risk you can take. If a handful of wallets control a large share of supply, a single decision by one of them (or a small coordinated group) can move price dramatically regardless of what every other holder does. A token where the top 10 wallets hold 15% of supply behaves very differently under stress than one where they hold 70% — in the second case, price is effectively hostage to a handful of addresses you can't see inside, and "the community is bullish" says little about whether that group is about to sell.

**The developer/deployer wallet** — the address that deployed the contract and, typically, created the initial liquidity pool — deserves individual scrutiny, since it usually has more information and power than any other holder. Check its current holdings (kept the original allocation, or reduced?), its transaction history (sold off amounts, and when relative to price?), and whether it retains special privileges in the contract — a question Section 5 develops. A developer wallet already sold down while the narrative is still "the team is fully committed" is a direct, checkable contradiction worth weighting heavily.

**Insider and early wallets** — addresses that acquired a large position very early, before public trading opened or in the first few minutes after — are visible in a token's earliest transactions on the block explorer, and matter because a lower cost basis creates an asymmetric incentive to sell into later demand. A single early wallet isn't necessarily a red flag — someone has to be first — but a *cluster* of wallets similar in size, created around the same time, entering the same narrow window, signals intentional bundling: supply spread across addresses to obscure how concentrated real ownership is. Modules 13 and 14 build on this, using Bubblemaps-style cluster visualization to make bundled wallets visible even when addresses look unrelated.

**Wallet concentration over time** matters as much as any single snapshot, since concentration is a trend, and its direction tells you something a snapshot can't. Concentration that's *decreasing* — top holders' share shrinking as independent buyers enter — is consistent with organic distribution. Concentration that's *increasing* — insiders quietly accumulating a larger share even as holder counts grow — suggests a small group positioning to control price action, often ahead of a coordinated sell. Checking the same numbers again a week later, rather than one point-in-time read, catches this.

**Liquidity providers** — whoever supplied the capital sitting in the DEX trading pool — matter because of one binary question: is that liquidity locked, burned, or neither?

- **Locked** — committed via a smart contract for a fixed period, mechanically impossible to withdraw early no matter who wants to.
- **Burned** — the LP tokens representing ownership of the pool sent to a dead address no one controls, making withdrawal permanently impossible.
- **Neither** — the deployer retains the ability to withdraw some or all of that liquidity at will, whenever they choose.

This third state is the direct mechanical precondition for the most devastating meme-coin scam, the rug pull, covered in full in Module 13: if liquidity can be pulled, at some point it may be, leaving holders with an asset that can no longer be sold for anything close to its prior price. Checking LP lock/burn status is close to a precondition for considering a token investable.

## 5. Contract Ownership & Permissions

**Contract ownership** is the first and most structural question: has ownership of the token's smart contract been **renounced** — meaning no one, including the original deployer, can call its privileged functions ever again — or is it still actively held by a wallet? Renunciation is a one-way, on-chain, publicly verifiable action; you're checking the contract's own state, not taking anyone's word for it. A contract still owned by a live wallet isn't automatically a scam — plenty of legitimate projects retain ownership temporarily — but every privileged capability below stays live as long as that ownership persists, which makes the *specific permissions* it grants the next thing to check.

**Contract permissions to check specifically** break down into three categories, each with a distinct failure mode. **Mint authority** is the ability to create new tokens out of thin air after launch — if retained and exercised, total supply increases without warning, diluting every holder's share and, worst case, letting the owner mint a huge batch and dump it into the market. **Freeze/blacklist authority** lets the contract owner block specific wallets from selling at all — the exact mechanism behind a "honeypot" (developed further in Module 13 §3): buying works normally, but selling is silently restricted for everyone except a pre-approved list, typically the deployer's wallets. **Fee/tax modification authority** is the ability to change the buy/sell tax after launch, sometimes with no upper limit — an owner can leave the tax at 2-3% while building trust, then set the sell tax to 99%, which doesn't technically prevent selling but makes it financially pointless, trapping capital as effectively as an outright freeze. Each permission, if present and not renounced, is a specific, checkable risk — a concrete capability in the contract's code right now, which is why Module 13 turns this into a hard, no-exceptions checklist item.

## 6. Trading Activity, Age & Community/Narrative Synthesis

**Trading and buy/sell behavior** — the ratio and pattern of buy versus sell transactions, visible on the block explorer — tells you something volume numbers alone can't: *who* is driving the activity. The thing to isolate is whether large sells come from top or insider wallets, versus spread broadly across many holders. Sells broadly distributed across many small holders looks like normal, healthy profit-taking in a liquid market. The same volume concentrated in a few large, early wallets looks like what it usually is — insiders exiting into buying pressure retail traders provide, often without realizing who's on the other side of the trade. Distinguishing these patterns is the payoff of the wallet-level work in Section 4; without knowing which wallets are early/insider, you can't tell them apart from the trade tape alone.

**Age of the token** functions as a dial, not a pass/fail filter. A newer token carries categorically higher risk: less time for the contract's behavior under real trading pressure, less time for a liquidity lock to be tested, less time for a genuine (or fake) community to reveal its character. But that same newness is also where the largest percentage moves in this asset class happen, since early is when the most attention and capital can still flow in relative to market cap. The correct use of age is as one input that shifts how much scrutiny everything else needs and how much capital a position deserves — a three-hour-old token demands a stricter pass on every other check, and a smaller position even if it passes, not automatic rejection.

**Community, narrative, and social growth** closes the loop back to Module 11 — apply that module's tools here rather than treating fundamentals and social analysis as separate tracks. Look for the same signature of genuine versus manufactured growth (diversified, organic engagement versus repetitive or bot-like activity — Module 11 §6), and ask whether the token's narrative fits a sector theme that's actively strong (Module 9's sector rotation) or forces a connection to one already cooling. A token can pass every fundamental check — clean holder distribution, locked liquidity, renounced contract — and still be a poor trade if its narrative has no genuine attention behind it; fundamentals tell you whether a token is *safe enough to consider*, and this step tells you whether attention and capital are likely to arrive.

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
