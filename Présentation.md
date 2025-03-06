# Présentation du projet

### Participant: Rodney NGUEMA William Krommer Mathéo Maussantos

## Projet choisit  : Routeur vpn 

Ce projet a pour but de réaliser un routeur et un VPN sur un support comme une machine virtuelle, en s'appuyant sur les connaissances acquises en cours de réseau.

Nous utiliseront Rocky linux et Unbuntu 


---

## 🌐 Configuration réseau

### Rocky Linux (Routeur)
| Interface | Type         | Adresse IP          |
|---------|-------------|-----------------|
| enp0s3 | NAT         | DHCP (10.0.2.15) |
| enp0s8 | Réseau interne | 192.168.100.1 |
| enp0s9 | Host-only (vboxnet0) | 192.168.56.2 |

---

### Ubuntu (Client)
| Interface | Type           | Adresse IP         |
|---------|--------------|----------------|
| enp0s3 | Réseau interne | 192.168.100.2 |

---