# Module 9 — Zoom & Camera Movement

Zooms are probably the single most-used technique in this editing style, which means they're also the easiest to overuse or make look amateurish. This module is about making every zoom feel like a deliberate choice, not a tic.

## The moves

- **Zoom-in / punch-in**: scale increases, drawing the viewer's focus tighter onto the frame (usually onto a face or a specific on-screen detail).
- **Zoom-out**: scale decreases, usually used to reveal something (context, a second element entering frame) or to "release" tension after a punch-in.
- **Punch-in specifically** refers to a *fast, often instant or near-instant* zoom — a hard jump in scale, not a smooth glide — used for comedic emphasis (contrast this with a slow keyframed zoom, used more for building tension, per Module 8's table).
- **Keyframed movement**: a smooth animated move between two states over a set duration, built exactly as practiced in Module 6 (two keyframes, value changes between them) — used for pans, slow zooms, or simulated "camera" drift on a static image/screenshot.
- **Sudden scale changes**: an instant cut from one static scale to another, no animation at all (a "cut zoom") — often *funnier and punchier* than an animated zoom because it mimics a hard edit rather than a camera move.
- **Position changes**: moving the framing (X/Y) rather than or in addition to scale — e.g., pushing in specifically toward a face in the corner of frame rather than the frame's center.

## What makes a zoom feel intentional vs. amateurish

The difference is almost never the zoom itself — it's **timing, speed, and restraint.**

- **Timing**: the zoom should land exactly on the beat of the moment it's emphasizing — a half-second early or late and it reads as sloppy, even if viewers can't articulate why. Nudge it frame-by-frame against the audio/reaction until it feels locked in.
- **Speed matches intensity**: a subtle punch-in (small scale change, fast) for a mild moment; a bigger, more dramatic scale jump for a big moment (Module 8's pairing table). A huge zoom on a small joke feels like the edit is overselling it — the opposite failure of a tiny zoom on a huge reaction, which feels like it's underselling it.
- **Consistency of style within a video**: pick a "zoom language" for the video (e.g., "punch-ins are always a hard cut-zoom, never eased") and stay consistent, rather than randomly mixing smooth and hard zooms with no logic — random mixing is what reads as amateurish, not the zooms themselves.
- **Restraint**: not every funny line needs a zoom (Module 8's core rule). A video with a zoom on literally everything trains the viewer to stop noticing zooms as meaningful at all.
- **Clean execution**: no visible edge artifacts (avoid zooming in so far that footage looks pixelated/blurry — Module 6's Transform panel shows the zoom percentage; as a rough guide, keep zooms under roughly 130–150% on 1080p-sourced footage before quality visibly degrades, more headroom if your source is 4K), and the zoom should never clip an important part of the frame (a face, on-screen text) awkwardly.

## Building a punch-in (practical, step-by-step)

1. Select the clip in the timeline, open Inspector → **Transform**.
2. Set the playhead to the exact frame the moment lands (the punchline, the reaction).
3. For a **hard cut-zoom** (no animation): use the Blade tool to split the clip at that exact frame, select the *second* half, and directly set its Zoom value higher (no keyframes needed — it's an instant jump because it's technically now a new clip).
4. For a **smooth punch-in**: keyframe the Zoom value from 1.0 to your target scale over a short window (roughly 4–8 frames for a fast punch feels snappy; longer feels more like a slow reveal — try both and trust your eye).
5. Play it back against the audio. Adjust the exact frame the zoom starts by a few frames in either direction until it feels locked to the moment rather than slightly ahead of or behind it.

## Exercises for mastering comedic zooms

1. Take one reaction clip and apply three different zoom treatments to the same moment (subtle smooth punch-in, hard cut-zoom, big dramatic slow zoom). Compare them back to back — notice how differently the *same* footage reads depending only on the zoom choice.
2. Take five different moments of varying intensity from one piece of footage (a mild joke, a big reaction, a jumpscare-style surprise, an awkward silence, a victory) and apply the Module 8 pairing table's suggested zoom treatment to each. Watch the sequence back — does the *variation* in zoom intensity across the five feel matched to the variation in the moments themselves?
3. Deliberately zoom on a moment that doesn't need it, then watch it back next to the same moment left alone. This builds the instinct for "does this moment actually call for a zoom" faster than any amount of reading about it.

Move to [Module 10: Memes & Visual Comedy](10-memes-visual-comedy.md).
