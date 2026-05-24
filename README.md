# 3ds Bot Progress Update

**Current estimated completion: 67%**

## Summary

The 3ds bot is now past the basic working-app stage. The main GUI, fixed 3DS viewer, locked ROI crop, n3DS View docking, InputRedirection controls, supervised battle-run flow, compact exports, and Auto Test Window workflow are mostly in place.

The current focus is improving Auto Test Window reliability across multiple encounters, strengthening shiny detection, reducing false positives, and preparing for safer automation.

---

## Progress Breakdown

| Area | Progress | Status |
|---|---:|---|
| Clean 3dd base | 100% | Passed |
| Modular app structure | 100% | Passed |
| GUI launch | 95% | Passed |
| Fixed 840×600 3DS viewer | 100% | Passed |
| Locked ROI crop geometry | 100% | Passed |
| n3DS View launch/docking | 95% | Passed |
| InputRedirection manual controls | 95% | Passed |
| Supervised button sequences | 90% | Passed |
| Run-from-battle sequence | 90% | Passed |
| Auto Test Window capture | 85% | Working |
| Auto Test Window re-arm | 70% | Improving |
| Second black-screen outro protection | 75% | Being tuned |
| Overworld reset detection | 65% | Improving |
| GUI responsiveness | 85% | Improved |
| Compact test export | 85% | Working |
| Shiny/non-shiny test workflow | 85% | Working |
| Shiny detection foundation | 65% | In progress |
| False-positive protection | 60% | In progress |
| Day/night shiny robustness | 55% | In progress |
| Species/background handling | 45% | In progress |
| Route/background profiles | 45% | In progress |
| Cave/surfing/water profiles | 20% | Planned |
| Full auto encounter loop | 35% | Not unlocked |
| Full unattended automation | 10% | Safety-gated |

---

## Current Status

**Overall progress: 67% complete**

The project has a stable base and is moving into reliability tuning. The most important blocker is not the GUI or input system anymore. The key blocker is making detection and re-arm behavior reliable enough to support safe automation.

---

## Current Priorities

1. Make Auto Test Window reliably continue across multiple encounters.
2. Finish shiny detection confidence scoring.
3. Reduce false positives.
4. Make detection stable across day/night lighting.
5. Add route, cave, surfing, and water background support.
6. Expand species and route-profile handling.
7. Unlock fuller automation only after safety checks pass.

---

## GitHub Status Line

**status: 67% complete — stable GUI/input base, supervised battle-run working, Auto Test Window improving, shiny detection and false-positive protection still in progress.**
