---
layout: default
title: Watchers
parent: Features
nav_order: 2
permalink: /docs/watchers/
---

<h1 align="center">Watchers</h1>

---

Watchers let you capture specific DMX or OSC values and show them in custom columns in Wireshark's packet list. Each column shows the value carried by matching packets, making it easier to track changes to a specific DMX channel, OSC value or part of an OSC address across packets.

## Quick Start

1. Open an existing capture file or start a new capture and leave it running.
2. Go to _Tools > 1 ShowShark Tools > 2 Watchers_.
3. Click **Add DMX Watcher** or **Add OSC Watcher**.
4. Click **Apply** to save the watcher configuration.
5. Follow [Setting Up Columns](#setting-up-columns) to add the watcher field, such as `show.watcher.1`, to Wireshark's packet list.
6. View the watcher values in the packet list.

## Watchers Window

The Watchers window shows each watcher slot and its custom column field, such as `show.watcher.1`. Unused slots are left blank.

<p align="center">
  <img src="/assets/images/watchers/watcher_window.png" alt="ShowShark Watchers window with configured watcher examples"
       style="width: 88%;">
</p>

## Applying Changes

- **Apply:** Saves the watcher settings.
- Adding, removing or changing the type of a watcher may require a plugin reload. ShowShark prompts you when needed.
- **Revert:** Restores the last applied watcher settings.

## Adding a DMX Watcher

Click **Add DMX Watcher** and fill in the DMX value you want to track.

| Field | Description |
| ----- | ----------- |
| **Protocol** | Choose `Any`, `sACN`, or `Art-Net`. `Any` matches the same universe and channel across both supported DMX protocols. |
| **Universe Number** | The universe to watch. |
| **Start Address** | The DMX channel to watch, from 1 to 512. |
| **Bits** | Use `8` or `16`. 16-bit combines two consecutive DMX channels into one value. If left blank, ShowShark uses 8-bit. |

{: .note }
> The format used for displayed DMX values, such as Percent, Decimal, or Hex, follows the **DMX Display** setting under _Tools > 4 ShowShark Options > 4 DMX Display_.

<p align="center" style="margin: 2rem 0 0.5rem;"><em>Example: sACN universe = 8, start = 1, bits = 16</em></p>

<p align="center" style="margin: 0.5rem 0 2rem;">
  <img src="/assets/images/watchers/dmx_watcher_sacn.png" alt="sACN watcher values shown as percentages"
       style="width: 49%; border-radius: 10px; filter: drop-shadow(0 12px 22px rgba(0, 0, 0, 0.24));">
</p>

<p align="center" style="margin: 2rem 0 0.5rem;"><em>Example: Art-Net universe = 8, start = 1, bits = 8</em></p>

<p align="center" style="margin: 0.5rem 0 2rem;">
  <img src="/assets/images/watchers/dmx_watcher_artnet.png" alt="Art-Net watcher values shown as decimal values"
       style="width: 49%; border-radius: 10px; filter: drop-shadow(0 12px 22px rgba(0, 0, 0, 0.24));">
</p>

## Adding an OSC Watcher

Click **Add OSC Watcher** and enter an OSC address pattern. OSC watchers use two special characters:

- `*` matches any text at that position.
- `#` marks the part of the address whose value you want to watch.

For example, `/position/xyz/*/#/*` watches the value at the second-to-last segment of any matching address.

OSC values are shown as their raw value.

<p align="center" style="margin: 2rem 0 0.5rem;"><em>Example: address = “/position/xyz/*/#/*”</em></p>

<p align="center" style="margin: 0.5rem 0 2rem;">
  <img src="/assets/images/watchers/osc_watcher_values.png" alt="OSC watcher values shown in Wireshark's packet list"
       style="width: 65%; border-radius: 10px; filter: drop-shadow(0 12px 22px rgba(0, 0, 0, 0.24));">
</p>

## Setting Up Columns

Use [Configure Columns](/docs/columns/) to add a custom column for each watcher. Set **Type** to **Custom** and enter the field shown in the Watchers window, such as `show.watcher.1`. The column remains blank for packets that do not match the watcher.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/docs/host-table/">← Host Table</a></div>
  <div style="text-align: right;"><a href="/docs/filter-builder/">Filter Builder →</a></div>
</div>
{:/}
