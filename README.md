Security Alert Monitoring & Incident Response Report. 


Task Summary
This assessment involved monitoring and analyzing a log of events. The main objective was to monitor security alerts, analyze potential threats and simulate incident response. Splunk was the SIEM tool utilized for task. It was used to identify suspicious activities such as failed logins, unusual IP addresses, or malware alerts. Proper mitigation measures were also recommended as a form of remediation.

Procedure
•	The SIEM tool (Security Information and Event Management) used for this task was Splunk Free Trial. The Demo session provided a platform for monitoring incoming logs, analyzing potential threats and simulating incident response.


•	The log record that was analyzed was a sample data provided and it contained simulated event logs with event timestamps, network connection logs showing IP addresses, authentication logs including successful and failed login attempts and malware detection alerts.


•	Logs captured were systematically were analyzed and corrective measures that would help in keeping organizations safe from cyberattacks by detecting suspicious activities early and responding quickly.
 


IDENTIFIED VULNERABILITIES
1.	Failed Login Attempts: This panel monitors and displays multiple failed user authentication attempts. A high rate of failed login attempt can indicate a brute-force or credential stuffing attack in progress, where the attacker is systematically trying to guess user passwords. Investigating these events is crucial to preventing unauthorized access and potential account compromise.

   
Severity Level: Medium


Reason: This indicates suspicious activity but no confirmed breach. It is often a precursor to more serious attacks like credential stuffing or brute force attacks. The severity can escalate to HIGH if the attempts are targeted at privileged accounts (e.g., admin, root) or if they are followed by a successful login.


2.	MALWARE DETECTION: This dashboard presents malware events sourced from endpoint security logs. The current screenshot shows multiple malicious activity alerts, including threats identified as ransomware behavior, a rootkit signature and Trojan detections.


Severity: Critical


Reason: The dashboard shows confirmed, executed malware on endpoints (ransomware, rootkits, Trojans). This is not a failed attempt or a probe; it is a successful breach. These malware types can lead to immediate data encryption (ransomware), persistent hidden access (rootkit), and remote system control (Trojan).


3.	UNUSUAL IP ADDRESSES: These various dashboards show unusual IP addresses that have tried to gain access, some of which already have.


Severity: Critical


Reason: Though some of the IP addresses failed to authenticate, they eventually where able to gain access which makes it a successful breach and can lead irreparable damages to the system if not detected early.


CORRECTIVE ACTIONS


•	DASHBOARD & ALERTS: Setting up real-time dashboards for malware, IP anomalies, login failure, and any other form security breach.


•	CORRELATION RULES: Create correlation searches to detect patterns (e.g., repeated logins from one IP across multiple accounts).


•	SOAR AUTOMATION: Use Splunk Phantom/ SOAR to automatically block IPs, disable compromised accounts, or isolate hosts.


•	BASELINE NORMAL ACTIVITY: Establish baselines for normal login behaviour and network activity, then trigger alerts for deviations.


•	LOG ENRICHMENT: Enrich logs with user context (AD group, asset criticality) for better triaging.

