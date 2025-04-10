# VMLab
Deployed Windows 10 VM in Azure, used Event Viewer, Log Analytics, and Microsoft Sentinel to analyze logs and build attack map.
# Azure Honeypot & Log Analysis Lab

This project demonstrates the creation of a honeypot using a Windows 10 Virtual Machine in Microsoft Azure, followed by log collection, analysis, and visualization using Event Viewer, Log Analytics Workspace, and Microsoft Sentinel.

## Lab Overview

### Part 1: Create the Honeypot (Azure VM)
- Deployed a **Windows 10 VM** on [Azure Portal](https://portal.azure.com)
- Configured **Network Security Group (NSG)** to allow all inbound traffic
- Disabled **Windows Firewall** on the VM to simulate a vulnerable system

### Part 2: Log Generation & Inspection
- Simulated brute force attack by failing 3 login attempts as a fake user (`employee`)
- Used **Event Viewer** to identify and verify failed login events (Event ID: 4625)

### Part 3: Log Forwarding and Centralized Monitoring
- Created a **Log Analytics Workspace (LAW)**
- Connected a **Microsoft Sentinel** instance to LAW
- Configured the **Windows Security Events via AMA** connector
- Used **Kusto Query Language (KQL)** to query security logs

### Part 4: Log Enrichment with IP Geolocation
- Imported a custom IP geolocation watchlist (`geoip-summarized.csv`) into Sentinel
- Enriched log data by mapping IP addresses to geographic locations using KQL and watchlist data

### Part 5: Attack Map Visualization
- Created an **Attack Map Workbook** in Microsoft Sentinel
- Used KQL and custom JSON (`map.json`) to visualize attacker locations on an interactive map

## Technologies Used
- Microsoft Azure
- Windows 10 Virtual Machine
- Network Security Groups (NSG)
- Windows Firewall / Event Viewer
- Log Analytics Workspace (LAW)
- Microsoft Sentinel (SIEM)
- Kusto Query Language (KQL)
- GeoIP Watchlist

## Key Skills Demonstrated
- Cloud Security & Infrastructure Setup
- Log Analysis and Threat Detection
- SIEM Configuration and Data Integration
- Data Enrichment and Visualization using KQL

## Resources
- [Azure Portal](https://portal.azure.com)
- [KQL Learning](https://kc7cyber.com/)
- [Cyber Range Environment](https://skool.com/cyber-range)

---

> 🚨 **Note:** Be mindful of VM runtime costs in Azure. Always stop or delete resources after use if not using a Cyber Range environment.
