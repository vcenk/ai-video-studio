# Architecture

## High-level structure

```text
ai-video-studio/
├── AGENTS.md
├── README.md
├── docs/
├── brands/
├── templates/
├── components/
├── scenes/
├── projects/
└── tools/
```

## Responsibility boundaries

### docs/
Editorial, production, design, and technical standards.

### brands/
Brand-specific colors, typography, logo usage, motion preferences, voice style, and other reusable identity rules.

### templates/
Starting points for major output types.

Examples:
- youtube-long
- youtube-short
- reel
- advertisement
- product-demo
- explainer

### components/
Low-level reusable visual primitives.

Examples:
- typography
- captions
- media frames
- chart primitives
- map primitives
- browser chrome
- audio helpers
- transition helpers

### scenes/
Higher-level reusable scene patterns.

Examples:
- Hook
- BigStatement
- BigNumber
- Quote
- Comparison
- Timeline
- Chart
- Map
- Broll
- Screenshot
- ProductDemo
- Takeaway
- CTA

### projects/
One directory per actual video.

Each project owns its:
- brief
- research
- script
- storyboard
- config
- assets
- outputs

### tools/
Internal utilities.

Possible examples:
- screenshot capture
- asset validation
- audio normalization
- subtitle conversion
- media probing
- thumbnail generation
- render validation

## Project configuration

Each project should have a machine-readable `video.json`.

Suggested fields:

```json
{
  "id": "example-video",
  "title": "Example Video",
  "format": "youtube-short",
  "aspectRatio": "9:16",
  "width": 1080,
  "height": 1920,
  "fps": 30,
  "language": "tr",
  "brand": "default",
  "renderer": "hyperframes"
}
```

## Timing

Timing must be deterministic.

Prefer frame-based timing or renderer-supported deterministic timing.

Avoid relying on:
- setTimeout-based sequencing
- real-time browser playback
- unpredictable network-dependent runtime media

## Assets

Project assets should be local or cached before final rendering.

Remote assets should not be required for reproducible final renders unless intentionally supported and validated.

## Future extension points

Architecture should leave room for:

- TTS adapters
- image-generation adapters
- AI B-roll generation
- stock-media search
- transcription
- auto-captioning
- music generation
- asset licensing metadata
- render queues
- cloud rendering
