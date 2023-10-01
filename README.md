<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

-Define Objectives and Requirements:

Clearly define the objectives of the deployment and identify the specific requirements, such as hardware, software, and networking prerequisites.
Select Deployment Environment:

Choose the appropriate deployment environment, which can include on-premises servers, cloud platforms (e.g., AWS, Azure, Google Cloud), or hybrid solutions.
Plan and Design:

Create a deployment plan and design architecture that outlines the system's components, their interactions, and scalability considerations.
Prepare Infrastructure:

Set up and configure the necessary infrastructure components, such as servers, databases, storage, and networking resources.
Software Installation:

Install the required software and dependencies on the designated servers or virtual machines. This may involve configuring operating systems, web servers, databases, and middleware.

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/lKmRcIy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Firstly, we will need to establish the resource group so that you can add your virtual machines for the Domain Controller (DC-1) and the Client Virtual Machine (Client-1). The Domain Controller VM will use a Windows Server 2022 system image (a serialized copy of the entire state of a computer system stored in some non-volatile form such as a file). 
</p>
<br />

<p>
<img src="https://i.imgur.com/w34Z93S.png" height="80%" width="80%" alt="client 1 vm settings"/>
</p>
<p>
Private IP address set to static (static IP addresses are necessary for devices that need constant access.)
<p align="center">
</p>
<br />

<p>
<img src="https://i.imgur.com/w34Z93S.png" height="80%" width="80%" alt="client 1 vm settings"/>
</p>
<p>
Second, check for a connection between the client device and domain controller by logging into Client-1 with Remote Desktop Connection (RDP) and pinging DC-1’s private IP address using ping -t (perpetual ping). ICMPv4 (ping) was allowed on the Domain Controller's (DC-1) Firewall in Windows Firewall (Core Networking Diagnostics - ICMP Echo Request (ICMPv4-In)). After logging back into Client-1 check to make sure the ping is successful.
</p>
<br />
