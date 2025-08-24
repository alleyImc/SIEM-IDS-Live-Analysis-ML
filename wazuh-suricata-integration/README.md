# Wazuh & Suricata Integration

This section documents the integration of Suricata IDS logs (`eve.json`) into the Wazuh SIEM platform using the Ubuntu 20.04.6 Desktop environment.

---

## Step 1: Editing the Wazuh Agent Configuration

Open the Wazuh agent configuration file and add the Suricata log source:

    sudo nano /var/ossec/etc/ossec.conf

Add the following snippet:

    <localfile>
      <log_format>json</log_format>
      <location>/var/log/suricata/eve.json</location>
    </localfile>

- *Figure 7.1:* Opening the `ossec.conf` file in a text editor  
- *Figure 7.2:* Adding the Suricata configuration snippet  
- *Figure 7.3:* Final view of the Suricata log path integration  

---

## Step 2: Restarting the Wazuh Agent

After saving the configuration changes, restart the Wazuh agent:

    sudo systemctl restart wazuh-agent

- *Figure 7.4:* Restarting and verifying the Wazuh agent service  

---

## Step 3: Generating and Verifying Events

Send a test request to trigger Suricata alerts:

    curl http://testmynids.org/uid/index.html

- *Figure 7.5:* Sending a test request from the Ubuntu agent  
- *Figure 7.6:* Viewing Suricata-detected events in the Wazuh Dashboard  
- *Figure 7.7:* Inspecting detailed Suricata event logs in the Wazuh Dashboard  

---

With these steps, Suricata IDS events are successfully forwarded to and monitored by the Wazuh SIEM environment.
