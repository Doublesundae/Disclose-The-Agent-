<h1> Disclose The Agent </h1>

<h2>Description</h2>
In this project, there were secret messages sent between two parties which also had a document attached with a location. The objective was to find out various amounts of information about the email message sent.
<br />


<h2>Tools Used</h2>

- <b>WireShark</b> 
- <b>Base64 Decoder</b>
- <b>Virus Total</b>
- <b>LetsDefend.io</b>


<h2>Environments Used </h2>

- <b>Orcale Virtual Box </b>
- <b>Windows 10</b> 

<h2>Walk-through</h2>

<p align="left">

  <h3>Question #1</h3>
What is the email address of Ann's secret boyfriend? <br/>
<br/>
<img src="https://i.imgur.com/ToOB8ap.png" height="80%" width="80%" alt="question 1"/>
<br/> 
<br/>
To get this answer, I had to narrow down the search to just SMTP traffic in Wireshark and locate the traffic specific to the email Transmission which gives us who the message is going.
<br/>
<br/>
<img src="https://i.imgur.com/1NU8bL0.png" height="80%" width="80%" alt="Answer 1"/>

<br />
<br />

<h3>Question #2</h3>
What is Ann's email password? <br/>
<br/>
<img src="https://i.imgur.com/YjNGnIz.png" height="80%" width="80%" alt="Question 2"/>
<br/>
To get this answer, I had to search for when Ann started the Authentication process. Once located, I also located when the password was prompted
<br/>
<br/>
<img src="https://i.imgur.com/fJNsSS2.png" height="80%" width="80%" alt="Answer 2"/>
<br />
<br />
Though we have the password, it is encoded and we will need to decode it, to do this the website "base64 decode and encode" was used.
<br/>
<br/>
<img src="https://i.imgur.com/XIFJWHT.png" height="80%" width="80%" alt="Answer 2"/>
<br />
<br />


<h3>Question #3</h3>
What is the name of the file that Ann sent to his secret lover?  <br/>
<br/>
<img src="https://i.imgur.com/uXkPQ06.png" height="80%" width="80%" alt="Question 3"/>
<br />
<br />
To Get this answer, We Had to follow the TCP stream of the traffic that gave us the answer to question #1. which gave us the attachment name <br/>
<br/>
<img src="https://i.imgur.com/6ao6JtR.png" height="80%" width="80%" alt="Answer 3"/>
<br/>
<br/>

<h3>Question #4</h3>
In what country will Ann meet with her secret lover?  <br/>
<br/>
<img src="https://i.imgur.com/eowbkwC.png" height="80%" width="80%" alt="Question 4"/>
<br />
<br />
This answer required us to extract the email from pcap file. once this is down we could open the file a view the location <br/>
<br/>
<img src="https://i.imgur.com/2cLu9uD.png" height="80%" width="80%" alt="Answer 4"/>
<img src="https://i.imgur.com/Cl2nCFx.png" height="80%" width="80%" alt="Answer 4"/>
<img src="https://i.imgur.com/W7ssVVQ.png" height="80%" width="80%" alt="Answer 4"/>
<br/>
<br/>

<h3>Question #5</h3>
What is the MD5 value of the attachment Ann sent? <br/>
<br/>
<img src="https://i.imgur.com/sPJCt97.png" height="80%" width="80%" alt="Question 4"/>
<br />
<br />
To Get this answer, The Virus total was used   <br/>
<br/>
<img src="https://i.imgur.com/jpkxZtT.png" height="80%" width="80%" alt="Answer 4"/>
<br/>
<br/>



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
