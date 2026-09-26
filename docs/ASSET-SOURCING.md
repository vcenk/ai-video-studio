# Asset Sourcing

## Objective

Every external asset used in a final video should be traceable and appropriate for the intended use.

## Asset classes

- user-owned media
- public-domain media
- licensed stock
- generated images
- generated video
- screenshots
- charts created from sourced data
- logos and trademarks used editorially
- music
- sound effects

## Project organization

Store video-specific assets under:

`projects/<project>/assets/`

Suggested subfolders:

```text
assets/
├── images/
├── video/
├── audio/
├── screenshots/
├── logos/
├── data/
└── generated/
```

## Provenance

For non-trivial projects, keep an asset manifest recording:
- filename
- source
- license/usage basis
- date retrieved/generated
- notes

## Generated assets

Generated assets should preserve the prompt or generation metadata where practical.

## Screenshots

Screenshots should include enough source context for internal verification.

## Remote media

Do not depend on unstable remote URLs during final rendering.

Download/cache required assets locally when allowed.

## Brand assets

Reusable brand assets belong under `brands/<brand>/`, not inside random projects.

## Do not

- scrape assets without considering usage rights
- use watermarked stock
- rely on low-resolution thumbnails for final output
- mix unrelated visual styles without intention
