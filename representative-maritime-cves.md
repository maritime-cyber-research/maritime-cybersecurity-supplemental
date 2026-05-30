---
title: "Examples of CVEs relevant to naval and maritime cyber-physical systems"
---

# Examples of CVEs relevant to naval and maritime cyber-physical systems

Supplementary CVE inventory used as representative evidence for product-level weaknesses that can become maritime-relevant in cyber-physical attack paths.

## Table

| CVE | Affected component | Maritime relevance | Weakness class | Attacker position | Potential impact | Why interesting |
| --- | --- | --- | --- | --- | --- | --- |
| CVE-2025-66216 | AIS-catcher < 0.64 | AIS receiver / AIS monitoring software | Heap buffer overflow | Ability to supply crafted AIS data | Denial of service and possible remote code execution | Direct AIS message parsing exposure. |
| CVE-2025-66217 | AIS-catcher < 0.64 | AIS receiver with MQTT integration | Integer underflow; heap overflow | Ability to send MQTT messages | Denial of service; memory corruption; possible RCE | Auxiliary MQTT interface expands attack surface. |
| CVE-2013-2038 | gpsd before 3.9 | GPS/NMEA0183 parsing | Malformed NMEA0183 handling | Ability to supply crafted GPS/NMEA data | Daemon crash and possible arbitrary code execution | Failure in navigation-data parsing. |
| CVE-2025-67268 | gpsd NMEA2000 driver | NMEA2000/GNSS data processing | Heap out-of-bounds write | Ability to supply crafted NMEA2000 packets | Memory corruption, denial of service, possible code execution | GNSS message parsing vulnerability. |
| CVE-2014-2940 | Cobham SAILOR 900/6000 satellite terminals | SATCOM terminal | Hardcoded admin credentials | Physical or terminal access | Administrative control of terminal | Hardcoded credentials in SATCOM infrastructure. |
| CVE-2014-2941 | Cobham SAILOR 6000 satellite terminals | SATCOM maintenance interface | Hardcoded Tbus2 credentials | Physical or terminal access to Tbus2 interface | Unauthorized access to terminal functions | Exposure of SATCOM maintenance interface. |
| CVE-2013-6034 | Multiple satellite terminals | SATCOM equipment | Hardcoded credentials | Network access to login interface | Unauthorized login access | Repeated credential weaknesses across SATCOM vendors. |
| CVE-2014-2942 | Cobham Aviator 700D/700E satellite terminals | SATCOM infrastructure | Improper PIN-code algorithm | Physical or terminal access | Privileged terminal session | Predictable superuser authentication mechanism. |
| CVE-2016-9361 | Moxa NPort serial device servers | Serial-to-IP gateway infrastructure | Authentication brute-force weakness | Ability to send repeated authentication attempts | Unauthorized administrative access via brute force | Exposure path into legacy OT infrastructure. |
| CVE-2024-9140 | Moxa routers and network security appliances | Connectivity infrastructure | OS command injection | Network access to vulnerable interface | Arbitrary code execution and device compromise | Compromise of connectivity infrastructure. |
| CVE-2025-0676 | Moxa routers and security appliances | Connectivity infrastructure | Command injection | Authenticated console access | Privilege escalation to root | Root escalation from authenticated maintenance access. |
| CVE-2025-28236 | Nautel VX Series transmitters | Radio/transmitter infrastructure | Insecure firmware update | Ability to supply crafted update package | Remote code execution during upgrade | Persistent compromise via firmware update. |

## Data

[Download CSV](./representative-maritime-cves.csv)
