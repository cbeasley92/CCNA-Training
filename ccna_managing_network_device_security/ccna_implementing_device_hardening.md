# Implementing Device Hardening

## Securing Unused Ports
This topic describes the need to secure unused ports
  * Unsecured ports can create a security vulnerability
  * A device that is plugged into an unused port is added to the network
  * Unused ports can be secured by disabling interfaces (ports)

Unused ports on a switch cab be a security risk. A hacker can plug a switch into an unused port and become part of the network. Therefore, unsecured ports can create a security hole.

## Port Security
Port security restricts port access by the MAC address
  * Dynamic (limited number of addresses)
  * Static (static configuration of addresses)
  * Combination (static plus dynamic)
  * Sticky learning

## Network Time Protocol
NTP provides time synchronization between network devices
  * NTP can get the correct time from internal or external time source
  * A router can act as an NTP server and client. Other devices (NTP clients) synchronize time with the rouer (NTP server)
