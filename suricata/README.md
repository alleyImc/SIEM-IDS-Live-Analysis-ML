# SIEM + IDS Live Traffic Analysis Project

In this project, Suricata IDS is installed and configured to monitor live network traffic and generate rule-based alerts.

## Installed Components
- Suricata
- Ruleset: ET Open
- Log formats: `fast.log`, `eve.json`
- Test command: `curl http://testmynids.org`

## Project Structure
- `suricata/` → Configuration files
- `logs/` → Sample test logs
- `screenshots/` → Alert screen capture 

## Next Steps
- Install Wazuh SIEM
- Forward Suricata's JSON logs to Wazuh for centralized analysis
