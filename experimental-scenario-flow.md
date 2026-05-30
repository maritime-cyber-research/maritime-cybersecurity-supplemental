---
title: "Experimental Scenario Flow: Product Vulnerability Meets AIS/ECDIS Triggering"
---

# Experimental Scenario Flow: Product Vulnerability Meets AIS/ECDIS Triggering

This experimental note mirrors the compact scenario-flow table in the article and adds a Mermaid diagram for GitHub rendering. It is meant as a visual supplement, not as a separate claim of exploitability.

## Scenario Table

| Stage | Example | Weakness Type | Role |
|---|---|---|---|
| Installation | Unsigned firmware update | Product vulnerability (CVE) | Persistence |
| Triggering | AIS/ECDIS trust assumptions | Architectural weakness | Activation |
| Execution | Dormant payload | Attack path | Malicious behavior |
| Outcome | Route manipulation, false alerts | Cyber-physical consequence | Operational impact |

## Mermaid Flow

```mermaid
flowchart LR
    A["Product vulnerability<br/>Unsigned firmware update"] --> B["Persistent modification<br/>Dormant payload installed"]
    B --> C["External navigation condition<br/>AIS/ECDIS data pattern"]
    C --> D["Context-aware activation<br/>Payload changes behavior"]
    D --> E["Bridge decision path<br/>Displays, alerts, operator response"]
    E --> F["Cyber-physical consequence<br/>Route manipulation or false alerts"]

    G["CVE records"] -. evidence .-> A
    H["Architectural analysis"] -. explains .-> C
    I["Underground forum evidence"] -. motivation context .-> C

    classDef product fill:#eef6ff,stroke:#3b82f6,stroke-width:1px,color:#0f172a;
    classDef arch fill:#f0fdf4,stroke:#22c55e,stroke-width:1px,color:#0f172a;
    classDef effect fill:#fff7ed,stroke:#f97316,stroke-width:1px,color:#0f172a;
    class A,B product;
    class C,H arch;
    class D,E,F effect;
```

## Mermaid Sequence View

```mermaid
sequenceDiagram
    participant Maint as Maintenance Path
    participant Comp as Shipboard Component
    participant AIS as AIS/ECDIS Environment
    participant Bridge as Bridge Decision-Making
    participant Vessel as Vessel Behavior

    Maint->>Comp: Insecure update introduces dormant behavior
    Note over Comp: Payload remains inactive
    AIS->>Comp: Navigation-data condition appears
    Comp->>Bridge: Behavior changes display, alert, or data path
    Bridge->>Vessel: Decision or command changes vessel behavior
```

