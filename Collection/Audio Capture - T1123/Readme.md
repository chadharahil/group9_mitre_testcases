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

![alt text](https://github.com/iamSoruban/DPI911SSA-Project-Group9/blob/master/Discovery/Account%20Discovery%20-%20T1087/Bat%20File.png)
*Figure 1: Sending the .bat file with the neccessary commands to execute*

After creating a bat file that contains necessary commands to discover important information on the systems about accounts, we will be sending the file to the victim and execute it.

![alt text](https://github.com/iamSoruban/DPI911SSA-Project-Group9/blob/master/Discovery/Account%20Discovery%20-%20T1087/Download%20and%20Execute.png)
*Figure 2: Downloading and executing*

<h1>Detection</h1>

To confirm this, we can use Splunk to analyze.

Using Splunk to detect the indicators
![alt text](https://github.com/iamSoruban/DPI911SSA-Project-Group9/blob/master/Discovery/Account%20Discovery%20-%20T1087/Splunk-1.png)
*Figure 3: Splunk Indicator detection*

Using Splunk to detect the indicators
![alt text](https://github.com/iamSoruban/DPI911SSA-Project-Group9/blob/master/Discovery/Account%20Discovery%20-%20T1087/Splunk-2.png)
*Figure 4: Splunk Indicator detection*
