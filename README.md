# Eviction-APT28-Threat-Hunting-SOC-Investigation-Lab

Threat hunting and SOC investigation lab focused on APT28 adversary behavior using the MITRE ATT&CK framework.

<img width="530" height="349" alt="image" src="https://github.com/user-attachments/assets/0f2ec828-4119-43f2-9795-263b308ae4df" />

image source: https://www.crowdstrike.com/content/dam/crowdstrike/www/en-us/wp/2016/09/FancyBearBlog-1.jpg

---

# Overview

This project documents my completion of the “Eviction” Lab, where I performed threat hunting and SOC analysis activities based on intelligence related to the APT28 threat group.

The lab focused on identifying adversary tactics, techniques, and procedures (TTPs) using the MITRE ATT&CK framework and understanding how attackers progress through different stages of the cyber kill chain.

Throughout the investigation, I analyzed persistence mechanisms, execution techniques, lateral movement activity, discovery actions, and potential data exfiltration methods used by advanced threat actors.

This project demonstrates practical blue-team skills including:

Threat hunting  
MITRE ATT&CK analysis  
SOC investigation workflows  
Detection engineering concepts  
Adversary behavior analysis  
Incident response thinking  

---

# We have been given a problem which is:

Sunny is a SOC analyst at E-corp, which manufactures rare earth metals for government and non-government clients. She receives a classified intelligence report that informs her that an APT group (APT28) might be trying to attack organizations similar to E-corp. To act on this intelligence, she must use the MITRE ATT&CK Navigator to identify the TTPs used by the APT group, to ensure it has not already intruded into the network, and to stop it if it has.

<img width="1864" height="825" alt="image" src="https://github.com/user-attachments/assets/2ba36295-bce8-4e1c-95df-f7e971d8736d" />

we have this database of the MITRE ATT&CK framework of the APT28

---

# 1) What is a technique used by the APT to both perform recon and gain initial access?

From the framework, we see that they use the spearphishing link

---

# 2) Sunny identified that the APT might have moved forward from the recon phase. Which accounts might the APT compromise while developing resources?

Here the APT group will likely compromise the email accounts

---

# 3) E-corp has found that the APT might have gained initial access using social engineering to make the user execute code for the threat actor. Sunny wants to identify if the APT was also successful in execution. What two techniques of user execution should Sunny look out for?

for this if we look at user execution, it will be best to look out for the malicious file and malicious link

---

# 4) If the above technique was successful, which scripting interpreters should Sunny search for to identify successful execution?

it is best to check the powershell and windows command shell

---

# 5) While looking at the scripting interpreters identified in Q4, Sunny found some obfuscated scripts that changed the registry. Assuming these changes are for maintaining persistence, which registry keys should Sunny observe to track these changes?

Best to use registry run keys. which are set to run automatically at logon

---

# 6) Sunny identified that the APT executes system binaries to evade defences. Which system binary's execution should Sunny scrutinize for proxy execution?

here it is the rundll32

---

# 7) Sunny identified tcpdump on one of the compromised hosts. Assuming this was placed there by the threat actor, which technique might the APT be using here for discovery?

from the framework, the best fitted option is network sniffing

---

# 8) It looks like the APT achieved lateral movement by exploiting remote services. Which remote services should Sunny observe to identify APT activity traces?

we know that smb/remote admin shares is the right option since it allows admin to remotely control hosts on internal network

---

# 9) It looked like the primary goal of the APT was to steal intellectual property from E-corp's information repositories. Which information repository can be the likely target of the APT?

sharepoint since it is used by organizations to share documents and informations

---

# 10) Although the APT had collected the data, it could not connect to the C2 for data exfiltration. To thwart any attempts to do that, what types of proxy might the APT use?

if the attacker is witty they will use the : external proxy or multi-hop proxy

---

# Now we are done
