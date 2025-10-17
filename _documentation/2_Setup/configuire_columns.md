---
layout: default
title: Configuire Columns
parent: Setup
nav_order: 2
permalink: /documentation/columns/
---

<h1 align="center">Columns</h1>

---
ShowShark adds extra informational fields to the packet list in Wireshake. These columns expose entertainment-specific information such as hostnames and universe numbers.

The columns are customisable however as a starter, follow the below instructions and you can add or remove columns as needed later on.

## Editing Columns

There are two types of columns we need; default Wireshakr columns and custom ShowShark columns.

1. Right click any column header (where you see Time, Protocol, Info, etc.) in the packet list and choose **Column Preferences**.
2. For now, clear all the columns by selecting each one and clicking the **–** button.
3. Copy the format as per the screenshot, adding columns using the **+** button:
	- For default Wireshark columns, set the **Type** to the appropriate type (for example **Source** for the source IP address).
	- For ShowShark columns, set the **Type** to **Custom** and enter the field name (for example `show.source.name` for Source Name).
4. You can reorder columns using the **Up / Down** buttons.
5. Click **OK** to apply the changes.
In the Column Preferences window:

![Lighting data column template](/assets/columns_dialog.png)

---

**Next step:** [Applying Colour Rules](/documentation/colour-rules/) to visually organise your packet list.
