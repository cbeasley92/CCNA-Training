# Exploring the Functions of Routing

## Role of a Router
Router in internetwork communication
  * Routers are required to reach hosts that are not in the local network
  * Routers use a routing table to route between networks

## Router Charactersics
Router Components:
  * CPU
  * Motherboard
  * Memory
  * Port
    - Management: For the connection of terminal used for management
    - Network: Various LAN or WAN media ports

## Router Functions
  * Path determination
  * Packet forwarding

## Path Determination
During the path-determination portion of transmitting data over a network, routers evaluating the available paths to remote destinations
  * Routers select the best path to the destination among various sources
  * Administrative distance defines the reliability of the route source

## Routing Table
As part of the part-determination procedure, the routing builds a routing table that identifies know networks and how to reach them

### Routing Table Information
The routing table consists of an ordered list of known netowrk addresses

### Routing Update Messages
Routers communicate with each other and maintain their routing tables.

## Types of Routes
  * Directly connected networks
  * Static routes
  * Dynamic routes
  * Default routes

## Dynamic Routing Protocols
Routing protocols use their own rules and metrics to build and update routing tables automatically

Metrics can be based on either a single characteristics or on several characteristics of a path. These metrics are most commonly used by routing protocols
  * Bandwidth
  * Delay
  * Cost
  * Hop count
  * Distance vector routing protocols
  * Link state routing protocols
