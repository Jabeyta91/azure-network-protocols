<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

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

- Create a resource group
- Virtual network and subnets
- Create two virtual machines one running windows the other Linux.
- Exam traffic using virtual machines using wireshark.

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/TICVLXX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I start by creating a Windows 10 Virtual Machine (VM). While creating the VM, select the previously created Resource Group labeled RGLab1. Then create a Linux (Ubuntu) VM, while I create the VM, select the previously created Resource Group and Vnet. Then by going to network watcher, then choose topology, Im prompted to enter my resource group and virtual network name. The  topology diagram displayed shows my connectivity from the subnet created to the two network interface cards (NIC). From there I can see my virtual network, network security group, and my virtual machine public IP address all in connection to my network interface card.

</p>
<br />

<p>
<img src="https://i.imgur.com/zgP5qq6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To access wireshark I then open remote desktop and paste the IP address of my windows virtual machine. Once my windows browser loads I search wireshark download on google. When the file is downloaded I open it in my computer folder and continue installation as prompted. As displayed in the picture once downlaod is complete wireshark shows live traffic. Its spamming traffic for the example you will notice even though im not yet doing anything so much stuff is happening in the background. The source IP address 10.0.0.4 is sending traffic. 
</p>
<br />

<p>
<img src="https://i.imgur.com/EZFEk1M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside my VM1 I open powershell and ping 10.0.0.5 which is my Linux VM2 private IP address. By filtering all traffic by Internet Control Message Protocol (IMCP). As you see there was four echo request followed by four replies. Source is diplaying VM1 IP address and the destination is VM2 IP address. 
</p>
<br />

<p>
<img src="https://i.imgur.com/EdzmSZr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
