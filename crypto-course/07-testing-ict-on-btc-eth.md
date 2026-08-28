# Module 7 — Testing Your ICT Model on BTC & ETH

**Est. length:** 4 days (8 hours) to run the first test cycle. This module's *loop* (test → record → analyze → adapt → retest) continues informally for as long as you trade BTC/ETH — 4 days gets you through one full cycle with a real, if small, sample.
**Prerequisite:** Module 6. **Feeds into:** Module 16 (formal ongoing journaling/backtesting cadence), Module 20 (playbook — only gets written once you have real numbers).

**The point of this module:** you do not yet know if your ICT model has an edge on BTC/ETH. Guessing, "feeling" confident, or assuming futures skill transfers is not evidence. This module produces real numbers.

---

## 1. What You Need to Learn

How to backtest objectively (defined rules, no hindsight bias); what sample size is actually needed before a conclusion means anything; how to calculate and interpret win rate, expectancy, average R, profit factor, drawdown, and setup frequency; how to segment results by condition (time of day, weekday/weekend, volatility regime) instead of lumping everything together; and the TEST → RECORD → ANALYZE → IDENTIFY WEAKNESSES → ADAPT IF NECESSARY → RETEST loop.

## 2. Why It Matters

An untested assumption ("ICT works, I know it works on futures") ported directly to real capital in a new market is how skilled traders lose money confidently. This module is the difference between "I believe this works" and "I have 40 recorded trades and here's what they show."

## 3. Foundational Concepts

- **Objective, pre-defined rules:** you must define your entry/stop/target criteria (using Module 6's checklist) *before* looking at whether a given historical setup "worked," or you will unconsciously cherry-pick winners. Write the rule, then scan chronologically forward through history applying it mechanically.
- **Sample size:** a handful of trades (5–10) tells you almost nothing — variance dominates at that size. Meaningful signal starts to emerge around 30+ trades, and real confidence needs 50–100+. This module gets you to a *first* small sample (target: 20–30 marked setups across BTC+ETH) — treat Day 33's conclusions as preliminary, not final, and keep the loop running through Module 16.
- **Backtesting vs. bar replay vs. forward paper trading:** backtesting (scanning historical charts) is fast but has some hindsight risk; bar replay (revealing candles one at a time, exactly like your ICT course taught) removes most of that risk and is the primary method here; forward paper trading (Module 18) removes it entirely but is slow. Use bar replay for this module.

## 4. Beginner Concepts

- **Win rate** = wins ÷ total trades. Alone, it's nearly meaningless — a 30% win rate can be highly profitable with a large average winner, and a 70% win rate can lose money with a tiny average winner and one huge loser.
- **Average R** = average result per trade in units of initial risk (1R = your stop distance). This is the number that actually matters more than win rate.
- **Expectancy** = (win rate × average win in R) − (loss rate × average loss in R). Positive expectancy = a real, mathematical edge over this sample; negative = the model *as tested* is losing money on average.
- **Profit factor** = gross profit ÷ gross loss. Above 1 = profitable in this sample; below 1 = not.
- **Maximum drawdown** = the largest peak-to-trough equity decline in the sample, in R — tells you what a losing streak actually feels like, separate from the average.

## 5. Intermediate Concepts

- **Setup frequency:** how often a valid, checklist-complete setup actually occurs (e.g., "2–3 per week on BTC 4H") — a low-frequency edge is still real but changes how you'll size/plan around it; you can't force setups that aren't there.
- **Execution quality tracking:** separate from whether the *setup* worked, track whether *you* executed it as planned (right entry, right stop, no early exit from fear) — a model can have positive expectancy while your execution of it is currently negative, and that's a you-problem, not a strategy-problem, to fix in Module 17.
- **Segmenting results:** don't just compute one aggregate win rate — break results down by: time of day/session-equivalent window, weekday vs. weekend, BTC vs. ETH, and volatility regime (calm range vs. expansion). A model can have a real edge in one segment and none in another — aggregate stats hide this.

## 6. Advanced Concepts

- **The TEST → RECORD → ANALYZE → IDENTIFY WEAKNESSES → ADAPT IF NECESSARY → RETEST loop:**
  1. **Test** — apply Module 6's checklist mechanically via bar replay across a defined historical window.
  2. **Record** — every setup (taken or skipped-but-valid) logged with full detail (Module 16's journal schema).
  3. **Analyze** — compute win rate, expectancy, avg R, profit factor, drawdown, segmented by the Section 5 categories.
  4. **Identify weaknesses** — which segment is dragging the aggregate down? Which checklist item, when violated, correlates with losses?
  5. **Adapt if necessary** — only change a rule if the data clearly supports it (e.g., "every loss happened on a weekend-liquidity setup" → add a weekend filter). Don't adapt based on a single bad trade or a hunch.
  6. **Retest** — re-run with the adapted rule on a fresh (or extended) sample to confirm the adaptation actually helped, rather than just curve-fitting to the first sample.
- **Do not invent a new strategy prematurely.** If your ICT-based checklist shows a small positive edge with room to refine (e.g., cutting one weak segment), refine it. Only consider it fundamentally non-transferable if a reasonably-sized, honestly-recorded sample shows persistent negative expectancy even after removing the worst segment.
- **Curve-fitting risk:** if you keep "adapting" until the same sample looks perfect, you've fit noise, not found an edge — this is why retesting on new data (Section 6, step 6) is non-negotiable, not optional polish.

## 7. Practical Exercises

- Set up a bar-replay session on BTC (a few months of historical daily/4H data) and a separate one for ETH.
- Using Module 6's 6-point checklist, scan forward mechanically, logging every checklist-complete setup (roughly targeting 10–15 per asset) with entry, stop, target, and outcome in R.
- Compute win rate, average R, expectancy, and profit factor separately for BTC and ETH, and combined.

## 8. Drills

- **Expectancy-calculation drill:** given a hypothetical 10-trade sample (wins/losses in R), calculate win rate, average R, and expectancy by hand.
- **Segment-spotting drill:** given a hypothetical 20-trade log with a "time of day" and "weekday/weekend" column, identify which segment is underperforming.

## 9. Real-World Applications

- This is the exact process — same loop, same math — you'll run again in Module 16 on a larger, ongoing sample, and again whenever you revise your BTC/ETH playbook (Module 20).

## 10. Challenges

- After your first 20–30-trade combined sample, write an honest one-paragraph verdict: does this checklist currently show a real (if small-sample, preliminary) edge, no edge, or an edge only in a specific segment — and what's your evidence, not your gut feeling?

## 11. Assessments

**Baseline (Day 30):** Predict, before testing, what you *expect* your win rate and expectancy to be on BTC/ETH using Module 6's checklist. (This gets checked against reality on Day 33 — expect to be at least partly wrong; that's normal and useful.)

**Exit (Day 33):** Present your full stats table (win rate, avg R, expectancy, profit factor, max drawdown) for BTC, ETH, and combined, segmented by at least two of the Section 5 categories, plus a written, evidence-based verdict and — if warranted by the data — one specific, justified adaptation to retest.

## 12. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | Trades/backtests without pre-defined rules, judges results by feel |
| Developing | Logs trades but doesn't compute real stats or segment them |
| Competent | Produces a complete, correctly-calculated stats table and an honest, evidence-based verdict |
| Advanced | Correctly identifies a weak segment and proposes a specific, non-arbitrary adaptation |
| Highly Proficient | Runs the full test→adapt→retest loop independently on new data without prompting |
| Mastery | Could explain to another trader exactly why their "it obviously works" claim needs a real sample first |

You need **Competent** to move to Module 8. (This loop keeps running — you are not "done" testing after 4 days; you have a *first* real data point.)

---

## 13. Day-by-Day Training Plan

### Day 30 — Backtesting Methodology & Statistics Literacy (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 15 | Write your Section 11 baseline predictions (expected win rate/expectancy). |
| Lesson | 45 | Read §3–5: objective rules, sample size, win rate/avg R/expectancy/profit factor/drawdown, setup frequency, execution tracking, segmentation. |
| Drill | 30 | Do the Section 8 expectancy-calculation drill by hand on a hypothetical sample. |
| Setup | 30 | Set up your bar-replay environment for BTC and ETH, and prepare a simple spreadsheet/log with columns: asset, date, checklist items met, entry, stop, target, result (R), time of day, weekday/weekend. |

### Day 31 — Running the BTC Backtest (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall the expectancy formula from memory. |
| Practical | 90 | Bar-replay BTC historical data, mechanically applying Module 6's checklist, logging every checklist-complete setup (target 10–15) with full detail. |
| Journal | 20 | Log any observations about setup frequency or obvious weak segments while they're fresh. |

### Day 32 — Running the ETH Backtest (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall BTC's setup frequency/observations from yesterday. |
| Practical | 90 | Bar-replay ETH historical data the same way (target 10–15 setups). |
| Journal | 20 | Note any qualitative differences from BTC (frequency, cleanliness of structure, volatility). |

### Day 33 — Analysis, Verdict, Exit Assessment (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall both assets' setup counts. |
| Analysis | 50 | Compute win rate, avg R, expectancy, profit factor, and max drawdown for BTC, ETH, and combined; segment by time-of-day and weekday/weekend at minimum. |
| Exit assessment | 40 | Write the Section 10 evidence-based verdict and, if warranted, one specific adaptation to retest in Module 16. |
| Reflection | 20 | Compare today's real numbers to your Day 30 baseline predictions — where were you overconfident or underconfident? |

**If below Competent** (stats miscalculated, or verdict isn't evidence-based): Day 34 repeats the analysis on the same log with closer guidance on the math and on separating fact from hunch. **If Competent+:** move to Module 8 — Crypto-Specific Market Data. (Carry your log forward — Module 16 builds the permanent, ongoing version of this.)
