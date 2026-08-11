# networkwalks-B082-week1-Cybersecurity-lab-setup
Cybersecurity Lab Setup
📌 Project Overview  
This project establishes a virtual cybersecurity and penetration-testing lab using VirtualBox and Kali Linux. The lab provides a safe, controlled environment for practicing security testing — including reconnaissance, vulnerability assessment, and exploitation — without risking real-world systems.

The setup uses a private NAT network, allowing future expansion with additional target machines for authorized testing.

**🎯 Objectives**

Install and configure VirtualBox

Import Kali Linux as a VM

Create a private NAT Network

Configure Kali Linux network connectivity

Assign a static IP address to the VM

Verify connectivity and DNS resolution

Take a clean baseline snapshot

Document the entire process

Prepare the lab for future cybersecurity projects

🛡️ Purpose of the Lab  
This lab is designed for learning and ethical security testing. It supports:

Network reconnaissance

Port scanning

Vulnerability assessment

Packet analysis

Web security testing

Exploitation practice

Experimentation with security tools

⚠️ Note: Use this lab only on systems you own or have explicit permission to test.

🏗️ Lab Architecture  
The NAT network allows attacker and target VMs to communicate internally while maintaining outbound internet access. More machines can be added later for advanced exercises.

⚙️ Lab Configuration

Component	Configuration
Host OS	Windows 11
Host RAM	32 GB
Processor	Intel Core i7
Hypervisor	VirtualBox 7.2
Security OS	Kali Linux 2026.2
Kali RAM	2048 MB
Virtual Network	NAT Network
Network Address	10.0.0.0/24
Kali IP Address	10.0.0.2/24
Gateway	10.0.0.1
DNS Server	8.8.8.8
Future VM Range	10.0.0.3–10.0.0.99


🪜 Setup Steps

Install 7-Zip – Extract Kali VM package (.7z).

Install VirtualBox – Set up the hypervisor.

Create NAT Network – Configure 10.0.0.0/24 with DHCP enabled.

Import Kali Linux VM – Attach to NAT Network, allocate 2 GB RAM, configure shared folder.

Configure Network – Assign static IP (10.0.0.2), gateway (10.0.0.1), DNS (8.8.8.8).

Create Snapshot – Save baseline state (“Clean Kali - Network Setup”).

🔎 Verification Tests

ip a → Correct IP displayed

ping 10.0.0.1 → Gateway reachable

ping 8.8.8.8 → Internet connectivity confirmed

nslookup networkwalks.com → DNS resolution works

nmap –version → Nmap installed

Snapshot restore → Baseline recovered

🐞 Challenges & Fixes

Network was not listed among the tools section in the Virtual Box file menu.
This was resolved to uninstalling and reinstalling the Virtual Box
💡 Key Learnings

Difference between NAT and NAT Network

How VM adapters affect communication

Configuring static IPs in Kali Linux

Importance of VM snapshots for recovery

Value of thorough documentation in cybersecurity projects

🔐 Ethical Use  
This lab is strictly for educational and authorized testing purposes.

🔗 Resources

7-Zip

VirtualBox

Kali Linux

👤 Author  
Solomon Alaba  
Cybersecurity Intern (B082)
LinkedIn: https://www.linkedin.com/in/solomon-alaba-391b0228b/ 

📌 Project Info  
Program: Cybersecurity at Networkwalks | Week 01 | Project: Lab Setup | Repository: GitHub
