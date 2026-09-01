# Module 6 — Software Deep Dive

Module 2 got you through one basic import-to-export loop. This module builds real fluency: the specific techniques that make up 90% of a Gaming + Reaction editor's actual day-to-day work in DaVinci Resolve. Go through these in order — each builds on the last.

## The Edit page vs the Cut page

You have two editing workspaces in Resolve:
- **Cut page**: simplified, fast, good for quick trims and rough assembly.
- **Edit page**: full control — multiple tracks, precise keyframing, detailed Inspector settings. **This is where you'll do almost all real comedic editing** (stacked memes, zooms, text, precise sound sync). Default to the Edit page from here on.

## Timeline fundamentals

The timeline is made of **tracks** — video tracks stack visually (higher track = rendered on top), audio tracks mix together. A typical Gaming + Reaction video timeline might look like:

```
V4: Text/captions
V3: Memes/reaction images
V2: Facecam
V1: Gameplay (or reaction footage)
A3: SFX
A2: Music
A1: Voice/game audio
```

Right-click a track header → **Add Track** to build this out. Keep it consistent across projects so you always know "memes go on V3" without thinking.

## Cutting and trimming

- **Blade tool (B)**: click on a clip to split it at that point. Use this to cut out a moment you want to isolate.
- **Trimming**: hover over a clip's left or right edge until the cursor changes, then drag. This shortens/lengthens the clip *without* moving other clips (it opens a gap unless you're in ripple mode — see below).
- **JKL playback**: press **L** to play forward, **K** to pause, **J** to play backward — tap repeatedly to change speed. This is the fastest way to scrub through footage looking for a moment, far faster than dragging the playhead by hand. Learn this early; it will save you hours.

## Ripple edits

A **ripple edit** trims a clip *and* automatically shifts everything after it to close the gap, keeping your whole timeline glued together with no dead black gaps. This is different from a normal trim, which leaves a gap.

- **Ripple Delete** (Shift+Delete on a selected clip, or right-click → Ripple Delete): removes the clip and pulls everything after it forward.
- **Ripple trim**: with the **Trim Edit** mode active, dragging a clip's edge also shifts subsequent clips, instead of leaving a gap.

**Why this matters for pacing (Module 16):** almost all of your "remove the boring part" work is ripple edits. If you just delete a section without rippling, you leave a black gap or silence that's just as bad as the boring footage was.

## Audio basics

- Drag audio (music/SFX/voice) onto its own track (A1, A2, A3…), same as video.
- **Volume**: select a clip → Inspector (top-right) → Audio tab → adjust Volume/Gain. Or drag the small volume line directly on the clip in the timeline.
- **Fades**: hover near a clip's top corner until a fade handle appears, drag inward to create a fade-in/fade-out — use this on music so it doesn't start/stop abruptly (Module 12 covers exactly when).
- **Audio Inspector → EQ/Dynamics** (basic): lets you cut harsh frequencies or even out volume — covered practically in Module 10–11's balancing sections.

## Video layers, images, and positioning/scaling

- Any clip or image on a **higher video track renders on top of** lower tracks — this is how facecams, memes, and text overlay gameplay.
- Select a clip → Inspector → **Transform** panel: **Zoom** (scale), **Pan**/**Tilt** (X/Y position), **Rotation**. This is how you position a facecam in a corner, or scale a meme image to a comfortable on-screen size.
- Drag the on-screen bounding box handles directly in the preview window for a fast, visual way to resize/reposition instead of typing numbers.

## Text

- **Effects Library → Titles → Text** (basic) or **Text+** (more control — use this one). Drag onto a track above your footage.
- Inspector lets you set font (Module 4/5's font library), size, color, position, and — importantly for comedic text — **outline/stroke and drop shadow**, which keep white/bold text readable over any busy gameplay background.

## Keyframes (the core skill behind zooms, motion, and animated effects)

A **keyframe** stores a value (position, scale, opacity, etc.) at a specific point in time. Set two different keyframes at two different times, and Resolve automatically animates *between* them — that's how a static image becomes a punch-in zoom or a meme that slides on screen.

**Basic keyframe workflow (do this now as a drill):**
1. Select a clip, open Inspector → Transform.
2. Move the playhead to where you want the zoom to *start*. Click the small keyframe (stopwatch/diamond) icon next to **Zoom** to add a keyframe at the current value (e.g., 1.0).
3. Move the playhead forward a few frames to where you want the zoom to *land*. Change the Zoom value (e.g., to 1.15). A new keyframe is created automatically because keyframing is active.
4. Play it back — the image now smoothly (or sharply, depending on spacing) scales up between those two points.

This exact mechanic — two keyframes, a value change between them — is the entire technical basis for Module 9's comedic zooms. Master this drill before moving forward.

## Speed changes

Right-click a clip → **Change Clip Speed**, or use the Inspector's speed control. A few uses specific to this channel's style:
- **Speed ramps** (gradual speed-up) to build energy heading into a payoff moment.
- **Fast-forward through genuinely dead/repetitive gameplay** (Module 13) instead of cutting it entirely, when you still want the viewer to see progress happened.
- Keep audio pitch-correction in mind — most software auto-corrects pitch on speed changes by default; occasionally an intentionally pitched-up/down voice is used for comedic effect (use sparingly).

## Basic effects and color correction

You don't need to become a colorist. What you need:
- **Color page (basic use)**: select a clip, go to the Color page, use the **Color Wheels** (Lift/Gamma/Gain) to fix footage that's too dark or has a color cast, and the **Contrast/Saturation** sliders to make footage feel punchier and more vivid — gaming/reaction content generally benefits from slightly boosted saturation and contrast versus flat raw footage.
- **Effects Library → Effects/OpenFX** on the Edit page: basic blur, glow, or vignette can be dragged onto a clip like a transition, useful for freeze-frame emphasis (Module 9) or a dreamy "flashback" look.

## Audio balancing

Covered in depth in Modules 10–12, but the mechanical basics: keep the creator's **voice as the loudest, clearest element**, game audio secondary, music and SFX supporting — never competing. Watch the Resolve **audio meters** (top of the Fairlight/Edit page) and keep voice peaks comfortably below clipping (the red zone), with music sitting noticeably lower under it.

## Transitions

Covered philosophically in Module 7, but mechanically: drag one from **Effects Library → Transitions** onto the boundary between two clips (or onto one clip's edge for a fade to/from black). Adjust duration by dragging its edges once placed.

## Export settings

On the **Deliver** page:
- **Format**: MP4, Codec: H.264 (widely compatible, reasonable file size) — H.265 gives smaller files at the same quality but slightly longer render times; either works for YouTube upload.
- **Resolution**: match your project (1080p most common for this channel type; 4K if source footage supports it).
- **Frame rate**: match your source footage exactly (don't convert 60fps gameplay down to 30fps on export — you lose the smoothness that matters for gaming content).
- **Bitrate**: use the built-in **YouTube 1080p/4K preset** — it's tuned to YouTube's re-compression, so you don't need to hand-tune this as a beginner.
- Always export to `04_Exports/Drafts/` first (Module 1), review the actual exported file (not just the timeline preview) before sending it anywhere, then move the approved final into `04_Exports/Final/`.

## Do this before Module 7

On a throwaway clip: build a 3-track timeline (gameplay, one image overlay, one text element), ripple-delete a section cleanly, keyframe a simple zoom-in on the image, add one basic color boost, and export it. If all of that runs smoothly without you needing to look up a button, you're ready for the creative modules.

Move to [Module 7: YouTube Editing Principles](07-youtube-editing-principles.md).
