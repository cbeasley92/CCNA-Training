# Introducing Basic IPv6

## IPv4 Addressing Exhaustion Workarounds
To extend the lifetime and usefulness of IPv4 and circumvent address shortage, several mechanisms were created:
  * CIDR
  * VLSM
  * NAT
  * DHCP

## IPv6 Features
  * **Larger address space:** Global reach capability, flexibility, aggregation, multihoming, autoconfiguration, "plug-and-play", renumbering
  * **Simple header:** Routing code streamlined, simpler processing in hardware
  * **Security and mobility:** Built into the standard, not as extensions
  * **Transition richness:** Several mechanism available, including "dual-stacking"

## IPv6 Addresses
Address representation is as follows:
  * Format is x:x:x:x:x:x:x:x, where x is a 16-bit hexadecimal field
    - Example: 2001:0DB8:010F:0001:0000:0000:0000:0ACD
  * Leading zeros in a field are optional
    - Example: 2001:DB8:10F:1:0:0:0:ACD
  * Successive fields of 0 are represented as "::" but only one in an address
    - Example: 2001:DB8:10F:1::ACD

IPv6 supports three types of addresses
  * **Unicast:* Unicast addresses are used in one-to-one context
  * **Multicast:** A multicast address identifies a group of interfaces. Traffic that is sent to a mutlicast address is sent to multiple destinations at the same time. An interface may belong to any number of multicast groups
  * **Anycast:** An IPv6 anycast address is assigned to an interface on more that one node. When a packet is sent to an anycast address, it is routed to the nearest interface that has this address. The nearest interface is found according to the measure of distance of the particular routing protocol. All nodes that share the same address should behave the same way so taht the service offered similarly regardless of the node that services the request

## IPv6 Unicast Addresses
Types fo IPv6 unicast addresses
  * **Global:** Starts with 2000::/3 and assigned by the Internet Assigned Numbers Authority
  * **Link Local:** This starts with FE80::/10

## IPv6 Addresses Allocation
  * Manual assignment with or without EUI-64
  * Stateless autoconfiguration
  * Stateful autoconfiguration

## Basic IPv6 Connectivity
Enabling IPv6 routing on Cisco routers:
```
ipv6 unicast-routing
```
Configures the interface with specific IPv6 address
```
ipv6 address 2001:db8:d145:C900::1/64
``` 
