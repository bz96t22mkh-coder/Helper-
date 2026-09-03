# Module 8 — Website

**Days 39–45 of ~120.**
Not an online store — a credibility and lead-capture tool, built with Claude Code and put on a real domain.

---

### DAY 39 — Defining What This Website Actually Needs to Do

**Module 8: Website — Lesson 1**

### TODAY'S OBJECTIVE

Define exactly what your website has to do for this specific business, and sketch a simple sitemap — before writing a single line of it — so Day 40's build has a clear, complete brief instead of guesswork.

### WHAT YOU NEED TO LEARN

**1. This is not an e-commerce store.** You are not selling individual t-shirts to consumers who browse and check out online. You sell customized bulk uniform orders to businesses, priced per order after a quote, with a 50% deposit and a real conversation involved. A shopping cart and checkout flow would be wasted complexity — and worse, it would misrepresent how you actually do business to a buyer who expects a B2B sales process. Your website has exactly two jobs:
- **Credibility** — when a prospect (or someone they forward your details to, like a finance manager or the actual company owner) looks you up, the site needs to make you look like a real, established, trustworthy supplier within seconds.
- **Lead capture** — turn a visitor into a quote request, a WhatsApp message, or a phone call. Every page should point toward one of those actions.

**2. What a B2B uniform-supplier site needs, no more:**
- **Homepage** — who you are, who you serve (security and cleaning companies), your positioning, and a clear call to action (request a quote / contact us).
- **Catalogue/services overview** — the categories of workwear you supply (drawing on your Module 5 catalogue), described in terms of the buyer's needs, not a product-by-product online store.
- **About/why us** — your positioning statement, your process (quote → deposit → order → inspection → delivery → balance), and what makes you different from a generalist (Module 7).
- **Contact/quote request** — phone/WhatsApp, email, and (added Day 42) a simple form so a visitor can request a quote without needing to already have your WhatsApp number.

That's it for v1. No blog, no login system, no payment gateway, no product pages with "add to cart" — none of that serves this business model, and every page you add that isn't pulling its weight is a page that has to be written, tested, and maintained for nothing.

**3. What a sitemap is and why you draw it before building.** A sitemap is just the list of pages and how they connect — which page links to which, and what the visitor is meant to do on each one. Drawing it first forces you to decide the site's structure while it's cheap to change (on paper) rather than after Claude Code has already built it.

### WHAT YOU NEED TO UNDERSTAND

The single biggest mistake beginners make with a first business website is over-scoping it — trying to build something that looks like a big e-commerce brand's site instead of what this business actually needs. A simple, fast, clear four-page site that does its two jobs (credibility + lead capture) well will outperform an ambitious ten-page site that's half-finished, slow, or confusing about what you actually want the visitor to do. Every page needs one clear next action for the visitor — if a page doesn't point somewhere (another page, or a contact action), cut it or fix it.

### EXERCISES

1. **Write one sentence each** for what "credibility" and "lead capture" mean specifically for your business (not the general definitions above — your own version, in your own words).
2. **Draw your sitemap** — a simple box-and-arrow sketch (paper or a notes app) of your four pages and how they link to each other, with the call-to-action on each page labeled.
3. **List the 3-5 catalogue categories** you'll show on the services/catalogue page, pulled directly from your Module 5 catalogue — not the full detailed product list, just the buyer-facing groupings (e.g. security uniforms, cleaning staff workwear, branded accessories — using your own actual catalogue's real categories).

A strong sitemap has no dead ends — every page leads somewhere, and the contact/quote action is never more than one click away from any page.

### BUSINESS IMPLEMENTATION

1. **[ME]** Write the credibility/lead-capture definitions for your business.
2. **[ME]** Draw the sitemap.
3. **[ME]** Pull the 3-5 catalogue categories from your Module 5 catalogue for the site.

### TODAY'S DELIVERABLES

- [ ] Credibility and lead-capture definitions written, specific to your business.
- [ ] A four-page sitemap sketched, with the call-to-action on each page labeled.
- [ ] 3-5 catalogue categories selected for the site.

### END-OF-DAY CHECK

1. Can I explain in one sentence why this site isn't an online store?
2. Does every page in my sitemap have a clear next action for the visitor?
3. Do I know exactly which catalogue categories will appear on the site?

### NEXT DAY

**Day 40** hands this sitemap to Claude Code as the brief for building website v1 — bring your sitemap, your brand pack (Module 7), and your catalogue categories.

---

### DAY 40 — Claude Code Builds Website v1

**Module 8: Website — Lesson 2**

### TODAY'S OBJECTIVE

Get a working first version of the website built — homepage, catalogue/services overview, and contact page — running locally so you can view and test it in a browser today.

### WHAT YOU NEED TO LEARN

**1. What "v1" means here.** Today's build is structure and placeholder-quality content in the right places, using your real brand direction (name, colours, positioning) — not final polished copy. Day 41 replaces placeholder text with real, written copy. Building structure first and copy second keeps each day focused on one job instead of trying to perfect everything at once.

**2. Why a static site (no framework, no database, no server code) is the right choice here.** Per the course's technology approach, you don't need anything more complex than plain HTML/CSS for a four-page credibility site — it loads fast, costs nothing beyond hosting, has no moving parts to break, and is simple to deploy (Day 44) and hand off to anyone later. Complexity you don't need yet is a cost, not a feature.

**3. What to check for in a first build**, before you even get to detailed testing (Day 43):
- Does every page match your sitemap and link correctly to the others?
- Is your brand pack's name, positioning, and colour direction actually reflected, not generic placeholder styling?
- Is there a clear call-to-action visible on every page without scrolling?
- Does it look reasonable on a phone-sized browser window, not just full desktop width? (Most of your prospects will look at this on a phone.)

### WHAT YOU NEED TO UNDERSTAND

A first build from a clear brief should already be close to right — but "close" isn't "done." Your job today isn't to silently accept whatever comes back; it's to look at it with the sitemap and brand pack open next to it and check it actually matches what you asked for. This is the same test-and-report loop from Day 1: read it, test it against what you actually need, tell Claude Code exactly what's off.

### EXERCISES

Before the build, gather what Claude Code needs from you:
1. Confirm your final sitemap (Day 39).
2. Confirm your brand pack details (business name, positioning statement, colour direction, contact details — all from Module 7).
3. Confirm your 3-5 catalogue categories with one short buyer-facing description each (a sentence or two per category, not full product specs).

### BUSINESS IMPLEMENTATION

1. **[ME]** Gather sitemap, brand pack details, and catalogue category descriptions.
2. **[CLAUDE CODE]** Build the three-page website v1.
3. **[ME]** View and test it against the sitemap and brand pack.

### CLAUDE CODE / AI BUILDING

**What we're building today:** a three-page static website (homepage, catalogue/services overview, contact) as plain HTML/CSS files, viewable directly in a browser with no server or build step required.

**The exact prompt to give Claude Code:**
```
Build website v1 for my business as a simple static site (plain HTML/CSS,
no framework, no build tools, no external dependencies) with these pages:

1. Homepage (index.html): business name and positioning statement
   [paste from brand pack], who we serve (security and cleaning companies
   in [your region]), a short "why us" summary [paste your top 2 USPs],
   and a clear call-to-action button linking to the contact page.

2. Catalogue/services overview (catalogue.html): these categories with a
   short buyer-facing description each: [paste your 3-5 categories +
   descriptions]. End with a call-to-action linking to the contact page.

3. Contact page (contact.html): business phone/WhatsApp number, business
   email [from Module 7], a short line about what happens after they
   reach out (quote → deposit → order → inspection → delivery), and a
   placeholder note that a quote-request form is coming.

Design direction: colour palette [paste from your Day 35 logo brief],
clean, professional, no stock photos or clip-art, mobile-responsive
(must look correct at phone width, not just desktop). Consistent
navigation linking all three pages on every page. Save everything under
business/website/.
```

**What to expect:** three linked, styled HTML pages that already look like a real small business site, using your actual name, positioning, colours, and catalogue categories — not lorem ipsum or generic stock text.

**How to test it:** open `business/website/index.html` in a browser, click through every link on your sitemap and confirm nothing is broken or missing, then resize the browser window down to phone width (or use your browser's mobile preview) and check every page still looks right and every call-to-action is still visible without awkward scrolling. Report anything wrong or missing back to Claude Code by name (which page, what's wrong) rather than vaguely.

### TODAY'S DELIVERABLES

- [ ] Website v1 built: homepage, catalogue page, contact page, linked correctly.
- [ ] Viewed in a browser and checked against the sitemap.
- [ ] Checked at phone width.
- [ ] Any issues reported back and fixed.

### END-OF-DAY CHECK

1. Does the site match my sitemap exactly?
2. Does it look and read like my actual brand, not a generic template?
3. Does every page work correctly at phone width?

### NEXT DAY

**Day 41** replaces the placeholder-quality text on these pages with real, considered copy — bring today's built site open in a browser so you can see exactly what needs rewriting.

---

### DAY 41 — Writing the Real Website Copy

**Module 8: Website — Lesson 3**

### TODAY'S OBJECTIVE

Write the actual, final words for every page of your website — headlines, service descriptions, and the about/why-us section — replacing yesterday's placeholder-quality text with copy that would genuinely convince a skeptical B2B buyer.

### WHAT YOU NEED TO LEARN

**1. Good B2B copy for this niche is specific, not clever.** You're not writing to entertain — you're writing so a busy ops manager scanning your site on their phone for 20 seconds understands exactly what you do, who it's for, and what to do next. Every sentence should answer one of: what do you do, who is it for, why should I trust you, what do I do now.

**2. A headline formula that works for this business:** [what you supply] + [who it's for], stated plainly. Compare:
- Weak: "Quality Uniforms for Every Business" — vague, could be any competitor.
- Strong: "Branded Uniforms for Security and Cleaning Companies — Ordered Right, Delivered On Time" — specific audience, specific promise.

**3. Worked example — a homepage "why us" section, written properly:**

> Weak version (what a placeholder or an unconfident first draft often looks like):
> "We offer the best uniforms at the best prices with excellent customer service and fast delivery for all your branded clothing needs."
>
> Strong version (specific, buyer-focused, uses real facts from your business):
> "We supply branded workwear specifically for security and cleaning companies — polos, golfers, and overalls, embroidered or printed with your logo. Every order is quoted with a 50% deposit and personally inspected before it's delivered, so there are no surprises when it arrives. Because we specialize in this industry, we already understand the sizing runs and reorder patterns that come with staff turnover — you won't need to re-explain your business every time you order."

Notice what changed: real specifics (deposit terms, personal inspection, understanding turnover) replace generic adjectives ("best," "excellent," "fast").

**4. Writing for the catalogue/services page.** For each category, don't just name it — say what it's for and why it matters to this buyer. E.g. for a security-uniform category: what garments, what they're typically used for (day-to-day duty wear), and a one-line note on durability or branding options — buyer-relevant facts, not marketing fluff.

### WHAT YOU NEED TO UNDERSTAND

Copy that tries to sound impressive usually sounds generic, because impressive-sounding language ("industry-leading," "world-class," "cutting-edge") is exactly what every unconvincing competitor also writes. Copy that sounds specific and confident, using real facts about how you actually operate, is what separates you — and it happens to also be the easiest kind to write, because you're not inventing anything, you're just describing your real process and real positioning (already defined in Module 7) in plain sentences.

### EXERCISES

1. **Write your homepage headline and sub-headline** using the formula above.
2. **Write your full "why us" section**, following the worked example's approach — specific, factual, buyer-focused.
3. **Write the description for each catalogue category**, buyer-relevant, not just a product name.
4. **Write your about/why-us page copy in full** — combine your positioning statement, your process (quote → deposit → order → inspection → delivery), and your USPs into paragraphs a visitor would actually read to the end.

A strong draft, read back to yourself, sounds like a confident, specific answer to "what do you do and why should I trust you" — not a list of adjectives. If you can delete a sentence and lose no real information, delete it.

### BUSINESS IMPLEMENTATION

1. **[ME]** Write all real copy: homepage headline/sub-headline, why-us section, catalogue descriptions, about page.
2. **[CLAUDE CODE]** Drop the finished copy into the existing site pages, replacing placeholder text.
3. **[ME]** Read every page start to finish for tone and accuracy once the copy is in place.

### CLAUDE CODE / AI BUILDING

**What we're building today:** the same three pages from Day 40, with your real, finished copy replacing all placeholder text.

**The exact prompt to give Claude Code:**
```
Update the existing website pages in business/website/ with this final
copy, replacing all placeholder text. Keep the existing layout, styling,
and navigation exactly as built — only replace text content.

Homepage headline: [paste]
Homepage sub-headline: [paste]
Homepage "why us" section: [paste full text]
Catalogue category descriptions: [paste each]
About/why-us page copy: [paste full text]

Keep formatting consistent with the existing design.
```

**What to expect:** the same site structure and design from Day 40, now reading like a real, specific, confident small business instead of a placeholder.

**How to test it:** read every page again start to finish as if you were a skeptical prospect seeing it for the first time — does it answer what you do, who it's for, why to trust you, and what to do next, within the first screen of each page?

### TODAY'S DELIVERABLES

- [ ] Final copy written for homepage, catalogue page, and about section.
- [ ] Copy dropped into the live site by Claude Code.
- [ ] Every page read start to finish and confirmed accurate and on-tone.

### END-OF-DAY CHECK

1. Does my homepage answer "what, who, why trust, what next" within the first screen?
2. Did I replace generic adjectives with specific, checkable facts throughout?
3. Would I be comfortable sending this site to a real prospect right now?

### NEXT DAY

**Day 42** adds a real contact/quote-request form to the contact page so a visitor can reach you without already having your WhatsApp number.

---

### DAY 42 — Claude Code Adds a Contact/Quote-Request Form

**Module 8: Website — Lesson 4**

### TODAY'S OBJECTIVE

Get a working quote-request form added to your contact page, so a visitor can submit their details and what they need directly from the site — your first automated lead-capture mechanism.

### WHAT YOU NEED TO LEARN

**1. What this form needs to capture**, to actually be useful as a lead-in for your sales process (Module 9): name, company name, phone/WhatsApp number, email, roughly how many staff need uniforms, and a free-text field for anything else they want to say. That's enough for you to follow up meaningfully without asking the visitor to fill in a long, off-putting form.

**2. What "working" means for a simple static site with no server.** Since your site is deliberately simple (no framework, no backend, no paid form service required), the form needs a plain, reliable way to get a submission to you — the standard, dependency-free approach is a form that opens the visitor's own email client with the details pre-filled (a "mailto" form), or a simple form service if you decide a paid option is worth it later. For v1, keep it dependency-free: no new account, no monthly cost, nothing that can silently break.

**3. Why every field should be as short as possible.** Every extra required field on a lead form measurably reduces how many people finish filling it in. Ask only what you need for a first follow-up — you'll get the rest in the discovery call (Module 9).

### WHAT YOU NEED TO UNDERSTAND

A quote-request form that's technically "on the page" but doesn't reliably get the message to you is worse than no form at all — it creates leads that quietly vanish. Today's test isn't just "does it look right," it's "if a stranger filled this in right now, would I actually receive it." Test that specifically before calling this done.

### EXERCISES

1. **List the exact fields** you want on the form, in order, and mark which are required vs. optional.
2. **Decide where submissions should land** — your business email (Module 7) is the simplest, most reliable v1 answer.

### BUSINESS IMPLEMENTATION

1. **[ME]** Decide the field list and where submissions go.
2. **[CLAUDE CODE]** Build the form on the contact page.
3. **[ME]** Submit a real test entry and confirm you actually receive it.

### CLAUDE CODE / AI BUILDING

**What we're building today:** a quote-request form on `contact.html` that reliably delivers submissions to your business email with no external service, account, or monthly cost required.

**The exact prompt to give Claude Code:**
```
Add a quote-request form to business/website/contact.html with these
fields: name (required), company name (required), phone/WhatsApp
(required), email (required), approximate staff count needing uniforms
(required), additional details (optional, free text).

On submit, the form should open the visitor's email client with a
pre-filled email to [your business email] containing all the submitted
details, clearly labeled (no external form service, no new account,
no dependencies). Style it to match the existing site design. Add a
short confirmation note near the form explaining what happens after
they submit (we'll respond within [your real turnaround promise]).
```

**What to expect:** a clean form matching the site's existing design, that when submitted, opens the visitor's email app with a ready-to-send message containing everything they entered.

**How to test it:** fill in the form yourself with realistic test data from a phone and from a desktop browser, submit it, and confirm the email that opens (or arrives, depending on the exact mechanism used) contains every field correctly labeled and readable. If anything is missing, mislabeled, or the email doesn't open correctly on either device, report the specific issue to Claude Code and get it fixed before moving on.

### TODAY'S DELIVERABLES

- [ ] Field list finalized.
- [ ] Form built on the contact page.
- [ ] Test submission completed from both phone and desktop and confirmed it reaches you correctly.

### END-OF-DAY CHECK

1. If a real stranger filled this form in right now, would I actually receive their details?
2. Does the form ask for only what I actually need for a first follow-up?
3. Does it work correctly on both phone and desktop?

### NEXT DAY

**Day 43** puts the whole site through a full test pass — functionality, mobile responsiveness, broken links, and load speed — before you buy anything or go live.

---

### DAY 43 — Testing the Website Thoroughly

**Module 8: Website — Lesson 5**

### TODAY'S OBJECTIVE

Run a complete test pass on the entire website before deploying it to a real domain, so nothing embarrassing or broken is live in front of an actual prospect.

### WHAT YOU NEED TO LEARN

**1. Why testing happens before deployment, not after.** Once a link to your site is out in the world (in a quote, in a WhatsApp message, on a Google Business listing later), broken pages or dead links cost you credibility with real prospects. Catching problems now, while the audience is just you, is free; catching them after a prospect finds them is not.

**2. The four categories to test, systematically, not just by clicking around casually:**
- **Functionality** — does every button, link, and the quote form actually do what it's supposed to?
- **Mobile responsiveness** — does every page look and work correctly at phone width, since most of your real traffic will be on phones?
- **Broken links** — does every internal link go to the right page, with no typos in file names or dead ends?
- **Load speed** — does the site open quickly, with no unnecessarily large images or files slowing it down?

### WHAT YOU NEED TO UNDERSTAND

Testing "by feel" (just clicking around a bit) reliably misses things, because you already know what the site is supposed to do and your brain fills in gaps a real visitor's wouldn't. A written checklist, worked through in order, catches what casual browsing misses — this is the same discipline as the quality-inspection habit you'll build for physical orders later (Module 13): a system beats a vibe every time.

### EXERCISES

Work through this test checklist in full, on a real device, checking off each line honestly:

**Functionality**
- [ ] Every navigation link on every page goes to the correct page.
- [ ] Every call-to-action button works and leads where it should.
- [ ] The quote-request form submits correctly and you receive it (retest from Day 42 if it's been a day or two).
- [ ] Contact details (phone, email) are correct and clickable where relevant (tap-to-call, tap-to-email on mobile).

**Mobile responsiveness**
- [ ] Every page is readable at phone width with no horizontal scrolling.
- [ ] Text isn't so small it needs zooming to read.
- [ ] Buttons and form fields are easy to tap accurately on a real touchscreen, not just a resized desktop browser.
- [ ] Nothing overlaps or gets cut off at common screen sizes.

**Broken links**
- [ ] Click every single link on every page, one at a time, and confirm it lands correctly.
- [ ] Check for typos in visible text and page titles.

**Load speed**
- [ ] Site opens promptly on a normal mobile data connection, not just fast wifi.
- [ ] No unnecessarily large images slowing pages down.

**Check your work:** if any box above is unchecked, that's a real bug — report it to Claude Code by page and specific issue (e.g. "on catalogue.html, the 'request a quote' button at the bottom links to the homepage instead of the contact page") rather than a vague "something's wrong with the catalogue page." A specific bug report gets fixed correctly the first time; a vague one costs another round trip.

### BUSINESS IMPLEMENTATION

1. **[ME]** Work through the full test checklist on a real phone and a real desktop browser.
2. **[CLAUDE CODE]** Fix every issue found, reported specifically.
3. **[ME]** Re-test anything that was fixed to confirm it's actually resolved.

### TODAY'S DELIVERABLES

- [ ] Full checklist worked through on both mobile and desktop.
- [ ] Every issue found reported specifically and fixed.
- [ ] Fixes re-tested and confirmed.

### END-OF-DAY CHECK

1. Did I test on a real phone, not just a resized desktop browser window?
2. Is every link on the site confirmed working, not just assumed?
3. Would I be comfortable sending this site's link to a real prospect right now?

### NEXT DAY

**Day 44** takes this tested site live on a real domain — a plain-language walkthrough of buying a domain and deploying, no deep technical detail required.

---

### DAY 44 — Deploying to a Real Domain

**Module 8: Website — Lesson 6**

### TODAY'S OBJECTIVE

Get your tested website live on a real, professional domain (yourbusiness.co.za or similar) that you can put on your one-pager, business cards, and quotes from now on.

### WHAT YOU NEED TO LEARN

**1. What a domain is, in plain terms.** A domain is the address people type or click to reach your site (like `yourbusiness.co.za`) instead of a long, unmemorable technical address. You rent it, annually, from a domain registrar — a company that manages domain name registrations. This is the R200-R400/year cost flagged back in the roadmap.

**2. What DNS is, in one sentence.** DNS is the system that translates your domain name into the technical address of wherever your site actually lives, so that typing your domain in a browser correctly points to your hosted site — you don't need to understand more than that to use it correctly.

**3. The three steps to going live**, in plain language:
- **Buy the domain** from a registrar — search for your chosen business name with a `.co.za` (or `.com`, if you're already thinking regionally per your Day 35 room-to-grow check) ending, and register whichever's available and matches your finalized name.
- **Choose simple hosting** — since your site is a plain static site with no server-side code, it can be hosted for free or very cheaply on a simple static-hosting service (options like GitHub Pages, Netlify, or Vercel are common, genuinely free-tier choices for exactly this kind of site; a registrar's own basic hosting is also a fine, simpler-to-manage option if you'd rather keep domain and hosting with one provider).
- **Point the domain at the hosting** — the registrar gives you a place to enter a small number of DNS settings (usually just copying values the hosting service gives you) that connect your domain name to where the site actually lives. This sounds more technical than it is: it's filling in a couple of fields the host tells you to fill in, and then waiting (usually minutes to a few hours) for it to take effect.

**4. Your email upgrade path, noted for later, not done today.** The roadmap flags that once you own a domain, you can upgrade from your Module 7 business Gmail address to a proper address on your own domain (e.g. `you@yourbusiness.co.za`) through a service like Google Workspace — worth doing once the domain exists and the business can justify the small monthly cost, not required today.

### WHAT YOU NEED TO UNDERSTAND

You don't need to become technical to do this correctly — a registrar and a hosting service both exist specifically to make this simple for non-technical business owners, and Claude Code can prepare your site files exactly the way whichever hosting option you pick expects them, and walk you through the specific screens step by step as you go. The one thing worth doing carefully is buying the domain itself, since that's the one part that's genuinely yours long-term (hosting can be changed later with far less friction than a domain name can).

### EXERCISES

1. **Search for your domain** at a registrar of your choice and confirm your preferred ending (`.co.za` most likely) is available for your exact finalized business name.
2. **Decide your hosting approach** — a free static host, or hosting bundled with your registrar — based on what feels manageable to you, not on any hard requirement.

### BUSINESS IMPLEMENTATION

1. **[ME]** Buy the domain.
2. **[CLAUDE CODE]** Prepare the site files for your chosen hosting method and walk you through the exact deployment and DNS steps for that specific host.
3. **[ME]** Complete the deployment steps and wait for DNS to take effect.
4. **[ME]** Confirm the live domain loads the correct site.

### CLAUDE CODE / AI BUILDING

**What we're doing today:** getting your already-built, already-tested site (business/website/) live at your real domain.

**The exact prompt to give Claude Code:**
```
I've bought the domain [your domain] and want to deploy the site in
business/website/ to [your chosen host — e.g. a specific free static
host, or my registrar's hosting]. Walk me through the exact steps for
this specific host, including any file preparation needed and the exact
DNS settings I need to enter at my registrar. Explain each step in
plain language before I do it.
```

**What to expect:** a specific, ordered set of steps for your exact chosen host — not generic advice — plus any small adjustments to your site files the host requires (e.g. a specific file or folder structure it expects).

**How to test it:** once DNS has had time to take effect (check back after an hour or two if it doesn't work immediately), open your real domain in a browser on your phone, on data (not just wifi), and confirm the correct, fully-tested site loads.

### TODAY'S DELIVERABLES

- [ ] Domain purchased.
- [ ] Hosting method chosen.
- [ ] Site deployed following Claude Code's exact steps.
- [ ] Live domain confirmed working on a phone, on mobile data.

### END-OF-DAY CHECK

1. Can I explain in one sentence what DNS does?
2. Does my real domain load the correct, working site?
3. Do I know where to go to renew this domain before it expires next year?

### NEXT DAY

**Day 45** is Module 8's capstone: a go-live checklist, the module quiz, and the bridge into Module 9 (Sales) — bring your live domain link.

---

### DAY 45 — Capstone: Go-Live Checklist and Module Review

**Module 8: Website — Lesson 7**

### TODAY'S OBJECTIVE

Confirm the website is genuinely ready to be shared with real prospects, review what Module 8 covered, and get ready to put the site to work in Module 9's sales conversations.

### WHAT YOU NEED TO LEARN

A go-live checklist is the final gate between "technically deployed" and "actually ready to hand to a stranger." It's short on purpose — most of the real testing already happened Day 43; today confirms nothing's drifted since then and that the live version (not just the local one) is correct.

### EXERCISES

**Go-live checklist** — confirm each on the actual live domain, not the local files:

- [ ] Domain loads correctly on both phone data and desktop wifi.
- [ ] Every link and the quote form still work on the live version.
- [ ] Business name, contact details, and colours match your brand pack exactly.
- [ ] No placeholder or test content remains anywhere on the site.
- [ ] The site is added to your company one-pager (Module 7) and your email signature.

**Module 8 review quiz:**
1. What are the website's two core jobs for this business?
2. Why didn't v1 include a shopping cart or online checkout?
3. What are the four categories you tested the site against on Day 43?
4. In one sentence, what does DNS do?

**Check your work:**
1. Credibility and lead capture.
2. This is a B2B, quote-then-deposit sales process, not consumer retail — a cart/checkout would misrepresent how the business actually operates and add complexity with no real benefit.
3. Functionality, mobile responsiveness, broken links, load speed.
4. It translates your domain name into the technical address of where your site is actually hosted, so the domain correctly points to your live site.

### BUSINESS IMPLEMENTATION

1. **[ME]** Work through the go-live checklist on the live domain.
2. **[ME]** Add the live website link to your one-pager and email signature.
3. **[ME]** Update `business/decisions-log.md` marking Module 8 complete, with the live domain recorded.

### TODAY'S DELIVERABLES

- [ ] Go-live checklist completed on the live site.
- [ ] Website link added to company one-pager and email signature.
- [ ] Module 8 quiz answered and checked.
- [ ] `business/decisions-log.md` updated.

### END-OF-DAY CHECK

1. Would I confidently send this live link to a real prospect today?
2. Is my website link now included everywhere it should be (one-pager, signature)?
3. Do I understand the difference between a domain, hosting, and DNS well enough to explain it to someone else?

### NEXT DAY

**Module 9 (Sales), Day 46** starts building your actual sales engine — the buyer's journey for a security or cleaning company owner — now that you have a credible website and one-pager to back up every conversation.
