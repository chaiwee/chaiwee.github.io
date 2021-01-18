---
layout: post
title: OSI Model in Plain English
---


**Learning objectives:**  
**1. What is OSI model?**  
**2. Purpose of each of the 7 layers**  

## 1. What is OSI model?  
The OSI Model is a conceptual framework that is used to describe how a network functions.   
In plain English -> standardize the way computer systems send information to each other.


Terms:  
**Nodes:** physical electronic device hooked up to a network, capable of sending or receiving info. over a network   

**Links:** it connects nodes on a network, it can be wired/cable-free   

**Protocol:** mutually agreed upon set of rules that allows two nodes on a network to exchange data  

**Network:** a group of computers, printers, or any other device that wants to share data  

**Topology:** it describes how nodes and links fit together in a network configuration

(https://lh5.googleusercontent.com/4oofyzO7Vpjz4oOAi30hEEcN8svH1Yon1SR96RKPyfC8jUeRo05nppE-r2BEXAbRH6BCrG1NPF4mtfUzmurmq5cepLtep_p0dEIytxLQithHzpBkOkzNKa8s5p1XkTtCpM2BjEHe)


What is a layer?
It is a way of organizing and grouping functionality and behaviour on and of a network.
In OSI model, layers are organized from the most tangible and physical to lesser , and closer to the end user.
Each layer abstracts lower level functionality away until by the time you get to the highest layer.


- Please | Physical Layer  
- Do | Data Link Layer  
- Not | Network Layer  
- Tell (the) | Transport Layer  
- Secret | Session Layer  
- Password (to) | Presentation Layer  
- Anyone | Application Layer  


** Be aware that the OSI model is a tool, not a set of rules.


## 2. Purpose of each of the 7 layers  


### Layer 1 Physical layer  
Includes everything from physical network devices, cabling , to how the cables hook up to the devices.
The data unit is the bit.
A bit is the smallest unit of transmittable digital information. Bits are binary. Bytes consist of 8 bits.
Nodes can send, receive, or send and receive bits.

Single transmission method:  
1. Only send or receive -> simplex  
2. Both send and receive -> duplex (send and receive at the same time, then full else half)  


### Layer 2 Data Link Layer  
Defines how data is formatted for transmission, how data flows between nodes, for how long and what to do when errors are detected.
It is mostly concerned for error detection, not error correction.
There are 2 distinct sublayers in layer 2:
- Media Access Control(MAC): it handles the assignment of a hardware identification number, called a MAC address. NO two devices should have the same MAC address.  
- Logical Link Control(LLC): it handles framing addressing and flow control.  
The data unit is the frame.  
Each frame contains a frame header, body, and a frame trailer.  
Header: contains MAC address for source and dest  
Body: contains bits being transmitted  
Trailer: includes error detection information （Error detection mechanisms examples: Cyclic Redundancy Check (CRC) and Frame Check Sequence(FCS)


### Layer 3 Network Layer  
This is where we send information between and across networks through the use of routers. Instead of node to node, we can now do network to network.  
Routers move data packets across multiple networks, they also connect to Internet Service Providers(ISP) to provide access to Internet(Once it's connected, an IP address is assigned).  
Routers store all the addressing and routing information (different paths for routing data packets across networks) in a routing tables.  
The data unit is data packet.  
Each data packet contains of frame and an IP address information wrapper.   
*** whether or not a data packet makes it to destination is not Layer 3's business ***  
IP addresses are associated with physical node's MAC addresses via Address Resolution Protocol(ARP).  



### Layer 4 Transport Layer
This specifies the connection between two nodes and how information is transmitted between them.  
It builds on the functions of Layer 2(line discipline, flow control and error control).  
This layer is also responsible for data packet segmentation(how data packets are broken up and sent over the network).  
It manages network congestion by not sending all the packets at once.  
Protocols of Layer 4:  

    1. Transmission Control Protocol(TCP)   
      - quality over speed    
      - requires handshake  
      - retry if dest does not receive all data  
      - ensure data packets are in correct order  
    2. User Datagram Protocol(UDP)  
      - speed over quality  
      - no handshake  
      - we'd never know if all data is transmitted  
      - does not ensure data packets are in correct order  


*** IP address + Port = Socket


### Layer 5 Session Layer  
This layer establishes, maintains, and terminates sessions.  
A session is a mutually agreed upon connection that is established between two network applications. ( not nodes! )  

    - Client and Server Model
    - Request and Response Model

Depending on the apps, hardware, protocols in use, session may support simplex, half-duplex or full-duplex modes.  
This layer responds to requests from presentation layer and issues request to transport layer.  
From Layer 5 and up, networks focus on ways of making connections to end-user applications and displaying data to the user.  


### Layer 6 Presentation Layer  
This layer is responsible for data formatting, such as character encoding and conversions, and data encryption.  
This layer makes sure that end-user apps operating on Layer 7 can successfully consume data and display it.  
SSL and TLS encryption protocols live on Layer 6. They help ensure that transmitted data is less vulnerable to malicious actor by providing authentication and data encryption for nodes operating on a network.  


### Layer 7 Application Layer  
This is the layer that is responsible for supporting services used by end-user applications.  
Examples : E-mail programs uses email protocols, FTP, SSH, SMTP, IMAP, DNS, HTTP  
Although this layer owns the services and functions that end-user apps need to work, the apps itself it's not included.




















