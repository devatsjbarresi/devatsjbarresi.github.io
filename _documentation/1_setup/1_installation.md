---
layout: default
title: Installation
parent: Setup
nav_order: 1
permalink: /docs/setup/installation/
---

<h1 align="center">Installation</h1>

---
ShowShark is easy to install. Here’s how to get started:

### Install Wireshark

Download and install the latest version of <a href="https://www.wireshark.org/download.html" target="_blank" rel="noopener noreferrer">Wireshark</a> for your operating system (macOS, Windows, or Linux).

Follow the instructions on the Wireshark website to complete the installation; you may need to install additional components such as WinPcap or Npcap on Windows which the installer will guide you through.

### Download the ShowShark Plugin

Download the latest version of the ShowShark plugin from the [ShowShark Download page](/download/).

### Open Wireshark

On first run, Wireshark may prompt you to allow access to network interfaces. Grant permission as needed to enable packet capturing.

### Find The Plugin Folder

1. Go to the menu:
- On Mac: Wireshark > About Wireshark > Folders.
- On Windows/Linux: Help > About Wireshark > Folders.
2. Find the entry called _Personal Lua Plugins_.

<img src="/assets/images/about_folders.png" alt="About Wireshark Folders dialog" style="display: block; margin: 0 auto;">

### Copy the Plugin File

1. Double click the folder path to open it in your file explorer and allow it to create the folder if it doesn't already exist.
2. Remove any other ShowShark plugin versions from this folder, including any ShowShark specific folders.
3. Copy the downloaded ShowShark Lua plugin file (e.g., `ShowShark_vX_X.lua`) from downloads into this folder.

### Enable the Plugin

1. In Wireshark, go to _Analyze > Reload Lua Plugins_ to load ShowShark into Wireshark (or restart Wireshark).
2. You should be greeted with the ShowShark About dialog, confirming that the plugin has loaded successfully. You should also see two new options in _Tools_ menu: _ShowShark_ and _ShowShark Filter Builder_.
3. Now, enable the plugin by going to _Analyze > Enabled Protocols..._, searching for "SHOW", and tick the checkbox.

<img src="/assets/images/setup/setup_window_enable_showshark.png" alt="Enable ShowShark protocol" style="display: block; margin: 0 auto;">

Whilst you're here, you may want to also enable:
- ACN including ACN over UDP
- ARTNET including artnet-udp

<img src="/assets/images/setup/setup_window_enable_acn.png" alt="Enable ACN protocols" style="display: block; margin: 0 auto;">
<img src="/assets/images/setup/setup_window_enable_artnet.png" alt="Enable Art-Net protocols" style="display: block; margin: 0 auto;">

Click _OK_ to apply the changes.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
	<div><a href="/docs/setup/">← Setup</a></div>
	<div style="text-align: right;"><a href="/docs/setup/configuration-profile/">Configuration Profile →</a></div>
</div>
{:/}

