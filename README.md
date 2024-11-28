# AttackerDefenderHomeLab
This is a straightforward home lab designed for beginners in cybersecurity to explore and experiment with various Kali Linux tools. It offers a hands-on approach to learning about these powerful applications. The setup is easy and requires just a home workstation or laptop, along with Kali Linux and Metasploitable 2.

## Introduction
This project demonstrates an attacker-defender lab setup for learning and showcasing penetration testing and network security skills. The lab uses:

- **Kali Linux**: As the attacker machine, equipped with tools for scanning, enumeration, and exploitation.
- **Metasploitable2**: As the intentionally vulnerable target machine for ethical hacking.
- **Wireshark**: For network traffic monitoring. (Optional)

The lab is designed to simulate real-world attack scenarios and defensive countermeasures in a safe and controlled environment. As long as the VM's are configured correctly, and you save a snapshot after you configure it then you will be fine. 

To set up these VM's follow this guide: 
https://www.youtube.com/watch?v=yf3jetn4tN8 (Make sure to set the network type to "Bridged Adapater") 

## Architecture
The lab operates on a **bridged network** configuration where the virtual machines and host machine share the same network segment. Below is an overview of the setup:

- **Router**: (192.168.1.1)
- **Host Machine**: (192.168.1.100) - Manages the lab and monitors traffic using Wireshark.
- **Kali Linux**: (192.168.1.101) - Performs scanning, exploitation, and brute-force attacks.
- **Metasploitable2**: (192.168.1.102) - Acts as the vulnerable system.

## Tools and Techniques
### Kali Linux (Attacker)
- **Tools Used**:
  - `nmap`: Network scanning and enumeration.
  - `Metasploit`: Exploitation framework for vulnerabilities.
  - `Hydra`: Password brute-forcing.
  - `Netcat`: Network interaction and exploitation.

### Metasploitable2 (Target)
- **Key Vulnerabilities**:
  - Open ports and services (FTP, SSH, HTTP, MySQL).
  - Weak credentials on critical services.
  - Unpatched vulnerabilities in Apache and MySQL.

### Host Machine
- **Monitoring**:
  - `Wireshark`: Captures and analyzes network traffic between the attacker and target.
