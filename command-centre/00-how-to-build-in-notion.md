# How To Actually Build This In Notion

Two ways to get this into your Notion account. Read §0 to pick, then follow the path.

## 0. Pick a path

| | Manual build (below) | Notion connector |
|---|---|---|
| What it is | You click through Notion yourself, following exact steps | You connect your Notion account to Claude, and Claude creates the pages/databases for you via the Notion API |
| Works right now, in this conversation? | Yes | **No** — this conversation is a coding session wired to your GitHub repo, not a general claude.ai chat. It can't reach your Notion account even if you connect it. |
| How to use it | Follow §1–§6 below | Go to claude.ai → Settings → Connectors → find **Notion** → Connect → authorize it to access your workspace/pages. Then open a **new, regular Claude chat** (not this one) and say "build my life command centre from this spec" and point it at this repo's `command-centre/` folder. It can then create pages, databases, and content directly. |

**My recommendation: do the manual build.** It's the same total effort either way (the connector still needs you to review/approve everything it creates, and mistakes are harder to fix after the fact than to avoid by building it yourself once, carefully). The manual path also means you actually understand where everything lives, which matters for a system you're going to run your life through daily. Budget **2–3 hours**, one sitting if possible.

---

## 1. Create the workspace

1. Go to notion.so, sign in (or create a free account).
2. Sidebar → **+ New page** → name it **🧭 Command Centre**. Leave it empty for now — this is your parent page, everything else nests under it.

## 2. Build each database using CSV import (fastest way to get rows in)

I've pre-built the row data for you as CSV files in `command-centre/csv-imports/` in this repo:
- `pillars.csv` → 8 rows, ready to import as-is
- `phases.csv` → Trading's full 9-phase ladder + AI/Uniform Phase 1 + all 20 Personal Development sections, ready as-is
- `curriculum-items-personal-development.csv` → the real Section 1, Day 1–6 content
- `goals.csv` → your Life Vision + 7 starter 90-Day goals

**To import each one:**
1. Open your **Command Centre** page.
2. Type `/` → choose **Import**.
3. Select **CSV** as the source, choose the file from your computer (download it from this repo first — open the file on GitHub, click "Raw," save it, or clone the repo).
4. Notion creates a new full-page database named after the file, with one column per CSV header and one row per line. Rename the page to match the names in `01-notion-architecture.md` (e.g. rename to "⭐ Pillars", "📈 Phases", "📖 Curriculum Items", "🎯 Goals").

Do this 4 times — once per CSV. That gets ~45 rows of real data into Notion in about 10 minutes total, instead of typing them by hand.

## 3. Fix property types after each import

CSV import makes every column plain **Text**. You need to change some to their real type, per the exact spec in `01-notion-architecture.md`. For each database, click the column header → **Edit property** → change **Type**:

- **Pillars:** `Priority` → Select (it'll auto-create the 4 options from your existing text values). `Status` → Select.
- **Phases:** `Status` → Select (options: Not Started, Active, Ready for Review, Completed). `Order` → Number.
- **Curriculum Items:** `Order` → Number. `Est. Minutes` → Number. `Type` → Select. `Status` → Select.
- **Goals:** `Level` → Select. `Status` → Select. `Target Date` → Date.

## 4. Add the databases that don't need pre-loaded rows

These start empty — create them directly (Command Centre page → `/table` → **Table - Full page**, name it, then add properties one by one via the **+** at the right end of the column headers): **Courses**, **Projects**, **Tasks**, **Habit Tracker**, **Trade Journal**, **Backtest Log**, **Strategies**, **YouTube Pipeline**, **Reading Log**, **Finance Tracker**, **Reviews**, **Weekly Time Summary**. Full property lists for every one of these are in `01-notion-architecture.md` §2–§14 — go column by column, typing the property name then picking its Type from the dropdown.

For **Courses**, add these 4 rows by hand (only 4, faster than a CSV): Personal Development Mastery Course (Content Status = ✅ Available), Day Trading Course, AI Automation Agency Course, Uniform Outsourcing Agency Course (all three ⏳ Needs Content until you give me their material — see the bottom of this message).

## 5. Wire up relations, rollups, formulas, and the button

This is the part CSV import can't do — do it once per database, it only takes a few minutes each since you already have the rows:

1. **Relations:** on each database, add a property → Type **Relation** → pick the target database. Then open each row and link it (e.g. on every Phases row, click into `Pillar` and pick the matching Pillar — with only ~30 rows this is quick).
2. **Rollups:** add property → Type **Rollup** → pick the Relation to go through → pick which property of the related page to show → pick the calculation (Sum/Percent/Count as specified per-database in `01-notion-architecture.md`).
3. **Formulas:** add property → Type **Formula** → paste the exact formula text given in `01-notion-architecture.md` (e.g. Tasks' `Variance` formula, the Priority-icon formula) into the formula editor.
4. **The Complete Phase button** (on Phases): add property → Type **Button** → **Edit** → add action **Edit page** (this page) → set `Status` = Completed → add a second action **Edit related page's property**, follow `Next Phase` → set `Status` = Active. Full spec in `01-notion-architecture.md` §9.

## 6. Build the views and the Today dashboard

For each database, click **+ Add a view** at the top to create the Table/Board views listed in `01-notion-architecture.md` (e.g. Tasks → "Today" view: Filter → `Date` → `is` → `Today`; Group by → `Pillar`; Sort → `Priority`). Then build the **TODAY** page last (§15 of that file) by going to your Command Centre page, typing `/` → **Linked view of database** → picking Tasks' "Today" view, and repeating for Phases' "Active Only" view and today's Habit Tracker row.

---

## Your day trading course and business courses — I still need these

You mentioned you have a day trading course and business courses to do during the day. I want to build their real daily content the same way I did for Personal Development (exact module/lesson/exercise, not a generic placeholder) — but I don't have that material. I checked this entire repository and it only contains the Personal Development course; the trading and business course content isn't here.

To finish this properly, send me one of these:
1. **Paste the course outline** here (module names, lesson titles, and roughly what each covers) — even a rough list is enough for me to do the workload analysis from your original brief and turn it into real daily assignments.
2. **Point me at where it lives** — another GitHub repo (tell me the name, I can request access), a Notion page, a doc, an export file — and I'll pull it in directly.
3. If the course only exists as videos/a platform you're enrolled in (not text), tell me the platform and structure (course name, module list) and I'll build the tracker around that structure, with you filling in lesson-level detail as you go.

Once I have it, I'll update `command-centre/04-personal-development-integration.md`-style real content for Trading, AI Agency, and Uniform Agency, replacing every `[COURSE CONTENT NEEDED]` placeholder in `06-first-90-days.md` with your actual Day 1 tasks.
