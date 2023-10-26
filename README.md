# SIEM-Sentinel
<h1>Taking Failed RDP(Remote Desktop Protocol) to IP Geolocation Information</h1>



<h2>Description</h2>
<b>The Powershell script in this repository is responsible for using the Windows Event Log information for failed RDP attacks around the globe and using a third party API to collect geographic information about the attackers location.
</b>
<br />
<br />
The script is used in this demo where I setup Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honey pot.
We will observe live attacks (RDP Brute Force) from all around the world. I will use a custom PowerShell script to
look up the attackers Geolocation information and plot it on an Azure Sentinel Map. Creating the virtual machine on Azure to bait attacks.
<br />
<br />


<p align="center">
<img src="https://i.imgur.com/jr7sibp.png" height="85%" width="85%" alt="Azure Virtual Machine"/>
</p>

<h2>Live Bait</h2>
<b>Opening the Windows Defender Firewall
</b>
<br />
<br />
It is imperative to open the Windows Defender Firewall properties to leave the Virtual Machine defenseless as live bait. This way attackers will be able to find the system more easily and allow you to use them as data in this project.
<br />
<br />


<p align="center">
<img src="https://i.imgur.com/E77E7Dw.png" height="85%" width="85%" alt="Azure Virtual Machine"/>
</p>


<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks from across the globe coming in; Custom logs being output with geodata</h2>
<b>Using the IP Address of the attackers, we are able to log their locations.(The Error is only due to having a capacity on the query)
</b>
<p align="center">
<img src="https://i.imgur.com/vNObA0s.png" height="85%" width="85%" alt="Map Data"/>
</p>

<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://i.imgur.com/KjgxVV6.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
