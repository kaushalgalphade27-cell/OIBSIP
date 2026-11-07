# Basic Network Scanning with Nmap

## 1. Project Overview
This project demonstrates basic network scanning using Nmap in a controlled Kali Linux virtual machine environment.

## 2. Objective
- Identify open, closed, and filtered ports.
- Detect running services and their versions.
- Perform operating system detection.
- Understand basic network security risks.

## 3. Tools and Environment
- Operating System: Kali Linux
- Virtualization: Oracle VirtualBox
- Scanning Tool: Nmap 7.98
- Programming/Testing Tool: Python 3.13.12

## 4. Scanning Activities

### A. Basic Network Scan
Command:
`nmap 10.0.2.15`

Result:
- Host status: Up
- Scanned TCP ports: 1000
- Filtered ports: 1000
- Open ports detected: 0

### B. Service Version Detection
A temporary HTTP server was started on localhost port 8000.

Command:
`nmap -sV -p 8000 127.0.0.1`

Result:
- Port: 8000/tcp
- State: Open
- Service: HTTP
- Version: SimpleHTTPServer 0.6
- Runtime: Python 3.13.12

### C. Operating System Detection
Command:
`sudo nmap -O -p 1-100,8000 127.0.0.1`

Result:
- Device type: General purpose
- OS estimate: Linux
- Network distance: 0 hops

Note: Nmap OS detection provides a fingerprint-based estimate, not a guaranteed exact OS version.

## 5. Security Analysis
- Filtered ports may indicate that firewall rules or network filtering are preventing responses.
- An open port indicates that a service is listening and should be reviewed.
- Running services should be kept updated and exposed only when required.
- Service version detection helps administrators identify software that may need security updates.

## 6. Files Included
- `nmap_scan_results.txt` – Saved Nmap scan outputs.
- `screenshots/` – Screenshots of the practical work.

## 7. Ethical Guidelines
- Scanning was performed only on the author's own Kali Linux virtual machine and localhost.
- Always obtain permission before scanning any other system or network.
- Do not scan public or third-party systems without authorization.

## 8. Conclusion
This project provided practical experience with Nmap, including basic port scanning, service version detection, and operating system detection in a controlled lab environment.
