## SSH Authentication Detection 

SSH Authentication was configured on the Ubuntu Wazuh server in order to detect failed SSH login attempts.

I focused on detecting these logs as they allow me to identify activity that could indicate a malicious actor guessing passwords or brute forcing etc. 

The Ubuntu server needed an SSH server installed and after it was installed and enabled failed SSH attempts could now be logged.

### Testing 

In order to test the detection, several login attempts from the windows laptop to access the Ubuntu Wazuh Server were made 

Authentication attempts were purposely failed by using the wrong password.

Wazuh was able to detect the failed logins and the 5760 rule was triggered. The log provided useful information including the target username and the SSH source port.

## Conclusion
The SSH authentication detection was tested and was successful. One failed login could be a misspelling by a user however repeated failed attempts could be a malicious actor trying to guess a password.
