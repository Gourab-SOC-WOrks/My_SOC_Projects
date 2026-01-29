🛡️ SOC Project 2 – Kali Linux Log Ingestion into Splunk

## Project Overview

This project demonstrates centralized log monitoring by ingesting Linux system logs from a **Kali Linux VM** into **Splunk Enterprise running on Windows**. The goal is to showcase **log ingestion, visibility, and SOC-style validation**, not advanced threat detection.

---

## Objective

* Configure Splunk Universal Forwarder on Kali Linux
* Enable Linux logging using rsyslog
* Forward logs to Splunk Enterprise (Windows)
* Verify successful ingestion using SPL queries
* Document evidence in a SOC-friendly structure

---

## Lab Environment

### SOC Server

* OS: Windows 10 / 11
* SIEM: Splunk Enterprise
* Role: Indexer & Search Head

### Log Source

* OS: Kali Linux (VMware / VirtualBox)
* Log Forwarder: Splunk Universal Forwarder (Linux)
* Logging Service: rsyslog

### Network

* NAT / Bridged (Lab setup)

---

## Log Flow Architecture

Kali Linux Logs
→ journald / rsyslog
→ Splunk Universal Forwarder
→ TCP 9997
→ Splunk Enterprise (Windows)
→ Index: `linux`

---

## Logs Collected

* `/var/log/auth.log` – Authentication & sudo activity
* `/var/log/syslog` – System events
* `/var/log/kern.log` – Kernel messages

> Note: These logs appeared after installing and enabling **rsyslog** on Kali Linux.

---

## Index Used

* **Index Name:** `linux`

---

## SPL Queries Used for Validation

* `index=linux`
* `index=linux | stats count`
* `index=linux | timechart count`

These queries confirm active log ingestion, event volume, and time-based continuity.

---

## Issues Faced & Fixes

* **No logs found in /var/log/** → rsyslog not installed

  * ✔ Installed and enabled rsyslog
* **Logs not appearing in Splunk** → Logging source inactive

  * ✔ Restarted rsyslog and Splunk Forwarder
* **Confusion between journald and syslog**

  * ✔ Learned journald stores logs in binary; rsyslog writes readable log files

---

## Key Learnings

* Linux logging fundamentals (journald vs rsyslog)
* Splunk Universal Forwarder configuration on Linux
* Index creation and validation in Splunk
* SOC-style evidence collection and documentation

---

## Project Status

✅ Logs successfully ingested
✅ Verified using SPL
✅ SOC interview–ready lab

---

**End of README**
