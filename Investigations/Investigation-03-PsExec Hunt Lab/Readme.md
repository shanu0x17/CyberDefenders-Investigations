# PsExec Hunt Lab

> **Platform:** CyberDefenders  
> **Category:** Network Forensics  
> **Difficulty:** Easy  
> **Tools:** Wireshark  

---

## Overview

This investigation focused on analyzing SMB network traffic from a provided PCAP file to identify attacker lateral movement using PsExec. The objective was to trace the attacker's movement across compromised systems, investigate authentication activity, identify administrative shares used during the attack, and reconstruct the attack path within the network.

---

## What I Did

During this investigation, I:

- Analyzed the provided PCAP file using Wireshark.
- Identified the initial compromised machine involved in the attack.
- Traced the attacker's first lateral movement to another host.
- Investigated SMB authentication traffic to identify the account used by the attacker.
- Examined PsExec service creation on the compromised machine.
- Identified the administrative network shares used during the attack.
- Tracked the communication between compromised systems through SMB traffic.
- Reconstructed the attacker's movement across multiple hosts within the network.
- Correlated the observed attacker behavior with the MITRE ATT&CK framework.

---

## Skills Practiced

- PCAP Analysis
- SMB Traffic Analysis
- Wireshark Investigation
- Lateral Movement Detection
- PsExec Investigation
- Credential Analysis
- MITRE ATT&CK Mapping

---

## Key Learnings

- Learned how PsExec is commonly used for lateral movement after an initial compromise.
- Improved the ability to analyze SMB traffic and administrative shares.
- Understood how service creation events can indicate remote execution.
- Gained practical experience reconstructing attacker movement between multiple systems.
- Strengthened network forensic investigation skills using packet captures.

---

## Reflection

This investigation enhanced my understanding of SMB-based lateral movement and demonstrated how packet analysis can be used to identify compromised systems, authentication activity, and attacker movement throughout a network.

---

**Status:** ✅ Completed
