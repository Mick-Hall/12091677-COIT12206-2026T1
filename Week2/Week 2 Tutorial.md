# Week 2

In week two we covered ***Encapsulation and Decapsulation in Network Communication***, in which we learnt how data as it travels from source to destination as it traverses the TCP/IP model. 

My Tutorial tasks on were:
- Create a new *GNS3* project
- Add four Linux hosts and one ethernet switch and connect together in a LAN
- Configure two of the hosts IP address using the *GNS3 configure* menu
- Start all nodes
- Configure both other hosts nodes using a console
- Show the configured IP address of the hosts

A screenshot of host 1's IP, configured using the *GNS3* configure menu can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week2/Setting-IP-12091677-host1.png) and host 2's IP, also configured using the *GNS3* configure menu can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week2/Setting-IP-12091677-host2.png).   
A screenshot of host 3's IP, configured using a console can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week2/Setting-IP-12091677-host3.png) and host 4's IP, also configured using a console can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week2/Setting-IP-12091677-host4.png).

My second tutorial tasks were:
- Ping from host 1 to host 2, stopping the ping after 5 responses
- View and understand the ping results
- Ping from a host to an IP that didn't exist on the network
- Ping host using different size, count and interval options

A screenshot of host 1 pinging host 2, and stopping the count after 5 responses using 'ctrl c' can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week2/Ping-Basics-12091677-simple.png).   
A screenshot of host 1 pinging the IP '10.10.0.100' can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week2/Ping-Basics-12091677-error.png). Host 1 replied *'Desination hsot unreachable'* because that IP address does not exist in the network.    
A screenshot of host 1 pinging host 4, specifying a count of 5 using -c, an interval of 2ms using -i and a size of 80 bytes using -s can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week2/Ping-Basics-12091677-options.png).   

This week i learned how to edit the text file using the command 'nano /etc/network/interfaces', uncomment out the commands to set a static IP and use the 'ifup' command to turn the virtual ethernet port on. I find this the best approach to setting a static IP because it is more challenging. I also learn handy ping options (-c, -i and -s) to specify the count, interval and size of a ping.   

A screenshot of the network with all hosts powered on can be viewed [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week2/Setting-IP-12091677-network.png).   
A copy of the *GNS3* project can be downloaded [here](https://github.com/Mick-Hall/12091677-COIT12206-2026T1/blob/main/Week2/Setting-IP-12091677.gns3project).
