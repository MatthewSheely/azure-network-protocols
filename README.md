<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create a Resource Group
- Create a Virtual Machine
- Download Wire Shark   
- Command & Observe ICMP
- Command & Observe DNS
- Command & Observe RDP
- Command & Observe SSH
- Command & Observe DHCP

  
<h2>Setup with Configuration</h2>

<h3>Create a Resource Group</h3>

1A. After signing into your Azure account. Go to Resource Groups and create a Resource Group.
<p align="center">
<img src="https://i.imgur.com/QsVKcoA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>

1B.Give your Resource Group a Name (Create Resource Group)
<p align="center">
<img src="https://i.imgur.com/DU4fEWU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

1C. Confirm Resource Group is Created
<p align="center">
<img src="https://i.imgur.com/ZC8ppB3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h3>Create a Virtual Machine</h3>

2A. Create two Virtual Machines (Windows & Linux)
<p align="center">
<img src="https://i.imgur.com/0Jcq3Gv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

2B. Choose the Resource Group Created, Name your Virtual Machine, and Select the Region you are in, along with the Operating System for the VM. 
<p align="center">
<img src="https://i.imgur.com/CCcJZDl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

2C. Choose the Size of your Operating System, create a username and password, check the confirm box, then create your VM.
<p></p>
<p align="center">
<img src="https://i.imgur.com/mMmzern.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

2D. Create a VM using Ubuntu as the Operating System
<p></p>
<p align="center">
<img src="https://i.imgur.com/Wi1N4RO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>

2E. Confirm your Virtual Machines have been created
<p align="center">
<img src="https://i.imgur.com/fRZkYPJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>

<h3>Download Wire Shark</h3>

3A. Login to VM1 (Client-1) using the Public IP Address
<p>
<p align="center">
<img src="https://i.imgur.com/hKA9muI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
  
3B. Use the login credential created for the VM1(Client-1)
<p align="center">
<img src="https://i.imgur.com/wA8maG7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

3C. Once logged into the VM, Use Microsoft Edge to Install Wireshark 
<p></p>
<p align="center">
<img src="https://i.imgur.com/8a6v3Go.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>

3D. Once completed you can start to observe traffic in Wireshark.
<p></p>
<p align="center">
<img src="https://i.imgur.com/wv628ex.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  
<h2>Actions and Observations</h2>

In this section, we will observe the traffic between VMs (DC-1 & Client-1). To do this we will need to use the private IP Address of the Ubuntu VM(DC-1) and ping from the Windows 10 VM (Client-1). 

<h3>Oberve ICMP</h3>

Below is ICMP traffic in Wireshark between VMs. 
<p align="center">
<img src="https://i.imgur.com/6oHEfxw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>

Below is ICMP (Internet Control Message Protocol) traffic in Wireshark between www.google.com and the VM.
  
<p align="center">
<img src="https://i.imgur.com/sCvsTP6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>

<h3>Observe DNS</h3>

Below is DNS (Domain Name System) traffic in Wireshark

<p align="center">
<img src="https://i.imgur.com/xf66EMJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p></p>

<h3>Observe RDP</h3>

Below is RDP (Remote Desktop Protocol) traffic in Wireshark

<p align="center">
<img src="https://i.imgur.com/zl0Bxpv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
<h3>Observe SSH</h3>

Below is SSH (Secure Shell) traffic in Wireshark
<p align="center">
<img src="https://i.imgur.com/3Is9VYi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h3>Observe DHCP</h3>

Below is DHCP (Dynamic Host Control Protocol) traffic in Wireshark
<p align="center">
<img src="https://i.imgur.com/m8dq18Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


