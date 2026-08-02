---
layout: default
title: Art-Net
parent: Protocols
nav_order: 2
permalink: /docs/art-net/
has_toc: false
---

<h1 align="center">Art-Net</h1>

---

ShowShark recognises **Art-Net** traffic and surfaces useful lighting network fields in Wireshark.

This dissector interprets Art-Net packets including:
- ArtPoll and ArtPollReply for node discovery
- ArtDMX for DMX512-A data transport
- Universe and subnet mappings
- Node names and version information

Use this view to confirm correct packet routing, identify nodes, and verify lighting network behaviour.
