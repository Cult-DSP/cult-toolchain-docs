# Validation and Reporting Flow

```mermaid
flowchart TB
    RUN[Transcoding run] --> V1[Deterministic ordering]
    RUN --> V2[Deterministic ID assignment]
    RUN --> V3[Atomic output behavior]
    RUN --> V4[Stable report generation]

    RUN --> P1[ADM parity validation]
    P1 --> P2[Compare C++ output to Python oracle]

    RUN --> T1[Structural invariant tests]
    RUN --> T2[Profile-specific tests]
    RUN --> T3[Failure-mode tests]
    RUN --> T4[MPEG-H fixture tests]

    RUN --> R1[Warnings / errors]
    RUN --> R2[Summary metadata]
    RUN --> R3[lossLedger[]]
    RUN --> R4[Status]

    R1 --> REPORT[report.json]
    R2 --> REPORT
    R3 --> REPORT
    R4 --> REPORT
```
