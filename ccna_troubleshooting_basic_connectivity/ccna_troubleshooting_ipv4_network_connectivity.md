# Troubleshooting IPv4 Network Connectivity

## Components of Troubleshooting End-to-End Connectivity
When there is no end-to-end connectivity, these are some items that you should investigate:
  * Check the cables, because there might be a faulty cable or interface
  * Make sure the devices are determining the correct path from the source to destination. Manipulating the routing information, if needed.
  * Verify that the default gateway is correct
  * Verify that name resolution settings are correct
  * Verify that ther are no ACLs that are blocking traffic

## Verification of End-to-End Connectivity
The `ping` command is a utility for testing IP connectivity between hosts
The `traceroute` command is a utility that allows observation of the path between two hosts
The `telnet` command can be used to test transport layer connectivity for any port
The cache can be cleared by using the `arp -d` command, if youw ant to repopulate the cache with updated information
Use the `show mac address-table` commadn to display the MAC address table on the switch

## Verification of Physical Connectivity Issues
The most common Cisco IOS commands for checking physical connectivity are the `show processes cpu`, `show memory`, and `show interface` commands.
The output of `show interface` command lists these important statistics that should be checked:
  * Input queue drops
  * Output queue drops
  * Input errors
  * Output errors

## Identification of Current and Desired Path
On the router, use the `show ip route` command to examine the routing table.
  * Directly connected
  * Local host routes
  * Static routing
  * Dynamic routing
  * Default route

The routing tables can be populated by these methods
  * Directly connected networks
  * Local host routes
  * Static routes
  * Dynamic routes
  * Default routes

The `show ip route` command displays the routing table in a router
  * **L:** Reserved for the local host route
  * **C:** Reserved for the directly connected networks
  * **S:** Reserved for static routes
  * **R:** Reserved for RIP
  * **O:** Reserved for OSPF routing protocol
  * **D:** Reserved for EIGRP. Letter D stands for DUAL, the update algorithm that is used by EIGRP

## ACL Issues
Use the `show ip access-lists` command to display the contents of all ACLs.
The `show ip interfaces` command displays IP interface information and indicates whether any IP ACLS are set on the interface
