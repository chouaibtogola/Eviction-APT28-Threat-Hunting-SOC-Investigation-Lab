#  Eviction – APT28 Threat Hunting & SOC Investigation Lab

Threat hunting and SOC investigation lab focused on APT28 adversary behavior using the MITRE ATT&CK framework.

<img width="530" height="349" alt="image" src="https://github.com/user-attachments/assets/0f2ec828-4119-43f2-9795-263b308ae4df" />

Image source: https://www.crowdstrike.com/content/dam/crowdstrike/www/en-us/wp/2016/09/FancyBearBlog-1.jpg

---

#  Overview

This project documents my completion of the “Eviction” Lab, where I performed threat hunting and SOC analysis activities based on intelligence related to the APT28 threat group.

The lab focused on identifying adversary tactics, techniques, and procedures (TTPs) using the MITRE ATT&CK framework and understanding how attackers progress through different stages of the cyber kill chain.

Throughout the investigation, I analyzed:
- Persistence mechanisms  
- Execution techniques  
- Lateral movement activity  
- Discovery actions  
- Potential data exfiltration methods used by advanced threat actors  

This project demonstrates practical blue-team skills including:
- Threat hunting  
- MITRE ATT&CK analysis  
- SOC investigation workflows  
- Detection engineering concepts  
- Adversary behavior analysis  
- Incident response thinking  

---

#  Problem Statement

Sunny is a SOC analyst at E-corp, which manufactures rare earth metals for government and non-government clients. She receives a classified intelligence report that informs her that an APT group (APT28) might be trying to attack organizations similar to E-corp.

To act on this intelligence, she must use the MITRE ATT&CK Navigator to identify the TTPs used by the APT group, ensure it has not already intruded into the network, and stop it if it has.

<img width="1864" height="825" alt="image" src="https://github.com/user-attachments/assets/2ba36295-bce8-4e1c-95df-f7e971d8736d" />

We have this database of the MITRE ATT&CK framework of the APT28.

---

#  Investigation & Findings

## 1. Technique used for recon + initial access
Spearphishing link

---

## 2. Accounts compromised during resource development
Email accounts

---

## 3. User execution techniques to look out for
- Malicious file  
- Malicious link  

---

## 4. Scripting interpreters to check execution
- PowerShell  
- Windows Command Shell  

---

## 5. Registry keys to observe for persistence
Registry Run Keys (automatically executed at logon)

---

## 6. System binary used for proxy execution
rundll32

---

## 7. Technique related to tcpdump on host
Network sniffing

---

## 8. Remote services for lateral movement
SMB / remote admin shares

---

## 9. Likely information repository target
SharePoint

---

## 10. Proxy types used for exfiltration
- External proxy  
- Multi-hop proxy  

---

#  Conclusion

This lab helped simulate real-world SOC investigation scenarios by analyzing APT28 behavior using the MITRE ATT&CK framework and understanding attacker movement across the environment.

---
