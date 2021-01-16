The OSI Model is a conceptual framework that is used to describe how a network functions. 
In plain English -> standardize the way computer systems send information to each other.

Learning objectives:
1. What is OSI model?
2. Purpose of each of the 7 layers
3. Problems that can happen at each of the 7 layers
4. Difference between TCP/IP model and OSI model

Terms:
Nodes: physical electronic device hooked up to a network, capable of sending or receiving info. over a network   

Links: it connects nodes on a network, it can be wired/cable-free   

Protocol: mutually agreed upon set of rules that allows two nodes on a network to exchange data  

Network: a group of computers, printers, or any other device that wants to share data  

Topology: it describes how nodes and links fit together in a network configuration

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

Layer 1 -> Physical layer
Includes everything from physical network devices, cabling , to how the cables hook up to the devices.
The data unit is the bit.
A bit is the smallest unit of transmittable digital information. Bits are binary. Bytes consist of 8 bits.
Nodes can send, receive, or send and receive bits.

Single transmission method:
1. Only send or receive -> simplex
2. Both send and receive -> duplex (send and receive at the same time, then full else half)


Layer 2 -> Data Link Layer
Defines how data is formatted for transmission, how data flows between nodes, for how long and what to do when errors are detected.
It is mostly concerned for error detection, not error correction.
There are 2 distinct sublayers in layer 2:
- Media Access Control(MAC): it handles the assignment of a hardware identification number, called a MAC address. NO two devices should have the same MAC address.
- Logical Link Control(LLC): it handles framing addressing and flow control.
The data unit is the frame.
Each frame contains a frame header, body, and a frame trailer.
Header: contains MAC address for source and dest
Body: contains bits being transmitted
Trailer: includes error detection information










