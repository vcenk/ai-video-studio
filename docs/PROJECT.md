# Project Definition

## What AI Video Studio is

AI Video Studio is an internal content production framework for creating reusable, programmable video workflows.

It supports multiple channels, brands, and formats from one codebase.

## Primary use cases

### Faceless YouTube
Long-form explanatory, educational, business, technology, finance, documentary-style, and narrative content.

### Short-form
YouTube Shorts, Instagram Reels, and TikTok-style vertical content.

### Advertising
Performance creatives, product ads, SaaS ads, launch videos, and feature promos.

### Product communication
Product demos, feature explainers, onboarding videos, release videos, and UI walkthroughs.

## Non-goals

The project is not intended to become:

- a full public CapCut replacement in the first phase
- a general-purpose nonlinear editor
- a one-click publishing bot
- a system that publishes without review
- a single-brand locked template library

## Design goals

- reusable scenes
- reusable brand themes
- reusable templates
- programmable rendering
- agent-friendly project structure
- clear separation between editorial and rendering logic
- low friction for creating a new video
- support for external AI media generation

## Renderer strategy

HyperFrames is the initial renderer.

The repository should remain renderer-agnostic enough that future workflows could incorporate:

- Remotion
- generative video APIs
- external compositing tools
- browser capture
- FFmpeg pipelines

## Editorial model

The system should optimize for meaningful visual storytelling, not merely transcript visualization.

Narration should drive meaning.
Visuals should add information, emphasis, contrast, or emotional context.
