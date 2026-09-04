## Custom SSH Brute Force Detection Rule 

A custom Wazuh rule was created to detect multiple failed SSH authentication attempts within a short period of time.
This purpose of this rule is to identify a potential brute force attack

## Custom Rule

The rule was created in `/var/ossec/etc/rules/local_rules.xml`

The rule was configured to:
- Monitor Rule 5760 authentication failure events
- Require the events to come from the same source IP
- Detect 5 failed authentication attempts
- Use a 60-second timeperiod
- Assign a severity level of 10
- Map the detection to MITRE ATT&CK T1110 (Brute Force)

## Testing

To test the new rule multiple SHH attempts were made from the Windows laptop within 60 seconds.

![Brute Force Log Alert](../Screenshots/Brute%20Force%20Log%20Alert.png)


  
Wazuh detected the failed logins and triggered rule 100002.
The activity was identified as:
Possible SSH brute-force attack: multiple authentication failures from the same source IP.
The alert was also mapped to MITRE ATT&CK T1110 – Brute Force.

![Powershell Password Attempts](../Screenshots/Powershell%20Password%20Attempts%20.png)
