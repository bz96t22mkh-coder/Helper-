# Module 2 — Software Selection & Your First Edit

## Choosing your editor

There are three programs worth seriously considering for a beginner building a Gaming + Reaction channel. Here's the honest comparison (verify current pricing yourself before committing — software pricing changes):

| | **DaVinci Resolve** (free) | **Adobe Premiere Pro** | **CapCut Desktop** |
|---|---|---|---|
| **Cost** | Free version: no watermark, no time limit, no feature gate on core editing/audio/color/effects. Optional one-time Studio upgrade (~$295) unlocks extras like advanced noise reduction and Magic Mask — not needed to start. | Subscription (~$20+/month as part of Creative Cloud), ongoing cost forever. | Free plan exists, but its Terms of Service **restrict commercial use** — a monetized YouTube channel is commercial use. A paid Standard/Pro plan (~$10–20/month) is required for a commercial-use license on content you create in the app. |
| **Learning curve** | Moderate — more powerful, so slightly more to learn, but the free "Cut" page is built for fast, simple editing. | Moderate–steep, industry-standard layout. | Easiest — built for speed and mobile-style workflows. |
| **Power/ceiling** | Very high — editing, color grading (Resolve's specialty), audio mixing (Fairlight), and visual effects (Fusion) all built in. You will not outgrow it. | Very high, huge plugin/template ecosystem, standard in professional studios. | Limited — fine for quick edits and short-form, weaker for structured multi-track long-form editing, keyframe control, and complex audio work. |
| **Built-in music/SFX safety** | None built in — you bring your own properly licensed assets (Module 4). | None built in (Adobe Stock is a separate paid add-on). | Has built-in music, but **library tracks are often registered with YouTube's Content ID by the original rights holder** — using them can redirect ad revenue on your video away from you even if you're a paying CapCut subscriber. Don't trust "built into the editor" as proof it's safe for monetized YouTube. |
| **Performance** | GPU-hungry but efficient once set up; runs well on modest hardware for 1080p work. | Can be heavier on RAM; generally solid. | Lightest, since it's built for simpler edits. |
| **Best for** | A serious, long-term YouTube editor who wants one tool that scales from "first cut" to "full comedic sound design and color" without switching software later. | Studios/teams already inside the Adobe ecosystem, or where a client requires Premiere project files. | Fast turnarounds, Shorts/TikTok-first content, editors who don't want a subscription and don't need deep timeline control. |

### The recommendation

**Learn DaVinci Resolve.** Reasoning, specific to this channel:

1. **It's genuinely free** with no functional handicap for what a Gaming + Reaction channel needs — full timeline control, keyframing, color, and Fairlight audio (crucial for balancing commentary, game audio, music, and SFX — Modules 10–12). No recurring cost is a real advantage for a channel just starting out.
2. **It has one of the largest free tutorial ecosystems on YouTube** — which matters, because your editor will be learning *from* YouTube while editing *for* YouTube.
3. **It won't be outgrown.** Premiere and Resolve are both professional-grade; there's no "upgrade path" you're missing by starting on Resolve. CapCut, by contrast, will start to feel limiting once you need frame-accurate multi-layer comedic editing (stacked memes + zoom + text + SFX on one moment).
4. **The commercial-use licensing is unambiguous** — the free version's license doesn't carry the same "is my plan actually cleared for a monetized channel" question CapCut's free tier does.

You are learning **one program**, not three. Every lesson from here forward in this course uses DaVinci Resolve terminology (Media Pool, Cut/Edit page, Inspector, Fairlight, Deliver page). If the creator or a future collaborator works in Premiere, the *concepts* (cutting, keyframing, ripple edits, exporting) transfer directly — only button locations change.

## Your first edit: import to export

Follow this in order, on a short (1–2 minute) piece of throwaway gaming footage. Don't worry about it being good — the goal is muscle memory with the basic loop, not a finished video.

### Step 1 — Install and create a project
1. Download DaVinci Resolve free from Blackmagic Design's official site and install it.
2. Open it → **New Project** → name it using your Module 1 convention (e.g., `2026-09-03_MinecraftEp12`).
3. Immediately **File → Save Project** into that episode's `02_Project_Files/` folder.

### Step 2 — Import footage
1. Go to the **Media** page (bottom toolbar).
2. In the **Media Storage** panel, browse to your `01_Raw_Footage/` folder.
3. Drag the footage into the **Media Pool** (bottom-left panel). This doesn't move or copy the file — Resolve just links to it, so don't move the original file afterward or you'll break the link.

### Step 3 — Create a timeline
1. Right-click your imported clip in the Media Pool → **New Timeline Using Selected Clips** (this auto-matches the timeline settings to your footage — the easiest way to start).
2. You're now on the **Cut** or **Edit** page, looking at your timeline with the clip already on it. (Cut page = simplified, fast editing; Edit page = full control. Start on Cut, move to Edit once comfortable — Module 6 covers both.)

### Step 4 — Cut clips
1. Move the playhead (the vertical line) to the point you want to cut.
2. Press **B** (Blade tool) then click on the clip at the playhead — or use the keyboard shortcut **Ctrl/Cmd+B** to split at the playhead directly.
3. You now have two separate clips you can work with independently.

### Step 5 — Move clips
1. Switch back to the **Selection** tool (**A**).
2. Click and drag a clip left/right on the timeline to reposition it. Resolve will show ripple/overwrite behavior depending on mode — for now, use it in a way where gaps don't appear (drag onto an empty part of the timeline, or use ripple mode — Module 6 explains ripple edits properly).

### Step 6 — Delete sections
1. Select the unwanted clip/section.
2. Press **Shift+Delete** (or right-click → **Ripple Delete**) to remove it *and* close the gap automatically, rather than plain **Delete**, which leaves a black gap behind.

### Step 7 — Add audio and music
1. Import a music/SFX file the same way you imported video (drag into Media Pool).
2. Drag it onto an **audio track** below your video track (Resolve auto-creates tracks as needed, or right-click the track header → **Add Track → Audio**).
3. Trim it the same way you trimmed video (Blade tool, drag edges).

### Step 8 — Add images
1. Drag an image file into the Media Pool, then onto a **video track above** your main footage (this is how overlays/memes work — higher tracks render on top of lower ones).
2. Trim its duration by dragging its edges on the timeline, same as any clip.

### Step 9 — Add text
1. Go to the **Effects Library** (top-left, Edit page) → **Titles**.
2. Drag a basic text title onto a video track above your footage.
3. Double-click it, and use the **Inspector** panel (top-right) to type your text and adjust size/position/font.

### Step 10 — Add transitions
1. In the Effects Library, open **Transitions**.
2. Drag one (start with a simple **Cross Dissolve**) onto the boundary between two clips on the timeline.
3. Use sparingly — Module 7 explains why hard cuts, not transitions, are the default in fast-paced YouTube comedic editing.

### Step 11 — Export
1. Go to the **Deliver** page.
2. Choose a preset — **YouTube 1080p** is a safe starting point (or 4K if your footage is 4K).
3. Set the **Filename** and **Location** (your project's `04_Exports/Drafts/` folder), following your Module 1 naming convention.
4. Click **Add to Render Queue**, then **Start Render**.

## Do this before Module 3

Complete the full loop above once on throwaway footage: import → cut → rearrange → delete a section → add music → add an image → add text → add one transition → export. Don't aim for funny yet — aim for *comfortable with the buttons*. Time yourself; if it takes over 30 minutes the first time, that's completely normal.

Then move to [Module 3: Copyright & Licensing Basics](03-copyright-basics.md) — **do not skip ahead to pulling memes and music into real videos before reading it.**
