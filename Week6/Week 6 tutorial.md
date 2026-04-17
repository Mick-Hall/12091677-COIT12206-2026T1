# Week 6

In Week 6 we covered ***Address resolution and ARP***, where we learnt about how ARP is used to map IP addresses to MAC addresses in a local network, how to view ARP tables and how to use default gateways to enable static routing.    

There were two tutorial tasks this week, the first tasks were:
- Use the Setting-IP-12091677 project which contains four Linux hosts and one Ethernet switch. Ensure all hosts have IP addresses. We will refer to the hosts as host A, host B, host C and host D
- View the ARP table of host A (in other words, show the IP neighbours)
- Ping from host A to host B
- Again view the ARP table of host A. Identify and understand the IP addresses and hardware addresses shown in the ARP table, as well as the state (e.g., REACHABLE)
- Ping from host C to host A
- Again view the ARP table of host A and understand what has changed

Initially, I used Host A to run the command *'ip neigh show'* to show the ARP table. This returned nothing because the ARP table for Host A was empty. I then pinged from Host A to Host B and then ran the command *'ip neigh show'* again to view Host A's ARP table. This time, the ARP table showed the IP, MAC address and port of Host B. I then pinged from Host C to Host A and viewed Host A's ARP table, it now showed Host B and Host C's IP, MAC and port. Host B's ARP table had changed from 'REACHABLE' to 'STALE', but remained in the table. A screenshot of the outputs can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week6/ARP-Basics-12091677-HostA-Table.png).    

The second tutorial tasks were:
- Create project named Default-Gateway-12091677. You may duplicate the View-Routes-12091677 project or start from a new project.
- Create a network with two Linux Hosts connected to a Linux Router 1 via one Ethernet switch in one subnet, another two Linux Hosts connected to a second Linux Router 2 via another Ethernet switch in a second subnet, and the two routers connected directly together to form a third subnet. In total, there are 4 hosts, 2 switches and 2 routers, creating 3 subnets
- Using the /etc/network/interfaces configuration on all hosts/routes: set IPv4 address for the devices; set gateways (default routers) where relevant; enable forwarding on the routers; and disable forwarding on all the hosts. Your teacher may advise you to use a specific network address
- Start all nodes
- View the routing table of each device
- Test your network with ping

A screenshot of the network, showing 4x Linux hosts, 2x ethernet switches and 2x routers, creating 3 subnets can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week6/Default-Gateway-12091677-network.png). The addition of coloured boxes separating the subnets makes it much easier to follow.   
IP addresses, gateways and forwarding was configured on each host and router, all nodes were then started and routing tables were viewed on each device, screenshots can be viewed below:   
-[Host 1 routing table](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week6/Default-Gateway-12091677-host1-routing-table.png)    
-[Host 2 routing table](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week6/Default-Gateway-12091677-host2-routing-table.png)     
-[Host 3 routing table](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week6/Default-Gateway-12091677-host3-routing-table.png)     
-[Host 4 routing table](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week6/Default-Gateway-12091677-host4-routing-table.png)     
-[Router 1 routing table](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week6/Default-Gateway-12091677-router1-routing-table.png)     
-[Router 2 routing table](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week6/Default-Gateway-12091677-router2-routing-table.png)    

I tried to ping between Host 1 and Host 3 and was unsucessful. I checked all configurations and they all looked good, so I then deleted all links between devices. I then re-added the links and tried pinging from Host 1 to Host 4 and was successful. A screenshot of the ping can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week6/Default-Gateway-12091677-ping.png).     
A copy of the *GNS3* project can be downloaded [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week6/Default-Gateway-12091677.gns3project).   


