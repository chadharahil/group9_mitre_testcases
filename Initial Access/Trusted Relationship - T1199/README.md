# Technique Description
## T1199 - Trusted Relationship
## [Description from ATT&CK](https://attack.mitre.org/techniques/T1199) 
>Adversaries may breach or otherwise leverage organizations who have access to intended victims. Access through trusted third party relationship exploits an existing connection that may not be protected or receives less scrutiny than standard mechanisms of gaining access to a network. Organizations often grant elevated access to second or third-party external providers in order to allow them to manage internal systems. Some examples of these relationships include IT services contractors, managed security providers, infrastructure contractors (e.g. HVAC, elevators, physical security). The third-party provider's access may be intended to be limited to the infrastructure being maintained, but may exist on the same network as the rest of the enterprise. As such, Valid Accounts used by the other party for access to internal network systems may be compromised and used.

# Assumption
For this scenario, we established a webserver located at 192.168.2.5 running apache2. We uploaded our Caldera RAT to the /var/www/html directory and named it OfficeUpdater.exe. We are assuming that the webserver on the network which was deployed by a third-party on the DMZ has been compromised. This trusted relationship with the webserver will be leveraged as a trusted third party to compromise the network. The malicious RAT was pushed onto the client machine by initiating a mail message to each client stating that they need to update their version of Microsoft Office ASAP using the executable located on the webserver’s index. Once the victim downloads and runs the program, the RAT will be initialized, and we will have full access to perform our malicious commands.

# Execution
This technique did not have a red atomic module

**Test 1 -**


![alt text](./Trusted%20Relationship%20-%20T1199/Trusted1.png)

**Test 2 -**

![alt text](./Screenshots/WMIC%20bypass%20using%20remote%20XSL%20file.JPG)

# Detection
Establish monitoring for activity conducted by second and third party providers and other trusted entities that may be leveraged as a means to gain access to the network. Depending on the type of relationship, an adversary may have access to significant amounts of information about the target before conducting an operation, especially if the trusted relationship is based on IT services. Adversaries may be able to act quickly towards an objective, so proper monitoring for behavior related to Credential Access, Lateral Movement, and Collection will be important to detect the intrusion.

## Splunk Filter
The following splunk query will allow us to detect these techniques

**Filter 1 -**
![alt text]()

**Filter 2 -**
![alt text]()
