<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<!--<h2>Video Demonstration</h2

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)-->

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH,RDH,DNS,DHCP,ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 24.04

<!--<h2>High-Level Steps</h2>

- Created a Resource Group (RG), a Windows and Linux Virtual Machines (VM)
- Downlaod Wireshark
- Step 3
- Step 4-->

<h2>Actions and Observations</h2>
<h4>Step 1: RG, Windows and Linux VM</h4>
<p>
<h5>RG</h5> <img src="RG Creation.jpg" height="25%" width="25%" alt="RG Creation"/> <h5>Windows</h5> <img src="Creat win-vm.jpg" height="25%" width="25%" alt="Windows VM"/> <h5>Linux</h5> <img src="linux-VM.jpg" height="25%" width="25%" alt="Linux VM"/>
</p>
<p>
After creating the Resource Group (RG), I set up Windows and Linux Virtual Machines (VMs) and placed them within the RG. I also configured a new Virtual Network and added both VMs to it. Then connect to them via Remote desktop.
</p>
<br />

<h4>Step 2: Wireshark and Configuring Firewall</h4> 
<p>
<h5>Install Wireshark</h5> <img src="Wireshark Install.jpeg" height="25%" width="25%" alt="Wireshark Install"/> <h5>Pinging Linux</h5> <img src="Ping Linux.jpeg" height="25%" width="25%" alt="Ping Linux"/> <h5>Continues Ping</h5> <img src="Continue Pinging.jpeg" height="25%" width="25%" alt="Continue Pinging"/> <h5>ICMP Deny</h5> <img src="Linux ICMP Deny.jpg" height="20%" width="20%" alt="ICMP Deny"/>

</p>
<p>
Wireshark is a network protocol analyzer that allows us to capture, inspect, and analyze network traffic. After installing Wireshark, I intended to ping Linux VM from Windows 10 VM using PowerShell, targeting the private IP address of the Linux VM. Next, I proceeded to configure the firewall by first initiating a continuous ping from the Windows 10 VM to the Linux VM and creating a new rule in Azure for the Linux VM to deny incoming ICMP traffic, in order to observe the outcome in Wireshark.
</p>
<br />

<h4>Step 3: SSH and DHCP</h4> 
<p>
<h5>SSH</h5> <img src="SSH.jpg" height="25%" width="25%" alt="SSH"/> <h5>DHCP</h5> <img src="release  renew.jpg" height="25%" width="25%" alt="rr"/>
</p>
<p>
I also worked with SSH (Secure Shell), which is a protocol that allows a computer to establish a secure connection with another computer. I successfully established an SSH connection from a Windows 10 VM to a Linux VM using the Linux private IP address and analyzed the corresponding traffic in Wireshark. Furthermore, I worked with DHCP (Dynamic Host Configuration Protocol), which is used to automatically assign IP addresses and other network configuration details to devices on a network. I observed DHCP traffic in Wireshark while experimenting with various PowerShell commands, such as: ipconfig /renew (which doesn't renew the IP address but initiates certain background processes) and ipconfig /release (which releases or drop the current assigned IP address)
</p>
<br />

<h4>Step 4: RDP(TCP- port 3389) and DNS(TCP & UDP- port 53)</h4> 
<p>
<h5>DNS</h5> <img src="ns.jpg" height="25%" width="25%" alt="nslookup"/> <h5>RDP</h5> <img src="conncet.jpg" height="20%" width="20%" alt=""/> <img src="conncection.jpg" height="20%" width="20%" alt=""/>
</p>
<p>
DNS(Domain Name System) is a system that converts human readable domain names into IP addresses that computers use to communicate. I used Wireshark to filter for DNS traffic only, so I could observe the traffic while executing commands in PowerShell. I typed 'nslookup google.com' in PowerShell, which displayed the IP address of the website. In Wireshark, I observed the packet traffic related to the DNS query and response. RDP(Remote Desktop Protocol) is a protocol used to remotely connect one computer to another, enabling access to the remote computers desktop environment wirelessly. This connection provides a remote desktop GUI (Graphical User Interface), allowing users to interact with the remote computer as if they're physically in front of it.


</p>
<br />
