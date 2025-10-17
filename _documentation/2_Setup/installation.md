---
layout: default
title: Installation
parent: Setup
nav_order: 1
permalink: /documentation/installation/
---

<h1 align="center">Installation</h1>

---
ShowShark is easy to install even if you’re not a networking expert. Here’s how to get started:

## Install Wireshark

Download and install the latest version of [Wireshark](https://www.wireshark.org/download.html) for your operating system (macOS, Windows, or Linux).

Follow the instructions on the Wireshark website to complete the installation; you may need to install additional components such as WinPcap or Npcap on Windows. Some of this may sound scary but as long as you download Wireshark from the official site, you'll be fine.

## Download the ShowShark Plugin

Download the latest version of the ShowShark plugin from the [ShowShark Download page](/download/).

In the download, you'll find a Lua plugin file (for example, `ShowShark_v1_0.lua`).

## Open Wireshark

On first run, Wireshark may prompt you to allow access to network interfaces. Grant permission as needed to enable packet capturing.

The first Wireshark screen you see may look a bit intimidating, but don't worry! You don't need to understand everything right away. Just focus on getting ShowShark installed for now.

## Adding the Plugin to Wireshark

The easiest way to find the correct plugin folder is from within Wireshark itself:

1. Open Wireshark.
2. Go to the menu: _Wireshark > About Wireshark > Folders_ (on macOS) or _Help > About Wireshark > Folders_ (on Windows/Linux).
3. Look for the entry called _Personal Lua Plugins_. This is the folder where you should place the ShowShark plugin files.

![About Wireshark Folders dialog](/assets/about_folders.png)

4. Double click the folder path to open it in your file explorer and allow it to create the folder if it doesn't already exist.
5. Copy the downloaded ShowShark Lua plugin file (e.g., `ShowShark_v1_0.lua`) into this folder.


## Load and Enable the Plugin

1. In Wireshark, go to _Analyze > Reload Lua Plugins_ to load ShowShark into Wireshark (or restart Wireshark).
2. You should be greeted with the ShowShark About dialogue, confirming that the plugin has loaded successfully.
3. You can verify the plugin loaded by checking _Tools > ShowShark_ and _Tools > ShowShark Filter Builder_ are the menu.
4. Enable the plugin by going to _Analyze > Enabled Protocols..._, searching for "SHOW", and tick the checkbox.

Whilst you're here, it's also useful to enable:
- ACN including ACN over UDP
- ARTNET including artnet-udp

![About Wireshark Folders dialog](/assets/enable_protocols_show.png)
![Enable ACN and Art-Net protocols](/assets/enable_protocols_acn.png)
![Enable ACN and Art-Net protocols](/assets/enable_protocols_artnet.png)

5. Click _OK_ to apply the changes.

---

**Next step:** [Configure Columns](/documentation/columns/) to customise your packet list display.

