# NETWORKWALKS-ABDUL-AZIM-B083-WK1-PM1-CYBERSECURITY-LAB-SETUP
**A cybersecurity and penetration testing lab setup** <br/>
## CYBERSECURITY LAB SETUP
**Building a controlled environment for penetration testing and ethical hacking.** <br/>

## PROJECT OVERVIEW
This project focuses on setting up a virtual lab for penetration testing and ethical hacking using Kali linux on a virtual box machine.
This virtual environment will be used for reconnaissance network scanning, ethical hacking, and  many more.
It uses a private network which would be used subsequently with other machines to carry out specific tasks.<br/>

### PROJECT OBJECTIVES
**The main objectives of this project are to:**
•	Install and configure VirtualBox.
•	Install/import Kali Linux as a virtual machine.
•	Create a private NAT Network for the cybersecurity lab.
•	Configure network connectivity for Kali Linux.
•	Assign a consistent IP address to the Kali VM.
•	Verify network connectivity and DNS resolution.
•	Take a clean VM snapshot for recovery.
•	Document the complete setup process.
•	Prepare the environment for future cybersecurity projects.<br/>


### 🛡️ Purpose of the Lab
**The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing.**
**It can be used for activities such as:**
•	Network reconnaissance
•	Port scanning
•	Vulnerability assessment
•	Packet analysis
•	Web security testing
•	Exploitation practice
•	Security-tool experimentation<br/>

⚠️ Important: This laboratory must only be used for systems that you own or have explicit permission to test. Do not use the lab or its tools to attack unauthorized systems.<br/>
⚙️ Lab Configuration
🧩 Component	⚙️ Configuration
🖥️ Host OS	Windows 11 Pro
🧠 Host RAM	8 GB
⚡ Processor	Intel Core i7
🧰 Hypervisor	VirtualBox 7.2
🐉 Security OS	Kali Linux 2026.2
🧠 Kali RAM	2048 MB
🌐 Virtual Network	NAT Network
📡 Network Address	10.0.0.0/24
🐧 Kali IP Address	10.0.0.2/24
🚪 Default Gateway	10.0.0.1
🌍 DNS Server	8.8.8.8
🔮 Future VM Range	10.0.0.3–10.0.0.99<br/>
	

## LAB SETUP PROCESS

### Step 1. Install 7zip
7zip was installed to extract the kali-linux package which was distributed as 7zip archive.<br/>

### Step 2. Install virtual box
The virtual box was install as the hypervisor.<br/>

### Step 3. Create NAT Network
A  NAT Network was created for the virtual virtual box in order to give it a private network.
A dedicated NAT Network was created in VirtualBox.
Configuration: Network Name: NatNetwork IPv4 Prefix: 10.0.0.0/24 DHCP: Enabled IPv6: Disabled
A NAT Network was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.
This will allow future attacker and target VMs to communicate within the lab.<br/>
 

### Step 4. Import Kali linux
The installed kali linux was imported from the file explorer by copying its path.
Adapter 1
Attached to: NAT Network
Network:     NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop
The VM was allocated a RAM of 2048 MB

A shared folder was also configured for transferring required files between the host operating system and the Kali VM.<br/>
 
________________________________________
### Step 5. Configure the Kali Linux Network
The Kali Linux network configuration was checked and configured with a consistent IPv4 address.
Example configuration:
IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8
A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises.<br/>

 
### Step 6. Create a Clean VM Snapshot
After completing the initial configuration, a VirtualBox snapshot was created.
Example snapshot name:
Clean Kali - Network Setup
The snapshot represents the clean baseline of the laboratory.
If a future exercise changes or damages the VM configuration, the machine can be restored to this baseline.<br/>

**🔎 Lab Verification**
✅ Test	🧾 Command	🎯 Expected Result
🌐 Check IP address	ip a	Correct Kali IP displayed
📡 Test gateway	ping 10.0.0.1	Successful replies
🌍 Test Internet connectivity	ping 8.8.8.8	Successful replies
🔎 Test DNS resolution	nslookup networkwalks.com	Domain resolves
🧰 Verify Nmap	nmap --version	Nmap version displayed
🔄 Verify snapshot	Restore snapshot and run ip a	Baseline configuration restored
Example Results
IP Address:
10.0.0.2/24

Gateway:
10.0.0.1

DNS:
8.8.8.8


## 💡 What I Learned
Through this project, I learned how to create and configure a virtual environment for cybersecurity practice.
The most important concepts I learned include:
### 1. NAT vs NAT Network
NAT translates private IP addresses to public IPs for internet access, while a NAT Network provides a virtualized network where multiple virtual machines share NAT-based connectivity.
### 2. Virtual Machine Networking
I learnt how a virtual machine network works both automatic and manually.
### 3. Static IP Configuration
I learned how to configure and verify IPv4 addressing, subnet masks, gateways, and DNS settings in Kali Linux.
### 4. VM Snapshots
I learned that a clean snapshot should be created before performing risky or experimental activities.
This provides a known-good recovery point for future cybersecurity exercises.

### 5. Documentation
I learned that documenting commands, configuration, screenshots, problems, and solutions is an important part of a professional cybersecurity project.
________________________________________
🔐 Security & Ethical Use
This laboratory is intended strictly for education purposes only.
________________________________________
🔗 Tools & Resources
•	7-Zip: https://7-zip.org/download.html
•	VirtualBox: https://virtualbox.org/wiki/Downloads
•	Kali Linux: https://kali.org/get-kali
________________________________________
👤 Author
Abdul-Aziz Abdul-Azim
LinkedIn: www.linkedin.com/in/abdul-azim-abdul-aziz-b15173411
________________________________________
📌 Project Information
Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity & Pentesting Lab Setup | Repository: GitHub


