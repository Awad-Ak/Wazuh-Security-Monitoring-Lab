File Integrity Monitoring (FIM)

FIM was configured in Wazuh to monitor a set directory on the Windows agent.
File creation, modification and deletion was tracked.

The laptop that was being monitored was running the Wazuh agent. The directory that was being configured was C:\Users\awadk\Downloads\Wazuh Test.
Real time monitoring was enabled in the ossec.conf file.

The configuration can be seen below:

<syscheck>
<disabled>no</disabled>
<frequency>43200</frequency>
<directories realtime="yes">C:\Users\awadk\Downloads\Wazuh Test</directories> </syscheck>

To test if FIM was working I created a test file, modified it and then deleted it.

![FIM File Created](../Screenshots/




Wazuh was able to detect and log these changes. Furthermore, the alerts provided info that can be used by an analyst to the file operations.

Conclusion 

Certain file modifications could be a sign of malicious activity eg an attacker could modify a companies files when they gain acsess to an endpoint in this case a windows laptop.

The FIM was successful as Wazuh was able to detect all the changes.
