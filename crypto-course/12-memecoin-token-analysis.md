# Module 12 — Meme-Coin Token & Tokenomics Analysis

**Est. length:** 3 days (6 hours).
**Prerequisite:** Modules 3, 10–11. **Feeds into:** Module 13 (security builds directly on contract/ownership checks here), Module 15 (framework's validation stage).

---

## 1. What You Need to Learn

How to analyze a meme coin's fundamentals *before* considering a trade: market cap, FDV, supply, liquidity, volume (review/application of Module 3), holder distribution, top/developer/insider wallets, wallet concentration, token ownership, liquidity providers, liquidity lock/burn, contract ownership and permissions, trading activity and buy/sell behavior, token age, and community/narrative/social growth (application of Module 11).

## 2. Why It Matters

This is the analytical core of "validation" in your six-step pipeline (Module 10 §6). A token can have a perfect chart and a viral narrative and still be catastrophically unsafe to buy because of what's underneath — this module teaches you to see that.

## 3. Market Cap, FDV, Supply, Liquidity, Volume — Applied

You built the concepts in Module 3. Here, apply them specifically to meme coins:
- **Market cap vs. liquidity, always together:** compute both, and flag any token where liquidity is a small fraction of stated market cap (a common, dangerous pattern — see Module 3 §5).
- **FDV vs. market cap:** most meme coins launch with 100% of supply already circulating (no team vesting) — in that case FDV = market cap and this risk is moot. When they *don't* (some do allocate a team/insider portion with a vesting schedule), check exactly when that unlocks.
- **Volume relative to liquidity and age:** a 3-day-old token with volume many multiples of its liquidity pool size is either genuinely viral or heavily wash-traded (Module 3 §6) — this module's wallet-level analysis (§4) is how you tell the difference.

## 4. Holder & Wallet Analysis

- **Holder distribution:** the percentage of total supply held by the top 10, top 20, and top 50 wallets (visible on the block explorer or a tool like Bubblemaps). High concentration in a handful of wallets = high risk that a single decision (by one wallet or a small coordinated group) can crash price.
- **Developer/deployer wallet:** the wallet that deployed the contract and/or created the initial liquidity — check its current holdings, its transaction history (has it sold significant amounts already?), and whether it retains any special contract privileges (§6).
- **Insider/early wallets:** wallets that acquired a large position very early (often before public trading, or heavily during the first few minutes) — visible in the token's earliest transactions on the explorer. A cluster of same-sized, same-age wallets is a strong bundling signal (Module 13–14 deepen this with Bubblemaps).
- **Wallet concentration over time:** check not just a snapshot but the *trend* — is concentration decreasing (organic distribution as new buyers enter) or increasing (insiders accumulating more)?
- **Liquidity providers:** who supplied the DEX pool's liquidity, and — critically — is that liquidity **locked** (time-locked via a locking contract, unable to be withdrawn early) or **burned** (LP tokens sent to a dead address, permanently unable to be withdrawn by anyone) or **neither** (the deployer can pull all liquidity at will — the mechanical basis of a classic "rug pull," detailed in Module 13)?

## 5. Contract Ownership & Permissions

- **Contract ownership:** check whether the contract's ownership has been **renounced** (no one, including the original deployer, can call privileged functions anymore) or is still held by a wallet.
- **Contract permissions to check specifically:** mint authority (can more tokens be created out of thin air, diluting/crashing holders?), freeze/blacklist authority (can the contract owner freeze specific wallets from selling — a classic honeypot mechanism), and fee/tax modification authority (can the owner suddenly change the buy/sell tax to something extreme, e.g., 99%, trapping holders?). Each of these being **present and not renounced** is a material, specific risk, not a vague "be careful" — Module 13 turns this into a hard checklist.

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
