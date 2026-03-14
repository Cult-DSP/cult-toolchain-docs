# Spatial Seed Architecture Docs

This set reframes the internal Spatial Seed system design as a diagram-first documentation package.

## Intended use
- systems architecture review
- data flow review
- module boundary clarification
- implementation planning

## Canonical framing
Spatial Seed is an **offline procedural authoring system**. It takes isolated stems as the canonical input, optionally uses a stereo reference mix for context, derives spatial behavior through analysis plus Seed Matrix control, and emits **scene/package outputs** rather than committing to final rendering. Its primary output is a **LUSID package** and its secondary output is **ADM/BW64 export**.

## Included docs
- `01-system-context.md`
- `02-core-systems-architecture.md`
- `03-offline-authoring-dataflow.md`
- `04-procedural-module-flow.md`
- `05-input-normalization-and-analysis.md`
- `06-output-contracts-and-boundaries.md`
- `07-validation-gaps-and-roadmap.md`
