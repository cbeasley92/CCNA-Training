# Implementing EIGRP

## Purpose of Dynamic Routing Protocols
Dynamic routing protocol characteristics follow:
  * Routing protocols are set of processes, algorithms, and messages that are used to exchange routing information
  * After directly connecting routes have been installed, a router populates its routing table with the best paths to remote destinations, as chosen by the routing protocol
  * After the path is determined, a router can route to the learned network

## Interior and Exterior Routing Protocols
Characteristics of autonomous systems
  * An AS in a collection of netowrks within a common administrative domain
  * IGPs operate within an AS
  * EGPs connect different autonomous systems

IGPs are used for routing within a routing domain. Those networks are under the controls of a sing organization. An AS commonly comprises many individual networks belonging to companies, schools, and other institutions.

## Distance Vector and Link-State Routing Protocols
The types of dynamic routing protocols follow:
  * Distance vector: RIP
  * Advanced distance vector: EIGRP
  * Link-state: OSPF and IS-IS

**Distance Vector:** The distance vector routing approach determines the direction (vector) and distance (a metricm such as hop count in the case of RIP) to any link in the internetwork.
**Advanced distance vector:** The advanced distance vector approach combines aspects of the link-state and distance vector algorithms
**Link-state:** The link-state approach, which uses the SPF algorithm, creates an abstraction of the exact topology of the entire internetowrk, or at least of the partition in which the router is situated

## Administrative Distance
  * Multiple routing protocols and static routes can be used at the same time
  * Routers choose the routing source with the lowest adminsistrative distance

## EIGRP Features
  * Rapid convergence
  * Load Balancing
  * Loop-free, classless routing
  * Reduced bandwidth usage
    - Boundless updates
    - No broadcast

## EIGRP Path Selection
To determine the best route (successor) and any backup routes (feasible successors) to a destination, EIGRP uses the following two parameters:
  * AD: The EIGRP metric for an EIGRP neighbor to reach the particular network, also sometimes referred to as the _reported distance_
  * FD: The AD for a particular network that is learned from an EIGRP neighbor plus the EIGRP metric to reach this neighbor. This sum provides an end-to-end metric from the router to the remote network.

## EIGRP Metric
  * EIGRP uses two criteria, by default, to calculate its metric
    - Bandwidth
    - Load
  * Optionally, EIGRP can use these criteria when calculating its metric (not recommended)
    - Reliability
    - Load

## Load Balancing with EIGRP
EIGRP knows two types of load balancing
  * Equal-cost load balancing
    - By default, up to four routes with a metric equal to the minimum metric are installed in the routing table
    - The routing table can have up to 16 entries for the same destination
  * Unequal-cost load balancing
    - By default, it is _not_ turned on
    - Load balancing can be performed through paths that have up to 128 times worse metrics than the successor route
