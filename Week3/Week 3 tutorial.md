# Week 3

In Week 3 we covered ***The TCP and IP Protocols*** in which we learnt how TCP and UDP packets travel in Transport Layer, how IP packets look, netcat and we completed our first assessment, in the form of an in class test during our Tutorial.   

I found the tasks in the test quite easy as we had been over them in the previous weeks tutorials. I struggled a little with the time allocated, only because I lost a few minutes looking for the test questions and spent time taking screenshots of my work. I could of improved my editing and layout a little if i had more time.   
My completed asssessment can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week3/In-class%20Lab%20Test%201%20Report%20-%2012091677.docx).   

After the test we continued with out tutorial tasks.      
My Tutorial tasks were 
- Start the netcat server on a host using a port that is ***not*** 12345
- On another host, start the netcat client to connect to the netcat server
- Send your name in a message from client to server
- Send your student ID in a message from server to client

I had to revisit the Tutorial recording before i got netcat working properly, i first tried setting the port for the server using the last 5 digits of my student ID number, but i got an error. I then used a different port, that was closer to 12345 (12121) and then it worked.    

A screenshot of the messages between client and server can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week3/Netcat-Basics-12091677-client-server%20.png).   

My second Tutorial tasks were
- On the link connecting host 1 to the switch, start a packet capture
- Ping from host 1 to host 2, sending three requests
- Use netcat to send your name from host 1 to host 3
- Stop the capture on the link
- Transfer the capture file from GNS3 to your host computer, saving as Capture-Basics-<studentid>-ping-netcat.pcap

Once I revisited the Tutorial recording, I transfered the .pcap file from *GNS3* to my local machine. I opened the *Wireshark* capture and realised I had only pinged host 2, I didn't use any netcat commands. Once I had realised this, I deleted the original file and completed the capture again.   

The *Wireshark* capture file can be downloaded [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week3/Capture-Basics-12091677-ping-netcat.pcap).

