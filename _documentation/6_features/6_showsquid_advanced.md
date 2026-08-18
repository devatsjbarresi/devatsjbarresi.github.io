---
layout: default
title: Advanced Mode
parent: ShowSquid
nav_order: 2
permalink: /docs/showsquid/advanced-mode/
---

<h1 align="center">ShowSquid Advanced Mode</h1>

---

## What Advanced Mode Is For

Advanced mode shows every supported protocol and its available settings, giving you more control over what ShowSquid sends and listens for.

## Getting Started

1. Open ShowSquid.
2. Go to _View > Level_ and select **Advanced**.
3. Select one or more network interfaces.
4. Enable the protocol groups you need.
5. Expand any protocol that needs additional configuration and enter the required options.
6. Click **Start**.
7. Watch the activity indicators and log, and look for new traffic in Wireshark.
8. Click **Stop** when finished.

<p align="center">
  <img src="/assets/images/showsquid/showsquid_advanced_stopped.png" alt="ShowSquid Advanced mode stopped with the full protocol list available"
       style="width: 90%;">
</p>

### While Running

When ShowSquid is running, the protocol controls are locked. The TX and RX indicators show transmitted and received traffic, while the status text shows when the next message is due to be sent.

<p align="center">
  <img src="/assets/images/showsquid/showsquid_advanced_started.png" alt="ShowSquid Advanced mode running with live protocol activity indicators"
       style="width: 90%;">
</p>

## Additional Protocols and Options

### sACN Options

Expand **sACN Discovery** to enter individual universes, comma-separated lists, or numeric ranges. ShowSquid joins the corresponding multicast groups so their packets can be captured in Wireshark.

<br>

<p align="center">
  <img src="/assets/images/showsquid/showsquid_sacn.png" alt="sACN Discovery options with individual universes and ranges entered"
       style="width: 65%; border-radius: 10px; filter: drop-shadow(0 12px 16px rgba(0, 0, 0, 0.28));">
</p>

### ArtPoll Options

Expand **ArtPoll** to choose how ShowSquid broadcasts ArtPoll messages. **Limited and Art-Net Default** sends to `255.255.255.255` and `2.255.255.255`. **Directed Broadcast** sends to the broadcast address calculated for each selected interface.

<br>

<p align="center">
  <img src="/assets/images/showsquid/showsquid_artpoll_advanced.png" alt="ArtPoll options for limited, Art-Net default, and directed broadcast addresses"
       style="width: 65%; border-radius: 10px; filter: drop-shadow(0 12px 16px rgba(0, 0, 0, 0.28));">
</p>

### mDNS

- Sends mDNS queries and listens for announcements and replies.

### SLP

- Sends SLP service requests and listens for replies.

### OSC Broadcast

Expand **OSC Broadcast** to enable predefined commands for supported manufacturers or add your own OSC commands.

Messages are sent to the broadcast address of each selected interface's subnet. **UDP Out** sets the destination port for each command, while **UDP In** sets the port ShowSquid listens on for incoming messages. Enabled commands are sent every 10 seconds.

<br>

<p align="center">
  <img src="/assets/images/showsquid/showsquid_osc.png" alt="OSC options with an Eos predefined command, a custom command, and UDP ports"
       style="width: 60%; border-radius: 10px; filter: drop-shadow(0 12px 16px rgba(0, 0, 0, 0.28));">
</p>

### Custom Multicast

Expand **Custom Multicast** to add multicast subscriptions that are not covered by the built in protocol options. ShowSquid joins each subscription on every selected interface but does not send any traffic.

<br>

<p align="center">
  <img src="/assets/images/showsquid/showsquid_custom_multicast.png" alt="Custom Multicast options with three multicast addresses and UDP ports"
       style="width: 60%; border-radius: 10px; filter: drop-shadow(0 12px 16px rgba(0, 0, 0, 0.28));">
</p>

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/docs/showsquid/getting-started/">← Getting Started</a></div>
  <div style="text-align: right;"><a href="/docs/resources/">Resources →</a></div>
</div>
{:/}
