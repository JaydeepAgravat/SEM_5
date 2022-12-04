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

##### Security

- Finally, a transport protocol can provide an application with one or more security services.
- For example, in the sending host, a transport protocol can encrypt all data transmitted by the
sending process, and in the receiving host, the transport-layer protocol can decrypt the data
before delivering the data to the receiving process.

# TCP vs UDP

|        Key        |                                                                                                                                TCP                                                                                                                               |                                                                                                        UDP                                                                                                        |
|:-----------------:|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
|     Definition    | It is a communications protocol, using which the data is transmitted between systems over the network. In this, the data is transmitted in the form of packets. It includes error-checking, guarantees the delivery and preserves the order of the data packets. | It is same as the TCP protocol except this doesn’t guarantee the error-checking and data recovery. If you use this protocol, the data will be sent continuously, irrespective of the issues in the receiving end. |
|       Design      | TCP is a connection-oriented protocol.                                                                                                                                                                                                                           | UDP is a connectionless protocol.                                                                                                                                                                                 |
|    Reliability    | TCP is more reliable as it provides error checking support and also guarantees delivery of data to the destination router.                                                                                                                                       | UDP, on the other hand, provides only basic error checking support using checksum. So, the delivery of data to the destination cannot be guaranteed in UDP as in case of TCP.                                     |
| Data transmission | In TCP, the data is transmitted in a particular sequence which means that packets arrive in-order at the receiver.                                                                                                                                               | There is no sequencing of data in UDP in order to implement ordering it has to be managed by the application layer.                                                                                               |
|    Performance    | TCP is slower and less efficient in performance as compared to UDP. Also TCP is heavy-weight as compared to UDP.                                                                                                                                                 | UDP is faster and more efficient than TCP.                                                                                                                                                                        |
|   Retransmission  | Retransmission of data packets is possible in TCP in case packet get lost or need to resend.                                                                                                                                                                     | Retransmission of packets is not possible in UDP.                                                                                                                                                                 |
|     Sequencing    | The Transmission Control Protocol has a function that allows data to be sequenced (TCP). This implies that packets arrive at the recipient in the sequence they were sent.                                                                                       | In UDP, there is no data sequencing. The application layer must control the order if it is necessary.                                                                                                             |
|    Header size    | TCP uses a variable-length (20-60) bytes header.                                                                                                                                                                                                                 | UDP has a fixed-length header of 8 bytes.                                                                                                                                                                         |
|     Handshake     | Handshakes such as SYN, ACK, and SYNACK are used.                                                                                                                                                                                                                | It's a connectionless protocol, which means it doesn't require a handshake.                                                                                                                                       |
|    Broadcasting   | Broadcasting is not supported by TCP.                                                                                                                                                                                                                            | Broadcasting is supported by UDP.                                                                                                                                                                                 |
|      Examples     | HTTP, HTTPs, FTP, SMTP, and Telnet use TCP.                                                                                                                                                                                                                      | DNS, DHCP, TFTP, SNMP, RIP, and VoIP use UDP.                                                                                                                                                                     |


# Web
- A Web page consists of objects.
- An object is simply a file - such as an HTML file, a JPEG image, a Java applet, or a video clip, that is addressable by a single URL.
- Most Web pages consist of a base HTML file and several referenced objects.
- For example, if a Web page contains HTML text and five JPEG images, then the Web page has six objects: the base HTML file plus the five images.
- The base HTML file references the other objects in the page with the objects’ URLs.
- Each URL has two components: the hostname of the server and the object’s path name.
- For example, the URL “http://www.someSchool.edu/someDepartment/picture.gif” has “www.someSchool.edu” is hostname and “/someDepartment/picture.gif” is a pathname.

# HTTP

- HyperText Transfer Protocol – Application layer protocol
- It is implemented in two programs.
1. Client Program
2. Server Program
- Exchanging HTTP message each others.
- HTTP defines the structure of these messages and how web client – web server exchange
messages.
- Hyper-Text Transfer Protocol
- It is Application layer protocol
##### Client:
- A browser that requests, receives, (using HTTP protocol) and “displays” Web objects.
- E.g. PC, Mobile
##### Server:
- Web server sends (using HTTP protocol)  objects in response to requests.
- E.g. Apache Web Server

##### Flow:
- A client initiates TCP connection (creates socket) to server using port 80.
- A server accepts TCP connection from client.
- HTTP messages (application-layer protocol messages) exchanged between browser (HTTP
client) and Web server (HTTP server).
- HTTP is “stateless protocol”, server maintains no information about past client requests.

##### HTTP connection types are:
1. Non-persistent HTTP
2. Persistent HTTP
- In Client-Server communication, Client making a series of requests to server, Server responding to each of the requests.
- Series of requests may be made back-to-back or periodically at regular time interval.
- So, Application developer need to make an important decision;
- Should each request/response pair be sent over a separate TCP connection.
- OR should all the requests and corresponding responses be sent over same TCP connection?

# Non-persistent HTTP

- A non-persistent connection is closed after the server sends the requested object to the client.
- The connection is used exactly for one request and one response.
- For downloading multiple objects, it required multiple connections.
- Non-persistent connections are the default mode for HTTP/1.0.
- Example: Transferring a webpage from server to client, webpage consists of a base HTML file and 10 JPEG images.
- Total 11 object are residing on server.
<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/computer_networks/NETWORK_IMG/2.1.png">
<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/computer_networks/NETWORK_IMG/2.2.png">

# Persistent HTTP

- Server leaves the TCP connection open after sending responses.
- Subsequent HTTP messages between same client and server sent over open connection.
- The server closes the connection only when it is not used for a certain configurable amount of time.
- It requires as little as one round-trip time (RTT) for all the referenced objects.
- With persistent connections, the performance is improved by 20%.
- Persistent connections are the default mode for HTTP/1.1.

# HTTP Message 
<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/computer_networks/NETWORK_IMG/2.3.png">
<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/computer_networks/NETWORK_IMG/2.4.png">

# User-Server Interaction OR Cookies
- A small text file created by a Web site that is stored in the user's computer either temporarily for that session only or permanently on the hard disk (persistent cookie).
- Cookies provide a way for the Web site to recognize you and keep track of your preferences.
###### Cookie technology has four components
1. a cookie header line in the HTTP response message
2. a cookie header line in the HTTP request message
3. a cookie file kept on the user’s end system and managed by the user’s browser
4. a back-end database at the Web site
###### Use of cookies
- authorization
- shopping carts
- recommendations
- user session state (Web e-mail)

<img src="https://miro.medium.com/max/1100/1*QOiM7Qbsb_QuRz6xFv1Hkw.webp">

# Web Caches (Proxy Server)

- It satisfies HTTP requests on the behalf of an origin Web server.
- The Web cache has its own disk storage and keeps copies of recently requested objects in this
storage.
- A user’s browser can be configured so, user’s HTTP requests are first directed to the Web
Cache.
- A browser sends all HTTP requests to cache.
- As an example, suppose a browser is requesting the object
http://www.someschool.edu/campus.gif
- Object in cache returns to client browser.
- Otherwise cache requests object from origin server, then returns object to client browser.
- Reduce response time for client request.
- Reduce traffic on an institution’s access link.
- Internet dense with caches: Insufficiency for content providers to effectively deliver content.
- Example: Institutional Network and Internet
- Reduce response time for client request.
- Reduce traffic on an institution’s access link.
- Internet dense with caches: Insufficiency for content providers to effectively deliver content.

<img src="https://o.quizlet.com/jC8W0icC1sv9-KMLxSbKdg.png">

# FTP
- File Transfer Protocol (FTP) is the commonly used protocol for exchanging files over the Network
or Internet.
- FTP uses the Internet's TCP/IP protocols to enable data transfer.
- FTP uses client-server architecture.
- FTP promotes sharing of files via remote computers with reliable and efficient data transfer.

<img src="https://netlab.ulusofona.pt/rc/book/2-application/2_03/02-13.jpg">

- In the above figure, a user interacts with FTP through an FTP user agent.
- The user first provides the hostname of the remote host, causing the FTP client process in the
local host to establish a TCP connection with the FTP server process in the remote host.
- The user then provides the user identification and password, which are sent over the TCP
connection as part of FTP commands.
- Once the server has authorized the user, the user copies one or more files stored in the local file
system into the remote file system (or vice versa).
- FTP uses two parallel TCP connections to transfer a file,
1. control connection
2. data connection

<img src="https://mscancer22.tripod.com/sitebuildercontent/sitebuilderpictures/kurose_320719_c02f14.gif" width=40%>

- The control connection is used for sending control information between the two hosts such as
user identification, password, commands to change remote directory and commands to put and
get files.
- The data connection is used to actually send a file.
- Because FTP uses a separate control connection, FTP is said to send its control information outof-band.
- When a user starts an FTP session with a remote host, the client side of FTP (user) first initiates a
control TCP connection with the server side (remote host) on server port number 21.
- The client side of FTP sends the user identification and password over this control connection.
- The client side of FTP also sends, over the control connection, commands to change the remote
directory.
- When the server side receives a command for a file transfer over the control connection (either
to or from, the remote host), the server side initiates a TCP data connection to the client side.
- FTP sends exactly one file over the data connection and then closes the data connection.
- If during the same session, the user wants to transfer another file, FTP opens another data
connection.
- Thus, with FTP, the control connection remains open throughout the duration of the user
session, but a new data connection is created for each file transferred within a session (that is,
the data connections are non-persistent).






