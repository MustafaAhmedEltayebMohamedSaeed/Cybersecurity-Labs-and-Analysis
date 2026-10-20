# SOC Incident Analysis: Phishing Alert Triage & Escalation

## Overview
A hands-on Security Operations Center (SOC) incident investigation focused on triaging a medium-severity email alert (`A-2703`). The activity involves analyzing email headers, evaluating social engineering indicators, and identifying suspicious file attachments for malware escalation.

## Incident & Indicator Summary
* **Ticket ID / Alert:** `A-2703` | `SERVER-MAIL Phishing attempt (possible download of malware)`
* **Sender Info:** Def Communications `<76tguyhh6tgftrt7tg.su>` (IP: `114.114.114.114`)
* **Recipient Info:** `<hr@inergy.com>` (IP: `176.157.125.93`)
* **Suspicious File Attachment:** Executable file disguised as a resume (`filename="bfsvc.exe"`)
* **Known Malicious File Hash (SHA-256):** `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b`

## Analysis & Key Findings
* **Social Engineering Tactics:** The sender used generic recruitment/HR baiting, complete with grammatical errors, typos ("Ingergy"), and password protection on the attachment (`paradise10789`) to bypass automated email gateway inspection.
* **Malicious Indicators:** High-risk `.su` top-level domain, mismatched sender domain/display name, executable file payload (`.exe`) disguised as a document, and a known malicious SHA-256 hash.
* **Resolution:** Ticket escalated for endpoint investigation, hash containment/blocking, and attachment sandbox analysis.

## Concepts & Skills Demonstrated
* SOC Alert Triage & Incident Handling
* Email Header & Domain Analysis
* Indicator of Compromise (IOC) Extraction (SHA-256 Hashes, IPs, Domains)
* Phishing & Social Engineering Mitigation
