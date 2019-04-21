<h1>Technique Description</h1>
<h2>T1123 - Audio Capture</h2>
<h2><a href="https://attack.mitre.org/techniques/T1123/">Description from ATT&CK</a></h2>
<blockquote>
 An adversary can leverage a computer's peripheral devices (e.g., microphones and webcams) or applications (e.g., voice and video call services) to capture audio recordings for the purpose of listening into sensitive conversations to gather information.

Malware or scripts may be used to interact with the devices through an available API provided by the operating system or an application to capture audio. Audio files may be written to disk and exfiltrated later.
</blockquote>

<h1>Assumption</h1>
Assume that the victim device is already compromised, and able to download files from a web server.

<h1>Execution</h1>

By using the SoundRecorder command we will be able to record audio and save it, by using /FILE <outputFile> name we can sepcify the output file, and by using /DURATION <time>, we can record it with the time limit.

![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Collection/Audio%20Capture%20-%20T1123/Screenshots/Recording%20CMD.png)
*Figure 1: Using the Command prompt to record the Audio for 30 seconds - 1*


![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Collection/Audio%20Capture%20-%20T1123/Screenshots/Recording%20Audio.png)
*Figure 2: Using the Command prompt to record the Audio for 30 seconds - 2*

<h1>Detection</h1>

Using Splunk to analyze: 

Using Splunk to detect the indicators
![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Collection/Audio%20Capture%20-%20T1123/Screenshots/Splunk-1.png)
*Figure 3: Splunk Indicator detection*

As we can see, in Splunk sound recorder is process is created.
By using this as filter, we can trigger an alert, when the SoundRecorder process starts.
