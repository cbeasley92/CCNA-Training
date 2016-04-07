# Configuring Serial Encapsulation

## Point-to-Point Connectivity
Ethernet emulation:
  * Simple
  * Affordable
  * Flexible

## Serial Communication Links
A point-to-point (or serial) communication link establishes a WAN communications path from the customer premises through a carrier netowrk to a remote network.

## HDLC Protocol
The HDLC protocl is one of two major data-link protocols that are commonly used with point-to-point WAN connections

## Point-to-Point Protocol
PPP provides a standard method for transporting datagrams over point-to-point links

## Troubleshooting Serial Connections
To troubleshoot link issues that are due to misconfigured encapsulation and authentication on the serial interface, follow these high-level steps:
1. Check that the correct cable is connected to the device (DTE and DCE)
2. Verify that both sides of the serial connection are configured with the same encapuslation -- PPP or HDLC
3. If PPP encapsulation is correctly configured on both sides of the link, verify that the CHAP authentication is succesful
