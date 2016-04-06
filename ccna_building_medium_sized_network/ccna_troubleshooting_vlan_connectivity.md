# Troubleshooting VLAN Connectivity

## Dynamic Trunking Protocol
Switchport mode interactions:
  * Manual configuration is recommended
  * Configure the port as trunk or access on both switches
  * The command **nonegotiate** disables negotiation

You should configure trunk links statically whenever possible.

## VLAN Troubleshooting
Steps:
1. Use the `show vlan` command to check whether the port belongs to the expected VLAN. If the port is assigned to the wrong VLAN, use the `switchport access vlan` command to correct the VLAN membership
2. If the VLAN to which the port is assigned is deleted, the port becomes inactive. Use the `show vlan` or `show interfaces switchport` commad to verify that tghe VLAN is present in the database

## Trunk Troubleshooting
Steps:
1. Use the `show interfaces trunk` command to check whether a trunk has been esetablished between switches. You should statically configure trunk links whenever possible. However, Cisco Catalyst switch ports, by default, run DTP, which tries to negotiate a trunk link.
2. Use the `show interfaces trunk` command to check whether the local peer 
