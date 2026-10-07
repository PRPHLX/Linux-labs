# Linux Labs

Hands-on Linux administration labs built in my Proxmox home lab. Each lab starts from a real task, documents the steps and the verification, and includes the mistakes and unexpected results I ran into.

## Labs

| Lab | Topic | Highlights |
|---|---|---|
| [Lab 01](Lab01-Ubuntu-Server-Setup/) | Ubuntu Server setup | Checksum-verified ISO, static IP, DNS on the AD domain controller, updates, QEMU guest agent, NTP |
| [Lab 02](Lab02-SSH-Hardening/) | SSH hardening | Host key verification, Ed25519 keys, passwords disabled, the `50-cloud-init.conf` precedence trap |
| [Lab 03](Lab03-Firewall-UFW/) | Firewall with UFW | Default deny, SSH limited to the LAN, closed vs filtered ports, reading block logs |
| [Lab 04](Lab04-Users-Permissions-Sudo/) | Users, permissions and sudo | Department groups, setgid, default ACLs, least-privilege sudo, a sudo-rs audit gap |
| [Lab 05](Lab05-Incident-Disk-Full/) | Incident: disk full | Diagnosis with `du`, online LVM extension with `lvextend` and `resize2fs`, root cause |

## Lab environment

| Component | Details |
|---|---|
| Hypervisor | Proxmox VE on a Dell OptiPlex 7060 (i5-8500, 24 GB RAM) |
| Linux server | LNX01 - Ubuntu Server 26.04.1 LTS, 192.168.100.20 |
| Domain controller / DNS | DC01 - Windows Server 2022, domain `homelab.local`, 192.168.100.10 |
| Admin workstation | Windows 11 desktop with PowerShell 7 and the OpenSSH client |
| Network | 192.168.100.0/24 behind a TP-Link TL-SG108PE managed switch |

## Skills practiced

- Linux server installation and post-install verification
- Networking: static IP, DNS, layered troubleshooting, TTL and TCP behavior
- SSH key authentication and server hardening
- Host firewall configuration and log analysis
- Users, groups, file permissions, ACLs and sudo delegation
- LVM storage management and incident response

## How these labs were built

These labs were built with guidance from documentation and AI-assisted troubleshooting. Every command was typed, executed and verified by me on my own hardware. Mistakes and results that did not match my expectations are documented in each lab.

## Related repositories

- [Windows-AD-labs](https://github.com/PRPHLX/Windows-AD-labs)
- [Networking-labs](https://github.com/PRPHLX/Networking-labs)
