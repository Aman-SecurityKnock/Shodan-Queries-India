# 🔍 Shodan Queries Focused on India 🇮🇳

> A curated collection of **Shodan search queries** to explore exposed devices and services **specifically in India**, categorized by device type with clear explanations and use cases.

---

## 📁 Table of Contents

- [🛠️ Industrial Control Systems](#industrial-control-systems)
- [🖥️ Remote Desktop & Admin Panels](#remote-desktop--admin-panels)
- [🌐 Network Infrastructure](#network-infrastructure)
- [🗄️ Network Attached Storage (NAS)](#network-attached-storage-nas)
- [📷 Webcams & IP Cameras](#webcams--ip-cameras)
- [🖨️ Printers & Copiers](#printers--copiers)
- [🏠 Smart Home & IoT Devices](#smart-home--iot-devices)
- [🎲 Random & Interesting Services](#random--interesting-services)
- [⚙️ Tools & Resources](#tools--resources)

---

## 🛠️ Industrial Control Systems

| Protocol / Vendor        | Shodan Query |
|--------------------------|--------------|
| Modbus Devices           | `port:502 country:IN` |
| Siemens S7               | `port:102 "siemens" country:IN` |
| BACnet Systems           | `port:47808 country:IN` |
| Schneider Electric HMI   | `"Schneider Electric" country:IN` |
| DNP3 Protocol            | `port:20000 country:IN` |

> **Use Case**: Track down unsecured ICS/SCADA systems used in infrastructure.

---

## 🖥️ Remote Desktop & Admin Panels

| Service          | Shodan Query |
|------------------|--------------|
| RDP (Windows)    | `port:3389 country:IN` |
| VNC (No Auth)    | `port:5900 "RFB" country:IN` |
| TeamViewer       | `"TeamViewer" country:IN` |
| AnyDesk          | `"AnyDesk" country:IN` |
| Mikrotik Winbox  | `port:8291 country:IN` |

> **Use Case**: Identify exposed remote access points.

---

## 🌐 Network Infrastructure

| Device / Brand       | Shodan Query |
|----------------------|--------------|
| Cisco Devices        | `"cisco" port:23 country:IN` |
| MikroTik Routers     | `"MikroTik" country:IN` |
| Ubiquiti Devices     | `"UBNT" country:IN` |
| Fortinet Firewall    | `"FortiGate" country:IN` |

> **Use Case**: Discover internet-facing network gear.

---

## 🗄️ Network Attached Storage (NAS)

| Brand         | Shodan Query |
|---------------|--------------|
| QNAP          | `"QNAP Turbo NAS" country:IN` |
| Synology      | `"Synology DiskStation" country:IN` |
| WD My Cloud   | `"My Cloud" country:IN` |
| Seagate       | `"Seagate NAS" country:IN` |

> **Use Case**: Explore personal and enterprise storage exposed online.

---

## 📷 Webcams & IP Cameras

| Brand / Type   | Shodan Query |
|----------------|--------------|
| Generic IP Cams | `has_screenshot:true port:554 country:IN` |
| Hikvision       | `"Hikvision" country:IN` |
| Dahua           | `"Dahua" country:IN` |
| Axis            | `"AXIS" country:IN` |

> **Use Case**: Identify open surveillance cameras.

---

## 🖨️ Printers & Copiers

| Type       | Shodan Query |
|------------|--------------|
| HP LaserJet| `"HP LaserJet" country:IN` |
| Brother    | `"Brother" country:IN` |
| Canon      | `"Canon printer" country:IN` |
| Raw Port   | `port:9100 country:IN` |

> **Use Case**: See office devices unintentionally exposed online.

---

## 🏠 Smart Home & IoT Devices

| Device / Protocol    | Shodan Query |
|----------------------|--------------|
| Home Assistant       | `"Home Assistant" country:IN` |
| Chromecast           | `"Chromecast" country:IN` |
| MQTT Devices         | `port:1883 country:IN` |
| WebOS TVs            | `"webOS" country:IN` |
| TP-Link Routers      | `"TP-LINK" country:IN` |

> **Use Case**: Find smart home systems that could be misconfigured.

---

## 🎲 Random & Interesting Services

| Service / Tech         | Shodan Query |
|------------------------|--------------|
| Jenkins CI             | `"X-Jenkins" country:IN` |
| GitLab Login           | `"GitLab" port:443 country:IN` |
| Kibana Dashboard       | `"kibana" port:5601 country:IN` |
| MongoDB Open Access    | `port:27017 country:IN` |
| Redis DB (No Auth)     | `port:6379 country:IN` |
| Docker API             | `port:2375 country:IN` |

> **Use Case**: Exposed DevOps tools & backends.

---

## ⚙️ Tools & Resources

- [Shodan](https://www.shodan.io/)
- [Censys](https://censys.io/)
- [Fofa](https://fofa.info/)
- [Nmap](https://nmap.org/)
- [GreyNoise](https://www.greynoise.io/)

---

## ⚠️ Disclaimer

> This repository is for **educational and ethical research** only.  
> Do **not** use these queries for unauthorized access. Always ensure you have **permission** before scanning or probing any network or device.
