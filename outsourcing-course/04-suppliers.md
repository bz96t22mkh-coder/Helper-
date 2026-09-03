# Module 4 — Suppliers

**Days 17–22 of ~120.**

This is where the business starts touching real, physical product. You'll understand exactly who you're outsourcing production to, find and vet real local suppliers, get real samples and quotes, learn to negotiate without damaging the relationship, and lock in a primary plus backup supplier — the two most important relationships this business depends on.

---

### DAY 17 — The Supply Chain Explained

**Module 4: Suppliers — Lesson 1**

### TODAY'S OBJECTIVE

Understand precisely what each type of supplier in your chain does, so you know exactly who you're looking for over the next few days instead of vaguely searching for "a uniform supplier."

### WHAT YOU NEED TO LEARN

**1. Blank-garment wholesalers.** These businesses supply plain, unbranded garments (golf shirts, t-shirts, overalls, jackets) in bulk, at wholesale prices well below retail. They typically don't do any branding themselves — they're a pure supply source for the raw product you'll have decorated. They usually carry a defined range of styles, sizes, and colours, with published or quotable per-unit pricing that drops as order quantity rises, and their own MOQs per style/colour/size.

**2. Decorators.** These are the businesses (often small, sometimes one-person operations, sometimes larger print/embroidery shops) that apply your customer's branding — a logo, a name, a company mark — onto the blank garment, using embroidery, screen printing, or heat transfer (Module 5 covers the trade-offs between these methods in depth). They typically charge per garment (sometimes with a flat setup fee per unique design/logo, which is where their own MOQ pressure often comes from — a small run doesn't spread that setup fee efficiently).

**3. How they fit together in your business.** You are the layer between these two specialists and your customer — you don't need either type of supplier to also be your customer-facing business. In practice:

```
YOU quote & take deposit from customer
   ↓
YOU order blank garments from a WHOLESALER (paid from the deposit)
   ↓
YOU send those blanks to a DECORATOR for branding
   ↓
YOU inspect the finished, branded product
   ↓
YOU deliver to customer & collect balance
```

Some businesses combine both roles in one company (a decorator who also stocks their own blanks) — this can simplify your supply chain to a single relationship, at the cost of potentially less competitive per-item pricing than sourcing blanks and branding separately. Both approaches are legitimate; you'll evaluate real options against each other starting Day 18.

**4. Why this distinction matters for vetting.** A business that's excellent at bulk garment supply (reliable stock, good pricing, fast dispatch) isn't necessarily good at embroidery quality, and vice versa — evaluating "a uniform supplier" as one undifferentiated thing means you might miss that your actual quality risk sits specifically with the decorator, not the wholesaler, or that your actual lead-time risk sits specifically with garment stock availability, not the branding step. Knowing which specialist does what lets you diagnose problems (and negotiate) precisely, instead of vaguely.

### WHAT YOU NEED TO UNDERSTAND

You don't need to have met either type of supplier yet to understand this distinction — today is purely conceptual, so that Days 18-21 (finding, vetting, sampling, negotiating) have a clear framework to slot real businesses into as you find them.

### EXERCISES

1. In your own words, explain the difference between a blank-garment wholesaler and a decorator, and why a business could be excellent at one and mediocre at the other.
2. List the two supply-chain structures described above (separate wholesaler + decorator, vs. a combined supplier doing both) and one advantage and one disadvantage of each, specific to a beginner with no track record yet.

(Open-ended conceptual exercises — there's no single correct structure to prefer; a strong answer shows you understand the trade-off, not that you've picked "the right answer.")

### BUSINESS IMPLEMENTATION

**[ME]**

1. Write a short note in `business/decisions-log.md` on which supply-chain structure (separate specialists vs. combined supplier) you're planning to search for first in Day 18's research, and why — you can revise this once you see what's actually available locally.

### TODAY'S DELIVERABLES

- [ ] Clear understanding of blank-garment wholesalers vs. decorators, in your own words.
- [ ] Initial preference noted for which supply-chain structure to search for first.

### END-OF-DAY CHECK

1. Could I explain to someone else what a blank-garment wholesaler does, and what a decorator does, without mixing them up?
2. Do I understand why quality risk and lead-time risk might sit with different suppliers in my chain?

### NEXT DAY

**Day 18** starts the real search — finding actual candidate suppliers of both types in your area, with Claude Code building you a proper tracker to organize what you find.

---

### DAY 18 — Finding Suppliers

**Module 4: Suppliers — Lesson 2**

### TODAY'S OBJECTIVE

Find a real, working list of candidate blank-garment wholesalers and decorators in your area (or reachable nationally, since many operate by courier), and get a proper supplier tracker built to organize what you find as you go.

### WHAT YOU NEED TO LEARN

**1. Where to actually look.** Google search ("blank golf shirts wholesale [your city/region]", "workwear embroidery [your city/region]", "screen printing supplier [your city/region]"), Google Maps, Facebook business pages (many smaller decorators operate primarily through Facebook, with a visible photo gallery of past work you can actually judge), local business directories, and — often the most reliable source — asking your Day 7 competitor research contacts or any local business-owner network you have access to who they use for their own supply. Some national wholesale garment suppliers serve the whole country by courier, which is worth knowing since your options aren't limited to only what's physically local to you.

**2. What you're collecting at this stage.** You're not vetting deeply yet (Day 19) or requesting samples yet (Day 20) — today is about building a real, wide candidate list: company name, contact details, what type of supplier they are (wholesaler, decorator, or combined), and a first impression from their public presence (website/Facebook — does it look active and professional, or abandoned?). Aim for breadth before depth — a shortlist of 1 candidate per category is not really a shortlist, it's a hope.

**3. A realistic target.** Aim for at least 4-5 candidate wholesalers and 4-5 candidate decorators (or 4-5 combined suppliers, if that's the structure you're leaning toward) by the end of today — enough that Day 19's vetting has real options to compare, and enough that Day 21-22's backup-supplier requirement isn't a last-minute scramble.

### WHAT YOU NEED TO UNDERSTAND

A wide net today costs you nothing but a bit of search time, and it directly prevents the Module 1 "single supplier, no backup" risk later — every candidate you find and log now, even ones you don't end up choosing, is a known option if your first choice ever lets you down.

### EXERCISES

1. Search and log at least 8-10 real candidate suppliers total (across wholesalers, decorators, and/or combined suppliers) using the methods above.
2. For each, note your genuine first impression from their public presence — active/professional vs. unclear/abandoned — as a rough initial filter, not a final judgment.

(Real-world research task using your own findings — never invent a supplier name, contact, or first impression. If your area genuinely has fewer than 8-10 findable candidates, note that honestly and consider whether national/courier-based suppliers should be part of your search.)

### BUSINESS IMPLEMENTATION

**[ME]**

1. Complete the search and log at least 8-10 real candidates into the supplier tracker built below.
2. Note any early standouts or immediate red flags in the tracker's notes column, ready for Day 19's proper vetting pass.

### CLAUDE CODE / AI BUILDING

**What we're building today:** a supplier tracker to organize every candidate you find, from first contact through to final decision — this becomes the permanent home for your supplier research from here through Day 22 and beyond.

**The exact prompt to give Claude Code:**
```
Build me a supplier tracker as a markdown table in business/suppliers/supplier-tracker.md
for a branded workwear outsourcing business. Columns:
- Supplier name
- Type (wholesaler / decorator / combined)
- Contact (phone/WhatsApp/email)
- First impression / notes
- MOQ (to fill in once known)
- Lead time (to fill in once known)
- Pricing notes (to fill in once known)
- Sample requested? (Y/N, date)
- Status (candidate / contacted / vetted / sample received / rejected /
  selected primary / selected backup)
Include a short instructions section at the top explaining how to use the
status column as candidates move through the vetting process over the
next few days.
```

**What to expect:** one markdown file with a clean table structure, ready to fill in with real candidates today and update through Day 22.

**How to test it:** add your real Day 18 candidates into it right now and confirm every column makes sense for what you're actually tracking — if a column's missing or unclear, tell me and I'll adjust it.

### TODAY'S DELIVERABLES

- [ ] Supplier tracker built and saved in `business/suppliers/`.
- [ ] At least 8-10 real candidate suppliers logged with first impressions.

### END-OF-DAY CHECK

1. Do I have a genuinely wide candidate list, not just the first one or two results I found?
2. Is my supplier tracker something I'll actually keep using through the rest of this module?

### NEXT DAY

**Day 19** narrows this wide candidate list with real vetting criteria, plus a proper outreach message template for making first contact.

---

### DAY 19 — Evaluating & Vetting Suppliers

**Module 4: Suppliers — Lesson 3**

### TODAY'S OBJECTIVE

Apply real vetting criteria to your Day 18 candidate list, and make real first contact with your strongest candidates using a proper outreach message.

### WHAT YOU NEED TO LEARN

**1. What to actually evaluate.** Beyond the first impression from Day 18, real vetting looks at:

| Factor | What to look for |
|---|---|
| **Quality** | Photos/samples of actual past work (not just stock catalogue images) — look for consistent stitching, colour accuracy, no visible fraying or misalignment |
| **Pricing** | Ask for real quotable pricing at realistic order volumes, not just "how much per shirt" with no quantity context |
| **Lead times** | Their stated turnaround, and — where possible — evidence they actually hit it consistently (reviews, or ask directly how often they run late) |
| **MOQs** | Their real minimum per style/colour/design — a hard constraint, not a negotiable detail at this stage |
| **Reliability signals** | How quickly and clearly they respond to your first message (a supplier who's slow or vague before you're even a customer is a real warning sign for after) |
| **Communication channel fit** | Do they operate comfortably over WhatsApp (your primary channel per the roadmap), or only by more formal/slow channels that would create friction in your actual workflow? |

**2. A real supplier outreach message template.** Keep it professional, specific, and easy to respond to — a vague "hi, do you supply uniforms?" gets a vague or slow answer.

```
Hi [Supplier name], my name is [your name] from [your business name].
I'm sourcing [blank golf shirts / embroidery services / etc.] for a
uniform supply business serving security and cleaning companies in
[region]. Could you share:
- Your MOQ per style/colour
- Indicative pricing at around [realistic quantity, e.g. 40-60 units]
- Typical lead time from order to ready
- Whether you can share photos of recent similar work
Happy to discuss further by WhatsApp or call, whichever's easier for you.
Thanks!
```

Adjust the bracketed quantity to something realistic for your actual pipeline — a wholesaler/decorator will price and prioritize you differently based on a vague inquiry versus one that signals a real, specific order size is coming.

### WHAT YOU NEED TO UNDERSTAND

Vetting at this stage is about narrowing your Day 18 list to a realistic shortlist of 2-3 strong candidates per category (wholesaler/decorator), not making a final decision yet — that happens after real samples (Day 20) and real negotiation (Day 21). Don't commit emotionally to "the one" this early; a supplier who looks great on paper can still disappoint once you see an actual sample.

### EXERCISES

1. Apply the vetting table above to your Day 18 candidates and narrow to a shortlist of 2-3 per category.
2. Send your outreach message (adapted to your own voice) to your full shortlist today.
3. Log every response (or non-response) in your supplier tracker.

(Real-world task using your own findings — log genuine responses, including any that don't reply, exactly as you did with prospect outreach in Module 2.)

### BUSINESS IMPLEMENTATION

**[ME]**

1. Complete the vetting and shortlisting.
2. Send real outreach to your shortlist and update the supplier tracker with every response.

### TODAY'S DELIVERABLES

- [ ] Shortlist of 2-3 candidates per supplier category, vetted against the criteria table.
- [ ] Real outreach sent to the full shortlist.
- [ ] Supplier tracker updated with responses.

### END-OF-DAY CHECK

1. Am I evaluating suppliers on real criteria, not just gut feeling from their website?
2. Did I send genuinely specific outreach, not a vague generic message?
3. Is my supplier tracker current with real responses?

### NEXT DAY

**Day 20** covers requesting and evaluating real samples and formal quotes from your shortlisted suppliers — the point where "looks good on paper" gets tested against the physical product.

---

### DAY 20 — Requesting Samples & Quotes

**Module 4: Suppliers — Lesson 4**

### TODAY'S OBJECTIVE

Request real samples and formal quotes from your shortlisted suppliers, and know exactly what to check once physical samples actually arrive.

### WHAT YOU NEED TO LEARN

**1. Requesting a sample and a formal quote.** Once a shortlisted supplier has responded to your Day 19 outreach, move to specifics: request a physical sample of a realistic product (e.g. the exact golf shirt/overall style you're likely to sell most), and a formal written quote at a realistic order quantity — not just a verbal "around R95 a shirt" figure, but something you can compare apples-to-apples against another supplier's written quote. Expect to pay for samples in most cases (a reasonable, normal cost of doing this research properly) — budget for it per the roadmap's expected expenses (R1,000-R3,000 across Module 4-5 for sample garments + branding).

**2. What to check when a sample arrives.** This is a physical quality-control check, done the same way you'll eventually check every real customer order (Module 1's quality-control discipline, starting here):

- **Fabric feel and weight** — does it feel like a durable workwear fabric, or thin/flimsy for the price quoted? (Module 5, Day 23 covers fabric basics in depth — for now, a simple hand-feel and stretch/durability check is enough.)
- **Stitching quality** — even seams, no loose threads, no puckering (fabric bunching unevenly along a seam).
- **Colour accuracy and consistency** — does it match what was shown/promised, and would it look consistent across a bulk order (ask if they can confirm colour-batch consistency at volume — a real risk with dye lots).
- **Sizing accuracy** — does a labelled size actually match real-world measurements? (Foreshadowing Day 3's size-chart lesson — a supplier whose sizing is inconsistent creates exactly the size-dispute risk you're trying to prevent.)
- **If branded, embroidery/print quality** — clean edges, correct colour match to the logo, no visible backing/stabilizer poking through on embroidery, no cracking or peeling on print/transfer (Module 5, Day 24 covers branding-method trade-offs in depth).

**3. Comparing quotes properly.** Line up every shortlisted supplier's quote side by side in your supplier tracker: price at the same quantity, MOQ, lead time, and your own quality assessment from the sample. The cheapest quote with a poor sample is not a good deal — remember Module 1's core discipline: your reputation with the customer depends on quality you personally verified, not the lowest number on a quote.

### WHAT YOU NEED TO UNDERSTAND

Samples and quotes can take real-world time to arrive — this is exactly the kind of dependency the roadmap flags as something that "carries over" naturally rather than something you should rush or fake. If a sample hasn't arrived by the time you reach Day 22's capstone, that's normal — Day 22 explicitly allows carrying this forward rather than forcing a decision on incomplete information.

### EXERCISES

1. Request samples and formal quotes from your full shortlist today.
2. Once any samples have arrived (today or as they come in), run the quality checklist above and log the results in your supplier tracker.

(Real-world task — log genuine results, including "still waiting" for anything not yet received. Never invent a sample result or a quote figure.)

### BUSINESS IMPLEMENTATION

**[ME]**

1. Request real samples and quotes from your shortlist.
2. Run and log the quality checklist against every sample that arrives.
3. Update the supplier tracker's pricing, MOQ, and lead-time columns with real, written quote information as it comes in.

### TODAY'S DELIVERABLES

- [ ] Samples and formal quotes requested from the full shortlist.
- [ ] Quality checklist run and logged against any samples received so far.
- [ ] Supplier tracker updated with real quote details.

### END-OF-DAY CHECK

1. Did I request a formal, written quote — not just a verbal estimate — from each shortlisted supplier?
2. Do I know exactly what to check when a physical sample arrives?
3. Am I comfortable that a real decision here depends on real samples, and that waiting for them is normal, not a delay to feel bad about?

### NEXT DAY

**Day 21** covers negotiation basics for supplier deals, and the discipline of always qualifying a backup supplier — even once you've found a primary you're excited about.

---

### DAY 21 — Negotiation Basics & Backup Suppliers

**Module 4: Suppliers — Lesson 5**

### TODAY'S OBJECTIVE

Learn practical, relationship-preserving negotiation basics for supplier deals, and lock in the discipline of always qualifying a backup supplier — directly addressing the "single point of failure" risk from Module 1.

### WHAT YOU NEED TO LEARN

**1. Negotiation basics that fit a long-term supplier relationship.** Unlike a one-time transaction, you want this supplier relationship to last — aggressive, one-sided negotiation tactics that squeeze every last rand out of a first deal can damage the goodwill you'll need later (priority during a rush order, flexibility on a payment timing issue, a favour when you're in a bind). Useful, relationship-safe negotiation moves:

- **Volume signalling, honestly.** If you genuinely expect growing, repeat order volume (a reasonable expectation in this niche given staff turnover), say so — suppliers often have real flexibility on price for a customer who represents ongoing business, not just a one-off order.
- **Ask, don't assume, about tiered pricing.** "Does your pricing improve at higher quantities, and if so, at what thresholds?" is a normal, expected question, not an aggressive one.
- **Trade non-price terms, not just price.** Faster payment (e.g. paying in full upfront for a first small order to build trust) in exchange for better pricing or priority lead time can be a better trade than squeezing the per-unit price on a supplier who's already offered a fair rate.
- **Never negotiate quality.** Pushing a supplier to cut corners on quality to hit a lower price recreates the exact risk Module 1 warned about — a bad batch reaching a customer. Negotiate price, terms, and lead time; never negotiate away the quality bar you tested in the sample.

**2. Why you always qualify a backup supplier, even once you've found a great primary.** This is not about distrust of your chosen supplier — even an excellent, reliable supplier can have a bad month, a stock-out, a machine breakdown, or simply be unable to meet a rush order's timeline. "Qualifying" a backup doesn't mean splitting your real orders between two suppliers day to day (which usually costs you the volume-pricing benefit of consolidating with one) — it means going through the same vetting and sample process with a second supplier per category, confirming they meet your quality bar, and keeping the relationship warm (even a small occasional order) so they're a real, tested option, not a name on a list you've never actually dealt with.

### WHAT YOU NEED TO UNDERSTAND

The value of a backup supplier is proportional to how real it actually is — a name you found on Google but never sampled or vetted is barely better than no backup at all, because you won't actually know if their quality or reliability holds up until you're relying on them in a crisis, which is the worst possible time to find out. Treat your backup with almost the same vetting rigor as your primary.

### EXERCISES

1. Write out, in your own words, one thing you'd be comfortable negotiating on with a supplier, and one thing you would never negotiate away, based on today's lesson.
2. Review your supplier tracker: do you currently have a real, sampled, vetted backup candidate in both the wholesaler and decorator (or combined) categories? If not, name your next step to get there.

(Open-ended, based on your own real supplier research so far.)

### BUSINESS IMPLEMENTATION

**[ME]**

1. If you've received quotes from more than one candidate per category, practice a real negotiation conversation (price, terms, or lead time — never quality) with at least one.
2. Explicitly identify, in your supplier tracker's status column, which candidate is your leading primary and which is your leading backup per category — even if final confirmation is still pending sample results.

### TODAY'S DELIVERABLES

- [ ] Personal negotiation boundaries (what's negotiable, what's not) written down.
- [ ] Backup-supplier status honestly assessed against real vetting, not just a name on a list.
- [ ] Supplier tracker updated with leading primary/backup candidates per category.

### END-OF-DAY CHECK

1. Do I know the difference between negotiating price/terms and negotiating away quality?
2. Do I have a real, vetted backup candidate, or just an unverified name?
3. Am I prepared to keep a backup relationship warm even once I'm not using them for most orders?

### NEXT DAY

**Day 22** is Module 4's capstone: finalizing your primary and backup supplier per category (carrying forward if real-world sample timing isn't finished yet), writing a supplier relationship SOP, and bridging into Module 5 (Products).

---

### DAY 22 — Module 4 Capstone: Locking In Your Suppliers

**Module 4: Suppliers — Lesson 6**

### TODAY'S OBJECTIVE

Finalize your primary and backup supplier decisions wherever your real-world research supports it, document a supplier relationship SOP so this discipline doesn't depend on memory, and confirm your understanding of the whole module before moving into Module 5 (Products).

### WHAT YOU NEED TO LEARN

**It's genuinely fine if this isn't fully finished today.** Real supplier sampling and quoting run on real-world timelines outside your control — if a sample is still in transit or a quote hasn't come back, carry that specific item forward as unfinished work rather than forcing a decision on incomplete information (exactly the same principle the roadmap applies to any real-world dependency). What matters today is finalizing everything that *is* ready, and being explicit about what isn't.

**A supplier relationship SOP — why it matters.** An SOP (standard operating procedure) here means a short, written, repeatable process for how you manage supplier relationships going forward, so the discipline built this module (never negotiate quality, always keep a backup warm, always get things in writing) survives past this week and becomes how the business actually runs, not just this module's homework. At minimum, it should cover:
- How often you check in with your primary supplier even with no active order (keeping the relationship warm).
- How often you place a small "keep-warm" order with your backup supplier, if at all.
- What triggers a re-evaluation of your primary (e.g. a missed deadline, a quality slip) versus what's a one-off you'd let go.
- Where quotes, samples results, and communication are logged (your supplier tracker).

### WHAT YOU NEED TO UNDERSTAND

This SOP is the first entry in what becomes a full SOP library in Module 19 — writing it now, while the reasoning behind each rule is fresh, is far easier than reconstructing it later from memory once you're deep into daily operations.

### EXERCISES

**Module 4 review quiz:**

a. What's the core difference between a blank-garment wholesaler and a decorator?
b. Name three things you should check when a physical sample arrives.
c. Name one thing that's reasonable to negotiate with a supplier, and one thing you should never negotiate away.
d. Why is an unvetted backup supplier name barely better than having no backup at all?

**Check your work:**

a. A wholesaler supplies plain, unbranded garments in bulk; a decorator applies the branding (embroidery/print/transfer) onto them. A business can be strong at one and weak at the other.
b. Any three of: fabric feel/weight, stitching quality, colour accuracy/consistency, sizing accuracy, and (if branded) embroidery/print quality.
c. Reasonable to negotiate: price at volume, payment terms, lead time/priority. Never negotiate away: quality — cutting corners here recreates the exact risk of a bad batch reaching a customer.
d. Because quality and reliability only actually show up under real testing (a real sample, a real order) — an unvetted name is unproven, and you won't discover it's unreliable until you're depending on it in a crisis, which is the worst time to find out.

### BUSINESS IMPLEMENTATION

**[ME]**

1. Finalize your primary and backup supplier per category in your supplier tracker, wherever real-world results support a decision — mark anything still pending clearly as "carried over," with what specifically you're waiting on.
2. Log the final supplier decisions (or the honest current status) as a dated entry in `business/decisions-log.md`.
3. Write your supplier relationship SOP (using the outline above) and save it in `business/suppliers/`.

### CLAUDE CODE / AI BUILDING

**What we're building today:** a short, written supplier relationship SOP, so this module's discipline becomes a repeatable process, not a memory.

**The exact prompt to give Claude Code:**
```
Write a supplier relationship SOP as business/suppliers/supplier-sop.md
for a branded workwear outsourcing business. Cover, based on decisions
already logged in business/decisions-log.md and business/suppliers/supplier-tracker.md:
- How often to check in with the primary supplier even with no active order
- Whether/how often to place a small keep-warm order with the backup
  supplier
- What triggers a re-evaluation of the primary supplier (e.g. missed
  deadline, quality slip) versus what's treated as a one-off
- Where all supplier communication, quotes, and sample results get logged
Keep it short — one page, a checklist-style document, not a policy essay.
```

**What to expect:** a short, practical checklist document you'd actually follow, not a long formal policy nobody reads.

**How to test it:** read it and ask yourself honestly whether you'd actually follow each line as written — if any step feels unrealistic or unclear, tell me and I'll adjust it.

### TODAY'S DELIVERABLES

- [ ] Primary and backup suppliers finalized per category, or explicitly marked as carried-over with a clear reason.
- [ ] Final decisions logged in `business/decisions-log.md`.
- [ ] Supplier relationship SOP written and saved.
- [ ] Module 4 review quiz completed and checked.

### END-OF-DAY CHECK

1. Do I have a real, vetted primary supplier per category — or a clear, honest status on what's still pending?
2. Do I have a real, vetted backup — or a clear next step to get one?
3. Do I have a written SOP I'd actually follow, not just a document that exists?

### NEXT DAY

**Module 5 (Day 23)** moves from suppliers to products — the specific uniform/workwear items relevant to your niche, fabric basics, and the branding methods (embroidery vs. print vs. transfer) you'll be choosing between for real customer orders.
