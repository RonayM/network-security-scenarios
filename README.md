Scenario 01 – Small Office Network Security
Context

Small office network

Around 8 user workstations (4 implemented in lab)

One ISP-provided router acting as default gateway

One unmanaged Layer 2 switch

DHCP provided by a dedicated server

No dedicated firewall device

Network Topology

Default Gateway (Router): 192.168.10.1

DHCP Server: 192.168.10.2

Network: 192.168.10.0/24

DHCP address pool starts from: 192.168.10.100

Client IP addresses are assigned dynamically

Observation

All client machines receive IP addresses automatically via DHCP

DHCP assigns addresses starting from 192.168.10.100

The first DHCP response is trusted by clients

All devices are located in a single flat network segment

No traffic filtering, access control, or firewall rules are applied

No monitoring or logging mechanisms are configured

Risk

A rogue DHCP server could assign a fake default gateway

Network traffic could be redirected without user awareness

Possible man-in-the-middle (MITM) attack

Credentials and sensitive data could be exposed

Flat network architecture increases the impact of a single compromised host

Decision

Use a single trusted DHCP server for IP address management

Separate infrastructure devices (router, server) from the DHCP pool

Keep the network flat to reflect a common real-world small office setup

Intentionally leave the network without firewall rules as a baseline state

Result

Client devices successfully obtain valid IP addresses in the range 192.168.10.100 – 192.168.10.149

Network connectivity is stable and functional

The lab accurately represents a typical small office environment

Security weaknesses are clearly identified for further improvement

Lab Implementation

Implemented using Cisco Packet Tracer

Devices used:

1× Router (2911)

1× Switch (2960)

1× Server (DHCP)

4× Client PCs

All clients receive IP addresses dynamically from the DHCP server
