# Ship cyber-physical attack surface considered in this paper

Supplementary version of the attack-surface table used to describe the ship as a cyber-physical environment rather than as a set of isolated devices.

## Table

| Domain | Typical assets | Representative data flows | Security relevance |
| --- | --- | --- | --- |
| Navigation and onboard IT | AIS, ECDIS, GPS/GNSS, IBS, VDR | Position, velocity, route, chart, alarm, voyage-recording data | Directly affects situational awareness, collision avoidance, and forensic evidence. |
| Onboard OT and control | Propulsion, engine monitoring, ballast, cargo, power management, PLC/RTU devices | Commands, sensor readings, alarms, actuator states | Creates cyber-physical consequences when manipulated or made unavailable. |
| Ship-shore communication | VSAT, SATCOM terminals, radio links, gateways, cellular routers | Remote access, maintenance, monitoring, e-mail, telemetry | Often bridges external networks to onboard IT/OT systems. |
| Port and shore-side services | Port MIS, VTS, customs systems, shipping management services | Port calls, cargo information, route plans, ship identity, operational reports | Compromise may affect logistics, reporting, routing, and trust relationships. |
| Stakeholders and third parties | Ship owner, operator, agent, equipment vendor, maintenance provider, crew/passengers | Remote monitoring, vendor support, operational coordination, user traffic | Expands the trust boundary beyond the vessel itself. |

## Data

[Download CSV](./ship-cyber-physical-attack-surface.csv)
