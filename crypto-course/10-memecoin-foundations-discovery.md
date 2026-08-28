# Module 10 — Meme-Coin Foundations & Discovery

**Est. length:** 5 days (10 hours). This is the start of your second full specialization — treated with the same seriousness as BTC/ETH, not as a side curiosity.
**Prerequisite:** Modules 1–9 (you need the fundamentals, tools, mechanics, and cycle-reading skills already built). **Feeds into:** every remaining meme-coin module (11–15, 21).

**Standing rule for this entire specialization:** discovering a token is not a reason to buy it. Discovery is step one of a six-step pipeline (§5); every token you find here goes through Modules 11–14 before Module 15 ever produces a trade decision.

---

## 1. What You Need to Learn

What meme coins are; why they pump; why they crash; how communities and narratives form around them; how liquidity, market cap, supply, and holder distribution affect price; the real difference between BTC/ETH trading, liquid-altcoin trading, and meme-coin trading; and how skilled meme-coin traders actually find opportunities (X/Twitter, DEX analytics, token scanners, explorers, wallet trackers, trending lists, volume/liquidity changes, new launches, narrative shifts).

## 2. Why It Matters

Meme coins are not "small versions of BTC." They're a structurally different asset class: near-zero fundamental value proposition, extreme and rapid liquidity/ownership concentration, social-attention-driven pricing, and survivorship measured in days or weeks for the vast majority. Treating meme-coin trading like BTC/ETH trading with smaller position size is how skilled traders lose money fast here — this module builds the correct mental model before Module 15 builds the trading framework.

## 3. Foundational Concepts

**What a meme coin is**, precisely, matters because getting the definition right changes what risks you expect from day one. It's a token — almost always, not a coin, using the distinction built in Module 1 §3, meaning it has no independent blockchain or validator set of its own — created quickly, usually with no functional product behind it at all, whose entire value proposition is attention, community, and narrative rather than utility, revenue, or cash flow of any kind. Most are launched one of two ways: via a bonding-curve platform (Pump.fun on Solana is the archetype), where the token's price follows a preset mathematical curve as people buy in before it "graduates" to a full decentralized-exchange listing, or deployed directly as an ERC-20 (Ethereum) or SPL (Solana) token paired with an initial liquidity pool on a DEX from day one. Understanding which launch path a given token took tells you something immediately about its current stage and risk profile — a bonding-curve token that hasn't graduated yet trades in a fundamentally different (and often more fragile) liquidity environment than one already trading against a real, externally-funded liquidity pool.

**Why they pump** follows a specific mechanical chain worth tracing link by link rather than treating as a mystery of "hype": it starts with thin liquidity — most meme coins have only a small pool of capital actually available to trade against — combined with an attention spike, whether from a viral post, an influencer mention, a fit with a currently-hot narrative (Module 9), or simply a well-timed launch. That attention spike brings buying pressure, and because the liquidity pool absorbing that buying is so small, price moves dramatically for a given dollar amount of buying — this is Module 3's price-impact mechanics operating at their most extreme, where a few thousand dollars of buying can move price by multiples rather than fractions of a percent. Crucially, the price move itself then *becomes* the story: a chart that's up 400% in an hour is itself now shareable, screenshot-able content that draws in more attention and more buyers independent of whatever the original catalyst was — this is reflexivity (Module 3 §6) in its purest form, where the price action and the narrative feed each other in a loop that has nothing to do with any underlying fundamental value.

**Why they crash** is the same thin-liquidity mechanism working in reverse, and understanding it removes any mystery from what otherwise looks like a sudden, inexplicable collapse: early holders and insiders — who bought before the attention spike, often at a fraction of the peak price — sell into the strength the reflexive pump created, absorbing what little buying pressure remains; liquidity itself can get pulled from the pool entirely, sometimes maliciously by the token's own deployer (a "rug pull," covered in full in Module 13); attention, which is the only thing propping the token up in the first place, moves on to whatever the next viral token or narrative is; and with no fundamental floor of any kind — no revenue, no product, no reason a rational buyer would step in "because it's cheap" — price can give back most of its gain as fast as, or faster than, it rose. The base rate here is not pessimism, it's simply an honest statistic worth sitting with before you trade a single one: the overwhelming majority of meme coins go to, or very near, zero, and the ones that don't are the memorable exceptions you hear about, not the norm you should expect.

## 4. Beginner Concepts

**How communities form** around a meme coin typically follows a recognizable pattern: an early group — often the launcher's own existing network, or the participants in whatever organic viral moment sparked the token — builds an initial social presence, usually a Telegram or Discord server and an X account, in the first hours after launch. From there, engagement and meme content (jokes, edited images, in-group references) spread the token beyond that initial group as more people discover and share it, and — this is the part worth watching closely as a trader — the community's size and energy become part of the pitch itself: "look how fast this grew" or "look how many people are in the Telegram" gets used as evidence of the token's legitimacy or momentum, even though a large, fast-growing community is a symptom of successful marketing and virality, not proof of any underlying value or durability.

**How memes become market narratives** hinges on a single mechanic: a meme coin succeeds at spreading when it latches onto something already culturally resonant — an existing meme, a current event, an animal, a public figure or a specific viral moment — because that gives the token a "story" that's legible and shareable in a single image or phrase, without requiring anyone to understand any underlying technology or thesis. This is why *legibility*, not logic, drives virality in this specific market: a token needs to be explainable and shareable in the time it takes someone to glance at a tweet, not defensible in a whitepaper, and the tokens that succeed at spreading are frequently the ones that are easiest to "get" instantly, regardless of whether there's any substance behind them at all.

**How liquidity affects price** was covered mechanically back in Module 3, and it applies here at its most extreme: thin liquidity pools mean that even small dollar amounts of buying or selling move price dramatically in both directions, which is precisely why meme coins can 10x on modest buying volume and just as easily collapse on modest selling — there simply isn't enough capital sitting in the pool to cushion the price against either direction.

**How market cap and supply affect price** is one of the most common beginner traps in this entire specialization, so it's worth stating plainly: a low price per token combined with an enormous total supply is not "cheap" in any meaningful sense — always compute the token's full market cap (price × circulating supply) and compare *that* number to the size of its liquidity pool (Module 3), rather than ever judging opportunity by the per-token price alone. The classic version of this trap sounds like "it's only $0.0000001, it can 100x easily" — but a token priced at $0.0000001 with 500 trillion tokens in circulation already has a market cap in the tens of millions of dollars, meaning it needs genuinely large new capital inflows to 100x from there, exactly like any other asset would; the tiny per-token price is an artifact of supply, not a sign of being early or undervalued.

**How holder distribution affects price** is a risk dimension entirely separate from the chart: a token where the top 10 wallets hold 60% or more of total supply carries enormous, potentially catastrophic sell-pressure risk regardless of how clean or bullish its chart pattern looks, because any one of those large wallets can dump into a rally at any moment, instantly overwhelming the thin liquidity described above and erasing the move (and anyone who bought into it) in minutes. This is why holder distribution — typically expressed as the percentage of supply held by the top 10, top 20, or top 50 wallets — is treated in this course as a first-class risk metric on par with liquidity itself, not a minor detail, and gets formalized into a full due-diligence checklist in Module 12.

**How catalysts affect price** rounds out this section: an exchange listing, an influencer's post, a sudden viral moment, or a broader narrative-sector pump (Module 9) can each independently spike attention and price on their own, and a single token can be hit by more than one at once. The core discovery skill worth building from day one is not just noticing that a token moved, but identifying the *specific* catalyst behind the move — or noticing the honest absence of one, which is itself an important, slightly more suspicious signal (a move with no identifiable catalyst is harder to have any conviction about, in either direction, than one you can point to a clear cause for).

## 5. BTC/ETH vs. Liquid-Altcoin vs. Meme-Coin Trading — The Real Differences

It's tempting, coming from an ICT futures background, to treat meme-coin trading as "the same skills, just applied to a smaller, more volatile asset" — smaller position size, same chart-reading approach, same risk-management logic, just scaled down. That assumption is the single most dangerous mental shortcut in this entire specialization, because several of the dimensions below aren't matters of *degree* between these three asset classes, they're matters of *kind* — meme coins don't just have "more" of the risks BTC/ETH have, they frequently have risks that simply don't exist at all in BTC/ETH trading (total, permanent loss of the underlying liquidity itself, for one, covered fully in Module 13). The table below lays out eight dimensions where the differences are real and structural, not cosmetic, and the paragraphs that follow it walk through why several of the more important rows work the way they do.

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

The **chart reliability** row deserves special attention given your ICT background, because it's the row most likely to trip you up. Your ICT edge on BTC/ETH works because those markets have deep, genuine institutional-scale participation — large, sophisticated players whose order flow leaves real footprints (liquidity pools, fair value gaps, order blocks) that recur because the same kinds of participants keep behaving in similar ways across market structure. A brand-new meme coin with $40,000 of liquidity has none of that: its "chart" can be, and often is, the footprint of a single wallet's buying and selling, or the mechanical output of a bonding curve, rather than the aggregated behavior of a genuine market. That doesn't mean chart reading is *useless* on meme coins — liquidity, support/resistance, and volume still mean something — but it means the confidence you're entitled to place in a meme-coin chart pattern is systematically lower than the confidence the same-looking pattern would earn you on BTC or ETH, a distinction built out fully in Module 14. The **backtestability** row matters for a related reason: your Module 7 backtesting process depends on market conditions recurring in similar-enough ways across history that a tested edge has predictive value going forward — but the meme-coin environment (which platforms are popular, which chains have the cheap/fast infrastructure, what kind of narrative currently attracts capital) changes so quickly that a backtest from six months ago may already describe a market that no longer exists, a limitation examined directly in Module 16.

## 6. The Six-Step Pipeline (Full Detail in Modules 11–15)

```
DISCOVERY → VALIDATION → TRADE SETUP → EXECUTION → MANAGEMENT → EXIT
```

This pipeline exists because meme-coin trading has a uniquely short distance between "I noticed this" and "I could lose real money on this" — a trending token is one tap away from a buy button on most discovery tools — and that speed is exactly why a forced, six-stage structure matters more here than almost anywhere else in trading. Each stage below produces a specific output and exists to stop a specific failure mode.

**Discovery** (this module) means finding a token worth looking at more closely — using the tools and techniques in §7 below — and it produces a *candidate*, nothing more. At this stage you know almost nothing verified about the token beyond what a screener shows you: its age, its current liquidity and market cap, and why it caught your attention. Treating a discovery-stage candidate as anything more than a name on a watchlist is the first place traders go wrong, because a token can look identical at the discovery stage whether it turns out to be a legitimate (if still highly speculative) community token or an outright scam contract designed to look identical to one.

**Validation** (Modules 11–14) is where the real work happens: X/Twitter vetting (is the attention organic or manufactured — Module 11), tokenomics and holder-concentration analysis (Module 12), security and scam screening (Module 13 — checking the contract itself for the mechanisms that let a deployer rug the liquidity or freeze your ability to sell), and an on-chain due-diligence and chart-reliability check (Module 14). This stage produces a binary outcome — *qualified* or *rejected* — and the overwhelming majority of discovery-stage candidates should get rejected here; that's the process working correctly, not a sign you're being too conservative.

**Trade setup** (Module 15) only happens for tokens that survived validation, and it means defining, in advance and in writing, your entry criteria, your invalidation point (the condition under which you accept you were wrong and exit), your position size, and your target — the same disciplined pre-commitment your ICT training already taught you for futures, applied here with even tighter constraints given the asset class's volatility.

**Execution, Management, and Exit** (defined in Module 15, practiced live in Module 18) is simply the discipline of actually placing, managing, and closing the trade according to the plan you already committed to, rather than improvising once real money and real emotion are involved.

**Never skip straight from Discovery to Execution.** A trending token with a good story is a *lead*, not a *trade* — and the entire purpose of naming these six stages explicitly, rather than leaving the process implicit, is to make it obvious, every single time, exactly which stage a given token is currently sitting at in your own process, so that "I found something exciting" never quietly gets treated as "I've done the work to trade this."

## 7. Discovery Techniques & Tools

**Trending and new-pair lists** — platforms like DEX Screener, Birdeye, and Pump.fun's "about to graduate" board — surface tokens by recent activity rather than requiring you to already know what you're looking for. The skill here isn't just scrolling the list; it's scanning for unusual volume or liquidity growth *relative to the token's age*, since a 2-hour-old token with real, organic-looking volume growth is a meaningfully different, more interesting signal than a 2-week-old token sitting flat with the same absolute numbers — age gives you the denominator that turns a raw number into a rate, and rate is what actually signals momentum.

**Volume and liquidity changes** matter more than price alone because price, on a thin pool, is trivially manipulable by a single well-funded wallet, while sustained growth in *both* volume and the underlying liquidity pool size is much harder to fake and suggests genuinely broader participation rather than one actor pushing a number around. A token whose price is up 50% on the back of a single large buy looks very different, on closer inspection, from one whose price is up 50% alongside a steadily growing pool of liquidity and dozens of distinct wallets trading it — the first is fragile and can reverse the instant that one wallet sells, the second has actual breadth behind it.

**Social momentum monitoring** — a full skill built out in Module 11 — means watching for a sudden spike in mentions, replies, or engagement around a specific token or a specific narrative on X, since social attention is the actual fuel behind a meme coin's price in a way it simply isn't for BTC or ETH. At the discovery stage you're only watching for the spike itself as a reason to look closer, not yet trying to judge whether that attention is organic or manufactured — that judgment call is exactly what Module 11 exists to teach.

**New-launch monitoring** means watching launch platforms in real time for tokens that fit a currently-strong narrative (Module 9) at the literal moment of launch, on the theory that a token launching directly into an already-hot narrative has a timing advantage a token launching into narrative indifference doesn't. This is simultaneously the highest-attention-timing-sensitivity technique here and the highest-risk, since a brand-new token has had zero time to accumulate any of the validation signals (Modules 11–14) that separate a legitimate community token from a scam built to look like one.

**Narrative-shift monitoring** takes the opposite vantage point from watching individual tokens: rather than tracking specific names, you watch for the *moment* a sector narrative shifts (Module 9 §5) and then ask which tokens are best-positioned to capture the newly-arriving attention — sometimes an existing token that already has infrastructure and community in that sector, sometimes a brand-new one launching to specifically capture it. Thinking at the narrative level first, and only then at the individual-token level, mirrors exactly the top-down cycle-and-narrative discipline built in Module 9, applied here at a more granular, tactical timescale.

## 8. Practical Exercises

- Spend a discovery session (no trading) on DEX Screener/Birdeye/Pump.fun, and log 5 candidate tokens using only discovery-stage information: name, chain, age, market cap, liquidity, 24h volume, and why it caught your attention (specific reason, not "it looked good").
- For each of the 5, write a one-line note on which pipeline stage it's currently at for you (all should currently be "Discovery — not yet validated").

## 9. Drills

- **Pump-mechanism drill:** given a hypothetical token's liquidity size and a hypothetical buy order size, explain mechanically why price would move the way it does.
- **Distribution red-flag drill:** given a hypothetical top-10-holder percentage, state whether it's a green, yellow, or red flag and why (formalized fully in Module 12, previewed here).

## 10. Real-World Applications

- Every discovery session for the rest of this course (and your real trading life) starts with the toolkit and discipline built in this module.

## 11. Challenges

- Explain, in your own words, why "I found it early" is not the same as "I validated it" — and why skipping validation is the single most common way meme-coin traders lose money on an otherwise-legitimate-looking token.

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
