# 🔍 Shodan Queries Focused on India 🇮🇳

> A curated collection of **Shodan search queries** to explore exposed devices and services **specifically in India**, categorized by device type with clear explanations, advanced filters, and real-world use cases.

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
- [🎯 Advanced Shodan Filters](#advanced-shodan-filters)
- [⚙️ Tools & Resources](#tools--resources)
- [⚠️ Disclaimer](#️disclaimer)

---

## 🛠️ Industrial Control Systems

| System/Protocol            | Shodan Query |
|----------------------------|--------------|
| Modbus Devices             | `port:502 country:IN` |
| Siemens S7 PLC             | `port:102 "siemens" country:IN` |
| BACnet Systems             | `port:47808 country:IN` |
| DNP3 Protocol              | `port:20000 country:IN` |
| Schneider Electric         | `"Schneider Electric" country:IN` |
| Rockwell Automation        | `"rockwellautomation" country:IN` |
| SCADA Panels (Generic)     | `"SCADA" country:IN` |

> 💡 Used in power plants, factories, and critical infrastructure—often misconfigured and exposed.

---

## 🖥️ Remote Desktop & Admin Panels

| Service/Protocol           | Shodan Query |
|----------------------------|--------------|
| Windows RDP                | `port:3389 country:IN` |
| VNC (Unauthenticated)      | `port:5900 "RFB" country:IN` |
| TeamViewer                 | `"TeamViewer" country:IN` |
| AnyDesk                    | `"AnyDesk" country:IN` |
| Mikrotik Winbox            | `port:8291 country:IN` |
| Synology DSM Admin Panel  | `port:5000 country:IN` |
| Remote Desktop (Generic)   | `"Remote Desktop" country:IN` |

> 💡 These can provide full system access if exposed without authentication.

---

## 🌐 Network Infrastructure

| Device/Brand               | Shodan Query |
|----------------------------|--------------|
| Cisco Routers              | `"cisco" port:23 country:IN` |
| MikroTik RouterOS          | `"RouterOS" country:IN` |
| Ubiquiti UniFi             | `"UBNT" country:IN` |
| FortiGate Firewalls        | `"FortiGate" country:IN` |
| Juniper Devices            | `"Juniper" country:IN` |
| Default Gateway Routers    | `http://:.1.1.1.1 country:IN` |

> 💡 Critical network devices often have remote management enabled and rarely updated firmware.

---

## 🗄️ Network Attached Storage (NAS)

| Brand                      | Shodan Query |
|----------------------------|--------------|
| QNAP NAS                   | `"QNAP Turbo NAS" country:IN` |
| Synology DiskStation       | `"Synology DiskStation" country:IN` |
| WD My Cloud                | `"My Cloud" country:IN` |
| Seagate NAS                | `"Seagate NAS" country:IN` |
| Buffalo NAS                | `"Buffalo NAS" country:IN` |
| ASUSTOR NAS                | `"ASUSTOR" country:IN` |
| NAS Devices on Web Port    | `"NAS" port:5000 country:IN` |

> 💡 NAS devices are often left with default credentials and hold critical personal or business data.

---

## 📷 Webcams & IP Cameras

| Camera Type / Brand        | Shodan Query |
|----------------------------|--------------|
| Open RTSP Cameras          | `has_screenshot:true port:554 country:IN` |
| Hikvision IP Cameras       | `"Hikvision" country:IN` |
| Dahua Cameras              | `"Dahua" country:IN` |
| Axis Cameras               | `"AXIS" country:IN` |
| WebcamXP                   | `"webcamXP" country:IN` |
| CGI-Based IP Cams          | `"webcam.cgi" country:IN` |
| Axis Media Streams         | `"Axis Media" country:IN` |

> 💡 Many camera models expose a live feed or snapshot due to weak or missing authentication.

---

## 🖨️ Printers & Copiers

| Device Type / Brand        | Shodan Query |
|----------------------------|--------------|
| HP Printers (JetDirect)    | `"HP LaserJet" country:IN` |
| Brother Printers           | `"Brother Web" country:IN` |
| Canon Printers             | `"Canon printer" country:IN` |
| IPP (CUPS Printers)        | `port:631 country:IN` |
| Port 9100 (Raw printing)   | `port:9100 country:IN` |

> 💡 Network printers are often vulnerable to data leaks, print bombs, or internal recon.

---

## 🏠 Smart Home & IoT Devices

| Device / Platform          | Shodan Query |
|----------------------------|--------------|
| Home Assistant             | `"Home Assistant" country:IN` |
| Chromecast Devices         | `"Chromecast" country:IN` |
| MQTT IoT Devices           | `port:1883 country:IN` |
| LG WebOS Smart TVs         | `"webOS" country:IN` |
| TP-Link Routers            | `"TP-LINK" country:IN` |
| Blynk IoT Dashboards       | `"Blynk" country:IN` |
| ESP IoT Web Servers        | `"ESPWebServer" country:IN` |

> 💡 Smart devices often ship with insecure configurations and are targets for botnets like Mirai.

---

## 🎲 Random & Interesting Services

| Service / Tech             | Shodan Query |
|----------------------------|--------------|
| Jenkins CI Dashboards      | `"X-Jenkins" country:IN` |
| GitLab Login Pages         | `"GitLab" port:443 country:IN` |
| Kibana Dashboards          | `"kibana" port:5601 country:IN` |
| MongoDB (No Auth)          | `port:27017 country:IN` |
| Redis (No Auth)            | `port:6379 country:IN` |
| Docker Daemons             | `port:2375 country:IN` |
| Glances Linux Monitors     | `"glances" country:IN` |
| OctoPrint (3D Printers)    | `"OctoPrint" country:IN` |
| phpMyAdmin Panels          | `"phpMyAdmin" country:IN` |
| OpenVPN Panels             | `"OpenVPN" country:IN` |

> 💡 Exposed devtools, databases, and dashboards are goldmines for attackers—and usually unintended.

---

## 🎯 Advanced Shodan Filters

Use these to **refine** or **geotarget** any of the above queries:

| Filter Type               | Example Query |
|---------------------------|---------------|
| City-specific             | `port:3389 country:IN city:"Mumbai"` |
| ISP/Org-specific          | `port:23 org:"BSNL" country:IN` |
| Screenshot availability   | `has_screenshot:true port:80 country:IN` |
| Software version match    | `port:6379 redis 6.0 country:IN` |

---

## ⚙️ Tools & Resources

- [Shodan.io](https://www.shodan.io/)
- [Censys.io](https://censys.io/)
- [Fofa.info](https://fofa.info/)
- [GreyNoise](https://www.greynoise.io/)
- [Nmap](https://nmap.org/)
- [Project Sonar](https://opendata.rapid7.com/sonar/)

---

## ⚠️ Disclaimer

> This repository is for **educational and ethical research purposes only**.  
> Do **not** use these queries for unauthorized access or illegal activity.  
> Always obtain proper permission before scanning or interacting with third-party systems.

---

### ✨ Want More?

Suggest categories, contribute new queries, or submit PRs!  
This is a growing resource for cybersecurity awareness, OSINT research, and infrastructure visibility in India.
"""
