# Transport Layer

- Transport Layer is the second layer in the TCP/IP model and the fourth layer in the OSI model. 
- It is an end-to-end layer used to deliver messages to a host. 
- It is termed an end-to-end layer because it provides a point-to-point connection rather than hop-to- hop, between the source host and destination host to deliver the services reliably. 
- The unit of data encapsulation in the Transport Layer is a segment. 

#### Working of Transport Layer

- At the sender’s side: 
  - The transport layer receives data (message) from the Application layer and then performs Segmentation, divides the actual message into segments, adds source and destination’s port numbers into the header of the segment, and transfers the message to the Network layer. 

- At the receiver’s side:
  - The transport layer receives data from the Network layer, reassembles the segmented data, reads its header, identifies the port number, and forwards the message to the appropriate port in the Application layer. 

#### Responsibilities of a Transport Layer

1. Process to process delivery
2. End-to-end Connection between hosts
3. Multiplexing and Demultiplexing
4. Congestion Control
5. Flow Control
6. Data integrity and Error correction

#### Protocols of Transport Layer

1. TCP(Transmission Control Protocol)
2. UDP (User Datagram Protocol)

# Discuss transport layer multiplexing and demultiplexing concepts.

- Multiplexing and Demultiplexing services are provided in almost every protocol architecture ever designed.
- UDP and TCP perform the demultiplexing and multiplexing jobs by including two special fields in the segment headers: the source port number field and the destination port number field. 
- **Multiplexing** 
  - Gathering data from multiple application processes of the sender, enveloping that data with a header, and sending them as a whole to the intended receiver is called multiplexing. 
- **Demultiplexing**
  - Delivering received segments at the receiver side to the correct app layer processes is called demultiplexing. 
- There are two types of multiplexing and Demultiplexing : 
  1. Connectionless Multiplexing and Demultiplexing
  2. Connection-Oriented Multiplexing and Demultiplexing
  
# UDP Header

- UDP header is an 8-bytes fixed and simple header.
- The first 8 Bytes contains all necessary header information and the remaining part consist of data.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/UDP-header.png">

- Header fields: 
1. Source Port: Source Port is a 2 Byte long field used to identify the port number of the source.
2. Destination Port: It is a 2 Byte long field, used to identify the port of the destined packet.
3. Length: Length is the length of UDP including the header and the data. It is a 16-bits field.
4. Checksum: Checksum is 2 Bytes long field. It is the 16-bit one’s complement of the one’s complement sum of the UDP header, the pseudo-header of information from the IP header, and the data, padded with zero octets at the end (if necessary) to make a multiple of two octets.

# TCP Header

- The header of a TCP segment can range from 20-60 bytes. 40 bytes are for options. If there are no options, a header is 20 bytes else it can be of upmost 60 bytes. 

<img src="https://media.geeksforgeeks.org/wp-content/uploads/TCPSegmentHeader-1.png">

- Header fields: 
 
1. Source Port Address  
- A 16-bit field that holds the port address of the application that is sending the data segment. 
 
2. Destination Port Address 
- A 16-bit field that holds the port address of the application in the host that is receiving the data segment. 
 
3. Sequence Number 
- A 32-bit field that holds the sequence number, i.e, the byte number of the first byte that is sent in that particular segment. It is used to reassemble the message at the receiving end of the segments that are received out of order. 
 
4. Acknowledgement Number  
- A 32-bit field that holds the acknowledgement number, i.e, the byte number that the receiver expects to receive next. It is an acknowledgement for the previous bytes being received successfully. 
 
5. Header Length (HLEN) 
- This is a 4-bit field that indicates the length of the TCP header by a number of 4-byte words in the header, i.e if the header is 20 bytes(min length of TCP header), then this field will hold 5 (because 5 x 4 = 20) and the maximum length: 60 bytes, then it’ll hold the value 15(because 15 x 4 = 60). Hence, the value of this field is always between 5 and 15. 
 
6. Control flags 
- These are 6 1-bit control bits that control connection establishment, connection termination, connection abortion, flow control, mode of transfer etc. Their function is: 
  1. URG: Urgent pointer is valid
  2. ACK: Acknowledgement number is valid( used in case of cumulative acknowledgement)
  3. PSH: Request for push
  4. RST: Reset the connection
  5. SYN: Synchronize sequence numbers
  6. FIN: Terminate the connection

7. Window size 
- This field tells the window size of the sending TCP in bytes. 
 
8. Checksum 
- This field holds the checksum for error control. It is mandatory in TCP as opposed to UDP. 
 
9. Urgent pointer 
- This field (valid only if the URG control flag is set) is used to point to data that is urgently required that needs to reach the receiving process at the earliest. The value of this field is added to the sequence number to get the byte number of the last urgent byte. 

# TCP vs UDP

| Basis                    | Transmission control protocol (TCP)                                                                                                                                                                                    | User datagram protocol (UDP)                                                                                                                                                                                                              |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type of Service          | TCP is a connection-oriented protocol. Connection-orientation means that the communicating devices should establish a connection before transmitting data and should close the connection after transmitting the data. | UDP is the Datagram-oriented protocol. This is because there is no overhead for opening a connection, maintaining a connection, and terminating a connection. UDP is efficient for broadcast and multicast types of network transmission. |
| Reliability              | TCP is reliable as it guarantees the delivery of data to the destination router.                                                                                                                                       | The delivery of data to the destination cannot be guaranteed in UDP.                                                                                                                                                                      |
| Error checking mechanism | TCP provides extensive error-checking mechanisms. It is because it provides flow control and acknowledgment of data.                                                                                                   | UDP has only the basic error checking mechanism using checksums.                                                                                                                                                                          |
| Acknowledgment           | An acknowledgment segment is present.                                                                                                                                                                                  | No acknowledgment segment.                                                                                                                                                                                                                |
| Sequence                 | Sequencing of data is a feature of Transmission Control Protocol (TCP). this means that packets arrive in order at the receiver.                                                                                       | There is no sequencing of data in UDP. If the order is required, it has to be managed by the application layer.                                                                                                                           |
| Speed                    | TCP is comparatively slower than UDP.                                                                                                                                                                                  | UDP is faster, simpler, and more efficient than TCP.                                                                                                                                                                                      |
| Retransmission           | Retransmission of lost packets is possible in TCP, but not in UDP.                                                                                                                                                     | There is no retransmission of lost packets in the User Datagram Protocol (UDP).                                                                                                                                                           |
| Header Length            | TCP has a (20-60) bytes variable length header.                                                                                                                                                                        | UDP has an 8 bytes fixed-length header.                                                                                                                                                                                                   |
| Weight                   | TCP is heavy-weight.                                                                                                                                                                                                   | UDP is lightweight.                                                                                                                                                                                                                       |
| Handshaking Techniques   | Uses handshakes such as SYN, ACK, SYN-ACK                                                                                                                                                                              | It’s a connectionless protocol i.e. No handshake                                                                                                                                                                                          |
| Broadcasting             | TCP doesn’t support Broadcasting.                                                                                                                                                                                      | UDP supports Broadcasting.                                                                                                                                                                                                                |
| Protocols                | TCP is used by HTTP, HTTPs, FTP, SMTP and Telnet.                                                                                                                                                                      | UDP is used by DNS, DHCP, TFTP, SNMP, RIP, and VoIP.                                                                                                                                                                                      |
| Stream Type              | The TCP connection is a byte stream.                                                                                                                                                                                   | UDP connection is message stream.                                                                                                                                                                                                         |
| Overhead                 | Low but higher than UDP.                                                                                                                                                                                               | Very low.                                                                                                                                                                                                                                 |

# Connection-oriented vs Connection-less Services

| S.NO | Connection-oriented Service                                                | Connection-less Service                                           |
|------|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| 1.   | Connection-oriented service is related to the telephone system.            | Connection-less service is related to the postal system.          |
| 2.   | Connection-oriented service is preferred by long and steady communication. | Connection-less Service is preferred by bursty communication.     |
| 3.   | Connection-oriented Service is necessary.                                  | Connection-less Service is not compulsory.                        |
| 4.   | Connection-oriented Service is feasible.                                   | Connection-less Service is not feasible.                          |
| 5.   | In connection-oriented Service, Congestion is not possible.                | In connection-less Service, Congestion is possible.               |
| 6.   | Connection-oriented Service gives the guarantee of reliability.            | Connection-less Service does not give a guarantee of reliability. |
| 7.   | In connection-oriented Service, Packets follow the same route.             | In connection-less Service, Packets do not follow the same route. |
| 8.   | Connection-oriented services require a bandwidth of a high range.          | Connection-less Service requires a bandwidth of low range.        |
| 9.   | Ex: TCP (Transmission Control Protocol)                                    | Ex: UDP (User Datagram Protocol)                                  |
| 10.  | Connection-oriented requires authentication.                               | Connection-less Service does not require authentication.          |

# Flow control vs Congestion control

| S.NO | Flow Control                                                                                                                                                                                                                             | Congestion Control                                                                                                                                                                    |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.   | Traffic from sender to receiver is controlled, to avoid overwhelming the slow receiver.                                                                                                                                                  | Traffic entering the network from a sender is controlled by reducing rate of packets.   Here, the sender has to control/modulate his own rate to achieve optimal network utilization. |
| 2.   | Flow control is typically used in data link layer.                                                                                                                                                                                       | Congestion control is applied in network and transport layer.                                                                                                                         |
| 3.   | In this, Receiver’s data is prevented from being overwhelmed.                                                                                                                                                                            | In this, Network is prevented from congestion.                                                                                                                                        |
| 4.   | In flow control, sender needs to take measures to avoid receiver from being overwhelmed depending on feedback from receiver and also in absence of any feedback.                                                                         | In this, many algorithms designed for transport layer/network layer define how endpoints should behave to avoid congestion.                                                           |
| 5.   | Types of Flow control are    Stop and Wait – For every frame transmitted, sender expects ACK from receiver. Sliding Window – ACK needed only after sender transmits data until window is full, which is allocated initially by receiver. | Mechanisms designed to prevent network congestions are  Network Queue Management Explicit Congestion Notification  TCP Congestion control                                             |







