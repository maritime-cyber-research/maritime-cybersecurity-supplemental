---
title: "Threat-model-driven security requirements for naval and maritime systems"
---

# Threat-model-driven security requirements for naval and maritime systems

Supplementary requirements table derived from the threat model. This table may remain outside the short article if the article focuses on evidence and scenario construction rather than requirements engineering.

## Table

| System area | Representative threat | Security requirement | Rationale |
| --- | --- | --- | --- |
| AIS/GNSS/ECDIS | Spoofing, false data injection, GPS manipulation | Cross-check sensor inputs; validate data consistency; use multiple signal sources when possible | Navigation displays should not trust a single unauthenticated external data stream. |
| VDR and logs | File forgery, deletion, remote file inclusion | Protect integrity of voyage records; verify files; restrict maintenance access | VDR data is both operationally and legally important after accidents. |
| VSAT/SATCOM | Default credentials, command injection, malicious devices | Change default credentials; enforce authentication; monitor with IDS/IPS; restrict management interfaces | SATCOM is often the bridge between external networks and onboard systems. |
| Shipboard network | DoS, brute force, weak segmentation | Segment IT/OT/crew networks; apply bandwidth limits; inspect packets and management traffic | Network separation limits propagation from user or communication networks into OT. |
| CAN/SAN/NMEA buses | False data injection, hardcoded credentials | Authenticate devices where possible; monitor anomalous messages; protect embedded credentials | Legacy maritime buses often prioritize interoperability over security. |
| Remote stakeholders | Spear phishing, spoofed e-mail, malware | Authenticate stakeholders; verify e-mail origin; apply anti-malware and least privilege | Ship owners, agents, vendors, and operators are necessary but risky trust relationships. |
| Sensors and actuators | False sensor data, malicious commands | Validate commands and sensor values against physical constraints | Cyberattacks become dangerous when digital inputs trigger physical actions. |
| Crew and physical access | Human error, tampering, onboard compromise | Training, video surveillance, physical protection of terminals and cabinets | The vessel is a moving ICS environment with both cyber and physical exposure. |

## Data

[Download CSV](./security-requirements-maritime-systems.csv)
