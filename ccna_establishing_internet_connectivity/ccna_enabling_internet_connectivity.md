# Enabling Internet Conntectivity

## Dynamic Host Configuration Protocol
Understanding DHCP:
  * DHCP is a client-server modet
  * A DHCP server allocates network addresses and delivers configurations
  * A DHCP client is a host that requests an IP address and configuration from a DHCP server

DHCP IP address allocation mechanism:
  * **Automatic allocation:** A permanent IP address is assigned to a client
  * **Dynamic allocation:** A client is assigned an IP address for a limited time
  * **Manual allocation:** A client is a assigned an IP address by the network administrator

## Introducing NAT
NAT allows private users to access the Internet by sharing one or more public IP addresses

## Types of Addresses in NAT
  * **Inside local:** Host on the inside network
  * **Inside global:** Usually assigned by an ISP and allows the customer outside access
  * **Outside global:** Host on the outside network

## Types of NAT
  * **Static NAT:** One-to-one address mapping
  * **Dynamic NAT:** Many-to-many address mapping
  * **PAT:** Many-to-one address mapping
