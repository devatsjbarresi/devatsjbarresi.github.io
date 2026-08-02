# Internal Documentation Workshop Notes

This untracked file is private working memory for the ongoing website
documentation
workshop. It is not product documentation and should not be published or
committed. Update it as each section is discussed so future sessions can pick up
the work without restating the brief.

## Working brief

- Discuss exactly one question, decision, or text block at a time. Do not present
  batches of questions.
- Read the relevant GitSite material before asking. Do not ask the user for
  information that the website already provides; questions should address
  genuine gaps, ambiguities, or working preferences.
- Do not edit any website file until the user has explicitly approved the
  proposed wording.
- Once wording is approved, apply it to the website immediately so the user can
  inspect the real file before the workshop moves on.
- Maintain this private notes file as needed without asking for approval or
  presenting its wording. For all public website content, bring the real page to
  the front in the browser and workshop the text with the user there.
- Keep the workshop conversational rather than following a rigid
  critique/rewrite procedure. Call out existing wording only when it is
  genuinely confusing, inaccurate, inconsistent, or unusually awkward.
- Normally propose one considered version of a text block. The user will request
  an alternative or specify adjustments when needed.
- Flag factual inconsistencies and broken links immediately, even when they are
  outside the text block currently being discussed.
- When applying approved wording, silently correct obvious spelling,
  punctuation, and formatting issues within that block without changing its
  meaning.
- Describe functionality as current only when it works in the public release.
  Unfinished or future functionality must be clearly labelled as planned.
- Work through the GitSite website one section or small block at a time.
- Workshop the wording collaboratively before moving on.
- Write for both newcomers and experienced users.
- Explain unfamiliar ideas in plain language, but use the correct technical
  terms where they are useful or necessary.
- Avoid over-explaining concepts that experienced users can reasonably work out
  for themselves.
- Keep the writing approachable, practical, and technically accurate.
- Use a friendly, direct, and informative tone. Do not sound formal,
  patronising, overly jovial, or padded with marketing language. Include all
  information relevant to the task without labouring obvious points.
- Use the approved opening of the main ShowSquid page as the reference example
  for tone: plain, technically accurate, friendly, and complete without
  padding.
- The revised Advanced Mode opening and "While Running" text also match the
  target tone and should be used as references during later sections.
- Use a neutral project voice: "ShowShark does..." and "ShowSquid sends...".
  Avoid "we" and avoid writing as though the products themselves are speaking.
- Address the reader as "you" where a pronoun is naturally required, especially
  in instructions. Do not force second-person wording into sentences that are
  clearer without it.
- Decide case by case whether unfamiliar technical terms need an inline
  explanation. Suggest one when it materially helps, rather than applying a
  rigid first-use rule or relying automatically on the Definitions page.
- Practical pages should mostly stand alone, particularly individual feature
  pages, while assuming a little prior knowledge. Link to related setup,
  protocol, and reference pages instead of duplicating full explanations.
- GitSite covers basic Wireshark use and links to Wireshark's own resources for
  more detail. Do not over-specify the precise assumed knowledge unless it
  becomes relevant to a particular block.
- ShowShark source code is available for checking facts and behaviour only. Do
  not change it as part of the website workshop.
- Treat the reference code as the default source for current behaviour when it
  disagrees with the website, but flag the discrepancy for discussion rather
  than silently assuming the implementation expresses the intended behaviour.
- A generated page is not necessarily implemented or ready. In particular, the
  Definitions page is hidden with `nav_exclude: true` and is not implemented.
  Do not repair or add links into it as though it were live content.
- Ignore hidden pages during the current workshop unless the user explicitly
  brings one into scope.
- Preserve the current page structure and navigation unless the user says
  otherwise. Flag a clear structural problem, but do not reorganise the site
  without approval.
- Numeric prefixes are for internal filenames and navigation ordering only.
  Public URL paths must use descriptive names without those numbers.
- The workshop primarily covers wording and content. Leave screenshots and
  visual layout unchanged unless the user specifically brings them into scope.
- Review each block with the user, but do not rewrite clear and accurate text
  merely for activity or superficial consistency. "Keep as written" is a valid
  outcome.

## Progress and decisions

- The current area of work is the ShowSquid documentation.
- The long-term aim is to review every visible page, not necessarily in
  navigation order.
- Complete the outstanding documentation areas first, then return for a full
  end-to-end review of the whole site rather than repeatedly rechecking finished
  pages during the workshop.
- Priority/newer areas are ShowSquid, OSC, Watchers, and updating the Host Table.
  Much of the remaining site is already solid and may need only a light review.
- Revised the opening of the main ShowSquid page to explain its relationship
  with ShowShark, why quiet devices and multicast subscriptions can limit the
  available traffic, what ShowSquid does, and how that helps ShowShark.
- Reviewed the main ShowSquid page's "Pages" block and kept it unchanged.
- Removed the main ShowSquid page's "When To Use ShowSquid" section because the
  approved opening now conveys the same information more clearly.
- Simplified the main ShowSquid page to match the Guide and Features landing-page
  pattern: a concise introduction followed directly by its child-page links.
  The introduction briefly explains the app's purpose without duplicating the
  Getting Started page. Removed the redundant "ShowSquid Guides" and "Next
  Step" headings.
- Moved the approved explanation of why ShowSquid is needed, what it does, and
  how it helps into the Getting Started page's "What Does ShowSquid Do?"
  section.
- Corrected the Getting Started page's protocol headings so they are nested
  beneath "Protocol Overview".
- Moved mDNS, SLP, and OSC from the Essential mode protocol overview to an
  "Additional Protocols" section on the Advanced Mode page, matching the
  controls visible in the screenshots.
- Rewrote the Advanced Mode opening to replace corporate wording such as "full
  protocol surface" and "option panes" with a direct explanation of the
  additional protocols, settings, and control it provides.
- Simplified step 7 of the Advanced Mode workflow and aligned it with the
  equivalent Essential mode instruction.
- Rewrote the Advanced Mode "While Running" text to name the TX and RX
  indicators and explain the send-status text shown in the screenshot.
- Clarified that the Advanced sACN universe options join the corresponding
  multicast groups so their packets can be captured in Wireshark; ShowSquid does
  not process the packets.
- Reviewed the Advanced Mode mDNS and SLP descriptions and kept them unchanged.
- Rewrote the Advanced Mode OSC description to make clear that predefined
  manufacturer messages and user-configured custom messages can both be sent.
- Expanded the Advanced Mode OSC settings text to explain UDP Out, UDP In, and
  the 10-second send interval shown in the focused screenshot.
- Added focused screenshots beneath Manufacturer Specific on Getting Started
  and beneath the sACN, ArtPoll, and OSC settings on Advanced Mode.
- Sized focused screenshots below their overview images: 50% for Manufacturer
  Specific, and 65% for sACN, ArtPoll, and OSC.
- Added 10 px rounded corners and a moderately stronger soft drop shadow to all
  four focused screenshots, matching the full app screenshots more closely.
- Added a visible line of space before each focused screenshot.
- Renamed "Additional Protocols" to "Additional Protocols and Options" and moved
  it above sACN so it covers all advanced protocol controls and additions.
- Added an ArtPoll Options explanation covering the limited, Art-Net default,
  and per-interface directed broadcast destinations.
- Corrected the Essential mode sACN entry: it now says that sACN Discovery
  listens for discovery packets rather than claiming it sends them.
- Prefer "join" in the short protocol descriptions, but "subscribe" is also a
  useful technical term and may be introduced naturally in explanatory text.
  Corrected the Essential mode descriptions for Manufacturer Specific and PSN;
  PSN uses one multicast group.
- Rewrote the Getting Started page's Essential mode introduction to explain
  concisely that it offers a smaller protocol set with mostly automatic
  configuration. Removed an added Advanced Mode sentence because the page was
  becoming too text-heavy after the preceding explanation.
- Revisit the homepage "Introducing ShowSquid" block. Its phrases such as
  "guided analysis workflows", "traffic stimulation support", "spin up
  focused test traffic", and "validate packet flow" are too corporate,
  developer-oriented, and wordy for the site's established tone.
- Replaced the homepage "Introducing ShowSquid" copy with the fuller approved
  explanation from the Getting Started page: it describes discovery messages,
  network requests, multicast groups, and listening for traffic, followed by
  the benefit to ShowShark.
- Subsequently removed the ShowSquid introduction from the homepage and added a
  concise "About ShowSquid" block beneath the Download page's product buttons,
  linking to the ShowSquid documentation. "About" was chosen over
  "Introducing" because it will not date like a release announcement.
- Removed the ShowSquid Companion App bullet from the homepage Features list;
  ShowSquid is not part of ShowShark's core feature list and is now introduced
  more appropriately on the Download page.
- Later restored ShowSquid to the homepage Features list at the user's
  preference, using a plain description of its device prompts, multicast joins,
  and listening behaviour, with the feature name linking to its documentation.
- Renamed the homepage feature "Entertainment Host Discovery" to the plainer
  "Device Discovery". Its description remains under review.
- Rewrote the Device Discovery description to say plainly that ShowShark
  identifies entertainment devices and collects their hostnames, manufacturers,
  and device types.
- Renamed the homepage feature "Host Tables" to "Host Table" to match the tool's
  name in the ShowShark interface.
- Simplified the Host Table description to "View discovered devices, their
  properties, and the protocols they support."
- Renamed "Detailed Protocol Information" to the plainer "Protocol Details";
  kept its clear and accurate description unchanged.
- Changed the Colour-Coded Display description from future tense ("will help")
  to present tense ("helps"). Kept the feature name unchanged at the user's
  preference. Reviewed the Filter Builder and Watchers entries and kept them as
  written.
- Removed the homepage "What ShowShark Does Not Do" section. Its negative
  framing interrupted the page, and the statement that ShowShark does not
  generate traffic could confuse readers now that the wider project includes
  the traffic-generating ShowSquid companion app.
- Simplified the homepage sACN description to "Streaming ACN for transporting
  DMX data over IP networks," removing the unnecessary parenthetical expansion
  of IP.
- Replaced the vague Art-Net description with a direct explanation that it
  transports DMX data and discovers devices over IP networks.
- Reworded the homepage IGMP description to explain that it manages IPv4
  multicast group membership for protocols such as sACN. Reviewed the concise
  mDNS description and kept it unchanged.
- Decided that the homepage Supported Protocols entries should each combine a
  very brief protocol description with what ShowShark displays or identifies,
  keeping each entry to one sentence. Updated sACN accordingly.
- Updated the Art-Net entry in the same compact format, covering DMX, device
  discovery, node details, universes, and DMX values.
- Reworked the IGMP entry collaboratively to focus on multicast subscriptions,
  querier identification, and ShowShark's clear entertainment-aware labels,
  including sACN universe numbers.
- Updated mDNS to combine its local host and service discovery role with
  ShowShark's identification of device names and advertised services.
- Updated OSC to identify it simply as Open Sound Control, then explain that
  ShowShark displays message addresses and values and supports tracking them
  with Watchers.
- Updated SLP to explain that ShowShark identifies advertised services and uses
  them to show which protocols devices support. The homepage Supported
  Protocols block is now complete.
- Removed the homepage Get Started button. The existing top-level Download
  navigation was initially considered sufficient, then the user clarified that
  the button should be replaced by the site's normal bottom text navigation.
  Added a right-aligned "Download →" link, then removed it and restored the
  original Get Started button after viewing both options in the browser.
- Reworked the Download page into separate ShowShark and ShowSquid sections.
  ShowShark now contains its version, download, Wireshark requirement, and
  Wireshark download; ShowSquid contains its short explanation, download, and
  documentation link.
- Integrated the ShowSquid documentation link into the product name in its
  Download page description and removed the separate "Learn about" link.
- Removed unnecessary bold styling from every item in the homepage BETA5 update
  list, retaining code formatting for the Host Table sort-field names.
- Removed the BETA5 update list from the homepage. All of its information is
  already represented in the Download page's version history, so no release
  details needed to be moved or duplicated.
- Moved the current BETA5 notes out of the collapsible Version History and made
  them visible below the ShowShark and ShowSquid download sections. Version
  History now contains BETA4 and earlier releases only.
- Reviewed the visible BETA5 release notes after moving them and kept their
  wording unchanged. The Download page is complete apart from adding Windows
  installer choices and finalising their links later.
- Fixed the Download page's broken `/docs/setup/` link. It now leads to
  `/docs/installation/` and is labelled "Installation".
- Moved the Advanced Mode page from `/docs/advanced-mode/` to
  `/docs/showsquid/advanced-mode/` and updated all internal links to match.
- Moved the Getting Started page from `/docs/getting-started/` to
  `/docs/showsquid/getting-started/` and updated all internal links to match.
- The sACN page contains references intended for the unfinished Definitions
  page. Treat these as unfinished content, not as ordinary broken links to fix.

## Project baseline from GitSite

- GitSite is the public ShowShark website and documentation, built with Jekyll
  and Just the Docs.
- ShowShark is a read-only Wireshark plugin for entertainment technicians of all
  experience levels.
- Its core purpose is to make entertainment-network traffic easier to see and
  understand, supporting fault-finding through device discovery, host data,
  protocol details, colour coding, filters, and value watchers.
- ShowShark processes captures locally, does not generate or modify traffic, and
  does not require special hardware for common protocols.
- ShowSquid is a separate downloadable desktop companion app. It actively
  prompts devices to communicate, listens for traffic, and gives ShowShark more
  useful capture data to analyse.
- ShowSquid is intended and should be presented as a ShowShark companion.
  Technically it can run alone, but standalone use is not useful enough to
  promote as a use case.
- ShowSquid is for temporary diagnostic use. It may be used during a live show,
  but it is not intended to remain active permanently.
- Present ShowSquid's temporary-use guidance as a calm note, not an alarming
  safety warning. Reserve stronger warnings for specific options with a real
  operational risk.
- ShowSquid's core purpose can be described as prompting quiet devices to
  communicate so ShowShark has more traffic to analyse.
- In Essential mode, sACN Discovery listens for sACN discovery packets; it does
  not send sACN discovery messages.
- sACN Discovery and ArtPoll exist in both Essential and Advanced modes.
  Advanced adds universe selection for sACN and more control over ArtPoll
  broadcast destinations.
- Manufacturer Specific also exists in Essential mode. OSC is entirely
  Advanced-only.
- Keep preliminary questions efficient. Ask a broader, more comprehensive
  question when needed, then get on with workshopping the text rather than
  conducting a long sequence of narrow questions.
- ShowSquid has Essential and Advanced modes and supports macOS and Windows
  downloads.

## Next discussion

- Continue the Advanced Mode "Additional Protocols and Options" section.
- The rendered ArtPoll explanation and screenshot spacing have been checked and
  need no further changes.
- Review the remaining ShowSquid pages in larger coherent sections.
- The ShowSquid Advanced Mode page is complete. Revisit it only during the final
  whole-site review unless a later change creates a specific inconsistency.
- Began the Installation page review from the top. Replaced its generic "easy to
  install" opening with a direct statement that the steps install ShowShark and
  enable it in Wireshark.
- Simplified the Install Wireshark block: removed the redundant operating-system
  list and obsolete WinPcap reference, while retaining a brief note that the
  Windows installer guides users through required additional components.
- Shortened the Installation page heading "Download and Unzip the ShowShark
  Plugin" to "Download ShowShark"; unzipping remains an instruction in the
  following text.
- Simplified the Download ShowShark paragraph into two direct sentences covering
  the download, unzipping, and archive contents. Reviewed the Open Wireshark
  block and kept it unchanged.
- Corrected "Find The Plugin Folder" to "Find the Plugin Folder" to follow the
  site's heading capitalisation.
- Restructured the plugin-folder directions into three correctly nested steps:
  open About Wireshark using the platform-specific menu, select Folders, and
  find Personal Lua Plugins. Kept the accompanying screenshot unchanged.
- Simplified all three Copy the Plugin File steps: open or create Personal Lua
  Plugins, remove earlier ShowShark files or folders, then copy the versioned Lua
  file from the unzipped download into that folder.
- Updated the Enable the Plugin screenshot reference to the user's manually
  edited `assets/images/enable_protocols_show.png`, which shows ShowShark 1.0
  without the outdated BETA2 suffix.
- Simplified Enable the Plugin step 1 to select Analyze > Reload Lua Plugins or
  restart Wireshark.
- Rewrote the load-confirmation step without enumerating menu names, which are
  out of date and may change. It now checks for the About dialog and several
  menus containing "ShowShark" under Tools.
- Split the final enablement instruction into three steps: open Enabled
  Protocols, search for SHOW and select it, then click OK.
- Moved "Click OK" above the screenshot so the ordered list remains continuous
  instead of restarting after the image.
- Began Configuration Profile review. Replaced the detailed opening explanation
  with a concise description of the ShowShark profile's layout and colours,
  noting that users can customise it later but should use the defaults for now.
- Simplified the Configuration Profile columns and colours bullets. In written
  menu paths, omit the leading ordering numbers from menu item names; retain
  numbers that are part of actual choices, such as `Colour Filter 1`.
- Configuration Profile is complete until the final whole-site review.
- Deferred the Menus page because it needs a larger rewrite reflecting the
  current menu structure; return to it as a separate piece of work.
- Resumed the Menus review against the current ShowShark source. Removed the
  internal `ShowShark Dev` section entirely; development/debug menus must not
  appear in the public documentation.
- Checked every public `register_menu` entry in the current ShowShark source,
  including dynamic Manufacturer and Watcher Filter Builder branches. Added a
  complete nested menu hierarchy using the menu ordering numbers as ordered-list
  markers, and removed the obsolete Build menu row.
- Reworked Menus into five linked sections with compact, borderless reference
  tables. Menu ordering numbers form the first column; menu labels remain plain
  text and links are worked into descriptions. Child menu rows are indented.
- Simplified Filter Builder to its five immediate numbered choices and linked
  the feature in its introduction; deeper protocol/manufacturer contents are
  intentionally left to the Filter Builder page.
- Rewrote Options descriptions in plain user-facing language and removed
  implementation detail about registered fields. The internal developer menu
  remains excluded.
- Applied the same compact borderless alignment to homepage Features and
  Supported Protocols, renamed the homepage feature to ShowSquid App, promoted
  those section headings to level two, and standardised visible spacing after
  level-two headings site-wide.
- Menus is complete until the final whole-site review. Its reload message stays
  a calm blue note; the orange warning treatment was tested and rejected as too
  alarming for expected behaviour.
- Configure Columns is complete until the final review. It is now a concise
  basic customisation guide rather than a full layout-rebuild procedure: it
  explains the purpose of packet-list columns, the default profile layout, and
  how to add, remove, configure, and reorder columns. The screenshot sits under
  the step that opens Column Preferences.
- Capturing received a quick tone pass: tightened the introduction, moved the
  bundled example-capture guidance to the top, rewrote the six quick capture
  steps with neutral current UI wording and inline links, corrected the Host
  Table menu path, and removed the redundant Other Resources section.
- Capturing is complete until the final whole-site review. The ShowSquid text
  explains why it helps a capture—prompting devices and joining multicast
  groups—without duplicating ShowSquid setup instructions.
- Next workshop area: Features. Continue one page and one wording decision at a
  time, then return to the deferred installer links and final whole-site review.
- Once the ShowSquid pages are complete, revisit the overly corporate ShowSquid
  copy on the homepage.
- Reviewed the Guide, Features, and ShowSquid parent pages for consistent
  purpose-led introductions and concise child-page descriptions. Guide and
  Features are complete for this pass; ShowSquid can be revisited in the final
  whole-site review.
- Host Table is complete for this pass. Reordered the page around Host
  Discovery, shared Host Information, and the two viewing locations; removed
  Quick Start, duplicated field explanations, the fixed columns table, and the
  generic Troubleshooting section. Controls now document only non-obvious
  actions. The packet-details screenshot still shows BETA2 and is intentionally
  deferred to the later screenshot pass.
- Next workshop area: Watchers.
- Watchers is complete for this pass. Tightened its introduction without losing
  the DMX and OSC examples, retained Quick Start because setup spans several
  connected steps, moved Applying Changes beside the Watchers window, removed
  the redundant button list, turned DMX display formatting into a blue note,
  and reduced column setup to a concise link to Configure Columns. Corrected
  the page navigation to Host Table and Filter Builder.
- Next workshop area: Filter Builder.
## 2026-07-29

- Reworked the Download page into aligned ShowShark and ShowSquid download cards, with Wireshark in a separate card underneath.
- Kept the example capture inside the ShowShark download rather than adding another prominent download button.
- Reworked the Filter Builder introduction, Getting Started steps, numbered menu reference, combination rules, Host Filters, Manufacturer Filters, Protocol Filters and Manual Editing sections.
- Replaced the top-level, Manufacturer and Protocol Filter Builder menu screenshots. Remaining older Filter Builder screenshots need a later replacement pass.
- Removed repetitive explanations, outdated access instructions and uncertain filter-application behaviour.

## 2026-07-30

- Treat the Wireshark links on the Resources page as the preferred references to reuse throughout the documentation: Capture Setup, Capture Interfaces, Main Toolbar, Display Filter Toolbar, Packet List Pane and Packet Details Pane.
- Reuse the ETC Resources links where relevant: Wireshark Setup and Background Info, Network Definitions, and EOS Networking Overview.
- Final consistency pass: review every top-level navigation page together and standardise their purpose, introductory copy, heading structure, contents lists, tone and child-page navigation.
- Completed the visible parent-page consistency pass for Guide, Features, ShowSquid, Resources and Reference. Parent pages use aligned child links with descriptions, disable the theme's duplicate generated contents list, and retain previous/next navigation. Resources remains a normal external-links page rather than a parent.
- Common Filters: manufacturer fields use `show.manufacturer.*`, `show.source.manufacturer.*` and `show.dest.manufacturer.*`. The documented `etc`, `hp`, `carallon` and `ma_lighting` suffixes were verified against the implementation.
- Common Filters is complete for this workshop pass. The new aggregate `show.ip` field and directional IP and manufacturer fields were verified against ShowShark.
- Completed a whole-site consistency pass: corrected numbered ShowShark menu paths, fixed Configure Columns field examples, standardised setup heading levels and page titles, repaired hidden sACN definition links, cleaned the unpublished Colour Rules draft, and continued the page navigation from Filter Builder to ShowSquid.
- A later screenshot pass is still needed wherever the documentation shows older ShowShark interfaces. Existing screenshots were left unchanged until accurate replacements are available.
