---
layout: default
title: IGMP
parent: General
---

# IGMP (Internet Group Management Protocol)

**IGMP** is the network protocol used by IPv4 systems to manage multicast group memberships.  
In entertainment networks, IGMP is vital for controlling how lighting and media devices subscribe to multicast groups used by **sACN** or other streaming data protocols.

## Overview
IGMP operates at the network layer and allows devices to:
- Join and leave multicast groups
- Report their membership to network switches and routers
- Optimise traffic by ensuring multicast data only reaches interested devices

ShowShark decodes IGMP packets and correlates them with sACN universes and multicast groups, making it easier to understand how data is distributed across the network.

## Key Features in ShowShark
- Identification of **IGMPv2** and **IGMPv3** messages
- Detection of **Membership Queries**, **Reports**, and **Leave Group** messages
- Tracking of queriers and last-query intervals
- Highlighting of entertainment multicast addresses (239.255.x.x)

## Example Uses
- Diagnosing missing lighting data caused by absent group memberships
- Confirming correct querier election and timing
- Detecting devices flooding the network with unnecessary multicast joins

---

_This section will soon include detailed IGMP packet breakdowns, querier timing visualisation, and examples of sACN universe joins._

