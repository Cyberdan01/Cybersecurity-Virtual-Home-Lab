<h1>Cybersecurity Virtual Home Lab</h1>

<h2>Description</h2>
The project consists of a walkthrough setting up my cybersecurity home lab, which includes Kali Linux, Metasploitable, Ubuntu Server (Wazuh), Ubuntu Desktop, and Flare VM. This home lab was designed as a controlled environment to explore real-world cybersecurity scenarios, simulate attacks and defenses, and analyze network behavior. VMware Workstation was used as the virtualization platform to host a set of virtual machines (VMs) commonly used in penetration testing, malware analysis, threat detection, and system hardening.
<br />


<h2>Languages and Utilities Used</h2>

- PowerShell

<h2>Environments Used </h2>
- VMware Workstation (21H2)
- Purpose: Practical learning, testing, and simulation of offensive and defensive security techniques. (21H2)

<h2>Program walk-through:</h2>

- <b>Virtual Machines Deployed</b>
1. Kali Linux
       <b>Purpose:<b/> Offensive Security / Penetration Testing

      <b>Tools Installed:<b/> Nmap, Burp Suite, Metasploit, Wireshark, John the Ripper, etc.

      <b>Use Case:<b/> Actively used to exploit vulnerabilities on target VMs (e.g., Metasploitable) and simulate red team tactics.

      <b>Network Mode:<b/> Host-only / Bridged (configurable)

2. <b>Metasploitable<b/>
      <b>Purpose:<b/> Vulnerable Target System

      <b>Description:<b/> Intentionally vulnerable Ubuntu-based Linux VM used to simulate common misconfigurations and vulnerabilities.

      Use Case: Targets for testing exploits, vulnerability scanning, and privilege escalation.

      Network Mode: Host-only

3. Flare VM
   Purpose: Malware Analysis and Reverse Engineering

   OS: Windows 10 (with FLARE VM toolkit installed)

   Tools Included: IDA Free, x64dbg, PEStudio, Wireshark, Sysinternals Suite, etc.

   Use Case: Static and dynamic analysis of malware in an isolated sandbox.

   Network Mode: NAT (with internet access), sometimes Host-only for isolated tests

4. Wazuh Manager
   Purpose: Security Information and Event Management (SIEM)

   OS: Ubuntu Server

   Use Case: Collects logs and monitors agents (e.g., Ubuntu/Kali) for security events, rule-based alerts, file integrity monitoring.

   Components Installed: Wazuh Manager

   Network Mode: Host-only (for isolated testing) or Bridged (for real traffic)

5. Ubuntu Linux (Client VM)
   Purpose: General-purpose target system

   Use Case: Simulates a real user workstation or server. Can be configured as a Wazuh agent or hardening practice target.

   Additions: OpenSSH, UFW, Apache2

   Network Mode: Host-only / Bridged

   Network Configuration
   Host-Only Network: Used to ensure all VM traffic remains isolated from the public internet. Ideal for testing exploits and payloads.

   Bridged Network (optional): Used for update access or communication with host when needed.

   Custom Static IPs: Assigned to VMs for easy identification and consistent testing.



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
