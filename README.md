# 3ds Bot Project — Completed So Far

Current stable base: **RE-32c**

## Overall status

| Area | Completion | Status |
|---|---:|---|
| Report-only ORAS hunting assistant | 80–85% | Stable working milestone |
| Full bot goal | 55–60% | Good progress, automation not started |
| Auto-catch shiny goal | 25–30% | Safety groundwork done, catch automation not started |

## Confirmed working

| Feature | Status |
|---|---|
| Clean portable-only build layout | Done |
| One top-level ZIP folder | Done |
| Clean root folder with only useful launch/control files | Done |
| No RAM/NTR active in current branch | Done |
| Report-only mode | Done |
| Input locked | Done |
| No RUN/touch/button/catch authority | Done |
| Faster route search | Done |
| Route catalog caching | Done |
| Route search debounce | Done |
| Fast UI encounter update | Done |
| Top banner updates quickly | Done |
| Live stats seen counter | Done |
| Live stats last seen | Done |
| Live stats species counts | Done |
| Shiny count de-duplication | Done |
| Same-battle duplicate Start guard | Done |
| Koffing OCR fallback | Done |
| Route 101 full profile fix | Done |
| Fiery Path profile selection | Done |
| Meteor Falls profile selection | Done |
| Route 119 Surf/Fishing profile selection | Done |
| Water route species counting | Done |
| All-shiny patch test controls in root | Done |
| All-shiny patch safety mode | Done |
| Shiny HOLD_NO_RUN safety path | Done |
| Evidence/freeze saving for shiny candidates | Done |
| Storage helper BAT files | Done |
| Old LocalAppData cleanup helper | Done |
| Current report label fix | Done |
| Code/speed audit cleanup | Done |

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

## Important fixes completed

| Build | Fix |
|---|---|
| RE-22b | Portable-only storage and Route 101 full-profile fix |
| RE-22c | ORAS water/surf/fishing profile groups |
| RE-22h | All-shiny patch raw detector reached 100% on Route 101 sample |
| RE-22j | Route/profile allowlist added to live stats OCR |
| RE-22l | Fast UI update before OCR completes |
| RE-22x | Koffing OCR fallback |
| RE-22w | Shiny count de-duplication |
| RE-22z | Same-battle duplicate Start guard fixed and confirmed |
| RE-32a | Stable report-only milestone |
| RE-32b | Report label fix |
| RE-32c | Code and speed audit cleanup |

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
