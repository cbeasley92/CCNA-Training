# Understanding TCP/IP Transport Layer

## TCP/IP Transport Layer Functions
Residing between the application and internet layers, the transport layer is fundamental to the operation of the TCP/IP layerd network architecture.

### TCP and UDP Transport
  * Session multiplexing
  * Identification of different applications
  * Segmentation (When required)
  * Flow control (When required)
  * Connection-oriented (When required)
  * Reliability

### Session Multiplexing
Session multiplexing is and activity in which a single computer with a single IP address is able to support multiple sessions simultaneously

### Identifying the Applications
To pass data streams to the proper applications, the transport layer must identify the target application

### Segmentation
TCP pass data streams to the proper application layers and prepares them for shipment onto the network

### Flow Control
If a sender transmits data faster than the receiver can receive it, the receiver drops the data and requires it to be retransmitted

### Connection-Oriented Transport Protocol
Within the transport layer, a connection-oriented protocol, such as TCP, establishes the session connection and then maintains the connection during the entire transmission

### Reliability
TCP reliability has these three main objectives:
  * Recognition and correction of data loss
  * Recognition and correction of duplicate or out-of-order data
  * Avoidance of congestion in the network


