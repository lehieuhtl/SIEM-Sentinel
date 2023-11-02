# SIEM-Sentinel
<h1>Taking Failed RDP(Remote Desktop Protocol) to IP Geolocation Information</h1>



<h2>Description</h2>
<b>The PowerShell script contained within this repository serves the purpose of harnessing Windows Event Log data to identify instances of failed RDP (Remote Desktop Protocol) attacks worldwide. It accomplishes this by interfacing with a third-party API that provides geographic information about the attackers' locations.
</b>
<br />
<br />
In this demonstration, a custom PowerShell script is utilized alongside the setup of Azure Sentinel, a Security Information and Event Management (SIEM) system. The script is connected to a live virtual machine acting as a honeypot, attracting live RDP brute force attacks from around the world. The PowerShell script extracts Windows Event Log data related to these attacks and uses a third-party API to retrieve geolocation information about the attackers. It then plots these geographic locations on an Azure Sentinel Map, offering a real-time visualization of the global RDP attack landscape, all made possible by the creation of a dedicated virtual machine within the Azure environment.
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
Opening the Windows Defender Firewall properties is a critical step in this project, as it intentionally weakens the virtual machine's security, rendering it more susceptible to incoming attacks. This deliberate vulnerability serves the purpose of luring potential attackers, enabling data collection and analysis for the project's objectives.
<br />
<br />


<p align="center">
<img src="https://i.imgur.com/E77E7Dw.png" height="85%" width="85%" alt="Azure Virtual Machine"/>
</p>

<h2>Logs Query</h2>
<b>Loggins the Information
</b>
<br />
<br />
To enhance the functionality and visibility of the SIEM logs in this project, it is essential to implement code that effectively segregates and distinguishes subcategories within the logs. This process allows for a more structured organization of the data. Furthermore, when extracting information from the logs, it is important to format it in a way that makes it easily digestible for display on the map. This approach contributes to a more streamlined and informative representation of the data on the Azure Sentinel Map.
<br />
<br />


<p align="center">
<img src="https://i.imgur.com/bdPjEUj.png" height="85%" width="85%" alt="Azure Virtual Machine"/>
</p>



<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks from across the globe coming in; Custom logs being output with geodata</h2>
<b>By utilizing the IP addresses of the attackers, we can accurately log their respective geographic locations. Any encountered errors in this process are solely attributed to query limitations and capacity constraints.
 
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/vNObA0s.png" height="85%" width="85%" alt="Map Data"/>
</p>

<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://i.imgur.com/KjgxVV6.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>


<!--
Credit to Josh Madakor for inspiration on recreating and coding.
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
