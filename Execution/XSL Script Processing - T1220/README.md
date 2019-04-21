# Technique Description
## T1220 - XSL Script Processing
## [Description from ATT&CK](https://attack.mitre.org/techniques/T1220/) 
>Extensible Stylesheet Language (XSL) files are commonly used to describe the processing and rendering of data within XML files. To support complex operations, the XSL standard includes support for embedded scripting in various languages. Adversaries may abuse this functionality to execute arbitrary files while potentially bypassing application whitelisting defenses. Similar to Trusted Developer Utilities, the Microsoft common line transformation utility binary (msxsl.exe) can be installed and used to execute malicious JavaScript embedded within local or remote (URL referenced) XSL files. Since msxsl.exe is not installed by default, an adversary will likely need to package it with dropped files. 

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
