---
layout: post
tags: [OSI MODEL]
title: "The OSI Model"
permalink: /OSI-Model
---

## Task 1 - What is the OSI Model
---

The OSI Model (Open Systems Interconnections) is a  birds eye view  how different network devices communicate with each other.

Here's an acronym to remember it:  

Here's an acronym to help remember the layers of the OSI model in order from layer 1 to layer 7:

**Please Do Not Throw Sausage Pizza Away**

The layers are:
-  **Physical**  
-  **Data Link**  
-  **Network**     
-  **Transport**  
-  **Session**  
-  **Presentation**  
- **Application**

![](osimodel.png)

At every individual layer that data travels through, specific processes take place, and pieces of information are added to this data  this process is called encapsulation.





### Answer the Questions Below

**Question:**  
What does the "OSI" in "OSI Model" stand for?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  Open Systems Interconnection
</details>

<br>
<br>


**Question:**  
How many layers (in digits) does the OSI model have?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  7
</details>

<br>
<br>


**Question:**  
What is the key term for when pieces of information get added to data?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  Encapsulation
</details>

<br>
<br>

## Task 2 - Layer 7 - Application
---

The Application Layer (Layer 7) is the part of the OSI model where humans interact with the network. It's the layer you use whenever you browse the internet, send an email, or use an app on your phone or computer. It provides services directly to you, the user, and makes sure that the data you're sending or receiving is ready to be displayed or used by the programs you interact with. The Platform that allows you to interact with is known as the GUI (As covered in the into to offensive to security section)


**Question:**  
What is the name of this Layer?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  Application
</details>

<br>
<br>


**Question:**  
What is the technical term that is given to the name of the software that users interact with?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  Graphical User Interface
</details>


## Task 3 - Layer 6 - Presentation
---

This layer is the translator of data when data is sent or received. So that the information being sent or received by the computer can be understood by the device. This done through a translator


**Question:**  
What is the name of this Layer?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  Presentation
</details>

<br>
<br>


**Question:**  
What is the main purpose that this Layer acts as?(hint:This layer translates data from one format to another)

<details>
  <summary><strong>Click to see Answer</strong></summary>
Translator
</details>


## Task 4 - Layer 5 - Session
---


The session layer (layer 5) synchronises the two computers to ensure that they are on the same page before data is sent and received. Once these checks are in place, the session layer will begin to divide up the data sent into smaller chunks of data and begin to send these chunks (packets) one at a time. This dividing up is beneficial because if the connection is lost, only the chunks that weren't yet sent will have to be sent again — not the entire piece of the data (think of it as loading a save file in a video game).

What is worthy of noting is that sessions are unique — meaning that data cannot travel over different sessions, but in fact, only across each session instead.


For example, when you're on a video call, the session layer helps keep the connection alive and ensures data is properly synchronized between the two devices.

**Question:**  
What is the name of this Layer?


<details>
  <summary><strong>Click to see Answer</strong></summary>
Session
</details>

<br>
<br>

**Question:**  
What is the technical term for when a connection is successfully established?


<details>
  <summary><strong>Click to see Answer</strong></summary>
Session
</details>

<br>
<br>

**Question:**  
What is the technical term for "small chunks of data"?

<details>
  <summary><strong>Click to see Answer</strong></summary>
Packets
</details>





## Task 5 - Layer 4 - Transport
---

The Transport Layer is like a traffic controller. It makes sure that data is sent and received correctly between devices. If any data gets lost along the way, it will resend it, ensuring everything arrives in order. It's like sending multiple packages through the mail and making sure they arrive at their destination in the correct order and without anything missing.
 ![](Tcpinaction.png)

 This made possible through 2 protocols, TCP(Transmission Control Protocol) and UDP (User Datagram Protocol). **TCP** functions by where the sender sends broken packets of where the receiver re-arranges the packets to ensure it get the whole message

TCP is used for situations such as file sharing, internet browsing or sending an email. This usage is because these services require the data to be accurate and complete (no good having half a file!).





  Here are their advantages and disadvantages.
 ![](tcpadv.png)


![](udpinaction.png)
The **UDP** functions by sending  the packets without checking whether the packets we received or not. However it does have it merits

UDP is useful in situations where there are small pieces of data being sent. For example, protocols used for discovering devices (ARP and DHCP that we discussed in Room 2 - Intro to LAN) or larger files such as video streaming (where it is okay if some part of the video is pixelated. Pixels are just lost pieces of data!)





![](udpadv.png)


**Question:**  
What is the name of this Layer?

<details>
  <summary><strong>Click to see Answer</strong></summary>
Transport
</details>

<br>
<br>


**Question:**  
What does TCP stand for?

<details>
  <summary><strong>Click to see Answer</strong></summary>
Transmission Control Protocol
</details>

<br>
<br>


**Question:**  
What does UDP stand for?

<details>
  <summary><strong>Click to see Answer</strong></summary>
User Datagram Protocol
</details>

<br>
<br>

**Question:**  
What protocol guarantees the accuracy of data?

<details>
  <summary><strong>Click to see Answer</strong></summary>
TCP
</details>

<br>
<br>

**Question:**  
What protocol doesn't care if data is received or not by the other device?

<details>
  <summary><strong>Click to see Answer</strong></summary>
UDP
</details>

<br>
<br>

**Question:**  
What protocol would an application such as an email client use?

<details>
  <summary><strong>Click to see Answer</strong></summary>
TCP
</details>

<br>
<br>

**Question:**  
What protocol would an application that downloads files use?

<details>
  <summary><strong>Click to see Answer</strong></summary>
TCP
</details>

<br>
<br>

**Question:**  
What protocol would an application that streams video use?

<details>
  <summary><strong>Click to see Answer</strong></summary>
UDP
</details>



## Task 6 - Layer 3 - Network
---
The Network Layer is like the GPS or map for data. It figures out the best route for the data to travel from one device to another, even if they're far apart. This is done by the OSPF(Open Shortest Path First) and RIP(Routing Information Protocol) It breaks the data into packets and directs them across the internet or network to reach the right IP address.


**Question:**  
What is the name of this Layer?

<details>
  <summary><strong>Click to see Answer</strong></summary>
Network
</details>

<br>
<br>

**Question:**  
Will packets take the most optimal route across a network? (Y/N)
<details>
  <summary><strong>Click to see Answer</strong></summary>
 Y
</details>

<br>
<br>

**Question:**  
What does the acronym "OSPF" stand for?


<details>
  <summary><strong>Click to see Answer</strong></summary>
 Open Shortest Path First
</details>

<br>
<br>

**Question:**  
What does the acronym "RIP" stand for?

<details>
  <summary><strong>Click to see Answer</strong></summary>
 Routing Information Protocol
</details>

<br>
<br>

**Question:**  
What type of addresses are dealt with at this layer?(Devices on a network use these. For example, 192.168.1.100)

<details>
  <summary><strong>Click to see Answer</strong></summary>
 IP Addresses
</details>






## Task 7 - Layer 2 - Data Link
---
The Data Link Layer is like a postman, making sure the data is delivered from one device to another within the same local network (like your home or office network on the network interface card ). It’s responsible for error detection and correction, ensuring that the data being transmitted is accurate and doesn't have any issues.

**Question:**  
What is the name of this Layer?

<details>
  <summary><strong>Click to see Answer</strong></summary>
Data Link
</details>


<br>
<br>

**Question:**  
What is the name of the piece of hardware that all networked devices come with?

<details>
  <summary><strong>Click to see Answer</strong></summary>
Network Interface Card
</details>




## Task 8 - Layer 1 - Physical
---
The Physical Layer is the hardware layer, dealing with the actual physical connections, like  ethernet cables, switches, Wi-Fi signals, and anything that physically transfers data. It’s the layer that sends electrical signals, light signals (in fiber optics), or radio waves (in wireless) to transmit the data. All of this information is relayed to the computer in their language as something called binary


**Question:**  
What is the name of this Layer?
<details>
  <summary><strong>Click to see Answer</strong></summary>
Physical
</details>

<br>
<br>

**Question:**  
What is the name of the numbering system that is both 0's and 1's?

<details>
  <summary><strong>Click to see Answer</strong></summary>
Binary
</details>

<br>
<br>

**Question:**  
What is the name of the cables that are used to connect devices?

<details>
  <summary><strong>Click to see Answer</strong></summary>
Ethernet Cables
</details>


## Task 9 - Practical - OSI Game
---
**Question:**  
Escape the dungeon to retrieve the flag. What is the flag? (Hint: Use the OSI MODEL to guide you)


<details>
  <summary><strong>Click to see Answer</strong></summary>
  THM{OSI_DUNGEON_ESCAPED}
</details>


## Task 10 - Continue Your Learning: Packets & Frames
---

[Packets & Frames](/packets&frames)
