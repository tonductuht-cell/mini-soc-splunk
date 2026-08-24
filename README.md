# Mini SOC Lab with Splunk

A hands-on SOC monitoring project built with Splunk Enterprise on macOS and Kali Linux. This lab centralizes authentication, Nmap, and privileged activity logs, then uses SPL to detect SSH brute-force attacks, network scanning, and suspicious sudo activity through a security dashboard.

## Architure
Kali Linux
 ├── auth.log
 └── nmap.log
        │
        ▼
Splunk Universal Forwarder
        │
        ▼
Splunk Enterprise
        │
        ▼
Index: soc_lab

## Detection rule
| Detection | Description |
|-----------|-------------|
| SSH Brute Force | Multiple failed SSH logins from one IP |
| Network Scanning | Analysis of Nmap scan results |
| Privileged Activity | Monitoring sudo commands executed as root |

## Dashboard
Include screenshots in the `images/` folder.

## Technologies
- Splunk Enterprise
- Splunk Universal Forwarder
- Kali Linux
- SPL (Search Processing Language)
