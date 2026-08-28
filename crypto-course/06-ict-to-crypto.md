# Module 6 — Applying ICT to Crypto

**Est. length:** 4 days (8 hours). One of the most important modules in the course.
**Prerequisite:** Modules 4–5, your ICT Futures course. **Feeds into:** Module 7 (testing), Module 20 (playbook).

**Critical framing:** This module does **not** re-teach ICT. It also does **not** assume your ICT edge transfers to crypto — that assumption gets tested with real data in Module 7. What this module does is give you a precise, honest map of *what's structurally identical*, *what's structurally different*, and *what you specifically need to watch for* before you trust a single crypto ICT setup.

---

## 1. What You Need to Learn

Which ICT concepts transfer directly to BTC/ETH with no modification; which ones behave differently because crypto is a 24/7, no-close, differently-liquid, differently-correlated market; and how to hold your existing strategy as a *hypothesis to test*, not a *known edge to apply*.

## 2. Why It Matters

The single biggest mistake a skilled futures trader makes moving into crypto is assuming "liquidity is liquidity, structure is structure" and trading crypto exactly like NQ/ES. Some of that transfers cleanly. Some of it doesn't, for specific, learnable reasons — and knowing which is which before Module 7's testing phase means your backtest actually tests something coherent, instead of randomly applying futures assumptions to a different market.

## 3. What Transfers Directly (Same Underlying Logic)

These concepts describe universal auction-market behavior — they don't care what's being traded, only that real participants are creating liquidity and reacting to it. On liquid venues (BTC/ETH spot and major perp markets), these transfer with essentially no conceptual modification:

- **Market structure** (higher highs/lows, BOS, CHoCH, MSS): structure is structure — price still trends, ranges, and reverses through the same structural signatures.
- **Liquidity concepts** (buy-side/sell-side liquidity, equal highs/lows, liquidity sweeps, draw on liquidity): still valid — retail/leveraged participants still cluster stops and orders at obvious levels; BTC/ETH perp markets, if anything, have *more* mechanically visible liquidity via liquidation clusters (Module 8) than futures do.
- **FVGs, IFVGs, order blocks, breaker/mitigation blocks, BPR:** these are artifacts of displacement and imbalance, which still occur on BTC/ETH the same way they occur on NQ/ES.
- **Displacement, CISD:** aggressive, imbalanced moves signaling institutional-scale participation still happen on BTC/ETH — large spot/derivatives desks and funds create the same footprints.
- **Premium/discount, OTE, dealing ranges:** still valid geometric concepts for a defined range on any liquid instrument.
- **HTF bias → LTF execution:** the top-down framework itself is asset-agnostic.
- **SMT (inter-market divergence):** arguably *more* useful in crypto — BTC vs. ETH, or BTC vs. a basket of large-caps, gives you a clean, always-available SMT pairing (see §5).

## 4. What Behaves Differently — and Why

- **No session close, so no clean daily/weekly "open" the way futures has one:** crypto has reference times (e.g., 00:00 UTC as a common "daily candle" convention on most platforms) but no exchange bell, no globex open, no settlement. Your AMD/Power-of-3 framework still applies to *whatever candle period you define*, but "the open" carries less unique institutional weight than a real futures session open — it's a convention, not an event.
- **True 24/7 trading means killzones are look-alikes, not identical:** instead of London/NY/Asia *session* killzones tied to exchange hours, crypto's high-liquidity/high-volatility windows cluster around (a) overlapping global trading-desk hours (roughly comparable to a blended London/NY window) and (b) scheduled macro catalysts (CPI, FOMC) that increasingly move BTC/ETH like a risk asset. These windows must be **empirically identified per asset**, not assumed from futures killzones — this is a direct Module 7 testing task.
- **Weekend liquidity is thinner and behaves differently:** futures simply doesn't trade weekends; crypto does, with materially reduced desk/institutional participation. This can produce cleaner (less noisy) liquidity sweeps into Monday, or the opposite — sharper, thinner, more erratic moves. This is testable, not assumable.
- **Volatility regime is different and asset-dependent:** BTC's volatility is closer to (but still above) traditional macro assets; ETH's is higher; altcoins/meme coins are categorically different (see Module 14) — the same stop distance/OTE logic needs asset-specific calibration, not a single fixed number carried over from NQ.
- **BTC dominance and inter-asset correlation add a context layer futures doesn't have in the same way:** an ETH long can fail not because your ETH read was wrong but because BTC dumped and dragged the whole market — a systemic risk factor to check *before* every crypto ICT entry, addressed by building a BTC-bias check into your process (Module 20 playbook).
- **News/catalyst structure is different:** futures has scheduled macro data; crypto has that *plus* crypto-specific catalysts (exchange listings, protocol upgrades, regulatory headlines, ETF flow days) that can override pure technical structure with far less warning than a scheduled economic release.
- **SMT changes shape:** in futures you might compare NQ vs. ES. In crypto, the cleanest SMT pairing is often BTC vs. ETH (or BTC vs. a broader alt basket) — divergence where one makes a new high/low and the other doesn't is a genuinely useful, always-on signal, but the "correlated pair" itself needs reselecting for crypto, not assumed to be the same pair-logic as futures indices.

## 5. Building Your Crypto-Adapted Checklist (Draft — Refined in Module 7)

Before you ever mark a setup as valid on BTC/ETH, check:
1. **HTF bias** — same as futures: weekly/daily structure and premium/discount.
2. **BTC-bias check** (new, crypto-specific) — if trading ETH or an altcoin, what is BTC doing right now? A conflicting BTC move is a real invalidation risk your futures process never had to check.
3. **SMT check** (adapted) — does BTC/ETH divergence (or BTC vs. alt-basket) corroborate or contradict the setup?
4. **Liquidity condition** (adapted) — is this a weekday "normal-liquidity" window or a thin weekend/off-hours window? Your risk/expectation should differ.
5. **Catalyst check** (new) — is there a scheduled macro release or a crypto-specific catalyst (listing, unlock, upgrade) imminent that could override structure?
6. **Everything else** — market structure, liquidity, FVG/OB, displacement, premium/discount, OTE — same as futures.

This checklist is a **draft hypothesis**, not a proven edge. Module 7 exists to find out whether trading it produces a real statistical edge, and to refine steps 2–5 based on actual results.

## 6. Practical Exercises

- Take one recent BTC daily/4H setup you marked in Module 4 and re-mark it using the full 6-point checklist above, noting anything you missed the first time (especially BTC-bias/SMT/catalyst, which don't exist in futures).
- Do the same for one ETH setup from Module 5.
- Identify BTC's empirically highest-volume/volatility hours over the last 5 trading days (using volume-by-hour on your charting tool) and compare them to your assumed futures killzones — are they the same hours, shifted, or different entirely?

## 7. Drills

- **Transfers-or-not drill:** given a list of 10 ICT concepts, sort them instantly into "transfers directly" vs. "needs crypto-specific adaptation," from memory.
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
