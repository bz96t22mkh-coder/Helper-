# Module 13 — Meme-Coin Security & Scam Detection

**Est. length:** 3 days (6 hours). Treat this as non-negotiable, not optional caution.
**Prerequisite:** Modules 2, 11, 12. **Feeds into:** Module 14 (on-chain confirmation of these patterns), Module 15 (framework's no-trade conditions), Module 21 (playbook security section).

---

## 1. What You Need to Learn

How to identify rug pulls, honeypots, malicious contracts, fake tokens/websites/X accounts/influencers/partnerships, fake volume, wash trading, insider dumping, bundled wallets, concentrated ownership, liquidity manipulation, pump-and-dumps, wallet drainers, phishing, fake airdrops, and malicious token approvals — and build **THE ULTIMATE MEME-COIN SAFETY CHECKLIST** to run before interacting with any unfamiliar token or site.

## 2. Why It Matters

Most meme-coin losses aren't "the trade went against me" — they're a scam mechanism doing exactly what it was built to do. This module's checklist is the single highest-leverage thing in this entire course for capital preservation.

## 3. Contract & Wallet-Level Threats

**Rug pull** is the baseline threat this course treats as most important — the most common, the most final, and the easiest to prevent with a single check. The mechanism: the developer or deployer withdraws the liquidity pool entirely, if it was never locked or burned (Module 12 §4), instantly collapsing the token's price to near zero, since the liquidity pool is what lets anyone convert the token back into another asset. Once it's pulled, holders aren't merely down on paper — they're holding a token with no real market to sell into at any price resembling what they paid. This scam is prevalent because it takes almost no technical sophistication: deploy a standard token contract, then execute a single withdrawal transaction whenever you choose. **Direct check:** LP lock/burn status (Module 12 §4), verified on-chain rather than taken on the project's word, is the single most important defense here — checkable in minutes before you risk capital.

**Honeypot** describes a contract coded so buying functions normally — drawing in buyers who see a rising price and no problem — while selling is blocked or heavily restricted for anyone except a list of approved wallets, typically the deployer's own. The asymmetry is what makes it effective: nothing about the buying experience gives any warning, so a buyer only discovers the trap when a sell transaction fails or returns a tiny fraction of expected value, by which point their capital is already committed. **Direct check:** run the token through a dedicated honeypot-detection tool (Module 2's RugCheck/GoPlus) *before* buying, not after — these tools simulate a sell against the live contract and surface a sell restriction invisible from the buy side alone — and treat any scanner flag as disqualifying rather than something to explain away because the chart or community looks appealing.

**Malicious contract functions** extend the honeypot's logic into capabilities embedded in a contract's code and triggered at the owner's discretion. Unrenounced mint authority lets the owner create unlimited new tokens, diluting or outright destroying existing holders' value on demand. Freeze/blacklist authority lets the owner block specific wallets from trading at all, narrowly (targeting large holders about to sell) or broadly. Modifiable transaction tax lets the owner spike the buy or sell tax to near-100% at will — not technically blocking a sale, but making it financially meaningless. These functions are dangerous precisely because they can sit dormant, unused, for as long as the deployer wants a token to look legitimate, only to be activated once enough capital has flowed in. **Direct check:** Module 12 §5's contract-permissions review, every time, with no exceptions for a token that "looks legitimate" — that's exactly the state a contract with dormant malicious functions is designed to project.

**Malicious token approvals** exploit a mechanism that's normally necessary for using any DEX: to let a smart contract move your tokens on your behalf (required for a standard swap), you grant it an "approval." The vulnerability appears when that approval is set to an *unlimited* amount rather than the exact amount needed, and the contract receiving it is malicious from the start or later upgraded to malicious behavior. An unlimited approval, once granted, remains valid indefinitely until you explicitly revoke it — giving that contract standing permission to move your full balance whenever it chooses, not just at the moment you approved it. A drainer contract disguised as an ordinary-looking dApp (a swap interface, a staking page, a mint page) can request this kind of broad approval, then later use it to empty your wallet of that token — and in some approval schemes, of more than just the one token. **Direct check:** approve only the exact amount needed for the transaction wherever your wallet interface allows it, rather than accepting the default "unlimited" approval many interfaces suggest, and periodically review and revoke old, unneeded approvals using a reputable revocation tool (services in the revoke.cash style — verify which tool is currently recommended, since the landscape shifts).

**Wallet drainers** are the most direct, front-line version of this threat category: malicious sites or contracts built around getting you to sign a single transaction or message that, the moment it's signed, transfers assets out of your wallet with no further interaction required. They're routinely disguised as something you'd want to interact with anyway: a mint page for a free NFT, a claim page for a token airdrop, or an innocuous "connect wallet to verify you're human" prompt. The signature is the entire attack — no separate hack of your wallet or keys, just a request worded so that what you're authorizing isn't what you think it is. **Direct check:** never sign a transaction or message you don't fully understand — read what your wallet's signature prompt is actually requesting, not just what the website around it claims it's for — and treat any unsolicited "connect your wallet" link as hostile until proven otherwise. This is also why this course insists on a dedicated, limited-funds trading wallet for meme-coin activity (the checklist's wallet-hygiene section, below): a drainer can only take what that specific wallet is holding or has approved, so a wallet that never holds more than you'd accept losing puts a hard ceiling on the damage any single drainer attempt can do.

## 4. Market-Manipulation Patterns

**Fake volume / wash trading** is the on-chain counterpart to the bot engagement covered in Module 11 §6 — instead of manufacturing the appearance of social interest, an entity trades with itself, or with a set of coordinated wallets it controls, to manufacture trading volume that doesn't actually exist. The purpose is to make a token look more actively traded, and therefore more legitimate, than the genuine participant count would produce on its own. **Direct check:** apply Module 3's volume-to-liquidity ratio red flag (also in Module 12 §3), then check on the explorer whether that volume is concentrated in a small number of wallets trading back and forth rather than spread across many independent addresses — genuine organic volume has a wide base of participants, wash-traded volume typically does not.

**Insider dumping** is the mechanism by which the wallet-level concentration you measured in Module 12 §4 turns into realized losses for other holders: early or insider wallets — those that acquired their position before public trading or in its earliest minutes — sell into the liquidity that later retail buying creates. This explains the common pattern of a fast, exciting pump immediately followed by an even faster crash: the "pump" is often retail demand arriving in response to rising price and attention, and the "crash" is the early wallets taking that demand as their exit. **Direct check:** track whether large recent sell transactions map to addresses already identified as early/insider wallets during your Module 12 analysis — if the biggest sellers during a price drop are the same wallets that got in first, that's not a coincidence worth explaining away.

**Bundled wallets** are the technique that makes insider dumping harder to see coming: many wallets that appear independent — different addresses, no obvious naming pattern connecting them — but were actually funded from the same source and act in coordination, buying, holding, and selling together on a shared schedule. The purpose is to disguise concentrated ownership as broad, healthy distribution: a holder count that looks like "500 independent wallets" can in reality be 20 people (or one) controlling 25 wallets each. **Direct check:** Bubblemaps-style cluster visualization (introduced in Module 2, deepened in Module 14) traces funding relationships between wallets and makes these clusters visible even when the addresses give no hint of the connection.

**Concentrated ownership** was covered as a static risk measurement in Module 12 §4; it belongs here too because it's the precondition that makes insider dumping and coordinated pump-and-dump schemes mechanically possible. A token where ownership is spread across thousands of independent holders cannot be dumped by "a decision," because no single decision controls enough supply to matter; a token where a handful of wallets or a bundled cluster controls a large share can be, at any moment those wallets choose. Every manipulation pattern in this section ultimately depends on concentration existing somewhere upstream of it.

**Liquidity manipulation** works by adding or removing liquidity strategically — not to trade the token, but to shape what the *chart* looks like to observers. A common version: briefly adding liquidity to make the pool look healthier right before a bigger, planned sell, since a deeper pool absorbs a large sell with less visible price impact, making the exit look calmer than it would against a thin pool. **Direct check:** watch liquidity-pool size as a trend over time rather than checking it once — a pool that grows suddenly for no stated reason, especially before or during unusual selling, deserves the same suspicion as a sudden sell itself.

**Pump-and-dump schemes** tie several of the above patterns into a coordinated campaign: a group — sometimes informal, sometimes a private Telegram or Discord group sold as "alpha calls" — buys a token together, deliberately spiking its price and drawing attention, then publicizes the move to attract retail buyers. Once retail demand provides real buying pressure, the organizing group sells into it, realizing gains directly funded by the later buyers' capital. **Direct check:** be maximally suspicious of any explicit "get in now" or "don't miss this" urgency tactic — genuine opportunities rarely require manufactured time pressure — especially from a group with a checkable history of similar calls followed by similar crashes.

## 5. Social-Layer Threats (Cross-Reference Module 11)

**Fake tokens and copycat contracts** are one of the most common real-world scam vectors, and unlike other threats here it targets the discovery moment itself: a scammer deploys a brand-new contract using the identical name and ticker as a trending, legitimate token, sometimes within minutes of the real one gaining attention, betting that traders searching by name will click the wrong contract address and buy the impostor instead. Because DEX Screener, Birdeye, and similar tools let anyone search by name or ticker, and a name and ticker cost nothing to copy, this scam requires only speed and a trending name to imitate — no technical sophistication at all. **Direct check:** never trust a name or ticker alone; verify the actual contract address against a primary source — the real project's own official account or website — before buying, every time, even (especially) when a token is moving fast and the name looks exactly right.

**Fake websites** are near-identical clones of a real project's official site, often hosted on a lookalike domain that differs from the real one by a single character, a different top-level domain, or a subtly altered spelling — built to harvest wallet connections and, in the worst cases, seed phrases entered directly into a fake "connect" or "recovery" flow. Because the visual clone can be pixel-perfect, appearance alone is not a reliable defense; the domain itself is the only thing that can't be perfectly copied. **Direct check:** always navigate to a project's site via a bookmark saved after verifying it once, or by typing the URL manually from a source you trust — never via a search-engine ad (ads can be bought for a lookalike domain) or a link sent in a DM.

**Fake X accounts and impersonation** were covered mechanically in Module 11 §6 as a credibility problem; here, the same pattern is also a direct security threat, not merely a source of bad information. An impersonation account isn't just spreading a false claim — it's frequently the delivery vehicle for a phishing link, a fake airdrop, or a direct DM-based scam, so the Module 11 credibility check and this module's security check are, in this case, the same check performed for two different reasons.

**Fake influencers and fake partnerships** are claims of an endorsement, collaboration, or official partnership that don't check out against the claimed party's own official channels — the same primary-source verification principle from Module 11 §4, applied to claims designed to borrow a well-known name's credibility. A token claiming "backed by [well-known figure]" with no corroborating post on that figure's own account should be treated as false until proven otherwise, not plausible until disproven.

**Fake airdrops** are among the most common and most effective wallet-drainer vectors because they exploit a genuinely pleasant expectation — free tokens for existing holders — that legitimate projects do sometimes deliver, which is what makes the fake version convincing. The pattern is an unsolicited message claiming "you're eligible for a free airdrop, connect your wallet or sign this message to claim it," when the actual purpose of that signature is to drain the wallet, not deliver anything. **Direct check:** treat any unsolicited airdrop claim as hostile until proven otherwise through the project's own verified official channel, and never sign anything to "claim" a reward without independently confirming its legitimacy across multiple sources first — a genuine airdrop can wait the few minutes verification takes; a drainer is counting on you not taking them.

**Phishing via DMs and fake support** covers any account reaching out directly — claiming to be "support," a team member, or offering an "exclusive opportunity" — through a channel that pressures you to act quickly and privately, away from scrutiny where the claim might get corrected. **Direct check:** legitimate teams and wallet/exchange support never DM first to ask for a seed phrase, a wallet connection, or urgent action — any message that does is not a borderline case, it is definitionally a scam attempt.

## 6. THE ULTIMATE MEME-COIN SAFETY CHECKLIST

Run this in full before buying, connecting a wallet to, or approving any interaction with an unfamiliar token or site:

**Contract & Liquidity**
- [ ] LP is locked or burned (not held freely by the deployer)
- [ ] Contract ownership is renounced, or the remaining owner privileges are understood and acceptable
- [ ] No active mint authority (or it's provably disabled)
- [ ] No freeze/blacklist authority
- [ ] Buy/sell tax is fixed and reasonable, not owner-modifiable to an extreme
- [ ] Ran through an automated scanner (RugCheck/GoPlus or equivalent) with no unexplained red flags

**Holders & Wallets**
- [ ] Top-10 holder concentration checked and acceptable for the risk you're taking
- [ ] Developer/deployer wallet history checked (not actively dumping)
- [ ] No obvious bundled-wallet cluster pattern (Bubblemaps or equivalent)

**Market Behavior**
- [ ] Volume-to-liquidity ratio checked, no unexplained wash-trading signature
- [ ] No signs of a coordinated pump group pushing urgency

**Social Layer**
- [ ] Contract address verified against a primary source, not just the name/ticker (copycat-contract check)
- [ ] Any claimed partnership/listing/endorsement verified at the primary source
- [ ] Official site URL verified manually, not via a link from a DM/ad
- [ ] Account posting about the token passed the Module 11 credibility checklist

**Your Own Wallet Hygiene**
- [ ] Using a dedicated trading wallet with limited funds, not your main holding wallet
- [ ] Not signing any transaction/message you don't fully understand
- [ ] No unsolicited "claim your airdrop" actions taken without independent multi-source verification
- [ ] Token approvals reviewed/limited, with periodic revocation of unused approvals

**If any box is unchecked and you don't have a specific, reasoned justification for proceeding anyway, don't proceed.**

## 7. Practical Exercises

- Run the full checklist on 2 real tokens from your Module 12 analyses — did anything change your conclusion from the fundamentals-only pass?
- Find one real historical case (news coverage is fine) of a rug pull, a honeypot, or a wallet-drainer scam, and identify exactly which checklist item, if checked beforehand, would have caught it.

## 8. Drills

- **Checklist-speed drill:** time yourself running the full checklist on a fresh token — aim to get faster without skipping items.
- **Scam-pattern-matching drill:** given a hypothetical scenario description, identify which specific scam type (rug pull, honeypot, wash trading, drainer, etc.) it matches.

## 9. Real-World Applications

- This checklist is a hard gate in your Module 15 trading framework's Validation stage, and the full checklist itself becomes a section of your Module 21 meme-coin playbook.

## 10. Challenges

- Explain to an imagined beginner, in under 2 minutes, why "the chart looks amazing" is never sufficient justification to skip this checklist.

## 11. Assessments

**Baseline (Day 53):** What crypto scams, if any, have you already heard of, and how would you currently try to avoid them?

**Exit (Day 55):** Run the complete Section 6 checklist on a real, unfamiliar token live, correctly identifying every check's status and giving a clear pass/fail/proceed-with-caution verdict with reasoning.

## 12. Mastery Criteria

| Level | Looks like |
|---|---|
| Beginner | No systematic scam checks, relies on gut feeling |
| Developing | Aware of scam types, doesn't run a complete checklist |
| Competent | Runs the full checklist reliably and reaches a reasoned verdict |
| Advanced | Spots subtle red flags (e.g., a slowly increasing insider concentration) unprompted |
| Highly Proficient | Checklist becomes fast, automatic habit on every new token |
| Mastery | Could teach someone else to build and use this checklist from scratch |

You need **Competent** to move to Module 14.

---

## 13. Day-by-Day Training Plan

### Day 53 — Contract & Wallet-Level Threats (2h)

| Segment | Min | What to do |
|---|---|---|
| Baseline | 10 | Write your current scam awareness (Section 11). |
| Lesson | 45 | Read §3: rug pulls, honeypots, malicious contract functions, malicious approvals, wallet drainers. |
| Practical | 45 | Check your own wallet's current token approvals using a revoke-style tool (Module 2); revoke any you don't recognize or need. |
| Review/journal | 20 | Explain, from memory, exactly how a wallet drainer typically operates. |

### Day 54 — Market-Manipulation & Social-Layer Threats (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall yesterday's approval-review findings. |
| Lesson | 40 | Read §4–5: wash trading, insider dumping, bundled wallets, liquidity manipulation, pump-and-dumps, fake sites/accounts/airdrops, phishing. |
| Practical | 50 | Find one real historical scam case and match it to a specific pattern (Section 7). |
| Review/journal | 20 | Do the Section 8 scam-pattern-matching drill on 3 hypothetical scenarios. |

### Day 55 — Building & Applying the Ultimate Checklist, Exit Assessment (2h)

| Segment | Min | What to do |
|---|---|---|
| Review | 10 | Recall today's scam-pattern matches. |
| Lesson | 15 | Read §6: the full Ultimate Meme-Coin Safety Checklist. |
| Practical | 45 | Run the checklist on 2 real tokens from Module 12. |
| Exit assessment | 40 | Run the checklist on a fresh, unfamiliar token live and give a full pass/fail/caution verdict. |
| Reflection | 10 | Write the Section 10 challenge answer. |

**If below Competent:** Day 56 repeats the checklist on 2 more fresh tokens with closer feedback on any missed or shallow checks. **If Competent+:** move to Module 14 — Meme-Coin On-Chain Analysis & Chart Reading.
