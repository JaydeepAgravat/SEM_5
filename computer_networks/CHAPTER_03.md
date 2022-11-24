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

1. Source Port: Source Port is a 2 Byte long field used to identify the port number of the source.
2. Destination Port: It is a 2 Byte long field, used to identify the port of the destined packet.
3. Length: Length is the length of UDP including the header and the data. It is a 16-bits field.
4. Checksum: Checksum is 2 Bytes long field. It is the 16-bit one’s complement of the one’s complement sum of the UDP header, the pseudo-header of information from the IP header, and the data, padded with zero octets at the end (if necessary) to make a multiple of two octets.









