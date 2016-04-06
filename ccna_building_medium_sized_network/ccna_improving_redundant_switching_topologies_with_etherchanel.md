# Improving Redundant Switched Topologies with EtherChannel

## Need for EtherChannel
  * When multiple links aggregate on a switch, congestion occurs
  * One solution is to increase uplink speed, but that solution cannot scale indefintely
  * Another solution is to multiply uplinks, but loop-prevention mechanisms disable some ports

## Advantages of EtherChannel
  * Logical aggregatoin of links between switches
  * High bandwidth
  * Load sharing across links
  * Viewed as one logical port to STP
  * Redundancy

## EtherChannel Protocols
  * PAgP
  * LACP

## Configuring EtherChannel
All interfaces within the EtherChannel mush have the same configuration:
  * Speed duplex
  * Mode
  * Native and allowed VLANs on trunk ports
  * Access VLANs on access ports

