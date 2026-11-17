---
name: vizavi-motion
description: "Create and refine original motion videos, product/UI animations and kinetic typography — from idea and dynamic storyboard to a verified MP4 export with music and SFX."
metadata:
  version: "1.7.0"
  display_name: "vizavi_motion"
---

# vizavi_motion

The three mechanics below are the core of this skill. The optional modules help carry them out; they do not replace them and do not impose a mandatory template. The user's explicit brief — format, duration, sound and allowed resources — takes priority over defaults. A simple idea is enough: make staging decisions yourself instead of sending the user a technical questionnaire. Never invent real product properties, prices or confirmed preferences.

By default prefer plain HTML/CSS/JavaScript, SVG/Canvas and your own controlled timeline when they are enough for the quality bar. Suitable libraries and engines are allowed when genuinely needed; don't pick a framework or install dependencies up front without a reason.

## 1. Quality by default

Create lively, rich, carefully detailed animation. During active storytelling the camera moves continuously: smooth acceleration and deceleration, a coherent path, motivated tilts, diagonals, slight rotations and orbits. Show perspective depth and the relative motion of foreground, midground and background. A single linear zoom on a flat composition does not count. A technical pause or a final readable frame does not need pointless motion.

Typography takes part in the action: an expressive typeface and the plasticity of shapes, letters, words and space — not just captions appearing. Objects have weight, inertia, material, light, contact and secondary reactions. Shift emphasis and shot size without long stalls or chaotic flicker; keep the richness through hierarchy rather than by stripping the environment.

Use motion blur based on relative motion and controlled depth of field in spatial/close shots. Add radial blur for cards or deep scenes when useful; it does not replace DOF or motion blur. Preserve legibility and recognisability. By default create fitting music **and** sound design, synced to rhythm, action and style, without requiring any particular generation tool. If the brief asks for silence, there is no audio. Never call a silent result scored. Details: [motion and sound](references/motion-and-sound.md).

Periodically tie transitions, cuts and significant actions to expressive accents in the actual music/SFX. These are meaningful sync points, not a mandatory cut on every beat.

## 2. Direction before implementation

Before the full build, develop one original idea/thread and a complete dynamic storyboard. For **each scene** propose 3–5 substantially different short creative options and pick the strongest for the whole. Short options, the chosen solution and a practical storyboard are enough; internal reasoning is not required.

For each shot fix: semantic accent, composition and layers, object action/change, text and its motion, camera, light/focus, entry from the previous scene, exit into the next, sound and rhythm. Scenes must develop the story causally. A circle, the letter O or a portal is only one possible device; don't repeat it automatically. 2–3 devices may be combined if they form one coherent action. Before an expensive build, test the main technical or artistic risk with a short probe. Details: [storyboard](references/storyboard.md).

## 3. Mandatory iteration after the first build

Treat the first build as an internal unfinished draft by default; don't hand it over as final. Watch the whole video, every scene and every transition; with sound, listen to the music, SFX and full mix. Check meaning, dull holds, pacing, camera, legibility, form, artifacts, seams and sync. Fix the root causes found, then re-check what changed and the whole. Never claim the skill is proven effective because instructions exist or one frame looks good.

Default deliverable: a finished **MP4 — 1920×1080, 60 fps, H.264, yuv420p, AAC audio**, unless the user asked for no sound. Also keep HTML/JS and other editable sources; 4K on request; explicit brief parameters beat defaults. An HTML preview does not replace the finished video.

Also check the **final decoded export**: its start, end, scene boundaries and technical parameters. Code, a contact sheet and a frame count do not replace perceiving the motion and sound. If a needed tool is unavailable, honestly name the specific unverified property and deliver the available artifact with the matching status, without calling it verified. Finish once significant defects are fixed and the brief's criteria are met; optional taste alternatives don't require endless rework. Details: [review and export](references/review-and-export.md).

### Optional modules — only when the task needs them

- Video or several references: [analysis and combination](references/video-references.md).
- Image series, a character, alpha: [identity continuity](references/image-continuity.md); choosing an image source: [image providers](references/image-providers.md).
- Ready-made 3D models, materials, hinges: [3D assets](references/models-3d.md); where to get them: [3D sources](references/3d-sources.md).
- Product interface animation, cursor and states: [SaaS/UI motion](references/saas-ui-motion.md).
- Agreed styles and verified sources: [registry](references/styles-and-sources.md). The six selected parts of the tutorial demo apply only to that demo; for other videos choose the language from their brief.
