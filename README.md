# Cyber Kill Chain - TryHackMe Writeup

## Overview

This repository contains my notes and understanding from completing the **Cyber Kill Chain** room on TryHackMe. The room is based on the Lockheed Martin Cyber Kill Chain framework and walks through each of the 7 stages attackers follow to achieve their objectives in a cyber attack. Understanding this framework is essential for SOC analysts, threat hunters, and incident responders to detect, mitigate, and prevent cyber intrusions.

---

## What is the Cyber Kill Chain?

Originally developed by Lockheed Martin in 2011, the Cyber Kill Chain maps out the phases of a cyber attack, from reconnaissance to exfiltration. Each phase represents an opportunity for defenders to detect and disrupt the adversary.

### The 7 Phases

1. **Reconnaissance**  
   - Goal: Collect information about the target.
   - Tools & Techniques:  
     - OSINT (e.g., theHarvester, Hunter.io, LinkedIn, Shodan)  
     - Email harvesting  
     - Public datasets and company websites  

2. **Weaponization**  
   - Goal: Create a malicious payload.  
   - Techniques:
     - Combine exploit + malware into deliverable
     - Office macros, infected PDFs
     - Command & Control (C2) setup
     - Use of purchased malware or custom toolkits  

3. **Delivery**  
   - Goal: Transmit the weapon to the victim.  
   - Methods:
     - Phishing emails (spearphishing)
     - USB drop attacks
     - Watering hole attacks / drive-by downloads  

4. **Exploitation**  
   - Goal: Trigger the payload to exploit a vulnerability.  
   - Examples:
     - Macro-enabled documents
     - Zero-day vulnerabilities
     - Fake login pages
     - Privilege escalation and lateral movement  

5. **Installation**  
   - Goal: Establish persistence on the victim's machine.
   - Techniques:
     - Backdoors, web shells
     - Meterpreter payloads
     - Registry run keys, startup folder
     - Service modification (T1543.003)
     - Timestomping  

6. **Command & Control (C2)**  
   - Goal: Maintain communication and control over the victim.  
   - Channels:
     - HTTP/HTTPS beaconing
     - DNS tunneling
     - Custom protocols and encryption  

7. **Actions on Objectives**  
   - Goal: Achieve the attacker's goal (data theft, disruption, etc.).  
   - Actions:
     - Credential theft
     - Data exfiltration
     - Destruction (e.g., deleting backups)
     - Internal reconnaissance  
     - Lateral movement  

---

## Key Takeaways

- Each phase provides an opportunity to **detect, disrupt, or contain** the attack.
- The Cyber Kill Chain emphasizes **early detection**, particularly during Reconnaissance and Delivery phases.
- Understanding attacker TTPs (Tactics, Techniques, and Procedures) helps defenders deploy appropriate countermeasures.

---

## Strengths & Weaknesses of the Cyber Kill Chain

### Strengths
- Structured view of the attack lifecycle
- Useful for SOC teams, blue teams, and threat hunting
- Focuses on **external attacks and malware**

### Weaknesses
- Focused primarily on perimeter-based defenses
- Less effective at detecting **insider threats**
- Needs to be complemented with models like **MITRE ATT&CK** and **Unified Kill Chain**

---


## Usage

This writeup serves as a quick reference for studying Cyber Kill Chain phases or building detection capabilities in a Blue Team/SOC environment.
