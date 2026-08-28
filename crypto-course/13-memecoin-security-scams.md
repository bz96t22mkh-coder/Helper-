# Module 13 — Meme-Coin Security & Scam Detection

**Est. length:** 3 days (6 hours). Treat this as non-negotiable, not optional caution.
**Prerequisite:** Modules 2, 12. **Feeds into:** Module 14 (on-chain confirmation of these patterns), Module 15 (framework's no-trade conditions), Module 21 (playbook security section).

---

## 1. What You Need to Learn

How to identify rug pulls, honeypots, malicious contracts, fake tokens/websites/X accounts/influencers/partnerships, fake volume, wash trading, insider dumping, bundled wallets, concentrated ownership, liquidity manipulation, pump-and-dumps, wallet drainers, phishing, fake airdrops, and malicious token approvals — and build **THE ULTIMATE MEME-COIN SAFETY CHECKLIST** to run before interacting with any unfamiliar token or site.

## 2. Why It Matters

Most meme-coin losses aren't "the trade went against me" — they're a scam mechanism doing exactly what it was built to do. This module's checklist is the single highest-leverage thing in this entire course for capital preservation.

## 3. Contract & Wallet-Level Threats

- **Rug pull:** the developer/deployer withdraws the liquidity pool entirely (if not locked/burned — Module 12 §4), instantly crashing the token to near-zero and leaving holders unable to sell for any real value. **Direct check:** LP lock/burn status (Module 12) — this is the single most important line of defense.
- **Honeypot:** a contract coded so that buying works but selling is blocked or heavily restricted for anyone except approved wallets (often the deployer's). **Direct check:** run the token through a honeypot-detection tool (Module 2's RugCheck/GoPlus) *before* buying, and be skeptical of any token where a scanner flags sell restrictions.
- **Malicious contract functions:** unrenounced mint authority (owner can create unlimited new tokens, destroying value), freeze/blacklist authority (owner can block specific wallets from trading), and modifiable transaction tax (owner can spike the sell tax to near-100% at will). **Direct check:** Module 12 §5's contract-permissions review, every time, no exceptions for a token that "looks legitimate."
- **Malicious token approvals:** granting a smart contract "approval" to spend your tokens (required for normal DEX swaps) can be exploited if the approval is unlimited and the contract is malicious or later upgraded maliciously — a drainer contract disguised as a normal dApp can then empty your wallet of that token (or, with certain approval types, more). **Direct check:** approve only the exact amount needed per transaction where your wallet allows it, and periodically review/revoke old approvals using a reputable revoke tool (e.g., revoke.cash-style services — verify current recommended tool at time of use).
- **Wallet drainers:** malicious sites/contracts specifically designed to request a wallet signature that, once signed, transfers out assets — often disguised as a mint page, a claim page, or a "connect to verify" prompt. **Direct check:** never sign a transaction/message you don't understand; read what a wallet's signature prompt is actually requesting; be maximally suspicious of any unsolicited link asking you to "connect wallet" to claim something.

## 4. Market-Manipulation Patterns

- **Fake volume / wash trading:** an entity trades with itself (or coordinated wallets) to manufacture the appearance of organic volume/interest. **Direct check:** Module 3's volume-to-liquidity ratio red flag, plus checking whether volume is concentrated in a small number of wallets on the explorer.
- **Insider dumping:** early/insider wallets (Module 12 §4) sell into the liquidity created by later, retail buying — the standard mechanism behind a fast pump followed by an even faster crash. **Direct check:** track whether large recent sells map to early/insider wallet addresses.
- **Bundled wallets:** many wallets that appear independent but were funded from the same source and act in coordination (buying/holding/selling together) — used to disguise concentrated ownership as "many holders." **Direct check:** Bubblemaps-style cluster visualization (Module 2, deepened in Module 14).
- **Concentrated ownership:** covered in Module 12 §4 — restated here as a market-manipulation *enabler*: concentrated supply is what makes insider dumping and coordinated pump-and-dump schemes mechanically possible in the first place.
- **Liquidity manipulation:** adding/removing liquidity strategically to create misleading price action (e.g., briefly adding liquidity to make a chart look healthier before a bigger sell). **Direct check:** watch liquidity-pool size over time, not just at a single snapshot.
- **Pump-and-dump schemes:** a coordinated group (sometimes via private groups/Telegram) buys a token together to spike price and attention, publicizes the move to attract retail buyers, then sells into that retail demand. **Direct check:** be maximally suspicious of any explicit "get in now" social pressure tactic, especially from a group/channel with a history of similar calls.

## 5. Social-Layer Threats (Cross-Reference Module 11)

- **Fake websites:** near-identical clones of a real project's site (often via a lookalike domain) designed to harvest wallet connections/seed phrases. **Direct check:** always navigate via a bookmarked or manually-typed, verified URL — never a search-ad or DM link.
- **Fake X accounts / impersonation:** covered in Module 11 §6 — restated here as a direct security threat, not just a credibility issue.
- **Fake influencers / fake partnerships:** claims of endorsement or partnership that don't check out against the claimed party's own official channels (Module 11 §4).
- **Fake airdrops:** an unsolicited "you're eligible for a free airdrop, connect your wallet/sign to claim" prompt — one of the most common wallet-drainer vectors. **Direct check:** treat any unsolicited airdrop claim as hostile until proven otherwise via the project's own verified official channel, and never sign anything to "claim" without independently verifying via multiple official sources first.
- **Phishing (DMs, fake support):** an account DMing you "support" or an "exclusive opportunity," especially impersonating a project team member or a wallet's official support. **Direct check:** legitimate teams/support never DM first asking for a seed phrase, a wallet connection, or urgent action.

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
