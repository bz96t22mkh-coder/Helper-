# Module 7 — Testing Your ICT Model on BTC & ETH

**Est. length:** 4 days (8 hours) to run the first test cycle. This module's *loop* (test → record → analyze → adapt → retest) continues informally for as long as you trade BTC/ETH — 4 days gets you through one full cycle with a real, if small, sample.
**Prerequisite:** Module 6. **Feeds into:** Module 16 (formal ongoing journaling/backtesting cadence), Module 20 (playbook — only gets written once you have real numbers).

**The point of this module:** you do not yet know if your ICT model has an edge on BTC/ETH. Guessing, "feeling" confident, or assuming futures skill transfers is not evidence. This module produces real numbers.

---

## 1. What You Need to Learn

How to backtest objectively (defined rules, no hindsight bias); what sample size is actually needed before a conclusion means anything; how to calculate and interpret win rate, expectancy, average R, profit factor, drawdown, and setup frequency; the difference between strategy quality and execution quality (whether the model works vs. whether you followed it); how to segment results by condition (time of day, weekday/weekend, volatility regime) instead of lumping everything together; and the TEST → RECORD → ANALYZE → IDENTIFY WEAKNESSES → ADAPT IF NECESSARY → RETEST loop.

## 2. Why It Matters

An untested assumption ("ICT works, I know it works on futures") ported directly to real capital in a new market is how skilled traders lose money confidently. This module is the difference between "I believe this works" and "I have 40 recorded trades and here's what they show."

## 3. Foundational Concepts

- **Objective, pre-defined rules** are the foundation the entire testing process rests on. You must write down your exact entry, stop, and target criteria — using Module 6's six-point checklist as the starting rule set — before looking at how a historical setup played out. The brain is extremely good at unconsciously noticing "this setup worked" and then reverse-engineering a reason it was valid, which makes every backtest look artificially profitable if you let it happen. The discipline: write the rule in full first, then scan forward through historical price chronologically, applying it exactly as written to whatever setup appears next, without looking ahead. This is why bar replay (below) is preferred over freely scrolling a chart — scrolling lets your eye jump ahead and see the outcome before you've committed to whether the setup qualified — pure hindsight bias.
- **Sample size** determines whether a backtest conclusion means anything or is just noise — intuition badly underestimates how much data is needed. A handful of trades (5–10) tells you almost nothing: ordinary variance dominates any real signal at that size, and you can lose your first 6 trades with a genuinely positive-expectancy strategy, or win your first 6 with no edge at all, purely by chance. Meaningful signal typically separates from noise around 30+ trades; real statistical confidence usually needs 50–100+. This module targets only a *first* sample — 20 to 30 marked setups combined across BTC and ETH — enough to form an evidence-based impression, but small enough that Day 33's conclusions stay preliminary. The loop (§6) keeps that sample growing through Module 16, rather than letting a 30-trade snapshot pass for a settled verdict.
- **Backtesting versus bar replay versus forward paper trading** are three ways to test a rule against reality, trading off speed against hindsight bias. Pure backtesting — scanning a fully-revealed historical chart for where criteria were met after the fact — is fastest but carries real hindsight risk, since your eye can't help registering nearby price action, including the outcome. Bar replay — the same tool your ICT futures course used, revealing candles one at a time as if live — removes most of that risk by forcing each decision with only the information available at that moment. Forward paper trading (Module 18) removes hindsight bias entirely but is slow — one trading day's data per real day. Given this module's timeline and sample-size target, bar replay is the right tool: fast enough to reach 20–30 setups in two sessions, rigorous enough to keep the sample honest.

## 4. Beginner Concepts

- **Win rate** is simply the number of winning trades divided by total trades — and on its own, it's nearly meaningless as a measure of whether a strategy is good. A strategy that wins only 30% of the time can still be highly profitable if its average winner is large relative to its average loser (a small number of big wins outweighing many small losses); conversely, a strategy that wins 70% of the time can lose money steadily if its winners are tiny and even one loss is disproportionately large (dangerous for a trader who lets losers run hoping for a reversal). Win rate is useful once paired with average win/loss size — but reporting it alone ("I'm right 65% of the time") tells you almost nothing about whether money is actually being made, which is why the next several metrics exist.
- **Average R** measures your average result per trade in units of your own initial risk — where 1R equals the dollar (or percentage) distance between entry and stop-loss — rather than raw dollars, which makes results comparable across trades of different sizes and different assets. A trade that risked $100 and made $300 is a +3R trade; one that risked $500 and lost its full stop is a −1R trade — both independent of dollar amounts, letting you compare a small ETH setup against a larger BTC one on the same scale. Average R matters more than win rate because it captures win/loss size directly — information win rate discards — and a solidly positive average R across a real sample (not just 5 or 6 trades, per §3) is structurally different from one hovering near zero or negative.
- **Expectancy** combines win rate and average win/loss size into a single number: given this sample, what do I expect to make, on average, per trade, in R? The formula is (win rate × average win in R) minus (loss rate × average loss in R) — for example, a strategy that wins 40% of the time with an average winner of +2.5R and loses 60% of the time with an average loser of −1R has an expectancy of (0.40 × 2.5) − (0.60 × 1) = 1.0 − 0.6 = +0.4R per trade: if the sample is representative, you'd expect to net roughly 0.4R per trade over time. A positive expectancy means the strategy made money on average *over this specific sample*, accounting for both how often it won and by how much; a negative expectancy means it lost money on average, no matter how good any individual win felt. Expectancy is a property of the sample you measured, not a guarantee about the future — why sample size (§3) and the retest step (§6) exist: a positive expectancy on 25 trades is encouraging evidence, not proof of a durable edge.
- **Profit factor** is gross profit divided by gross total loss across the sample — total R gained from winning trades, divided by total R lost from losing trades — a second lens on the same question expectancy answers, framed as a ratio rather than a per-trade average. Above 1.0 means the sample was profitable overall; below 1.0 means it was not, regardless of win rate. Profit factor and expectancy generally agree in direction, since they're built from the same wins and losses, but profit factor doubles as a sanity check — a profit factor of 1.8 is a more intuitive way to say "this sample made almost twice as much as it lost" than the equivalent expectancy figure.
- **Maximum drawdown** is the single largest peak-to-trough decline in your running equity across the sample, measured in R — it answers a question neither expectancy nor profit factor addresses: what does the worst stretch of this strategy actually *feel like* to live through? A strategy can have a healthy positive expectancy overall while still containing a stretch of 6 or 8 consecutive losing trades in the middle of the sample — average performance and worst-case experience are different things, and a trader who only knows the average can be blindsided by a losing streak that, while consistent with the strategy's math, feels like it has stopped working. Concretely: if your running cumulative equity (in R), trade by trade, goes 1, 3, 4, 3, 2, 1, 0, 3 — that's a +1, +2, +1, then four straight −1 losses, then a +3 — equity peaked at 4R after the third trade and bottomed at 0R after the fourth loss, before recovering. The max drawdown for that stretch is peak minus trough: 4R, even though the sample still ends at a healthy +3R cumulative. Tracking max drawdown matters because it determines whether you can stay in a strategy, psychologically and financially, through its normal variance — excellent expectancy with an intolerable drawdown isn't a strategy you'll keep executing, which connects to execution-quality tracking in §5 below.

## 5. Intermediate Concepts

- **Setup frequency** — how often a fully valid, checklist-complete setup actually occurs, e.g. "2 to 3 per week on BTC's 4-hour chart" — is distinct from whether the setup is profitable, and conflating the two is a common mistake. A low-frequency edge is not a lesser edge: a strategy producing only a handful of valid setups per month can still have excellent expectancy. But low frequency has practical consequences: it takes longer to accumulate the sample size (§3) you need for confidence, it limits how much capital and attention that setup type can absorb, and it means you cannot force setups that aren't there out of eagerness or because a losing streak makes you want to "make it back." Measuring your own setup frequency honestly during this backtest gives you a realistic expectation for live trading, rather than discovering later that valid setups are rarer than you assumed.
- **Execution quality tracking** separates a question about the *strategy* from a question about *you* — the fix for each differs. Whether a given setup, correctly identified, would have been profitable if traded exactly as planned is a strategy question — everything in §3–4 measures that. Whether *you actually executed it* as planned — entering at the right level rather than chasing, placing the stop where the rule specified, holding to the target rather than panicking out on a scary pullback — is a separate, execution question. A model can have positive expectancy on paper while your live execution of it is net negative, purely from behavioral slippage between rule and action — that gap is a *you*-problem to diagnose and fix (Module 17's discipline work), not evidence the strategy doesn't work. Tracking both layers from the start, even where "execution" mostly means "did I honestly apply the rule as written," builds the habit you'll need once real capital and emotion are involved.
- **Segmenting results** means refusing to settle for one aggregate win rate or expectancy number and instead breaking your sample down by the conditions each trade occurred under — time of day, weekday versus weekend (Module 6, §4), BTC versus ETH, and volatility regime (calm/ranging versus expansion/high-volatility) at minimum. This matters because aggregate statistics can look mediocre or even negative while concealing a segment with a real edge sitting next to one with none or actively losing — average the two together and you'd wrongly discard a strategy that works well under specific conditions, or wrongly trust one propped up by a few good trades in a favorable segment. This is the kind of pattern the TEST → RECORD → ANALYZE → IDENTIFY WEAKNESSES → ADAPT → RETEST loop (§6) is built to surface — you cannot identify a weak segment to remove, or a strong one to lean into, without segmenting results rather than lumping them into a single number.

## 6. Advanced Concepts

- **The TEST → RECORD → ANALYZE → IDENTIFY WEAKNESSES → ADAPT IF NECESSARY → RETEST loop** is the complete process this module trains. Understanding *why* it's a loop — not a one-time procedure — matters as much as knowing its six steps, because Module 16's ongoing journaling is this same loop run continuously:
  1. **Test** — apply Module 6's checklist mechanically, via bar replay, across a clearly defined historical window, per §3's objective-rules discipline: rule written first, then applied chronologically without looking ahead.
  2. **Record** — log every setup that met your criteria, whether taken or consciously skipped, using Module 16's journal schema (entry, stop, target, outcome in R, and the tags — time of day, weekday/weekend, asset — needed for §5's segmentation). A skipped setup is just as informative as one you took; excluding it reintroduces the cherry-picking problem §3 warned against.
  3. **Analyze** — compute win rate, expectancy, average R, profit factor, and max drawdown (§4), then break those same numbers down by the §5 categories rather than stopping at one aggregate figure.
  4. **Identify weaknesses** — look for which segment is dragging the aggregate result down (a particular time window, a particular asset, weekend trades) and for which checklist item, when violated or marginal, correlates with the losing trades — this step is diagnostic, not corrective; apply the same objectivity as the original test.
  5. **Adapt if necessary** — change a rule only when the data clearly supports it, e.g. "every loss in this sample happened on a weekend-liquidity setup, so add a weekend filter" — a conclusion drawn from the segmented data, not a single bad trade that stung, or a hunch about what "should" be true. If the data doesn't clearly point to a fix, say so and keep collecting sample rather than inventing an adaptation to feel like progress was made.
  6. **Retest** — apply the adapted rule to a fresh or extended sample it wasn't built from, to confirm the change actually improved results rather than merely fitting the noise of the first sample (see curve-fitting risk, below). Skipping this step is the most common way traders convince themselves an adaptation helped when it didn't.
- **Do not invent a new strategy prematurely.** If your checklist, honestly tested, shows even a small positive edge with an identifiable weak segment to refine — e.g., positive expectancy overall but a losing segment on weekends — refine that weakness (add the weekend filter, retest) rather than discard the whole approach. Reserve "this doesn't transfer to crypto" for a different situation: a reasonably-sized, honestly-recorded sample (not 8 trades) that still shows persistent negative expectancy even after you've identified and removed the worst-performing segment. Abandoning a checklist after one rough day, or 10 trades, is not evidence-based — it's the same "feeling"-driven decision-making §2 warned against, just pointed the opposite direction.
- **Curve-fitting risk** is the danger inside step 5: keep "adapting" your rules, tweak after tweak, until the same sample looks flawless, and you haven't found a real edge — you've fit your rules to the noise of that one sample, the way an overfit model memorizes its training data without learning anything generalizable. A rule set curve-fit to one 25-trade sample can look perfect on that sample and still perform no better than random on the next, because what it learned was the idiosyncratic quirks of those 25 trades, not repeatable market behavior. This is why the retest step is non-negotiable: retesting on data the adaptation wasn't built from is the only real check against curve-fitting, and a strategy only ever tested on the sample that produced it should never be trusted.

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
