# Homelab

A self-hosted homelab built for hands-on learning in 
IT infrastructure, systems administration, and cybersecurity.

---

## Hardware

| Component | Spec |
|-----------|------|
| CPU | Intel i5-8600K |
| RAM | 16GB DDR4 |
| Storage | 1TB NVMe (OS), 1TB HDD (data) |
| GPU | NVIDIA GTX 1070 Ti |
| OS | Ubuntu Server 24.04 LTS |
| Network | Gigabit Ethernet (static IP) |

---

## Current Stack

| Service | Purpose | Status |
|---------|---------|--------|
| Docker + Docker Compose | Container orchestration | ✅ Running |
| Portainer | Container management UI | ✅ Running |
| UFW | Host firewall (default deny) | ✅ Running |

---

## Infrastructure Decisions

**Static IP** — Assigned a static IP via Netplan to ensure 
services and SSH access remain stable across reboots.

**SSH Key Authentication** — Password authentication not used. 
Access requires a private key, eliminating brute force 
vulnerability on port 22.

**Firewall Policy** — UFW configured with default deny on 
incoming traffic. Only ports 22 (SSH) and 9443 (Portainer 
HTTPS) explicitly allowed. Defense in depth: UFW and SSH 
key auth operate as independent security layers.

---

## Roadmap

- [ ] Network-level ad blocking and DNS control (Pihole)
- [ ] System monitoring and dashboards (Prometheus + Grafana)
- [ ] Self-hosted cloud storage (Nextcloud)
- [ ] Intrusion detection and SIEM (Wazuh)
- [ ] Local AI model hosting (Ollama)

---

## Skills Demonstrated

`Linux` `Ubuntu Server` `SSH` `Docker` `Docker Compose`
`Containerization` `UFW` `Firewall Configuration`
`Netplan` `Static Networking` `Defense in Depth`

---

## Notes

Detailed learning notes, decision logs, and troubleshooting 
records are maintained in a private Obsidian vault. 
This repo documents the infrastructure and reasoning 
behind each decision.