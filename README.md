# 🌐 FTP Using DNS — Computer Networks Lab (BTCS 606L)

> **Central University of Kashmir** — Department of Information Technology  
> Academic Year: 2025–2026

---

## 📋 Project Overview

This project simulates a **multi-subnet corporate intranet** environment using **Cisco Packet Tracer**.  
It demonstrates Inter-VLAN routing, DNS name resolution, and FTP file transfer across two separate networks.

---

## 🏗️ Network Architecture

| Zone | Subnet | Devices |
|------|--------|---------|
| Staff Zone (Left) | `192.168.1.0/24` | PC1, PC2, Switch0 |
| Server Zone (Right) | `10.0.0.0/8` | FTP Server, DNS Server, Switch1 |
| Gateway | Both | Cisco 2911 Router |

---

## ⚙️ Configuration Summary

### Router (Gateway)
| Interface | IP Address | Network |
|-----------|-----------|---------|
| GigabitEthernet0/0 | `192.168.1.1` | Staff Zone |
| GigabitEthernet0/1 | `10.0.0.1` | Server Zone |

### Servers
| Server | IP Address | Service |
|--------|-----------|---------|
| FTP Server | `10.0.0.2` | FTP (user: `student` / pass: `cisco123`) |
| DNS Server | `10.0.0.3` | DNS → `ftp.nanna.com` maps to `10.0.0.2` |

### Client PCs
| Device | IP Address | Gateway | DNS |
|--------|-----------|---------|-----|
| PC1 | `192.168.1.10` | `192.168.1.1` | `10.0.0.3` |
| PC2 | `192.168.1.11` | `192.168.1.1` | `10.0.0.3` |

---

## 🧪 Testing

1. **Ping DNS Server** from PC1: `ping 10.0.0.3`
2. **FTP Upload** from PC1: `ftp ftp.nanna.com` → `put testfile.txt`
3. **FTP Download** from PC2: `ftp ftp.nanna.com` → `get testfile.txt`

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `ftp_using_dns.pkt` | Cisco Packet Tracer simulation file |
| `report/cn_project_report.pdf` | Full lab report with configuration steps |

---

## 👥 Contributors

| Name | Roll No |
|------|---------|
| Mehdi Hafiz | 2324CUKmr21 |
| Owais ul Alam Sofi | 2324CUKmr26 |
| Saliq Naqash | 2324CUKmr29 |
| Seerat Batul | 2324CUKmr32 |

> **Guided by:** Dr. Shahid Sultan
