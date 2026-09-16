# Module 10 — Meme-Coin Foundations & Discovery

**Est. length:** 5 days (10 hours). Your second full specialization — treated with the same seriousness as BTC/ETH, not a side curiosity.
**Prerequisite:** Modules 1–9 (you need the fundamentals, tools, mechanics, and cycle-reading skills already built). **Feeds into:** every remaining meme-coin module (11–15, 21).

**Standing rule for this entire specialization:** discovering a token is not a reason to buy it. Discovery is step one of a six-step pipeline (§6); every token you find here goes through Modules 11–14 before Module 15 produces a trade decision.

---

## 1. What You Need to Learn

What meme coins are; why they pump and crash; how communities and narratives form around them; how liquidity, market cap, supply, and holder distribution affect price; the real differences between BTC/ETH, liquid-altcoin, and meme-coin trading; how skilled traders find opportunities (trending/new-pair lists, volume/liquidity changes, social-momentum monitoring, new launches, narrative shifts); and the six-step Discovery→Validation→Trade Setup→Execution→Management→Exit pipeline governing every token you find.

## 2. Why It Matters

Meme coins are not "small versions of BTC." They're a structurally different asset class: near-zero fundamental value, rapid liquidity/ownership concentration, social-attention-driven pricing, and survivorship measured in days or weeks for most. Treating meme-coin trading like BTC/ETH trading with smaller position size is how skilled traders lose money fast here — this module builds the correct mental model first.

## 3. Foundational Concepts

**What a meme coin is:** almost always a token, not a coin (Module 1 §3), with no independent blockchain of its own — created quickly with no functional product, valued on attention, community, and narrative rather than utility or cash flow. Most launch via a bonding-curve platform (Pump.fun on Solana is the archetype), price following a preset curve until it "graduates" to a full DEX listing, or directly as an ERC-20/SPL token paired with a liquidity pool from day one. The launch path signals risk: a pre-graduation token trades in a more fragile environment than one on a real, externally-funded pool.

**Why they pump** follows a mechanical chain, not "hype." Thin liquidity — most meme coins have only a small pool of capital to trade against — combines with an attention spike: a viral post, an influencer mention, a hot narrative (Module 9), or a well-timed launch. That spike brings buying pressure that, against so small a pool, moves price dramatically — Module 3's price-impact mechanics at their most extreme, where a few thousand dollars can move price by multiples of a percent. The move itself then *becomes* the story: a chart up 400% in an hour draws in more buyers regardless of the catalyst — reflexivity (Module 3 §6), price and narrative feeding each other with no link to fundamental value.

**Why they crash** is the same mechanism in reverse — four mechanisms, often at once. Early holders and insiders, who bought before the spike at a fraction of peak price, sell into the strength the pump created. Liquidity can get pulled entirely, sometimes maliciously by the deployer (a "rug pull," Module 13). Attention — the only thing propping the token up — moves to the next viral token. With no fundamental floor (no revenue, no product, no reason to buy "because it's cheap"), price gives back its gain as fast as it rose. Base rate: most meme coins go to, or near, zero — survivors are memorable exceptions, not the norm.

## 4. Beginner Concepts

**How communities form:** an early group — the launcher's network, or participants in the viral moment that sparked the token — builds a Telegram/Discord and X presence within hours. Meme content then spreads it further. Watch closely: community size becomes part of the pitch — "look how fast this grew" — though fast growth signals marketing, not underlying value.

**How memes become market narratives:** a meme coin spreads when it latches onto something culturally resonant — an existing meme, a current event, an animal, a public figure — giving it a story shareable in a single image, no technical understanding required. *Legibility*, not logic, drives virality: the tokens that spread are usually just the easiest to "get" instantly, regardless of substance.

**How liquidity affects price** — covered in §3 and Module 3 — earns its own line: liquidity, not market cap or narrative strength, determines how violently a given amount of buying or selling moves price.

**How market cap and supply affect price:** a low per-token price with an enormous total supply isn't "cheap." Always compute full market cap (price × circulating supply) against liquidity pool size (Module 3). The classic trap: "it's only $0.0000001, it can 100x easily" — but at $0.0000001 with 500 trillion tokens circulating, market cap is already in the tens of millions, needing real new capital to 100x. The tiny price is an artifact of supply, not a sign of being early.

**How holder distribution affects price:** a token where the top 10 wallets hold 60%+ of supply carries catastrophic sell-pressure risk regardless of chart — any one wallet can dump into a rally, overwhelming thin liquidity and erasing the move in minutes. Holder concentration (top 10/20/50 wallet %) is a first-class risk metric on par with liquidity, formalized in Module 12.

**How catalysts affect price:** an exchange listing, an influencer's post, a viral moment, or a narrative-sector pump (Module 9) can each spike attention and price. The core skill is identifying the *specific* catalyst behind a move — or noting its absence, itself a suspicious signal.

## 5. BTC/ETH vs. Liquid-Altcoin vs. Meme-Coin Trading — The Real Differences

Coming from an ICT futures background, it's tempting to treat meme-coin trading as the same skills scaled down — smaller size, same chart-reading, same risk logic. That's the most dangerous shortcut in this specialization: several dimensions below are differences of *kind*, not *degree* — meme coins frequently carry risks that don't exist in BTC/ETH trading at all (total, permanent loss of underlying liquidity, Module 13). The table lays out eight structural differences; the paragraphs after explain the most important rows.

| Dimension | BTC/ETH | Liquid Altcoin (top ~50–100 by market cap) | Meme Coin |
|---|---|---|---|
| Fundamental backing | Strong (scarcity/settlement thesis, real usage) | Moderate (real product/usage, varies widely) | Essentially none — attention/community only |
| Liquidity | Deep | Moderate–deep, varies | Often extremely thin, especially early |
| Holder concentration risk | Low | Low–moderate | Frequently severe |
| Chart reliability (ICT-style TA) | High — genuine institutional-scale participation | Moderate | Often low — see Module 14 on when charts stop containing reliable information |
| Typical lifespan | Established, ongoing | Established, ongoing (though many alts also fail over years) | Days to weeks for most; rare survivors |
| Primary driver of price | Macro flows, adoption, supply schedule, broad market structure | Sector narrative + fundamentals + broad market | Social momentum + narrative + liquidity mechanics, almost entirely |
| Backtestability | Yes (Module 7) | Partially | Very limited — environment changes too fast (Module 16) |
| Appropriate position sizing logic | Standard ICT risk management | Standard, slightly more conservative | Materially smaller, with hard, pre-committed max-loss thinking (Module 17) |

The **chart reliability** row is the one most likely to trip you up. Your ICT edge on BTC/ETH works because those markets have deep institutional participation whose order flow leaves real footprints (liquidity pools, fair value gaps, order blocks) that recur. A brand-new meme coin with $40,000 of liquidity has none of that — its "chart" is often just one wallet's buying and selling, or a bonding curve's mechanical output. The confidence a meme-coin chart pattern earns is systematically lower than the same pattern on BTC or ETH (Module 14). **Backtestability** suffers similarly: conditions need to recur across history (Module 7) for a tested edge to hold, but the meme-coin environment changes so fast that a six-month-old backtest may already describe a market that no longer exists (Module 16).

## 6. The Six-Step Pipeline (Full Detail in Modules 11–15)

```
DISCOVERY → VALIDATION → TRADE SETUP → EXECUTION → MANAGEMENT → EXIT
```

This pipeline exists because meme-coin trading has a uniquely short distance between "I noticed this" and "I could lose real money on this" — a trending token is one tap from a buy button. Each stage below produces a specific output and stops a specific failure mode.

**Discovery** (this module) means finding a token worth a closer look (§7) — it produces a *candidate*, nothing more, verified only by what a screener shows: age, liquidity, market cap, why it caught your attention. Treating a candidate as more than a watchlist name is the first place traders go wrong — a legitimate community token and a scam contract can look identical here.

**Validation** (Modules 11–14) is where the real work happens: X/Twitter vetting (Module 11), tokenomics/holder-concentration analysis (Module 12), security/scam screening (Module 13), and an on-chain/chart-reliability check (Module 14). It produces *qualified* or *rejected* — most candidates should get rejected here, which is the process working correctly.

**Trade setup** (Module 15) only happens for tokens that survived validation: your entry criteria, invalidation point (where you accept you were wrong and exit), position size, and target — defined in writing, the same pre-commitment your ICT training taught you for futures, with tighter constraints here given the volatility.

**Execution, Management, and Exit** (Module 15, practiced live in Module 18) means placing, managing, and closing the trade per the plan you committed to, not improvising once real money and emotion are involved.

**Never skip straight from Discovery to Execution.** A trending token with a good story is a *lead*, not a *trade* — naming these six stages keeps it obvious which stage a token is at, so "I found something exciting" never becomes "I've done the work to trade this."

## 7. Discovery Techniques & Tools

**Trending and new-pair lists** — DEX Screener, Birdeye, Pump.fun's "about to graduate" board — surface tokens by recent activity. Scan for volume or liquidity growth *relative to age*: a 2-hour-old token with real growth is more interesting than a 2-week-old token flat at the same numbers — age turns a raw number into a rate.

**Volume and liquidity changes** matter more than price alone: price on a thin pool is trivially manipulable by one wallet, while growth in *both* volume and liquidity is harder to fake. A token up 50% on one large buy differs from one up 50% alongside a growing pool and dozens of distinct wallets — the first reverses the instant that wallet sells, the second has real breadth.

**Social momentum monitoring** — built out fully in Module 11 — means watching for a sudden spike in mentions or engagement around a token or narrative on X, a meme coin's actual fuel in a way it isn't for BTC or ETH. At discovery you're only flagging the spike — judging whether it's organic is Module 11's job.

**New-launch monitoring** means watching launch platforms in real time for tokens fitting a currently-strong narrative (Module 9) at the moment of launch — a timing advantage over indifference. It's the highest-risk technique too: a brand-new token has had zero time to accumulate the validation signals (Modules 11–14) separating a legitimate token from a scam built to look like one.

**Narrative-shift monitoring** takes the opposite vantage point: instead of tracking tokens, watch for the *moment* a sector narrative shifts (Module 9 §5) and ask which tokens are best-positioned to capture it — an existing token with infrastructure there, or a new one built to capture it — mirroring Module 9's top-down discipline at a tactical timescale.

## 8. Practical Exercises

- Spend a discovery session (no trading) on DEX Screener/Birdeye/Pump.fun, and log 5 candidate tokens using only discovery-stage information: name, chain, age, market cap, liquidity, 24h volume, and why it caught your attention (specific reason, not "it looked good").
- For each of the 5, write a one-line note on which pipeline stage it's currently at for you (all should currently be "Discovery — not yet validated").

## 9. Drills

- **Pump-mechanism drill:** given a hypothetical token's liquidity size and a hypothetical buy order size, explain mechanically why price would move the way it does.
- **Distribution red-flag drill:** given a hypothetical top-10-holder percentage, state whether it's a green, yellow, or red flag and why (formalized fully in Module 12, previewed here).

## 10. Real-World Applications

- Every discovery session for the rest of this course, and your real trading life, starts with the toolkit built in this module.

## 11. Challenges

- Explain, in your own words, why "I found it early" is not the same as "I validated it" — and why skipping validation is the most common way meme-coin traders lose money on an otherwise-legitimate-looking token.

## 12. Assessments

**Baseline (Day 41):** What do you currently believe determines whether a meme coin goes up or down?

**Exit (Day 45):** Run a full discovery session and produce 5 logged candidate tokens with complete discovery-stage data, correctly explain the BTC/ETH-vs-altcoin-vs-meme-coin differences table from memory, and correctly state the six-step pipeline and why Discovery alone never justifies a trade.

## 13. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | Buys based on "it's trending" / a hot tip, no discovery discipline |
| Developing | Can browse discovery tools but doesn't log structured candidate data |
| Competent | Runs a structured discovery session, logs candidates correctly, understands the six-step pipeline |
| Advanced | Distinguishes organic momentum from manufactured hype at first glance |
| Highly Proficient | Discovery becomes a fast, repeatable daily habit with consistent quality |
| Mastery | Could teach someone else the discipline of "discovery is not a decision" |

You need **Competent** to move to Module 11.

---

## 14. Day-by-Day Training Plan

### Day 41 — What Meme Coins Are, Why They Pump/Crash (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 10 | Write your current belief about what determines meme-coin price (Section 12). |
| Lesson | 45 | Read §3: what a meme coin is, why they pump, why they crash. |
| Research | 45 | Browse 3 real meme coins' price charts (past pumps/crashes, no trading) and, for each, write a one-line hypothesis on what likely drove the pump and the crash. |
| Review/journal | 20 | Explain, from memory, the reflexivity loop that drives a meme-coin pump. |

### Day 42 — Communities, Narratives & the Trading-Type Comparison (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's pump/crash hypotheses. |
| Lesson | 40 | Read §4–5: community formation, meme-to-narrative mechanics, holder distribution/market cap/liquidity effects, and the BTC/ETH vs. altcoin vs. meme-coin comparison table. |
| Practical | 40 | Pick one real, currently-trending meme coin and identify: its narrative hook, its rough holder-concentration signal (top holders %, if visible on your Module 2 tools), and its liquidity size. |
| Review/journal | 30 | Do the Section 9 distribution red-flag drill using today's real token. |

### Day 43 — Discovery Tools & Techniques (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall today's holder-concentration/liquidity findings. |
| Lesson | 30 | Read §7: trending lists, volume/liquidity changes, social momentum, new-launch monitoring, narrative-shift monitoring. |
| Practical | 60 | Run your first structured discovery session (Section 8): log 5 candidate tokens with full discovery-stage data. |
| Review/journal | 20 | Note which discovery technique (trending list, new-launch board, narrative-driven search) produced your most interesting candidate, and why. |

### Day 44 — The Six-Step Pipeline & Discipline (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's 5 candidates. |
| Lesson | 30 | Read §6: the full Discovery→Validation→Setup→Execution→Management→Exit pipeline, and why skipping stages is the core risk. |
| Practical | 50 | Run a second discovery session, logging 5 more candidates, explicitly tagging each with its current pipeline stage (all "Discovery"). |
| Review/journal | 30 | Write the Section 11 challenge answer in your own words. |

### Day 45 — Integration & Exit Assessment (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall the six-step pipeline from memory. |
| Practical | 40 | Run a final discovery session for the exit assessment — 5 fresh candidates, full data. |
| Exit assessment | 50 | Present your candidates and answer the Section 12 exit questions (comparison table, pipeline, why discovery ≠ decision). |
| Reflection | 20 | What was your gut instinct wrong about, if anything, this week? |

**If below Competent:** Day 46 repeats one more discovery session with tighter feedback on data completeness and pipeline discipline. **If Competent+:** move to Module 11 — X/Twitter Research & Narrative Literacy.
