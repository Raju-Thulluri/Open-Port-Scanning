# Scan Your Local Network for Open Ports
# Overview

This project demonstrates scanning a local network for open ports using Nmap and analyzing network traffic with Wireshark. The task focuses on identifying open ports on a specified IP (e.g., localhost) and capturing related network packets.
# Tools Used

1. Nmap: A free, open-source tool for network discovery and port scanning (nmap.org).
   
2.Wireshark: A network protocol analyzer for capturing and inspecting packets (wireshark.org).
# Requirements
Nmap (install from nmap.org)

Wireshark (install from wireshark.org)

Administrative privileges for running Nmap and Wireshark
# Usage
 
**# 1.Install Tools:**
 
1.Nmap: **sudo apt-get install nmap**(Linux) or download from nmap.org.
 
2.Wireshark: **sudo apt-get install wireshark** (Linux) or download from wireshark.org.

**# 2.Run Nmap Scan:**

**Scan localhost:**

bash:

nmap -oN scan_results.txt 127.0.0.1

**Scan specific ports with service detection:**

bash

nmap -p 21,22,23,80,443,445,3389 -sV 127.0.0.1

**# 3.Capture Traffic with Wireshark:**

Open Wireshark, select the network interface (e.g., loopback), and start capturing.

Run the Nmap scan while capturing.

Filter packets (e.g., tcp or ip.addr == 127.0.0.1) and save as scan_traffic.pcap.

**# 4.Document Results:**

Save Nmap output and Wireshark capture.

Watch the network of Nmap terminal and Wireshark interface.

# Results

Nmap: Identified open ports (e.g., 80, 443) on 127.0.0.1. See scan_results.txt and nmap_output.png.

Wireshark: Captured TCP SYN packets during the scan. See scan_traffic.pcap and wireshark_capture.png.

# Warning: Ethical use only

Only scan networks or devices you own or have explicit permission to scan. Unauthorized scanning is illegal and unethical.

The provided scan was performed on 127.0.0.1 (localhost) for safety.
