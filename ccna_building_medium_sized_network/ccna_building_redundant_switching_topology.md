# Building Redundant Switching Topologies

## Issues in Redundant Topologies
  * Eliminates single points of failure
  * Causes broadcast storms, redundant frame copies, and MAC address table instability
  * A loop-avoidance mechanism is required

The **Spanning Tree Protocol (STP)** is a network protocol that builds a logical loop-free topology for Ethernet networks. The basic function of STP is to prevent bridge loops and the broadcast radiation that results from them.

## Types of Spanning-Tree Protocols
  * IEEE 802.1D
  * PVST+
  * 802.1w (RSTP)
  * Rapid PVST+

## Per VLAN Spanning Tree Plus
Root spanning trees for each VLAN 
