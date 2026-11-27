---
codex: 1
project: Hardware.ChiMesh
code: HCM
layer: stories
status: living
updated: 2026-11-22
---
<!-- GENERATED from MindAttic.Tickets/data/Tickets.db by `tickets db render`. Do not edit: this file is rewritten from the database; change stories and tickets with the tickets CLI. -->

# Hardware.ChiMesh — User Stories
> ✅ done (shipped & tested) · 🟡 partial · ⬜ planned. Every ✅ cites the test.

## Priority backlog
_Nothing recorded yet._

## Tickets
> Permanent log of every change and fix — this repo's ticket system. Rows are append-only: never
> delete or reword one; only move its Status (open → closed / wont-do) and fill in Ref. Status is
> a word, not a glyph, so tickets don't count toward the story index. Keep this section last.

| ID | Date | Type | Status | Summary | Ref |
|---|---|---|---|---|---|
| HCM-T1 | 2026-11-22 | docs | closed | Start the permanent ticket log in the ticket database | — |
| HCM-T2 | 2026-11-22 | docs | closed | 2026-11-22 morning | — |
| HCM-T3 | 2026-11-24 | fix | wont-do | Hunt the whole repo for real bugs with no time limit and fix every confirmed one | portfolio reset: generic bughunt sweep; defects found during the hardware build are filed as fix tasks |
| HCM-T4 | 2026-11-27 | feature | open | Provisioning sets a secured channel and the docs match the repo before any hardware is built | — |
| HCM-T5 | 2026-11-27 | feature | open | provision-node.ps1 applies one shared PSK to every node per RFC 0001 | — |
| HCM-T6 | 2026-11-27 | feature | open | Add optional -Psk to scripts/cli/provision-node.ps1 and ChiMesh.Console provision per RFC 0001 option 3 (write with meshtastic --ch-set psk, read back to confirm, never echo the key); keep default-PSK behaviour only when -Psk is omitted; PS 5.1 ASCII-safe | — |
| HCM-T7 | 2026-11-27 | docs | open | README Configure the node: generate one PSK on the first node, pass it to the rest with -Psk, Option 2 channel-URL fallback; mark RFC 0001 status implemented and drop the default-PSK line from Limitations | — |
| HCM-T8 | 2026-11-27 | feature | open | BIBLE and README cite only files that exist, and the parts table is current | — |
| HCM-T9 | 2026-11-27 | docs | open | docs/BIBLE.md Â§3 and Â§4.1 still cite tools/build-readme.ps1 and README.htm, both removed when the GitHub Pages docs site was adopted (CM-T31): point them at the docs site, regenerate BIBLE.digest.md, codex doctor passes | — |
| HCM-T10 | 2026-11-27 | docs | open | Re-check every part in config/parts.json (price, link, stock) and copy the result by hand into the README parts tables (CM-LAW-7); note the check date | — |
| HCM-T11 | 2026-11-27 | feature | open | One node built exactly by the guide, provisioned, healthchecked and holding up outdoors on solar | — |
| HCM-T12 | 2026-11-27 | feature | open | Parts ordered, one node assembled, flashed, provisioned and passing the healthcheck | — |
| HCM-T13 | 2026-11-27 | chore | open | Owner hands-on: order one node worth of core parts plus consumables and tools from config/parts.json (SMA not RP-SMA, LFP cell, TP5000) | — |
| HCM-T14 | 2026-11-27 | chore | open | Owner hands-on: TP5000 jumper to LFP first (CM-LAW-3), assemble per README Assemble, flash stock Meshtastic over USB with the cell unplugged (CM-LAW-2); note any guide step that was wrong or unclear | — |
| HCM-T15 | 2026-11-27 | chore | open | Run ChiMesh.Console provision chimesh-001 with -Psk and healthcheck; all six checks pass (a public Meshtastic node or phone app may serve as the NodeDB peer); paste the output into README Verify the mesh; file fix tasks for script defects | — |
| HCM-T16 | 2026-11-27 | docs | open | Correct the README Assemble/Flash/Configure steps from the first-build notes, and move BIBLE Â§6 tooling and node rows to verified with the date | — |
| HCM-T17 | 2026-11-27 | feature | open | The node runs outdoors on its panel and LFP cell for seven days and the power budget is confirmed | — |
| HCM-T18 | 2026-11-27 | chore | open | Owner hands-on: install the LFP cell, mount the node outdoors, log battery voltage daily (meshtastic --info or app telemetry) for seven days | — |
| HCM-T19 | 2026-11-27 | docs | open | Write the measured harvest vs draw from the seven-day run into README Power budget and Limitations, and decide whether a second cell or 5 W panel is needed | — |
