# Module 13 — Meme-Coin Security & Scam Detection

**Est. length:** 3 days (6 hours). Treat this as non-negotiable, not optional caution.
**Prerequisite:** Modules 2, 12. **Feeds into:** Module 14 (on-chain confirmation of these patterns), Module 15 (framework's no-trade conditions), Module 21 (playbook security section).

---

## 1. What You Need to Learn

How to identify rug pulls, honeypots, malicious contracts, fake tokens/websites/X accounts/influencers/partnerships, fake volume, wash trading, insider dumping, bundled wallets, concentrated ownership, liquidity manipulation, pump-and-dumps, wallet drainers, phishing, fake airdrops, and malicious token approvals — and build **THE ULTIMATE MEME-COIN SAFETY CHECKLIST** to run before interacting with any unfamiliar token or site.

## 2. Why It Matters

Most meme-coin losses aren't "the trade went against me" — they're a scam mechanism doing exactly what it was built to do. This module's checklist is the single highest-leverage thing in this entire course for capital preservation.

## 3. Contract & Wallet-Level Threats

**Rug pull** is the scam this entire course treats as the baseline threat to defend against, because it's simultaneously the most common, the most final, and the easiest to prevent with a single check. The mechanism is direct: the developer or deployer withdraws the liquidity pool entirely — if it was never locked or burned in the first place (Module 12 §4) — which instantly collapses the token's price to near zero, since the liquidity pool is what actually lets anyone convert the token back into another asset. Once it's pulled, holders aren't merely down on paper; they're holding a token with no real market to sell into at any price that resembles what they paid. The reason this scam is so prevalent is that it requires almost no technical sophistication beyond deploying a standard token contract and, at a moment of the deployer's choosing, executing a single withdrawal transaction — it doesn't need a clever exploit, just an unlocked pool and patience. **Direct check:** LP lock/burn status (Module 12 §4) — verified on-chain, not taken on the project's word — is the single most important line of defense against this specific scam, and it's checkable in minutes before you ever risk capital.

**Honeypot** describes a contract deliberately coded so that buying functions completely normally — drawing in buyers who see a rising price and no problem — while selling is blocked or heavily restricted for anyone except a list of approved wallets, typically the deployer's own. The asymmetry is what makes it effective: nothing about the buying experience gives any warning, so a buyer only discovers the trap when they try to sell and the transaction fails or returns a tiny fraction of expected value, by which point their capital is already committed. **Direct check:** run the token through a dedicated honeypot-detection tool (Module 2's RugCheck/GoPlus) *before* buying, not after — these tools specifically simulate a sell transaction against the live contract and will surface a sell restriction that's invisible from the buy side alone — and treat any flag from a scanner as disqualifying rather than something to explain away because the chart or the community looks appealing.

**Malicious contract functions** extend the honeypot's logic into a broader set of capabilities that can be embedded in a contract's code and triggered at the owner's discretion at any time, including well after a token has traded normally for a while and built up apparent trust. Unrenounced mint authority lets the owner create unlimited new tokens out of thin air, diluting or outright destroying existing holders' value on demand. Freeze/blacklist authority lets the owner block specific wallets from trading at all, which can be used narrowly (targeting large holders about to sell) or broadly. Modifiable transaction tax lets the owner spike the buy or sell tax to near-100% at will, which doesn't technically block a sale but makes it financially meaningless — money extracted through the tax itself rather than through an outright freeze. What makes these functions dangerous is precisely that they can sit dormant, unused, for as long as the deployer wants a token to look legitimate, only to be activated once enough capital has flowed in to make activation worthwhile. **Direct check:** Module 12 §5's contract-permissions review, every single time, with no exceptions carved out for a token that "looks legitimate" — legitimacy-by-appearance is exactly the state a contract with dormant malicious functions is designed to project.

**Malicious token approvals** exploit a mechanism that's actually a normal, necessary part of using any DEX: to let a smart contract move your tokens on your behalf (required for a standard swap), you grant it an "approval." The vulnerability appears when that approval is set to an *unlimited* amount rather than the exact amount needed for the transaction at hand, and the contract receiving that approval is malicious from the start or is upgraded to malicious behavior later — because an unlimited approval, once granted, remains valid indefinitely until you explicitly revoke it, giving that contract standing permission to move your full balance of that token whenever it chooses, not just at the moment you approved it. A drainer contract disguised as an ordinary-looking dApp (a swap interface, a staking page, a mint page) can request exactly this kind of broad approval and then, at any later point, use it to empty your wallet of that token — and in some approval schemes, of more than just the one token. **Direct check:** approve only the exact amount needed for the transaction at hand wherever your wallet interface allows it, rather than accepting the default "unlimited" approval many interfaces suggest, and periodically review and revoke old, no-longer-needed approvals using a reputable revocation tool (services in the revoke.cash style — verify which tool is currently recommended and reputable at the time you use it, since the landscape shifts).

**Wallet drainers** are the most direct, front-line version of this entire threat category: malicious sites or contracts built specifically around the goal of getting you to sign a single transaction or message that, the moment it's signed, transfers assets out of your wallet — no further interaction from you required. They're routinely disguised as something you'd want to interact with anyway: a mint page for a free NFT, a claim page for a token airdrop, or an innocuous-looking "connect wallet to verify you're human" prompt. The signature itself is the entire attack; there's no separate hack of your wallet or your keys, just a request worded or structured so that what you're actually authorizing isn't what you think you're authorizing. **Direct check:** never sign a transaction or message you don't fully understand — take the extra few seconds to read what your wallet's signature prompt is actually requesting, not just what the website around it claims it's for — and treat any unsolicited link inviting you to "connect your wallet" to claim or verify something as hostile until proven otherwise.

## 4. Market-Manipulation Patterns

**Fake volume / wash trading** is the on-chain counterpart to the bot engagement covered in Module 11 §6 — instead of manufacturing the appearance of social interest, an entity trades with itself, or with a set of coordinated wallets it controls, purely to manufacture the appearance of organic trading volume and interest that doesn't actually exist. The purpose is to make a token look more actively traded, and therefore more legitimate and more worth paying attention to, than the genuine participant count would ever produce on its own. **Direct check:** apply Module 3's volume-to-liquidity ratio red flag (also revisited in Module 12 §3), and go a step further by checking on the explorer whether the volume generating that ratio is concentrated in a small number of wallets trading back and forth, rather than spread across many independent addresses — genuine organic volume has a wide base of participants, wash-traded volume typically does not.

**Insider dumping** is the mechanism by which the wallet-level concentration you learned to measure in Module 12 §4 actually turns into realized losses for other holders: early or insider wallets — the ones that acquired their position before public trading or in its earliest minutes — sell into the liquidity that later, retail buying creates. This is the standard mechanical explanation behind the extremely common pattern of a fast, exciting pump immediately followed by an even faster crash: the "pump" is often, in significant part, retail demand arriving in response to rising price and social attention, and the "crash" is the wallets that got in first taking that demand as their exit. **Direct check:** track whether large recent sell transactions map to addresses you already identified as early/insider wallets during your Module 12 analysis — if the biggest sellers during a price drop are the same wallets that got in before anyone else, that's not a coincidence worth explaining away.

**Bundled wallets** are the technique that makes insider dumping harder to see coming: many wallets that appear, on the surface, to be independent holders — different addresses, no obvious naming pattern connecting them — but that were actually funded from the same original source and act in coordination, buying, holding, and selling together on a shared schedule. The purpose is specifically to disguise concentrated ownership as broad, healthy distribution: a holder count that looks like "500 independent wallets" can in reality be 20 people (or one person) controlling 25 wallets each. **Direct check:** Bubblemaps-style cluster visualization (introduced in Module 2, deepened substantially in Module 14) traces the funding relationships between wallets and makes these clusters visible even when the addresses themselves give no hint of the connection.

**Concentrated ownership** was covered as a static risk measurement in Module 12 §4; the reason it belongs in this module too is to make explicit what that concentration actually *enables*. Concentrated supply isn't just a risk metric sitting on a dashboard — it's the literal precondition that makes insider dumping and coordinated pump-and-dump schemes mechanically possible in the first place. A token where ownership is genuinely spread across thousands of independent holders cannot be dumped by "a decision," because no single decision controls enough supply to matter; a token where a handful of wallets or a bundled cluster controls a large share can be, at any moment those wallets choose. Every manipulation pattern in this section ultimately depends on concentration existing somewhere upstream of it.

**Liquidity manipulation** works by adding or removing liquidity strategically — not to trade the token, but to shape what the *chart* looks like to observers. A common version: briefly adding a meaningful amount of liquidity to make price look more stable and the pool look healthier right before a bigger, planned sell, since a deeper pool absorbs a large sell with less visible price impact, making the exit look calmer (and less alarming to remaining holders) than it would against a thin pool. **Direct check:** watch liquidity-pool size as a trend over time rather than checking it once — a pool that grows suddenly for no stated reason, especially right before or during a period of unusual selling, deserves the same suspicion as a sudden sell itself.

**Pump-and-dump schemes** tie several of the above patterns together into a coordinated campaign: a group — sometimes organized informally, sometimes through private Telegram or Discord groups sold as "alpha calls" — buys a token together, deliberately spiking its price and drawing social attention, then publicizes the resulting move to attract retail buyers who see the price action and the excitement and want in. Once retail demand arrives and provides real buying pressure, the organizing group sells into it, realizing gains that are directly funded by the later buyers' capital. **Direct check:** be maximally suspicious of any explicit "get in now," "don't miss this," or similarly urgent social pressure tactic — genuine opportunities rarely require this specific kind of manufactured time pressure — especially when it comes from a group or channel with a checkable history of similar calls followed by similar crashes.

## 5. Social-Layer Threats (Cross-Reference Module 11)

**Fake websites** are near-identical clones of a real project's official site, frequently hosted on a lookalike domain that differs from the real one by a single character, a different top-level domain, or a subtly altered spelling — built specifically to harvest wallet connections and, in the worst cases, seed phrases entered directly into a fake "connect" or "recovery" flow. Because the visual clone can be pixel-perfect, appearance alone is not a reliable defense; the domain itself is the only thing that can't be perfectly copied. **Direct check:** always navigate to a project's site via a bookmark you saved after verifying it once, or by typing the URL manually from a source you trust — never via a search-engine ad (ads can be bought for a lookalike domain) or a link sent in a DM.

**Fake X accounts and impersonation** were covered mechanically in Module 11 §6 as a credibility problem; restated here, the point is that the same pattern is also a direct security threat, not merely a source of bad information. An impersonation account isn't just spreading a false claim — it's frequently the delivery vehicle for a phishing link, a fake airdrop, or a direct DM-based scam, meaning the credibility check from Module 11 and the security check in this module are, in this case, the same check performed for two different reasons.

**Fake influencers and fake partnerships** are claims of an endorsement, collaboration, or official partnership that don't check out against the claimed party's own official channels — the same primary-source verification principle from Module 11 §4 applied specifically to claims designed to borrow a well-known name's credibility to make a token look more legitimate or more connected than it actually is. A token claiming "backed by [well-known figure]" with no corroborating post anywhere on that figure's own account should be treated as false until proven otherwise, not treated as plausible until disproven.

**Fake airdrops** are among the most common and most effective wallet-drainer vectors precisely because they exploit a genuinely pleasant expectation — free tokens for existing holders or community members — that legitimate projects do sometimes deliver, which is exactly what makes the fake version convincing. The pattern is an unsolicited message or post claiming "you're eligible for a free airdrop, connect your wallet or sign this message to claim it," when the actual purpose of that connection or signature is to drain the wallet, not to deliver anything. **Direct check:** treat any unsolicited airdrop claim as hostile by default until proven otherwise through the project's own verified official channel, and never sign anything to "claim" a reward without independently confirming its legitimacy across multiple official sources first — a genuine airdrop can always wait the extra few minutes that verification takes; a drainer is specifically counting on you not taking them.

**Phishing via DMs and fake support** covers any account reaching out directly — claiming to be "support," a project team member, or offering an "exclusive opportunity" — through a channel that puts pressure on you to act quickly and privately, away from public scrutiny where the claim might get corrected by someone else. **Direct check:** internalize, as close to an absolute rule as exists in this course, that legitimate teams and legitimate wallet or exchange support never DM first to ask for a seed phrase, a wallet connection, or urgent action — any message that does is not a borderline case requiring judgment, it is definitionally a scam attempt.

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
