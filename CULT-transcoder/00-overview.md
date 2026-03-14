# CULT Transcoder Architecture Docs

This set reframes the internal design spec as diagram-first documentation.

## Intended use
- systems architecture review
- data flow review
- toolchain boundary clarification
- implementation planning

## Canonical framing
CULT is a **scene-first transcoder**. It ingests immersive-audio source formats, extracts source-specific metadata and structure, normalizes them into a canonical scene model aligned with **LUSID Scene v0.5**, and emits canonical scene outputs plus reporting artifacts. Fixed-channel rendering and layout commitment remain downstream responsibilities, primarily in Spatial Root.

## Included docs
- `01-system-context.md`
- `02-core-systems-architecture.md`
- `03-transcoding-dataflow.md`
- `04-format-ingest-paths.md`
- `05-validation-and-reporting-flow.md`
- `06-toolchain-boundaries.md`
- `07-extensibility-roadmap.md`
