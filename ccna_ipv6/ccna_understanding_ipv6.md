# Understanding IPv6

## IPv6 Header Changes and Benefits
The IPv6 header contains eight fields
  * Version
  * Traffic Class
  * Flow Label
  * Payload Length
  * Next Header
  * Hop Limit
  * Source Address
  * Destination Address

## ICMPv6
ICMPv6 Messages
  * Provides diagnostics
  * Router discovery
  * Neighbor discovery

## Neighbor Discovery
Neighbor discovery performs the same functions in IPv6 as ARP does in IPv4

Neighbor discovery:
  * Determines the link layer address of a neighbor
  * Finds neighbor routers on the link
  * Queries for duplicate addresses
  * Is achieved by using ICMPv6 with IPv6 multicast

## Stateless Autoconfiguration
Stateless autoconfiguration uses neighbor discovery mechanisms to find routers and dynamically create IPv6 addresses.
