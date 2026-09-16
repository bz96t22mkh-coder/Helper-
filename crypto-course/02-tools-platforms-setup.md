# Module 2 — Tools, Platforms & Environment Setup

**Est. length:** 6 days (12 hours).
**Prerequisite:** Module 1 (Competent). **Feeds into:** everything — this is the toolkit and the live accounts you'll use for the rest of the course.

**Verification note:** Exchange availability, licensing, and fees change. Facts below were checked as of August 2026 (South Africa's FSCA CASP regime, live since June 2023) — re-verify current licensing and fees before depositing real funds.

---

## 1. What You Need to Learn

The complete toolkit for a crypto trader: exchanges/trading platforms, charting platforms, market-data platforms, token-discovery tools, DEX analytics, on-chain analytics, blockchain explorers, wallet-analysis tools, contract-analysis tools, scam-detection tools, X/Twitter research approach, news sources, portfolio trackers, and journaling tools — plus the practical setup: choosing an exchange, KYC, deposits/withdrawals, spot buy/sell, self-custody wallet setup, hardware wallets, network selection, gas, connecting/disconnecting wallets to DEXs, swapping, and slippage.

## 2. Why It Matters

You cannot analyze BTC dominance without a data source for it, vet a meme coin without a chart tool, explorer, and contract-analysis tool, or trade at all without an exchange and a safely set-up wallet. This module builds the entire operating environment before Module 3 asks you to analyze anything.

## 3. The Toolkit, by Category

For every tool: what it does, why you need it, how/when to use it, free-or-paid, difficulty, and what to look for. South Africa-relevant notes are flagged **[SA]**.

This toolkit is deliberately *not* one all-in-one platform — no such platform exists in crypto the way your futures broker's terminal bundled charting, execution, and data into one login. You'll run a small stack of specialized tools, each covering one layer: custody, execution, charting, discovery, verification. Free/Paid and Difficulty matter too: paid tiers are about data depth or automation, not paywalling beginner functionality, and a "Beginner" tool can still cause an irreversible mistake if you skip §4's security rules.

### 3.1 Exchanges (CEX) — fiat on/off-ramp and spot trading

A centralized exchange (CEX) is a custodial on-ramp between the ZAR in your bank account and crypto: until you withdraw, the exchange holds your funds and your account is a claim against their ledger, not direct ownership ("not your keys, not your coins," §3.2). South Africa's FSCA began regulating crypto asset service providers (CASPs) in June 2023. KYC (ID document + proof of address) is the legal mechanism letting a licensed CASP move fiat in and out of the regulated banking system on your behalf.

| Tool | What it does | Why you need it | Free/Paid | Difficulty | What to look for |
|---|---|---|---|---|---|
| Luno | ZAR deposit/withdraw, spot buy/sell BTC/ETH/major alts | Primary SA fiat on-ramp | Free account, trading fees apply | Beginner | **[SA]** FSCA-licensed CASP; supports ZAR bank transfer; good BTC/ETH liquidity, limited altcoin range |
| VALR | ZAR deposit/withdraw, spot + (newer) derivatives | SA-headquartered, broader asset range than Luno, often deeper liquidity | Free account, trading fees apply | Beginner–Intermediate | **[SA]** FSCA-licensed CASP since 2024; reported (Moneyweb, Oct 2025) as SA's first licensed crypto-derivatives issuer — verify current scope before using derivatives; check current fee schedule and available pairs |
| Binance | Global CEX, largest volume/liquidity, wide asset range, futures | Deepest liquidity for BTC/ETH derivatives data (funding/OI) even if you don't fund an account there | Free account, trading fees apply | Intermediate | Verify current SA regulatory status before depositing — it was not on the FSCA's licensed-provider list as of 2024; use for **market data only** if uncertain, and confirm current standing before moving funds |
| Kraken / Coinbase | Global CEXs, generally strong compliance track record | Alternative fiat/crypto on-ramps, good API data | Free account, fees apply | Beginner–Intermediate | Check ZAR support (often limited/absent — may require a stablecoin or card route) |

**Rule for this course:** use an **FSCA-licensed CASP** (Luno or VALR, verified current) for actual ZAR deposits/withdrawals and spot holdings; treat any other exchange as data-only until you've verified its legal standing for SA residents. Binance stays data-only rather than excluded because its volume makes it one of the best sources of the derivatives data (funding, OI) Module 8 depends on.

### 3.2 Self-custody wallets

A self-custody wallet flips the CEX's custodial model: instead of an exchange holding a balance for you, *you* hold a private key — cryptographic data that is the sole proof of ownership of whatever crypto is associated with it on-chain. There is no company, support line, or password reset behind it; the private key (represented as a human-readable **seed phrase**, typically 12 or 24 words) *is* the asset — anyone who has it has full, irreversible control, and losing it with no backup means the funds are gone forever. A **hot wallet** (MetaMask, Phantom) keeps that key on an internet-connected device, exposed to malware and phishing; a **hardware wallet** (Ledger, Trezor) keeps it on a dedicated offline device that never exposes the key to the internet, even when approving a transaction — the right tier once your holdings are worth more than you'd accept losing to a hot-wallet compromise. §4 covers the seed-phrase handling discipline that separates "self-custody" from "self-inflicted loss."

| Tool | What it does | Why | Free/Paid | Difficulty | Look for |
|---|---|---|---|---|---|
| MetaMask | Browser/mobile hot wallet for Ethereum + EVM chains (and L2s) | Standard for ETH/EVM DEX interaction | Free | Beginner | Only ever download from metamask.io or official app stores; verify the extension ID |
| Phantom | Browser/mobile hot wallet for Solana (and now multi-chain) | Standard for Solana meme-coin trading | Free | Beginner | Same install-source caution as above |
| Ledger / Trezor | Hardware wallets — private keys never touch an internet-connected device | Serious security tier for anything beyond small trading balances | Paid (~$60–150) | Intermediate | Buy **only** direct from the manufacturer or an authorized reseller — never a marketplace listing, never "pre-configured" |

### 3.3 Charting & market data

Charting and market-data tools exist because no single exchange interface gives the full picture. TradingView carries the same drawing tools, multi-timeframe workflow, and philosophy your ICT futures training relies on — the transfer is in interface and methodology, not the asset. Funding, open interest, and liquidation data are *not* price data — a separate category describing positioning and leverage under the price, which Module 8 builds a framework around. CoinGecko and CoinMarketCap aggregate fundamental data (market cap, supply, FDV — defined precisely in Module 3) across nearly the whole asset universe.

| Tool | What it does | Why | Free/Paid | Difficulty | Look for |
|---|---|---|---|---|---|
| TradingView | Charting with your existing ICT toolkit (drawing tools, multi-timeframe) on BTC/ETH spot and futures feeds | Where you'll do all BTC/ETH ICT chart work | Free tier usable; paid unlocks more indicators/alerts | Beginner (you already know this from ICT) | Use exchange-native data feeds (e.g., Binance perp feed) for volume/OI-relevant work |
| Exchange-native charts (Binance, Bybit) | Futures-specific data: funding, OI, liquidations directly on-chart | Needed for Module 8 | Free | Beginner | Cross-check numbers against a dedicated data site below |
| CoinGecko / CoinMarketCap | Market cap, supply, volume, FDV across nearly every asset | Fast fundamental snapshot of any coin/token | Free | Beginner | Circulating vs. total vs. max supply are easy to confuse — check which one a page is actually showing (Module 3 defines each) |
| Coinglass | Funding rates, open interest, liquidation heatmaps, long/short ratios | Core Module 8 data source | Free tier + paid | Intermediate | Aggregated-vs-single-exchange numbers can diverge — check which you're viewing |

### 3.4 Token discovery & DEX analytics (meme-coin core toolkit)

This category is the meme-coin trader's equivalent of a chart feed, covering a market structure different from the CEX order books you've used so far. New meme coins are typically born on a **launch platform** like Pump.fun, trading against a **bonding curve** — price rises mechanically as people buy directly from the curve, with no separate liquidity pool yet — before "graduating," once enough capital flows in, to a real pool on a DEX. A bonding-curve-stage token has no pool an outside seller could drain; a graduated token behaves like any AMM-priced asset, subject to everything Module 3 teaches about liquidity and price impact. Standard charting platforms don't index this universe of thousands of newly-created DEX pairs, which is why DEX Screener, DexTools, and Birdeye exist — their checks are a first pass, not a verdict (Modules 12–13).

| Tool | What it does | Why | Free/Paid | Difficulty | Look for |
|---|---|---|---|---|---|
| DEX Screener | Real-time DEX pair charts, volume, liquidity, holder count, trending lists across chains | Your primary meme-coin discovery + charting tool | Free (paid boosts exist for *projects*, not you) | Beginner–Intermediate | Liquidity size, age of pair, volume-to-liquidity ratio, whether trading is "paid-boosted" (marketing, not signal) |
| Birdeye | Solana-focused DEX analytics, holder distribution, security flags | Deep Solana meme-coin due diligence | Free tier + paid | Intermediate | Built-in security checks (mint authority, freeze authority) — verify independently, don't take a single tool's score as final |
| Pump.fun (and similar launch platforms) | Where a large share of new Solana meme coins are created/launched | Understanding the "birth" mechanism of tokens you'll research | Free to view | Beginner | Bonding-curve stage vs. "graduated" to a real DEX pool — very different risk profiles |
| DexTools | Similar to DEX Screener; pair discovery/charting across chains | Cross-check secondary source | Free tier + paid | Beginner–Intermediate | Same caution on paid trending/boosts as DEX Screener |

### 3.5 On-chain analytics & blockchain explorers

Every public blockchain records every transaction, wallet balance, and contract's code and interactions in a ledger anyone can read — this transparency is what a blockchain **explorer** exposes in a searchable interface (Etherscan for Ethereum, Solscan for Solana, equivalents elsewhere). Explorers function as *ground truth*: a chart tool can be misconfigured, a Twitter account can lie, but the explorer shows the actual, verifiable on-chain record. Nansen and Arkham layer wallet *labeling* on top of that raw data, and Bubblemaps visualizes holder relationships as a cluster map — same-sized, same-age wallets receiving tokens from the same source, a signature of insiders splitting an allocation to disguise concentration (Module 13–14).

| Tool | What it does | Why | Free/Paid | Difficulty | Look for |
|---|---|---|---|---|---|
| Etherscan (ETH) / Solscan (SOL) / BscScan etc. | Blockchain explorer — every transaction, wallet, and contract is public here | Ground-truth verification for anything a chart or Twitter account claims | Free | Intermediate (you'll build fluency across Modules 8, 14) | Contract "Read"/"Write" tabs, holder list, top-holder concentration, contract creator wallet |
| Nansen / Arkham | Wallet labeling, "smart money" tracking, fund-flow analysis | Identifying whether known/whale wallets are buying or dumping | Free tier limited; full access paid | Advanced | Labels can be wrong/outdated — verify, don't blindly follow |
| Bubblemaps | Visual holder-cluster mapping (spots wallets that are secretly linked) | Detecting bundled/insider wallet clusters (Module 13–14) | Free tier + paid | Intermediate | Clusters of same-sized, same-age wallets holding a large % — classic insider/bundle pattern |

### 3.6 Contract & security analysis

A token on a smart-contract chain isn't just a price on a chart — it's code, and that code can be written to be actively hostile to buyers. A **honeypot** is a contract coded so buying works but selling is blocked or taxed punishingly, trapping buyers; **mint authority**, if not renounced, lets whoever holds it create new tokens at will, diluting every holder; **freeze authority** lets a designated address freeze other wallets' balances, preventing them from trading. Token Sniffer, RugCheck, and GoPlus Security automate checking for these red flags plus liquidity lock/burn status, giving a fast first-pass screen. But automated scoring can't catch a contract that's technically "clean" yet has supply concentrated in insider wallets ready to sell in coordination — the gap manual explorer review closes, reading the holder list and owner privileges yourself rather than trusting a green checkmark. Module 13–14 builds this into a full due-diligence process.

| Tool | What it does | Why | Free/Paid | Difficulty | Look for |
|---|---|---|---|---|---|
| Token Sniffer / RugCheck / GoPlus Security | Automated contract-risk scoring (honeypot check, mint/freeze authority, ownership renounced, liquidity lock) | First-pass automated screen before manual due diligence | Free | Beginner–Intermediate | Treat "green flags" as necessary, not sufficient — always cross-check manually in Module 13 |
| Manual explorer check | Reading the actual contract/holder data yourself on Etherscan/Solscan | The automated tools above miss things; this doesn't | Free | Advanced (built in Module 13–14) | Top-10 holder %, LP lock/burn status, contract owner privileges |

### 3.7 X/Twitter, news, portfolio, journal

The last category covers the tools around your actual trading, not the mechanics themselves. X (Twitter) is where crypto narratives and catalysts break first — often a founder's tweet or an exchange's own account, before a listing hits a news site — which is why Module 11 builds a research methodology around it. That same speed makes X the easiest venue to fake a catalyst. Primary-source news outlets and official project/exchange accounts are your cross-check. Portfolio trackers should only ever get *read* access — anything asking for API withdrawal permission has no legitimate reason to. The journal is the connective tissue for the entire course; Module 16 covers structure, but the habit starts now.

| Tool | What it does | Why | Free/Paid | Difficulty | Look for |
|---|---|---|---|---|---|
| X (Twitter) — Search, Lists, Advanced Search | Real-time narrative/catalyst discovery | Core Module 11 tool | Free (some features paywalled) | Intermediate | Account age, follower-to-engagement ratio, verified vs. impersonation |
| CoinDesk / The Block / official project accounts / exchange announcement pages | Legitimate news and listing announcements | Distinguishing real catalysts from rumor | Free | Beginner | Primary source (the exchange/project itself) beats any secondhand account |
| CoinStats / Delta / a spreadsheet | Portfolio tracking across exchanges/wallets | Knowing your real exposure at a glance | Free tier + paid | Beginner | Never connect via API keys with withdrawal permission enabled |
| Notion / spreadsheet / plain markdown | Your two trading journals (Module 16) | Non-negotiable — this course is built around journaling everything | Free | Beginner | Structure over prettiness — see Module 16 templates |

## 4. Practical Setup (Phase 4) — What You'll Actually Do

**Security ground rules, stated once, that apply for the rest of your life in crypto:**
1. Never enter your seed phrase into a website, app, or "wallet recovery support" chat. A legitimate wallet never asks for it after initial setup.
2. Never screenshot, cloud-back-up, or type your seed phrase into a note app. Write it on paper (or a metal backup) and store it physically.
3. Only download wallet software from the official site/app store, verified by URL, not a search-ad or a link in a DM.
4. Start with small amounts until every step (deposit, withdraw, swap) is proven to work.
5. Use a dedicated "trading" hot wallet with limited funds for meme-coin/DEX activity — never your main holding wallet.

**The setup sequence:**
1. Choose your CEX (Luno or VALR, current FSCA-licensed status verified) → create account → complete KYC (ID document + proof of address; this is required by SA law for licensed CASPs) → deposit ZAR via bank transfer → buy a small amount of BTC and ETH at spot to learn the order flow (market vs. limit order, fees shown before confirming).
2. Install a self-custody hot wallet (MetaMask for EVM chains, Phantom for Solana) → generate a new wallet → write down the seed phrase on paper → verify it → understand the difference between your CEX balance (custodial) and your wallet balance (self-custody) once you withdraw a small amount from the CEX to your own wallet address.
3. Understand network selection: when withdrawing, you must match the network (e.g., ETH via ERC-20 vs. SOL via native Solana) between sender and receiver — sending to the wrong network can permanently lose funds. Always send a small test amount first on any new wallet/exchange pairing.
4. Practice a DEX swap: connect your wallet to a DEX (Jupiter for Solana, Uniswap for Ethereum), swap a small amount, and observe: the quoted price, the slippage-tolerance setting, the gas/fee estimate, and the final confirmation screen before signing.
5. Practice disconnecting your wallet from a site (via the wallet's "connected sites" setting) — get in the habit of disconnecting after every session.
6. Hardware wallet: not required for this phase's small test amounts, but decide now what threshold ("once my self-custody balance exceeds R___") triggers buying one (Ledger or Trezor, from the manufacturer or an authorized reseller only — never a marketplace listing) — you're not setting it up today, just fixing the number in advance so a hot-wallet-only habit doesn't quietly become permanent as balances grow.

## 5. Practical Exercises

- Build your own one-page "tool stack" reference sheet: one tool per category in §3, with what you'll use it for.
- Do the full setup sequence in §4 with small real amounts (your own money, your own decision on amount — this course never tells you how much to risk).

## 6. Drills

- **Network-matching drill:** given 3 hypothetical withdrawal scenarios (e.g., "sending USDC from Coinbase to a Solana wallet"), identify the correct network to select and what would go wrong if you picked the wrong one.
- **Tool-recall drill:** for each of the 7 categories in §3, name the primary tool from memory and its one main use, no notes.

## 7. Real-World Applications

- Every module from here uses this toolkit directly — Module 4/5 use TradingView + Coinglass; Modules 10–14 use DEX Screener, Solscan, RugCheck, and X.

## 8. Challenges

- Complete one full real deposit → buy → withdraw-to-self-custody → small DEX swap cycle, and write a short after-action note on anything that felt confusing or risky.

## 9. Assessments

**Baseline (Day 7):** List every crypto tool/app you've already used, if any, and what you used it for.

**Exit (Day 12):** (1) Name and describe the correct tool for 6 of the 7 categories in §3 from memory. (2) Walk through, step by step, how you'd safely withdraw ETH from a CEX to a new self-custody wallet, including the network-matching check. (3) State the 5 security ground rules from memory. (4) Confirm you've completed the real setup sequence (CEX account + KYC + one small buy; self-custody wallet created with seed phrase backed up; one small DEX swap practiced).

## 10. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | No accounts set up, or set up without understanding custody/network risk |
| Developing | Accounts exist but needed heavy guidance; can't recall tool categories unprompted |
| Competent | Full setup complete and safe; recalls tool stack and security rules unprompted |
| Advanced | Chooses the right tool for a new, unstated task without being told which category it falls in |
| Highly Proficient | Runs the full stack fluently as second nature by Module 8+ |
| Mastery | Could safely onboard someone else end-to-end, catching their mistakes before they happen |

You need **Competent** to move to Module 3.

---

## 11. Day-by-Day Training Plan

### Day 7 — Exchanges & Choosing Your CEX (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 10 | List any crypto tools/apps you've used already. |
| Lesson | 40 | Read §3.1 (exchanges) and the SA licensing verification note. |
| Research | 40 | Compare Luno vs. VALR current fees, supported assets, and confirm current FSCA-licensed status for both. |
| Practical | 20 | Create your CEX account and begin KYC. |
| Journal | 10 | Note which CEX you chose and why. |

**Objective:** pick and start onboarding to a licensed SA exchange with eyes open, not on brand recognition alone.

### Day 8 — Charting, Market Data & Portfolio Tools (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall your CEX choice rationale. |
| Lesson | 35 | Read §3.3 (charting/market data) and §3.7 (news/portfolio/journal). |
| Practical | 45 | Set up TradingView with BTC and ETH charts; create a free Coinglass account and locate current BTC funding rate and OI. |
| Practical | 20 | Set up a simple portfolio tracker or spreadsheet template (empty for now). |
| Journal | 10 | Record today's BTC funding rate and OI as your first data point. |

**Objective:** have a working chart + data environment before Module 3 needs it.

### Day 9 — Token Discovery & DEX Analytics (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall today's tool list for charting/data. |
| Lesson | 35 | Read §3.4 (token discovery/DEX analytics). |
| Practical | 45 | Open DEX Screener and Birdeye; browse the trending list for Solana — do not trade, just observe the interface: liquidity, volume, pair age, holder count columns. |
| Practical | 20 | Open Pump.fun and observe the bonding-curve vs. graduated-pool distinction on 2–3 live examples. |
| Journal | 10 | Write what "trending" showed you that felt suspicious vs. credible, purely on first impression (you'll formalize this in Module 13). |

**Objective:** get comfortable navigating the meme-coin discovery interfaces before any research/trading responsibility is attached.

### Day 10 — On-Chain, Contract Analysis, X/Twitter & News (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's DEX Screener observations. |
| Lesson | 35 | Read §3.5–3.7 (explorers, wallet/contract analysis, X/Twitter, news). |
| Practical | 40 | Open Etherscan and Solscan; look up ETH's largest exchange wallet and find a token contract's "Read Contract" tab to locate its holder list. Separately, note that BTC uses its own explorer (e.g. mempool.space) rather than Etherscan/Solscan. |
| Practical | 25 | Run one token through RugCheck or GoPlus Security and read every field it returns, even ones you don't yet understand. |
| Journal | 10 | List 3 fields from the contract scanner you don't yet understand — Module 13 will explain them. |

**Objective:** build first exposure to on-chain/contract tools ahead of the deep-dive modules.

### Day 11 — Practical Setup: CEX Funding & Self-Custody Wallet (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 5 | Recall the 5 security ground rules (§4) from memory before reading them again. |
| Lesson | 15 | Re-read §4 security ground rules and setup sequence carefully. |
| Practical | 60 | Complete CEX KYC if not done; deposit a small amount of ZAR; execute one small spot buy of BTC or ETH, reading every fee/confirmation screen before clicking. |
| Practical | 30 | Install MetaMask and Phantom; generate new wallets; write seed phrases on paper (never digitally); verify each phrase using the wallet's built-in verification step. |
| Journal | 10 | Confirm in writing: "My seed phrases are backed up on paper, not digitally, and I have not shared them with anyone or anything." |

**Objective:** complete your first real, careful custody transitions.

### Day 12 — Practical Setup: Withdrawal, Network Selection, DEX Swap & Exit (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall the network-matching risk from §4. |
| Practical | 40 | Withdraw a small amount from your CEX to your self-custody wallet, double- and triple-checking the network matches before confirming. |
| Practical | 40 | Connect your wallet to a DEX (Jupiter/Uniswap) and execute one small swap, observing quoted price, slippage setting, and fee before signing. Disconnect the wallet afterward. |
| Exit assessment | 20 | Complete the Section 9 exit task in full. |
| Reflection | 10 | What felt riskiest today, and what would you double-check next time? |

**Objective:** finish Module 2 with a fully working, safely-set-up trading environment and a genuine understanding of every step you took.
**After today you should be able to:** independently onboard to a CEX, self-custody safely, and execute a DEX swap without hand-holding.

**If exit assessment lands below Competent:** Day 13 repeats the weakest setup step with a second small transaction under closer scrutiny before moving on. **If Competent+:** move to Module 3.
