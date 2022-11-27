# Computer Network

- A computer network is a system in which multiple computers are connected to each other to
share information and resources.
- The connection between networked computing devices is established using either cable
media or wireless media. 

# Advantages of Computer Networks

- Central Storage of Data 
- Anyone can connect to a computer network 
- Faster Problem-solving 
- Reliability 
- It is highly flexible 
- Security through Authorization 
- It boosts storage capacity 

# Disadvantages of Computer Networks

- It lacks robustness 
- It lacks independence 
- Virus and Malware 
- Cost of the network 

# Application of computer network

- online bill payment
- watching movies or shows at home
- home tutoring
- social media access
- playing games
- internet access, etc.

# Type of Computer Network

| Basis                | LAN                                                           | MAN                                                        | WAN                                                                           |
|----------------------|---------------------------------------------------------------|------------------------------------------------------------|-------------------------------------------------------------------------------|
| Full-Form            | LAN stands for local area network.                            | MAN stands for metropolitan area network.                  | WAN stands for wide area network.                                             |
| Geographic Span      | Operates in small areas such as the same building or campus.  | Operates in large areas such as a city.                    | Operates in larger areas such as country or continent.                        |
| Ownership            | LAN’s ownership is private.                                   | MAN’s ownership can be private or public.                  | While WAN also might not be owned by one organization.                        |
| Transmission Speed   | The transmission speed of a LAN is high.                      | While the transmission speed of a MAN is average.          | Whereas the transmission speed of a WAN is low.                               |
| Propagation delay    | The propagation delay is short in a LAN.                      | There is a moderate propagation delay in a MAN.            | Whereas, there is a long propagation delay in a WAN.                          |
| Congestion           | There is less congestion in LAN.                              | While there is more congestion in MAN.                     | Whereas there is more congestion than MAN in WAN.                             |
| Design & Maintenance | LAN’s design and maintenance are easy.                        | While MAN’s design and maintenance are difficult than LAN. | Whereas WAN’s design and maintenance are also difficult than LAN as well MAN. |
| Fault tolerance      | There is more fault tolerance in LAN.                         | While there is less fault tolerance.                       | In WAN, there is also less fault tolerance.                                   |

# Internet

- The internet is a type of world-wide computer network.
- The internet is the collection of infinite numbers of connected computers that are spread across
the world.
- It is established as the largest network and sometimes called a network of a network.
- The Internet is a global computer network providing a variety of information and
communication facilities, consisting of interconnected networks using standardized
communication protocols.
- When two computers are connected over the Internet, they can send and receive all kinds of
information such as text, graphics, voice, video, and computer programs.

# Protocol

- A protocol is a set of rules that manages data communications.
- Protocols define methods of communication, how to communicate when to communicate etc.
- A protocol is an agreement between the communicating parties on how communication is to
proceed.
- Important elements of protocols are
- 1. Syntax 2. Semantics 3. Timing

# The Network Edge
- It defines those computers of the network used at the edge (end) of the network. These computers are known as hosts or end system.
- A host can be classified into the following two types:
1. Clients: 
- Refer to the computer systems that request servers for the completion of a task.
- The clients are generally called desktop PCs or workstations.
2. Servers:
- Refer to the computer systems that receive requests from the clients and process them. After the processing is complete, the servers send a reply to the clients who sent the request.

# Peer-to-Peer Network vs Client-Server Network     

| S.NO | Client-Server Network                                                                                     | Peer-to-Peer Network                                                                                 |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 1.   | In Client-Server Network, Clients and server are differentiated, Specific server and clients are present. | In Peer-to-Peer Network, Clients and server are not differentiated.                                  |
| 2.   | Client-Server Network focuses on information sharing.                                                     | While Peer-to-Peer Network focuses on connectivity.                                                  |
| 3.   | In Client-Server Network, Centralized server is used to store the data.                                   | While in Peer-to-Peer Network, Each peer has its own data.                                           |
| 4.   | In Client-Server Network, Server respond the services which is request by Client.                         | While in Peer-to-Peer Network, Each and every node can do both request and respond for the services. |
| 5.   | Client-Server Network are costlier than Peer-to-Peer Network.                                             | While Peer-to-Peer Network are less costlier than Client-Server Network.                             |
| 6.   | Client-Server Network are more stable than Peer-to-Peer Network.                                          | While Peer-to-Peer Network are less stable if number of peer is increase.                            |
| 7.   | Client-Server Network is used for both small and large networks.                                          | While Peer-to-Peer Network is generally suited for small networks with fewer than 10 computers.      |

# Techniques used in data communications to transfer data


| Circuit Switching                                                                                                                                                             | Packet Switching                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| In-circuit switching has there are 3 phases:  i) Connection Establishment.  ii) Data Transfer.  iii) Connection Released.                                                     | In Packet switching directly data transfer takes place.                                                                   |
| In-circuit switching, each data unit knows the entire path address which is provided by the source.                                                                           | In Packet switching, each data unit just knows the final destination address intermediate path is decided by the routers. |
| In-Circuit switching, data is processed at the source system only                                                                                                             | In Packet switching, data is processed at all intermediate nodes including the source system.                             |
| The delay between data units in circuit switching is uniform.                                                                                                                 | The delay between data units in packet switching is not uniform.                                                          |
| Resource reservation is the feature of circuit switching because the path is fixed for data transmission.                                                                     | There is no resource reservation because bandwidth is shared among users.                                                 |
| Circuit switching is more reliable.                                                                                                                                           | Packet switching is less reliable.                                                                                        |
| Wastage of resources is more in Circuit Switching                                                                                                                             | Less wastage of resources as compared to Circuit Switching                                                                |
| It is not a store and forward technique.                                                                                                                                      | It is a store and forward technique.                                                                                      |
| Transmission of the data is done by the source.                                                                                                                               | Transmission of the data is done not only by the source but also by the intermediate routers.                             |
| Congestion can occur during the connection establishment phase because there might be a case where a request is being made for a channel but the channel is already occupied. | Congestion can occur during the data transfer phase, a large number of packets comes in no time.                          |
| Circuit switching is not convenient for handling bilateral traffic.                                                                                                           | Packet switching is suitable for handling bilateral traffic.                                                              |
| In-Circuit switching, the charge depends on time and distance, not on traffic in the network.                                                                                 | In Packet switching, the charge is based on the number of bytes and connection time.                                      |
| Recording of packets is never possible in circuit switching.                                                                                                                  | Recording of packets is possible in packet switching.                                                                     |
| In-Circuit Switching there is a physical path between the source and the destination                                                                                          | In Packet Switching there is no physical path between the source and the destination                                      |
| Circuit Switching does not support store and forward transmission                                                                                                             | Packet Switching supports store and forward transmission                                                                  |
| Call setup is required in circuit switching.                                                                                                                                  | No call setup is required in packet switching.                                                                            |
| In-circuit switching each packet follows the same route.                                                                                                                      | In packet switching packets can follow any route.                                                                         |
| The circuit switching network is implemented at the physical layer.                                                                                                           | Packet switching is implemented at the datalink layer and network layer                                                   |
| Circuit switching requires simple protocols for delivery.                                                                                                                     | Packet switching requires complex protocols for delivery.                                                                 |
# Transmission Media
<img src="https://www.tutorialandexample.com/wp-content/uploads/2020/10/image-210.png" width=50%>

# Network Topologies

- A Network Topology is the arrangement of the various components of a computer network.

<img src="https://cdn.educba.com/academy/wp-content/uploads/2019/06/Types-of-network-topology-2.png" width=50%>
<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/computer_networks/NETWORK_IMG/1.01.png" width=70%>

# OSI vs TCP/IP

| OSI Model                                                                                                                                                                             | TCP/IP Model                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| It stands for Open System Interconnection.                                                                                                                                            | It stands for Transmission Control Protocol.                                                                                                                |
| OSI model has been developed by ISO (International Standard Organization).                                                                                                            | It was developed by ARPANET (Advanced Research Project Agency Network).                                                                                     |
| It is an independent standard and generic protocol used as a communication gateway between the network and the end user.                                                              | It consists of standard protocols that lead to the development of an internet. It is a communication protocol that provides the connection among the hosts. |
| In the OSI model, the transport layer provides a guarantee for the delivery of the packets.                                                                                           | The transport layer does not provide the surety for the delivery of packets. But still, we can say that it is a reliable model.                             |
| This model is based on a vertical approach.                                                                                                                                           | This model is based on a horizontal approach.                                                                                                               |
| In this model, the session and presentation layers are separated, i.e., both the layers are different.                                                                                | In this model, the session and presentation layer are not different layers. Both layers are included in the application layer.                              |
| It is also known as a reference model through which various networks are built. For example, the TCP/IP model is built from the OSI model. It is also referred to as a guidance tool. | It is an implemented model of an OSI model.                                                                                                                 |
| In this model, the network layer provides both connection-oriented and connectionless service.                                                                                        | The network layer provides only connectionless service.                                                                                                     |
| Protocols in the OSI model are hidden and can be easily replaced when the technology changes.                                                                                         | In this model, the protocol cannot be easily replaced.                                                                                                      |
| It consists of 7 layers.                                                                                                                                                              | It consists of 4 layers.                                                                                                                                    |
| OSI model defines the services, protocols, and interfaces as well as provides a proper distinction between them. It is protocol independent.                                          | In the TCP/IP model, services, protocols, and interfaces are not properly separated. It is protocol dependent.                                              |
| The usage of this model is very low.                                                                                                                                                  | This model is highly used.                                                                                                                                  |
| It provides standardization to the devices like router, motherboard, switches, and other hardware devices.                                                                            | It does not provide the standardization to the devices. It provides a connection between various computers.                                                 |


