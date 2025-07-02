OSI Model (Open Systems Interconnection)
------------------------------------------
The OSI Model is a conceptual framework created by the International Organization for Standardization (ISO). It divides the process of network communication into 7 layers, each with a specific function. It is mainly used for teaching, troubleshooting, and standardization.
The 7 Layers of OSI:
Physical – Transmits raw bits (cables, signals)
Data Link – Frames, MAC addresses, switches
Network – Routing, IP addresses
Transport – Ensures reliable data (TCP/UDP)
Session – Manages connections between apps
Presentation – Translates, encrypts, compresses
Application – Interfaces with software (e.g., browsers, email)

TCP/IP Model (Transmission Control Protocol/Internet Protocol)
------------------------------------------------------------------
The TCP/IP Model is a real-world, practical model that forms the basis of the modern internet. It has 4 layers, and protocols like TCP, IP, HTTP, FTP are part of it.
The 4 Layers of TCP/IP:
Network Access (or Link) – Physical transmission (Ethernet, Wi-Fi)
Internet – Routing and IP addressing
Transport – End-to-end communication (TCP/UDP)
Application – Supports applications (HTTP, DNS, SMTP)

Ports in networking
---------
In networking, a port is like a door on your computer that lets data in and out through specific applications or services.

Types of Ports
Well-known ports-0 – 1023-Common system services (HTTP, SSH)
Registered ports-1024 – 49151-Used by software/apps (e.g., MySQL)
Dynamic/private port-49152 – 65535-Temporary ports used by clients

Protocols in Networking
------------------------
A protocol is a set of rules that defines how data is transmitted between devices in a network.
Just like humans use languages to communicate (English, Hindi, etc.), computers use protocols to exchange data accurately and securely.

🔹 Common Types of Protocols

🔸 1. HTTP (HyperText Transfer Protocol)
Used for: Browsing websites
Port: 80
Example: When you visit http://example.com

🔸 2. HTTPS (HTTP Secure)
Used for: Secure websites (encrypted)
Port: 443
Uses: SSL/TLS encryption
Example: https://bank.com

🔸 3. FTP (File Transfer Protocol)
Used for: Transferring files between computers
Port: 21 (control), 20 (data)

🔸 4. SSH (Secure Shell)
Used for: Secure remote login and command-line access
Port: 22
Example: ssh user@192.168.1.10

🔸 5. TCP (Transmission Control Protocol)
Purpose: Reliable, connection-based communication
Features: Data is guaranteed and ordered
Used in: HTTP, HTTPS, FTP, SMTP

🔸 6. UDP (User Datagram Protocol)
Purpose: Faster but unreliable communication
Features: No guarantee of delivery
Used in: Streaming, gaming, DNS

🔸 7. DNS (Domain Name System)
Used for: Translating domain names into IP addresses
Port: 53

🔸 8. SMTP / POP3 / IMAP
SMTP (Port 25): Sends emails
POP3 (Port 110): Downloads emails (removes from server)
IMAP (Port 143): Syncs email between devices and server
