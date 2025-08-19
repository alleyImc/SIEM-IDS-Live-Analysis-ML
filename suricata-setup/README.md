# Suricata Installation and Configuration

This section documents the installation, configuration, and validation steps for **Suricata IDS** on Ubuntu 20.04.6 Desktop. The process follows the methodology applied in the thesis, supported with screenshots for each step.

## 6.1 Suricata Installation

- Updating system repositories and installing required tools.  
  *(Fig. 6.1 Updating repositories and installing required packages)*  
- Adding Suricata stable PPA repository.  
  *(Fig. 6.2 Adding Suricata PPA repository)*  
- Installing Suricata and its dependencies.  
  *(Fig. 6.3 Installing Suricata and dependencies)*  

## 6.2 Verification and Service Status

- Checking Suricata version information.  
  *(Fig. 6.4 Checking Suricata version)*  
- Verifying initial Suricata service status.  
  *(Fig. 6.5 Initial service status)*  

## 6.3 Configuration

- Configuring the network interface in Suricata settings.  
  *(Fig. 6.6 Network interface configuration)*  
- Setting EVE JSON output for logs.  
  *(Fig. 6.7 Configuring EVE log output)*  

## 6.4 Restarting and Validating Service

- Restarting Suricata service.  
  *(Fig. 6.8 Restarting the service)*  
- Validating service status after restart.  
  *(Fig. 6.9 Service status check)*  
- Checking Suricata log file (`suricata.log`).  
  *(Fig. 6.10 Checking suricata.log output)*  
- Confirming service startup from `suricata.log`.  
  *(Fig. 6.11 Service startup validation)*  
- Inspecting `stats.log`.  
  *(Fig. 6.12 Checking stats.log)*  
- Validating performance and statistics from `stats.log`.  
  *(Fig. 6.13 Performance verification from stats.log)*  

## 6.5 Rule Updates and Test Rule

- Downloading and applying updated rule sets.  
  *(Fig. 6.14 Updating rule sets)*  
- Creating a custom test rule for Suricata.  
  *(Fig. 6.15 Creating custom rule)*  
- Adding the custom rule to configuration.  
  *(Fig. 6.16 Adding test rule to Suricata)*  
- Restarting Suricata service after rule changes.  
  *(Fig. 6.17 Restarting after test rule addition)*  

## 6.6 Log Monitoring and Event Testing

- Sending a curl request to test address.  
  *(Fig. 6.18 Sending test curl request)*  
- Validating alert in `fast.log`.  
  *(Fig. 6.19 Test alert in fast.log)*  
- Checking detailed alert in `eve.json`.  
  *(Fig. 6.20 Test alert in eve.json)*    

---

At the end of these steps, **Suricata IDS was successfully installed, configured, and validated**, ensuring that network traffic was being monitored and logged properly.
