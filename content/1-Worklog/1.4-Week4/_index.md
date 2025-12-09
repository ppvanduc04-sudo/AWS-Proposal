---
title: "Week 4 Worklog"
date: "2025-09-29"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

## 🎯 Week 4 Objectives

- Install, configure, and deploy a site-to-site VPN on Linux 2023.  
- Migrate from **Openswan** to **Libreswan** due to incompatibility issues with Linux 2023.  
- Understand the mechanisms of **IPsec**, **IKEv1/v2**, **DPD**, and how to validate VPN status.  

---

## 🗂 Tasks Implemented During the Week

| Day | Tasks | Start Date | End Date | Documentation |
| --- | ----- | ----------- | -------- | -------------- |
| **2** | - Checked the status of Openswan on Linux 2023.<br>- Used diagnostic commands: `ipsec verify`, `ipsec whack --status`.<br>- Identified the root cause of IPsec service failing to start. | 01/10/2025 | 01/10/2025 | Openswan docs, Linux man pages |
| **3** | - Analyzed Pluto & systemd logs using: `journalctl -xeu ipsec.service`.<br>- Identified errors: Pluto daemon not running and missing control file `/run/pluto/pluto.ctl`. | 02/10/2025 | 02/10/2025 | Linux systemd docs |
| **4** | - Concluded that Openswan is incompatible with Linux 2023.<br>- Decided to migrate to **Libreswan 4.12**.<br>- Backed up existing configs: `/etc/ipsec.conf` and `/etc/ipsec.d/*`. | 03/10/2025 | 03/10/2025 | Libreswan official docs |
| **5** | - Installed Libreswan on Linux 2023.<br>- Created new configuration files: `/etc/ipsec.conf` and `/etc/ipsec.secrets`.<br>- Configured the site-to-site VPN tunnel (Tunnel2) with correct local/remote IPs and pre-shared key. | 04/10/2025 | 04/10/2025 | Libreswan docs |
| **6** | - Validated configuration using: `ipsec validate` and `ipsec auto --check`.<br>- Restarted IPsec service: `systemctl restart ipsec`.<br>- Checked IKE/SA states via: `ipsec whack --status`. | 05/10/2025 | 05/10/2025 | Linux man pages |
| **7** | - Configured system-level settings for VPN:<br>&emsp;+ Enabled IP forwarding<br>&emsp;+ Allowed UDP 500 & 4500 in firewall<br>- Performed routing checks and initial tunnel testing. | 06/10/2025 | 07/10/2025 | Linux networking docs, AWS docs |

---

## ✅ Week 4 Achievements

### 1. Successful Migration from Openswan to Libreswan 4.12
- Openswan 2.6.x failed to start on Linux 2023 due to kernel incompatibility.  
- Libreswan 4.12 was successfully installed and is running stably.  
- New configuration files were created using modern Libreswan syntax.  

### 2. Site-to-Site VPN Configured Successfully
- Tunnel **Tunnel2** was configured with correct technical parameters:  
  - Local IP  
  - Remote IP  
  - Pre-shared key  
  - Phase 1 & Phase 2 algorithms  
- Pluto service is now running without socket or daemon startup errors.  

### 3. Strengthened Understanding of IPsec and Related Components
- Gained deeper knowledge of:  
  - **IKE (Internet Key Exchange)**  
  - **IPsec ESP/AH**  
  - **DPD (Dead Peer Detection)**  
  - Phase 1 negotiation: AES256 / SHA1 / MODP1024  
  - Phase 2 negotiation: AES128 / SHA1 / MODP1024  


### 4. Mastered Key Commands for VPN Monitoring & Maintenance
- `ipsec whack --status` –
