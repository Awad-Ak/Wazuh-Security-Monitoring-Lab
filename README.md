# Wazuh-Security-Monitoring-Lab
A security lab that uses the SIEM tool Wazuh to collect and track security events on both Windows and Linux 

This lab was designed to recreate common security events and then investigate them further through the Wazuh dashboard.

The project focused on detecting:

File Integrity Monitoring 
SSH authentication failure detection 
SSH brute force detection

Project Goals/Objectives
Create a virtual machine which runs Ubuntu Linux using VMware
Install Wazuh on the Ubuntu VM
Configure Wazuh Manager and Indexer 
Used Windows laptop as the monitored device 
Installed Wazuh Agent on Windows laptop
Configure FIM on Windows laptop
Create, edit and delete a file to simulate changes which creates logs
Install SSH on Ubuntu VM
Simulate failed SSH authentication attempts (logins) from Windows laptop 
Create a custom rule to trigger when there is an SSH brute force atttack
Mapped the detection to MITRE ATT&CK
