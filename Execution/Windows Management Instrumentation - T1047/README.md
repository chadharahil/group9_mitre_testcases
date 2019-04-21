# Technique Description
## T1047 - Windows Management Instrumentation
## [Description from ATT&CK](https://attack.mitre.org/techniques/T1047/) 
>Windows Management Instrumentation (WMI) is a Windows administration feature that provides a uniform environment for local and remote access to Windows system components. It relies on the WMI service for local and remote access and the server message block (SMB) and Remote Procedure Call Service (RPCS) for remote access. RPCS operates over port 135. An adversary can use WMI to interact with local and remote systems and use it as a means to perform many tactic functions, such as gathering information for Discovery and remote Execution of files as part of Lateral Movement.

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
