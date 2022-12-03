# Application Layer

- The application layer in the OSI model is the closest layer to the end user which means that the application layer and end user can interact directly with the software application.
- This layer allows users to send data, access data and use networks.
- The application layer programs are based on client and servers.

##### Functions of the application layer

- Identifying communication partners
- Determining resource availability
- Synchronizing communication

##### Services of Application Layers

1. Mail Services
- An application layer provides Email forwarding and storage.
2. Directory Services
- An application contains a distributed database that provides access for global information about various objects and services.
3. Authentication
- It authenticates the sender or receiver's message or both.
4. File Transfer, Access, and Management (FTAM)
- An application allows a user to access files in a remote computer, to retrieve files from a computer and to manage files in a remote computer. 
- FTAM defines a hierarchical virtual file in terms of file structure, file attributes and the kind of operations performed on the files and their attributes.
5. Network Virtual terminal
- An application layer allows a user to log on to a remote host.

##### Application layer protocols 
1. Telnet
2. FTP
3. SMTP
4. DNS
5. DHCP

# Network Applications

- A Network application is an application running on one host and provides
communication to another application running on a different host.
- A network application development is writing programs that run on
different end systems and communicate with each other over the network.
- In the Web application, there are two distinct programs that communicate with each
other: the browser program running in the user's host; and the Web server program
running in the Web server host.

###### Examples of network applications are
- e-mail
- web
- text messaging
- remote login
- P2P file sharing
- multi-user network games
- streaming stored video (YouTube)
- voice over IP (e.g., Skype)
- real-time video conferencing
- social networking

# Network Application Architectures

- There are two possible structure of applications
1. Client-Server architecture
2. P2P (Peer to Peer) architecture

##### Client-Server architecture
- In a client-server architecture, there is an always-on host, called the server, which provides
services requested from many other hosts, called clients.
- A classic example is the Web application for which an always-on Web server services requests
from browsers running on client hosts. When a Web server receives a request for an object from
a client host, it responds by sending the requested object to the client host.
- Note that with the client-server architecture, clients do not directly communicate with each
other; for example, in the Web application, two browsers do not directly communicate with
each other.
- Another characteristic of the client-server architecture is that the server has a fixed, well-known
address, called an IP address. Because the server is always on, a -client can always contact the
server by sending a packet to the server’s IP address.
- Some of the better-known applications with client-server architecture include the Web, FTP,
Telnet, and e-mail.

##### P2P architecture
- In P2P architecture, there is no dedicated server.
- Pairs of hosts, called peers communicate directly with each other.
- Because the peers communicate without passing through a dedicated server, the architecture is called peer-to-peer.
- Many of today’s most popular and traffic-intensive applications are based on P2P architectures. 

# Processes Communicating

- process is a program under execution.
- Processes on two different end systems communicate with each other by exchanging messages across the computer network.
- A process that initiates the communication is called the client. 
- A process that waits to be contacted to begin the session is called the server.

# Socket

- Any message sent from one process to another must go through the underlying network.
- A process sends messages into and receives messages from, the network through a software
interface called a socket.
- A process is similar to a house and its socket is similar to its door.
- When a process wants to send a message to another process on another host, it shoves (passes) the message out its door
(socket).
- This sending process assumes that there is a transportation infrastructure on the other side of its door that will transport the message to the door of the destination process.
- Once the message arrives at the destination host, the message passes through the receiving process’s door (socket), and the receiving process then acts on the message.

<img src="https://i.stack.imgur.com/4APkp.png">

# Transport Services available to Applications

##### Reliable Data Transfer

- Reliable data transfer is to guarantee that the data sent by one end of the application is
delivered correctly and completely to the other end of the application.
- If a protocol provides such a guaranteed data delivery service, it is said to provide reliable data
transfer.
- One important service that a transport-layer protocol can potentially provide to an application is
process-to-process reliable data transfer.
- When a transport protocol provides this service, the sending process can just pass its data into
the socket and know with complete confidence that the data will arrive without errors at the
receiving process.

##### Throughput

- Throughput is the rate at which the sending process can deliver bits to the receiving process.
- The transport protocol ensures that the available throughput is always at least r bits/sec.

##### Timing

- A transport-layer protocol can also provide timing guarantees.
- An example guarantee might be that every bit that the sender pumps into the socket arrives at
the receiver’s socket no more than 100 msec later. Such a service would be appealing to
interactive real-time applications, such as Internet telephony, virtual environments,
teleconferencing, and multiplayer games, all of which require tight timing constraints on data
delivery in order to be effective.
Security
- Finally, a transport protocol can provide an application with one or more security services.
- For example, in the sending host, a transport protocol can encrypt all data transmitted by the
sending process, and in the receiving host, the transport-layer protocol can decrypt the data
before delivering the data to the receiving process.

