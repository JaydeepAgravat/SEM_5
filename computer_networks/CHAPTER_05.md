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
