---
layout: default
title: Configure Columns
parent: Guide
nav_order: 3
permalink: /docs/guide/columns/
---

<h1 align="center">Columns</h1>

---
ShowShark adds extra informational fields to the <a href="https://www.wireshark.org/docs/wsug_html_chunked/ChUsePacketListPaneSection.html" target="_blank" rel="noopener noreferrer">packet list</a> in Wireshark. These columns expose entertainment-specific information such as hostnames and universe numbers.

The columns are customisable; however, as a starter, use the default columns provided by ShowShark which are included in the ShowShark [Configuration Profile](/docs/setup/configuration-profile/).

To reset columns to ShowShark defaults: Go to _Tools > ShowShark > 2 Displays > Reset Columns_.

## Editing Columns

There are two types of columns we need; default Wireshark columns and custom ShowShark columns.

1. Right click any column header (where you see Time, Protocol, Info, etc.) in the <a href="https://www.wireshark.org/docs/wsug_html_chunked/ChUsePacketListPaneSection.html" target="_blank" rel="noopener noreferrer">packet list</a> and choose **Column Preferences**.
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


---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
	<div><a href="/docs/guide/host-table/">← Host Table</a></div>
	<div style="text-align: right;"><a href="/docs/guide/filter-builder/">Filter Builder →</a></div>
</div>
{:/}
