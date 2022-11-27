# Data link layer

- The Data-link layer is the second layer from the bottom in the OSI (Open System Interconnection) network architecture model.
- It is responsible for the node-to-node delivery of data.
- Its major role is to ensure error-free transmission of information.
- It is also responsible to encode, decode and organize the outgoing and incoming data.
- This is considered the most complex layer of the OSI model as it hides all the underlying complexities of the hardware from the other above layers. 

#### Sub-layers of Data Link Layer

1. Logical Link Control (LLC)
2. Media Access Control (MAC)

#### Services provided by Data Link Layer

1. Framing
  - The data link layer receives the information in the form of packets from the Network layer, it divides packets into frames and sends those frames bit-by-bit to the underlying physical layer. 
  - It also attaches some special bits (for error control and addressing) at the header and end of the frame. 
  - At the receiver’s end, DLL takes bits from the Physical layer organizes them into the frame, and sends them to the Network layer. 
2. Addressing
  - The data link layer encapsulates the source and destination’s MAC address/ physical address in the header of each frame to ensure node-to-node delivery.
  - MAC address is the unique hardware address that is assigned to the device while manufacturing. 
3. Error Control
  -  Data can get corrupted due to various reasons like noise, attenuation, etc.
  -  So, it is the responsibility of the data link layer, to detect the error in the transmitted data and correct it using error detection and correction techniques respectively. 
  -  DLL adds error detection bits into the frame’s header, so that receiver can check received data is correct or not.
4. Flow Control
  - If the receiver’s receiving speed is lower than the sender’s sending speed, then this can lead to an overflow in the receiver’s buffer and some frames may get lost.
  - So, it’s the responsibility of DLL to synchronize the sender’s and receiver’s speeds and establish flow control between them. 
5. Access Control
  - When multiple devices share the same communication channel there is a high probability of collision, so it’s the responsibility of DLL to check which device has control over the channel and CSMA/CD and CSMA/CA can be used to avoid collisions and loss of frames in the channel. 
6. Reliable delivery

# Error Detection Techniques

1. Parity Check
2. Checksum
3. Cyclic redundancy check

<img src="https://media.geeksforgeeks.org/wp-content/uploads/detect12.jpg">
<img src="https://media.geeksforgeeks.org/wp-content/uploads/detect13.jpg">
<img src="https://media.geeksforgeeks.org/wp-content/uploads/detect15.jpg">

# Ethernet

- Ethernet is one of the most widely used LAN technologies. 
- The reason behind its wide usability is Ethernet is easy to understand, implement, maintain, and allows low-cost network implementation.
- Ethernet offers flexibility in terms of topologies that are allowed.
- Ethernet generally uses Bus Topology.
- Ethernet operates in two layers of the OSI model, Physical Layer, and Data Link Layer. 
- For Ethernet, the protocol data unit is Frame since we mainly deal with DLL.
- In order to handle collision, the Access control mechanism used in Ethernet is CSMA/CD. 

#### Types of Ethernet Networks

1. Switch Ethernet
2. Fast Ethernet
3. Gigabit Ethernet

#### Advantages of Ethernet

1. Speed
2. Effectiveness
3. Good data transfer quality
4. Security
5. Fairly low cost
6. Reliability

#### Disadvantages of Ethernet

1. Connections
2. Mobility
3. Expandability

# Bit stuffing & Byte stuffing

<a href="https://www.geeksforgeeks.org/difference-between-byte-stuffing-and-bit-stuffing/">X</a>

# Address Resolution Protocol

<a href="https://www.geeksforgeeks.org/how-address-resolution-protocol-arp-works/">X</a>

# Types of Communication Links

- Communication links enable the stations to communicate with each other.

1. Point to Point Link
- Point to Point link is a dedicated link that exists between the two stations.
- The entire capacity of the link is used for transmission between the two connected stations only.
2. Broadcast Link
- Broadcast link is a common link to which multiple stations are connected.
- The capacity of the link is shared among the connected stations for transmission.
- Bus Topology

#### Access Control
- Access Control is a mechanism that controls the access of stations to the transmission link.
- Broadcast links require the access control.
- This is because the link is shared among several stations.
#### Need of Access Control-
- To prevent the occurrence of collision or if the collision occurs, to deal with it.

# Multiple Aceess Protocols / method:
<img src="https://media.geeksforgeeks.org/wp-content/uploads/2-44.jpg">

# Aloha

- There are two different versions of Aloha-
1. Pure Aloha
2. Slotted Aloha

### 1. Pure Aloha
- It allows the stations to transmit data at any time whenever they want.
- After transmitting the data packet, station waits for some time.
- Then, following 2 cases are possible :
1. Case-01:
- Transmitting station receives an acknowledgement from the receiving station.
- In this case, transmitting station assumes that the transmission is successful.
2. Case-02:
- Transmitting station does not receive any acknowledgement within specified time from the receiving station.
- In this case, transmitting station assumes that the transmission is unsuccessful.
- Then, Transmitting station uses a Back Off Strategy and waits for some random amount of time.
- After back off time, it transmits the data packet again.
- It keeps trying until the back off limit is reached after which it aborts the transmission.
#### Efficiency
- Efficiency of Pure Aloha (η) = G x e-2G
- where G = Number of stations willing to transmit data
- Maximum Efficiency of Pure Aloha (η) = 18.4%
- The maximum efficiency of Pure Aloha is very less due to large number of collisions.

### 2. Slotted Aloha

- Slotted Aloha divides the time of shared channel into discrete intervals called as time slots.
- Any station can transmit its data in any time slot.
- The only condition is that station must start its transmission from the beginning of the time slot.
- If the beginning of the slot is missed, then station has to wait until the beginning of the next time slot.
- A collision may occur if two or more stations try to transmit data at the beginning of the same time slot.

#### Efficiency

- Efficiency of Slotted Aloha (η) = G x e-G
- where G = Number of stations willing to transmit data at the beginning of the same time slot
- Maximum Efficiency of Slotted Aloha (η) = 36.8%
- The maximum efficiency of Slotted Aloha is high due to less number of collisions.

### Difference Between Pure Aloha And Slotted Aloha

|                               Pure Aloha                              |                                                           Slotted Aloha                                                           |
|:---------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------------:|
|             Any station can transmit the data at any time.            |                                Any station can transmit the data at the beginning of any time slot.                               |
|         The time is continuous and not globally synchronized.         |                                          The time is discrete and globally synchronized.                                          |
|         Vulnerable time in which collision may occur  = 2 x Tt        |                                         Vulnerable time in which collision may occur  = Tt                                        |
|   Probability of successful transmission of data packet  = G x e-2G   |                                  Probability of successful transmission of data packet  = G x e-G                                 |
|            Maximum efficiency = 18.4%  (Occurs at G = 1/2)            |                                           Maximum efficiency = 36.8%  ( Occurs at G = 1)                                          |
| The main advantage of pure aloha is its simplicity in implementation. | The main advantage of slotted aloha is that it reduces the number of collisions to half and doubles the efficiency of pure aloha. |

<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/computer_networks/NETWORK_IMG/5.01.png">
<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/computer_networks/NETWORK_IMG/5.02.png">
<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/computer_networks/NETWORK_IMG/5.03.png">

# CSMA / CD

- CSMA / CD stands for Carrier Sense Multiple Access / Collision Detection.
- CSMA / CD is used in wired LANs.
- CSMA / CD only minimizes the recovery time.
- It does not take any steps to prevent the collision until it has taken place.
- This access control method works as follows:

#### Step-01: Sensing the Carrier
- Any station willing to transmit the data through senses the carrier.
- If it finds the carrier free, it starts transmitting its data packet otherwise not.
- Each station can sense the carrier only at its point of contact with the carrier.
- It is not possible for any station to sense the entire carrier.
- there is a huge possibility that a station might sense the carrier free even when it is actually not.
#### Step-02: Detecting the Collision
- It is the responsibility of the transmitting station to detect the collision.
- For detecting the collision, CSMA / CD implements the following condition.
- This condition is followed by each station-
- `Transmission delay >= 2 x Propagation delay`
- Each station must transmit the data packet of size whose transmission delay is at least twice its propagation delay.
- If the size of data packet is smaller, then collision detection would not be possible.
```
Transmission delay = Length of data packet (L) / Bandwidth (B)
Propagation delay = Distance between the two stations (D) / Propagation speed (V)
Length Of Data Packet : L >= 2 x B x D / V
```
```
Case-01:

If no collided signal comes back during the transmission,
It indicates that no collision has occurred.
The data packet is transmitted successfully.

Case-02:

If the collided signal comes back during the transmission,
It indicates that the collision has occurred.
The data packet is not transmitted successfully.
Step-03 is followed.
```

#### Step-03: Releasing Jam Signal
- It alerts the other stations not to transmit their data immediately after the collision.

#### Step-04: Waiting For Back Off Time

- After the collision, the transmitting station waits for some random amount of time called as back off time.
- After back off time, it tries transmitting the data packet again.
- If again the collision occurs, then station again waits for some random back off time and then tries again.
- The station keeps trying until the back off time reaches its limit.
- After the limit is reached, station aborts the transmission.
- Back off time is calculated using Back Off Algorithm.
