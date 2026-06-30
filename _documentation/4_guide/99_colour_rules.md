---
layout: default
title: Colour Rules
nav_exclude: true
published: false
permalink: /docs/colour-rules/
---

<h1 align="center">Applying Colour Rules</h1>

---
ShowShark includes a colour rules file which helps visualise different types of traffic in the packet list.

When the plugin is loaded, it places the colour rules file in the ShowShark documents folder. The folder can be accessed via _Tools > ShowShark > Open Documents Folder_.

## Apply Colour Rules

1. Open Wireshark
2. Go to _View > Coloring Rules..._
3. Click the **Clear all colouring rules** button.
4. Click the **Import...** button.
5. Navigate to the ShowShark documents folder and select `ShowShark_Colour_Rules_1.0.colours`.
6. Click **OK** to apply the colour rules.

<img src="/assets/images/colour_rules.png" alt="Wireshark Colouring Rules dialog" style="display: block; margin: 0 auto;">


> **Note:** The colour rules file includes Wireshark's default colouring rules. It's safe to clear all existing rules before importing—no default colours will be lost.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
	<div><a href="/docs/filter-builder/">← Filter Builder</a></div>
	<div style="text-align: right;"><a href="/docs/capturing/">Capturing →</a></div>
</div>
{:/}


{: .note }
> *The table currently doesn't display well on small screens given all the parameters. The window can be stretched to view all columns. The next version will not use the display level settings, but will include filter buttons to show and hide columns for easier viewing.*

{: .warning }
> This is a warning callout with orange styling. Use it for cautionary information.

{: .important }
> This is an important callout with red styling. Use it for critical information that must not be missed.

{: .highlight }
> This is a highlight callout with purple styling. Use it to emphasize key points or special information.

{: .new }
> This is a 'new' callout with green styling. Use it to highlight new features or recent updates.