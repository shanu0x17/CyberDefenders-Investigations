# XLMRat Lab — Network Forensics Investigation

**Analyst:** Shantanu Gayke  
**Platform:** CyberDefenders  
**Category:** Network Forensics  
**Difficulty:** Easy  
**Tools:** Wireshark, CyberChef, PowerShell, VirusTotal, Python3  
**Focus:** Malware Delivery, Script Analysis, Stealth Execution

---

## 1. Objective

The objective of this investigation was to analyze network traffic and malware-related artifacts to identify the malware delivery process, analyze malicious scripts, and determine the techniques used by the attacker for stealthy execution.

The investigation focused on identifying:

- The URL used to download the first malware stage
- The hosting provider associated with the IP address
- The malware family and executable characteristics
- The malware compilation timestamp
- The LOLBin used for stealthy execution
- Files dropped by the malicious script

---

## 2. Scenario

A SOC investigation identified suspicious network activity associated with the delivery and execution of malware.

The investigation involved analyzing captured network traffic, examining malicious scripts, and investigating the recovered malware sample to reconstruct the attack chain.

The primary objective was to determine how the malware was delivered, identify the malware family, and understand the techniques used to execute the payload stealthily.

---

## 3. Investigation Performed

### Step 1 — Identified the Initial Malware Download

Network traffic was analyzed using **Wireshark** to identify the request responsible for downloading the first-stage malware.

The payload was downloaded from:

`http://45.126.209.4:222/mdm.jpg`

The `.jpg` extension was used for the downloaded file, but the investigation identified it as part of the malware delivery process.

---

### Step 2 — Investigated the Hosting Infrastructure

The IP address associated with the malware download was investigated to identify the hosting provider.

**Hosting Provider:**

`reliableSite.net`

This provided additional information about the infrastructure used to host the malicious payload.

---

### Step 3 — Identified the Malware Family

The malicious executable was analyzed and correlated with malware intelligence.

The sample was identified as:

**AsyncRAT**

The SHA256 hash of the malware executable was also examined as part of the investigation.

---

### Step 4 — Analyzed PE Metadata

The PE header of the malware executable was examined to identify its compilation timestamp.

**Compilation Timestamp:**

`2023-10-30 15:08`

This timestamp provided additional context about the analyzed malware sample.

---

### Step 5 — Analyzed the Malicious Script

The malicious scripts were examined and deobfuscated to understand the execution process.

The investigation identified the use of a legitimate Windows executable as a **LOLBin** for stealthy process execution.

**LOLBin:**

`C:\Windows\Microsoft.NET\Framework\v4.0.30319\RegSvcs.exe`

The use of `RegSvcs.exe` allowed the attacker to leverage a legitimate Windows component during execution.

---

### Step 6 — Identified Dropped Files

The malicious script was analyzed to identify files dropped during execution.

These files were treated as forensic artifacts that could provide additional information about the malware execution chain.

---

## 4. Key Findings

| # | Finding | Result |
|---|---|---|
| 1 | Initial Malware Download | `http://45.126.209.4:222/mdm.jpg` |
| 2 | Hosting Provider | `reliableSite.net` |
| 3 | Malware Family | **AsyncRAT** |
| 4 | PE Compilation Timestamp | `2023-10-30 15:08` |
| 5 | LOLBin Used | `RegSvcs.exe` |
| 6 | Execution Technique | Stealthy process execution |
| 7 | Primary Evidence | Network traffic, malicious scripts, malware sample |

---

## 5. MITRE ATT&CK Mapping

| Technique | Description |
|---|---|
| **T1105 – Ingress Tool Transfer** | The malware was downloaded from remote infrastructure. |
| **T1218.009 – Regsvcs/Regasm** | The legitimate `RegSvcs.exe` executable was leveraged for execution. |
| **T1027 – Obfuscated Files or Information** | Malicious scripts required analysis/deobfuscation. |

---

## 6. Indicators of Compromise (IOCs)

### IP Address

`45.126.209.4`

### URL

`http://45.126.209.4:222/mdm.jpg`

### Hosting Provider

`reliableSite.net`

### Malware Family

`AsyncRAT`

### LOLBin

`C:\Windows\Microsoft.NET\Framework\v4.0.30319\RegSvcs.exe`

### Compilation Timestamp

`2023-10-30 15:08`

---

## 7. Executive Summary

The investigation identified an **AsyncRAT malware delivery chain** involving a payload downloaded from `45.126.209.4` over port `222`.

Further investigation identified the associated hosting provider as `reliableSite.net` and confirmed the malware family as **AsyncRAT**.

Analysis of the malicious scripts revealed the use of the legitimate Windows **RegSvcs.exe** binary for stealthy process execution. PE metadata analysis and malware investigation provided additional context about the recovered sample.

The investigation demonstrated how network traffic analysis, malware analysis, script analysis, and threat intelligence can be combined to reconstruct a malware infection chain and extract relevant indicators of compromise.

---

## 8. Recommendations

- Block identified malicious IP addresses and URLs at network security controls.
- Monitor outbound connections to unusual ports.
- Detect suspicious execution of LOLBins such as `RegSvcs.exe`.
- Monitor abnormal use of Microsoft .NET utilities.
- Perform threat-intelligence checks on suspicious files and hashes.
- Monitor systems for unexpected files dropped by malicious scripts.
- Investigate suspicious PowerShell and scripting activity associated with unusual network connections.

---

## 9. Investigation Status

**XLMRat Lab — Completed ✔️**

**Skills Demonstrated:**

`Network Forensics` → `Malware Analysis` → `Script Analysis` → `Threat Intelligence` → `LOLBin Detection` → `IOC Extraction`
