# 🛡️ Incident Handler’s Journal

### Entry 1 – Ransomware Incident
 Incident handler's journal
Date: 
2025-03-11
	Description
	A ransomware attack affected a healthcare clinic, encrypting critical patient records and disrupting operations. The attack originated from a phishing email containing a malicious attachment.
	Tool(s) used
	No specific tools mentioned, but forensic tools, email security filters, and anti-malware software could be useful.
	The 5 W's 
	The 5 W's of an incident.
* Who caused the incident?
A cybercriminal group targeting healthcare and transportation industries.
* What happened?
Employees received a phishing email with a malicious attachment. The ransomware encrypted files and displayed a ransom note.
* When did the incident occur?
The attack occurred on Tuesday morning at 9:00 a.m.
* Where did the incident happen?
The attack targeted a small U.S. healthcare clinic.
* Why did the incident happen?
Employees unknowingly opened a phishing email, which deployed malware to encrypt files.
	Additional notes
	Employees should receive cybersecurity awareness training to avoid phishing emails.
The company should implement email filtering, endpoint protection, and frequent data backups.
Incident response plans (IRPs) should be in place to minimize downtime and future attacks.

### Entry 2 – SQL Injection Attack
Date: 2025-03-18   
Description:  
An attempted SQL injection attack was discovered on the hospital’s web portal. The system logs showed multiple failed login attempts followed by SQL-like input in the search field. This entry shows detection and containment steps of the NIST incident lifecycle.  

Tool(s) used:  
Wireshark was used to analyze incoming traffic. Suricata IDS flagged suspicious inputs.  

The 5 W’s:  
* Who caused the incident?  
A malicious actor attempting to exploit input validation vulnerabilities.  

* What happened?  
The attacker injected SQL code into a public search form to extract data.  

* When did it occur?  
The activity occurred over several hours late in the evening.  

* Where did it happen?  
On the hospital's online appointment portal.  

* Why did it happen?  
The attacker was likely attempting to steal patient information through database injection.  

Additional Notes:  
The input field was not properly sanitized. Developers applied input validation and parameterized queries to resolve the issue. Logs were forwarded to the SOC.


Reflections/Notes: This incident highlighted the importance of employee security awareness training. Many ransomware attacks start from phishing emails, so educating staff on how to recognize malicious emails is crucial.

### Entry 3 – Splunk Log Analysis
Date: 2025-03-22   
Description:  
Used Splunk to perform log analysis and detect brute-force login attempts on the internal HR system. This helped in understanding log correlation and the detection phase of NIST IR Lifecycle.  

Tool(s) used:  
Splunk  
* Loaded log data from the firewall and authentication server  
* Used search queries to identify repeated failed login attempts from the same IP  
* Created an alert to notify when threshold is crossed  

Additional Notes:  
Splunk made it easy to visualize and analyze large log datasets. Learned how to build dashboards and use fields to filter logs effectively.

### Entry 4 – VirusTotal Malware Scan
Date: 2025-03-25   
Description:  
Investigated a suspicious file by uploading its hash to VirusTotal. This helped in analyzing malware behavior and supported detection and analysis.  

Tool(s) used:  
VirusTotal  
* Uploaded SHA256 hash of suspicious file  
* Reviewed reports from 50+ antivirus engines  
* File was flagged by multiple engines as a trojan  

Additional Notes:  
VirusTotal is fast and provides insights from many security vendors. This helped in quick validation of a suspicious file during an investigation.

Reflections/Notes:

**Were there any specific activities that were challenging for you?**  
Yes, analyzing packet data with Wireshark was hard at first because of all the network traffic. But after watching some tutorials, it made more sense.  

**Has your understanding of incident detection and response changed since taking this course?**  
Yes. Before, I didn’t understand how tools like Splunk or Suricata were used. Now I know how to detect attacks and analyze logs.  

**Was there a specific tool or concept that you enjoyed the most? Why?**  
I enjoyed using Splunk the most. It made me feel like a real analyst, and I liked how easy it was to find suspicious patterns in logs.
