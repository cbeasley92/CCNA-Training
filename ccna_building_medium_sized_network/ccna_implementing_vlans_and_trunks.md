# Implementing VLANs and Trunks

## Issues in Poorly Designed Networks
  * Large broadcast domains
  * Management and support challenges
  * Possible security vunerabilities

## VLAN Introduction
VLANs improve network performance by separating large broadcast domains into smaller segments. A VLAN allows a network administrator to create logical groups of netowrk devices. These devices act as if they were in their own independent network, even if they share a common infrastructure with other VLANs.

## Trunking with 802.1Q
  * Combining many VLANs on the same port is called trunking
  * A trunk allows the transportation of frames from different VLANs
  * Each frame has a tag that specifies the VLAN that it belongs to
  * Frames are forwarded to the corresponding VLAN based on the tag information

VLAN Trunking Protocol (VTP) is a Cisco proprietary protocol that propagates the definition of Virtual Local Area Networks (VLAN) on the whole local area network. To do this, VTP carries VLAN information to all the switches in a VTP domain. VTP advertisements can be sent over ISL, 802.1Q, IEEE 802.10 and LANE trunks.

More information availabe at [http://www.cisco.com/c/en/us/support/docs/lan-switching/vtp/10558-21.html]

## Creating a VLAN
Creating VLAN named "Sales"
```
conf t
vlan 2
name Sales
```

Verfiying VLAN2
```
show vlan id 2
```

## Assigning a Port to a VLAN
How to assign a port to a VLAN
```
conf t
interface FastEthernet 0/3
switchport mode access
switchport access vlan 2
```

