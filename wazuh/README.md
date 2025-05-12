# SIEM + IDS Security Monitoring Project (Wazuh)

This project demonstrates the deployment of Wazuh SIEM directly on a Ubuntu system for real-time security log monitoring and analysis.

## ✅ Environment Details
- **SIEM Platform:** Wazuh 4.11
- **Installation method:** Direct script (`wazuh-install.sh`)
- **Web interface:** https://<your-ip>:443  
- **Access username:** `admin`
- **Access password:**  
  To retrieve the password, run:
  ```bash
  sudo tar -O -xvf /root/wazuh-install-files.tar wazuh-install-files/wazuh-passwords.txt

