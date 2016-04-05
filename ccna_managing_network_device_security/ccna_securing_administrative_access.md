# Securing Administrative Access

## Network Device Security Overview
Common threats to network device security and mitigation strategies can be summarized as follows:
  * Remote access threats
  * Local access and physical threats
  * Environmental threats
  * Electrical threats
  * Maintenance threats

## Securing Access to Privileged EXEC Mode
Configuring enable password
  `enable password C1sco123`
Configuring enable secret password
  `enable secret sanfran`
Verification of configured passwords
  `show running-config | include enable`

## Securing Remote Access
Configuring ssh:
```
hostname SwitchX
ip domain-name cisco.com
username user1 secret C1sco123
crypto key generate rsa modulus 1024
line vty 0 15
login local
transport input ssh
exit
ip ssh version 2
```

## Enable Remote Access Connectivity
Configure the IP address of a default gateway on a switch
```
ip default-gateway 10.1.1.1
```

To configure the switch so that it can be accessed remotely, a default gateway is needed. To configure a default gateway for the switch, use the `ip default-gateway` command.

## Limiting Remote Access with ACLs
  * Configure an  ACL
  * Apply the ACL to the lines
    - `access-class`

## External Authentication Options
External authentication may be perferable to local authentication
  * A local authentication database can be an administrative burden
  * External authentication provides scalability
  * You can use RADIUS or TACACS+


