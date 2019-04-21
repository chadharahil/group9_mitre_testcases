# Technique Description
## T1078 - Valid Accounts
## [Description from ATT&CK](https://attack.mitre.org/techniques/T1078/) 
>Adversaries may steal the credentials of a specific user or service account using Credential Access techniques or capture credentials earlier in their reconnaissance process through social engineering for means of gaining Initial Access. Compromised credentials may be used to bypass access controls placed on various resources on systems within the network and may even be used for persistent access to remote systems and externally available services, such as VPNs, Outlook Web Access and remote desktop. Compromised credentials may also grant an adversary increased privilege to specific systems or access to restricted areas of the network. Adversaries may choose not to use malware or tools in conjunction with the legitimate access those credentials provide to make it harder to detect their presence.

# Assumption

# Execution
This technique did not have a red atomic module

**Test 1 -**
![alt text](./Screenshots/WMIC%20bypass%20using%20local%20XSL%20file.JPG)

**Test 2 -**
![alt text](./Screenshots/WMIC%20bypass%20using%20remote%20XSL%20file.JPG)

# Detection
Configure robust, consistent account activity audit policies across the enterprise and with externally accessible services. Look for suspicious account behavior across systems that share accounts, either user, admin, or service accounts. Activity may be from interactive login sessions or process ownership from accounts being used to execute binaries on a remote system as a particular account. Correlate other security systems with login information (e.g., a user has an active login session but has not entered the building or does not have VPN access). Perform regular audits of domain and local system accounts to detect accounts that may have been created by an adversary for persistence.

## Splunk Filter
The following splunk query will allow us to detect these techniques

**Filter 1 -**
![alt text]()

**Filter 2 -**
![alt text]()