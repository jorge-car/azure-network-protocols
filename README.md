<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>This porjects observes various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create two diffrent clinets using VMs in Microsoft Azure
- Create a consistent/nonstop ping to observe icmp traffic. block and re enable the traffic using microsoft azure
- install wire shark and command line observe diffrent network types and thier connection to the other client
- Filter the diffrent network traffic in wire sharkwire shark and command line observe diffrent network types and thier connection to the other client


<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To observe diffrent traffic between two diffrent clinets we first need two virtual machines create in microsoft azure that will act as the clinets.
the Vms will have a diffrent operating systems linux and windows. In the first picture we can observe traffic in wire shark that is constanly being sent and recieved this just daily activty that clients have while being operated.

ICMP traffic( commands: ping,-t)

We can use the serch bar to filter to certain traffic such as icmp. Using Microsoft powershell we can use the private ip address of the other Vm and the command ping. Traffic will be sent and receieved between the two clinets. Usinng the same line of code and add the command -t we can have a constant steam of traffic being sent out.

Certain traffic can also be blocked by going into microsoft azure and using Secruity rules we can make a rule that blocks certain traffic from being recieved. in the example we block the icmp traffic being sent by the first clinet from the second.

SSH Traffic
SSH traffic can be observed by filtering for it in the serch bar. Then in client one using the command ssh(username of vm2)(and the private ping of the client). shown in the picture. then saying yes we get ssh trffic and using ctrl c we can stop and exit the traffic

DHCPTraffic

DHCP helps give our client to be assigned an ip address upon start up or when a an ip address is needed. we say ipconfig /renew we can recieve a new ip address and we can observe the dhcp traffic being created when the ip address is being reissued.

DNS traffic
DNS traffic happens in the backend of the client all the time so we can see that some of the traffic is being shown in the photo. We can use the command nsalookup to observe the DNS traffic of our client to an online website such as google. Example in the photo


using wire shark we can observe the diffrent kinds of traffic  such as SSH, DHCP,DNS, and RPD. going into wire shark we can see that we can filter the traffic using the serch bar 
</p>

<br />
