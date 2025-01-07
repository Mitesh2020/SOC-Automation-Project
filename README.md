# SOC Automation Project
This project automates SOC workflows using open-source tools like Wazuh, Shuffle, and TheHive. It aims to streamline event collection, alerting, and incident response to enhance SOC efficiency.
<br><br><br>
## Project Design
The project integrates multiple tools and systems to automate and enhance SOC operations. Below is the design layout for reference:

![design](https://github.com/user-attachments/assets/d3349ba6-9ddb-4817-894a-0e131a30c6cc)
<br><br><br>
## System Requirements
To ensure the smooth functioning and optimal performance of the SOC Automation system, the following system requirements must be met:

| Requirement      | Specification                    |
|------------------|----------------------------------|
| **Storage**      | 150 GB (SSD Recommended)        |
| **RAM**          | 32 GB (Cloud PC Recommended for < 32 GB RAM) |
| **OS**           | Windows 11 (Primary)            |

<br><br>
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

<br><br>
## Project Workflow

1. **Day 1 - Design:**
   - Create a logical diagram of the project using [draw.io](https://app.diagrams.net/).
   - Diagram includes the architecture and flow between Wazuh, TheHive, Shuffle, and email.
   - [Watch Design Video](https://youtu.be/YxpUx0czgx4?si=Nb7qEI7Mk3_kl01T)

2. **Day 2 - Install:**
   - Install Wazuh and TheHive on an Ubuntu Server VM.
   - Set up virtual machines and install the required applications.
   - [Watch Installation Video](https://youtu.be/YxpUx0czgx4?si=exsKXJJdOqT08mO2)
   - [Download Sysmon for Windows 10/11](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
   - [Download sysmonconfig.xml file](https://github.com/olafhartong/sysmon-modular/blob/master/sysmonconfig.xml)

3. **Day 3 - Configure:**
   - Configure Wazuh and TheHive servers and endpoints.
   - Ensure both systems are communicating and processing telemetry.
   - [Watch Configuration Video](https://youtu.be/VuSKMPRXN1M?si=53MFANru39zZFO-0)
   - [/etc/cassandra/cassandra.yaml](https://github.com/Mitesh2020/SOC-Automation-Project/blob/main/cassandra.yaml)
   - [/etc/elasticsearch/elasticsearch.yml](https://github.com/Mitesh2020/SOC-Automation-Project/blob/main/elasticsearch.yml)
   - [/etc/thehive/application.conf](https://github.com/Mitesh2020/SOC-Automation-Project/blob/main/application.conf)
   - [/etc/elasticsearch/jvm.options.d/jvm.options](https://github.com/Mitesh2020/SOC-Automation-Project/blob/main/jvm.options%20for%20TheHive)
   - [/etc/wazuh-indexer/jvm.options](https://github.com/Mitesh2020/SOC-Automation-Project/blob/main/jvm.options%20for%20Wazuh)


4. **Day 4 - Telemetry:**
   - Generate telemetry using Mimikatz at endpoints.
   - Trigger and ingest telemetry into Wazuh for analysis.
   - [Watch Telemetry Generation Video](https://youtu.be/amTtlN3uvFU?si=tTBudwOKH0LZ0u53)
   - [Download Mimikatz](https://github.com/gentilkiwi/mimikatz/releases)

5. **Day 5 - SOAR:**
   - Create an automated workflow between Wazuh, TheHive, Shuffle, and email to notify SOC analysts when alerts are triggered.
   - The workflow will automatically send alerts to TheHive and email them to SOC analysts.
   - [Watch SOAR Automation Video](https://youtu.be/GNXK00QapjQ?si=za-3VrnxoaA07XcJ)
   - [Create Account on Shuffle](https://shuffler.io/)
   - [Create Account on VirusTotal](https://www.virustotal.com/)


