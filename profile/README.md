<h1 align=center> Foggy's Homelab</h1>
<div align="center">
    <a href="https://www.linkedin.com/in/jake-l-fogden/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?&style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>&nbsp
    <a href="mailto:jakelfogden@outlook.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
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
┣━ IPAM
┣━ Core GitHub Runner (K3s)
┣━ Rancher (Kubernetes cluster management)
┣━ Monitoring Stack (Grafana, Prometheus, InfluxDB)
┗━ Adguard

┳ UPS-Man (RPi - Alpine)
┗━ NUT (Network UPS Tools)

┳ Prmx-mini-1 (Proxmox)
┣━ Kubernetes (Master)
┣━ Kubernetes (Worker)
┣━ Home Assistant
┗━ External-facing Bastion Host

┳ Prmx-mini-2 (Proxmox)
┣━ Kubernetes (Master)
┣━ Kubernetes (Worker)
┣━ Development Nodes
┗━ streamrecorder.io Node

┳ Prmx-mini-3 (Proxmox)
┣━ Kubernetes (Master)
┣━ Kubernetes (Worker)
┣━ Misc. Hosting
┗━ Game Servers

┳ TrueNAS
┣━ Media Storage
┣━ Backups
┗━ Proxmox ISO Store
```