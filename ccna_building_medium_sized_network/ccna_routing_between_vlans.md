# Routing Between VLANs

## Purpose of Inter-VLAN Routing
  * A VLAN creates a separate switching segment
  * Traffic cannot be switched between VLANs
  * VLANs have different IP subnets
  * Routing is necessary to forward traffic between VLANs

## Options for Inter-VLAN Routing
  * Router with a separate interface in each VLAN
  * Router with a trunk link
  * Layer 3 switch

## Configuring a Router with a Trunk Link
```
interface GigabitEthernet 0/0.10
encapsulation dot1Q 10
ip address 10.1.10.1 255.255.255.0
interface GigabitEthernet 0/0.20
encapsulation dot1Q 20
ip address 10.120.1 255.255.255.0
```
The **encapsulation dot1q 20** command enables 802.1Q encapsulation trunking on the GigabitEthernet0/0.20 subinterface. The value 20 represents the VLAN number, therefor assocuating 802.1Q-tagging traffic from this VLAN with the subinterface.


