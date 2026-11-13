# W2--PM2-FINAL-REPORT-NETWORKWALKS
REPORT FINAL NETWORKWALKS

PENETRATION TESTING REPORT
FOOTPRINTING & NETWORK SCANNING PHASES
W2-PM-FINAL | CYBERSECURITY |  NETWORKWALKS

| PENTESTER (CYBERSECURITY PROFESSIONAL) | RECALDO CHAPFUWA |
| :--- | ---: |
| PROGRAM/BATCH | B084-NETWORKWALKS |
| MODULES COMPLETED | W1 -PM1 KALI TOOLS  W2 -PM2-ZENMAP SCANNING W2 -PM2 FOOTPRING WITH THEHARVESTER|
| CLIENT/TARGET | 1)MICROSOFT.COM BY THEHARVESTER 2) MY LOCAL LAN NETWORK |
| PERMMISSION SECURED FROM CLIENT | YES |
| PHASES COVERED |1) RECONNAISSAINCE AND FOOTPRINTING 2) ZENMAP SCANNING |

1. Liability Disclaimer
I have performed these activities only on the systems & devices where I had secured written permission or the devices/systems that I own myself. All these materials are for education and research purpose only. Do not use anything from here to break the law. The instructor, the authors and Networkwalks are not responsible for what you do with this knowledge. Every action you take is your own responsibility. Misuse can lead to criminal charges, heavy fines, loss of your job and a permanent record. In most countries unauthorised access is a crime even when nothing is damaged.

2. Introduction
The project covers footprinting and reconnaissance with theHarvester finding information on the domain microsoft.com provided with limits and sources for the company.All commands were run on my Kali Linux connected to nat networks via networkwalks.It also covers Zenmap scanning to scan or find out details of my target but using my LAN network on my pc.I installed Nmap for Zenmap GUI used for scanning.I shall provide the evidence collected doing the procedure.


3. Tools Used
The table below lists each tool used in this report and its purpose.

| TOOL   | PURPOSE  |
|:--- | ---: |
| KALI LINUX ON WINDOWS | Operating systems used for reconnaissance activities or footprinting and finding theHarvester preinstalled on KALI LINUX |
| theHARVESTER | used for finding email addresses and ip configurations |
| Zenmap | Scan the local subnet to find live hosts, IPs and MAC addresses and topology of network|
| COMMAND PROMPT | Local IP and MAC address identification and also nmap information|

4. Activities Performed
4.1 Footprinting & Reconnaissance
I collected information on email address and ip configuration of the domain microsoft.com using theHarvester.

4.2 Network Scanning with Zenmap
For the second activity, I used Zenmap to perform network discovery on my local network. The practical required me to identify my local IP address and subnet, discover live hosts, identify their IP and MAC addresses, and generate a network topology.
I first used the Windows ipconfig command to identify my local IP address and LAN subnet. I then entered the subnet into Zenmap and selected Ping Scan to identify active hosts.I collected 19 live hosts on my network and 19 mac addresses.I took a screenshot of my topology and legend which shows the meaning of the topology.
After completing the scan, I opened the Topology section in Zenmap, enabled the legend and saved the network topology in PDF format as required by the practical task.
Note: The actual subnet, number of hosts and addresses should be replaced with the results from my own network when submitting the report.

5. Risk Analysis / Impact
Based on the information collected during the footprinting and network scanning activities, I identified the following potential risks.

Risk Category
Specific Threat / Scenario
Likelihood
Impact Level
Operational & Security Impact
Operational Security (OPSEC)
Source IP Attribution: Querying target DNS servers or APIs directly without routing traffic through a proxy or VPN.
High
Medium
Target Blue Teams or Threat Intelligence feeds can identify the tester's real IP address, revealing the source of the assessment and compromising stealth.
Active Scanning Creep
Unintended Active Probing: Enabling active modules (e.g., -c for DNS brute-forcing, -n for reverse DNS, or -v for virtual host verification).
Medium
High
Shifts the engagement from passive OSINT to active scanning. This triggers IDS/IPS alerts, fills target logs, and may violate Rules of Engagement (RoE) if active scanning isn't authorized yet.
Legal & Compliance
Scope Violation / Third-Party Harm: Harvesting data belonging to third-party vendors, shared hosting providers, or out-of-scope subsidiaries.
Medium
High
Collecting or interacting with out-of-scope assets violates legal authorization (e.g., CFAA, GDPR) and exposes the tester/firm to legal liability.
Data Integrity
False Positives & Stale Data: Relying on outdated cached records from search engines or DNS aggregators.
High
Low
Wastes penetration testing hours investigating decommissioned subdomains, parked domains, or incorrect employee email formats.
API & Rate Limiting
Account Suspension & IP Bans: Aggressive querying of public search engines (Google, Bing) or exhausting paid API quotas (Shodan, Hunter).
High
Low
Results in temporary CAPTCHA blocks, IP blacklisting by search providers, or depletion of expensive enterprise API credits needed for later phases.

6. Recommendations
Based on the observations from these activities, I recommend the following security improvements.

Mitigation Strategy
Route traffic through a dedicated VPN, Tor, or a cloud-based jump host/VPS assigned specifically to the engagement.
Stick strictly to passive data sources (e.g., -b bing,crtsh,duckduckgo) during initial recon; verify RoE before enabling active flags.
Strictly filter outputs against the authorized domain/IP scope list before conducting any follow-up enumeration.
Cross-reference harvested assets with live DNS resolution and WHOIS records before moving to vulnerability scanning.
Use the -S (start result) and -l (limit) flags to throttle queries, and rotate API keys or user-agents responsibly.
Restrict file permissions (chmod 600 api-keys.yaml), use environment variables where possible, and encrypt the Linux testing drive.
Store all tool outputs inside an encrypted volume (e.g., VeraCrypt or LUKS) and securely wipe data upon engagement completion.

7. Conclusion
During Week 2 of my Cybersecurity & Ethical Hacking internship, I completed practical activities covering footprinting, reconnaissance and network scanning.
In the footprinting activity, I used six Kali Linux tools to collect information about the target domain. I used theHarvester to obtain information about api,email addresses and ip configuration of domain. I learnt that theharvester has tools for domain name,source,limit etc.
I learnt also about this:
❑ theHarvester is passive recon: it reads public sources and never touches the target.
❑ Different data sources return different results, so always try more than one.
❑ Harvested emails feed phishing campaigns; sub-domains expand the attack surface.
❑ The less an organization exposes publicly, the harder every later attack stage becomes.
❑ theHarvester comes pre-installed in Kali Linux but if you are using other OS then you can install it
In the network scanning activity, I used Zenmap to identify my local network configuration and discover active hosts. I also collected IP and MAC address information and created a network topology.
The exercises showed me that information gathering is an important part of cybersecurity. Even before attempting to exploit a system, a security professional can learn a significant amount about an environment by carefully analyzing publicly available information and network responses.
I also learned that technical findings should be documented clearly. A good cybersecurity report should explain what was performed, what was discovered, what the observation means, what risk it may create, and what can be done to reduce that risk.
Finally, I learned that reconnaissance and scanning must always be performed within an authorized scope. These activities were completed as part of the assigned educational cybersecurity lab.

8.EVIDENCE COLLECTED

<img width="947" height="247" alt="TheHarvester 1 png" src="https://github.com/user-attachments/assets/23ce6c5b-222a-456e-ab3d-68544ee23518" />
<img width="911" height="374" alt="TheHarvester 2 png" src="https://github.com/user-attachments/assets/e39d8213-5d2c-4ebe-9a24-bb65472ff392" />
<img width="946" height="396" alt="TheHarvester 3 png" src="https://github.com/user-attachments/assets/01384789-dafa-40d3-a56a-df5c121d678c" />
<img width="667" height="393" alt="TheHarvester 4 png" src="https://github.com/user-attachments/assets/d44cc5b8-e71f-4c8f-99f6-cb8d37109094" />
<img width="741" height="387" alt="TheHarvester 5 png" src="https://github.com/user-attachments/assets/135a0ef3-de89-4014-a608-4bfac2754b74" />
<img width="346" height="386" alt="TheHarvester 6 png" src="https://github.com/user-attachments/assets/ac36b073-cb13-479f-b56f-693253fb3b28" />
<img width="285" height="368" alt="TheHarvester 7 png" src="https://github.com/user-attachments/assets/a70bbb29-9f29-4e27-8f14-edd01719fa72" />
<img width="938" height="493" alt="Screenshot 2026-11-13 093012" src="https://github.com/user-attachments/assets/d9bcf1ff-4843-4f85-959e-e3ca468bba90" />
<img width="937" height="464" alt="Screenshot 2026-11-13 094138" src="https://github.com/user-attachments/assets/17bd4575-e876-47b8-aecf-fa3aa34c817e" />
<img width="937" height="464" alt="Screenshot 2026-11-13 100655" src="https://github.com/user-attachments/assets/618004f9-4b45-4120-879e-abfda3bb672c" />

👤 Author
Recaldo Chapfuwa
Cybersecurity Student B084
LinkedIn: http://linkedin.com/in/recaldo-chapfuwa-44380a223

📌 Project Information
Program Name: Cybersecurity program at Networkwalks | Week: 02 | Repository: GitHub




























 




























































 
 


