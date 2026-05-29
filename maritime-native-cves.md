# Maritime-native CVEs affecting navigation, SATCOM, and shipboard communication equipment

Supplementary table for vulnerabilities in equipment with a direct maritime or shipboard communication role, including NavBox, FELCOM, Cobham, and satellite terminal families.

## Table

| CVE | CVSS | Affected component | Maritime role | Weakness | Access | Potential impact |
| --- | --- | --- | --- | --- | --- | --- |
| CVE-2026-2754 | 7.5 | Navtor NavBox | ECDIS/OT data gateway | Missing authentication on HTTP API | Remote network | Disclosure of ECDIS/OT information, device identifiers, and service logs. |
| CVE-2018-16705 | 9.8 | FURUNO FELCOM 250/500 | Shipboard SATCOM terminal | Unauthenticated credential disclosure | Remote/local network | Exposure of usernames, password hashes, and SMS password. |
| CVE-2018-16591 | 9.8 | FURUNO FELCOM 250/500 | Shipboard SATCOM terminal | Unauthenticated password change | Remote/local network | Unauthorized modification of Admin, Log, Service, and SMS passwords. |
| CVE-2018-16590 | 9.8 | FURUNO FELCOM 250/500 | Shipboard SATCOM terminal | Client-side-only authentication | Remote/local network | Authentication bypass and administrative access. |
| CVE-2019-9533 | 9.8 | Cobham EXPLORER 710 | Portable SATCOM terminal | Shared root password across firmware versions | Device/network access | Administrative compromise after password recovery or reverse engineering. |
| CVE-2019-9529 | 5.5 | Cobham EXPLORER 710 | Portable SATCOM terminal | No authentication by default | Local network | Unauthenticated access to the web portal and configuration changes. |
| CVE-2019-9530 | 5.5 | Cobham EXPLORER 710 | Portable SATCOM terminal | Unrestricted web-root file access | Local network | Disclosure of files stored in the web root directory. |
| CVE-2019-9531 | 9.8 | Cobham EXPLORER 710 | Portable SATCOM terminal | Unauthenticated Telnet/AT-command access | Remote network | Execution of AT commands and shell-like access to the device. |
| CVE-2019-9532 | 7.8 | Cobham EXPLORER 710 | Portable SATCOM terminal | Cleartext password transmission | Local network | Credential interception and portal compromise. |
| CVE-2019-9534 | 7.8 | Cobham EXPLORER 710 | Portable SATCOM terminal | Unsigned firmware update | Local network | Custom firmware upload, persistence, traffic interception, or DoS. |
| CVE-2013-7180 | 7.8 v2 | Cobham SAILOR, FleetBroadBand, EXPLORER BGAN, AVIATOR | Maritime and mobile SATCOM equipment | Weak password recovery restriction | Physical/terminal access | Administrative privilege acquisition through reset-code spoofing. |
| CVE-2013-6034 | 10.0 v2 | GateHouse, Harris BGAN, Hughes, Inmarsat, Japan Radio, Thuraya terminals | Maritime/mobile satellite terminals | Hardcoded credentials | Unspecified login vector | Unauthorized login to satellite terminal firmware. |
| CVE-2013-6035 | 10.0 v2 | GateHouse, Harris BGAN, Hughes, Inmarsat, Japan Radio, Thuraya terminals | Maritime/mobile satellite terminals | No authentication on TCP port 1827 | Remote network | Arbitrary code execution through unauthenticated protocol operations. |

## Data

[Download CSV](./maritime-native-cves.csv)
