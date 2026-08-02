---
layout: default
title: Getting Started
parent: ShowSquid
nav_order: 1
permalink: /docs/showsquid/getting-started/
---

<h1 align="center">ShowSquid Getting Started</h1>

---

## What Does ShowSquid Do?

Some devices remain quiet until asked for information, and some multicast traffic may not reach your computer unless it joins the relevant group.

ShowSquid sends discovery messages and network requests, joins selected multicast groups, and listens for replies and other traffic. This gives ShowShark more information to identify devices and show what they are doing.

## Getting Started (Essential Mode)

Essential mode provides a smaller set of commonly used protocol groups, with most configuration handled automatically.

1. Open ShowSquid.
2. Select one or more network interfaces. ShowSquid will send and receive traffic on every selected interface.
3. Enable or disable the available protocols as needed. Under **Manufacturer Specific**, choose which manufacturers to include.
4. Click **Start**. ShowSquid begins sending discovery messages and network requests, subscribes to the selected multicast groups, and listens for replies.
5. Watch the activity indicators and log, and look for new traffic in Wireshark.
6. Click **Stop** when you are done.

<p align="center">
  <img src="/assets/images/showsquid/showsquid_essential_stopped.png" alt="ShowSquid Essential mode stopped with an interface and protocol groups selected"
       style="width: 70%;">
</p>

### While Running

While ShowSquid is running, the setup controls remain locked until you click **Stop**. The TX and RX indicators flash each time ShowSquid sends or receives messages.

<p align="center">
  <img src="/assets/images/showsquid/showsquid_essential_started.png" alt="ShowSquid Essential mode running with live protocol activity indicators"
       style="width: 70%;">
</p>

### Log

Open the log from **View > Log** to see a timestamped record of ShowSquid's send and receive activity.

## Protocol Overview

### sACN Discovery

- Listens for sACN discovery packets.

### Art-Net (ArtPoll)

- Sends ArtPoll messages and listens for ArtPollReply responses.

### Manufacturer Specific

- Joins selected manufacturer-specific multicast groups and listens for traffic.

<br>

<p align="center">
  <img src="/assets/images/showsquid/showsquid_manu_specific.png" alt="Manufacturer Specific options with ETC, MA Lighting, and Pharos selected"
       style="width: 50%; border-radius: 10px; filter: drop-shadow(0 12px 16px rgba(0, 0, 0, 0.28));">
</p>

### PSN

- Joins the PSN multicast group and indicates when traffic is present.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/docs/showsquid/">← ShowSquid</a></div>
  <div style="text-align: right;"><a href="/docs/showsquid/advanced-mode/">Advanced Mode →</a></div>
</div>
{:/}
