# Module 16 — Backtesting & Journaling

**Est. length:** 3 days (6 hours) to build the permanent systems. Both journals are then used for the rest of your trading life.
**Prerequisite:** Module 7 (BTC/ETH testing), Module 15 (meme-coin framework). **Feeds into:** Module 17 (psychology/risk review uses journal data), Module 18 (paper trading logs into these journals), Module 19 (playbooks reference journal statistics).

---

## 1. What You Need to Learn

How to extend Module 7's BTC/ETH backtesting into an ongoing, statistically honest practice; exactly what can and cannot be meaningfully backtested for meme coins, and why; and the complete schemas for your two permanent journals — the **Crypto Trading Journal** (BTC/ETH) and the **Meme-Coin Trading/Research Journal**.

## 2. Why It Matters

A single 20–30 trade sample (Module 7) is a start, not a conclusion. Real edge-detection requires an ongoing, disciplined logging habit, honestly maintained even when the results are unflattering. And meme coins need a fundamentally different kind of record — since you can't backtest them the normal way, your *research journal* (what you rejected and why) is as important as your *trading journal* (what you executed).

## 3. Ongoing BTC/ETH Backtesting — Extending Module 7

**Keep the sample growing, indefinitely, not just until Module 7 felt "done."** It's tempting to treat your original 20–30 trade backtest as a completed project — you built the spreadsheet, you ran the numbers, you moved on. But 20–30 trades is barely enough to see the rough shape of an edge, let alone trust it under different market conditions than the ones it happened to be tested in. Every new backtested or paper-traded setup you take, from this point forward, gets logged into the exact same schema you built in Module 7, so that your sample keeps compounding toward the 50–100+ trades where statistical patterns actually start to separate from noise. The habit to build is treating "how many trades are in my sample" as a number you always know, and always want to see grow — not a box you checked once.

**Track the full stat set continuously, not as a one-time calculation.** Win rate alone tells you almost nothing on its own — a 30% win rate with a 4:1 average win-to-loss ratio is a strong system, and a 70% win rate with a 1:5 ratio is a slow-motion disaster. That's why Module 7 had you track the fuller picture: win rate, average win, average loss, expectancy (your average result per trade, in R, accounting for both win rate and size), average R, profit factor (gross profit divided by gross loss), maximum drawdown, longest losing streak, and setup frequency (how often the setup actually occurs, which determines whether an edge is even usable at scale). The extension here is computing all of these on **rolling windows** — your last 20 trades, your last 50 — rather than as a single all-time number. A rolling view is what lets you notice that your expectancy has quietly degraded over the last 20 trades even though your lifetime number still looks fine, which is often the first real signal that market conditions have shifted or that you've drifted from your own rules.

**Segment every result, every time, the same way Module 7 taught you to.** A single pooled number across all your trades hides more than it reveals, because "your edge" is rarely one uniform thing — it's usually a collection of different edges (or non-edges) across different conditions that happen to average out to some overall number. Keep breaking results down by asset (BTC vs. ETH often behave differently enough to warrant separate stats), by market condition (your Module 9 cycle read at the time of the trade — a setup that works beautifully in a strong bull phase may be a coin-flip or worse in distribution), by time-of-day or session-equivalent window, and by volatility regime. Segmentation is what turns "I have an edge" into the much more useful and much more honest "I have an edge in these specific conditions, and I don't yet know if I have one outside them" — and it's the only way to eventually answer questions like whether you should simply stop taking a certain setup type during a certain market phase.

**Keep small-sample discipline as a permanent guardrail, not a one-time Module 7 lesson.** The temptation to declare victory (or defeat) early doesn't go away once you have more overall trades logged — it just moves to whichever segment is currently thin. If you've taken 200 total trades but only 12 of them were BTC trades during a clearly-defined bear phase, you still know almost nothing about your BTC-in-a-bear-phase edge, regardless of how confident your overall numbers make you feel. The rule stays exactly as strict as it was in Module 7: never declare "this doesn't work" or "this definitely works" for any segment below roughly 30 trades in that specific segment. Below that threshold, the only honest description of your results is "preliminary" — worth continuing to track, not worth acting on as if it were settled.

## 4. What Can and Cannot Be Meaningfully Backtested for Meme Coins

**Individual meme-coin setups cannot be backtested in the traditional sense, and it's worth understanding the three separate reasons why, because each one rules out a different workaround you might otherwise be tempted to try.** First, the *population* of available tokens is constantly changing in a way BTC/ETH's market structure simply isn't — last month's best-performing setup type (say, a specific pattern around new launches on a particular chain) may not exist in anything like the same form next month, because the tokens, the launch mechanisms, and the trading venues themselves turn over far faster than the broad market structure of an established asset. A BTC backtest from three years ago is testing the same asset, on largely the same kind of market structure, that exists today; a meme-coin "backtest" from three months ago may be testing a population of tokens and a liquidity environment that has already meaningfully changed. Second, liquidity and holder structures for any *specific* historical token can't be replayed with realistic execution assumptions — you can't know, after the fact, what your actual fill would have been on a thin, fast-moving pool, because your own hypothetical order would have been a meaningful fraction of the available liquidity, which means the backtest's assumed fill price is closer to fiction than to a defensible estimate. Third, narrative and social conditions (Modules 9 and 11) are a huge driver of meme-coin price action and are fundamentally **non-stationary** — they don't repeat the same way twice, because a narrative's power comes partly from its novelty, and a narrative that worked in one market cycle can fail completely in the next simply because the audience has already seen it before.

**What *can* be meaningfully tracked and reviewed, instead, is two things: your process quality, and your realized trade statistics understood with the right caveats.** Process quality means checking, systematically, whether you actually followed the Module 15 framework's stages — did you run the full Stage 4 research, did you respect your Stage 10 no-trade conditions — and, importantly, whether your qualification and rejection filter correctly screened out the scams and red flags it was designed to catch. This second piece is checkable *retrospectively*, even for tokens you never traded: if you rejected a token for a specific security reason, you can go back weeks later and check whether it in fact rugged or crashed, which is direct confirming (or disconfirming) evidence about whether your filter is well-calibrated. Realized trade statistics — win rate, average R, expectancy — can still be computed exactly the way they are for BTC/ETH, but they need to be held with a different level of confidence: understand them as **lower-confidence and faster-decaying** than the equivalent BTC/ETH numbers. A meme-coin "edge" measured three months ago may simply no longer hold today, not because your execution changed, but because the underlying environment — the population of tokens, the dominant narratives, the typical liquidity depth — has already moved on, in a way that BTC/ETH's comparatively stable market structure doesn't experience nearly as fast.

**The honest posture to hold across your entire meme-coin specialization is that skill development here relies much more heavily on live, disciplined process review (an ongoing thread through Module 18) than on historical backtesting**, precisely because historical backtesting in the traditional sense isn't reliably available to you. Practically, this means treating every real or paper trade you take as your primary data source about whether the framework is working — not a historical dataset you can mine once and trust indefinitely — and treating the **outcomes of tokens you rejected** as data that's every bit as valuable as the outcomes of trades you actually took, since your qualification filter's accuracy is just as measurable, and just as important to your long-term results, as your entry timing.

## 5. The Crypto Trading Journal (BTC/ETH)

Log every taken trade — and, separately, every valid setup you correctly identified but chose to skip, so you can track opportunity cost rather than only ever reviewing the trades you happened to take — with these fields. It's worth pausing on why the schema is this specific rather than just "entry, exit, result": each field exists to answer a distinct question you'll need answered later, and a journal missing any of them quietly closes off a whole category of review. The **market condition** and **HTF bias** fields exist so that, months from now, you can segment your results by the exact conditions Section 3 asked you to segment by, rather than trying to reconstruct what the market was doing from memory. The **ICT setup** and **crypto-specific checks** fields record not just that you took a trade, but which specific, named setup and which of Module 6's crypto-adapted confirmations you relied on — without this, "I trade ICT setups" tells you nothing useful about which *specific* setups are actually carrying your results and which are dead weight. **Entry, stop, target, risk (%), result, and result (R)** are the mechanical core that lets you compute every statistic from Section 3. **Execution quality** and **mistakes** are what separate a trade's *outcome* from the *quality of the decision* that produced it — a loss on a well-executed plan and a loss on an abandoned plan look identical in the result column, but they mean completely different things about what you need to fix. **Psychology notes** feeds directly into Module 17's work on trading psychology, since patterns in your emotional state at entry are often the earliest warning sign of a developing discipline problem, well before it shows up in the statistics themselves. And **screenshot/reference** plus **lesson** exist because a journal you can't visually cross-reference, and that doesn't force you to distill a takeaway in the moment, tends to decay into a list of numbers nobody actually reviews.

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

In review, these fields are what let a single row become more than a record of one trade. Pull thirty rows together, filter by market condition, and you can see whether your ICT setups actually hold up in distribution phases the way they do in a strong bull trend. Filter by execution quality and cross-reference against result (R), and you can quantify something most traders only sense vaguely — exactly how much of your drawdown comes from bad setups versus good setups poorly executed. That distinction changes what you actually need to work on, and it's only visible if the fields were filled in honestly at the time, not reconstructed favorably afterward.

## 6. The Meme-Coin Trading / Research Journal

This journal has a fundamentally different job than the BTC/ETH journal above, and its scope reflects that: log **every candidate that reaches Stage 3 (Qualification) or beyond** — deliberately including rejected ones, not just the tokens you traded. This is the single most important structural difference between the two journals. A BTC/ETH journal built only from taken trades is a reasonable record, because Module 7's backtesting already gives you a separate way to evaluate the strategy itself; but as Section 4 established, meme coins don't have that separate backtesting channel, which means your *rejection* record is doing work that, for BTC/ETH, backtesting would otherwise do. Every field below is designed to make that rejection record actually useful rather than a pile of names you vaguely remember passing on.

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

The fields from **market cap** through **on-chain observations** exist to capture the same evidence base your Module 12–14 research process already produces — the point of logging it rather than letting it live only in your head during the research session is that it lets you go back later and check whether a specific metric (say, top-10 holder concentration above some threshold) actually predicted trouble across many tokens, not just the one you're looking at today. The **decision** field, paired with its stated reason, is what makes a rejection reviewable at all — "rejected, felt off" gives you nothing to calibrate against later, while "rejected: top 10 wallets controlled 71% and three were funded from the same source" is a specific claim you can go check the outcome of. That check is exactly what the **outcome of rejected tokens (follow-up)** field is for, and it's arguably the single highest-leverage field in either journal: revisiting a rejected token two weeks later and confirming it rugged is direct, concrete evidence that your Stage 3/4 filter is working, while finding that a rejected token instead ran up cleanly without incident is equally valuable evidence that some part of your filter may be too strict, or that you rejected it for the wrong reason. Over enough tokens, this follow-up field is what turns "I think my filter is well-calibrated" into a statement you can actually back with a track record — which is precisely the kind of evidence Section 4 argued has to substitute for the historical backtesting meme coins can't reliably support.

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
