# AI Video Studio

Internal video production framework for faceless YouTube videos, Shorts/Reels, advertising creatives, product demos, explainers, and branded video assets.

## Core principle

This repository is not a single channel project. It is an in-house production system.

- **Codex** acts as the production agent.
- **HyperFrames** is the initial programmable rendering engine.
- External tools may provide research, images, B-roll, voice, music, screenshots, or generative footage.
- Each video is treated as an independent project with its own brief, script, storyboard, assets, and output.
- Shared components, templates, and brand systems are reusable across projects.

## Intended outputs

- 16:9 YouTube long-form faceless videos
- 9:16 YouTube Shorts
- Instagram Reels
- TikTok-style vertical videos
- SaaS/product advertising
- Product demos
- Explainers
- Data-driven videos
- Branded social media creatives

## Repository philosophy

The system should optimize for:

1. Retention
2. Clarity
3. Reusability
4. Fast iteration
5. Deterministic rendering
6. Brand consistency
7. Human review before publishing

See `AGENTS.md` and the `docs/` directory before implementing video features.
