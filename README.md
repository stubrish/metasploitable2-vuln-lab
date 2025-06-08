
# Metasploitable2-vuln-lab

Metasploitable2 Vulnerable Lab is designed to show how one can detect and attack common vulnerabilities in Metasploitable 2. The lab deals with testing different open ports and services, which helps learners recognize real attacks and become better ethical hackers. 



## Lab Setup & Configuration

To get started with the Metasploitable2 Vulnerable Lab, make sure you have the following:

- **Metasploitable 2 VM**: Download and import the Metasploitable 2 virtual machine from the official source.
- **Penetration Testing Platform**: Kali Linux (recommended) or other security-focused distros like Parrot OS, BlackArch, or custom setups with Metasploit Framework, Nmap, Burp Suite, and other essential pentesting tools.
- **Network Configuration**: Ensure both your attacker machine (Kali) and Metasploitable 2 VM are on the same network or subnet for connectivity.
- **Basic Tools Installed**:
  - Nmap (for port scanning)
  - Metasploit Framework (for exploiting vulnerabilities)
  - Other tools like Hydra, Netcat, or Wireshark as needed.
- **Virtualization Software**: Such as VMware Workstation, VirtualBox, or any compatible hypervisor.


## Port Scanning

To begin the assessment, a thorough port scan was performed on the Metasploitable 2 target using the following Nmap command:

```bash
nmap -sV --version-all -O -sS -p- -T4 <target-ip>
```
This Nmap command is used to perform a detailed scan of the target machine to discover open ports, running services, and the operating system. Here's what each option means:

- `-sV`: Detects the version of services running on open ports.  
- `--version-all`: Requests a thorough version detection for more accurate results.  
- `-O`: Enables operating system detection.  
- `-sS`: Performs a stealthy TCP SYN scan to quickly find open ports without completing the TCP handshake.  
- `-p-`: Scans all 65,535 TCP ports instead of the default top 1,000 ports.  
- `-T4`: Uses a faster timing template for quicker scan execution while maintaining accuracy.
