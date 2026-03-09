---
layout: default
title: Capturing
nav_order: 3
has_children: true
nav_fold: false
permalink: /docs/capturing/
---

<h1 align="center">Capturing Network Traffic</h1>

---
Wireshark captures network packets as they travel across your network interface. ShowShark then analyses the captured data to provide entertainment network-specific insights.
The more packets you capture, the more complete ShowShark's analysis becomes, but on the flip side, larger captures require more processing time.

{: .note }
> Future documentation will include more detailed ShowShark and entertainment-specific capture guidance, with examples and screenshots. In the meantime, the official Wireshark documentation is a great resource for learning effective capture workflows.

## Very Quick Capture Steps

1. **Choose the Interface** - On opening Wireshark, select the interface where your entertainment traffic is flowing (Wi-Fi, Ethernet, etc.).
	*See*: [Wireshark: Capture Interfaces](https://www.wireshark.org/docs/wsug_html_chunked/ChCapInterfaceSection.html)

2. **Start the Capture** - Press the green "Start capturing" button and let the capture run for long enough to see a representative sample (often ~1 minute is plenty).
	*See*: [Wireshark: Main Toolbar](https://www.wireshark.org/docs/wsug_html_chunked/ChUseMainToolbarSection.html)

3. **Stop the Capture** - Click the red square button to stop capturing.

4. **Open Host Table** - View discovered devices via _Tools > ShowShark > Host Table_.
	*See*: [Host Table](/docs/guide/host-table/)

5. **Explore** - Browse the packet list and packet details panes, and try different column layouts.
	You can also try display filters (including via ShowShark's [Filter Builder](/docs/guide/filter-builder/)) to focus on specific traffic types.
	*See*: [Wireshark: Packet List Pane](https://www.wireshark.org/docs/wsug_html_chunked/ChUsePacketListPaneSection.html), [Wireshark: Packet Details Pane](https://www.wireshark.org/docs/wsug_html_chunked/ChUsePacketDetailsPaneSection.html), and [Wireshark: Display Filter Toolbar](https://www.wireshark.org/docs/wsug_html_chunked/ChUseFilterToolbarSection.html)

6. **Save Important Captures** - Use _File > Save As_ to keep capture files for later analysis.

## Other Resources

See [ShowShark Resources](/docs/resources/)

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
	<div><a href="/docs/setup/configuration-profile/">← Configuration Profile</a></div>
	<div style="text-align: right;"><a href="/docs/analysing/">Analysing →</a></div>
</div>
{:/}

