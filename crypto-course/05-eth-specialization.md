# Module 5 — ETH Specialization

**Est. length:** 4 days (8 hours).
**Prerequisite:** Module 4. **Feeds into:** Module 6 (ICT transfer analysis), Module 7 (testing), Module 8 (deeper data), Module 20 (playbook).

**Scope note:** Same as Module 4 — this builds ETH-specific knowledge and a first observational ICT chart pass. The transfer-analysis and testing verdicts come in Modules 6–7.

---

## 1. What You Need to Learn

ETH market structure, ETH-specific liquidity/volatility, ETH's relationship with BTC (including the ETH/BTC ratio), ETH derivatives (funding, OI, liquidations), ETH's ecosystem role (staking, L2s, gas/burn), and ETH on-chain data.

## 2. Why It Matters

ETH is your second primary specialization, and it behaves differently from BTC in ways that matter for trading: it's more tied to on-chain activity (gas usage, L2 growth, DeFi), it has a variable, sometimes-deflationary supply, and it trades with meaningful independence from BTC that shows up as the ETH/BTC ratio — a useful, testable signal.

## 3. Foundational Concepts

**ETH market structure itself** (BOS, CHoCH, liquidity, FVGs) doesn't get separate treatment here — structure isn't ETH-specific, and the same auction-market logic from Module 4 applies. This module covers what makes ETH different: its supply, narrative, and behavior relative to BTC. Hands-on structure practice comes in the chart-marking exercise (§7) and Day 25.

- **ETH's supply is not fixed.** Since the Merge (September 2022), Ethereum no longer issues new ETH to proof-of-work miners; instead it goes to validators staking ETH via proof-of-stake, at a rate that scales with total ETH staked (more staked → slightly higher aggregate issuance, lower per-validator yield). EIP-1559 adds a fee-burn mechanism: every transaction pays a "base fee" that is destroyed rather than paid to a validator; a separate "priority fee" (tip) goes to the block producer. Total ETH supply is a tug-of-war between issuance (adds ETH) and burn (removes it). Heavy on-chain activity — a popular NFT mint, a DeFi liquidation cascade, high L2-settlement volume — burns more than the network issues, making ETH net-deflationary for that period; a quiet period does the opposite. Check your current regime on any public ETH supply tracker (Day 22's research task). BTC's ~21 million cap and fixed halving schedule mean its supply story is announced years in advance and doesn't move with usage; ETH's is a live, usage-linked number that occasionally becomes a headline narrative ("ETH is deflationary") — treat that with the same skepticism as any other narrative (Fact vs. Narrative, Module 1), since a deflationary window doesn't guarantee a price outcome.
- **ETH as "the settlement layer for an economy"** is a fundamentally different value proposition than BTC's, shaping what news you watch for each asset. BTC's dominant narrative is monetary: a fixed-supply store of value whose case rests on scarcity and adoption as "digital gold," independent of whether the network is actually *used*. ETH's case rests on *usage* — DeFi protocols that let people lend, borrow, and trade without an intermediary; stablecoins (Module 12) settling enormous volume on Ethereum and its L2s; and growing real-world-asset tokenization — requiring Ethereum to function as infrastructure, like a payments rail other financial activity builds on. Because ETH's value case is tied to usage, ETH-specific developments — a major upgrade shipping, an L2 volume surge, a stablecoin issuer settling more on Ethereum — can move ETH's price independently of BTC — a comparable BTC-only narrative (e.g., a corporate treasury purchase) has no equivalent effect on ETH. Track ETH-specific catalysts separately in your market snapshot (Section 10) rather than assuming "crypto moved" always means BTC's narrative moved and everything followed.
- **The ETH/BTC ratio** is ETH's price quoted in BTC instead of dollars — the ETHBTC ticker on TradingView, mechanically (ETH price in USD) ÷ (BTC price in USD). It strips out the dollar-denominated moves BTC and ETH tend to share and isolates *relative* performance: a rising ratio means ETH is outperforming BTC (often "risk-on," altcoin-favorable conditions, formalized in Module 9's cycle analysis); a falling ratio means capital is consolidating into BTC — "BTC dominance rising" (Module 4, revisited in Section 6). This ratio belongs on your standing watchlist because, unlike a single asset's price (which conflates "is crypto up" with "is this asset preferred"), it isolates relative risk appetite and is always available to test — the kind of input your Module 20 playbook will formalize as a market-condition filter.

## 4. Beginner Concepts

- **Staking** secures Ethereum's proof-of-stake consensus, and staking flows are a real, second-order supply-side factor. A holder stakes ETH either by running a validator (locking 32 ETH) or, more commonly, through a staking pool or liquid-staking provider (pooling smaller amounts and issuing a receipt token). That ETH becomes collateral that can be destroyed ("slashed") for dishonest validator behavior, earning yield paid in newly issued ETH (the issuance side of Section 3's equation). Staked ETH is less liquid than unstaked ETH — historically not withdrawable at all, and even now withdrawals queue — so large shifts into or out of staking are a supply-side signal distinct from ordinary spot buying/selling. A wave of *unstaking* after a protocol change eases withdrawals represents previously locked ETH becoming freely tradeable — different pressure than a whale selling spot holdings. Recognize staking-queue changes as one of the context inputs Module 8 will have you track alongside exchange netflows.
- **Layer 2 networks** — Arbitrum, Base, Optimism, and others — are separate execution environments that process most everyday crypto activity (a swap, an NFT mint, a small DeFi position) far more cheaply than Ethereum mainnet, by batching transactions off-chain and periodically posting a compressed proof back to Ethereum, inheriting its security without their own validator set. This creates real tension in ETH's narrative: L2 growth is a tailwind for the "settlement layer" thesis (Section 3), since more L2 activity means more usage anchored to Ethereum's security. But because that activity happens *off* mainnet, it generates less of the gas revenue that historically fed EIP-1559's burn — so aggressive L2 growth can, short-term, reduce ETH's deflationary pressure even while strengthening its long-term relevance. Hold this trade-off as Hypothesis/Narrative, not Fact, until you've seen how it plays out.
- **Gas usage, the burn mechanism, and price action** is context you shouldn't over-read. "Gas" is the fee users pay to process a transaction; when usage spikes — an NFT mint, intense DeFi trading — gas prices rise as users bid for limited block space, and since the base fee is burned (Section 3), a high-usage period burns more ETH than a quiet one. It's tempting to treat "burn is spiking" as itself bullish — resist that. High burn tells you the network is being used heavily *right now*, useful background on network health, but it's not predictive: a burn spike can coincide with a rally (excited buying) or a selloff (panic selling and liquidations also generate heavy gas usage). Treat gas/burn data like most on-chain data in Module 8: probabilistic context, never a standalone trade signal.

## 5. Intermediate Concepts

- **ETH's volatility relative to BTC** has direct consequences for position sizing and stops under the same ICT framework. ETH has historically shown larger swings than BTC in both directions — rallies run further, drawdowns cut deeper — consistent with ETH being a "higher beta" asset: more sensitive to shifts in risk appetite, due to its smaller market cap, narrative sensitivity (Section 6), and heavier leveraged-derivatives representation (below). A stop distance and position size calibrated for BTC will often be too tight or too large for the "equivalent" ETH setup — an order block or FVG of similar significance may need a wider invalidation distance, and an unadjusted stop gets you stopped out by volatility, not by your thesis being wrong. Practice this in the Section 8 drill; the same principle — different numerical calibration — carries forward to altcoins and meme coins (Module 14), where the effect is far more extreme.
- **ETH/BTC correlation, and where it breaks down**, is easy to oversimplify. ETH and BTC usually move together with high correlation — both are "majors" held by the same large pool of participants, and a sharp move in either drags the other along (why Module 6 has you run a BTC-bias check before trusting an ETH setup). But usually-high correlation isn't constant: over multi-week and multi-month horizons the ETH/BTC ratio (Section 3) trends as capital rotates in relative preference, and during those windows the assets can diverge — ETH grinding higher against a flat or pulling-back BTC, or vice versa. These divergence windows are real, tradeable context, not noise. Part of what you're training across Modules 5–9 is distinguishing "both reacting to the same crypto-wide shift" from "capital rotating in preference" — the second has different implications for altcoins broadly (Module 9).
- **ETH's derivatives market** — funding rates, open interest, liquidations, the same mechanics from Module 4 — works identically in structure but often differently in *degree*. Funding is the periodic payment perp traders exchange to keep contract price tethered to spot; open interest is total notional value of outstanding positions; liquidations occur when a position's losses consume its margin and the exchange force-closes it. What differs on ETH is that its derivatives market often runs "hotter" — funding spikes higher, OI builds more aggressively relative to market cap, and liquidation cascades can be sharper — particularly during altcoin-favorable regimes (rising ETH/BTC ratio, falling BTC dominance) when speculative appetite concentrates in ETH and altcoins rather than BTC. The "funding is extreme, watch for a squeeze" read from BTC needs its own ETH-specific baseline — what's extreme on ETH isn't the same number as on BTC — which the Section 7 exercise calibrates by comparing ETH funding/OI to BTC's.

## 6. Advanced Concepts

- **Reading the ETH/BTC ratio as a regime filter** means cross-referencing it against BTC dominance (Module 4) before concluding on the broader market regime. When the ratio is rising *and* dominance is falling, the two numbers agree: capital is rotating out of BTC into ETH (and typically altcoins beyond it), corroborating a genuine risk-on shift (Module 9 builds a fuller cycle framework around this). When the ratio rises *without* a corresponding fall in dominance — ETH simply outperforming a rising BTC — that's a weaker, more ambiguous signal, possibly just an ETH-specific catalyst (Section 3) rather than a broader rotation. The general principle (Module 8's approach to on-chain and derivatives data): a single metric alone is weak evidence; two or more agreeing is meaningfully stronger — never proof.
- **ETH-specific on-chain data** — covered conceptually here, deepened with tooling in Module 8 — gives a window into the economic activity behind the settlement-layer narrative (Section 3). Stablecoin supply growth on Ethereum and its L2s is one signal: rising supply typically means fresh capital entering the ecosystem for DeFi, trading, or other activity — a leading indicator of future *capacity*, distinct from price. Exchange netflows for ETH (same concept as BTC's, Module 4) — net ETH onto exchanges (often read as sell pressure) versus off exchanges into self-custody or staking (accumulation intent) — and staking-queue changes (Section 4) round out this picture. Every one of these is context, not a predictor: stablecoin supply rising doesn't guarantee a rally, nor do exchange inflows guarantee a selloff — they shift the odds, nothing more.
- **ETH's heightened sensitivity to ecosystem-specific narrative and news**, relative to BTC, follows from the settlement-layer-versus-store-of-value distinction (Section 3). Because ETH's value proposition is about *usage* — will people build on it, will L2s keep growing, will institutions route activity through it — usage news moves ETH more than comparably-sized BTC news moves BTC: a major protocol upgrade, a significant exploit undermining DeFi confidence, and ETH-specific regulatory developments (ETF approval/rejection and flows) all carry outsized narrative weight. BTC's simpler "digital gold" narrative is less sensitive to equivalent news, since there's less of an "is the ecosystem succeeding" story to speak to. When building your ETH market snapshot (Section 10), expect more live, unresolved narrative items in the ETH column than in a comparable BTC snapshot — an accurate reflection of how these assets' stories differ, not a flaw in your analysis.

## 7. Practical Exercises

- Pull up the ETH/BTC ratio chart (TradingView ticker ETHBTC). Identify its recent trend (rising/falling/flat) over the last 1–3 months and cross-reference against BTC dominance's recent trend from Module 4 Day 18 — are they telling a consistent story?
- Check current ETH funding rate and OI (Coinglass) and compare qualitatively to BTC's from Module 4 Day 19 — which is running "hotter"?
- Mark a recent ETH daily/4H chart with market structure, liquidity, and at least one FVG/order block, same as the BTC exercise.

## 8. Drills

- **ETH/BTC regime drill:** given a hypothetical ETH/BTC ratio direction plus a hypothetical BTC dominance direction, state whether they corroborate a risk-on or risk-off read, or conflict (and if they conflict, what that itself tells you — uncertainty, not a clean signal).
- **Volatility-adjustment drill:** given the same ICT setup type on BTC and ETH, explain how you'd think differently about stop distance/position size given ETH's typically higher volatility.

## 9. Real-World Applications

- The ETH/BTC ratio becomes a standing input to your Module 9 cycle/narrative reads and your Module 20 playbook's "market condition" filter.

## 10. Challenges

- Produce a complete ETH market snapshot (mirroring the BTC one from Module 4): price/trend, ETH/BTC ratio direction, current funding/OI, one current ecosystem narrative (L2 growth, an upgrade, ETF flows, etc.), each labeled Fact/Hypothesis/Narrative.

## 11. Assessments

**Baseline (Day 22):** What do you currently know about ETH beyond "it's the second-biggest crypto"?

**Exit (Day 25):** Produce the full ETH market snapshot (Section 10), explain the current ETH/BTC ratio regime read against BTC dominance, and mark a recent ETH chart with ICT structure/liquidity/FVG correctly labeled.

## 12. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | Knows ETH exists, nothing structural or relational to BTC |
| Developing | Knows ETH facts in isolation, doesn't connect ETH/BTC ratio to dominance |
| Competent | Produces a full ETH snapshot and correctly reads the ETH/BTC-vs-dominance regime signal |
| Advanced | Marks ICT structure on ETH charts unprompted, adjusting for ETH's volatility profile |
| Highly Proficient | Integrates ETH-specific narrative sensitivity into trade context automatically |
| Mastery | Could teach someone else to read BTC-vs-ETH relative positioning end-to-end |

You need **Competent** to move to Module 6.

---

## 13. Day-by-Day Training Plan

### Day 22 — ETH Fundamentals: Supply, Staking, Burn, Ecosystem Role (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 10 | Write your current ETH knowledge (Section 11). |
| Lesson | 40 | Read §3–4: variable supply/EIP-1559 burn, staking, ETH as settlement layer, L2 role. |
| Research | 40 | Check current ETH net issuance (inflationary or deflationary right now) on a public ETH supply tracker, and note current total value/activity on major L2s. |
| Review/journal | 30 | Explain, from memory, why ETH's supply mechanism is fundamentally different from BTC's, and why that matters for a long-term holder vs. a short-term trader. |

### Day 23 — ETH Volatility & the ETH/BTC Ratio (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's supply-mechanism explanation. |
| Lesson | 30 | Read §5–6: ETH volatility vs. BTC, ETH/BTC ratio, regime-filter logic. |
| Chart work | 50 | Do the Section 7 ETH/BTC-vs-BTC-dominance cross-reference exercise. |
| Review/journal | 30 | Do the Section 8 ETH/BTC regime drill with today's real data. |

### Day 24 — ETH Derivatives & On-Chain Context (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall today's regime read. |
| Lesson | 25 | Read §5–6 derivatives/on-chain sections. |
| Practical | 45 | Check current ETH funding/OI on Coinglass and compare to BTC's; check current stablecoin-supply trend on Ethereum/L2s if available via your Module 2 tools. |
| Review/journal | 40 | Write the full ETH market snapshot draft (Section 10), labeling each item Fact/Hypothesis/Narrative. |

### Day 25 — Applying ICT to an ETH Chart + Exit Assessment (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's snapshot draft. |
| Chart work | 40 | Mark a recent ETH daily/4H chart with market structure, liquidity, and at least one FVG/order block. |
| Exit assessment | 50 | Present the full ETH snapshot and marked chart per Section 11's exit task. |
| Reflection | 20 | What's the clearest behavioral difference you've now observed between BTC and ETH? |

**If below Competent:** Day 26 repeats the snapshot/chart exercise with tighter feedback. **If Competent+:** move to Module 6 — Applying ICT to Crypto.
