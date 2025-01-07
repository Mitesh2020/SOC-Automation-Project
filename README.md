# SOC Automation Project
This project automates SOC workflows using open-source tools like Wazuh, Shuffle, and TheHive. It aims to streamline event collection, alerting, and incident response to enhance SOC efficiency.

## Project Design
The project integrates multiple tools and systems to automate and enhance SOC operations. Below is the design layout for reference:

![design](https://github.com/user-attachments/assets/d3349ba6-9ddb-4817-894a-0e131a30c6cc)

## System Requirements
To ensure the smooth functioning and optimal performance of the SOC Automation system, the following system requirements must be met:

| Requirement      | Specification                    |
|------------------|----------------------------------|
| **Storage**      | 150 GB (SSD Recommended)        |
| **RAM**          | 32 GB (Cloud PC Recommended for < 32 GB RAM) |
| **OS**           | Windows 11 (Primary)            |

## Software/Tools Usage

| Name                       | Usage                                                                 |
|----------------------------|-----------------------------------------------------------------------|
| **VMware/VirtualBox**      | Virtualization software for creating and managing virtual machines.  |
| **Windows 11**             | Primary operating system serving as the Wazuh agent host.            |
| **Ubuntu Server 22.04**    | Lightweight OS for hosting Wazuh and TheHive on separate VMs.        |
| **Sysmon**                 | Windows system monitor for detailed logging of process activities.   |
| **Mimikatz**               | Penetration testing tool to simulate security breaches.              |
| **SquareX**                | Browser extension for disposable email usage.                        |
| **Draw.io**                | Tool for creating project architecture and design diagrams.          |
| **Wazuh Manager**          | Centralized agent-based monitoring and analysis solution.            |
| **Wazuh Dashboard**        | Visualization and management interface for Wazuh.                   |
| **Wazuh Indexer**          | Backend storage and search engine for Wazuh.                        |
| **TheHive**                | Incident response platform for managing alerts and cases.            |
| **Cassandra**              | Database used as a backend for TheHive.                             |
| **Elasticsearch**          | Search engine for indexing and querying TheHive data.               |
| **VirusTotal**             | Online file and URL analysis service for threat detection.          |
| **Ngrok**                  | Port forwarding to connect local TheHive setup with Shuffle cloud.  |
| **UFW**                    | Firewall configuration to manage network traffic.                   |
| **Shuffler.io**            | Workflow automation platform for SOC processes.                     |

## Project Workflow

1. **Day 1 - Design:**
   - Create a logical diagram of the project using [draw.io](https://app.diagrams.net/).
   - Diagram includes the architecture and flow between Wazuh, TheHive, Shuffle, and email.

2. **Day 2 - Install:**
   - Install Wazuh and TheHive on an Ubuntu Server VM.
   - Set up virtual machines and install the required applications.

3. **Day 3 - Configure:**
   - Configure Wazuh and TheHive servers and endpoints.
   - Ensure both systems are communicating and processing telemetry.

4. **Day 4 - Telemetry:**
   - Generate telemetry using Mimikatz at endpoints.
   - Trigger and ingest telemetry into Wazuh for analysis.

5. **Day 5 - SOAR:**
   - Create an automated workflow between Wazuh, TheHive, Shuffle, and email to notify SOC analysts when alerts are triggered.
   - The workflow will automatically send alerts to TheHive and email them to SOC analysts.


