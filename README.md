# Performing-Active-Reconnaissance-Lab

<h2>Description</h2>

Project consists of using network scanning tools in order to perform active reconnaissance on a virtual target network to gather information on network structure, endpoints, and ports. This project was done in a virtual lab set up. 
<br />

<h2> Lab Topography</h2>

<img width="900" height="658" alt="image" src="https://github.com/user-attachments/assets/afbc31c7-b905-487b-95a8-bd9955de19ff" />

<h2>Languages and Utilities Used</h2>

- <b>Nmap / Zenmap</b> 
- <b>Wireshark</b>
- <b>Nessus<b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Kali Linux</b>
- <b>pfSense<b>

<h2>Program walk-through:</h2>

<p align="center">
Open Zenmap and enter target IP range for scan, and select scan type through Profile drop-down; hit scan: <br/>
<img width="1060" height="347" alt="image" src="https://github.com/user-attachments/assets/8f004eeb-d41f-485f-b15c-16a30688984c" />

<br />
<br />
"Posts / Host" tab to check what OS is being run for the IP:  <br/>
<img width="1385" height="400" alt="image" src="https://github.com/user-attachments/assets/baf2ed25-675b-4877-8b86-56a79e499eaf" />

<br />
<br />
Check "Host Details" tab for port and other info: <br/>
<img width="1384" height="777" alt="image" src="https://github.com/user-attachments/assets/67eee87a-53bf-4f64-97d1-c04260902132" />

<br />
<br />
"Scans" tab to remove or append scan results:  <br/>
<img width="840" height="425" alt="image" src="https://github.com/user-attachments/assets/c8f31ec6-883b-4215-bfe8-dc66a78c7469" />

<br />
<br />
"Intense Scan" for network topology; "Topology" Tab > "Legend" for more info:  <br/>
<img width="1105" height="687" alt="image" src="https://github.com/user-attachments/assets/8faa44c7-2d85-4cdd-ba31-4fc0a896e28c" />

<br />
<br />

**To create new custom scan options:**
Zenmap "Profile" Tab > Create "New profile / Ctrl + P" > Clear default scan options in top box > "Scan" tab to select scan options; "Ping" Tab for custom ping options during scan > save changes:  <br/>
<img width="1185" height="703" alt="image" src="https://github.com/user-attachments/assets/3d62c217-5316-42ed-bc1f-8844a49b8fb1" />

<br />
<br />
Set up Wireshark interface > Scan on Zenmap > input search filters in Wireshark for packet results :  <br/>
<img width="1294" height="524" alt="image" src="https://github.com/user-attachments/assets/b58a9954-21a8-4fba-a8c9-246d7b2d37cc" />

<br />

<h2>Using Nessus</h2>

<br />
Create Nessus scan: Log in to Nessus > "Policies" tab under "Resources" > "New Policy" > Select Templates (Basic Network Scan was used) > Create:  <br/>
<img width="1920" height="508" alt="image" src="https://github.com/user-attachments/assets/156d1e6f-dff3-4e34-899a-f2d5f6068e00" />

<br />
<br />
"My Scans" Tab > "New Scan" > "User Defined" > select policy > enter target IP, save, and start scan > retrieve scan findings: <br/>
<img width="1905" height="1019" alt="image" src="https://github.com/user-attachments/assets/5dd985a1-9d33-4f89-8e2d-44482611179d" />

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
