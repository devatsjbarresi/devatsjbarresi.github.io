---
layout: default
title: Installation
parent: Guide
nav_order: 1
permalink: /docs/installation/
---

<h1 align="center">Installation</h1>

---
Follow these steps to install ShowShark and enable it in Wireshark.

## Install Wireshark

Download and install the latest version of <a href="https://www.wireshark.org/download.html" target="_blank" rel="noopener noreferrer">Wireshark</a>. Follow the Wireshark installation instructions for your system; on Windows, the installer will guide you through any required additional components.

## Download ShowShark

Download the latest version of ShowShark from the [Download page](/download/), then unzip it. The archive contains the ShowShark Lua plugin and an example capture file.

## Open Wireshark

On first run, Wireshark may prompt you to allow access to network interfaces. Grant permission as needed to enable packet capturing.

## Find the Plugin Folder

1. Open **About Wireshark**:
   - macOS: _Wireshark > About Wireshark_
   - Windows and Linux: _Help > About Wireshark_
2. Select **Folders**.
3. Find **Personal Lua Plugins**.

<img src="/assets/images/about_folders.png" alt="About Wireshark Folders dialog" style="display: block; margin: 0 auto;">

## Copy the Plugin File

1. Double-click the **Personal Lua Plugins** path to open the folder. If it does not exist, allow Wireshark to create it.
2. Remove any earlier ShowShark plugin files or folders.
3. Copy the ShowShark Lua plugin file—for example, `ShowShark_v1_0_BETA5.lua`—from the unzipped download into the **Personal Lua Plugins** folder.

## Enable the Plugin

1. In Wireshark, select _Analyze > Reload Lua Plugins_, or restart Wireshark.
2. The ShowShark About dialog should appear, confirming that the plugin has loaded. You should also see several menus containing "ShowShark" under _Tools_.
3. Go to _Analyze > Enabled Protocols_.
4. Search for `SHOW` and select its checkbox.
5. Click **OK**.

<img src="/assets/images/enable_protocols_show.png" alt="Enable ShowShark protocol" style="display: block; margin: 0 auto;">

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
	<div><a href="/docs/guide/">← Guide</a></div>
	<div style="text-align: right;"><a href="/docs/configuration-profile/">Configuration Profile →</a></div>
</div>
{:/}
