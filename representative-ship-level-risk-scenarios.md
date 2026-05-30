---
title: "Representative ship-level risk scenarios derived from CVE families"
---

# Representative ship-level risk scenarios derived from CVE families

Supplementary scenario table summarizing how CVE families can be interpreted as ship-level attack paths rather than isolated product flaws.

## Table

| Scenario | Entry point | Initial weakness | Possible propagation | Operational effect |
| --- | --- | --- | --- | --- |
| Remote ship reconnaissance | NavBox, SATCOM, web portals | Missing authentication or unrestricted file access | Disclosure of internal network parameters, logs, credentials, and device status | Improved attacker knowledge before targeting ECDIS, OT, or maintenance paths. |
| SATCOM-to-OT pivot | SATCOM terminal or ship gateway | Hardcoded credentials, no authentication, weak password recovery | Access from communication equipment to monitoring or control networks | Remote foothold in shipboard infrastructure. |
| Navigation-data manipulation | AIS, GPS/GNSS, NMEA parser, ECDIS input path | Lack of authentication, parser bugs, false data injection | Malformed or spoofed data reaches navigation display or alarm logic | False collision scenarios, route changes, or degraded situational awareness. |
| Forensic evidence compromise | VDR or logging service | Remote access, file inclusion, file forgery, weak integrity protection | Deletion, replacement, or alteration of voyage records | Reduced ability to reconstruct accidents or attribute attacks. |
| Persistent infrastructure compromise | Router, transmitter, SATCOM terminal, firmware update path | Unsigned firmware, command injection, root access | Backdoor installation or traffic interception | Long-term monitoring, selective disruption, or covert manipulation. |
| Crew/stakeholder compromise | E-mail, remote maintenance, user networks | Phishing, malware, weak separation between crew and ship networks | Malware crosses from user-facing systems to operational networks | Indirect compromise of onboard IT/OT systems. |

## Data

[Download CSV](./representative-ship-level-risk-scenarios.csv)
