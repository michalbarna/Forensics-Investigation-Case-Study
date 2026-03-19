_This project is based on a simulated forensic investigation conducted in an academic environment._

# Digital Forensics Investigation – Ransomware Incident

## Overview
This project presents a digital forensic investigation of a ransomware attack on a Windows Server 2022 system within a corporate HR environment. 

The investigation involved analysing a forensic disk image to determine the origin, execution, and impact of the attack. Using industry-standard tools, artefacts were identified and correlated 
to reconstruct the full attack chain and assess user involvement.

---

## Objectives
- Identify the initial infection vector  
- Determine how the ransomware was executed  
- Analyse system and user activity during the attack  
- Assess the impact of the incident  
- Reconstruct a timeline of events  

---

## Tools & Technologies
- Autopsy (for artefact analysis and timeline correlation)
- FTK Imager (for forensic validation and sector-level analysis)
- Windows Event Viewer (log analysis)
- Registry Explorer (registry analysis)

---

## Key Findings
- Initial compromise occurred via a phishing email containing a malicious MediaFire link  
- User downloaded a compressed archive (`CV.rar`) containing a disguised executable (`CV.pdf.cmd`)  
- Execution of the script triggered a PowerShell command to download a ransomware payload (`temp.exe`) from a remote C2 server  
- Ransomware execution resulted in encryption of 25+ files with a custom extension (`.eBUlMeWOP`)  
- Anti-forensic activity detected, including deletion of Prefetch files and timestamp anomalies  
- 27+ artefacts were identified and correlated to reconstruct the full attack timeline  
- No evidence of malicious intent by the user; compromise resulted from social engineering

- ## Investigation Outcome
The investigation successfully reconstructed the complete infection chain, from initial phishing email to ransomware execution and system impact. 

Evidence confirmed that the attack was delivered through social engineering, with no indication of intentional malicious activity by the user. The findings highlight the importance of email 
security awareness and monitoring of PowerShell activity in enterprise environments.
