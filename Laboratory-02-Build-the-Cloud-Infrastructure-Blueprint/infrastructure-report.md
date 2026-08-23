
# Infrastructure Report

## Overview
This report documents the findings from investigating the Linux server environment provided through the KillerCoda Playground, as part of the Cloud Infrastructure Assessment for CloudNova Technologies. Findings are grouped into Server, Network, and Storage information, matching the evidence screenshots in the `screenshots/` folder.

---

## 1. Server Information
**Commands used:** `cat /etc/os-release`, `uname -r`, `lscpu`, `nproc`, `hostname`

| Component | Value |
|---|---|
| Operating System | Ubuntu 24.04.4 LTS (Noble Numbat) |
| Kernel Version | 6.8.0-138-generic |
| CPU Model | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| Architecture | x86_64 |
| CPU Cores | 1 |
| Virtualization | Full (KVM hypervisor) |
| Hostname | ubuntu |

**Screenshot:** `screenshots/server-information.png`

---

## 2. Network Information
**Commands used:** `ip a`, `hostname -I`

| Interface | IP Address | Status |
|---|---|---|
| lo (loopback) | 127.0.0.1/8 | UP |
| enp1s0 | 172.30.1.2/24 | UP |
| docker0 | 172.17.0.1/16 | DOWN (no carrier) |

**Screenshot:** `screenshots/network-information.png`

---

## 3. Storage Information
**Commands used:** `free -h`, `df -h`, `mount | grep -E "^/dev"`

**Memory (RAM):**
| Total | Used | Free | Shared | Buff/Cache | Available |
|---|---|---|---|---|---|
| 1.9Gi | 414Mi | 828Mi | 1.1Mi | 829Mi | 1.5Gi |

**Swap:** 1.0Gi total, 0B used, 1.0Gi free

**Disk Capacity:**
| Filesystem | Size | Used | Available | Use% | Mounted on |
|---|---|---|---|---|---|
| /dev/vda1 | 19G | 5.4G | 13G | 30% | / |
| /dev/vda16 | 881M | 117M | 703M | 15% | /boot |
| /dev/vda15 | 105M | 6.2M | 99M | 6% | /boot/efi |

**Mounted File Systems:**
- /dev/vda1 on / (ext4, rw,relatime,discard,errors=remount-ro,commit=30)
- /dev/vda16 on /boot (ext4, rw,relatime)
- /dev/vda15 on /boot/efi (vfat, rw,relatime,fmask=0077,dmask=0077)

**Screenshot:** `screenshots/storage-information.png`

---

## Notes
This is a single-core, low-memory virtualized Ubuntu environment running under KVM. In a real cloud deployment, this configuration would only suit lightweight testing or a minimal microservice — production workloads would require scaling up CPU cores, RAM, and disk based on expected traffic and demand.
