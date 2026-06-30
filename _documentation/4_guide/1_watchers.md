---
layout: default
title: Watchers
parent: Features
nav_order: 10
permalink: /docs/watchers/
---

<h1 align="center">Watchers</h1>

---

Watchers let you capture specific protocol values (for example DMX or OSC values) and expose them as ShowShark watcher columns so you can track how those values change over time.

Use Watchers when you want to follow value progression across packets instead of manually opening packet details each time.

{: .tip }
> Watchers are intended to be part of normal analysis workflow: create a watcher, apply it, then add watcher columns to your packet list.

## Quick Start

1. Open Wireshark and load a capture.
2. Go to _Tools > ShowShark Tools > Watcher_.
3. Add a watcher using **Add DMX Watcher** or **Add OSC Watcher**.
4. Click **Apply Watcher**.
5. Add watcher columns in Wireshark column preferences using custom fields like `show.watcher.1`, `show.watcher.2`, and so on.
6. Review value progression directly in the packet list.

## Watcher Types (Current)

- Protocol/value watchers exposed by ShowShark internals.
- DMX value tracking watchers.
- OSC value tracking watchers.

{: .note }
> Watchers are based on ShowShark-captured values that may not appear as normal default packet-dissector fields.

## Detailed Workflow

## 1. Open Watcher Window

Open _Tools > ShowShark Tools > Watcher_ to launch the watcher editor.

## 2. Add Watchers

Use the bottom-row watcher controls:

- **Add DMX Watcher**
- **Add OSC Watcher**
- **Revert**
- **Online Help**
- **Apply Watcher**
- **Close**

## 3. Apply Watchers

After adding or editing watchers, click **Apply Watcher** so the active watcher list is used.

## 4. Show Watchers in Columns

Open Wireshark column preferences and add **Custom** columns that point to watcher fields.

Example field names:

- `show.watcher.1`
- `show.watcher.2`
- `show.watcher.3`

{: .important }
> Use dot index format (`show.watcher.1`) for watcher field names.

## 5. Edit or Remove Watchers

You can manually edit existing watcher entries or remove them from the Watcher window, then re-apply.

## Output You Should Expect

- Watcher values shown in packet-list columns.
- Fast visual tracking of value progression across packets.

## Practical Playbooks

## DMX Progression Check

1. Add a DMX watcher.
2. Apply watchers.
3. Add a `show.watcher.1` column.
4. Sort or scan packets and verify progression patterns.

Use this to confirm expected ramps, step changes, or stuck values.

Example DMX watcher expression:

- `show.sacn.dmx {universe = 1, channel = 1, bit_depth = 16}`

## OSC Value Check

1. Add an OSC watcher.
2. Apply watchers.
3. Add a `show.watcher.1` or `show.watcher.2` column.
4. Verify incoming OSC value changes over time.

Use this to confirm control data is updating as expected.

## Screenshot Placeholders

### Watcher Window Controls

![Watcher window controls placeholder](/assets/images/placeholders/watchers-placeholder.svg)

### Watcher List After Apply

![Watcher list placeholder](/assets/images/placeholders/watchers-placeholder.svg)

### Packet List with Watcher Columns

![Watcher column placeholder](/assets/images/placeholders/watchers-placeholder.svg)

## Current Limitations

- No special caveats to call out beyond standard workflow.
- Documentation examples will expand as more watcher types are added.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/docs/capturing/">← Capturing</a></div>
  <div style="text-align: right;"><a href="/docs/menus/">Menus →</a></div>
</div>
{:/}
