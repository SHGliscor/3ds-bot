Current Status: 62% complete — stable GUI/input base, shiny detection training in progress, full automation still safety-gated.

inspiration taken from 

pokebot-gen3
pokebot-nds
pokemonautomation 

links to be added

# 3DS Shiny Hunting Bot Progress Breakdown

Current project branch/base: RE-New series  
Current estimated completion: **62%**

## Progress by Area

| Area | Status | Progress |
|---|---:|---:|
| Clean new project base | Passed | 100% |
| Modular app structure | Passed | 100% |
| GUI launch and layout | Passed | 95% |
| Fixed 3DS viewer frame | Passed | 100% |
| Locked gameplay ROI/crop | Passed | 100% |
| n3DS View launch/docking | Passed | 95% |
| InputRedirection connection/manual buttons | Passed | 90% |
| Supervised button sequences | Passed | 90% |
| Safe run-from-battle sequence | Passed | 85% |
| Recording/clip scout workflow | Working | 80% |
| Non-shiny/shiny comparison workflow | Working | 75% |
| Shiny detection logic | In progress | 55% |
| False-positive protection | In progress | 45% |
| Day/night robustness | In progress | 40% |
| Route/background coverage | Planned/In progress | 35% |
| Encounter species detection | In progress | 45% |
| Route profiles | In progress | 45% |
| Hunt method support | Planned | 25% |
| Full auto encounter loop | Not unlocked yet | 20% |
| Full unattended automation | Safety-gated | 10% |
| Packaging/build polish | Working | 75% |
| GitHub documentation/readme | Needs update | 35% |

## Overall Estimate

**Current bot completion: ~62%**

The project is past the basic prototype stage. The app launches, the viewer is stable, the crop geometry is locked, manual InputRedirection works, supervised sequences work, and the shiny comparison workflow is now being trained/tested.

The main remaining work is:

1. Finish reliable shiny detection.
2. Reduce false positives.
3. Add day/night, cave, grass, water/surfing, and route background handling.
4. Expand route/profile data.
5. Add more shiny hunting methods.
6. Move from supervised actions into safe automation.
7. Only then unlock full unattended hunting.

## Important Safety Note

Full automation is **not unlocked yet**.  
The bot should stay supervised until shiny detection and false-positive protection are much more reliable.

## Current Testing Focus

The next tests should focus on:

- Day non-shiny Poochyena
- Night non-shiny Poochyena
- Day shiny Poochyena
- Night shiny Poochyena
- Later: cave, surfing, water, and different route backgrounds

## Project Direction

The current best path is:

1. Lock shiny detection first.
2. Add greyscale/sparkle/frame-difference checks.
3. Add profile-aware background handling.
4. Add safe auto-run.
5. Add full encounter loop.
6. Add shiny stop/alert.
7. Add more hunt methods.
