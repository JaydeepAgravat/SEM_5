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










