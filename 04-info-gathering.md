🔎 Information Gathering
--------------------------
Target - https://www.bridgeapi.io/
   1.whois :-
Name - bridgeapi.io
Registry Domain ID - fd64e3652b0b4b91900fa6f1fae4e1bf-DONUTS
Registered On - 2017-05-03T16:02:51Z
Expires On - 2026-05-03T16:02:51Z
Updated On - 2025-03-17T09:23:12Z
Domain Status - client transfer prohibited
Name Servers - eva.ns.cloudflare.com,eff.ns.cloudflare.com

  2.dig :-
  it is a powerful DNS lookup tool used to query DNS records for a domain name — perfect for info gathering, pentesting, or troubleshooting.
  basic syntax : dig [options] [domain] [record_type]

  dig https://bridgeapi.io
output :https://bridgeapi.io [200 OK] Country[US], CMS[WordPress], X-Powered-By[PHP/7.4.3], etc.

   3.NSLookup :-

   Find IP Address of a Domain : nslookup bridgeapi.io
 Server:         192.168.29.1
Address:        192.168.29.1#53

Non-authoritative answer:
Name:   bridgeapi.io
Address: 75.2.70.75
Name:   bridgeapi.io
Address: 99.83.190.102

  4.shodan :-
Shodan is a powerful search engine that scans and indexes internet-connected devices like:
Web servers
Routers
Security cameras
Databases
IoT devices
Industrial control systems (SCADA)
Unlike Google (which indexes websites), Shodan indexes devices + services exposed to the internet — perfect for cybersecurity, pentesting, and recon.

 5. basic python script for info gathering :-
 import subprocess
import socket
from shodan import Shodan

target = "bridgeapi.io"
shodan_api_key = "YOUR_SHODAN_API_KEY"  # Replace with your key

def run_command(command):
    result = subprocess.getoutput(command)
    print(f"\n>>> {command}\n{result}\n")
    return result

# WHOIS
run_command(f"whois {target}")

# DNS Lookups
run_command(f"dig {target} ANY +noall +answer")
run_command(f"nslookup -type=ns {target}")
run_command(f"host {target}")

# Get IP address
ip = socket.gethostbyname(target)
print(f"\nResolved IP: {ip}")

# Nmap Scan
run_command(f"nmap -Pn -sV -T4 {ip}")

# Shodan Info
try:
    api = Shodan(shodan_api_key)
    result = api.host(ip)
    print("\nShodan Results:")
    print(f"IP: {result['ip_str']}")
    print(f"Organization: {result.get('org')}")
    print(f"Operating System: {result.get('os')}")
    print(f"Open Ports: {result['ports']}")
except Exception as e:
    print("Shodan error:", e)

   6. basic bash script for info gathering :-
   #!/bin/bash

TARGET="bridgeapi.io"
IP=$(dig +short $TARGET | head -n 1)

echo "🔍 WHOIS Info:"
whois $TARGET

echo -e "\n🌐 DIG:"
dig $TARGET ANY +noall +answer

echo -e "\n📡 NSLOOKUP:"
nslookup -type=ns $TARGET

echo -e "\n📨 MX Records:"
dig $TARGET MX +short

echo -e "\n📁 HOST:"
host $TARGET

echo -e "\n🌍 Resolved IP: $IP"

echo -e "\n🛡️ Nmap Scan:"
nmap -Pn -sV -T4 $IP

echo -e "\n📦 CURL Headers:"
curl -I https://$TARGET

echo -e "\n💥 Done." 