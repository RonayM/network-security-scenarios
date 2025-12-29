# Scenario 01 – Small Office Network Security

## Context
- Small office network
- Around 8 user workstations
- One ISP-provided router
- One unmanaged switch
- DHCP enabled on the router
- No dedicated firewall device

## Observation
- All clients receive IP addresses automatically
- The first DHCP response is trusted
- No network segmentation is present
- No monitoring or logging is configured

## Risk
- A rogue DHCP server could assign a fake default gateway
- Network traffic could be redirected without user awareness
- Possible man-in-the-middle attack
- Credentials and sensitive data could be exposed

## Decision
- Limit DHCP service to a single trusted device
- Use static gateway configuration where applicable
- Introduce basic firewall rules
- Separate user and infrastructure traffic

## Result
- Rogue DHCP servers become ineffective
- Traffic follows expected network paths
- Reduced risk of MITM attacks
- Improved control over the network
