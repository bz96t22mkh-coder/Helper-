# Module 16 — Backtesting & Journaling

**Est. length:** 3 days (6 hours) to build the permanent systems. Both journals are then used for the rest of your trading life.
**Prerequisite:** Module 7 (BTC/ETH testing), Module 15 (meme-coin framework). **Feeds into:** Module 17 (psychology/risk review uses journal data), Module 18 (paper trading logs into these journals), Module 19 (playbooks reference journal statistics).

---

## 1. What You Need to Learn

How to extend Module 7's BTC/ETH backtesting into an ongoing, statistically honest practice; exactly what can and cannot be meaningfully backtested for meme coins, and why; and the complete schemas for your two permanent journals — the **Crypto Trading Journal** (BTC/ETH) and the **Meme-Coin Trading/Research Journal**.

## 2. Why It Matters

A single 20–30 trade sample (Module 7) is a start, not a conclusion. Real edge-detection requires an ongoing, disciplined logging habit, honestly maintained even when the results are unflattering. And meme coins need a fundamentally different kind of record — since you can't backtest them the normal way, your *research journal* (what you rejected and why) is as important as your *trading journal* (what you executed).

## 3. Ongoing BTC/ETH Backtesting — Extending Module 7

- **Keep the sample growing:** every new backtested or paper-traded setup gets logged with the same schema as Module 7, building toward genuine statistical confidence (50–100+ trades) over time, not treated as "done" after the first cycle.
- **Full stat set, tracked continuously:** win rate, average win, average loss, expectancy, average R, profit factor, maximum drawdown, longest losing streak, setup frequency — computed on rolling windows (e.g., last 20, last 50 trades) so you can see whether performance is stable, improving, or degrading, not just a single lifetime number.
- **Segment every time:** by asset (BTC vs. ETH), market condition (Module 9's cycle read at time of trade), time of day/session-equivalent window, and volatility regime — exactly as started in Module 7, continued indefinitely.
- **Small-sample discipline:** never declare "this doesn't work" or "this definitely works" below ~30 trades in a given segment; below that, describe results as preliminary and keep testing.

## 4. What Can and Cannot Be Meaningfully Backtested for Meme Coins

- **Cannot be backtested in the traditional sense:** individual meme-coin setups, because (a) the *population* of available tokens is constantly changing — last month's best-performing setup type may not exist in the same form next month; (b) liquidity/holder structures for any specific historical token can't be replayed with realistic execution assumptions; (c) narrative/social conditions (Module 9, 11) are a huge driver and are fundamentally non-stationary (they don't repeat the same way twice).
- **Can be meaningfully tracked and reviewed:** your **process quality** — did you follow the Module 15 framework's stages, did your qualification/rejection filter correctly avoid the scams/red flags it was designed to catch (checkable retrospectively even for rejected tokens — did rejected-for-security-reasons tokens later rug/crash, confirming the filter worked?), and your **realized trade statistics** (win rate, avg R, expectancy) computed the same way as BTC/ETH but understood as *lower-confidence and faster-decaying* — a meme-coin "edge" from 3 months ago may not hold today because the environment itself changed, unlike BTC/ETH's more structurally stable market.
- **The honest posture:** meme-coin skill development relies much more heavily on **live, disciplined process review** (Module 18, ongoing) than on historical backtesting — treat every real (or paper) trade as your primary data source, and treat "outcomes of tokens you rejected" as equally valuable data on your qualification filter's accuracy.

## 5. The Crypto Trading Journal (BTC/ETH)

Log every taken trade (and, separately, every valid-but-skipped setup, to track opportunity cost) with these fields:

| Field | Description |
|---|---|
| Asset | BTC or ETH |
| Date/time | Entry time |
| Market condition | Cycle phase read (Module 9) at time of trade |
| HTF bias | Your top-down bias going in |
| ICT setup | Which specific setup type (per Module 6's checklist) |
| Crypto-specific checks | BTC-bias check, SMT read, liquidity condition, catalyst check (Module 6 §5) |
| Entry | Price/level |
| Stop | Price/level and R-distance |
| Target | Price/level |
| Risk (%) | % of account risked |
| Result | Win/loss/breakeven |
| Result (R) | Outcome in units of initial risk |
| Execution quality | Did you follow your own plan? (Module 7 §5) |
| Mistakes | Anything you'd do differently |
| Psychology notes | Emotional state during the trade (feeds Module 17) |
| Screenshot/reference | Chart image or description |
| Lesson | One-line takeaway |

## 6. The Meme-Coin Trading / Research Journal

Log **every candidate that reaches Stage 3 (Qualification) or beyond** — including rejected ones — with these fields:

| Field | Description |
|---|---|
| Token | Name/ticker |
| Date discovered | — |
| Chain | ETH/Solana/other |
| Market cap | At time of research |
| Liquidity | Pool size at time of research |
| Volume | 24h volume at time of research |
| Holders | Total holder count |
| Top wallets | Top-10/20 holder % |
| Narrative | What story/sector it fits (Module 9, 11) |
| X activity | Credibility read (Module 11) |
| Catalyst | Specific driver, if any |
| Contract/security checks | Full Module 13 checklist result |
| On-chain observations | Module 14 findings |
| Risk factors | Anything notable |
| Decision | Qualify / Reject, with the specific reason |
| Trade thesis (if qualified) | Entry criteria, invalidation, sizing, target (Module 15) |
| Entry / Stop / Target | If traded |
| Result | If traded |
| Result (R) | If traded |
| Outcome of rejected tokens (follow-up) | Revisit rejected tokens after 1–2 weeks: did the rejection reasoning hold up (it rugged/died) or not (it ran without incident)? This calibrates your filter. |
| Mistakes | — |
| Lesson | — |

## 6.1 Review Cadence

- **After every trade/research session:** log immediately, while details are fresh — not from memory a day later.
- **Weekly:** review both journals, update the rolling stats (Section 3), and specifically revisit 2–3 recently-rejected meme coins to check filter calibration.
- **Monthly:** full stats review (Module 18 deepens this into formal performance analysis) and a written note on any pattern you're noticing in your own mistakes.

## 7. Practical Exercises

- Set up both journals (spreadsheet or your preferred tool from Module 2) with the exact schemas above.
- Backfill your Module 7 BTC/ETH sample and your Module 10–15 meme-coin research into the appropriate journal, retroactively.
- Pick 2 rejected meme coins from Module 12–13 and check, right now, what happened to them since — did your rejection hold up?

## 8. Drills

- **Field-recall drill:** name every field in both journal schemas from memory.
- **Backtestable-or-not drill:** given a hypothetical claim ("I backtested my meme-coin strategy over the last year and got a 65% win rate"), explain what's specifically untrustworthy about that claim given §4.

## 9. Real-World Applications

- These two journals are the permanent record you'll use in Module 18 (performance analysis) and every future trading decision — this is not a one-time course exercise.

## 10. Challenges

- Write a short, honest statement of your current BTC/ETH sample size and what confidence level (per Module 7 §3) that actually supports — resist the temptation to overstate it.

## 11. Assessments

**Baseline (Day 62):** Have you ever kept a trading journal before? What made it work or fail?

**Exit (Day 64):** Present both fully-built, backfilled journals, correctly explain why meme coins can't be traditionally backtested, and correctly state your current BTC/ETH sample size and confidence level without overstating it.

## 12. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | No journal, or an inconsistent one |
| Developing | Journal exists, fields incomplete or inconsistently filled |
| Competent | Both journals fully built, backfilled, and used consistently |
| Advanced | Weekly review habit catches a real calibration issue (e.g., filter too loose/strict) |
| Highly Proficient | Journaling becomes immediate, automatic habit after every session |
| Mastery | Could design a journal schema for a new strategy from scratch |

You need **Competent** to move to Module 17.

---

## 13. Day-by-Day Training Plan

### Day 62 — Ongoing BTC/ETH Backtesting Discipline (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 10 | Reflect on any past journaling attempts (Section 11). |
| Lesson | 30 | Read §3: ongoing backtesting, rolling-window stats, segmentation, small-sample discipline. |
| Practical | 50 | Set up the Crypto Trading Journal (Section 5) and backfill your Module 7 sample. |
| Review/journal | 30 | Do the Section 10 challenge: write your honest current sample size/confidence statement. |

### Day 63 — Meme-Coin Journal & the Backtesting Limits (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's BTC/ETH stats. |
| Lesson | 30 | Read §4: what can/can't be backtested for meme coins, and why. |
| Practical | 50 | Set up the Meme-Coin Trading/Research Journal (Section 6) and backfill your Module 10–15 research, including rejected tokens. |
| Review/journal | 30 | Revisit 2 rejected tokens and log their outcomes since (Section 7). |

### Day 64 — Review Cadence & Exit Assessment (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall both journals' current state. |
| Lesson | 15 | Read §6.1: weekly/monthly review cadence. |
| Practical | 35 | Run your first full weekly review on both journals per §6.1. |
| Exit assessment | 40 | Present both complete journals and answer Section 11's exit questions. |
| Reflection | 20 | What did backfilling reveal about your own process that you hadn't noticed in the moment? |

**If below Competent:** Day 65 repeats journal completion/backfill with closer feedback on missing or shallow fields. **If Competent+:** move to Module 17 — Psychology & Risk Management.
