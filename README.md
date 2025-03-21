# Présentation du projet

### Participants:
- Rodney NGUEMA
- William Krommer
- Mathéo Maussantos

## Projet choisi : Routeur, VPN

Ce projet a pour but de réaliser un **routeur avec différentes fonctionnalités tel que : vpn, firewall, dhcp** à l'aide de machines virtuelle. Nous utiliserons deux machines sous  **Rocky Linux** qui nous servirons respectivement de  serveur VPN et de routeur et des machines sous **Ubuntu** qui nous ser client VPN.

---

# 🌐 Configuration réseau

## **Rocky Linux (Routeur VPN)**

| Interface | Type               | Adresse IP         | Description                              |
|-----------|--------------------|--------------------|------------------------------------------|
| enp0s3    | NAT                | DHCP (10.0.2.15)   | Interface réseau NAT pour la connectivité avec l'extérieur (Internet). |
| enp0s8    | Réseau interne     | 192.168.100.1      | Interface réseau interne pour la communication avec le réseau local (client Ubuntu). |
| enp0s9    | Host-only (vboxnet0) | 192.168.56.2      | Interface en mode "host-only" pour la communication avec l'hôte de la machine virtuelle. |

---

## **Ubuntu (Client 1)**

| Interface | Type               | Adresse IP         | Description                              |
|-----------|--------------------|--------------------|------------------------------------------|
| enp0s3    | Réseau interne     | 10.5.1.150         | Interface réseau interne pour la communication avec le routeur VPN (Rocky Linux). |

---

## **Ubuntu (Client )**

| Interface | Type               | Adresse IP         | Description                              |
|-----------|--------------------|--------------------|------------------------------------------|
| enp0s3    | Réseau interne     | 10.5.1.151         | Interface réseau interne pour la communication avec le routeur VPN (Rocky Linux). |

---

## **Serveur VPN (Rocky Linux avec WireGuard)**

| Interface | Type               | Adresse IP         | Description                              |
|-----------|--------------------|--------------------|------------------------------------------|
| enp0s3    | Réseau local (DHCP) | 10.5.1.177/24      | Interface réseau pour la communication avec le réseau interne ou externe. |
| wg0       | VPN                | 10.255.255.1/24    | Interface WireGuard pour gérer la connexion VPN. |

---

# 📊 Pour lancer la prise de métriques sur le VPN avec **Node Exporter** :

```bash
[root@vpn node_exporter-1.3.1.linux-amd64]# ./node_exporter &
```


