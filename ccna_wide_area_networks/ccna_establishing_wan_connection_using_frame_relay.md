# Establishing a WAN Connection Using Frame Relay

## Understanding Frame Relay
  * Used for WAN networks
  * Connection-oriented, packed-swiching service
  * Connections made by virtual circuits

## Frame Relay Topologies
  1. Partial-Mesh
  2. Full-Mesh
  3. Star (Hub-and-Spoke)

## Frame Relay Reachability Issues
Frame Relay NBMA connectivity causes problems with routing protocols
  * Split horizon (EIGRP)
  * Neighbor discovery and DR and BDR election (OSPF)
  * Broadcast replication

**Split Horizon:** With the routing protocols EIGRP and RIP, the split-horizon rule reduces routing loops by preventing a routing update that is received on an interface from being forwarded out the same interface
**Neighbor discovery and DR and BDR election:** OSPF over NBMA networks work in nonbroacast network mode by default, and neighbors are not automatically discovered.
**Broadcast Replication:** With routers taht support multipoint connections over a single interface that terminates in many PVCs, the router must replicate broadcast packets, such as routing update broadcasts, on each PVC to the remote routers

## Frame Relay Address Mapping
  * Automatic discovery of DLCI is from the Frame Relay switch using LMI
  * Local DLCI must be mapped to a destination network layer address:
    - Automatic mapping with Inverse ARP
    - Manual configuration using a static Frame Relay map
