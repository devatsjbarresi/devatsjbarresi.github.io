---
layout: default
title: Configure Columns
parent: Guide
nav_order: 3
permalink: /documentation/guide/columns/
---

<h1 align="center">Columns</h1>

---
ShowShark adds extra informational fields to the packet list in Wireshark. These columns expose entertainment-specific information such as hostnames and universe numbers.

The columns are customisable; however, as a starter, follow the instructions below and you can add or remove columns as needed later on.

**To reset columns to ShowShark defaults:** Go to **Tools > ShowShark > 2 Displays > Reset Columns**.

## Editing Columns

There are two types of columns we need; default Wireshark columns and custom ShowShark columns.

1. Right click any column header (where you see Time, Protocol, Info, etc.) in the packet list and choose **Column Preferences**.
2. For now, clear all the columns by selecting each one and clicking the **–** button.
3. Copy the format as per the screenshot, adding columns using the **+** button:
	- For default Wireshark columns, set the **Type** to the appropriate type (for example **Source** for the source IP address).
	- For ShowShark columns, set the **Type** to **Custom** and enter the field name (for example `show.source.name` for Source Name).
4. You can reorder columns using the **Up / Down** buttons.
5. Click **OK** to apply the changes.

In the Column Preferences window:

<p align="center">
  <img src="/assets/images/columns_dialog.png" alt="Lighting data column template"
       style="width: 75%;">
</p>

{: .note }
> The table currently doesn't display well on small screens given all the parameters. The window can be stretched to view all columns. The next version will include filter buttons to show and hide columns for easier viewing.

---

<div style="display: flex; justify-content: space-between; align-items: center;">
  <a href="/documentation/guide/host-table/">< Host Table</a>
  <a href="/documentation/guide/filter-builder/">Filter Builder ></a>
</div>
