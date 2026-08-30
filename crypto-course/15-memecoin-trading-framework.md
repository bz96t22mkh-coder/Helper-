# Module 15 — Meme-Coin Trading Framework

**Est. length:** 3 days (6 hours) to assemble and first-apply the framework. Refinement continues through Modules 16–18.
**Prerequisite:** Modules 9–14 (this module is the synthesis of everything before it). **Feeds into:** Module 16 (journaling/limited backtesting), Module 18 (paper trading it live), Module 21 (this becomes your permanent playbook).

---

## 1. What You Need to Learn

One primary, testable meme-coin trading framework — not ten strategies — that combines market condition (Module 9), discovery (Module 10), narrative/X vetting (Module 11), tokenomics (Module 12), security (Module 13), on-chain/chart reliability (Module 14), and risk management, into a single repeatable, 11-stage process — discovery, qualification, research, entry criteria (with a confirmation requirement built in), stop/invalidation, position sizing, target/exit, trade management, no-trade conditions, and risk controls.

## 2. Why It Matters

Every module so far has been a piece. Without assembling them into one disciplined sequence, you'll apply them inconsistently under real pressure (FOMO, a fast-moving chart) — exactly when discipline matters most. This framework is what turns "I know a lot about meme coins" into "I have a process I actually follow."

## 3. The Framework: Full Pipeline

### Stage 1 — Market Condition Check (Module 9)
Every session starts here, before you've even looked at a single candidate token, because meme coins are the most reflexive, sentiment-dependent instrument you'll trade — they don't have independent fundamentals holding their price up, so they are almost entirely a function of how much risk appetite currently exists across the broader market. Before any discovery session, you're answering three questions from Module 9: what's the current cycle phase (accumulation, bull, distribution, or bear)? Is BTC dominance trending up or down (rising dominance typically means capital is consolidating into BTC and fleeing everything riskier, including meme coins; falling dominance often means capital is rotating out along the risk curve, which is exactly the environment meme coins thrive in)? And is there an active, genuinely strong narrative pulling attention and capital into the space right now, or is the whole sector quiet? This check exists because the single best-researched, most technically sound meme-coin setup will still very likely fail if it's fighting a risk-off macro backdrop — the tide matters more than the individual swimmer. That's why this stage carries an explicit **no-trade condition**: if the broad market condition is clearly risk-off (BTC dominance sharply rising, market breadth collapsing, narratives going quiet), meme-coin conditions are structurally unfavorable, and the correct response is to reduce activity or stand fully aside — not to keep hunting for "the one token good enough to buck the trend," which is exactly the rationalization that gets traders into trouble in a deteriorating market.

### Stage 2 — Discovery (Module 10)
Discovery is deliberately kept separate from qualification and research, and it's worth understanding why: the moment you let excitement about a specific token creep into how you *source* candidates, you've already biased the rest of the pipeline before it starts. This stage is purely mechanical — you run your Module 10 sourcing methods (trending lists on aggregators, new-launch monitoring feeds, narrative-shift tracking across the sectors that are currently hot) and produce a plain list of candidates with basic, objective data attached: age, market cap, liquidity, and volume. Nothing more. **No decision gets made at this stage, qualitative or otherwise** — you are not yet asking "is this good," only "does this exist and what are its basic vitals." Skipping straight from a trending-list glance to an entry decision is exactly the shortcut that produces impulse trades; keeping discovery as its own distinct, judgment-free stage is what makes the rest of the pipeline possible to apply consistently.

### Stage 3 — Qualification (fast first-pass filter)
Qualification exists to solve a real resource problem: your full Stage 4 research process (narrative vetting, tokenomics analysis, the complete safety checklist, on-chain investigation) takes real time and attention, and on any given day discovery will hand you far more candidates than you can or should fully research. Qualification is a fast, cheap first pass whose entire job is to reject the obvious junk before you invest that time — liquidity that's below whatever personal minimum threshold you've set, holder concentration that's extreme enough to see at a glance without deep analysis, or an immediate red flag from an automated honeypot/contract scanner. The critical thing to understand about this stage is what it is *not*: it is not a substitute for full validation, and passing qualification is not remotely the same thing as being safe to trade. A token can sail through a thirty-second qualification check and still turn out to be an elaborately disguised scam that only the full Stage 4 process would catch. Qualification protects your time; only Stage 4 protects your capital.

### Stage 4 — Research / Validation (Modules 11–14)
This is where the real work happens, and it's deliberately built as a checklist run in full rather than a series of ad hoc looks, because the whole point of the modules that fed into this stage was to replace "vibes-based" research with a repeatable, evidence-based process. For every candidate that survives qualification, you run: the X/Twitter credibility and narrative check from Module 11 (is the community and attention around this token organic, or manufactured?); the tokenomics and wallet/holder analysis from Module 12 (who actually controls supply, and under what unlock schedule?); the full Ultimate Meme-Coin Safety Checklist from Module 13 (is the contract itself safe — no hidden mint function, no blacklist capability, liquidity actually locked?); and the on-chain investigation and chart-reliability scoring from Module 14 (tracing real transaction history, and honestly scoring how much weight the chart itself deserves). Running all four in full, every time, for every candidate that reaches this stage, is what prevents the failure mode where you do a thorough job on the checks you find interesting and skip the ones that feel tedious — often precisely the ones that would have caught the problem. The output isn't a feeling; it's a completed research writeup and an explicit **qualify** or **reject** decision, with your reasoning stated plainly enough that you (or someone else) could review it later and understand exactly why you decided what you decided.

### Stage 5 — Entry Criteria
Entry criteria only get defined for tokens that already passed Stage 4 — this stage is about *when*, not *whether*, and conflating the two is a common source of impulsive entries. Before you're anywhere near placing an order, you write down, in specific and falsifiable terms, exactly what chart or on-chain condition would trigger your entry: for example, a liquidity sweep followed by a reclaim, but only on a token that already scored at least "moderate" on Module 14's chart-reliability test (since, as that module covered, the same-looking sweep means far less on a low-reliability chart); or a confirmed narrative catalyst arriving alongside genuinely broadening volume, rather than a single wallet's activity. The specific examples matter less than the discipline of picking criteria that match your own tested observations rather than copying someone else's template wholesale — a criterion you don't actually understand or believe in is one you won't hold to when a trade starts moving against you. Just as important is defining what **confirmation** you require beyond the raw trigger alone — for instance, requiring that volume stays elevated for several candles after the sweep, rather than acting on a single wick that could just as easily reverse immediately. Confirmation costs you a small amount of entry price in exchange for meaningfully reducing how often you get faked out, and on an instrument as prone to wicks and manipulation as a meme coin, that trade-off is usually worth making deliberately rather than skipping under time pressure.

### Stage 6 — Stop/Invalidation
A stop level defined *after* you're already in a trade isn't a risk control, it's a rationalization waiting to happen — which is why this stage requires you to define, in writing, before you enter, the specific condition that would prove your thesis wrong. Meme-coin invalidation needs to be thought of as two distinct types, because a single price-based stop isn't enough to cover the actual ways these trades fail. The first is a **price-based** stop in the familiar sense — loss of a key structure level that was part of your original thesis. The second is a **condition-based** invalidation that has nothing to do with price at all: if the liquidity pool gets pulled, if a previously-clean contract suddenly shows a permission change, if an insider wallet starts dumping in size — any of these proves your safety thesis wrong regardless of where price currently sits, and should trigger an immediate exit. This second type is where meme coins diverge most sharply from your BTC/ETH training: a condition-based invalidation frequently requires fast, manual action, because many DEX interfaces don't support the kind of standing stop order you'd rely on in traditional futures trading — which means part of "defining" this invalidation is also deciding, in advance, how you'll actually execute an exit quickly if the condition fires while you're not staring at the screen.

### Stage 7 — Position Sizing
Position sizing on a meme-coin trade needs to start from a fundamentally different assumption than your BTC/ETH sizing does: on a futures setup, a full stop-out is a bounded, well-understood tail event; on a meme coin, a fast, complete loss of the position — not a controlled stop-out, but the token going to zero in minutes because a rug or an exploit fires with no warning — is a realistic, non-tail outcome that will happen to you with some regularity if you trade this specialization long enough. Module 17 formalizes the exact numbers, but the sizing principle to internalize now is this: size every meme-coin position so that its complete, fast loss is genuinely, practically acceptable to you — not merely tolerable in the abstract, but a loss that doesn't change your trading behavior, your sleep, or your account's ability to keep operating. If a hypothetical total loss on a position would make you feel like "that's a shame, but fine," you're sized correctly; if it would make you feel like you need to make it back immediately, the position was too large regardless of how good the setup looked going in.

### Stage 8 — Target / Exit Planning
Meme coins can produce spectacular, multiple-times-your-entry moves — and can just as easily give the entire move back within minutes, far faster than a BTC/ETH position typically reverses. That asymmetry is exactly why your take-profit approach needs to be decided before entry rather than improvised on the way up. A common and generally sound approach is scaling out in tranches as price extends — taking partial profit at predefined levels so that some gain is locked in regardless of what happens afterward, while leaving a runner position for further upside. The alternative — holding for a single large target with no partial exits — is not inherently wrong, but it is a materially different risk decision than scaling out, because it means the entire trade's outcome hinges on the token still being near its high at the moment you finally decide to sell, on an instrument where reversals can erase days of gains in a single candle. The point of this stage isn't to mandate one approach over the other; it's to make sure you're choosing between them deliberately, in writing, before you're emotionally invested in watching the number go up.

### Stage 9 — Trade Management
Trade management is where a meme-coin position most sharply diverges from a BTC/ETH position in terms of ongoing attention required, because the underlying safety conditions you validated at entry are not guaranteed to hold for the life of the trade. Liquidity providers can pull funds after you've entered; a wallet that looked clean during Stage 4 research can start dumping mid-trade; a locked-liquidity timer can expire while you're still holding. This means trade management for a meme-coin position isn't just "watch price and manage the stop" — it explicitly includes periodically re-running the relevant parts of the security and on-chain checklist while the position is open, not treating Stage 4's validation as a one-time check that's good for the life of the trade. A token that was genuinely safe at 2:00pm can stop being safe at 2:15pm, and the only way you'll know in time to act is if you're still checking.

### Stage 10 — No-Trade Conditions (explicit list)
A no-trade list only works if it's specific enough to override you in the moment you're most tempted to trade anyway — which is why this stage collects, in one explicit place, every hard condition under which you do not take a meme-coin trade, full stop, regardless of how good any individual setup looks: the market-condition stage from Stage 1 reading risk-off; a candidate failing any hard item on the Module 13 safety checklist; a Module 14 chart-reliability score of "low" with no other corroborating validation to offset it; you noticing that you're trading from FOMO or urgency rather than off a completed Stage 4 research writeup (Module 17 goes deeper on recognizing this state in yourself); or having already hit your daily or weekly risk limit for this specialization (also formalized in Module 17). The value of writing these down explicitly, in advance, is that in the moment — when a chart is moving fast and adrenaline is high — you are far more likely to follow a pre-committed rule you can simply check against than to correctly apply fresh judgment under pressure.

### Stage 11 — Risk Controls (Overview — Full Detail in Module 17)
This final stage sets the account-level guardrails that sit above any individual trade decision: a maximum position size per trade, a maximum number of concurrent meme-coin positions you'll hold at once (correlation risk is real here — many meme coins move together on shared narrative or broad risk-sentiment shifts, so five "different" positions can behave like one oversized bet), and a maximum daily or weekly loss limit specific to this specialization, kept separate from your BTC/ETH limits since the two instruments have very different loss profiles and shouldn't share a single risk budget. Module 17 will formalize the exact numbers behind each of these; the point to take from this overview now is that risk controls at the account level are what keep a bad day, or a string of bad decisions on any single stage above, from becoming an account-ending event.

## 4. How to Test This Framework

It would be tempting — and dishonest — to treat this 11-stage framework as validated simply because each of its pieces is individually grounded in modules you've already studied. It is not. A framework being *logically well-constructed* is a different claim from a framework being *empirically effective*, and the honest starting position is that you don't yet know how well this specific pipeline performs until you've actually run it against real candidates and tracked the results. Full backtesting, in the Module 7 BTC/ETH sense of replaying years of historical price data through a fixed rule set, is **not fully possible** for meme coins: the population of tokens that exist, the liquidity structures they trade in, and the narrative conditions driving them all change too fast and too fundamentally for a historical replay to tell you much about future conditions (Module 16 formalizes exactly what can and can't be tested, and why). That doesn't mean the framework gets a pass on being tested — it means the *method* of testing has to be different, and there are three things that are both possible and required in place of a traditional backtest.

1. **Paper-trade the full framework** (Module 18) on real, live candidates for a meaningful sample size before risking a single dollar of real capital. This matters more here than it would for a BTC/ETH strategy, because a meme-coin framework has many more moving, judgment-dependent parts — qualification thresholds, reliability scoring, security-checklist calls — that only reveal their weaknesses when applied to live, messy, real candidates rather than reasoned about in the abstract. Paper trading the entire pipeline, stage by stage, on real tokens as they actually appear is how you find out whether your Stage 5 entry criteria actually trigger sensibly in practice, before that discovery costs you money.

2. **Journal every step** (Module 16) — and specifically, not just the entries and exits you'd log for a BTC/ETH trade, but every qualification and rejection decision too, including the ones where you never came close to trading. This is the piece that's easy to skip and expensive to have skipped: without a record of what you rejected and why, you have no way to later check whether your Stage 3 qualification filter and Stage 4 research process are actually well-calibrated — correctly screening out genuine junk — rather than either letting scams through because a threshold was too loose, or rejecting perfectly viable tokens because a threshold was too strict. A framework's qualification and rejection logic is just as testable as its entries, but only if you log the rejections in the first place.

3. **Review win rate, average R, and — critically — how often the no-trade conditions in Stage 10 correctly kept you out of a loss.** This last measure is easy to overlook because it never shows up in a simple win/loss tally: a no-trade condition that fires and keeps you out of a token that would have gone to zero produces no trade at all, and therefore no entry in a naive stats sheet — but it is exactly as valuable to your results as a winning trade, and arguably more instructive, since it's direct evidence that a specific piece of your discipline is working as designed. Tracking this deliberately, as a distinct category of process-quality feedback separate from raw win/loss statistics, is how you learn whether the framework's guardrails are actually earning their place in the pipeline or just adding friction without adding protection.

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
