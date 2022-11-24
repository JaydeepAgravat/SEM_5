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
