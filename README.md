# 3DS Bot Project Roadmap and Progress

Last updated: 2026-05-22

This README tracks the current state of the ORAS shiny hunting bot project.

GitHub currently represents the stable **RE-32c** baseline, while active local/chat development has moved into the **RE-33 safety, preflight, auto-focus, and guarded input planning** track.

## Overall progress

| Goal | GitHub-tracked progress | Current project estimate | Notes |
|---|---:|---:|---|
| Report-only ORAS hunting assistant | 80-85% | 85-88% | Stable working milestone. Viewer/OCR, route profiles, encounter logging, and reports are mostly working. |
| Full shiny hunting bot | 55-60% | 72-75% | Core detection/reporting is strong. Remaining work is mostly safe automation and long-run reliability. |
| Auto-catch shiny goal | 25-30% | 30-35% | Safety groundwork exists, but real catch automation is intentionally not active yet. |
| Safe real input / auto-run | 0-10% | 35-45% | Input authority is still locked. Current work is preflight, manual unlock, auto-focus, and guarded RUN automation. |
| Full hands-off hunting loop | Not active | 45-55% | Architecture and reports are in place, but the real loop needs safe input unlock and soak testing. |

## Current roadmap percentages

| Area | Progress | Status |
|---|---:|---|
| Clean portable build layout | 100% | Done |
| Single top-level ZIP folder layout | 100% | Done |
| Viewer/OCR stability | 85% | Mostly stable |
| Route/profile detection | 80-85% | Strong progress |
| ORAS route/profile coverage | 80-85% | Built-in profiles working; more coverage and validation still useful |
| Encounter logging and reports | 90% | Stable |
| Live stats and species counts | 85-90% | Working, with ongoing UI polish |
| Shiny candidate detection/evidence saving | 85-90% | Safety hold path exists |
| UI polish/status panels | 75-80% | Improved, still needs clean start/stop and focus controls |
| Safety/preflight system | 80% | Strong report-only safety; manual unlock path still staged |
| Auto-focus UI helper | 40-50% | Next active step |
| Manual unlock token workflow | 55-65% | Preflight/report-ready, real input still blocked by design |
| Input redirection layer | 35-45% | Planned/present as report-only safety layer |
| Auto-run from battle | 35-45% | Planned next major milestone, not active by default |
| Full encounter loop automation | 45-55% | Needs safe RUN automation first |
| Long soak reliability | 50-60% | Needs short test batches first, then longer validation |
| Auto-catch shiny | 25-35% | Future stage only after RUN/input safety is proven |

## Confirmed completed milestones

- Portable-only build structure.
- Clean root folder and organized reports, recordings, and logs.
- Report-only mode.
- Input locked by default.
- No RUN, touch, button, or catch authority in the stable branch.
- Fast route search, route catalog caching, and route search debounce.
- Fast UI encounter updates.
- Top banner updates quickly.
- Live stats: seen counter, last seen, and species counts.
- Shiny count de-duplication.
- Same-battle duplicate Start guard.
- Koffing OCR fallback.
- Route 101 full profile fix.
- Fiery Path profile selection.
- Meteor Falls profile selection.
- Route 119 Surf/Fishing profile selection.
- Water route species counting.
- All-shiny patch test controls and safety mode.
- Shiny HOLD_NO_RUN safety path.
- Evidence/freeze saving for shiny candidates.
- Storage helper BAT files and old LocalAppData cleanup helper.
- Current report/build label fix.
- Code/speed audit cleanup.

## Route/profile work completed

| Area | Status |
|---|---|
| Route 101 | Bot-tested, stable |
| Fiery Path | UI/profile tested, OCR species counting working |
| Meteor Falls | UI/profile no-leak tested |
| Route 119 Surf/Fishing + Feebas Group | Tested, Tentacool counting confirmed |
| Main ORAS land routes | Added as source-backed profiles |
| Cave/interior profiles | Added as source-backed profiles |
| Surf/water/fishing groups | Added as grouped profiles |
| Trust labels split into data/runtime/input status | Done |

## Current safety status

The bot is still intentionally locked:

```text
Mode: REPORT ONLY
Input: LOCKED
RUN automation: DISABLED
Touch input: DISABLED
Button input: DISABLED
Catch automation: DISABLED
RAM/NTR branch: DISABLED
```

Real input must remain blocked until the manual unlock, preflight, focus validation, and RUN decision guard are all passing.

## Next build direction

### RE-33 safety/input preflight track

1. Add automatic UI focus helper.
2. Keep real input locked by default.
3. Add clear start/stop controls without changing the 3DS viewer dimensions.
4. Improve manual unlock token preflight reports.
5. Add guarded auto-run decision reporting.
6. Only enable real RUN input after all safety checks pass:
   - correct window focus,
   - correct battle state,
   - correct target/non-target decision,
   - manual unlock token present,
   - no shiny candidate detected,
   - no unknown or OCR-unsafe state.

## What should be tested next

Use small 3-5 encounter batches.

1. Confirm the app opens and focuses cleanly.
2. Confirm the 3DS viewer/gameplay dimensions are unchanged.
3. Confirm reports still generate in the correct folders.
4. Confirm route/profile selection still works.
5. Confirm encounter species counts still save correctly.
6. Confirm safety reports still say real input is blocked by default.
7. Confirm no RUN, touch, or button input is sent unless the future manual unlock path explicitly allows it.

## Progress summary

Current best estimate:

```text
GitHub stable baseline: 58-60% complete
Current active project estimate: 72-75% complete
After auto-focus + safer start/stop + preflight polish: 76-78%
After safe auto-run from battle works: 82-86%
After full encounter loop and reliability testing: 90%+
```

The largest remaining milestone is safe real input control. Once guarded auto-run from battle works reliably, the project will move from a report-only assistant toward a true hands-off shiny hunting loop.
