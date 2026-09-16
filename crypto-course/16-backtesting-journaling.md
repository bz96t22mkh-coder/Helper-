# Module 16 — Backtesting & Journaling

**Est. length:** 3 days (6 hours) to build the permanent systems. Both journals are then used for the rest of your trading life.
**Prerequisite:** Module 7 (BTC/ETH testing), Module 15 (meme-coin framework). **Feeds into:** Module 17 (psychology/risk review uses journal data), Module 18 (paper trading logs into these journals), Module 19 (playbooks reference journal statistics).

---

## 1. What You Need to Learn

How to extend Module 7's BTC/ETH backtesting into an ongoing, statistically honest practice; what can and cannot be meaningfully backtested for meme coins, and why; and the complete schemas for your two permanent journals — the **Crypto Trading Journal** (BTC/ETH) and the **Meme-Coin Trading/Research Journal**.

## 2. Why It Matters

A single 20–30 trade sample (Module 7) is a start, not a conclusion — real edge-detection requires an ongoing, disciplined logging habit, maintained honestly even when results are unflattering. Meme coins need a different kind of record: since you can't backtest them the normal way, your *research journal* (what you rejected and why) is as important as your *trading journal* (what you executed).

## 3. Ongoing BTC/ETH Backtesting — Extending Module 7

**Keep the sample growing indefinitely, not just until Module 7 felt "done."** It's tempting to treat your 20–30 trade backtest as done — spreadsheet built, numbers run, moved on. But that barely shows the rough shape of an edge, let alone whether it holds under different market conditions. Every new backtested or paper-traded setup gets logged into the same Module 7 schema, compounding the sample toward the 50–100+ trades where statistical patterns separate from noise. Treat "how many trades are in my sample" as a number you always know and want growing.

**Track the full stat set continuously, not as a one-time calculation.** Win rate alone tells you almost nothing — a 30% win rate with a 4:1 win-to-loss ratio is a strong system; a 70% win rate with a 1:5 ratio is a slow-motion disaster. Module 7 had you track: win rate, average win, average loss, expectancy (average result per trade in R, accounting for win rate and size), average R, profit factor (gross profit ÷ gross loss), maximum drawdown, longest losing streak, and setup frequency (how often it occurs, which determines whether an edge is usable at scale). The extension: compute all of these on **rolling windows** — last 20 trades, last 50 — not just an all-time number. A rolling view shows expectancy quietly degrading over the last 20 trades even though the lifetime number looks fine, often the first sign conditions have shifted or you've drifted from your rules.

**Segment every result, every time, the same way Module 7 taught you to.** A single pooled number hides more than it reveals, because "your edge" is usually a collection of different edges (or non-edges) across conditions that average out. Break results down by asset (BTC vs. ETH often behave differently enough to warrant separate stats), by market condition (your Module 9 cycle read at the time — a setup that works beautifully in a bull phase may be a coin-flip or worse in distribution), by time-of-day or session-equivalent window, and by volatility regime. Segmentation turns "I have an edge" into the more honest "I have an edge in these specific conditions, and don't yet know if I have one outside them" — the only way to know whether to stop taking a setup during a certain market phase.

**Keep small-sample discipline a permanent guardrail, not a one-time Module 7 lesson.** The temptation to declare victory (or defeat) early doesn't disappear with more trades logged — it just moves to whichever segment is thin. Take 200 total trades with only 12 BTC trades in a clearly-defined bear phase: you still know almost nothing about that edge, however confident your overall numbers feel. The rule stays as strict as in Module 7: never declare "this doesn't work" or "this definitely works" below roughly 30 trades in that segment. Below that, the only honest description is "preliminary" — worth tracking, not worth acting on as settled.

## 4. What Can and Cannot Be Meaningfully Backtested for Meme Coins

**Individual meme-coin setups cannot be backtested in the traditional sense, for three separate reasons.** First, the *population* of available tokens keeps changing in a way BTC/ETH's market structure doesn't — last month's best-performing setup (say, a pattern around new launches on a chain) may not exist in the same form next month, since tokens, launch mechanisms, and venues turn over far faster than an established asset's market structure. A BTC backtest from three years ago tests the same asset, on largely the same structure, as today; a meme-coin "backtest" from three months ago may test a population and liquidity environment that's already changed. Second, liquidity and holder structures for a *specific* historical token can't be replayed with realistic execution assumptions — you can't know what your fill would have been on a thin, fast-moving pool, since your own order would have been a meaningful fraction of available liquidity, making the assumed fill price closer to fiction than estimate. Third, narrative and social conditions (Modules 9 and 11) are a huge driver of meme-coin price action and are fundamentally **non-stationary** — a narrative's power comes partly from its novelty, and one that worked in one cycle can fail completely in the next simply because the audience has already seen it.

**What *can* be meaningfully tracked and reviewed instead is two things: your process quality, and your realized trade statistics, understood with the right caveats.** Process quality means checking whether you actually followed the Module 15 framework's stages — did you run full Stage 4 research, respect Stage 10's no-trade conditions — and whether your qualification/rejection filter correctly screened out the scams and red flags it was designed to catch. This is checkable *retrospectively*, even for tokens you never traded: if you rejected one for a specific security reason, check weeks later whether it in fact rugged — direct evidence your filter is well-calibrated. Realized trade statistics — win rate, average R, expectancy — can still be computed as for BTC/ETH, but hold them **lower-confidence and faster-decaying** than equivalent BTC/ETH numbers. A meme-coin "edge" measured three months ago may no longer hold, not because your execution changed, but because the environment — token population, dominant narratives, typical liquidity depth — has already moved on, faster than BTC/ETH's comparatively stable structure moves.

**The honest posture across your entire meme-coin specialization: skill development here relies much more on live, disciplined process review (an ongoing thread through Module 18) than on historical backtesting**, since the latter isn't reliably available in the traditional sense. Practically, treat every real or paper trade as your primary data source for whether the framework is working, not a dataset you mine once and trust indefinitely — the rejected-token follow-up above is the clearest example of that ongoing data collection.

## 5. The Crypto Trading Journal (BTC/ETH)

Log every taken trade — and, separately, every valid setup you correctly identified but skipped, so you can track opportunity cost, not just trades you took — with these fields. The schema is this specific, not just "entry, exit, result," because each field answers a distinct question you'll need later; a journal missing any of them quietly closes off a category of review. The **market condition** and **HTF bias** fields exist so that, months from now, you can segment results by the exact conditions Section 3 asked you to, rather than reconstructing what the market was doing from memory. The **ICT setup** and **crypto-specific checks** fields record not just that you took a trade, but which specific, named setup and which of Module 6's crypto-adapted confirmations you relied on — without this, "I trade ICT setups" tells you nothing about which *specific* setups are carrying your results and which are dead weight. **Entry, stop, target, risk (%), result, and result (R)** are the mechanical core that lets you compute every statistic from Section 3. **Execution quality** and **mistakes** separate a trade's *outcome* from the *quality of the decision* behind it — a loss on a well-executed plan and a loss on an abandoned plan look identical in the result column but mean completely different things about what to fix. **Psychology notes** feeds directly into Module 17's work on trading psychology, since patterns in your emotional state at entry are often the earliest warning sign of a developing discipline problem, well before it shows up in the statistics. And **screenshot/reference** plus **lesson** exist because a journal you can't visually cross-reference, and that doesn't force a takeaway in the moment, tends to decay into a list of numbers nobody reviews.

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

In review, these fields let a single row become more than a record of one trade. Pull thirty rows together, filter by market condition, and see whether your ICT setups hold up in distribution phases the way they do in a strong bull trend. Filter by execution quality and cross-reference against result (R), and quantify something most traders only sense vaguely — how much of your drawdown comes from bad setups versus good setups poorly executed. That distinction is only visible if the fields were filled in honestly at the time, not reconstructed favorably afterward.

## 6. The Meme-Coin Trading / Research Journal

This journal has a fundamentally different job than the BTC/ETH journal above: log **every candidate that reaches Stage 3 (Qualification) or beyond** — deliberately including rejected ones, not just the tokens you traded. This is the single most important structural difference between the two journals. A BTC/ETH journal built only from taken trades is a reasonable record, because Module 7's backtesting already gives you a separate way to evaluate the strategy; but as Section 4 established, meme coins don't have that backtesting channel, so your *rejection* record does the work backtesting would otherwise do. Every field below makes that rejection record useful rather than a pile of names you vaguely remember passing on.

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

The fields from **market cap** through **on-chain observations** capture the same evidence base your Module 12–14 research process already produces — logging it, rather than letting it live only in your head, lets you check later whether a specific metric (say, top-10 holder concentration above some threshold) actually predicted trouble across many tokens, not just the one in front of you. The **decision** field, paired with its stated reason, makes a rejection reviewable at all — "rejected, felt off" gives you nothing to calibrate against later, while "rejected: top 10 wallets controlled 71% and three were funded from the same source" is a specific claim you can check the outcome of. That check is what the **outcome of rejected tokens (follow-up)** field is for, and it's arguably the single highest-leverage field in either journal: revisiting a rejected token two weeks later and confirming it rugged is direct, concrete evidence your Stage 3/4 filter is working, while finding it ran up cleanly without incident is equally valuable evidence that part of your filter is too strict, or that you rejected it for the wrong reason. Over enough tokens, this field turns "I think my filter is well-calibrated" into a statement backed by a track record — the evidence Section 4 says has to substitute for backtesting here.

### Review Cadence

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
| Lesson | 15 | Read §6's Review Cadence subsection: weekly/monthly review cadence. |
| Practical | 35 | Run your first full weekly review on both journals per §6's Review Cadence subsection. |
| Exit assessment | 40 | Present both complete journals and answer Section 11's exit questions. |
| Reflection | 20 | What did backfilling reveal about your own process that you hadn't noticed in the moment? |

**If below Competent:** Day 65 repeats journal completion/backfill with closer feedback on missing or shallow fields. **If Competent+:** move to Module 17 — Psychology & Risk Management.
