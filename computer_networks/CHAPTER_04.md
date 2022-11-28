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
4. Logical Addressing 
- The data link layer executes the physical addressing, and the network layer performs logical addressing. 
- It can use it to determine between source and destination system.
5. Internetworking 
- This is the network layer’s central role that provides a logical connection between different networks types.
6. Fragmentation 
- Fragmentation breaks the packets into the minimal single data units that traverse through multiple networks.



#### services which are expected from the network layer are:  
1. Error Control 
2. Flow Control 
3. Congestion Control 

# Network service model
- The network service model defines the characteristics of end-to-end transport of data between one "edge" of the network and the other.
- i.e., between sending and receiving end systems.

#### Services provided by network layer for individual datagrams

1. Guaranteed delivery: This service guarantees that the packet will eventually arrive at itsdestination.
2. Guaranteed delivery with bounded delay: This service not only guarantees delivery of the packet, but delivery within a specified host-to-host delay bound (for example, within 100 msec).

#### Services provided by network layer for a flow of datagrams

3. In-order packet delivery: This service guarantees that packets arrive at the destination in the order that they were sent.
4. Guaranteed minimal bandwidth: This network-layer service emulates the behaviour of a transmission link of a specified bit rate (for example, 1 Mbps) between sending and receiving hosts. As long as the sending host transmits bits at a rate below the specifiedbit rate, then no packet is lost.
5. Guaranteed maximum jitter: This service guarantees that the amount of time between the transmission of two successive packets at the sender is equal to the amount of time between their receipt at the.
6. Security services: Using a secret session key known only by a source and destination host, the network layer in the source host could encrypt the payloads of all datagrams being sent to the destination host. The network layer in the destination host would then be responsible for decrypting the payloads. With such a service, confidentiality would be provided to all transport-layer segments (TCP and UDP) between the source and destination hosts.

# Datagram Switching vs Virtual Circuit 

|                                                                                     Datagram Switching                                                                                      |                                                                                                     Virtual Circuit                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| It is connection less service. There is no need for reservation of resources as there is no dedicated path for a connection session.                                                        | Virtual circuits are connection-oriented, which means that there is a reservation of resources like buffers, bandwidth, etc. for the time during which the new setup VC is going to be used by a data transfer session. |
| All packets are free to use any available path. As a result, intermediate routers calculate routes on the go due to dynamically changing routing tables on routers.                         | The first sent packet reserves resources at each server along the path. Subsequent packets will follow the same path as the first sent packet for the connection time.                                                  |
| Data packets reach the destination in random order, which means they need not reach in the order in which they were sent out.                                                               | Packets reach in order to the destination as data follows the same path.                                                                                                                                                |
| Every packet is free to choose any path, and hence all the packets must be associated with a header containing information about the source and the upper layer data.                       | All the packets follow the same path and hence a global header is required only for the first packet of connection and other packets will not require it.                                                               |
| Datagram networks are not as reliable as Virtual Circuits.                                                                                                                                  | Virtual Circuits are highly reliable.                                                                                                                                                                                   |
| Efficiency high, delay more                                                                                                                                                                 | Efficiency low and delay less                                                                                                                                                                                           |
| But it is always easy and cost-efficient to implement datagram networks as there is no need of reserving resources and making a dedicated path each time an application has to communicate. | Implementation of virtual circuits is costly as each time a new connection has to be set up with reservation of resources and extra information handling at routers.                                                    |
| A Datagram based network is a true packet switched network. There is no fixed path for transmitting data.                                                                                   | A virtual circuit network uses a fixed path for a particular session, after which it breaks the connection and another path has to be set up for the next session.                                                      |
| Widely used in Internet                                                                                                                                                                     | Used in X.25, ATM(Asynchronous Transfer Mode)                                                                                                                                                                           |
