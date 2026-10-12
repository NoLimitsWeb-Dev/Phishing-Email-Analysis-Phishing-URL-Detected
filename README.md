# Phishing-Email-Analysis-Phishing-URL-Detected

## Phishing Email Analysis

### Practice with SOC Alert

### 86 - SOC141 - Phishing URL Detected

---

<img width="1919" height="586" alt="image" src="https://github.com/user-attachments/assets/b1f3dbe6-d7eb-44ab-b7d3-59a91caed199" />

Here is My assigned Ticket, seating in my Investigation Channel; ready to be investigated

---

* Click Details to view more information about the Ticket.
<img width="1912" height="848" alt="image" src="https://github.com/user-attachments/assets/fee51c12-8716-456e-8a5a-900e1724dc61" />

---

* Click >> Create Ticket to Create ticket for EventID: 86
* Click the blue Continue button to create a ticket
* Click OK when the window pops up “Ticket Created” indicating my “The ticket has been created successfully.”
<img width="1896" height="813" alt="image" src="https://github.com/user-attachments/assets/9b322cde-7774-4fad-ab7e-16ad5ab20cc6" />
<img width="788" height="562" alt="image" src="https://github.com/user-attachments/assets/5a5646b4-6469-474d-9250-2d6777595454" />

---

### Play Book Opens

(Which is used to begin the guided incident response investigation for this specific SOC141 - Phishing URL Detected alert.)

<img width="1916" height="597" alt="image" src="https://github.com/user-attachments/assets/a812e8b5-5c8c-4df2-8796-4f6802a8a1d6" />

This screen highlights a critical security alert:

• Incident Name: SOC141 - Phishing URL Detected

• Incident Type: Proxy

• Created Date: 2026-10-12 09:48:53

The dashboard indicates that I am currently navigating within the Case Management section (highlighted on the left panel).

Click blue Start Playbook! button.

---

<img width="999" height="366" alt="image" src="https://github.com/user-attachments/assets/a9f1ab2f-ebd3-4040-adbd-3c1cc7780dbe" />

### Collection Data

**Source Address:**            172.16.17.49
**Destination Address:**       91.189.114.8
**User-Agent:**                Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.88 Safari/537.36

* Click **Next**
---

<img width="973" height="393" alt="image" src="https://github.com/user-attachments/assets/c9c3bac2-889d-42cd-beef-397afd158763" />

* Click Log Management
* Click Basic
* Type in One of the IoC”s eg. **Source IP Address:** 172.16.17.49 or **Destination Address:** 91.189.114.8

<img width="1905" height="867" alt="image" src="https://github.com/user-attachments/assets/a2a3d61d-4d07-4631-8dca-a30794266456" />

<img width="1913" height="711" alt="image" src="https://github.com/user-attachments/assets/d9cb57c1-4266-4e56-8e97-613c6e9d591d" />

--- 

* Select **Malicious**

<img width="965" height="580" alt="image" src="https://github.com/user-attachments/assets/098baabb-697a-44e2-8cff-4c0a471ba1f5" />

<img width="1905" height="969" alt="image" src="https://github.com/user-attachments/assets/9290120f-8376-46f3-b701-380242b05c01" />

The image shows a VirusTotal analysis report for a highly malicious URL ```http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io``` that is actively flagged as a phishing and malware threat.

### Analysis Overview

• Target Entity: The analyzed URL is http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io.

• Community Score: 11 out of 93 security vendors have flag it as malicious. This is a very high detection rate for a URL, confirming that the link is dangerous.

• Core Threat Categories: The vendors explicitly categorize this URL as Phishing, Malicious, and Malware.

### Key Detection Breakdowns

Major cyber security vendors have reached a clear consensus regarding this link:

• Phishing: Flagged by industry leaders including Kaspersky, BitDefender, Fortinet, Sophos, alphaMountain.ai, CyRadar, G-Data, and LevelBlue.

• Malware & Malicious: Flagged as a direct malware distribution threat or malicious asset by VIPRE, Webroot, and Lionic.

• Suspicious: Flagged for suspicious behavior by ESET and Gridinsoft.


### Threat Context & Risks

• Compromised Infrastructure: The domain path utilizes a WordPress directory (/wp-content/plugins/akismet/). This strongly indicates that a legitimate website (mogagrocol.ru) was hacked. Attackers are hosting phishing landing pages or scripts inside hidden folders.

• Targeted Phishing Parameter: The URL ends with ?email=ellie@letsdefend.io. This structure is typically used in credential harvesting setups. It pre-fills a targeted victim's email address onto a fake login screen to make the phishing page look more convincing.

---

<img width="946" height="590" alt="image" src="https://github.com/user-attachments/assets/05eeb9e7-cf94-4035-a71d-aa7ba3df8503" />

* Click **Accessed**

**Destination Address Filter:**
<img width="1917" height="637" alt="image" src="https://github.com/user-attachments/assets/68e324b3-1b90-465f-b0a1-b78538898943" />

**Requested Url:** http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io
<img width="1899" height="653" alt="image" src="https://github.com/user-attachments/assets/8c97aa33-9082-4544-87ff-1e9e06134463" />

**Domain**
<img width="1912" height="634" alt="image" src="https://github.com/user-attachments/assets/26c265ac-4f74-4eea-b5dd-6796ee806569" />

### Accessed Device Details:

* When was it accessed:                  2021-03-22 18:23:54
* What is the source address:            172.16.17.49
* What is the destination address:       91.189.114.8
* Which user tried to access:            ellie (Hostname: EmilyComp)
* What is User Agent:                    Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.88 Safari/537.36                   
* Is the request blocked:                Allowed

---

