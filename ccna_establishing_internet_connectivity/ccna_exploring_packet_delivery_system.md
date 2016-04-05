# Exploring the Packet Delivery Process

## Layer 2 Addressing
Layer 2 characteristics:
  * Ethernet uses MAC address
  * Identifies end devices in the LAN
  * Enables the packet to be carried by the local media across each segment

## Layer 3 Addressing
Layer 3 device functions:
  * The network layer provides connectivity and path selection between two host systems
  * In the host, this path between the data link layer and the upper layers
  * In the router, it is the acutal path across the network

## Address Resolution Protocol
ARP provides two basic functions
  * Resolving IP address to MAC addresses
  * Maintaining a cache of mappings

To send data to a destination, a host on an Ethernet network must know the physical (MAC) address of the destination. ARP provides the essential service of mapping IP addresses to physical addresses on a network

The term _address resolution_ refers to the process of binding the network layer IP address of a remote device to its locally reachable, data link layer MAC address. 
