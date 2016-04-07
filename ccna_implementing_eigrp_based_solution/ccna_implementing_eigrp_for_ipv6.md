# Implementing EIGRP for IPv6

## EIGRP for IPv6
  * Neighbor discovery
  * Incremental updates
  * Fast convergence -- DUAL
  * Uses mutlicast for updates
  * Composite metric
  * Load balancing
  * Three tables
    - Neighbor table
    - Topology table
    - Routing table

## EIGRP for IPv6 Commands
```
ipv6 unicast-routing
ipv6 router eigrp 1
no shutdown
ipv6 eigrp 1

show ipv6 eigrp topology
show ipv6 eigrp neighbors
show ipv6 route eigrp
```

