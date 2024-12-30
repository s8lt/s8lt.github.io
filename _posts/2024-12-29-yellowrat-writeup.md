---
layout: post
title: Yellow Rat WriteUp
date: 2024-12-29 10:30:00 -0500
---

# CyberDefender Yellow Rat WriteUp
## Easy Threat Intel
### Tools: VirusTotal 

#### This lab has equipeed us with the skills to investigate malware behind abnormal network traffic at GlobalTech Industries 

![Title](https://i.imgur.com/F6tx9ip.png)
<style>
  details {
    margin-bottom: 20px;
  }
</style>

<details>
<summary> Q1: Understanding the adversary helps defend against attacks. What is the name of the malware family that causes abnormal network traffic?

</summary> 

<br>
We proceed to unzip the file we are given and utilize an online tool called VirusTotal that's used for analzying malware in different file formats. In this exercise, we are given a hash format within a zip file we are tasked with unzipping. 

1.  We proceed to unzip the file and copy the hash we are given
    * ``` 30E527E45F50D2BA82865C5679A6FA998EE0A1755361AB01673950810D071C85 ```

2. Navigating to VirusTotal, we dump the hash into the input field under the search tab as shown below

![Description](https://i.imgur.com/slTfBUF.png)

3. After entering our hash we are given our results of the hash
![Results](https://i.imgur.com/Ve4R4j8.png)

We can see that our results show that our hash has been up to no good, we are shown a lot of information at once. We go back to our question, it is asking for the name of the malware family that causes abnormal network traffic. 

4. We move forward and go to the **Relations** tab, our goal is to see the malware family in a clear visual way which prompts us to head to the Graph Summary section and click on our graph. 

5. The graph is shown, to better visualize the graph we change it to a **Tree Representation**

From the picture below, we can conclude our answer along with using context clues. We can see RAT which is Remote Access Trojan which is apart of the Malware family. We can gather from this that <font color="red"> **Yellow Cockatoo RAT** </font> is the answer we were looking for!! 

![Goal](https://i.imgur.com/c7jf3Bn.png)

</details>

<details> 
<summary> Q2: As part of our incident response, knowing common filenames the malware uses can help scan other workstations for potential infection. What is the common filename associated with the malware discovered on our workstations? </summary>
<br> 
Using the keyword filename, we go on to look under the details panel, and search under the "Names" category. From there, we arrive to our answer of 
<font color="red">111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll </font>

![Picture](https://i.imgur.com/c7hfo98.png)

</details>

<details>
<summary>Q3: Determining the compilation timestamp of malware can reveal insights into its development and deployment timeline. What is the compilation timestamp of the malware that infected our network? 
</summary>
<br> 
Staying in the <b> Details </b> section, we navigate to the <b> History </b> subsection. Within the History subsection we are looking for when it was first deployed after development. Seeing <b> Creation Time </b>, we are presented with the answer of <font color=red> 2020-09-24 18:26:47. </font>

</details>

<details>
<summary> Q4: Understanding when the broader cybersecurity community first identified the malware could help determine how long the malware might have been in the environment before detection. When was the malware first submitted to VirusTotal?
</summary>
<br> Within the same section of the last question, We are in the Details > History section and we can look for the “First Submission” answer. Here we can see our answer being <font color=red> 2020-10-15 02:47:37 UTC </font>
</details>

<details>
<summary>
Q5: To completely eradicate the threat from Industries' systems, we need to identify all components dropped by the malware. What is the name of the .dat file that the malware dropped in the AppData folder?
</summary>
<br>
To find the .dat file, we utilize the community tab at our advantage. We search for the report that cound contain the details of the malware that dropped in the AppData folder. We navigate to the following link 

<a href="url"></a> https://redcanary.com/blog/yellow-cockatoo/ . At this link, we are presented with the evidence of our answer through the Red Canary report. 

![answr](https://i.imgur.com/qFhja0a.png)
</details>

<details>
<summary>
Q6: It is crucial to identify the C2 servers with which the malware communicates to block its communication and prevent further data exfiltration. What is the C2 server that the malware is communicating with?
</summary>
<br>
To find the C2 server, we look at the same Red Canary report. Within the report we navigate to the C2 section, where we see our answer being <font color= red> https://gogohid.com </font>

![answer](https://i.imgur.com/l4aNIuP.png) 
</details>

### We have completed the second portion of the Starting Point on CyberDefenders !!
### Our next WriteUp will be 3/5 of the Starting Point which will be GrabThePhisher. 