# LUSID Overview

LUSID is the canonical internal scene and package contract for the Cult DSP immersive-audio toolchain. Its role is to provide a stable, implementation-agnostic scene representation between source-format ingest, normalization, downstream playback, and future transformation or export workflows. LUSID defines the handoff contract for scene state, timing, node identity, and audio asset binding rather than the internals of any one parser, renderer, runtime, or UI.

## Design goals

- schema-first
- human-readable
- playback-oriented
- deterministic
- implementation-agnostic
- graceful degradation

Unknown optional fields on known node types should be ignored. Unsupported non-critical node types may be ignored with warning. Playback-critical data should remain clear and stable.

## Package structure

A canonical package contains:

- `scene.lusid.json`
- `audio/`
- `metadata/`

`scene.lusid.json` is the authoritative scene document. `audio/` contains canonical audio assets referenced by the scene, and `metadata/` may contain optional provenance-oriented supporting material.

## Canonical scene document

The current top-level structure is centered on:

- `version`
- `duration`
- `sampleRate`
- `timeUnit`
- `metadata`
- `frames`

Frames are ordered by time and represent scene state at specific time positions. Motion and changing playback parameters are currently expressed through changes across successive frames. Interpolation is consumer-defined.
