# Understanding the TCP/IP Internet Layer

## Internet Protocol
IP Characteristics:
  * Operates at the internet layer of the TCP/IP stack
  * Connectionless protocol
  * Packets treated independently
  * Hierarchical addressing
  * Best effort delivery
  * No data-recovery features
  * Media-independent
  * Two variants IPv4 and IPv6

## IPv4 Address Representation
IP address consists of two parts
  * Network ID
  * Host ID

## IP Address Classes

### Class A
Class A address block is designed to support extremely large networks with more than 16 million host addresses

### Class B
Class B address space is designed to suppor the needs fo a moderate to large netowrks with more than 65,000 hosts

### Class C
Class C address space is the most commonly available address class

### IP Address Ranges
| IP Addrss Class | First Octet Decimal Value | First Octet Binary Value | Possible Number of Hosts |
| --- | --- | --- | --- |
| Class A | 1-126 | 00000001 to 01111110* | 16,777,214 |
| Class B | 128-191 | 10000000 to 10111111 | 65,534 |
| Class C | 192-223 | 11000000 to 11011111 | 254 |

## Domain Name System
DNS provides an efficient way to convert human-readable names of IP end systems into machine-readable IP addresses that are necessary for routing.


