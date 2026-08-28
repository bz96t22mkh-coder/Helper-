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

- **Objective, pre-defined rules** are the foundation the entire testing process rests on, and skipping this step quietly invalidates everything that follows even if you don't notice it happening. The requirement is simple to state and surprisingly hard to actually follow: you must write down your exact entry, stop, and target criteria — using Module 6's six-point checklist as the starting rule set — *before* you look at how a given historical setup played out, because the human brain is extremely good at unconsciously noticing "this setup worked" first and then reverse-engineering a plausible-sounding reason it was valid, a bias that will make every backtest look artificially profitable if you let it happen. The discipline that prevents this is mechanical and a little tedious on purpose: write the rule in full before you start, then scan forward through historical price chronologically — left to right, exactly as time actually passed — applying the rule exactly as written to whatever setup appears next, without looking ahead first to see if it worked. This is precisely why bar replay (below) is preferred over freely scrolling a historical chart: scrolling lets your eye jump ahead and see the outcome before you've committed to whether the setup qualified, which is hindsight bias in its purest form.
- **Sample size** determines whether anything you conclude from a backtest actually means something, or whether you're just describing noise, and the numbers here are worth internalizing precisely because intuition badly underestimates how much data is actually needed. A handful of trades — 5 to 10 — tells you almost nothing regardless of how good or bad they look, because at that size ordinary variance (a run of good or bad luck that has nothing to do with whether your edge is real) completely dominates any genuine signal; you can lose your first 6 trades with a real, positive-expectancy strategy, or win your first 6 with a strategy that has no edge at all, purely by chance. Meaningful signal typically starts to separate from noise somewhere around 30 or more trades, and genuine statistical confidence in a result usually needs 50 to 100 or more. This module is explicitly designed to get you only to a *first* sample — the target here is 20 to 30 marked setups combined across BTC and ETH — which is enough to start forming an informed, evidence-based impression, but is still small enough that Day 33's conclusions must be treated as preliminary, not final. The loop (§6) exists precisely so that this sample keeps growing through Module 16 rather than a 30-trade snapshot being mistaken for a settled verdict.
- **Backtesting versus bar replay versus forward paper trading** are three different ways to test a rule against reality, and they trade off speed against how much hindsight bias they let slip through. Pure backtesting — scanning a fully-revealed historical chart and identifying, after the fact, where your criteria were met — is the fastest method, but it carries real hindsight risk, because your eye can't help but register nearby price action (including the outcome) even while you're trying to evaluate a setup "as if" you didn't know what came next. Bar replay — the same tool your ICT futures course used, which reveals historical candles one at a time as if you were watching them form live — removes most of that hindsight risk by forcing you to make (or not make) each decision with only the information that would actually have been available at that moment, which is why it's the method this module requires. Forward paper trading (Module 18) — placing simulated trades on the market as it happens in real time, with zero possibility of hindsight — removes the bias entirely, but it's slow, since you can only accumulate one trading day's worth of data per real trading day. Given this module's tight timeline and sample-size target, bar replay is the right tool: fast enough to reach 20–30 setups in two focused sessions, rigorous enough to keep the sample honest.

## 4. Beginner Concepts

- **Win rate** is simply the number of winning trades divided by total trades, and it's the statistic every new trader instinctively reaches for first — which makes it important to understand precisely why it is, on its own, nearly meaningless as a measure of whether a strategy is good. A strategy that wins only 30% of the time can still be highly profitable overall if its average winning trade is large relative to its average losing trade (a small number of big wins more than covering a larger number of small losses), and conversely a strategy that wins 70% of the time can lose money steadily if its winners are tiny and even one of its losses is disproportionately large (a pattern especially dangerous for a trader who lets losers run in hope of a reversal). The lesson isn't that win rate is useless information — it's genuinely useful once paired with average win/loss size — but that reporting win rate alone, the way a beginner instinctively does ("I'm right 65% of the time"), tells you almost nothing about whether money is actually being made, which is exactly why the next several metrics exist.
- **Average R** measures your average result per trade in units of your own initial risk — where 1R equals the dollar (or percentage) distance between your entry and your stop-loss — rather than in raw dollars, and that normalization is exactly what makes results comparable across trades of wildly different sizes and even across different assets. A trade that risked $100 and made $300 is a +3R trade; a trade that risked $500 and lost its full stop is a −1R trade — notice both numbers are independent of the actual dollar amounts, which is what lets you meaningfully compare a small ETH setup against a larger BTC setup, or a trade from three months ago against one from yesterday, on one consistent scale. This is the number that matters more than win rate for judging whether a strategy is worth trading, because it directly captures the size of your wins relative to your losses — information win rate throws away entirely — and a strategy producing a solidly positive average R across a real sample (not just 5 or 6 trades, per §3) is doing something structurally different from one hovering near zero or negative, regardless of how often it technically "wins."
- **Expectancy** combines win rate and average win/loss size into a single number that answers the actual question you care about: given this sample, what do I expect to make, on average, per trade, in R? The formula is (win rate × average win in R) minus (loss rate × average loss in R) — for example, a strategy that wins 40% of the time with an average winner of +2.5R and loses 60% of the time with an average loser of −1R has an expectancy of (0.40 × 2.5) − (0.60 × 1) = 1.0 − 0.6 = +0.4R per trade, meaning that, if this sample is representative, you'd expect to net roughly 0.4R for every trade you take over time. A positive expectancy is the mathematical definition of a real edge *over this specific sample* — it means the strategy made money on average, accounting properly for both how often it won and by how much — while a negative expectancy means the strategy, as tested, lost money on average, no matter how good any individual win felt. The italicized qualifier matters: expectancy is a property of the sample you measured, not a guarantee about the future, which is exactly why sample size (§3) and the retest step (§6) exist — a positive expectancy on 25 trades is encouraging evidence, not proof of a durable edge.
- **Profit factor** is gross profit divided by gross total loss across the sample — total R gained from all winning trades summed together, divided by total R lost from all losing trades summed together — and it gives you a second, complementary lens on the same underlying question expectancy answers, framed as a ratio rather than a per-trade average. A profit factor above 1.0 means the sample was profitable overall (gains outweighed losses in aggregate); below 1.0 means it was not, regardless of what the win rate alone suggested. Profit factor and expectancy will generally agree with each other in direction (both positive or both negative) since they're built from the same underlying wins and losses, but profit factor can be useful as a sanity check or a second way to communicate the same result — a profit factor of 1.8, for instance, is a more intuitive way to say "this sample made almost twice as much as it lost" than the equivalent expectancy figure might convey on its own.
- **Maximum drawdown** is the single largest peak-to-trough decline in your running equity across the sample, measured in R, and it answers a question neither expectancy nor profit factor addresses directly: what does the worst stretch of this strategy actually *feel like* to live through? A strategy can have a healthy positive expectancy overall while still containing a stretch of 6 or 8 consecutive losing trades somewhere in the middle of the sample — average performance and worst-case-experienced performance are genuinely different things, and a trader who only knows the average can be blindsided by a losing streak that, while consistent with the strategy's long-run math, feels emotionally like the strategy has stopped working. Tracking max drawdown from your very first sample matters because it's the number that will actually determine whether you can *psychologically and financially* stay in a strategy through its normal variance — a strategy with excellent expectancy but a drawdown deeper than you can tolerate isn't one you'll actually be able to keep executing, which connects directly to the execution-quality tracking in §5 below.

## 5. Intermediate Concepts

- **Setup frequency** — how often a fully valid, checklist-complete setup actually occurs in real market conditions, for example "2 to 3 per week on BTC's 4-hour chart" — is a piece of information distinct from whether the setup is profitable, and conflating the two is a common mistake. A low-frequency edge is not a lesser edge; a strategy that only produces a handful of valid setups per month can still have excellent expectancy and be entirely worth trading — but low frequency has real practical consequences you need to plan around: it takes proportionally longer to accumulate the sample size (§3) you need for statistical confidence, it constrains how much of your available capital and attention that particular setup type can productively absorb, and — perhaps most importantly for discipline — it means you cannot force setups that aren't there simply because you're eager to trade or because a losing streak makes you want to "make it back." Measuring your own setup frequency honestly during this module's backtest gives you a realistic expectation to calibrate against once you start looking for these setups live, rather than discovering only in real trading that valid setups are rarer than you assumed.
- **Execution quality tracking** separates a question about the *strategy* from a question about *you*, and the distinction matters because the fix for each is completely different. Whether a given setup, correctly identified, would have been profitable if traded exactly as planned is a strategy question — everything in §3–4 measures that. Whether *you actually executed it* as planned — entering at the right level rather than chasing, placing the stop where the rule specified rather than moving it, holding to the target rather than panicking out early on a scary-looking pullback — is a separate, execution question, and the two can diverge in a way that's easy to miss if you only look at your own trading results rather than tracking both layers. It's entirely possible for a model to have genuine positive expectancy on paper while your live execution of that same model is currently net negative, purely because of behavioral slippage between the rule and what you actually did — and that gap is a *you*-problem to diagnose and fix (the focus of Module 17's discipline work), not evidence that the underlying strategy doesn't work. Tracking both layers from the start of this module, even in a backtest where "execution" mostly means "did I honestly apply the rule as written," builds the habit you'll need once real capital and real emotion are involved.
- **Segmenting results** means refusing to settle for one aggregate win rate or expectancy number and instead breaking your sample down by the conditions each trade actually occurred under — time of day or session-equivalent window, weekday versus weekend (Module 6, §4), BTC versus ETH, and volatility regime (a calm, ranging market versus an expansion/high-volatility one) at minimum. The reason this step is not optional busywork is that a strategy's aggregate statistics can look mediocre or even negative while concealing a segment where it has a real, strong edge, sitting right next to a segment where it has none or actively loses — average the two together and you'd wrongly discard a strategy that works well under specific, identifiable conditions, or wrongly trust one that only works because of a few good trades in a favorable segment dragging up an otherwise weak average. This is precisely the kind of pattern the TEST → RECORD → ANALYZE → IDENTIFY WEAKNESSES → ADAPT → RETEST loop (§6) is built to surface — you cannot identify a weak segment to remove, or a strong segment to lean into, without first looking at your results segmented rather than lumped into a single number.

## 6. Advanced Concepts

- **The TEST → RECORD → ANALYZE → IDENTIFY WEAKNESSES → ADAPT IF NECESSARY → RETEST loop** is the complete process this module trains, and understanding *why* it's a loop — rather than a one-time linear procedure you complete once and move on from — is as important as knowing its six steps, because the entire discipline of Module 16's ongoing journaling is this same loop run continuously rather than once:
  1. **Test** — apply Module 6's checklist mechanically, via bar replay, across a clearly defined historical window, exactly as specified in §3's objective-rules discipline: the rule is written first, then applied chronologically without looking ahead.
  2. **Record** — log every setup that met your criteria, whether you actually took it or consciously skipped it, with full detail using Module 16's journal schema (entry, stop, target, outcome in R, and the contextual tags — time of day, weekday/weekend, asset — needed for §5's segmentation). A setup you skipped is just as informative as one you took; excluding skipped-but-valid setups from your record quietly reintroduces the cherry-picking problem §3 warned against.
  3. **Analyze** — compute win rate, expectancy, average R, profit factor, and max drawdown (§4), then break those same numbers down by the §5 categories rather than stopping at one aggregate figure.
  4. **Identify weaknesses** — look specifically for which segment is dragging the aggregate result down (a particular time window, a particular asset, weekend trades) and for which checklist item, when it was violated or marginal, correlates with the losing trades — this step is diagnostic, not corrective, and should be done with the same objectivity as the original test.
  5. **Adapt if necessary** — change a rule only when the data clearly and specifically supports the change, for example "every loss in this sample happened on a weekend-liquidity setup, so add a weekend filter to the checklist" — a conclusion drawn from looking at the actual segmented data, not from a single bad trade that happened to sting, or from a hunch about what "should" be true. If the data doesn't clearly point to a specific fix, the honest move is to say so and keep collecting sample, not to invent an adaptation to feel like progress was made.
  6. **Retest** — apply the adapted rule to a fresh or extended sample the adaptation wasn't built from, specifically to confirm the change actually improved results going forward rather than merely fitting the noise of the first sample perfectly (see curve-fitting risk, below). Skipping this step is the single most common way traders convince themselves an adaptation helped when it didn't.
- **Do not invent a new strategy prematurely.** If your ICT-based checklist, honestly tested, shows even a small positive edge with an identifiable weak segment to refine — for example, positive expectancy overall but a losing segment on weekends — the correct response is to refine that specific weakness (add the weekend filter, retest), not to discard the whole approach and start over with something new. Reserve the conclusion "this doesn't transfer to crypto" for a genuinely different situation: a reasonably-sized, honestly-recorded sample (not 8 trades) that still shows persistent negative expectancy even *after* you've identified and removed the worst-performing segment. Abandoning a checklist after one rough day, or after 10 trades, is not evidence-based — it's the same "feeling"-driven decision-making §2 warned against, just pointed in the opposite direction.
- **Curve-fitting risk** is the danger lurking inside step 5 if you're not disciplined about it: if you keep "adapting" your rules, tweak after tweak, until the very same sample you're testing against looks flawless, you haven't found a real edge — you've simply fit your rules to the specific noise of that one sample, the way an overfit statistical model memorizes its training data without learning anything generalizable. A rule set curve-fit to one 25-trade sample can look perfect on that sample and still perform no better than random on the next one, because what it actually learned was the idiosyncratic quirks of those particular 25 trades, not a genuine, repeatable market behavior. This is precisely why the retest step in the loop above is described as non-negotiable rather than optional polish: retesting an adaptation on data it wasn't built from is the only real check against having curve-fit rather than improved, and a strategy that only ever gets tested on the sample that produced it should never be trusted, no matter how good its statistics on that one sample look.

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
