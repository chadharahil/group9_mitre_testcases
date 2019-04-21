# Technique Description
## T1220 - XSL Script Processing
## [Description from ATT&CK](https://attack.mitre.org/techniques/T1220/) 
>Extensible Stylesheet Language (XSL) files are commonly used to describe the processing and rendering of data within XML files. To support complex operations, the XSL standard includes support for embedded scripting in various languages. Adversaries may abuse this functionality to execute arbitrary files while potentially bypassing application whitelisting defenses. Similar to Trusted Developer Utilities, the Microsoft common line transformation utility binary (msxsl.exe) can be installed and used to execute malicious JavaScript embedded within local or remote (URL referenced) XSL files. Since msxsl.exe is not installed by default, an adversary will likely need to package it with dropped files. 

# Assumption

# Execution
The Atomic-Red-Team T1220 module describes the test for this technique (https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1220/T1220.md)

Test 1 - WMIC bypass using local XSL file
![alt text](./Screenshots/WMIC%20bypass%20using%20local%20XSL%20file.JPG)

Test 2 - WMIC bypass using remote XSL file
![alt text](./Screenshots/WMIC%20bypass%20using%20remote%20XSL%20file.JPG)

# Detection
Detection is done by monitoring processes to discover the execution and arguments of msxsl.exe and wmic.exe. Compare recent invocations of these utilities with prior history of known good arguments and loaded files to determine anomalous and potentially adversarial activity (ex: URL command line arguments, creation of external network connections, loading of DLLs associated with scripting). Command arguments used before and after the script invocation may also be useful in determining the origin and purpose of the payload being loaded.

The presence of msxsl.exe or other utilities that enable proxy execution that are typically used for development, debugging, and reverse engineering on a system that is not used for these purposes may be suspicious.

## Splunk Filter
The following splunk query will allow us to detect these techniques

Filter 1 - 
![alt text]()

Filter 2 - 
![alt text]()
