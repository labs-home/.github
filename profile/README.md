<h1 align=center> Foggy's Homelab</h1>
<div align="center">
    <a href="https://github.com/foggy-j" target="_blank"><img src="https://img.shields.io/badge/Personal%20GitHub-gray?style=for-the-badge&logo=github" alt="LinkedIn"></a>&nbsp
    <a href="https://www.linkedin.com/in/jake-l-fogden/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge" alt="LinkedIn"></a>&nbsp
    <a href="mailto:jakelfogden@outlook.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=maildotru&logoColor=white" alt="Email"></a>
</div>

### Includes Terraform, Ansible and base configuration files for my personal Homelab.

## Why is my Homelab public?
There are a number of reasons as to why my Homelab is public, the first and primary reason is to present the methods I am using for managing my Homelab, and providing insight for those who are seeking inspiration for there own Homelabs. I also use this to showcase my skills for job interviews and on my CV.

## How can these files be utilised by others?
Whilst some of the files located in these repos are aligned for my own Homelab, there are README's in many of the directories that covers various pieces of information, including what can be adapted so others can use the code but with their own Homelabs.

## Featured Tools
**The tools mentioned below are some that are used in a number of the repos to perform various actions:**
- **Terraform** - IaC tool to apply configuration for services such as Cloudflare, Proxmox etc.
- **Ansible** - IaC tool to provision configuration for hosts.
- **Taskfile** - Alternative to Makefile which simplifies execution of tasks.
- **GitHub** Actions - CI/CD tool that I use for testing and applying configuration.
- **Discord** - All Homelab and GitHub repo events send notifications to a private Discord server.

## Homelab Architecture
```
┳ Core-FW (Proxmox)
┣━ OPNSense
┣━ Bind9 DNS
┣━ Unifi Controller
┣━ External-facing Bastion Host
┣━ IPAM
┣━ Home Assistant
┣━ Monitoring Stack (Grafana, Prometheus, InfluxDB)
┗━ Adguard

┳ Tools-Mini (Debian)
┗━ GitHub Runner (Provisioning)

┳ UPS-Man (RPi - Alpine)
┗━ NUT (Network UPS Tools)

┳ Prmx-mini-1 (Proxmox)
┣━ Kubernetes (Master & Worker)
┗━ Kubernetes (Staging Environment)

┳ Prmx-mini-2 (Proxmox)
┣━ Kubernetes (Master & Worker)
┗━ Development Nodes

┳ Prmx-mini-3 (Proxmox)
┣━ Kubernetes (Master & Worker)
┣━ Misc. Hosting
┗━ Game Servers

┳ TrueNAS
┣━ Media Storage
┣━ Backups
┗━ Proxmox ISO Store
```