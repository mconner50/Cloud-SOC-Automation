# Cloud-SOC-Automation

## Objective

This Cloud-Based SOC Automation project allowed me to set up a Cloud Based system utilizing tools like Wazuh, TheHive, Shuffler, and Sysmon on Vultr to detect, analyze, and Automate alerts, with the goal of setting up an environment to analyze how a SIEM agent like Wazuh can detect Mimikatz on a system. This project allowed me to understand how companies can decrease Incident response time based on the 
### Skills Learned


- Implementation and deployment of Cloud-Based Servers to house active tools
- Strengthen proficiency in maintaining a safe and separated environment from the host system
- Gained a deeper understanding on utilizing API keys to connect Security devices in Shuffler to create an automatic emailer.
- Enhanced knowledge utilizing SIEMs and Automation knowledge to lessen the burden of manually finding what threats are occurring on a system.
- Development of critical thinking and problem-solving in terms of recognizing how these systems help and increase productivity for Cyber Professionals.
### Tools Used

- Cloud-based environment builders like Vultr, AWS, and Azure to build within the cloud, as most companies have moved to today.
- Case management like TheHive which incorporates alot of tools to ensure all aspects like Metrics, Alerts, Case reporting are available for cyber teams.
- Telemetry generation tools like Sysmon to help analyze the Windows traffic that Mimikatz produces and ensure that it is capture by our SIEM
- A Security Information Event Management System like Wazuh that you create an agent in to help detect data and sends it to other tools to then be scanned and identified.

## Steps (more detailed coming soon when have the time from full time work and school)
Configuring Wazuh and sysmon on Vultr-
<img width="1024" height="768" alt="Sysmon config" src="https://github.com/user-attachments/assets/01529672-d172-4e40-80ca-71d9e4df3e74" />
<img width="1024" height="768" alt="vultr-Wazuh" src="https://github.com/user-attachments/assets/60c3f4ad-8a00-43e8-b38f-0a964c9fe585" />
<img width="1024" height="768" alt="Wazuh" src="https://github.com/user-attachments/assets/ff6001d7-d6fe-45b4-b4db-5aec3223c74f" />
<img width="1024" height="768" alt="Wazuh SysmonConnected" src="https://github.com/user-attachments/assets/ed759838-54a0-4b8c-be6e-36e9e91b6c14" />

The Hive installed and logged in
<img width="1024" height="768" alt="TheHive" src="https://github.com/user-attachments/assets/171c7056-da7b-44a0-a696-a664548530f4" />
<img width="1024" height="768" alt="TheHivelogin" src="https://github.com/user-attachments/assets/3f0bc10b-b8dd-4d06-9eab-2f83ed58eca3" />

Setting up a Wazuh Agent that will detect mimikatz details within the cloud enviornment-
<img width="1024" height="768" alt="Agent" src="https://github.com/user-attachments/assets/c35272e2-8136-4a6f-94ed-fb3635666c63" />
<img width="1918" height="1034" alt="Screenshot 2025-09-16 233830" src="https://github.com/user-attachments/assets/c7b2a34a-1a1d-48dc-bf9d-40c5fc401cfb" />

Utilizing Shuffler for setup the automation and to send notifications - looking specifically for hashes, and mimikatz material.
<img width="442" height="348" alt="Screenshot 2025-09-19 182851" src="https://github.com/user-attachments/assets/9fe86d8f-26bf-46c1-9ede-435ed4f8567b" />
Hash it found when it searched for mimikatz activity

<img width="1589" height="906" alt="Shuffler notif" src="https://github.com/user-attachments/assets/d3d1ea1b-9b53-440e-9b44-cfa273dc0a93" />
In this image utilizing a webhook and an API key for Virus total we created an automation that will detect when mimikatz is attempting to run.

<img width="1589" height="906" alt="Shuffler notif" src="https://github.com/user-attachments/assets/2d7aa60f-49f1-49f0-8f71-94cead9f6723" />

<img width="1578" height="899" alt="The hive configured" src="https://github.com/user-attachments/assets/17e83d34-e6b5-443d-87ef-9bd4494d8506" />
The Hive configured on Shuffler which utilizing the Cassandra Apache server we setup to then help provide case management systems. In this case with The Hive setup it will lead into our next screenshot where we see a Ticket being created and popping up in Wazuh from the agent detecting the case that was opened.
<img width="1911" height="979" alt="Ticket" src="https://github.com/user-attachments/assets/9f07e922-2a93-4d78-9774-2b267f9268dc" />
This ticket was created through the automated responses that we created through Shuffler to then detect Mimikatz activity on our vultr servers that attempt to go through the server and steal informationl.
