---
layout: default
title: Configure Columns
parent: Guide
nav_order: 4
permalink: /docs/columns/
---

<h1 align="center">Configure Columns</h1>

---
ShowShark includes additional columns in Wireshark's packet list for entertainment-specific information such as hostnames and universe numbers.

You can choose which packet information is shown and arrange the columns in the order that works for you.

The ShowShark [Configuration Profile](/docs/configuration-profile/) includes a default column layout to get you started. You can customise it later.

## Modify Columns

Use Wireshark's Column Preferences to add, remove, and reorder columns.

1. Right-click any column heading in the packet list and select **Column Preferences**.

   <p align="center">
     <img src="/assets/images/columns_dialog.png" alt="Wireshark Column Preferences"
          style="width: 75%;">
   </p>

2. Use **+** to add a column or **–** to remove the selected column.
3. Choose the column type:
	- For a standard Wireshark column, choose the relevant **Type**, such as **Source** for the source IP address.
	- For a ShowShark column, set **Type** to **Custom** and enter its field name, such as `show.source.name` for Source Name.
4. Use **Up** and **Down** to reorder the columns.
5. Click **OK** to apply your changes.

## ShowShark Column Examples

Set **Type** to **Custom**, then enter a ShowShark field name in the **Fields** box:

- Source Name: `show.source.name`
- Destination Name: `show.dest.name`
- Universe: `show.dmx.universe`
- Watcher 1: `show.watcher.1`
- Watcher 2: `show.watcher.2`

Watcher columns keep selected DMX or OSC values visible while you move through packets. See [Watchers](/docs/watchers/) to configure them.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
	<div><a href="/docs/menus/">← Menus</a></div>
	<div style="text-align: right;"><a href="/docs/capturing/">Capturing →</a></div>
</div>
{:/}
