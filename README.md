# SOC Automation Project
This project automates SOC workflows using open-source tools like Wazuh, Shuffle, and TheHive. It aims to streamline event collection, alerting, and incident response to enhance SOC efficiency.

## Project Design
![design](https://github.com/user-attachments/assets/d3349ba6-9ddb-4817-894a-0e131a30c6cc)

## Tools/Software Installation

1. **Installed VMware or Virtual Box**.
2. **Downloaded Windows 10 Pro ISO file** for using it as a Wazuh agent.
3. **Installed Sysmon with its configuration file (.xml)** in my primary OS (Windows 11).
4. **Installed Ubuntu 18.04.6 LTS** from Microsoft Store and set up Wazuh in it.
5. **Installed Ubuntu 20.04.6 LTS** from Microsoft Store and set up TheHive with dependencies including Elasticsearch, Java, Cassandra, and TheHive itself.

## Things to Remember
1. **Internet Connection**: Virtual machines should be connected to the internet to access them using their IP addresses.
2. **Wazuh Setup**: A minimum of 8GB RAM and 50GB HDD/SSD space is required for the Wazuh setup.
3. **Firewall Rules**: Firewall rules must be altered to access port 443 for the Wazuh dashboard using UFW in Ubuntu.
