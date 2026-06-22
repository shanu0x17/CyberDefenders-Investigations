# Investigation 01 - JetBrains Lab

## Overview

This investigation focused on analyzing network traffic from a compromised web server using Wireshark. The objective was to identify attacker activity, extract indicators of compromise (IOCs), understand persistence mechanisms, and map observed behavior to the MITRE ATT&CK framework.

## Skills Practiced

- PCAP Analysis
- Wireshark Investigation
- IOC Identification
- Web Exploitation Analysis
- Network Forensics

## Tools Used

- Wireshark
- CyberDefenders Lab Environment

## Investigation Process

1. Examined HTTP traffic within the PCAP.
2. Identified suspicious requests targeting the web server.
3. Tracked attacker activity after initial access.
4. Analyzed communication patterns and indicators.
5. Correlated findings with attack techniques.

## Key Findings

- Identified evidence of web server compromise.
- Observed attacker activity following successful exploitation.
- Extracted multiple indicators of compromise (IOCs).
- Analyzed attacker communication behavior.
- Mapped observed activity to relevant MITRE ATT&CK techniques.

## MITRE ATT&CK Techniques Observed

- Initial Access
- Execution
- Command and Control

## Lessons Learned

- Network traffic can reveal the complete attack chain.
- PCAP analysis is valuable for incident response investigations.
- Understanding HTTP traffic patterns helps identify malicious behavior.
- Indicators of compromise are critical for detection and future monitoring.

## Reflection

This was my first CyberDefenders SOC Analyst Tier 1 investigation. The lab improved my understanding of Wireshark-based investigations and demonstrated how network evidence can be used to reconstruct attacker activity.
