Types of Threats
-----------------
1. Malware (Malicious Software)
Definition: Software designed to damage, disrupt, or gain unauthorized access.
Examples:
Viruses – Spread by attaching to files
Worms – Spread without user action
Trojans – Disguised as legitimate software
Ransomware – Locks files and demands payment
Spyware – Secretly collects data

🔹 2. Phishing
Definition: Fake emails or messages designed to trick users into giving sensitive info.
Example: An email that looks like it's from a bank, asking you to click a link and enter your password.

🔹 3. Social Engineering
Definition: Manipulating people into revealing confidential information.
Example: A phone call pretending to be IT support asking for your login credentials.

🔹 4. Man-in-the-Middle (MitM) Attacks
Definition: Attacker secretly intercepts communication between two parties.
Example: Someone on the same Wi-Fi network intercepting your login data.

🔹 5. Denial-of-Service (DoS) / DDoS
Definition: Overloading a system or website with traffic to crash it.
DoS = One machine
DDoS = Many machines (botnets)

🔹 6. Zero-Day Exploits
Definition: Attacks that exploit unknown vulnerabilities before a fix is available.

Why dangerous? No patch exists yet — so even updated systems are vulnerable.

🔹 7. SQL Injection
Definition: Inserting malicious SQL code into a web form to access or change a database.

Example: Logging in to a site without a password by tricking it with SQL code.

🔹 8. Brute Force Attacks
Definition: Trying many password combinations until the correct one is found.

🔹 9. Credential Stuffing
Definition: Using stolen usernames/passwords from one site to try and access others.

🔹 10. Insider Threats
Definition: Attacks from employees or contractors with access to internal systems.

CIA Triad in Cybersecurity
-----------------------------
🔹 1. Confidentiality
Goal: Keep data private and only accessible to authorized users.
Examples:
Encryption of files
Passwords and multi-factor authentication (MFA)
Access controls and permissions
Threats:
Data breaches
Eavesdropping
Insider leaks

🔹 2. Integrity
Goal: Ensure data is accurate, unchanged, and trustworthy.
Examples:
Hashing (e.g., SHA-256)
Checksums
Digital signatures
Threats:
Unauthorized changes to data
Data tampering or corruption
Man-in-the-middle attacks

🔹 3. Availability
Goal: Make sure data and systems are available when needed.
Examples:
Redundant systems (backups, failover)
DDoS protection
Regular system maintenance
Threats:
Denial-of-Service (DoS) or DDoS attacks
Hardware failures
Natural disasters

Real-world breaches
--------------------
1. Equifax (2017) 
📝 Overview & Timeline
The breach began May 12, 2017, when attackers exploited an unpatched Apache Struts vulnerability (CVE‑2017‑5638) in Equifax’s web portal 
Hackers gained internal credentials and moved laterally due to flat network design, accessing sensitive data.
Stolen data (145 M Americans' PII) was exfiltrated over 76 days undetected 
Discovery occurred after an expired SSL certificate disabled internal traffic inspection tools 
Public disclosure came September 7, 2017, well after discovery.

2.MOVEit / Cl0p Attack (2023)
📝 What Happened
A zero‑day SQL injection in MOVEit file transfer software allowed Cl0p to install a web shell (“LEMURLOOT”) 
Timeline:
May 27: Attack initiated.
May 31: Vendor released patch
June: Massive data exfiltration across ~2,700 organizations (~93 M records)

3.Snowflake Cloud Breach (2024)
📝 Incident Summary
Over 160 Snowflake customer environments were breached.
Attackers (UNC5537/Scattered Spider) used stolen credentials (infostealer malware) without MFA 
Clients like AT&T, Ticketmaster, Santander impacted; AT&T’s metadata was fully exposed 
Relied on credential reuse, highlighting MFA absence as a critical vulnerability.