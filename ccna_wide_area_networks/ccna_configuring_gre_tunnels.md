# Configuring GRE Tunnels

## GRE Tunnel Overview
GRE = Generic Routing Encapsulation
  * One of many tunneling protocols
  * IP protocol 47 defines GRE packets
  * Allows routing information to be passed between connected networks
  * No encryption

## GRE Tunnel Verification
To determine whether the tunnel interface is up or down, use the `show ip interface brief` command. You can verify the state of a GRE tunnel by using the `show interface tunnel` command. The line protocol on a GRE tunnel interface is up as long as there is a route to the tunnel destination
