# Lockdown Lab

> **Platform:** CyberDefenders  
> **Category:** Network Forensics  
> **Difficulty:** Easy  
> **Tools:** Wireshark, Volatility 3, VirusTotal

---

## Overview

This investigation focused on reconstructing a multi-stage cyber intrusion by analyzing network traffic, memory artifacts, and a recovered malware sample. The objective was to identify the attacker's reconnaissance activity, track the web shell deployment, investigate persistence mechanisms, analyze the reverse shell communication, and attribute the malware using threat intelligence.

---

## What I Did

During this investigation, I:

- Analyzed the provided PCAP file using Wireshark to identify reconnaissance and exploitation activity.
- Identified the attacker's source IP and detected the use of Nmap for HTTP service enumeration.
- Traced SMB activity to determine the network shares accessed by the attacker.
- Identified the uploaded ASPX web shell used to achieve remote code execution.
- Investigated the reverse shell connection and identified the listening port used by the attacker.
- Performed memory analysis using Volatility 3 to obtain kernel information, active processes, and network connections.
- Investigated suspicious persistence mechanisms and located the implanted executable within the Startup directory.
- Correlated running processes with active network connections to identify the malicious process responsible for outbound communication.
- Performed malware intelligence analysis using VirusTotal to identify the malware family, detect UPX packing, and determine the command-and-control (C2) domain.
- Mapped the observed attacker behavior to the MITRE ATT&CK framework.

---

## Skills Practiced

- PCAP Analysis
- Network Forensics
- Memory Forensics
- Volatility 3
- Malware Analysis
- Threat Intelligence
- VirusTotal Investigation
- Process Analysis
- Persistence Detection
- MITRE ATT&CK Mapping

---

## Key Learnings

- Learned how attackers perform reconnaissance before exploiting exposed services.
- Improved understanding of web shell deployment and reverse shell communication.
- Gained hands-on experience performing Windows memory analysis using Volatility 3.
- Learned how to identify persistence mechanisms through process and file analysis.
- Understood how threat intelligence platforms like VirusTotal help attribute malware and identify C2 infrastructure.
- Strengthened the ability to combine network, memory, and malware artifacts to reconstruct a complete attack timeline.

---

## Reflection

This investigation provided practical experience in combining multiple forensic disciplines to analyze a complete intrusion. By correlating evidence from network traffic, memory analysis, and malware intelligence, I was able to reconstruct the attack lifecycle and understand how different forensic artifacts complement each other during a real-world incident investigation.

---

**Status:** ✅ Completed
