# Module 15 — Meme-Coin Trading Framework

**Est. length:** 3 days (6 hours) to assemble and first-apply the framework. Refinement continues through Modules 16–18.
**Prerequisite:** Modules 9–14 (this module is the synthesis of everything before it). **Feeds into:** Module 16 (journaling/limited backtesting), Module 18 (paper trading it live), Module 21 (this becomes your permanent playbook).

---

## 1. What You Need to Learn

One primary, testable meme-coin trading framework — not ten strategies — combining market condition (Module 9), discovery (Module 10), narrative/X vetting (Module 11), tokenomics (Module 12), security (Module 13), on-chain/chart reliability (Module 14), and risk management into a single repeatable, 11-stage process: market-condition check, discovery, qualification, research, entry criteria (with a confirmation requirement built in), stop/invalidation, position sizing, target/exit, trade management, no-trade conditions, and risk controls.

## 2. Why It Matters

Every module so far has been a piece. Without assembling them into one disciplined sequence, you'll apply them inconsistently under real pressure (FOMO, a fast-moving chart) — exactly when discipline matters most. This framework turns "I know a lot about meme coins" into "I have a process I follow."

## 3. The Framework: Full Pipeline

### Stage 1 — Market Condition Check (Module 9)
Meme coins have no independent fundamentals holding price up — price is almost entirely a function of market-wide risk appetite. Every session starts, before looking at a candidate, with three questions from Module 9: what's the current cycle phase (accumulation, bull, distribution, or bear)? Is BTC dominance rising or falling (rising means capital is consolidating into BTC and fleeing riskier assets, including meme coins; falling means capital is rotating out along the risk curve — the environment meme coins thrive in)? Is there an active, strong narrative pulling attention and capital into the space, or is the sector quiet? Even the best-researched setup will likely fail against a risk-off macro backdrop. Hence the explicit **no-trade condition**: if the market is clearly risk-off (BTC dominance sharply rising, breadth collapsing, narratives going quiet), reduce activity or stand fully aside — don't hunt for "the one token good enough to buck the trend."

### Stage 2 — Discovery (Module 10)
Discovery is purely mechanical — no judgment calls — because letting excitement about a specific token bias how you *source* candidates biases the rest of the pipeline before it starts. Run your Module 10 sourcing methods (trending lists on aggregators, new-launch monitoring feeds, narrative-shift tracking across currently-hot sectors) and produce a plain list of candidates with basic data: age, market cap, liquidity, volume. Nothing more. **No decision gets made here, qualitative or otherwise** — you're not yet asking "is this good," only "does this exist and what are its basic vitals." Skipping straight from a trending-list glance to an entry decision is the shortcut that produces impulse trades.

### Stage 3 — Qualification (fast first-pass filter)
Qualification solves a resource problem: full Stage 4 research (narrative vetting, tokenomics analysis, the safety checklist, on-chain investigation) takes real time, and discovery hands you more candidates than you can fully research in a day. Qualification is a fast, cheap pass that rejects obvious junk first — liquidity below your minimum threshold, holder concentration extreme enough to see at a glance, or an immediate red flag from an automated honeypot/contract scanner. It is not a substitute for full validation: a token can sail through a thirty-second check and still be an elaborately disguised scam only Stage 4 would catch. Qualification protects your time; only Stage 4 protects your capital.

### Stage 4 — Research / Validation (Modules 11–14)
This is where the real work happens: a full checklist, not ad hoc looks, replacing "vibes-based" research with a repeatable, evidence-based process. For every candidate that survives qualification, run: the X/Twitter credibility and narrative check from Module 11 (is the community organic, or manufactured?); the tokenomics and wallet/holder analysis from Module 12 (who controls supply, under what unlock schedule?); the full Ultimate Meme-Coin Safety Checklist from Module 13 (no hidden mint function, no blacklist capability, liquidity actually locked?); and the on-chain investigation and chart-reliability scoring from Module 14 (tracing real transaction history, scoring how much weight the chart deserves). Running all four every time prevents thoroughly checking what interests you while skipping what feels tedious — often exactly the checks that would have caught the problem. The output is a completed research writeup and an explicit **qualify** or **reject** decision, reasoning stated plainly enough to review later.

### Stage 5 — Entry Criteria
Entry criteria only get defined for tokens that already passed Stage 4 — this stage is about *when*, not *whether*; conflating the two causes impulsive entries. Before placing an order, write down, in falsifiable terms, what chart or on-chain condition would trigger entry: for example, a liquidity sweep followed by a reclaim, but only on a token scoring at least "moderate" on Module 14's chart-reliability test (the same sweep means far less on a low-reliability chart); or a confirmed narrative catalyst alongside genuinely broadening volume, rather than a single wallet's activity. Pick criteria you've tested and believe in, not a copied template you won't hold to under pressure. Just as important: define what **confirmation** you require beyond the raw trigger — for instance, volume staying elevated for several candles after the sweep, rather than acting on one wick that could reverse immediately. Confirmation costs a small amount of entry price to meaningfully cut how often you get faked out — worth it on an instrument as prone to wicks and manipulation as a meme coin.

### Stage 6 — Stop/Invalidation
A stop level defined *after* you're already in a trade isn't a risk control — it's a rationalization waiting to happen. This stage requires you to define, in writing, before you enter, the specific condition that would prove your thesis wrong. Meme-coin invalidation splits into two types, because a single price-based stop isn't enough to cover how these trades actually fail. The first is a **price-based** stop in the familiar sense — loss of a key structure level from your original thesis. The second is a **condition-based** invalidation that has nothing to do with price: the liquidity pool gets pulled, a previously-clean contract suddenly shows a permission change, or an insider wallet starts dumping in size. Any of these proves your safety thesis wrong regardless of where price sits, and should trigger an immediate exit. Meme coins diverge sharply from BTC/ETH here: many DEX interfaces don't support the standing stop orders you'd rely on in traditional futures trading, so a condition-based invalidation frequently requires fast, manual action. Part of "defining" this invalidation is deciding, in advance, how you'll execute an exit quickly if the condition fires while you're not staring at the screen.

### Stage 7 — Position Sizing
Position sizing on a meme-coin trade starts from a different assumption than BTC/ETH sizing: on a futures setup, a full stop-out is a bounded, well-understood tail event; on a meme coin, a fast, complete loss — the token going to zero in minutes because a rug or exploit fires with no warning — is a realistic, non-tail outcome you will hit with some regularity if you trade this specialization long enough. Module 17 formalizes the exact numbers, but the principle now: size every position so its complete, fast loss is genuinely acceptable — not merely tolerable in the abstract, but a loss that doesn't change your trading behavior, your sleep, or your account's ability to keep operating. If a hypothetical total loss would make you feel "that's a shame, but fine," you're sized correctly; if it would make you feel you need to make it back immediately, the position was too large regardless of how good the setup looked.

### Stage 8 — Target / Exit Planning
Meme coins can produce spectacular, multiple-times-your-entry moves — and can just as easily give the entire move back within minutes, far faster than a BTC/ETH position typically reverses. That asymmetry is why your take-profit approach needs to be decided before entry, not improvised on the way up. A common, generally sound approach is scaling out in tranches as price extends — locking in some gain at predefined levels while leaving a runner for further upside. The alternative — a single large target with no partial exits — isn't inherently wrong, but it's a materially different risk decision: the outcome hinges on the token still being near its high when you finally sell, on an instrument where reversals can erase days of gains in a single candle. Choose deliberately, in writing, before you're emotionally invested in watching the number go up.

### Stage 9 — Trade Management
Trade management is where a meme-coin position most sharply diverges from BTC/ETH, because the safety conditions you validated at entry aren't guaranteed to hold for the life of the trade. Liquidity providers can pull funds after you've entered; a wallet that looked clean during Stage 4 research can start dumping mid-trade; a locked-liquidity timer can expire while you're still holding. So management isn't just "watch price and manage the stop" — it means periodically re-running the relevant security and on-chain checks while the position is open. A token safe at 2:00pm can stop being safe at 2:15pm, and the only way you'll know in time to act is if you're still checking.

### Stage 10 — No-Trade Conditions (explicit list)
A no-trade list only works if it's specific enough to override you in the moment you're most tempted to trade anyway. This stage collects, in one place, every hard condition under which you do not take a meme-coin trade, regardless of how good the setup looks: Stage 1's market condition reading risk-off; a candidate failing any hard item on the Module 13 safety checklist; a Module 14 chart-reliability score of "low" with no corroborating validation; noticing you're trading from FOMO or urgency rather than off a completed Stage 4 research writeup (Module 17 goes deeper on this); or already having hit your daily or weekly risk limit for this specialization (also formalized in Module 17). Writing these down in advance means that when a chart is moving fast and adrenaline is high, you're far more likely to follow a pre-committed rule than to apply fresh judgment under pressure.

### Stage 11 — Risk Controls (Overview — Full Detail in Module 17)
This final stage sets account-level guardrails that sit above any individual trade decision: a maximum position size per trade, a maximum number of concurrent meme-coin positions (correlation risk is real — many meme coins move together on shared narrative or risk-sentiment shifts, so five "different" positions can behave like one oversized bet), and a maximum daily or weekly loss limit specific to this specialization, kept separate from your BTC/ETH limits since the two instruments have very different loss profiles. Module 17 formalizes the exact numbers; the point here is that account-level risk controls keep a bad day, or a string of bad decisions above, from becoming an account-ending event.

## 4. How to Test This Framework

It would be tempting — and dishonest — to treat this 11-stage framework as validated simply because each piece is individually grounded in modules you've already studied. It is not: being *logically well-constructed* is different from being *empirically effective*, and you don't yet know how well this pipeline performs until you've run it against real candidates and tracked the results. Full backtesting, in the Module 7 BTC/ETH sense of replaying years of historical price data through a fixed rule set, is **not fully possible** for meme coins: the population of tokens, the liquidity structures they trade in, and the narrative conditions driving them all change too fast for a historical replay to tell you much about future conditions (Module 16 formalizes what can and can't be tested, and why). That doesn't exempt the framework from testing — the *method* has to be different. Three things are both possible and required in place of a traditional backtest.

1. **Paper-trade the full framework** (Module 18) on real, live candidates for a meaningful sample size before risking real capital. This matters more here than for a BTC/ETH strategy, because a meme-coin framework has many more judgment-dependent parts — qualification thresholds, reliability scoring, security-checklist calls — that only reveal their weaknesses when applied to live, messy candidates. Paper trading the pipeline, stage by stage, on real tokens is how you find out whether your Stage 5 entry criteria actually trigger sensibly in practice, before that discovery costs you money.

2. **Journal every step** (Module 16) — not just entries and exits, but every qualification and rejection decision too, including tokens you never came close to trading. This is easy to skip and expensive to have skipped: without a record of what you rejected and why, you can't later check whether your Stage 3/4 filters are well-calibrated — correctly screening out junk, rather than letting scams through because a threshold was too loose, or rejecting viable tokens because it was too strict. Rejection logic is just as testable as entries, but only if you log the rejections.

3. **Review win rate, average R, and — critically — how often Stage 10's no-trade conditions correctly kept you out of a loss.** This last measure is easy to overlook: a no-trade condition that fires produces no trade, and so no entry in a naive stats sheet — but it's exactly as valuable as a winning trade, and arguably more instructive, since it's direct evidence a piece of your discipline is working. Tracking this as process-quality feedback is how you learn whether the framework's guardrails are earning their place or just adding friction.

## 5. Practical Exercises

- Write out your own personal version of Stages 5–10 in specific, concrete terms (not the generic examples above) — this becomes your first framework draft.
- Take one real qualified candidate from Module 12–14's work and run it through the complete framework, stage by stage, ending in either a defined paper-trade plan or a documented reject decision.

## 6. Drills

- **Stage-recall drill:** name all 11 stages from memory, in order, without notes.
- **No-trade-condition drill:** given a hypothetical scenario (e.g., "market condition is risk-off but the token looks amazing"), state the correct action per your framework.

## 7. Real-World Applications

- This framework, once refined through Modules 16–18, becomes the entire content of your Module 21 meme-coin playbook.

## 8. Challenges

- Walk through a real token, end-to-end, through all 11 stages, out loud or in writing, including at least one point where the framework would have stopped you from a trade you might otherwise have taken on impulse.

## 9. Assessments

**Baseline (Day 59):** Before building it, sketch what you currently imagine a "good meme-coin process" would look like, in your own words.

**Exit (Day 61):** Present your complete, personalized 11-stage framework in writing, and walk one real candidate through it end-to-end with a clear entry/reject decision and full reasoning at each stage.

## 10. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | No defined framework, decisions made ad hoc per token |
| Developing | Framework exists on paper, not consistently applied |
| Competent | Applies the full framework to a real candidate correctly and completely |
| Advanced | Catches own impulse-driven deviations from the framework in real time |
| Highly Proficient | Framework application becomes fast and automatic |
| Mastery | Could teach someone else to build and apply their own version of this framework |

You need **Competent** to move to Module 16.

---

## 11. Day-by-Day Training Plan

### Day 59 — Assembling the Framework Skeleton (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 10 | Sketch your current mental model of "a good process" (Section 9). |
| Lesson | 50 | Read §3 in full: all 11 stages. |
| Practical | 40 | Write your own concrete version of Stages 5–10 (entry criteria, invalidation, sizing approach, exit approach, management rules, no-trade list). |
| Review/journal | 20 | Do the Section 6 stage-recall drill. |

### Day 60 — Risk Controls, No-Trade Conditions & Testing Approach (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall all 11 stages from memory again. |
| Lesson | 30 | Read §4: why full backtesting isn't possible here, and what testing approach (paper trading + journaling) replaces it. |
| Practical | 50 | Finalize your personal no-trade-condition list (Stage 10) and draft rough risk-control numbers (Stage 11) to be formalized in Module 17. |
| Review/journal | 30 | Do the Section 6 no-trade-condition drill on 3 hypothetical scenarios. |

### Day 61 — Full Application & Exit Assessment (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall your no-trade-condition list. |
| Practical | 50 | Run one real qualified candidate through the complete 11-stage framework end-to-end (Section 5). |
| Exit assessment | 40 | Present the full framework and the walked-through candidate per Section 9's exit task. |
| Reflection | 20 | Where in the pipeline are you personally most likely to cut corners under real pressure, and what will you do about it? |

**If below Competent:** Day 62 repeats the full walk-through on a fresh candidate with tighter feedback on whichever stage was weakest. **If Competent+:** move to Module 16 — Backtesting & Journaling.
