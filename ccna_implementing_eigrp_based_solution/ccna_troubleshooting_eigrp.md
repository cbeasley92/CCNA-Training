# Troubleshooting EIGRP

## Components of Troubleshooting EIGRP
After configuring EIGRP, you would first test connectivity to the remote network. If the ping fails, you should check if the router has EIGRP neighbors. Neighbor adjacency might not be up for a number of reasons, such as the following
  * The interface between the devices is down
  * The two routers have mismatching EIGRP autonmous systems
  * Proper interfaces are not enabled for the EIGRP process
  * An interface is configured as passive

If the EIGRP neighbor relationship is up between the two routers, there may be a routing problem. Here are some issues that may cause a connectivity problem for EIGRP
  * Proper networks are not being advertised on remote routers
  * An access list is blocking advertisements of remote networks
  * Automatic summary is causing confusion in your discontiguous network

## Troubleshooting EIGRP Neighbor Issues
```
show ip eigrp neighbors
show ip eigrp route

show ip interface brief

show ip protocols

show ip eigrp interfaces Serial 0/0/0
```

## Troubleshoot EIGRP Routing Table Issues
```
show ip protocols

show ip protocols | begin Routing for Networks

router eigrp 1
network 172.16.1.0

show ip protocols

show ip route

router eigrp 1
no auto-summary
```
