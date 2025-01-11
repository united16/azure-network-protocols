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
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
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
<img src="RG Creation.jpg" height="25%" width="25%" alt="RG Creation"/> <img src="Creat win-vm.jpg" height="25%" width="25%" alt="Windows VM"/> <img src="linux-VM.jpg" height="25%" width="25%" alt="Linux VM"/>
</p>
<p>
After creating the Resource Group (RG), I set up Windows and Linux Virtual Machines (VMs) and placed them within the RG. I also configured a new Virtual Network and added both VMs to it. Then connect to them via Remote desktop.
</p>
<br />

<h4>Step 2: Wireshark, Configuring Firewall and Secure Shell </h4> 
<p>
<img src="Wireshark Install.jpeg" height="25%" width="25%" alt="Wireshark Install"/> <img src="Ping Linux.jpeg" height="25%" width="25%" alt="Ping Linux"/> <img src="Continue Pinging.jpeg" height="25%" width="25%" alt="Continue Pinging"/> 
  <img src="Linux ICMP Deny.jpg" height="20%" width="20%" alt="ICMP Deny"/>

</p>
<p>
Wireshark is a network protocol analyzer that allows us to capture, inspect, and analyze network traffic. After installing Wireshark, I intended to ping Linux VM from Windows 10 VM using PowerShell, targeting the private IP address of the Linux VM. Next, I proceeded to configure the firewall by first initiating a continuous ping from the Windows 10 VM to the Linux VM and creating a new rule in Azure for the Linux VM to deny incoming ICMP traffic, in order to observe the outcome in Wireshark.
</p>
<br />

<h4>Step 3: DHCP and DNS</h4> 
<p>
<img src="" height="25%" width="25%" alt=""/> <img src="" height="25%" width="25%" alt=""/> <img src="" height="25%" width="25%" alt=""/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h4>Step 4: RDP</h4> 
<p>
<img src="" height="25%" width="25%" alt=""/> <img src="" height="25%" width="25%" alt=""/> <img src="" height="25%" width="25%" alt=""/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
