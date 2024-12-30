# SOC Automation Project
This project automates SOC workflows using open-source tools like Wazuh, Shuffle, and TheHive. It aims to streamline event collection, alerting, and incident response to enhance SOC efficiency.

## Project Design
![design](https://github.com/user-attachments/assets/d3349ba6-9ddb-4817-894a-0e131a30c6cc)

## Tools/Software Installation

1. **Installed VMware or Virtual Box**.
2. **Downloaded Windows 10 Pro ISO file** for using it as a Wazuh agent.
3. **Installed Sysmon with its configuration file (.xml)** in the Windows 10 Pro VM.
4. **Installed Ubuntu 18.04.6 LTS** from Microsoft Store and set up Wazuh in it.
5. **Installed Ubuntu 20.04.6 LTS** from Microsoft Store and set up TheHive with dependencies including Elasticsearch, Java, Cassandra, and TheHive itself.

## Things to Remember
1. **Internet Connection**: Virtual machines should be connected to the internet to access them using their IP addresses.
2. **Wazuh Setup**: A minimum of 8GB RAM and 50GB HDD/SSD space is required for the Wazuh setup.
3. **Firewall Rules**: Firewall rules must be altered to access port 443 for the Wazuh dashboard using UFW in Ubuntu.

## Shortcut to Search Any Word in Nano Editor
Hold `Ctrl + w`

## Configure TheHive
1. Replace localhost address with the IP address of the VM on which TheHive is set up in `Cassandra.yaml` file.
2. Replace seed from `localhost:7000` to `"IP address of VM on which TheHive is set up":7000` in `Cassandra.yaml` file.
3. Stop Cassandra service & remove old files located at `/var/lib/Cassandra/*`.
4. Start Cassandra service & check the status to ensure it is active.
5. Uncomment `cluster.name` in `elasticsearch.yml` file and replace value `my-application` with `thehive`.
6. Uncomment `node.name` without changing its value, and uncomment `network.host`, replacing it with the IP address of the VM on which TheHive is set up.
7. Uncomment `http.port` without changing its value, and uncomment `cluster.initial_master_nodes`, removing `"node-2"` as it's a demo environment.
8. Start and enable the Elasticsearch service, checking its status to ensure it is active.
9. Check file ownership for TheHive with `ls -la /opt/thp`, change owner to thehive user & group with `chown -R thehive:thehive /opt/thp`.
10. Replace localhost IP address with the IP address of the VM on which TheHive is set up in TheHive's `application.conf` file.
11. Replace `cluster-name` value with `"thp"` in `Cassandra.yaml` file.
12. Again, replace localhost IP address (2nd occurrence) with the IP address of the VM on which TheHive is set up in `application.conf` file.
13. Replace `application.baseUrl` value with `http://"IP address of VM on which TheHive is set up":9000`.
14. Start and enable TheHive service, checking its status to ensure it is active.
15. Login with `http://"IP address of VM on which TheHive is set up":9000` using default credentials `admin@thehive.local:secret`.

## Configure Wazuh
1. Open the second Ubuntu instance where Wazuh is set up and open Wazuh dashboard in the browser of Windows 10 Pro VM.
2. Deploy a new agent and copy/paste the given command to execute in the required agent system (i.e., Windows 10 Pro VM).

## Things to Remember
1. Allow port 1514 & 1515 for communication between Wazuh and the deployed agent (Windows 10 Pro VM). Configure the firewall rule in the Ubuntu instance where Wazuh is set up.
