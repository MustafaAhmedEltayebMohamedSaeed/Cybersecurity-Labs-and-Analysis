# Incident Final Report: E-Commerce Data Breach & Forced Browsing Analysis

## Executive Summary
A comprehensive investigation report detailing a major security incident involving unauthorized access and exfiltration of approximately 50,000 customer Personally Identifiable Information (PII) and financial records from an e-commerce platform.

## Key Incident Details
* **Incident Date:** December 28, 2022
* **Impact:** 50,000 customer records compromised; $100,000 estimated financial impact
* **Attack Vector:** Forced Browsing / Insecure Direct Object Reference (IDOR) on web application purchase confirmation endpoints (`order_number` URL parameter manipulation)
* **Extortion Threat:** Prior $25k–$50k cryptocurrency extortion attempt following initial unauthorized data access

## Technical Findings & Log Analysis
* Web server access logs revealed a single external IP generating an abnormally high volume of sequential requests to purchase confirmation URLs.
* Lack of URL authorization checks allowed sequential enumeration and harvesting of customer data.

## Remediation & Mitigation Recommendations
* **Access Control & Authorization:** Enforce session authentication across all data endpoints and implement URL allowlisting.
* **Proactive Testing:** Establish mandatory routine web application vulnerability scanning and quarterly penetration testing.
* **Incident Response & Disclosure:** Coordinated with PR for breach disclosure and offered identity theft protection services to affected customers.

## Concepts & Skills Demonstrated
* Web Application Vulnerability Analysis (IDOR / Forced Browsing)
* Web Server Log Auditing & Forensics
* Incident Escalation & Extortion Analysis
* Executive Summary Reporting & Breach Disclosure Procedures
