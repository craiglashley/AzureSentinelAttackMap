<h1>Azure Sentinel Honeypot With Attack Map</h1>

<h2>Description</h2>
I created a vulnerable virtual machine by exposing it to the internet and then collected logs from bad actor login attempts. These logs were parsed through Azure Sentinel to create an attack map.

![image](https://github.com/craiglashley/AzureSentinelAttackMap/assets/164884179/be0bcf9c-f6b1-4d07-85b5-06212bfaf6e8)
<br />

<h2>Languages</h2>

- [PowerShell](https://learn.microsoft.com/en-us/powershell/)  

<h2>Resources</h2>

- [SIEM Tutorial | Azure Sentinel Tutorial | MAP with LIVE CYBER ATTACKS!](https://www.youtube.com/watch?v=02RE3B2uIvw)  
  
<h2>Utilities Used</h2>

- [Azure Windows Virtual Machine](https://azure.microsoft.com/en-us/products/virtual-machines)  
- [Azure Log Analytics](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/log-analytics-workspace-overview)  
- [Windows Defender in the Cloud](https://learn.microsoft.com/en-us/azure/defender-for-cloud/defender-for-cloud-introduction)  
- [Azure Sentinel](https://azure.microsoft.com/en-us/products/microsoft-sentinel)  
- [Windows Firewall](https://learn.microsoft.com/en-us/windows/security/operating-system-security/network-security/windows-firewall/)  
- [Windows Event Viewer](https://learn.microsoft.com/en-us/shows/inside/event-viewer)  
- [ipgeolocation API Key](https://app.ipgeolocation.io/)

<h2>Steps and Results</h2>
<p align="center">
Setup Azure

![image](https://github.com/craiglashley/craiglashley/assets/164884179/96a30e1d-dbe2-4064-b399-0750cce98b44)
<p align="center">
Create Windows VM

![image](https://github.com/craiglashley/craiglashley/assets/164884179/fcbb69c5-5a90-4eb0-835c-682088a382ab)
<p align="center">
Inbound Firewall Rule

![image](https://github.com/craiglashley/craiglashley/assets/164884179/51179464-9a1a-42b0-ad70-298b7d3a0b9c)
<p align="center">
Create Log Analytics Workspace

![image](https://github.com/craiglashley/craiglashley/assets/164884179/7037242f-dc35-4667-ae2a-cd25bcbac464)
<p align="center">
Connecting VM to Log Analytics

![image](https://github.com/craiglashley/craiglashley/assets/164884179/36fce30e-067f-4a96-b8c2-ea8320a82996)
<p align="center">
Add Microsoft Sentinel to a workspace

![image](https://github.com/craiglashley/craiglashley/assets/164884179/2d5e25c4-5bd2-470d-ad25-33c8fac13ce0)
<p align="center">
Establish RDP Connection to VM

![image](https://github.com/craiglashley/craiglashley/assets/164884179/3d3d75eb-25ad-4c80-bcc2-9525016e2151)
<p align="center">
Change Windows settings to No

![image](https://github.com/craiglashley/AzureSentinelAttackMap/assets/164884179/3d96f2a2-aa10-41eb-b235-84f7249b0fbc)
<p align="center">
Turn Domain, Private, and Public Firewalls Off

![image](https://github.com/craiglashley/craiglashley/assets/164884179/70889e82-ed73-4d03-ac57-14fc5cb10f45)
<p align="center">
Copy Custom_Security_Log_Exporter into VM PowerShell

![image](https://github.com/craiglashley/AzureSentinelAttackMap/assets/164884179/280c54d3-6964-462e-a271-947a1c4d3ed8)
<p align="center">
Get free API Key from https://app.ipgeolocation.io/

![image](https://github.com/craiglashley/craiglashley/assets/164884179/e38bf270-2a4b-455d-bdaf-0ca473cc3eac)
<p align="center">
Add API Key To PowerShell

![image](https://github.com/craiglashley/craiglashley/assets/164884179/a41c7d89-d4c9-467d-9865-8f43f59183a9)
<p align="center">
Create a custom log in Azure Log Analytics

![image](https://github.com/craiglashley/craiglashley/assets/164884179/7dcda777-0681-4d19-995b-0fb8e30c5e45)
<p align="center">
Failed Login Attempts

![image](https://github.com/craiglashley/craiglashley/assets/164884179/350f73a0-d19b-4970-b2d8-acfe60b9ac9d)
<p align="center">
Create a New Workbook in Sentinel to Display Attack Map

![image](https://github.com/craiglashley/craiglashley/assets/164884179/d3da4dcd-8165-484e-a22d-67b59b14f58a)
