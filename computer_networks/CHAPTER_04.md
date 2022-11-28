# Network Layer

- Network layer is the third layer in the OSI model of computer networks.
- It’s main function is to transfer network packets from the source to the destination.
- It is involved both at the source host and the destination host.
- At the source, it accepts a packet from the transport layer, encapsulates it in a datagram and then deliver the packet to the data link layer so that it can further be sent to the receiver.
- At the destination, the datagram is decapsulated, the packet is extracted and delivered to the corresponding transport layer. 

#### Features 

1. Main responsibility of Network layer is to carry the data packets from the source to the destination without changing or using it. 
2. If the packets are too large for delivery, they are fragmented i.e., broken down into smaller packets. 
3. It decides the route to be taken by the packets to travel from the source to the destination among the multiple routes available in a network (also called as routing). 
4. The source and destination addresses are added to the data packets inside the network layer. 

#### Services 

1. Packetizing 
- Decapsulating the payload from the network layer packet at the destination is known as packetizing. 
2. Routing
- In a network, there are a number of routes available from the source to the destination.
- The network layer specifies has some strategies which find out the best possible route.
- This process is referred to as routing.
- There are a number of routing protocols which are used in this process and they should be run to help the routers coordinate with each other and help in establishing communication throughout the network. 
3. Forwarding
- Forwarding is simply defined as the action applied by each router when a packet arrives at one of its interfaces. 
- When a router receives a packet from one of its attached networks, it needs to forward the packet to another attached network (unicast routing) or to some attached networks(in case of multicast routing). 

#### services which are expected from the network layer are:  
1. Error Control 
2. Flow Control 
3. Congestion Control 
