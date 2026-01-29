SOC Lab – Windows Log Monitoring with Splunk
Overview

This project demonstrates a SOC-style implementation of centralized Windows endpoint monitoring using Splunk Enterprise. The lab focuses on collecting, indexing, and analyzing Windows Security logs, Sysmon telemetry, and Application logs to detect suspicious authentication activity, endpoint behavior, and system errors.

The project simulates real-world SOC challenges such as audit policy enablement, permission issues, log ingestion failures, and structured troubleshooting.

Objectives

Centralize Windows endpoint logs into Splunk

Enable and validate Windows audit policies

Collect Security, Sysmon, and Application logs

Separate logs using a proper indexing strategy

Build SOC-relevant detections using SPL

Document troubleshooting and resolution steps

Log Sources

Windows Security Event Logs (authentication, account activity)

Sysmon Operational Logs (process creation, network connections, file activity)

Windows Application Logs (application and service errors)

Tools & Technologies

Splunk Enterprise (Free Trial)

Splunk Universal Forwarder

Windows Event Logging

Sysmon (Sysinternals)

SPL (Search Processing Language)

Architecture (High Level)

Windows Endpoint → Splunk Universal Forwarder → TCP 9997 → Splunk Enterprise → Detection & Analysis

Detections Implemented

Failed login / brute-force detection (Event ID 4625)

Suspicious process execution (Sysmon Event ID 1)

Network connection monitoring (Sysmon Event ID 3)

Application error monitoring (Application log Level 2)

SPL queries and proof screenshots are available in the 07-Detections/ folder.

Project Structure
01-Architecture/
02-Setup/
03-Inputs-Configuration/
04-Indexes/
05-Sysmon/
06-Log-Verification/
07-Detections/
08-Troubleshooting/
09-Report/
README.md

Proof & Validation

Screenshots of log ingestion and searches

SPL queries for each detection use case

btool validation of inputs

Troubleshooting and resolution documentation

All proof artifacts are stored in their respective folders.

Skills Demonstrated

SIEM log onboarding and validation

Windows NT security and auditing

Sysmon telemetry analysis

SPL-based detection engineering

SOC-style troubleshooting and documentation

Limitations

Single endpoint lab environment

No Active Directory domain

Alerts not automated (search-based detections only)

Future Enhancements

Convert detections into real-time alerts

Map detections to MITRE ATT&CK

Add Active Directory authentication logs

Tune Sysmon configuration to reduce noise


Author

Gourab Das

This project is intended for learning and SOC skill demonstration purposes.