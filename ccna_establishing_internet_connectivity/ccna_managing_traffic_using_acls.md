# Managing Traffic Using ACLs
Access Control Lists

## Using ACLs
What is an ACL?
  * An ACL is a Cisco IOS tool for traffic identification
  * An ACL is a list of permit and deny statements
  * An ACL identifies traffic based on the information within the IP packet
  * After traffic is identified, different actions can be taken
  * ACLs can be used on routers and switches

An ACL is a Cisco IOS feature that is used for traffic identification. The ACL enables an administrator to create a set of rules in the form of permit and deny statesments that describe which traffic should be identified. Traffic identification is based on the header value in the IP packet. Identified traffic can recieve different treatment, depending on which Cisco IOS function is using the ACLs.

### Example ACL
```
deny host 10.10.10.2
permit any
```
This ACL blocklist host `10.10.10.2` but allows all other connections.

### Example Blocking Subnet with ACL:
Subnets:
  * 1 - 30
  * 33 - 62
  * 64 - 96
  * 128 - 160

To block the third subnet.
```
deny host 192.168.1.63
permit any
```

## ACL Operation
ACL Tests:
  * An ACL consists of a series of permit and deny statements
  * An ACL is consulted in top-down order
  * The first match executes the permit or deny action and stops further ACL matching
  * There is a implicit deny all statements at teh end of each ACL

## ACL Wildcard Masking
When processing ACLs, a router needs a mechanism to determine which bits of an IP address must match. A wildcard mask describes which bits of an IP address mustwatch in an IP packet to result in a match for a permit or deny statement. This topic describes how to use wildcard masks with ACLs.

Wildcard bits - how to check the corresponding addres bits:
  * 0 means to match the value of the corresponding address bit
  * 1 means to ignore the value of the corresponding address bit

## Types of ACLs
Two main types fo ACLs:
  * Standard ACL:
    - Checks source IP address
    - Permits or denies entire protocol suite
  * Extended ACL:
    - Checks source and destination IP address
    - Generally permits or denies specific protocols and applications

**Standard ACLs:** Standard IP ACLs check the source addresses of the packets that can be routed. The result either permits or denies the output for an entire protcol suite, which is based on the source network, subnet, or host IP address.
**Extended ACLs:** Extended IP ACLs check both the source and destination packet addresses. They can also check for specific protocols, port numbers, and other parameters, which allows administrators more flexibility and control.
