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
- <b>OpenVAS<b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Kali Linux</b>
- <b>pfSense<b>

<h2>Program walk-through:</h2>


 <h2>Zenmap </h2>
Open Zenmap and enter target IP range for scan, and select scan type through Profile drop-down; hit scan: <br/>
<img width="1060" height="347" alt="image" src="https://github.com/user-attachments/assets/8f004eeb-d41f-485f-b15c-16a30688984c" />
ICMP ping scan to check for responses

<br />
<br />
"Posts / Host" tab to check what OS is being run for the IP:  <br/>
<img width="1385" height="400" alt="image" src="https://github.com/user-attachments/assets/baf2ed25-675b-4877-8b86-56a79e499eaf" />
Quick scan plus - command: nmap -sV -T4 -O -F --version-light 172.30.0.20,30,40 172.31.0.40,50,60

- <b>-sV (requests service version scan)</b>
- <b>-T4 (set scan timing/aggressiveness; T0 (parnoid), T3(normal), T5(insance))</b>
- <b>-O (enables OS detection in sequence)</b>
- <b>-F (restricts port scanning to 100 most common ports)</b>


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
**To create new custom scan options, ie. Custom scan for SSH, HTTP, HTTPS ports:**
Zenmap "Profile" Tab > "New profile / Ctrl + P" > Clear default scan options in top box > Enter "Profile name" > "Scan" tab; scan options: "TCP scan" dropdown; Choose to disable reverse DNS resolution:  <br/>
<img width="853" height="564" alt="image" src="https://github.com/user-attachments/assets/465add82-613c-4d06-beaf-d814b7807c87" />

<br />
<br />
Setup ports to ping: "Ping" tab > select "SYN ping (-PS)" > enter ports (22,80,443) > "Save changes:  <br/>
<img width="854" height="564" alt="image" src="https://github.com/user-attachments/assets/82122f97-d7ab-4ff9-bbf1-9d81d83d7aaf" />

<br />
<br />
Enter target IP, Select custom profile; Scan results:  <br/>
<img width="1105" height="758" alt="image" src="https://github.com/user-attachments/assets/205e930c-ab54-4cc3-94e1-a7d9421644ae" />

<h2>Wireshark </h2>

<br />
Filtering for results of previous scans: Set up Wireshark interface > Scan on Zenmap > input search filters in Wireshark for packet results :  <br/>
<img width="1294" height="524" alt="image" src="https://github.com/user-attachments/assets/b58a9954-21a8-4fba-a8c9-246d7b2d37cc" />

<br />

<h2>Using Nessus Vulnerability Scan</h2>

<br />
Create Nessus scan: Log in to Nessus > "Policies" tab under "Resources" > "New Policy" > Select Templates (Basic Network Scan was used) > Create:  <br/>
<img width="1920" height="508" alt="image" src="https://github.com/user-attachments/assets/156d1e6f-dff3-4e34-899a-f2d5f6068e00" />

<br />
<br />
"My Scans" Tab > "New Scan" > "User Defined" > select policy > enter target IP, save, and start scan > retrieve scan findings: <br/>
<img width="1905" height="1019" alt="image" src="https://github.com/user-attachments/assets/5dd985a1-9d33-4f89-8e2d-44482611179d" />

<br />
<br />
<h2>Using Kali Linux for Active Recon</h2>

<br />
Using nmap through the Terminal - SYN scan:  <br/>
<img width="811" height="526" alt="image" src="https://github.com/user-attachments/assets/d96f4420-5573-473a-86a5-47b55b4cb8c6" />

<br />

- <b>-n (disable DNS)<b>
- <b>-Pn (disable ping scan)<b>
- <b>-sS (SYN Stealth scan)<b>
- <b>-F (limit to common ports)<b>
- <b>-T5 (aggressive timing for faster scan)<b>

<br />
<br />
ACK scan:  <br/>
<img width="661" height="190" alt="image" src="https://github.com/user-attachments/assets/484d3f88-84ef-412d-bc20-54669a38a5c0" />
<br />

- <b>-sA (ACK scan)<b>

<br />
<br />
traceroute - check route to target address:  <br/>
<img width="661" height="253" alt="image" src="https://github.com/user-attachments/assets/87318423-c6e4-40f5-8042-28eee5536cdd" />

<br />
<br />
UDP scan:  <br/>
<img width="693" height="432" alt="image" src="https://github.com/user-attachments/assets/91c4aba0-580a-419c-8b33-725e62d25a18" />
<br />

- <b>-sU (UDP scan)<b>
- <b>-v (verbose)<b>

<br />
<br />
Scan with script:  <br/>
<img width="654" height="290" alt="image" src="https://github.com/user-attachments/assets/1e989b12-f9e9-4847-a280-0473c4e3505c" />

- <b>-p (port specification)<b>

<br />

<h2>TCP Connect Scan</h2>

<br />
Zenmap TCP Connect Scan:  <br/>
<img width="1099" height="567" alt="image" src="https://github.com/user-attachments/assets/55b4924f-8e1d-47fa-a183-f3411e133609" />

-<b>-sT (TCP Connect Scan)<b>

<br />
<br />
Captured results of scan:  <br/>
<img width="1292" height="310" alt="image" src="https://github.com/user-attachments/assets/872a8586-25da-4a29-921e-ab026df7b8c1" />

<h2>OpenVAS Greenbone Vulnarbility Scanner</h2>

<br />
<br />
Open Greenbone > "Scans" tab > "Tasks" > "New Task":  <br/>
<img width="617" height="533" alt="image" src="https://github.com/user-attachments/assets/aa6c61ab-32e3-41c0-b05d-b680a5be41e0" />

<br />
<br />
Task Setup - create new target, enter target IP > save > start task:  <br/>
<img width="998" height="256" alt="image" src="https://github.com/user-attachments/assets/986112e9-ce02-4927-b0e1-87c3def28127" />

<br />
<br />
check results > click on date > "Results":  <br/>
<img width="1587" height="710" alt="image" src="https://github.com/user-attachments/assets/b3d07552-7b38-49e5-91c6-df417cec035d" />
Clicking a vulnerability shows details on detection results and solutions.



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
