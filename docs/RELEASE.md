---
layer: release
status: living
---
# ChiMesh — Release charter

> The one finish line this repo is working toward. Every open ticket in this repo sits under one of the epics
> below, and every epic is part of the milestone. Work that does not fit is out of scope until this milestone is
> reached (owner, 2026-11-27, MAT-T319).

## 1. What this is
A buildable guide and PowerShell tooling for solar-powered RAK4631 Meshtastic nodes (stock firmware, LiFePO4
power) that prove multi-hop LoRa routing across Chicago.

## 2. The milestone: ChiMesh 1.0, first node live {#milestone}
- **Milestone:** MS-71, "first node built, provisioned and running on solar"
- **Published means:** the guide is the GitHub README plus its GitHub Pages docs site; the unit is one physical
  node deployed outdoors.
- **The natural stopping point:** the guide, parts catalog and provision/healthcheck tooling exist but have never
  met hardware. One node, built exactly by the guide, provisioned on a secured channel, passing the healthcheck and
  holding up on solar outdoors for a week, proves the whole build path and the power chain. Every later node is a
  repeat of a proven recipe, so this is where the guide becomes trustworthy.

## 3. Done when (acceptance checks)
1. exists — `scripts/cli/provision-node.ps1` accepts `-Psk` and the README documents the secured channel (RFC 0001).
2. signoff — one node assembled per the README, provisioned with `ChiMesh.Console provision`, and
   `healthcheck` passes all six checks; output recorded in the README's Verify section.
3. signoff — the node runs outdoors on its panel and LFP cell for seven days without a brown-out; the observed
   power numbers are recorded in the README's Power budget.

## 4. Epics, in priority order
| Priority | Epic (ticket) | What it delivers | Features |
|---|---|---|---|
| 900 | HCM-T4 Node tooling ready | Secured-channel provisioning and docs that match the repo | HCM-T5 Secured channel PSK (990), HCM-T8 Docs match the repo (980) |
| 800 | HCM-T11 First node live | One node built, provisioned, healthchecked and proven on solar | HCM-T12 Build and provision (890), HCM-T17 Outdoor solar run (880) |

## 5. Out of scope (not before this milestone)
- The three-node multi-hop proof (`A → via B → C`) — the next milestone; it is two more copies of this one.
- v2 disguised lamp-style enclosure — after the protocol is proven.
- Custom or forked firmware — CM-LAW-5, stock Meshtastic only.
- An interactive configurator, cost calculator or generated parts table — the README is static by design.
- Winter power upgrades (second cell, 5 W panel) — documented options; only acted on if the outdoor run shows need.
- Repo-wide bughunt sweeps — defects found while building are filed as fix tasks.

## 6. Current verified state
- README sections 01–08, `config/parts.json` (20 parts, 4 axes), `config/versions.json` and part images exist and
  cross-reference (review only).
- `provision-node.ps1` / `healthcheck-mesh.ps1` / `ChiMesh.Console` hardened across CM-T11..T29 (region codes,
  exit codes, PS 5.1 parsing, read-back confirmation, pull-latest fast-forward) — never run against hardware.
- Docs site on GitHub Pages (f93c254, CM-T31).
- No node has been ordered or built; channel 0 still uses the default PSK.

## 7. Decision record
- 2026-11-27 — charter drafted from README, BIBLE, RFC 0001 and tickets (FOR-T41); Legion vote: Approve, plurality quorum reached, 6/6 answering voters approve (3 providers without keys), no dissent.
- Triage: 1 open → done 0, duplicate 0, wont-do 1 (HCM-T3 generic bughunt), kept 0, new tasks 10.
