<h1>Technique Description</h1>
<h2>T1010 - Account Discovery</h2>
<h2><a href="https://attack.mitre.org/techniques/T1010/">Application Window Discovery</a></h2>
<blockquote>
Adversaries may attempt to get a listing of open application windows. Window listings could convey information about how the system is used or give context to information collected by a keylogger.
</blockquote>

<h1>Assumption</h1>
Assume that the victim device is already compromised, and able to download files from a web server.

<h1>Execution</h1>

By using the C# file provided by Redcanary, we compile the file.

![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Discovery/Application%20Window%20Discovery%20-%20T1010/Screenshots/Compiling%20C%20Sharp.png)
*Figure 1: Compiling the C# file*

After compiling the file and getting the Executable, we can execute it to see the Running Applications.

![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Discovery/Application%20Window%20Discovery%20-%20T1010/Screenshots/Executing%20Application.png)
*Figure 2: Downloading and executing*

<h1>Detection</h1>

To confirm this, we can use Splunk to analyze.

Using Splunk to detect the indicators
![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Discovery/Application%20Window%20Discovery%20-%20T1010/Screenshots/Splunk-1.png)
*Figure 3: Splunk Indicator detection*

Using Splunk to detect the indicators
![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Discovery/Application%20Window%20Discovery%20-%20T1010/Screenshots/Splunk-2.png)
*Figure 4: Filtering processes that uses cmd*

Using Splunk to detect the indicators
![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Discovery/Application%20Window%20Discovery%20-%20T1010/Screenshots/Splunk-2.png)
*Figure 5: Filtering using process ID that we collected from the previous Application*
