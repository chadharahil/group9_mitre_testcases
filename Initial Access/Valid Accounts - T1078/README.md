# Technique Description
## T1078 - Valid Accounts
## [Description from ATT&CK](https://attack.mitre.org/techniques/T1078/) 
>Adversaries may steal the credentials of a specific user or service account using Credential Access techniques or capture credentials earlier in their reconnaissance process through social engineering for means of gaining Initial Access. Compromised credentials may be used to bypass access controls placed on various resources on systems within the network and may even be used for persistent access to remote systems and externally available services, such as VPNs, Outlook Web Access and remote desktop. Compromised credentials may also grant an adversary increased privilege to specific systems or access to restricted areas of the network. Adversaries may choose not to use malware or tools in conjunction with the legitimate access those credentials provide to make it harder to detect their presence.

# Assumption

# Execution
This technique did not have a red atomic module

Test 1 - 
![alt text]()

Test 2 - 
![alt text]()

# Detection
Detection is done by monitoring processes and command line arguments.

## Splunk Filter
The following splunk query will allow us to detect these techniques

Filter 1 - 
![alt text]()

Filter 2 - 
![alt text]()
