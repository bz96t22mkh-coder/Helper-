# Module 3 — Crypto Market Mechanics

**Est. length:** 3 days (6 hours).
**Prerequisite:** Modules 1–2. **Feeds into:** Modules 4–5 (BTC/ETH analysis) and 12 (meme-coin tokenomics) both lean on this directly.

---

## 1. What You Need to Learn

Market cap, volume, liquidity, circulating/total/max supply, FDV, tokenomics, market depth, slippage, spread, order books vs. liquidity pools, price impact — i.e., exactly what makes a crypto price actually move.

## 2. Why It Matters

You already know price moves on order flow from futures. Crypto adds: fixed/inflationary/deflationary supply schedules, order-book *and* AMM-pool price discovery depending on venue, and assets where "market cap" is a number that can be almost meaningless if liquidity is thin (a common meme-coin trap you must be immune to by Module 12).

## 3. Foundational Concepts

Before any number on a chart means anything, you need to understand what that number is actually measuring — and just as importantly, what it is *not* measuring, because the gap between the two is where most beginner mistakes in crypto come from.

**Market capitalization (market cap)** is calculated as price × circulating supply, and it answers one specific question: what is the market, right now, collectively valuing every circulating unit of this asset at? That's it. It is a snapshot valuation multiplied out from the last traded price — no one wrote a check for the full market cap, and nowhere is that amount of capital actually sitting inside the project. It is also, critically, not what you'd receive if every holder tried to sell simultaneously: since price is set by the last trade, a wave of selling crashes the price on the way down, so the "market cap" evaporates precisely because people try to realize it — a mechanical fact, not a pessimistic take, and one that becomes dangerous to ignore on any asset where liquidity is thin (a meme-coin trap you must be immune to by Module 12).

**Volume** is the total value traded in a period — every buy and every sell, summed. On its own it tells you activity level; paired with price direction it tells you something about conviction. High volume accompanying a rising price suggests real participants are stepping in at size and agreeing on direction — a healthy signal. But high volume on a token whose price is flat or falling can mean the opposite of "activity": it can mean wash trading, where the same capital (often the project's own) trades back and forth between wallets purely to inflate the volume figure that discovery tools display, making a dead token look alive to newcomers scanning trending lists. You won't be able to reliably spot this yet — that comes with the ratio-based techniques in Module 13 — but you should already treat volume as a number that requires context, never as proof of genuine interest by itself.

**Liquidity** is the amount of capital sitting ready to transact near the current price — order-book depth on a centralized exchange (CEX), or the size of the pooled reserves on a decentralized exchange (DEX) automated market maker (AMM). This is the number that actually governs how much you can buy or sell before your own order starts moving the price against you, and it is a completely different thing from market cap. A token can carry an eye-catching market cap while the actual liquidity behind it — the capital available to absorb trades — is a tiny fraction of that figure. Learning to check liquidity as a first-class number, not an afterthought to market cap, is one of the single highest-value habits this course builds in you, because it's the mechanism behind nearly every "the chart looked fine and then I couldn't get out" story you'll hear from undisciplined meme-coin traders.

## 4. Beginner Concepts

**Circulating, total, and max supply** describe three different slices of a token's existence, and conflating them is one of the most common beginner errors. *Circulating supply* is the count of tokens actually in public hands and available to trade right now. *Total supply* adds in tokens that have been minted but are not yet circulating — held in a team allocation, a treasury, or locked under a vesting schedule that releases them gradually over time. *Max supply* is the hard ceiling: the total number of tokens that will ever exist, if the protocol has one at all. Bitcoin's max supply is fixed at 21 million by consensus rules that no single party can change (a fact you'll return to in Module 4's discussion of BTC's fixed-supply narrative); many other tokens have no max supply at all and are deliberately inflationary, meaning new supply is minted indefinitely, diluting existing holders over time unless demand grows to match it. Knowing which of the three numbers you're looking at — and which one a chart tool is actually quoting when it labels something "supply" — is a prerequisite for every other calculation in this section.

**FDV (Fully Diluted Valuation)**, calculated as price × max (or total) supply, exists precisely to correct for the blind spot that circulating-supply-based market cap leaves open. A token can look inexpensive by market cap — a small circulating supply multiplied by price yields a modest number — while its FDV, using the full eventual supply, reveals that the market cap will grow many times over as locked tokens unlock and enter circulation, absent some offsetting rise in demand. Concretely: if only 10% of a token's total supply is circulating today, and the other 90% unlocks to early investors and the team over the next two years, every one of those unlocks is a new source of sell pressure hitting the market regardless of how the chart looks in the meantime. This is a foundational read for both meme-coin and altcoin due diligence, and you'll formalize it into a specific red-flag check in §6 below and again in Module 12.

**Tokenomics** is the umbrella term for the complete design of a token's economic life: its supply schedule, how that supply was and will be distributed among team, investors, treasury, and public holders, the vesting schedule governing when locked allocations unlock, any burn or emission mechanisms that shrink or grow supply over time, and what real utility (if any) the token has that would generate organic demand independent of speculation. Tokenomics is a fundamental risk factor that exists entirely separate from anything a price chart shows you — a token can have a beautiful, textbook-bullish chart pattern while its tokenomics guarantee that a large, cheaply-acquired team allocation is about to unlock and get sold into whatever demand you're relying on. Reading tokenomics is chart-independent due diligence, and it's a skill this course builds specifically because ICT chart-reading, however good, cannot see it.

**The order book**, on a CEX, is the live, continuously-updating list of every open buy order (bids) and every open sell order (asks) at each price level away from the current price — it is the literal mechanism by which a centralized exchange matches buyers to sellers. The **spread** is the gap between the single best (highest) bid and the single best (lowest) ask; a tight spread means buyers and sellers are willing to transact very close to each other, itself a sign of a liquid, efficiently-priced market, while a wide spread signals thinner participation and higher cost simply to enter and exit a position.

**Market depth** takes the order book a step further by measuring how much order size sits within a given percentage band of the current price — for example, how much total buy-side size exists within 1% below the current price. Deep markets can absorb a large order with barely a ripple in price; thin markets show a depth chart with big gaps between price levels, meaning even a moderate-sized order has to "walk the book" through several price levels to get filled, moving the price meaningfully against the trader as it goes. This is the order-book-side version of the same underlying concept that governs slippage on a DEX, which you'll meet next.

## 5. Intermediate Concepts

**Slippage** is the gap between the price you expected when you placed an order and the price you actually received once it filled, and the cause is mechanical: your own order size moving through the available liquidity — whether that's working down through order-book levels on a CEX or shifting the ratio inside an AMM pool on a DEX. On deep liquidity this effect is negligible: a $500 market order on ETH/USDT barely registers against the enormous liquidity sitting at that price. On a brand-new meme coin with a shallow pool, that same $500 order can be a chart-moving event, visibly pushing the price up (or down, if you're selling) by a meaningful percentage in a single transaction. This is why "size your position appropriately for the liquidity you're trading into" is not a vague risk-management platitude in this course — it's a direct, calculable consequence of the mechanics you're learning right now.

**Price impact on AMMs** follows a more rigid, calculable relationship than order-book slippage does. Because a decentralized exchange pool prices assets algorithmically off the ratio of the two reserves sitting inside it (the constant-product formula underlying most AMMs), your trade size relative to the total pool size directly and predictably determines how much the price moves — a larger trade against a smaller pool always produces worse execution, following the same curve every time. This is different from an order book, where price impact depends on however buy and sell orders happen to be stacked at that moment, which can vary trade to trade even at similar sizes. Understanding that AMM price impact is a function you could actually calculate — rather than an unpredictable market condition — is exactly the kind of mechanical grounding that will let you reason about meme-coin liquidity quantitatively instead of just eyeballing a chart, starting in Module 12.

**Why market cap lies on low-liquidity assets** is the practical payoff of everything above, and it deserves to be stated as bluntly as possible: a token can display a headline market cap of $10 million on a discovery tool while the actual liquidity pool backing it holds only $8,000. In that scenario, a single $5,000 sell order isn't a rounding error — it could crash the price by 40% or more, because there simply isn't enough capital in the pool to absorb it without the price ratio shifting dramatically. This is the single most important habit this module aims to install: never evaluate market cap alone, always check it against liquidity in the same glance, because the two numbers answer different questions and only together do they tell you anything about real risk.

## 6. Advanced Concepts

**The FDV-to-market-cap ratio as a red-flag detector** turns the FDV concept from §4 into an active screening tool. When FDV sits far above current market cap, it means a large amount of supply is still locked and will eventually enter circulation — but the ratio alone doesn't tell you whether that's dangerous. The follow-up questions that actually matter are *when* that supply unlocks (a cliff next month is a very different risk than a linear vest over four years) and *to whom* it unlocks (a team/insider allocation with every incentive to sell into strength behaves very differently from a broad public allocation with no coordinated seller). A high ratio without answers to those two questions isn't yet a verdict — it's a flag that tells you exactly where to dig next, which is the posture this course wants you to hold toward every red flag you'll learn.

**The volume-to-liquidity ratio** is a mechanical tell for wash trading, introduced here so you understand *why* it works before Module 13 turns it into a formal technique. Genuine trading volume is bounded by how much liquidity exists to trade against — real buyers and sellers can only transact as fast as the pool or order book lets them without incurring painful slippage. So when you see daily volume that is many multiples of the entire liquidity pool size, that volume did not plausibly come from organic traders absorbing normal slippage on every trade; it's a strong signal that the same capital is cycling back and forth (often across wallets controlled by the same party) purely to inflate the volume figure that trending lists display to newcomers. Calculating this ratio takes ten seconds and instantly reframes an impressive-looking volume number as a warning sign instead of a green flag.

**Reflexivity in thin markets** describes a feedback loop that is largely absent on deep, liquid assets like BTC and ETH but dominates the behavior of illiquid meme coins: because there is so little liquidity to absorb trades, price on a thin asset is largely just a function of the last handful of trades. That price move itself becomes visible information — a rapid move gets noticed on a discovery-tool ranking, which more people see, who then trade based on the move they just saw, which produces the next move, and so on. This self-reinforcing loop is the mechanical reason meme coins are capable of the extreme, fast, seemingly-irrational price action they're known for, and it's also why "the chart," in the technical, statistically-meaningful sense you're used to from ICT futures trading, carries far less genuine information on these assets than it does on BTC or ETH — a distinction Module 14 will build directly on top of.

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
