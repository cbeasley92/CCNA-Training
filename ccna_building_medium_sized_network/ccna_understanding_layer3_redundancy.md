# Understanding Layer 3 Redundancy

## The Need for Default Gateway Redundancy
End devices are typically configured with a single default gateway IP address that does not change when the network topology changes. If the router whose IP address is configured as the defaul gateway fails, the local device is unable to send packets off the local network segment, effectively disconnecting it from the rest of the network. Even if a redundant router exists that could serve as a default gateway for that segment, there is no dynamic method by which these devices can determine the address of a new default gateway.

## Default Gateway Redundancy
With the type of router redundancy that is show in the figure, a set of routers work together to presetnt the illusion of a single router to the host on the LAN. By sharing an IP (Layer 3) address and a MAC (Layer 2) address, two or more routers can act as a single "virtual" router

These are the stops that take place when a router fails:
1. The standby router stops seeing hello messages from the forwarding router
2. The standby router assumes the role of the forwarding router
3. Because the new forwarding router assumes both the IP and MAC addresses of the virtual router, the end stations see no disruption in the service

## HSRP
  * HSRP defines a group of routers -- one active and one standby
  * Virtual IP and MAC address are shared between the two routers
  * To verify HSRP state, use the **show standby** command
  * HSRP is Cisco propriety, and VRRP is a standard protocol

## HSRP Interface Tracking
Interface tracking enables the priority of a standby group router to be automatically adjusted based on the availability of the router interfaces. When a tracked interface becomes unavailable, the HSRP tracking feature ensures what a router with an unavailable key interface will relinquish the active router role.

## HSRP Load Balancing
Rotuers can simultaneously provide redundant backup and preform load sharing across various subnets

## Gateway Load Balancing Protocol
  * Allows full use of resources on all devices without the administrative burden of creating multiple groups
  * Provides a single virtuak IP address and multiple virtual MAC addresses
  * Routes traffic toa  single gateway distributed across routers
  * Provides automatic rerouting in the event of a failure
