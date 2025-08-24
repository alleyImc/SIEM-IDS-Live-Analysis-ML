# SIEM + IDS Live Analysis with Suricata and Wazuh

## Project Overview
The primary objective of this project is to **detect a DoS attack using Suricata (an open-source IDS)** and to **monitor its impact on system resources through Wazuh (a SIEM platform)**. 
The attack simulation was carried out using **GoldenEye** on Kali Linux, targeting an Apache2 web server running on the Ubuntu agent. The generated traffic was captured by Suricata, which produced detailed alerts and logs. These logs were then forwarded to Wazuh, where they were visualized and analyzed in a centralized dashboard. 

Unlike a traditional setup that focuses solely on alert generation, this project also evaluates the **system-level impact of the attack**. To achieve this, customized dashboards were built in Wazuh to monitor CPU usage, memory consumption, and system load averages throughout the attack period. 
By correlating Suricata alerts with system metrics, the project provides a holistic view of how the system behaves before, during, and after the attack.

---

## Motivation and Tool Selection
- **Why Wazuh instead of a pure ELK Stack?** 
  While many works in the literature adopt the ELK stack, Wazuh was chosen because it extends ElasticSearch with integrated security components such as file integrity monitoring, rootkit detection, vulnerability assessment, and threat intelligence. This makes it more user-friendly and provides centralized management capabilities.

- **Why Suricata as IDS?** 
  Suricata was selected due to its ability to produce detailed logs at both the network and application layers, its support for multi-core performance, and its seamless integration with Wazuh.

- **Why GoldenEye for the attack simulation?** 
  GoldenEye allows various HTTP-based DoS attack techniques, enabling Suricata to generate alerts even at Layer 7 (application level). This enriches the realism of the test scenario and ensures more diverse event logging.

These choices combined enhanced the observability, attack detection capability, and overall reliability of the experiment.

---

## Findings and Results
- **Suricata Detection:** 
  Suricata successfully detected abnormal TCP behaviors, generating signatures such as 
  *`SURICATA STREAM Packet with invalid ack`* and 
  *`SURICATA STREAM SHUTDOWN RST invalid ack`*. 
  The source and destination IPs matched the attack scenario, and all logs confirmed that the traffic was carried over HTTP.

- **Alert Volume:** 
  During the most intense minutes of the attack, the alert frequency rose above **450 alerts per minute**, showing the system’s responsiveness to high-volume DoS traffic.

- **System Resource Impact:** 
  - CPU usage spiked above **60%** during the attack. 
  - Memory usage showed a clear upward trend as the IDS engine consumed more RAM to process traffic. 
  - System load averages temporarily increased to **very high levels (near 10 in 1-minute average)**, proving that the system was under heavy stress. 

- **Wazuh Visualization:** 
  The customized dashboards provided real-time monitoring of CPU, memory, disk, and load averages. This enabled correlation between IDS alerts and system performance degradation, offering a comprehensive perspective on the system’s reaction to the attack.

---

## Conclusion
This project demonstrates the **successful integration of Suricata IDS and Wazuh SIEM** in detecting and analyzing DoS attacks in real time. 
It proves that:
1. Suricata is effective in generating detailed alerts for both network and application layer anomalies. 
2. Wazuh offers a powerful platform for correlating those alerts with system health metrics. 
3. Together, they provide a **holistic detection and monitoring capability**, ensuring not only that the attack is detected but also that its **impact on system resources** is fully understood. 

The approach is practical, open-source, and extensible, making it applicable for both research and production-level security monitoring environments.

