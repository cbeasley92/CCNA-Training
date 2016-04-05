# Implementing Traffic Filters with ACLs

## ACL Operation
When ACLs are sused for traffic filtering, they can operate inbound or outbound. The direction ditermines at which point packets are tested against teh ACL as they pass through the router.
  * **Outbound ACLs:** Incoming packets are routed to the outbound interface and then are processed through the outbound ACL. 
  * **Inbound ACLs:** Incoming packets are processed by the ACL before they are routed to an outbout interface

## Configuring Numbered, Extended IPv4 ACLs
```
access-list 110 deny ip host 10.1.1.101 host 209.165.202.197
access-list 110 permit tcp 10.1.1.0 0.0.0.255 any eq 80
```

## Configuring Named ACLs
The ACL configuration mode is used to configure a named ACL
```
ip access-list extended WEB_ONLY
permit tcp 10.1.1.0 0.0.0.255 any eq www
20permit tcp 10.1.1.0 0.0.0.255 any eq 443
```

```
ip access-group WEB_ONLY in
```

## ACL Configuration Guidelines
These guidelines are recommended:
  * The type of ACL, standard or extended, determines what is filtered
  * Only one ACL per interface, per protocol, and per direction is allowed
  * The most specific statement should be at the top of an ACL. The most general statement should be at the bottom of an ACL.
  * The last ACL test is always and implicit "deny everything else" statement, so every list needs at least one permit statement
  * When placing and ACL in a network, follow these guidelines:
    - Place extended ACLs close to the source
    - Place standard ACLs close to the destination
  * An ACL can filter traffic going through the router or traffic to and from the router, depending on how it is applied


