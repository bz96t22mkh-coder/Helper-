# Module 4 — BTC Specialization

**Est. length:** 6 days (12 hours). Your primary specialization gets the deepest early investment.
**Prerequisite:** Modules 1–3. **Feeds into:** Module 6 (ICT transfer analysis), Module 7 (testing), Module 8 (deeper on-chain/derivatives), Module 20 (playbook).

**Scope note:** This module builds BTC-specific market knowledge and a first, observational pass at marking your existing ICT concepts on BTC charts. Module 6 covers *which* ICT concepts transfer and *why*; Module 7 covers *testing* whether your model has a real edge on BTC. Don't expect a verdict on "does ICT work on BTC" yet — that's Module 7, on purpose, so the verdict is evidence-based.

---

## 1. What You Need to Learn

BTC market structure, BTC-specific liquidity behavior, BTC volatility characteristics, BTC market cycles (including halving cycles), BTC dominance, BTC's influence on the wider market, an introduction to BTC derivatives (funding, OI, liquidations), an introduction to BTC on-chain data, and how to read a complete BTC market snapshot.

## 2. Why It Matters

BTC is your primary specialization. Genuine expertise here means you can look at BTC and correctly separate "this is normal BTC behavior" from "this is unusual and worth investigating" — a discrimination ability generic crypto content never gives you, because it's asset-specific, built from repetition on this one market.

## 3. Foundational Concepts

- **Fixed supply, no dilution risk:** 21M hard cap, current issuance via mining rewards that halve roughly every 4 years ("the halving") until ~2140. Unlike altcoins/meme coins, BTC's supply schedule is fully known and can't be changed by any authority — this is why BTC dominance and "digital gold" narratives exist.
- **BTC as the market's base asset:** most of the crypto market is priced and correlated relative to BTC — when BTC moves sharply, correlated assets (nearly everything, to varying degrees) tend to move with it. Meme coins are the least correlated in the short term but still get crushed in a serious BTC downturn (risk-off contagion).
- **24/7, no session close:** unlike futures, BTC never closes. There's no daily settlement/gap — liquidity and volatility instead cluster around specific hours (see §5) and around scheduled macro events (CPI, FOMC) that affect BTC because of its increasing correlation to macro risk assets.

## 4. Beginner Concepts

- **BTC dominance (BTC.D):** BTC's share of total crypto market cap. Rising dominance = capital rotating *into* BTC (often relative safety within crypto, or new capital entering conservatively). Falling dominance = capital rotating into altcoins ("alt season" conditions) — you'll use this directly in Module 9.
- **Halving cycles:** historically, BTC has shown multi-year cycles loosely tied to the ~4-year halving schedule (reduced new supply). This is a **pattern observed in a small number of historical cycles, not a law of physics** — treat it as a hypothesis to weigh, not a certainty to bet on.
- **BTC volatility profile:** lower volatility than most altcoins/meme coins, but still far higher than traditional FX/equities — it moves in both regime types: prolonged low-volatility ranges and sharp, fast expansions (often on macro news or large liquidation cascades).

## 5. Intermediate Concepts

- **Session/liquidity behavior on BTC:** while BTC trades 24/7, volume and volatility still concentrate — historically heavier around U.S. and Asian trading hours, and around major macro data releases (CPI, FOMC, NFP), similar in spirit to your futures killzones but driven by macro calendar + regional liquidity rather than a fixed session close.
- **Weekend behavior:** BTC often sees thinner liquidity on weekends (less institutional/CEX desk activity), which can mean cleaner liquidity sweeps into weekday opens, or sharper moves on lower volume — a real, testable difference from futures (see Module 7).
- **BTC as a macro-correlated asset (evolving):** since institutional adoption (ETFs, corporate treasuries) increased, BTC's correlation to equities/macro risk sentiment has grown at times and decoupled at others — don't assume a fixed correlation; check current conditions.

## 6. Advanced Concepts

- **BTC derivatives basics** (deepened in Module 8): perpetual futures dominate BTC trading volume over spot on many venues. **Funding rate** = the periodic payment between longs and shorts that keeps perp price near spot — persistently positive funding = crowded long positioning (a potential long-squeeze risk); persistently negative = crowded short positioning. **Open interest (OI)** = total value of outstanding derivative contracts — rising OI + rising price = new money entering (healthy trend); rising OI + flat price = building tension (often resolved by a liquidation cascade).
- **Liquidations:** when leveraged positions are forcibly closed as price moves against them, often triggering all a "liquidation cascade" — mechanically explains many of BTC's sharpest, fastest wicks. You will learn to identify a liquidation-driven move vs. a spot-driven move using data (Module 8), not by guessing from the wick shape alone.
- **BTC on-chain data (introduced here, deepened in Module 8):** exchange net flows (coins moving to exchanges often precede selling pressure; moving off exchanges often signals accumulation/holding), and long-term holder behavior. These are **probabilistic context, not signals to trade blindly** — same honesty rule as everywhere else in this course.

## 7. Practical Exercises

- Pull up a BTC weekly and daily chart. Identify the last 2 major cycle highs/lows (if data is available on your platform) and note roughly where BTC dominance was doing at each (rising into the low, falling into the high, or unclear) — observational, not predictive.
- Check current BTC funding rate and OI (Coinglass). Write one sentence interpreting current positioning (crowded long/short/neutral) — clearly labeled as **Hypothesis**, not fact about future price.
- Mark BTC's daily chart (last 2–3 weeks) with your existing ICT toolkit: market structure (BOS/CHoCH), liquidity pools (equal highs/lows), and any FVGs/order blocks you can identify — purely observational, no trading decision yet.

## 8. Drills

- **Dominance-read drill:** given a hypothetical BTC.D chart direction, state whether conditions favor altcoin strength or BTC-relative strength, and why.
- **Funding-interpretation drill:** given 3 hypothetical funding-rate scenarios (strongly positive, near zero, strongly negative), state what each implies about crowd positioning — and what it does *not* guarantee.

## 9. Real-World Applications

- Everything here becomes the "market context" layer you check before ever taking an ICT-based BTC trade idea in Module 6–7.

## 10. Challenges

- Write a complete "BTC market snapshot" for today: price, trend/structure on daily and weekly, current BTC dominance and its recent direction, current funding rate and OI level, and any major upcoming macro event — labeling each item as Fact, Hypothesis, or Narrative.

## 11. Assessments

**Baseline (Day 16):** What do you currently know about BTC beyond "it's the first cryptocurrency"? Be honest about gaps.

**Exit (Day 21):** Produce a complete BTC market snapshot (per the Section 10 challenge) live, and mark a recent BTC chart with market structure, liquidity, and at least one FVG/order block using your existing ICT vocabulary, correctly labeled.

## 12. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | Knows BTC is "digital gold," nothing structural |
| Developing | Knows definitions (dominance, funding, halving) but doesn't synthesize them into a snapshot |
| Competent | Produces a full, correctly-labeled BTC market snapshot unprompted |
| Advanced | Correctly marks ICT structure/liquidity on a live BTC chart without guidance |
| Highly Proficient | Integrates dominance/funding/OI context into chart reads automatically |
| Mastery | Could teach someone else to read BTC's current market state end-to-end |

You need **Competent** to move to Module 5.

---

## 13. Day-by-Day Training Plan

### Day 16 — BTC Fundamentals: Supply, Base-Asset Role, 24/7 Nature (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 10 | Write your current BTC knowledge (Section 11). |
| Lesson | 40 | Read §3–4: fixed supply/halving, BTC as base asset, 24/7 market, dominance, cycle-pattern caveat. |
| Practical | 40 | Pull up BTC weekly chart; note the last 1–2 halving dates roughly and observe price behavior around them (observational only). |
| Review/journal | 30 | Explain, from memory, why BTC dominance rising or falling matters for the rest of the market. |

### Day 17 — BTC Volatility & Session/Weekend Behavior (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's dominance explanation. |
| Lesson | 30 | Read §4–5: volatility profile, session/liquidity concentration, weekend behavior. |
| Chart work | 50 | On BTC's daily/4H, compare volatility and range on 3 recent weekdays vs. 2 recent weekend days. Note anything different about liquidity sweeps or range. |
| Review/journal | 30 | Write 3–4 sentences on how BTC's "no session close" changes how you'd think about killzones vs. futures. |

### Day 18 — BTC Dominance & Influence on the Wider Market (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall session/weekend observations. |
| Lesson | 25 | Reinforce §4 dominance concept with real current BTC.D data. |
| Research | 45 | Track current BTC.D level and its trend (rising/falling/flat) over the last 30–90 days on a dominance chart (CoinGecko/TradingView "BTC.D"). |
| Chart work | 30 | Compare BTC's recent trend to one large altcoin's — is the altcoin outperforming or underperforming BTC right now, and is that consistent with the dominance trend? |
| Journal | 10 | Do the Section 8 dominance-read drill. |

### Day 19 — BTC Derivatives: Funding, OI, Liquidations (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall the dominance/altcoin relationship from yesterday. |
| Lesson | 35 | Read §6: funding rate, OI, liquidations, liquidation cascades. |
| Practical | 45 | On Coinglass, record current BTC funding rate, OI (and its recent trend — rising/falling), and check the liquidation heatmap for nearby liquidity clusters. |
| Review/journal | 30 | Write the Section 8 funding-interpretation drill using today's real numbers, labeled Hypothesis. |

### Day 20 — BTC On-Chain Data Introduction (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall today's funding/OI numbers. |
| Lesson | 30 | Read §6 on-chain intro: exchange flows, long-term holder behavior, probabilistic-not-predictive framing. |
| Research | 50 | Using a free on-chain dashboard (e.g., CryptoQuant free tier, or a public dashboard you find via Module 2's tool list), check current BTC exchange netflow direction (net inflow or outflow) over the last week. |
| Review/journal | 30 | Write one sentence on what today's exchange-flow direction *might* imply, explicitly labeled Hypothesis, not Fact about future price. |

### Day 21 — Applying ICT to a BTC Chart + Exit Assessment (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall on-chain flow direction from yesterday. |
| Chart work | 40 | Mark a recent BTC daily/4H chart with market structure (BOS/CHoCH), liquidity (equal highs/lows, draw on liquidity), and at least one FVG/order block, using your existing ICT vocabulary — purely observational. |
| Exit assessment | 50 | Produce a full BTC market snapshot (Section 10 challenge) and present your marked chart, labeling every claim Fact/Hypothesis/Narrative. |
| Reflection | 20 | What about BTC surprised you most this week compared to what you assumed from futures trading? |

**If below Competent:** Day 22 repeats the snapshot + chart-marking exercise on fresh data with targeted feedback on the weakest component. **If Competent+:** move to Module 5 — ETH Specialization.
