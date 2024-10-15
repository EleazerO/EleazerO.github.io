---
layout: post
tags: [Networking]
title: "Networking"
permalink: /what-is-networking
---
## Task 1 - What is Networking ##

Put simply, networks are group of devices connected together.
![whatisanetwork](whatisanetwork.png)

**Question**<br>
What is the key term for devices that are connected together




<br>
<br>
<br>
<br>
<br>

**Answer**
<br>
Network


## Task 2 - What is the internet ##

The internet is a vast network of smaller networks, all interconnected. These smaller networks can include local networks in homes, businesses, universities, and governments, as well as larger networks operated by internet service providers. Together, these networks form a massive, global network that allows computers and devices to communicate with each other, regardless of their physical location.



![Description of the image](internetimg.png)

#### Brief history of the internet ###

It  started in 1960s known as  the ARPANET project which was funded by the United States Defence department. This was a very basic form of internet known as the node-node communication. In 1989 the internet that we all use today was eventually  created by Tim Berners-Lee(WWW-World Wide Web)




**Question**
Who invented the World Wide Web?


<br>
<br>
<br>


**Answer**
Tim Berners-Lee




## Task 3 - identifying Devices a network
If a network is compused of many devices that are interconnected to communicate with each other, who would know who is who on the network and how would they be able to send information to who they want to. Thats when **Ip Adresses** come into play. So what is it?

**Ip(Internet Protocol) Adresses** are unique numbers used to represent a device on a network which can change over a period of time.

![Description of the image](octects.png)

These numbers are divided into 4 parts known as octets. These octets represent binary information, which is the computer's language, and they help identify the location of a computer on the network. The structure of octets allows for a large number of possible variations, ensuring that many devices can have unique IP addresses, enabling effective communication across the network.

"There are 2 types of IP addresses:

Public IP Addresses: These are used to identify a device on the **internet**. This is from your internet service provider

Private IP Addresses: These are used to identify devices within a **local network**, allowing them to communicate with each other." This given by your **router**  



![Description of the image](Public&Privateadress.png)

As we all know there are millions of millions of users on the internet which means there must be a lot public IP addresses because if one ip Addresses is the same as another person this will prevent information going to the right person. Initially public Ip addresses where using Ipv4 which had 4.29 billion addresses But was not enough. So IPV6 was created and supports ip addresses up to  340 trillion IP addresses Its 340,282,366,920,938,000,000,000,000,000,000,000,000

**MAC Addresses**
Every Computer that can connect to the internet has a network interface card.  The mac address is for  sending information on a local network. It is made has a twelve character hexadecimal split into two's and separated by a colon.


## Questions ##


**Question**<br>
What does the term "IP" stand for


**Answer**<br>
Internet protocol



**Qustion**<br>
What is each section of an IP address called?



**Answer**<br>
Octet


**Question**<br>
 How many sections (in digits) does an IP address have?

**Answer**<br>
4

**Question**<br>
What does the term "MAC" stand for

**Answer**<br>
Media access control


## Task 4 -Ping   ##


 Ping is a network utility that measures or response time between two devices over a network, typically between your computer and a server. It operates using the ICMP (Internet Control Message Protocol) to send Echo Request packets to a target host and waits for Echo Reply packets.

 ![ping](ping.png)


In the screenshot they were pinging the private address 192.168.1.254. Ping states that we sent 6 ICMP packets which were recived in 4.16 secs.


Lets do a demo to learn how to actually ping.

## Lab Practice ##

Step 1<br>
Type in Ip address 10.10.10.10 and click on the send ping request button.

Note!  the command "-C" is basically how many packets you want to send. So in this case its 4 packets. Unto the next.


![ping](pingtest.png)


Step 2 <br>
Type in 8.8.8.8 to ping to it.....boom! There's the flag
![final ping](ping888.png)


## Questions ##

**Question**
What does protocol
does ping use

**Answer**
ICMP


**Question**
What is the syntax to ping 10.10.10.10?

**Answer**
ping 10.10.10.10

**Question**
What flag do you get when you ping 8.8.8.8

**Answer**<br>
THM{I_PINGED_THE_SERVER}


## Task 5 ##
[Intro_to_lan](intro_to_lan)


<!-- This is a comment in Markdown
#
Nice so i am  recognisable and others can recognise me on a network and have the ability so send types of information. How and where do i send the information to? This is done through Ports

#Ports are the channels where protocol can send their  information -->
