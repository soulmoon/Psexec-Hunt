# PsExec Hunt - CyberDefender CTF Lab

**Category:** Network Forensics  
**Tactics:** Execution, Defense Evasion, Discovery, Lateral Movement  
**Tool Used:** Wireshark  

---

## Scenario
An alert from the Intrusion Detection System (IDS) flagged suspicious lateral movement activity involving **PsExec**. This suggests potential unauthorized access and movement across the network.  
As a SOC Analyst, your mission is to investigate the provided **PCAP** file to trace the attacker’s activities — identifying their entry point, the machines targeted, the extent of the breach, and the critical indicators of their tactics and objectives.

---

## Questions & Answers

**Q1:** What is the IP address of the machine from which the attacker initially gained access?  
**Answer:** `10.0.0.130`
<img width="940" height="229" alt="image" src="https://github.com/user-attachments/assets/7875920d-bbb2-4d6f-b650-d81c4db97f07" />
<img width="940" height="132" alt="image" src="https://github.com/user-attachments/assets/264db465-9c26-4ac7-994f-8423659ac303" />


---

**Q2:** What is the hostname of the machine the attacker first pivoted to?  
**Answer:** `Sales-PC`
<img width="940" height="464" alt="image" src="https://github.com/user-attachments/assets/479be87a-e699-43b6-a993-404ea5b3c4e4" />

---

**Q3:** What username did the attacker use for authentication?  
**Answer:** `Ssales`
<img width="940" height="648" alt="image" src="https://github.com/user-attachments/assets/d8c58031-778c-45ae-8e7e-198aff3add4e" />

---

**Q4:** What is the name of the service executable the attacker set up on the target?  
**Answer:** `psexesvc`
<img width="940" height="608" alt="image" src="https://github.com/user-attachments/assets/7223b45b-5593-4add-afc3-a0a0d9eb2fd5" />

---

**Q5:** Which network share was used by PsExec to install the service on the target machine?  
**Answer:** `ADMIN$`
<img width="940" height="397" alt="image" src="https://github.com/user-attachments/assets/4dbc2672-283e-4cdc-939f-e89d1b6860ef" />

---

**Q6:** Which network share did PsExec use for communication between machines?  
**Answer:** `IPC$`
<img width="940" height="756" alt="image" src="https://github.com/user-attachments/assets/fa73390f-170d-49d7-920f-d048c9b322f4" />

---

**Q7:** What is the hostname of the second machine the attacker targeted for lateral movement?  
**Answer:** `Marketing-PC`
<img width="940" height="477" alt="image" src="https://github.com/user-attachments/assets/16007b85-8c8a-42d6-952d-641052d3fc01" />

---

## Learning Outcomes
- How to identify **SMB-based lateral movement** in PCAP data.  
- Using **Wireshark filters** to extract NTLMSSP authentication details.  
- Recognizing PsExec service installation patterns.  
- Mapping attacker pivot paths between machines.

---

## Repository
You can view and download this walkthrough here:  
[**GitHub Repository**](https://github.com/soulmoon/PsExec-Hunt)

---

**Author:** *soulmoon*  
**Platform:** [CyberDefenders.org](https://cyberdefenders.org)  
