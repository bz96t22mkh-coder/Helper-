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

- **What a meme coin is:** a token (almost always, not a coin — see Module 1 §3) created quickly, usually with no functional product, whose value proposition is attention, community, and narrative rather than utility or cash flow. Most are launched via a bonding-curve platform (e.g., Pump.fun-style) on Solana or deployed directly as an ERC-20/SPL token with an initial DEX liquidity pool.
- **Why they pump:** thin liquidity + attention spike (from a viral post, an influencer mention, a narrative fit, or a well-timed launch) → buying pressure moves price dramatically because there's little liquidity to absorb it (Module 3's price-impact mechanics, at their most extreme) → the price move itself becomes the story, attracting more attention/buyers (reflexivity, Module 3 §6).
- **Why they crash:** the same thin liquidity works in reverse — early holders/insiders sell into strength, liquidity gets pulled (sometimes maliciously, Module 13), attention moves to the next token, and with no fundamental floor, price can return most of the way to zero as fast as it rose. The overwhelming majority of meme coins go to (or near) zero — this is a base-rate fact, not pessimism.

## 4. Beginner Concepts

- **How communities form:** an early group (often the launcher's own network, or an organic viral moment) builds initial social presence (a Telegram/Discord, an X account) → engagement and meme content spread the token beyond the initial group → community size and energy become part of the pitch itself ("look how big/fast this community grew").
- **How memes become market narratives:** a meme coin latches onto something already culturally resonant (an existing meme, a current event, an animal, a public figure/moment) — the token's "story" is legible and shareable in a single image/phrase, which is precisely what makes it spreadable on social media. Legibility, not logic, drives virality here.
- **How liquidity affects price:** covered mechanically in Module 3 — thin liquidity pools mean small dollar amounts move price dramatically in both directions.
- **How market cap and supply affect price:** a low price per token with an enormous supply is not "cheap" — always compute market cap and compare it to liquidity (Module 3), never judge by the per-token price alone (a classic beginner trap: "it's only $0.0000001, it can 100x easily" ignores that it may already have a huge effective market cap).
- **How holder distribution affects price:** a token where the top 10 wallets hold 60%+ of supply carries enormous, catastrophic sell-pressure risk regardless of chart pattern — those wallets can dump into any rally. Distribution (percentage held by, say, the top 10/20/50 holders) is a first-class risk metric, formalized in Module 12.
- **How catalysts affect price:** an exchange listing, an influencer post, a viral moment, or a narrative-sector pump (Module 9) can each independently spike attention and price — identifying the *specific* catalyst (or the absence of one) behind a move is core discovery work.

## 5. BTC/ETH vs. Liquid-Altcoin vs. Meme-Coin Trading — The Real Differences

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

## 6. The Six-Step Pipeline (Full Detail in Modules 11–15)

```
DISCOVERY → VALIDATION → TRADE SETUP → EXECUTION → MANAGEMENT → EXIT
```

- **Discovery** (this module): finding a token worth looking at closer. Produces a *candidate*, not a decision.
- **Validation** (Modules 11–14): X/Twitter vetting, tokenomics/holder analysis, security/scam screening, on-chain due diligence, chart-reliability check. Produces a *qualified* or *rejected* token.
- **Trade setup** (Module 15): defining entry criteria, invalidation, position size, target — only for tokens that passed validation.
- **Execution, Management, Exit** (Module 15, practiced in Module 18): actually placing, managing, and closing the trade with discipline.

**Never skip straight from Discovery to Execution.** A trending token with a good story is a *lead*, not a *trade*.

## 7. Discovery Techniques & Tools

- **Trending/new-pair lists** (DEX Screener, Birdeye, Pump.fun "about to graduate" boards): scan for unusual volume or liquidity growth relative to the token's age — a 2-hour-old token with real organic volume growth is a different signal than one sitting flat.
- **Volume and liquidity changes:** a sudden spike in both (not just price) is more meaningful than price alone — price can be pumped by a single wallet; sustained volume/liquidity growth suggests broader participation.
- **Social momentum monitoring** (deep dive in Module 11): watching for a sudden spike in mentions/engagement around a specific token or narrative on X.
- **New-launch monitoring:** watching launch platforms for tokens fitting a currently-strong narrative (Module 9) at the moment of launch — highest risk, highest attention-timing sensitivity.
- **Narrative-shift monitoring:** when a sector narrative shifts (Module 9 §5), watching for the tokens best-positioned to capture the new attention, rather than only watching individual tokens in isolation.

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
