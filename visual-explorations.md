# Visual Explorations

This page collects experimental visual summaries derived from the supplementary CVE tables and research notes. The figures are exploratory: they are meant to suggest possible article figures, not to replace the curated tables.

## Evidence-to-Scenario Map

This is the cleanest candidate for the article because it explains the paper's logic without requiring the reader to inspect every CVE table.

```mermaid
flowchart TB
    A["CVE records<br/>public product vulnerabilities"] --> D["Curated maritime relevance"]
    B["Underground forum evidence<br/>attacker interest and techniques"] --> D
    C["AIS/ECDIS trigger model<br/>trusted navigation-data flows"] --> D

    D --> E["Product vulnerability<br/>persistence, access, code execution"]
    D --> F["Architectural weakness<br/>trusted external data enters bridge decisions"]
    E --> G["Dormant or prepared capability"]
    F --> H["External navigation condition"]
    G --> I["Context-dependent activation"]
    H --> I
    I --> J["Ship-level cyber-physical risk"]

    classDef evidence fill:#eef2ff,stroke:#6366f1,color:#111827;
    classDef mechanism fill:#ecfdf5,stroke:#22c55e,color:#111827;
    classDef effect fill:#fff7ed,stroke:#f97316,color:#111827;
    class A,B,C,D evidence;
    class E,F,G,H,I mechanism;
    class J effect;
```

## CVE Relevance Taxonomy

```mermaid
mindmap
  root((Maritime CVE relevance))
    Maritime native
      Direct shipboard equipment
      SATCOM and navigation systems
      Clear operational role
    Maritime adjacent
      AIS/NMEA/GNSS software
      Maritime-associated vendors
      Navigation-data processing
    Deployment-dependent infrastructure
      Firmware/update paths
      Gateways and radio infrastructure
      Relevance depends on placement
    Disconnected or corrected
      False positives
      LLM-suggested mismatches
      Boundary control for dataset quality
```

## Article-Framing Quadrant

This one is interpretive rather than empirical. It helps decide what belongs in the article body and what should remain in GitHub side material.

```mermaid
quadrantChart
    title CVE relevance framing for the short article
    x-axis Generic deployment --> Maritime-specific deployment
    y-axis Product flaw --> Cyber-physical coupling
    quadrant-1 Core article evidence
    quadrant-2 Native product exposure
    quadrant-3 Background infrastructure
    quadrant-4 Architectural trigger relevance
    "NavBox / FELCOM / Cobham": [0.78, 0.45]
    "AIS-catcher / gpsd-NMEA": [0.58, 0.72]
    "Nautel firmware update": [0.30, 0.68]
    "Moxa gateways": [0.35, 0.42]
    "Corrected false positives": [0.12, 0.15]
```

## Mermaid Count Sketches

```mermaid
pie showData
    title Curated CVEs by relevance class
    "Maritime native" : 11
    "Vendor-associated / environment-dependent" : 3
    "Maritime adjacent" : 2
    "Maritime relevant" : 2
    "Deployment-dependent infrastructure" : 1
    "Domain adjacent" : 1
    "Unclassified" : 1
```

```mermaid
pie showData
    title Curated CVEs by severity
    "High" : 9
    "Critical" : 7
    "Medium" : 4
    "Unspecified" : 1
```

## Generated SVG Charts

These SVGs are generated from `maritime-cve-research-notes.md` using a small standard-library Python script.

![Curated CVEs by relevance class](./figures/cve-relevance-class-distribution.svg)

![Curated CVEs by severity](./figures/cve-severity-distribution.svg)

![Evidence roles mentioned in CVE notes](./figures/cve-evidence-role-keywords.svg)

## Summary Tables

### Relevance Classes

| Class | Count |
| --- | --- |
| Maritime native | 11 |
| Vendor-associated / environment-dependent | 3 |
| Maritime adjacent | 2 |
| Maritime relevant | 2 |
| Deployment-dependent infrastructure | 1 |
| Domain adjacent | 1 |
| Unclassified | 1 |

### Severity

| Severity | Count |
| --- | --- |
| High | 9 |
| Critical | 7 |
| Medium | 4 |
| Unspecified | 1 |

### Evidence-Role Keywords

| Role | Count | Example CVEs |
| --- | --- | --- |
| Authentication / access | 14 | CVE-2026-2754, CVE-2018-16705, CVE-2018-16591, CVE-2018-16590 |
| Remote code execution | 7 | CVE-2025-66217, CVE-2013-2038, CVE-2025-28236, CVE-2019-9532 |
| Disclosure / reconnaissance | 2 | CVE-2019-9533, CVE-2013-6034 |
| Navigation-data input | 5 | CVE-2025-66217, CVE-2025-66216, CVE-2013-2038, CVE-2019-9534 |
| Firmware / persistence | 13 | CVE-2025-28236, CVE-2023-41086, CVE-2023-39429, CVE-2023-39222 |

## Notes

- The keyword chart is intentionally approximate. It counts whether a CVE note contains at least one keyword associated with each evidence role.
- The quadrant chart is interpretive rather than measured. It is useful for discussion and article-framing decisions, not as empirical evidence.
- The generated counts exclude the disconnected or corrected suggestions section, so the charts describe only the curated CVE notes.
