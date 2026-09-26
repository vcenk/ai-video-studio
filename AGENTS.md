# AGENTS.md

This file defines how Codex and other coding agents should work inside AI Video Studio.

## Mission

Build and maintain an internal programmable video production system capable of producing high-quality faceless YouTube content, short-form vertical videos, ads, explainers, product demos, and branded video assets.

The system must not behave like an automated slideshow generator.

Every scene must answer:

- What is the viewer hearing?
- What should the viewer see at that exact moment?
- Why is that visual the best representation of the narration?
- What keeps attention from dropping?

## Core rules

1. **Storyboard before implementation.**
   Do not build a final video composition without an approved or internally coherent storyboard.

2. **Visualize ideas, not sentences.**
   Never default to putting narration text over a generic image.

3. **Prefer meaningful visual transformation.**
   Use charts, numbers, maps, diagrams, UI animation, screenshots, B-roll, compositing, kinetic typography, and transitions when they explain the idea better.

4. **Design for retention.**
   Long static shots, repeated layouts, and visually redundant scenes should be avoided unless intentionally used for contrast.

5. **Use reusable components.**
   If a visual pattern appears more than once, prefer turning it into a shared component.

6. **Keep projects isolated.**
   A project's research, script, assets, output, and local configuration belong under `projects/<project-name>/`.

7. **Keep framework logic reusable.**
   General components, templates, utilities, and render tooling must not be hard-coded to one video.

8. **HyperFrames is an implementation dependency, not the identity of the system.**
   Architecture must allow future use of additional renderers or external generative video systems.

9. **Human review is required before publication.**
   The repository may automate production, but not final editorial judgment.

## Required production order

For a new video project, follow:

1. Brief
2. Research
3. Angle
4. Hook
5. Script
6. Visual script
7. Storyboard
8. Asset plan
9. Voice/audio plan
10. Scene implementation
11. Captions
12. Render
13. Quality control
14. Final export

## Mandatory project files

Each significant video project should include:

- `brief.md`
- `research.md`
- `script.md`
- `storyboard.md`
- `video.json`
- `assets/`
- `output/`

## Scene quality standard

A scene definition should normally include:

- timing
- narration
- purpose
- visual description
- on-screen text
- animation
- media/B-roll
- audio/SFX
- transition in
- transition out

## Faceless video standard

Avoid this weak pattern:

- narration says a fact
- generic stock photo appears
- narration says next fact
- another generic stock photo appears

Prefer:

- claims become visual structures
- numbers animate
- relationships become diagrams
- locations become maps
- chronology becomes timelines
- comparisons become split screens or charts
- product concepts become UI demonstrations
- abstract ideas become motion metaphors
- narration and visual timing reinforce each other

## Editing rhythm

Use visual changes intentionally.

Short-form videos generally need faster pacing than long-form videos. Pattern interrupts can include:

- scale changes
- typography changes
- chart reveals
- hard cuts
- sound accents
- B-roll swaps
- camera pushes
- color-field changes
- unexpected visual metaphors
- UI overlays
- animated arrows or callouts

Do not over-edit every second. Use contrast.

## Code expectations

- Prefer clear, composable modules.
- Keep timing deterministic.
- Avoid animation logic tied to wall-clock timing.
- Centralize aspect ratio, frame rate, duration, theme, and typography settings.
- Keep assets referenced through project-local manifests where practical.
- Avoid unexplained magic numbers.
- Add comments only where the implementation would otherwise be unclear.

## Rendering

Initial renderer: HyperFrames.

The architecture should allow:
- 16:9
- 9:16
- 1:1
- multiple resolutions
- multiple frame rates where supported
- preview renders
- final renders

## Final check before declaring a video complete

Verify:

- no missing assets
- no overflow/cropping
- captions are readable
- on-screen text is legible on mobile
- narration timing matches scenes
- music does not overpower voice
- SFX are intentional
- no scene feels visually dead
- no unlicensed or questionable asset is used
- project can be rendered again reproducibly
