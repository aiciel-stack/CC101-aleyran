
# Cloud Infrastructure Components

This document identifies and explains the major infrastructure components observed in the Linux environment provided by the KillerCoda Playground, based on the investigation conducted in `infrastructure-report.md`.

---

## 1. Compute Resources

**What it is in this environment:**
The compute resource is the virtual machine itself — a single-vCPU instance running an Intel Xeon E312xx (Sandy Bridge) processor, virtualized under a KVM hypervisor.

**Purpose:**
Compute resources provide the processing power needed to execute programs, run operating systems, and handle application workloads. In this environment, the single vCPU handles everything from running the shell to executing the Linux commands used in this investigation.

**Why it matters in cloud computing:**
Compute is the foundation of any cloud service — it's what customers actually pay for and scale up or down based on demand (e.g., adding more vCPUs or provisioning additional instances during high traffic). Cloud providers abstract physical hardware into virtual compute units so multiple customers can share the same physical server safely and efficiently.

**Relation to KillerCoda:**
KillerCoda itself is a great example of compute virtualization — it provisions a lightweight, temporary VM (this one running under KVM) that behaves like a full Linux server, without the user ever touching physical hardware.

---

## 2. Storage Resources

**What it is in this environment:**
The primary storage is the `/dev/vda1` virtual disk (19G, ext4), mounted as the root filesystem, along with `/dev/vda16` (`/boot`) and `/dev/vda15` (`/boot/efi`).

**Purpose:**
Storage resources persist data — the operating system files, logs, user files, and any application data — even when the compute instance is powered off or restarted (session-dependent in KillerCoda's case).

**Why it matters in cloud computing:**
Storage is a distinct, separately billed and scaled resource in the cloud (e.g., AWS EBS, Azure Managed Disks). Decoupling storage from compute lets cloud architects resize disks, take snapshots, or move storage between instances without touching the compute layer.

**Relation to KillerCoda:**
The `vda` virtual disks are a textbook example of block storage — device names prefixed with `vd` indicate they're virtual disks presented by the KVM hypervisor to the guest OS, not physical drives.

---

## 3. Networking Resources

**What it is in this environment:**
The environment has three network interfaces: `lo` (loopback), `enp1s0` (the active interface with IP `172.30.1.2/24`), and `docker0` (a bridge interface, currently down).

**Purpose:**
Networking resources allow the compute instance to communicate — with other machines, the internet, or other containers/services running locally (like Docker).

**Why it matters in cloud computing:**
Networking defines how cloud resources are reached and secured. Cloud providers use virtual networks, subnets, and firewalls (security groups) to control traffic between instances and the outside world — critical for both connectivity and security.

**Relation to KillerCoda:**
The `enp1s0` interface represents the VM's virtual NIC assigned by the hypervisor, while `docker0` shows that the environment is also container-aware, hinting at how cloud environments often run nested virtualization (containers inside VMs).

---

## 4. Operating System

**What it is in this environment:**
Ubuntu 24.04.4 LTS (Noble Numbat), kernel version 6.8.0-138-generic.

**Purpose:**
The operating system manages hardware resources (CPU, memory, disk, network) and provides the interface (shell, filesystem, process management) through which users and applications interact with the compute resource.

**Why it matters in cloud computing:**
The OS is the layer where most configuration, security patching, and software installation happens. Cloud providers often offer OS images (AMIs, VM images) so customers can quickly launch instances with a pre-configured OS.

**Relation to KillerCoda:**
KillerCoda provisions a fresh Ubuntu LTS image for each session — LTS (Long Term Support) versions are commonly used in cloud environments because of their stability and extended security support.

---

## Summary

| Component | Example in this Environment | Cloud Computing Role |
|---|---|---|
| Compute | Single vCPU (KVM-virtualized Xeon) | Runs processing workloads |
| Storage | /dev/vda1, /dev/vda15, /dev/vda16 | Persists data independently of compute |
| Networking | enp1s0, docker0, lo | Connects instance to other systems/internet |
| Operating System | Ubuntu 24.04.4 LTS | Manages and exposes hardware resources |
