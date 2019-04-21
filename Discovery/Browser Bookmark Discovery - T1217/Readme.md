<h1>Technique Description</h1>
<h2>T1217 - Browser Bookmark Discovery</h2>
<h2><a href="https://attack.mitre.org/techniques/T1217/">Description from ATT&CK</a></h2>
<blockquote>
Adversaries may enumerate browser bookmarks to learn more about compromised hosts. Browser bookmarks may reveal personal information about users (ex: banking sites, interests, social media, etc.) as well as details about internal network resources such as servers, tools/dashboards, or other related infrastructure.
</blockquote>

<h1>Assumption</h1>
Assume that the victim device is already compromised, and able to download files from a web server.

<h1>Execution</h1>
From the Redcanary we dont see any stpes to product Bookmarks Discovery on Windows, therefore we have created a batch file that contains the command to collect the Bookmarks from the Chrome's Default Bookmark Location.
By executing that, we were able to get the Bookmark fil.


![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Discovery/Browser%20Bookmark%20Discovery%20-%20T1217/Screenshots/No%20Bookmark.PNG)
*Figure 1: SeAs we can see, there is no method provided for Bookmark Discovery in Windows*



![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Discovery/Browser%20Bookmark%20Discovery%20-%20T1217/Screenshots/Bat%20file.png)
*Figure 2: Bat file*

![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Discovery/Browser%20Bookmark%20Discovery%20-%20T1217/Screenshots/Reading.png)
*Figure 3: Reading the Bookmark File*


<h1>Detection</h1>

Even though, this does the same job, however it doesnt show as much as visiblity, compare to the Linux and Mac
![alt text](https://github.com/chadharahil/group9_mitre_testcases/blob/master/Discovery/Browser%20Bookmark%20Discovery%20-%20T1217/Screenshots/Splunk-2019-04-21-08-59-40.png)
*Figure 4: Splunk Indicator detection*


