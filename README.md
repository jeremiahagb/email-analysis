<h1>Email Analysis</h1>



<h2>Description</h2>
This project consists of utilizing the open source tools to do basic email investigations to determine if an email is malicious or legit.
<br />

<h2>Findings</h2>

- <b>[Short summary of investigation](https://1drv.ms/w/s!Ai9Jkhg_z_WvuBGfUx74XRMo9fO6?e=ccebKR)</b>


<h2>Utilities Used</h2>

- <b>MXtoolbox</b>
- <b>VirusTotal</b>
- <b>abuseipdb</b>
- <b>TalosIntelligence</b>
- <b>urlscan.io</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (22H2)

<h2>Program walk-through:</h2>

<p align="center">
I received a forwarded email to determine the validity: <br/>
<img src="https://i.imgur.com/Mf0MMDz.png" height="80%" width="80%" alt="Received an email"/>
<br />
<br />
I then obtained the raw message and analyzed the header in MXtoolbox; DMARC, DKIM, and SPF checked off:  <br/>
<img src="https://i.imgur.com/k2bkyGk.png" height="80%" width="80%" alt="Analyzed email header"/>
  <img src="https://i.imgur.com/AgK3VQu.png" height="80%" width="80%" alt="Analyzed email header"/>
<br />
<br />
I observed the IP was blacklisted: <br/>
<img src="https://i.imgur.com/8odEnzR.png" height="80%" width="80%" alt="Blacklisted IP"/>
<br />  
<img src="https://i.imgur.com/YWiH5MQ.png" height="80%" width="80%" alt="Blacklisted IP"/>
<br />  
<br />
I then scanned the IP address in Virus Total and 1 security vendor flagged it as malicious:  <br/>
<img src="https://i.imgur.com/xlEre9T.png" height="80%" width="80%" alt="Scan IP in VirusTotal"/>
<br />
<br />
Further scanning of the IP in AbuseIPDB showed it to be reported 405 times with a confidence of abuse rate of 58%:  <br/>
<img src="https://i.imgur.com/HouVSVw.png" height="80%" width="80%" alt="Scanned in AbuseIPDB"/>
<br />
<br />
There were several recent reports of spam, spoofing, phishing, etc:  <br/>
<img src="https://i.imgur.com/h5LaDWX.png" height="80%" width="80%" alt="Identified categories of attacks"/>
<br />
<br />
TalosIntelligence shows the IP to have a good reputation:  <br/>
<img src="https://i.imgur.com/7Ybf7nQ.png" height="80%" width="80%" alt="Scanned in TalosIntelligence"/>
<br />
<br />  
<br />
Also, a scan of a clickable link within the email was done in VirusTotal and urlscan.io, both didn't show it as being malicious: <br/>
<img src="https://i.imgur.com/4d3KaHn.png" height="80%" width="80%" alt="VirusTotal scan"/>
<img src="https://i.imgur.com/QTZs2Q2.png" height="80%" width="80%" alt="Urlscan.io results"/>
<br />
<br />  

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
