# Module 6 — Applying ICT to Crypto

**Est. length:** 4 days (8 hours). One of the most important modules in the course.
**Prerequisite:** Modules 4–5, your ICT Futures course. **Feeds into:** Module 7 (testing), Module 20 (playbook).

**Critical framing:** This module does **not** re-teach ICT. It also does **not** assume your ICT edge transfers to crypto — that assumption gets tested with real data in Module 7. What this module does is give you a precise, honest map of *what's structurally identical*, *what's structurally different*, and *what you specifically need to watch for* before you trust a single crypto ICT setup.

---

## 1. What You Need to Learn

Which ICT concepts transfer directly to BTC/ETH with no modification; which ones behave differently because crypto is a 24/7, no-close, differently-liquid, differently-correlated market; and how to hold your existing strategy as a *hypothesis to test*, not a *known edge to apply*.

## 2. Why It Matters

The single biggest mistake a skilled futures trader makes moving into crypto is assuming "liquidity is liquidity, structure is structure" and trading it exactly like NQ/ES. Some of that transfers cleanly; some doesn't, for specific, learnable reasons — knowing which is which before Module 7's testing means your backtest actually tests something coherent, instead of randomly applying futures assumptions to a different market.

## 3. What Transfers Directly (Same Underlying Logic)

These concepts describe universal auction-market behavior — they don't care what's being traded, only that real participants are creating liquidity and reacting to it. On liquid venues (BTC/ETH spot and major perp markets), these transfer with essentially no conceptual modification:

- **Market structure** — higher highs/higher lows in an uptrend, lower highs/lower lows in a downtrend, and the shifts between them via BOS, CHoCH, and MSS — transfers to BTC and ETH with no conceptual changes: it requires only real capital reacting to price, true of BTC/ETH's deep markets just as of NQ or ES. Mark structure on a BTC/ETH chart exactly as you were taught on futures — Module 7 tests not *whether* structure exists but whether trading off it produces the same statistical edge given different participants, hours, and volatility.
- **Liquidity concepts** — buy-side/sell-side liquidity above old highs and below old lows, equal highs/lows, liquidity sweeps, and "draw on liquidity" — remain fully valid on crypto, and arguably become *more* visible. The mechanism (retail and leveraged traders clustering stops at obvious levels, which sophisticated participants then run before the "real" move) doesn't care whether it's NQ futures or BTC perpetuals. Crypto liquidity is actually more visible than futures because perpetual markets publish liquidation-cluster data (Module 8) showing, with real precision, where over-leveraged positions will be forcibly closed — a data-backed view of stop-loss-equivalent liquidity that futures order-flow tools don't offer as cleanly.
- **Fair value gaps, inverse FVGs, order blocks, breaker/mitigation blocks, and BPR** all describe artifacts left behind by displacement — a fast, imbalanced move that leaves an inefficiency (a gap between where buyers and sellers last transacted) or a footprint of the last opposing order flow (an order block). These require only that displacement occurs, which happens on BTC and ETH for the same reason as NQ or ES: large participants moving size faster than the order book can absorb it. The pattern-recognition skill transfers completely; Module 7 tests whether *trading reactions to* these patterns holds up statistically given crypto's liquidity and participant profile.
- **Displacement and CISD (Change in State of Delivery)** — the aggressive move signaling a shift from one order-flow regime to another, often the first sign institutional-scale participation has entered — transfers directly, since it describes *who's moving the market*, not *what*. On BTC and ETH, the equivalent to a futures institutional desk is large spot buyers/sellers, derivatives desks, and automated trading funds moving size — same behavioral footprint, different institutions. Recognizing a genuine displacement move transfers one-for-one; Module 7 builds empirical confidence it carries the same predictive value on crypto.
- **Premium/discount, the Optimal Trade Entry (OTE) zone, and dealing ranges** are pure geometry applied to a defined price range — where price sits relative to the midpoint (premium or discount), and where it has statistically reacted best (the 62–79% OTE zone). Geometry doesn't change because the y-axis is dollars-per-Bitcoin instead of dollars-per-E-mini: any liquid, trending, retracing instrument can have a dealing range and premium/discount split, and BTC/ETH do this cleanly given their deep liquidity. Module 7 tests not whether you *can* draw these zones (trivially, yes) but whether price respects them at a similar hit rate to futures — the geometry transfers with certainty; its *statistical reliability* is the open question.
- **The higher-timeframe-bias-to-lower-timeframe-execution framework** — bias from weekly/daily structure and premium/discount, then a lower timeframe for entry timing — is asset-agnostic: it's about *how to organize your analytical process*, not the instrument. It only requires structure and liquidity at multiple timeframes simultaneously, true of BTC/ETH just as of NQ/ES. The wrinkle (§4): without a universally-recognized session open, defining *which* candle counts as "the daily" or "the weekly" requires picking a convention (e.g., 00:00 UTC) and staying consistent, rather than inheriting an obvious session boundary.
- **SMT (Smart Money Technique, or inter-market divergence)** — comparing two correlated instruments for a new high/low one fails to confirm, read as hidden weakness or strength — not only transfers but arguably becomes *more* useful in crypto. Your futures pair (NQ vs. ES) is fixed; BTC and ETH give an equally clean, arguably more reliably-correlated pairing that's *always available*, since both trade 24/7 with no session gaps. A BTC/ETH divergence, or BTC-versus-alt-basket divergence, gives a continuously-available second data point to corroborate or question a setup, built into your checklist in §5.

## 4. What Behaves Differently — and Why

Not everything ports over cleanly, and the reasons why are specific and learnable rather than vague hand-waving about crypto being "different." Each of the following differences stems from a concrete structural fact about how crypto markets operate — always-on trading, no exchange-defined session structure, a different participant base, or added correlation layers — and each one is something Module 7 will have you verify empirically rather than take on faith.

- **No session close, and therefore no single, universally-recognized daily or weekly "open."** Futures has an explicit institutional event — Globex opens at a defined time, settlement is defined, and "the open" is a moment every participant observes simultaneously. Crypto trades continuously with no exchange bell or settlement to anchor a candle boundary — the "00:00 UTC daily candle" most platforms default to is a convention, not an event the market itself observes. Your AMD (Accumulation-Manipulation-Distribution)/Power-of-3 framework still applies to whatever candle period you define, but hold "the open" itself with less weight than on futures, since it lacks that same institutional significance.
- **True 24/7 trading means killzones are look-alikes, not identical, to futures.** Futures killzones (London, New York, Asia) are tied to when specific exchanges and desks are physically open. Crypto has no exchange-hours constraint, but high-liquidity windows still cluster: roughly the overlapping hours where major global desks (crypto-native and TradFi) are active, loosely resembling a blended London/New York window, plus windows around *scheduled macro catalysts* (CPI, FOMC) that increasingly move BTC/ETH like traditional risk assets. Don't assume memorized futures killzone hours apply unchanged — the §6 exercise has you empirically identify BTC's actual highest-volume hours from real data.
- **Weekend liquidity is thinner, and behaves differently, in ways that cut both directions.** Futures don't trade weekends at all. Crypto keeps trading, but with materially reduced institutional/market-maker participation, leaving a market technically open but thinner underneath. Sometimes that produces a *cleaner* setup (fewer competing participants, a textbook-clean sweep into Monday's open); other times sharper, more erratic moves (thin order-book depth causing whipsaws). Which describes BTC/ETH weekend behavior, and whether it's consistent enough to build a rule around, is a question for Module 7's testing — not something to assume.
- **Volatility regime differs by asset**, requiring asset-specific calibration, not one fixed number carried from NQ. Crypto's volatility is a spectrum: BTC, while higher than most traditional macro assets, is the *lowest*-volatility crypto asset; ETH runs hotter (Module 5, §5); and beyond the majors, altcoins and meme coins (Module 14) become categorically more volatile — often too large for futures-scale stops to mean anything. The OTE logic and "stop beyond invalidation" still apply everywhere on this spectrum, but the actual stop distance needs recalibrating per asset (Modules 5 and 14 do this per asset).
- **BTC dominance and inter-asset correlation add a systemic context layer** single-instrument futures trading doesn't confront. A technically correct NQ read generally plays out as predicted; no second instrument overrides it. In crypto, an ETH long can be technically correct by every ICT criterion and still fail because BTC sold off and dragged the market down with it — BTC functions as a systemic risk factor for nearly everything else in crypto (the flip side of the BTC/ETH correlation in Module 5, §5). "What is BTC doing right now" becomes a mechanical check before trusting any altcoin or ETH setup — the BTC-bias check formalized in §5 and, later, your Module 20 playbook.
- **News and catalyst structure is additive, not substitutive.** You already track scheduled macro data (CPI, FOMC, NFP); crypto adds an entirely separate category of catalysts that arrive with far less warning: an exchange listing, a protocol upgrade, a crypto-specific regulatory headline, or an ETF-flow release. Because these can appear with little or no scheduled warning, they risk overriding clean technical structure with less notice than you're used to — why your checklist (§5) adds a catalyst check with no futures equivalent.
- **SMT is the one concept that doesn't sort cleanly into "transfers" or "changes"** — it's both. The *logic* (§3) transfers without modification; what changes is the specific *pair* — NQ-versus-ES doesn't exist in crypto, so BTC-versus-ETH (or BTC-versus-alt-basket) takes its place. Carry that into the checklist below.

## 5. Building Your Crypto-Adapted Checklist (Draft — Refined in Module 7)

Before you ever mark a setup as valid on BTC/ETH, check:
1. **HTF bias** — the same mechanical process as futures: establish directional bias from weekly and daily structure, and locate current price within its premium or discount relative to the relevant dealing range (§3). Nothing about this step changes moving into crypto; it's included here purely for completeness, since it remains the foundation every other check sits on top of.
2. **BTC-bias check** (new, crypto-specific) — before trusting a setup on ETH or any altcoin, explicitly check what BTC's own structure and immediate price action are doing. This step has no equivalent in a single-instrument futures process, and skipping it is the single most common way a technically correct altcoin/ETH read gets invalidated by a systemic BTC move you never checked for (§4). In practice this means glancing at BTC's HTF and immediate structure every time, not just when something already feels unstable.
3. **SMT check** (adapted) — look for BTC/ETH divergence, or BTC-versus-alt-basket divergence (§3), and ask whether it corroborates or contradicts the setup you're considering. A divergence that agrees with your directional read adds a small amount of corroborating evidence; a divergence that contradicts it is a reason for caution, not necessarily a reason to abandon the setup outright, but a flag worth weighing.
4. **Liquidity condition** (adapted) — determine whether you're looking at a normal weekday liquidity window or a thinner weekend/off-hours window (§4), and adjust your risk expectations accordingly — a sweep or a reaction that would be reliable in full weekday liquidity carries different (and, per Module 7, not yet empirically confirmed) reliability in thin weekend conditions.
5. **Catalyst check** (new) — check whether a scheduled macro release or a known crypto-specific catalyst (an exchange listing, a token unlock, a protocol upgrade date) is imminent, since either can override clean technical structure with limited warning (§4). This is a habit borrowed partly from futures (macro calendar awareness) and extended to cover crypto-native events futures traders never had to track.
6. **Everything else** — market structure, liquidity concepts, FVG/order block, displacement, premium/discount, OTE: apply these exactly as you learned them on futures (§3), since nothing about them requires crypto-specific adaptation.

This checklist is a **draft hypothesis**, not a proven edge. Module 7 exists to find out whether trading it produces a real statistical edge, and to refine steps 2–5 based on actual results.

## 6. Practical Exercises

- Take one recent BTC daily/4H setup you marked in Module 4 and re-mark it using the full 6-point checklist above, noting anything you missed the first time (especially BTC-bias/SMT/catalyst, which don't exist in futures).
- Do the same for one ETH setup from Module 5.
- Identify BTC's empirically highest-volume/volatility hours over the last 5 trading days (using volume-by-hour on your charting tool) and compare them to your assumed futures killzones — are they the same hours, shifted, or different entirely?

## 7. Drills

- **Transfers-or-not drill:** given a list of 10 ICT concepts, sort them instantly into "transfers directly" vs. "needs crypto-specific adaptation," from memory. (SMT is the one concept that's genuinely both — its logic transfers, only its pair choice adapts — so answer it as "transfers, with one adaptation" rather than forcing it into a single bucket.)
- **BTC-bias-check drill:** given a hypothetical ETH long setup and a hypothetical simultaneous BTC structure break to the downside, state what you'd do (skip, reduce size, wait) and why.

## 8. Real-World Applications

- This checklist becomes the entry criteria you formally backtest in Module 7, and eventually the "Entry" and "No-Trade Conditions" sections of your Module 20 BTC/ETH playbook.

## 9. Challenges

- Write, from memory and in your own words, the single clearest example of an ICT concept that would have *misled* you on crypto if you hadn't adapted for a crypto-specific factor (BTC-bias, thin weekend liquidity, or a catalyst).

## 10. Assessments

**Baseline (Day 26):** Before instruction, guess: which of the 6-point checklist items do you think are genuinely new to crypto vs. carried over from futures?

**Exit (Day 29):** Re-mark 2 real recent BTC/ETH setups (one each) with the full 6-point checklist, correctly identifying every crypto-specific factor (BTC-bias, SMT, liquidity condition, catalyst) in addition to standard ICT structure — and explain, unprompted, why you are not yet calling this a "proven strategy."

## 11. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | Applies ICT to crypto exactly as done in futures, no adaptation |
| Developing | Aware adaptations exist, misses them inconsistently on live charts |
| Competent | Reliably applies the full 6-point checklist, correctly distinguishing transferred vs. adapted concepts |
| Advanced | Catches crypto-specific invalidation (BTC conflict, thin liquidity, catalyst) before it costs a trade |
| Highly Proficient | Runs the checklist as automatic habit across BTC and ETH |
| Mastery | Could teach another ICT trader exactly what changes moving into crypto and why |

You need **Competent** to move to Module 7 — where this checklist gets tested with real numbers, not assumed to work.

---

## 12. Day-by-Day Training Plan

### Day 26 — What Transfers Directly (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 10 | Guess which checklist items are new vs. carried over (Section 10). |
| Lesson | 45 | Read §3: everything that transfers directly, with the reasoning for why. |
| Chart work | 45 | Re-mark one BTC setup from Module 4 with structure/liquidity/FVG/OB, confirming these transfer cleanly. |
| Review/journal | 20 | Write, from memory, the list of directly-transferring concepts. |

### Day 27 — What Behaves Differently (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's transfer list. |
| Lesson | 45 | Read §4: 24/7 markets, killzone look-alikes, weekend liquidity, volatility regime, dominance/correlation, catalyst structure, SMT reshaping. |
| Research | 45 | Do the Section 6 volume-by-hour exercise on BTC and compare to your assumed futures killzones. |
| Review/journal | 20 | Explain, from memory, why crypto's killzones can't just be assumed from futures. |

### Day 28 — Building the Crypto-Adapted Checklist (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's volume-by-hour findings. |
| Lesson | 25 | Read §5: the 6-point checklist. |
| Chart work | 55 | Re-mark one BTC and one ETH setup using the full checklist, explicitly noting BTC-bias, SMT, liquidity condition, and any catalyst. |
| Review/journal | 30 | Do the Section 7 transfers-or-not drill and the BTC-bias-check drill. |

### Day 29 — Integration & Exit Assessment (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall the full 6-point checklist from memory. |
| Chart work | 50 | Do the Section 10 exit task: 2 fresh setups (BTC + ETH), full checklist applied. |
| Challenge | 30 | Write the Section 9 challenge answer. |
| Reflection | 30 | What's your honest current confidence that this checklist has a real edge on crypto — and why is that question unanswerable without Module 7? |

**If below Competent:** Day 30 repeats checklist application on 2 new setups with targeted feedback on whichever crypto-specific factor was missed. **If Competent+:** move to Module 7 — Testing Your ICT Model on BTC & ETH.
