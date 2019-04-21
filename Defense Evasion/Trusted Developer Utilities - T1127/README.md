# Technique Description
## T1127 - XSL Script Processing
## [Description from ATT&CK](https://attack.mitre.org/techniques/T1127/) 
>There are many utilities used for software development related tasks that can be used to execute code in various forms to assist in development, debugging, and reverse engineering. These utilities may often be signed with legitimate certificates that allow them to execute on a system and proxy execution of malicious code through a trusted process that effectively bypasses application whitelisting defensive solutions.
>Examples-
>MSBuild
>RCSI
>WinDbg/CDB
>Tracker

# Execution
The Atomic-Red-Team T1127 module describes the test for this technique (https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1127/T1127.md)

**Test 1 - MSBuild Bypass Using Inline Tasks:**
![alt text](./Screenshots/MSBuild%20Bypass%20Using%20Inline%20Tasks.JPG)


# Detection
The presence of these or other utilities that enable proxy execution that are typically used for development, debugging, and reverse engineering on a system that is not used for these purposes may be suspicious.

Use process monitoring to monitor the execution and arguments of MSBuild.exe, dnx.exe, rcsi.exe, WinDbg.exe, cdb.exe, and tracker.exe. Compare recent invocations of those binaries with prior history of known good arguments and executed binaries to determine anomalous and potentially adversarial activity. It is likely that these utilities will be used by software developers or for other software development related tasks, so if it exists and is used outside of that context, then the event may be suspicious. Command arguments used before and after invocation of the utilities may also be useful in determining the origin and purpose of the binary being executed.


**Filter 1 - Process Creation Monitoring Command Line Argument "MSBuilder.exe"**
![alt text](./Screenshots/Defense%20Evasion%20Splunk%20Threat%20Notification.JPG)

