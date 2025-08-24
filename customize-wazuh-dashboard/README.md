# Customized Wazuh Dashboard – System Metrics

This document describes the customization of the Wazuh dashboard to monitor **Ubuntu Agent system metrics**.  
The customization steps were inspired by the official Wazuh blog:  
- [Monitoring Linux resource usage with Wazuh](https://wazuh.com/blog/monitoring-linux-resource-usage-with-wazuh/)  

A screenshot (Figure 8.18) demonstrates the final customized dashboard panel after test.

---

## Added Dashboards and Their Roles

- **CPU Usage – Live Chart**  
  Displays the real-time CPU utilization of the agent.  
  Sudden and unexpected spikes may indicate malicious activity, abnormal processes, or potential DoS attacks.  

- **Disk Usage – Live Chart**  
  Shows the real-time percentage of disk usage.  
  Abnormal disk usage could indicate attackers leaving large files, ransomware activity, or anomalies in log storage.

- **Memory Usage – Live Chart**  
  Displays real-time memory utilization.  
  Memory leaks, misconfigured applications, or memory-hungry malware could cause sudden spikes, affecting system stability and security.

- **System Load Average – Live Chart**  
  Shows the process queue length over 1, 5, and 15-minute averages.  
  High load averages may suggest system overload, performance degradation, or an ongoing DoS attack.  

---

 With these customizations, the Wazuh dashboard provides enhanced visibility into the **performance and security posture** of the monitored Ubuntu agent.  

---

*Figure 8.18*: Customized Ubuntu Agent System Metrics Panel
