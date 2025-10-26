# Task-04
ASK-NO-4-Setup-and-Use-a-Firewall-on-Windows-Linux
🎯 Overview:
This project demonstrates how to configure and test firewall rules on Kali Linux using UFW (Uncomplicated Firewall).

📝 Step-by-Step Procedure:
Linux:
Enable Firewall
Activated UFW to start filtering network traffic:


✅Commands Used
sudo ufw enable
sudo ufw status numbered
sudo ufw deny 23/tcp
telnet localhost 23
nc -vz localhost 23
sudo ufw allow 22/tcp
sudo ufw delete deny 23/tcp
🚨 Firewall Summary
A firewall acts as a security filter between a system and external traffic.

Allow rules permit safe traffic (e.g., SSH on port 22).
Deny rules block unsafe or unused services (e.g., Telnet on port 23).
By configuring firewall rules, we minimize exposure to attacks and ensure only authorized connections are allowed.
Windows 11:
🧰 Tool: Windows Defender Firewall (GUI-based interface)
Open Windows Firewall Settings: Navigated to: Control Panel → System and Security → Windows Defender Firewall Clicked on 'Advanced Settings' from the left panel to access advanced rule configuration.

View Current Firewall Rules: Selected 'Inbound Rules' to view existing traffic rules. Observed default rules for applications and system services.

Create Rule to Block Inbound Traffic on Port 23 (Telnet): • Clicked 'New Rule' in Inbound Rules. • Selected 'Port' as the rule type. • Chose 'TCP', specified port 23. • Action: Block the connection. • Applied rule to: Domain, Private, Public. • Gave it a name: Telnet.

Test the Block Rule: Opened Command Prompt and attempted to connect using: telnet localhost 23
