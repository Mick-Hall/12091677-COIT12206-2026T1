# Week 5   

In Week 5 we covered ***Switching and Virtual LANs***, where we learnt in depth about switches, VLAN's and how/what that data does as it travels between devices. In the tutorial, we configured vlan's on a managed switch and a router, configured access and trunk ports on the switch and learned more new commands. 

There were two tutorial tasks this week, the first tasks were:
- Create project named Vlan-Basics-12091677
- Add four (4) nodes of type Linux Host and one node of type OpenvSwitch. Connect the four hosts direct to the switch starting from port eth1 and up, leaving eth0 on the switch unused
- Set the IP addresses of all hosts to use the same subnet
- Start all five nodes
- Test connectivity between each host
- Configure the switch so two hosts are on one VLAN, and the other two hosts on a different VLAN. Using VLAN IDs based on the last three digits of my student ID (12091677).
- Test connectivity between each host, and view the ARP tables

A screenshot of the network, showing 4x Linux hosts and one switch, all on the one subnet can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week5/Vlan-Basics-12091677-network.png).    
Connectivity was tested between hosts and I found that I couldn't ping any host at all until I ran the command on the switch *'sh /etc/openvswitch/init.sh'*. Once this command was entered, I could ping each host from Host 1.    
The switch was then configured so Host 1 on port eth1 and Host 2 on port eth2 were on vlan 677, and Host 3 on port eth3 and Host 4 on eth4 were on vlan 678 using the commands *'ovs-vsctl set port eth1 tag=677'*, *'ovs-vsctl set port eth2 tag=677'*, *'ovs-vsctl set port eth3 tag=678'* and *'ovs-vsctl set port eth4 tag=678'*.   
A screenshot of the tagged ports can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week5/Vlan-Basics-12091677-ports.png).    
Connectivity was then tested between hosts, and I found that I could ping from Host 1 to Host 2 because it was on the same subnet, but I couldn't ping Host 3 or 4 on the different subnet.   
A copy of the *GNS3* project can be downloaded [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week5/Vlan-Basics-12091677.gns3project).    

The second turorial tasks were:
- Copy the project Vlan-Basics-12091677 to a new project Vlan-Router-12091677
- Add a Linux Router node to the project, connecting to port eth0 of the switch
- Set the IP addresses of two hosts to be on one IP subnet, and the other two hosts on a different IP subnet
- Start all nodes
- Configure two different VLANs on the access ports of the switch (similar to VLAN Basics task)
- Configure the eth0 port of the switch as a trunk port accepting all VLAN IDs
- Configure the router interface to support the two VLANs, assigning an IP address for each VLAN sub-interface
- Test connectivity between each host, ensuring all hosts have connectivity

A screenshot of the network, showing 4x Linux hosts, 1x switch and 1x router on two different subnets can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week5/Vlan-Router-12091677-network.png).   
The switch was configured so vlan's 677 and 678 were on access ports using the same commands used to configure the switch in the first task. The switch was then configured so port eth0 (that now had a router connected) was a trunk port allowing the two vlan's using the command *'ovs-vsctl set port eth0 trunks=677,678'*.    
A screenshot of the tagged access and trunked switch ports can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week5/Vlan-Router-12091677-ports.png).   
The router was then configured so eth0 could carry two vlan's by creating two sub-interfaces on eth0. The command *'ip link add link eth0 name eth0.677 type vlan id 677'* and *'ip link add link eth0 name eth0.678 type vlan id 678'* was used to create the two sub-interfaces for each vlan.  
The sub-interfaces were then assigned IP addresses using the command *'ip address add 10.10.1.1/24 dev eth0.677'* and *'ip address add 10.10.2.1/24 dev eth0.678'*, and finally the links were turned on using the command *'ip link set dev eth0.677 up'* and *'ip link set dev eth0.677 up'*.    
A screenshot of the router config can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week5/Vlan-Basics-12091677-router-config.png).    
When I checked connectivity, I tried multiple ways but I couldn't ping from vlan 677 to vlan 678. I tried allowing forwarding on the router using the command *'up sysctl net.ipv4.ip_forward=1'* but still had no success. I put this down to router configuration, the communication on both subnets was fine, but the communication between the two subnets failed. I could ping the router interfaces on both subnets, but not between the two subnets.    
A copy of the *GNS3* project can be downloaded [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week5/Vlan-Router-12091677.gns3project).     





