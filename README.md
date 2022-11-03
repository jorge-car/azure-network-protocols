<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>This project observes various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Actions and Observations</h2>

<p>
<img src="https://i.postimg.cc/KYDMzLmb/2022-11-02-54.png" height="50%" width="50%" alt="Powershell"/>
</p>

<p>
  <h2>What we are doing</h2>
  
To observe diffrent traffic between two diffrent clinets we first need two virtual machines created in microsoft azure that will act as the clinets.
the Vms will have a diffrent operating systems linux and windows.

<img src="https://i.postimg.cc/Jn9DYQqb/2022-11-02-53.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>


<h2>ICMP traffic( commands: ping,-t)</h2>

We can use the serch bar to filter to certain traffic such as icmp. Using Microsoft powershell we can use the private ip address of the other Vm and the command ping. Traffic will be sent and receieved between the two clinets. Usinng the same line of code and add the command -t we can have a constant steam of traffic being sent out.

<img src="https://i.postimg.cc/zXqXzMVy/2022-11-02-41.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

Certain traffic can also be blocked by going into microsoft azure and using Secruity rules we can make a rule that blocks certain traffic from being recieved. in the example we block the icmp traffic being sent by the first clinet from the second.

<img src="https://i.postimg.cc/1XCTZf8c/2022-11-02-55.png" height="80%" width="50%" alt="Disk Sanitization Steps"/>
<h2>SSH Traffic</h2>

SSH traffic can be observed by filtering for it in the serch bar. Then in client one using the command ssh(username of vm2)(and the private ping of the client). shown in the picture. then saying yes we get ssh trffic and using ctrl c we can stop and exit the traffic

<img src="https://i.postimg.cc/0yJFYPNW/2022-11-02-56.png" height="80%" width="50%" alt="Disk Sanitization Steps"/>


<h2>DHCPTraffic</h2>

DHCP helps give our client to be assigned an ip address upon start up or when a an ip address is needed. we say ipconfig /renew we can recieve a new ip address and we can observe the dhcp traffic being created when the ip address is being reissued.

<h2>DNS traffic</h2>

DNS traffic happens in the backend of the client all the time so we can see that some of the traffic is being shown in the photo. We can use the command nsalookup to observe the DNS traffic of our client to an online website such as www.disney.com Example in the photo

<img src="https://i.postimg.cc/pX31X4BD/2022-11-02-51.png" height="80%" width="50%" alt="Disk Sanitization Steps"/>

<img src="https://i.postimg.cc/YSzXR9B3/2022-11-02-52.png" height="80%" width="50%" alt="Disk Sanitization Steps"/>


This project showed diffrent kinds of traffic and how we were able to observe them by using our tools :)

<br />
