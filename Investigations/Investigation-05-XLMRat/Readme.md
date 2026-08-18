# XLMRat Lab

> **Platform:** CyberDefenders  
> **Category:** Network Forensics  
> **Difficulty:** Easy  
> **Tools:** Wireshark, CyberChef, PowerShell, VirusTotal, Python3  

---

## Overview

This investigation focused on analyzing network traffic and malware-related artifacts to reconstruct a multi-stage malware infection. The objective was to identify the initial malware delivery source, investigate the associated hosting infrastructure, analyze the malware sample and malicious scripts, identify the malware family, and determine the techniques used for stealthy execution.

---

## What I Did

During this investigation, I:

- Analyzed the provided network traffic using Wireshark to identify the initial malware download.
- Identified the URL used to download the first-stage malware: `http://45.126.209.4:222/mdm.jpg`.
- Investigated the associated IP address and identified the hosting provider as `reliableSite.net`.
- Analyzed the recovered malware executable and identified the malware family as **AsyncRAT**.
- Examined the malware's PE header and identified the compilation timestamp as `2023-10-30 15:08`.
- Analyzed and deobfuscated malicious scripts to understand the malware execution process.
- Identified the use of `C:\Windows\Microsoft.NET\Framework\v4.0.30319\RegSvcs.exe` as a LOLBin for stealthy process execution.
- Investigated the files dropped by the malicious script as part of the malware execution chain.
- Used malware intelligence techniques to correlate the identified artifacts with known malicious activity.
- Mapped the observed attacker behavior to relevant MITRE ATT&CK techniques.

---

## Skills Practiced

- Network Forensics
- PCAP Analysis
- Malware Analysis
- Script Analysis
- Threat Intelligence
- Wireshark
- CyberChef
- VirusTotal Investigation
- LOLBin Detection
- MITRE ATT&CK Mapping

---

## Key Learnings

- Learned how network traffic can be used to identify the initial delivery stage of a malware infection.
- Improved understanding of how attackers use legitimate Windows binaries such as `RegSvcs.exe` for stealthy execution.
- Gained practical experience analyzing and deobfuscating malicious scripts.
- Learned how PE metadata can provide useful information about a malware sample.
- Understood how threat intelligence can be used to identify malware families and investigate attacker infrastructure.
- Strengthened the ability to correlate network, script, and malware artifacts to reconstruct an infection chain.

---

## Reflection

This investigation provided practical experience in analyzing a malware infection from its initial network delivery through execution. By combining network traffic analysis, script investigation, PE metadata analysis, and threat intelligence, I was able to understand the different stages of the attack and identify the techniques used to execute the malware stealthily.

---

**Status:** ✅ Completed
