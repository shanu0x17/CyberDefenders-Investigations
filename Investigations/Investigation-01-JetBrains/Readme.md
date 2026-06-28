# JetBrains Lab

> **Platform:** CyberDefenders
> **Category:** Network Forensics
> **Difficulty:** Easy
> **Tools:** Wireshark, NetworkMiner, Brim

---

## Overview

This investigation focused on analyzing a compromised web server using a provided PCAP file. The objective was to reconstruct the attack timeline, identify how the attacker gained access, investigate post-exploitation activity, and understand the overall impact of the compromise.

---

## What I Did

During this investigation, I:

- Analyzed the provided PCAP file using Wireshark.
- Identified the attacker's IP address through HTTP traffic analysis.
- Determined the web server version and researched the associated CVE.
- Traced the attacker's actions after the initial compromise.
- Investigated the uploaded webshell and its execution timeline.
- Identified persistence mechanisms used by the attacker.
- Examined credential modifications performed during the attack.
- Investigated the attempted container escape activity.
- Correlated attacker behavior with MITRE ATT&CK tactics.

---

## Skills Practiced

- PCAP Analysis
- HTTP Traffic Analysis
- Web Exploitation Investigation
- IOC Identification
- Timeline Reconstruction
- MITRE ATT&CK Mapping

---

## Key Learnings

- How to investigate a web server compromise using only network traffic.
- How attacker activities can be reconstructed from packet captures.
- The importance of identifying Indicators of Compromise (IOCs).
- How MITRE ATT&CK helps classify attacker behavior.

---

## Reflection

This investigation improved my confidence in using Wireshark to analyze real-world attack traffic and strengthened my understanding of network forensics and incident investigation.
