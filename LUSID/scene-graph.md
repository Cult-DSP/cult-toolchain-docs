# LUSID Scene Graph

LUSID currently behaves like a time-indexed scene graph. The authoritative scene document is `scene.lusid.json`. Rather than a single static hierarchy, the scene is serialized as an ordered sequence of frames, and each frame contains typed nodes describing scene state at that time.

## Core ideas

- one authoritative scene document
- one ordered timeline of frames
- typed nodes within each frame
- stable node identities across time
- explicit asset binding for audio-bearing nodes
- consumer-defined interpolation between serialized states

## Core node types

Playback-critical core node types:

- `audio_object`
- `direct_speaker`
- `LFE`

Auxiliary core node types:

- `spectral_features`
- `agent_state`

## Identity model

LUSID uses a stable `X.Y` identity convention. `X` identifies a group and `Y` identifies the node within that group. This supports deterministic asset binding, traceability, and stable scene references across frames.

## Asset model

Audio-bearing nodes should bind explicitly to assets. Canonical naming follows node identity:

- `X.Y.wav`
- `LFE.wav`

## Time model

Frames are ordered by time. `duration` is authoritative for total scene length. The final frame timestamp does not necessarily define total duration.
