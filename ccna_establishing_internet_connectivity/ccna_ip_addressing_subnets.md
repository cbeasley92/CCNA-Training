# Understanding IP Addressing and Subnets

**Example:**
192.168.1.0/25

192.168.1.0 is the network address
192.168.1.127 is the broadcast address

192.168.1.128 is the network address
192.168.1.255 is the broadcast address

**Example:**
192.168.1.37
255.255.255.224

Block Size = 265 - 224 = 32
  32 * 2 = 64 - 2 = 62
  0 - 62

**Example:**
If an ethernet port on the rounter was assigned 172.16.112.1/20, what is the maximum number of hosts allowed on this subnet?
32 - 20 = 12
2^12 = 4096 - 2 = 4094

**Example**
The internetwork is using subnets of the address 192.168.1.0 with a subnet mask of 255.255.255.224. Routing protocol RIPv2. Which address coule be assigned?
A: 192.168.1.31
B: 192.168.1.64
C: 192.168.1.127
*D*: 192.168.1.190

| Binary Table |
| --- | --- | 
| 1000 0000 | 128 |
| 1100 0000 | 192 |
| 1110 0000 | 224 |
| 1111 0000 | 240 |
| 1111 1000 | 248 |
| 1111 1100 | 252 |
| 1111 1110 | 254 |
| 1111 1111 | 255 |

## Subnets
Network administrators often need to divide netowrks, especially large networks, into, subnetworks, or subnets, to provide scalability.

## Subnet Masks
A subnet mask
  * Defines the number of bits that represetn the network and subnet part of the address
  * Used by end systems to identify the destination IP address as either local or remote
  * Used by Layer 3 devices to determine network path

## Applying Subnet Masks
Procedure for implementing subnets:
  1. Determinethe IP address space
  2. Based on the organizational and administrative structure, determine the number of subnets that are required
  3. Based on the address class and require number of subnets, determine the number of bits that you needd to borrow from the host ID
  4. Determine the binary and decimal value of the subnet mask
  5. Apply the subnet mask to the network IP address to determine teh subnet and host addresses
  6. Assign subnet addresses to specific interfaces for all devices that are connected to the newtwork

## Variable-Length Subnet Mask
VLSM affords the options of including more than one subnet mask within a network and subnetting an already subnetted network address.
VSLM offers these benefits:
  * More efficient use of IP addresses
  * Better-definied network hierarchical levels

