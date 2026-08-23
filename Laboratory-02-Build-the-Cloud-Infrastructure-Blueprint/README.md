# Laboratory Activity 2: Build the Cloud Infrastructure Blueprint

## Mission Overview
This laboratory activity simulates the planning phase of a cloud deployment for a fictional company, CloudNova Technologies. The mission was to investigate a Linux server environment (provided via KillerCoda), identify its infrastructure components, compare major public cloud providers, and produce professional technical documentation as if preparing a report for a client.

## Objectives
- Explain the major components of cloud infrastructure.
- Investigate the hardware and software resources available in a Linux environment.
- Differentiate compute, storage, networking, and identity resources.
- Interpret the relationship between cloud infrastructure components.
- Create professional technical documentation using Markdown.
- Continue building a structured GitHub Cloud Computing Portfolio.

## Cloud Infrastructure Components
- **Compute** — the virtual machine (single vCPU, Intel Xeon E312xx under KVM) that runs the OS and processes.
- **Storage** — the virtual disks (`/dev/vda1`, `/dev/vda15`, `/dev/vda16`) that persist data.
- **Networking** — the interfaces (`enp1s0`, `docker0`, `lo`) that connect the instance to other systems.
- **Operating System** — Ubuntu 24.04.4 LTS, managing all of the above.

Full details are documented in `infrastructure-report.md` and `cloud-components.md`.

## Tools Used
- KillerCoda Playground (Linux terminal environment)
- Git and GitHub (version control and portfolio hosting)
- Markdown (technical documentation)
- Draw.io (cloud architecture diagram)

## Linux Commands Executed
```
cat /etc/os-release
uname -r
lscpu
nproc
hostname
ip a
hostname -I
free -h
df -h
mount | grep -E "^/dev"
```

## Skills Learned
- Investigating a Linux server's hardware and software specifications from the command line.
- Differentiating compute, storage, and networking resources in a real environment.
- Comparing equivalent services across AWS, Microsoft Azure, and Google Cloud Platform.
- Writing structured technical documentation using Markdown.
- Resolving Git conflicts and pushing organized commits to a GitHub portfolio.

## Challenges Encountered
Initial `git push` attempts were rejected because the local repository's history didn't match the remote (since some files were created directly through GitHub's web interface). This was resolved by configuring git identity and pulling remote changes before pushing again. Reading detailed terminal output (like `lscpu`) also required care to correctly extract accurate CPU and virtualization details.
