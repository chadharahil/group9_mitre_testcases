# Technique Description
## T1028 - Windows Remote Management
## [Description from ATT&CK](https://attack.mitre.org/techniques/T1028) 
>Windows Remote Management (WinRM) is the name of both a Windows service and a protocol that allows a user to interact with a remote system (e.g., run an executable, modify the Registry, modify services). It may be called with the winrm command or by any number of programs such as PowerShell. 

# Assumption

# Execution
The Atomic-Red-Team T1089 module describes the test for this technique (https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1107/T1107.md)

**Test 1 -**
![alt text](./Screenshots/WMIC%20bypass%20using%20local%20XSL%20file.JPG)

**Test 2 -**
![alt text](./Screenshots/WMIC%20bypass%20using%20remote%20XSL%20file.JPG)

# Detection
Detection is done by monitoring processes to discover use of WinRM within an environment by tracking service execution. If it is not normally used or is disabled, then this may be an indicator of suspicious behavior. Monitor processes created and actions taken by the WinRM process or a WinRM invoked script to correlate it with other related events.

## Splunk Filter
The following splunk query will allow us to detect these techniques

**Filter 1 -**
![alt text]()

**Filter 2 -**
![alt text]()
