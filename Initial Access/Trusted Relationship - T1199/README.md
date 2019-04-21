# Technique Description
## T1199 - Trusted Relationship
## [Description from ATT&CK](https://attack.mitre.org/techniques/T1199) 
>Adversaries may breach or otherwise leverage organizations who have access to intended victims. Access through trusted third party relationship exploits an existing connection that may not be protected or receives less scrutiny than standard mechanisms of gaining access to a network. Organizations often grant elevated access to second or third-party external providers in order to allow them to manage internal systems. Some examples of these relationships include IT services contractors, managed security providers, infrastructure contractors (e.g. HVAC, elevators, physical security). The third-party provider's access may be intended to be limited to the infrastructure being maintained, but may exist on the same network as the rest of the enterprise. As such, Valid Accounts used by the other party for access to internal network systems may be compromised and used.

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
