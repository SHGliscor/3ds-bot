## 3ds Bot Project Progress So Far

The 3ds bot has moved from a basic prototype/mockup into a supervised detection and reporting tool. It is currently designed to stay safe: report-only, portable-only, and input-locked. No RUN, touch, A/B, D-pad, battle, or catch automation has been enabled yet.

## Completed So Far

| Area | What We Have Done | Status |
|---|---|---:|
| Core app structure | Built a portable Windows-style bot package with GUI, reports, recordings folders, logs, and organized build outputs. | Done |
| Clean ZIP structure | Updated builds so files sit inside one top-level folder and reports/logs are moved into their own folders instead of cluttering the root. | Done |
| Safety lock system | Added safety locks so the bot remains report-only and cannot send input/touch/button actions. | Done |
| Input authority | Kept RUN/input redirection as a planned/report-only layer, locked by default. | Locked |
| Capture/viewer layout | Built the main game viewer UI and cleaned the layout around the gameplay frame. | Mostly done |
| Black border cleanup | Improved the viewer so capture-card black borders are visually reduced while keeping gameplay dimensions. | Done |
| Live stats panel | Added live stats into the UI and moved it into cleaner empty space around the viewer. | In progress |
| Live hunt cleanup | Removed unnecessary live hunt text/labels and reduced clutter in the main UI. | Done |
| Species count | Added species count tracking and live encounter counting. | In progress |
| Last seen tracking | Added last-seen Pokémon tracking, but it still needs fixing for some routes/species like Koffing/Numel tests. | Needs work |
| OCR encounter detection | Added OCR-based Pokémon name detection from the encounter/nameplate area. | Working, needs polish |
| OCR audit/reporting | Added OCR audit output so detections can be checked from reports. | Done |
| Route profile support | Added route profiles and route/profile loading. | In progress |
| Route selector/search | Added route selector/search and route trust warnings. | Done |
| Route confidence tiers | Added GREEN/YELLOW/RED route confidence tiers. | Done |
| Route 101 profile | Built and tested Route 101 as a known working ORAS route profile. | Working |
| Bulk ORAS route profiles | Added many ORAS land route profiles as RED/UNTESTED placeholders. | Added, needs validation |
| Fiery Path testing | Began testing Fiery Path; found live stats/last seen/species count issues. | Active issue |
| Target matching | Added target Pokémon matching/reporting logic. | In progress |
| Target switch validation | Built a manual/report-only validation kit for switching target Pokémon such as Zigzagoon/Poochyena. | Done |
| Decision timeline | Added report fields showing detected Pokémon, target match, final action, safety lock, OCR audit, and decision timeline. | Done |
| Manual unlock review gate | Added a report-only manual unlock qualification gate. | Done |
| RUN automation | Still disabled. Bot currently reports HOLD/NO_RUN rather than pressing buttons. | Not enabled |
| RAM/NTR research | Pulled RAM/address references from PKMN-NTR and packaged ORAS address tables into CSV/JSON. | Researched, paused |
| External references | Added PokémonDB as the primary route/encounter data source, with 3DSRNGTool, PKHeX, and PKMN-NTR as supporting references. | Done |
| Build metadata | Added requirement that report/build labels, app titles, logs, dashboards, and metadata match the current build name. | Standard added |
| Testing workflow | Shifted testing toward small 5–10 encounter batches due to limited time. | Standard added |

## Current State

| Bot Mode | Estimated Progress |
|---|---:|
| Safe supervised detection bot | 65–70% |
| Full automated RE shiny hunting bot | 45–50% |
| Fully polished, route-complete ORAS bot | 35–45% |
| **Total overall progress** | **45–50%** |

## Current Strengths

- The bot is now much more than a mockup.
- The UI is cleaner and more practical.
- Safety locks are strong.
- Route/profile infrastructure exists.
- OCR detection works enough to drive reports and live stats.
- Reports are useful for debugging.
- Build packaging is cleaner and easier to test.
- We have started ORAS-specific route support.

## Current Known Issues

| Issue | Notes |
|---|---|
| Live stats not always updating | Koffing and Numel tests showed missed or incorrect updates. |
| Last seen not reliable yet | Last seen did not update correctly for Koffing. |
| Species count still inconsistent | Fiery Path test only added one Numel when more were expected. |
| Route profiles need validation | Bulk ORAS routes exist but many are still RED/UNTESTED. |
| OCR still needs hardening | Needs better encounter-state handling and species confirmation. |
| No real automation yet | RUN/input control remains locked/report-only. |

## Current Focus

The active focus is fixing live stats and encounter tracking on Fiery Path.

Current test target:

```text
Fiery Path:
- Koffing should update last seen
- Numel should increment species count correctly
- Live stats should update every confirmed encounter
- No input/touch/button actions should be sent
