## What's New

- Added 3 colour filter options to display menu.
- Added function to display DMX values by percent, hex or decimal.
- Added Art-Net poll flag.
- Added `show.artnet.poll` field.

## What's Fixed

- Fixed auto-update of host table.
- Fixed handling of multicast destination addresses correctly.
- Fixed bug that was showing multiple devices as IGMP querier.
- Fixed bug that was showing “non-entertainment” devices in the host table.
- Significantly improved performance.


## Known Issues
- Editing manufacturer and protocol filters manually may not update correctly in the Filter Builder.
- Host table is missing filter buttons.
- SLP rows are not added correctly in packet details.
- mDNS does not parse hostnames.
- MAC addresses as source or destination are not handled (for example, layer 2 broadcast).
- Custom display filter fields `show.sacn.universe` and `show.sacn.dmx` are not yet functional.