# Module 3 — Crypto Market Mechanics

**Est. length:** 3 days (6 hours).
**Prerequisite:** Modules 1–2. **Feeds into:** Modules 4–5 (BTC/ETH analysis) and 12 (meme-coin tokenomics) both lean on this directly.

---

## 1. What You Need to Learn

Market cap, volume, liquidity, circulating/total/max supply, FDV, tokenomics, market depth, slippage, spread, order books vs. liquidity pools, price impact — i.e., exactly what makes a crypto price actually move.

## 2. Why It Matters

You already know price moves on order flow from futures. Crypto adds: fixed/inflationary/deflationary supply schedules, order-book *and* AMM-pool price discovery depending on venue, and assets where "market cap" is a number that can be almost meaningless if liquidity is thin (a common meme-coin trap you must be immune to by Module 12).

## 3. Foundational Concepts

- **Market capitalization (market cap)** = price × circulating supply. It answers "what is the market currently valuing all circulating tokens at" — it is **not** how much money has "gone into" the asset, and it is **not** how much you'd get if everyone sold (that would crash the price long before the last seller, especially with thin liquidity).
- **Volume** = total value traded in a period. High volume + rising price = conviction. High volume + flat/falling price on a token can mean wash trading (fake volume) — a Module 13 red flag.
- **Liquidity** = how much capital sits ready to trade near the current price (order-book depth on a CEX, or pool size on a DEX). Liquidity, not market cap, determines how much you can actually buy/sell before price moves against you.

## 4. Beginner Concepts

- **Circulating supply**: tokens currently in public hands/trading. **Total supply**: circulating + tokens minted but locked/reserved (team, treasury, vesting). **Max supply**: the hard cap that will ever exist (BTC: 21M; some tokens have no max supply — inflationary).
- **FDV (Fully Diluted Valuation)** = price × max (or total) supply. A token can look "cheap" by market cap while FDV reveals a huge amount of future supply that will eventually unlock and dilute holders — critical in meme-coin and altcoin analysis.
- **Tokenomics**: the full design of a token's supply, distribution, vesting schedule, emissions/burns, and utility. Bad tokenomics (huge team allocation unlocking soon, no real distribution) is a fundamental risk factor independent of chart pattern.
- **Order book** (CEX): a live list of buy (bid) and sell (ask) orders at each price level. **Spread** = gap between best bid and best ask — tight spread = liquid market.
- **Market depth**: how much size sits within a given % of current price on the order book — thin depth means a moderate order causes a large price move.

## 5. Intermediate Concepts

- **Slippage**: the difference between the price you expected and the price you actually got, caused by your own order size moving through the book/pool. Large on thin liquidity, small on deep liquidity — this is why the same $500 trade is a non-event on ETH/USDT and a chart-moving event on a brand-new meme coin.
- **Price impact on AMMs**: because DEX pools price algorithmically off the ratio of two assets, your trade size relative to pool size directly determines your price impact — there's a real, calculable relationship (bigger trade relative to pool = worse price), unlike an order book where impact depends on how orders are stacked.
- **Why market cap lies on low-liquidity assets**: a token can show a "$10M market cap" while its actual liquidity pool holds $8,000 — meaning a $5,000 sell could crash price 40%+. Always check liquidity *alongside* market cap, never market cap alone.

## 6. Advanced Concepts

- **FDV/market-cap ratio as a red flag detector**: a very high FDV relative to current market cap signals large future dilution (unlocks) — ask *when* and *to whom* that supply unlocks before assuming today's price action will hold.
- **Volume-to-liquidity ratio**: unusually high daily volume relative to pool size can indicate wash trading (fabricated volume to appear active) rather than genuine interest — a Module 13 technique, introduced here mechanically.
- **Reflexivity in thin markets**: on illiquid assets, price *is* largely a function of the last few trades, which itself changes sentiment, which drives the next few trades — a feedback loop that produces the extreme, fast moves meme coins are known for, and why "the chart" carries far less statistical information there than on BTC/ETH (foreshadowing Module 14).

## 7. Practical Exercises

- Pick BTC, ETH, and one large-cap altcoin: record price, circulating supply, market cap, total supply, max supply, and FDV for each (CoinGecko/CoinMarketCap). Note which ones have a max supply and which don't, and what that implies long-term.
- Pick one meme coin on DEX Screener: record market cap, liquidity pool size, and 24h volume. Calculate volume ÷ liquidity and market cap ÷ liquidity. Flag anything that looks disproportionate.

## 8. Drills

- **Slippage-estimate drill:** given a hypothetical pool size and trade size, reason through (no exact formula needed) whether slippage would be small, moderate, or severe.
- **FDV-trap drill:** given two hypothetical tokens' market cap and FDV, identify which one carries more future-dilution risk and why.

## 9. Real-World Applications

- Every BTC/ETH analysis in Modules 4–5 uses volume/liquidity/depth as inputs. Every meme-coin qualification in Module 12 starts with market cap vs. liquidity vs. FDV.

## 10. Challenges

- Find one real token where market cap looks attractive but liquidity is dangerously thin, and write 3 sentences explaining exactly what would happen if you tried to exit a meaningful position.

## 11. Assessments

**Baseline (Day 13):** Explain, in your own current understanding, what market cap means and whether it tells you how much money is "in" an asset.

**Exit (Day 15):** Given a real or hypothetical token's price, circulating supply, max supply, and liquidity pool size, calculate market cap and FDV, and state whether the liquidity is adequate relative to the market cap — with reasoning, not a guess.

## 12. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | Treats market cap as "money invested"; unaware of liquidity vs. market cap gap |
| Developing | Knows the definitions but doesn't check them together in practice |
| Competent | Reliably checks market cap, liquidity, and FDV together before judging a token's size/risk |
| Advanced | Spots wash-trading and dilution red flags from raw numbers unprompted |
| Highly Proficient | Applies this instinctively while scanning DEX Screener trending lists |
| Mastery | Could teach someone else why "market cap" alone is a trap |

You need **Competent** to move to Module 4.

---

## 13. Day-by-Day Training Plan

### Day 13 — Market Cap, Supply, FDV (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 10 | Write your current understanding of market cap (Section 11). |
| Lesson | 35 | Read §3–4: market cap, volume, liquidity, circulating/total/max supply, FDV. |
| Research | 45 | Do the Section 7 exercise for BTC, ETH, and one large-cap altcoin. |
| Review/journal | 30 | Explain, from memory, why FDV can reveal a risk that market cap alone hides. |

### Day 14 — Order Books, AMMs, Slippage, Depth (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's FDV explanation. |
| Lesson | 35 | Read §4–5: order books, spread, market depth, slippage, AMM price impact. |
| Practical | 45 | On TradingView/exchange, examine BTC/ETH order-book depth at a few price levels; on DEX Screener, examine one meme-coin's liquidity pool size vs. a recent large trade's visible price impact on the chart. |
| Review/journal | 30 | Write the slippage-estimate drill (Section 8) for 2 hypothetical scenarios. |

### Day 15 — Wash Trading, Reflexivity, Exit Assessment (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall order-book vs. AMM pricing differences. |
| Lesson | 25 | Read §6: volume-to-liquidity red flags, reflexivity in thin markets. |
| Practical | 40 | Do the Section 7 meme-coin liquidity exercise (market cap ÷ liquidity, volume ÷ liquidity) on a real trending token. |
| Exit assessment | 35 | Complete Section 11's exit task. |
| Reflection | 10 | What's the single biggest mechanical mistake a beginner makes by trusting market cap alone? |

**If below Competent:** Day 16 repeats the liquidity/FDV analysis on a fresh token with tighter feedback. **If Competent+:** move to Module 4 — BTC Specialization.
