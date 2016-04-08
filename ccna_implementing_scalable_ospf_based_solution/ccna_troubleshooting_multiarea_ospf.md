# Troubleshooting Multiarea OSPF

# OSPF Neighbor States
The exchange process that happens when routers appear on the network
1. A router is enabled on the LAN and is in a down state because it has not exchanged information with any other router. The router begins by sending a hello packet through each of its interfaces that are participating in OSPF, although it does not know the identity of any other routers
2. All directly connected routers that are running OSPF receive the hello packet from the first router and add the router to their lists of neighbors. After adding the router to the list, other routers are in the INIT state
3. Each router that received the hello packet sends a unicast reply hello packet to the first router with its corresponding information. The neighbor field in the hello packet includes all neighboring routers and the first router
4. When the first router receives these hello packets, it adds all of the routers that had its router ID in their hello packets to its own neighbor relationship database. After this process, the first router is in the two-way state. At this poing all routers that have each other in their lists of neighbors have established bidirectional communication


