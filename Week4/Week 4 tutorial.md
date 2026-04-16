# Week 4

In Week 4 we covered ***Advanced routing***, where we learned how data is routed or forwarded from source to destination, the best path the data takes, the protocols used, viewed routing tables and learned more new commands.   
Given it was the Easter long weekend, progress this week was a little slow. I found the lecture tasks this week were a little more challenging, mainly because *GNS3* kept crashing when trying to use the router console for the OSPF tasks. To rectify the issue, a simple restart of *GNS3* and *Virtual Box* was required.

There were two Tutorial tasks this week, the first tasks were:
- Create project named View-Routes-12091677
- Add two nodes of type Linux Host and one node of type Linux Router, with all three nodes connected to one Ethernet switch. Then add a third Linux Host connected directly to the Linux Router. In total there are three hosts, one router and one switch, creating two subnets
- Select an IPv4 network address to use in each of your two subnets, and set the static IP addresses for each host and router interface
- Enable forwarding on the router, and disable forwarding on all the hosts
- Start all nodes
- View the routing table of each device
- Test your network with *ping*

 A screenshot of the network showing two Linux hosts on one subnet (10.10.1.0/24) and one Linux host on a different subnet (10.10.2.0/24) can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week4/View-Routes-12091677-network.png).   
 Forwarding was enabled on the router using the command 'sysctl net.ipv4.ip_forward=1' and disabled on the hosts using the command 'sysctl net.ipv4.ip_forward=0'.    
 Screenshots of the routing tables can be viewed on the links below:    
 - [Host 1](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week4/View-Routes-12091677-host1.png)
 - [Host 2](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week4/View-Routes-12091677-host2.png)
 - [Host 3](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week4/View-Routes-12091677-host3.png)
 - [Router 1](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week4/View-Routes-12091677-router.png)       

A screenshot of a sucessful ping between hosts on different subnets can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week4/View-Routes-12091677-ping.png).    
A copy of the *GNS3* project can be downloaded [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week4/View-Routes-12091677.gns3project).   

 
 
