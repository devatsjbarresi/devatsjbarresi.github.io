---
layout: default
title: ShowSquid
nav_order: 6
permalink: /docs/showsquid/
has_children: true
nav_fold: false
---

<h1 align="center">ShowSquid</h1>

---

ShowSquid is a desktop companion app for ShowShark.

Its purpose is simple: **prompt devices to talk so ShowShark has more to analyse**.

## Purpose

ShowSquid exists to prompt devices to talk, so you have better traffic to analyse.

It is useful when:

- You are on a quiet network and need faster visibility.
- You want to surface more protocol activity before deep analysis.
- You want ShowShark to have more data to work with for host and protocol insights.

## What ShowSquid Does

At a high level, ShowSquid does three things:

1. **Prompts network conversations**
  ShowSquid sends protocol-appropriate discovery or stimulus traffic so devices are more likely to respond.

2. **Monitors live protocol activity**
  While running, ShowSquid listens for responses and ongoing traffic across the protocol groups you enabled.

3. **Surfaces activity in a user-friendly way**
  It presents runtime state, protocol TX/RX activity, and timestamped logs so you can immediately see what is active and what is quiet.

The result is richer traffic in Wireshark and better visibility in ShowShark.

## Getting Started

1. Open ShowSquid.
2. Select one or more network interfaces.
3. Enable the protocol groups you need.
4. Enter any required options (for example universes, command presets, or profile toggles).
5. Click **Start**.
6. Watch activity indicators and log output.
7. Click **Stop** when finished.

ShowSquid validates your setup before starting and clearly reports blocked or error states when action is needed.

## Protocol Overview (High Level)

## sACN

- Helps surface sACN discovery and data activity.
- Useful for universe-level visibility.
- Setup properties: universe entry supports comma lists and numeric ranges.

## Art-Net (ArtPoll)

- Prompts Art-Net discovery responses from compatible devices.
- Useful for quickly identifying Art-Net speaking devices.

## mDNS

- Surfaces service/device advertisements using multicast DNS.
- Useful for seeing service-oriented device announcements.

## SLP

- Surfaces service announcements exposed through SLP.
- Useful for protocol/service capability discovery.

## Manufacturer Multicast Profiles

- Monitors vendor-specific multicast behaviors for supported profile groups.
- Profile groups: ETC, MA Lighting, Pharos.

## OSC

- Monitors OSC send/receive activity.
- Useful when control paths are OSC-driven.
- Setup properties: presets, custom command rows, per-row UDP Out and UDP In ports.

## PSN

- Monitors receive-side PSN activity.
- Useful for seeing PSN traffic presence quickly.

## Essential and Advanced

- ShowSquid launches in **Essential** mode for fast setup.
- Use **Advanced** mode when you need full protocol surface and detailed option panes.
- See [Advanced Mode](/docs/showsquid/advanced/) for advanced-only detail.

## How ShowSquid Helps ShowShark

ShowSquid increases the amount and variety of protocol traffic visible during capture sessions.

That means ShowShark features can give you useful results sooner.

## Screenshot Placeholder

![ShowSquid overview placeholder](/assets/images/placeholders/watchers-placeholder.svg)

## Next Step

Continue with [Advanced Mode](/docs/showsquid/advanced/).

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/docs/features/">← Features</a></div>
  <div style="text-align: right;"><a href="/docs/showsquid/advanced/">Advanced Mode →</a></div>
</div>
{:/}
