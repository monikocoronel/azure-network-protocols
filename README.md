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

- Step 1: Create some sample file shares with various permissions
- Step 2: Attempt to access file shares as a normal user
- Step 3: Create an “ACCOUNTANTS” Security Group, assign permissions, an test access

<h2>Actions and Observations</h2>

Step 1: Create some sample file shares with various permissions

<p>
<img src="https://i.imgur.com/8N3x86J.png" height="80%" width="80%" 
</p>
<p>
 
On DC-1, on the C:\ drive, create 4 folders: “read-access”, “write-access”, “no-access”, “accounting”

<p>
<img src="https://i.imgur.com/WO8p2ZJ.png" height="80%" width="80%" 
</p>
<p>
Set the following permissions for the “Domain Users” group:
Folder: “read-access”, Group: “Domain Users”, Permission: “Read”

</p>
<br />

<p>
<img src="https://i.imgur.com/RjWGCbH.png" height="80%" 
</p>
<p>
Folder: “write-access”,  Group: “Domain Users”, Permissions: “Read/Write”
</p>
<br />
