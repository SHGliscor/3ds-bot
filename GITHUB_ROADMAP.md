# Real 3DS Shiny Hunter Roadmap

This roadmap is organized for GitHub Projects, milestones, or issues. Each checkbox can be copied into a GitHub issue body, project task list, or milestone description.

## Milestone 1: Starter Mode v1

**Goal:** Finish and lock down ORAS starter shiny hunting for Treecko, Torchic, Mudkip, and Random starter selection.

**Status:** Nearly complete.

### Completed

- [x] Add starter selection for Treecko, Torchic, Mudkip
- [x] Add Random starter selection
- [x] Use Torchic sequence as the base starter sequence
- [x] Treecko starter selection uses LEFT
- [x] Mudkip starter selection uses RIGHT
- [x] Add robust starter-selection directional input
- [x] Add Robust Sparkle detector
- [x] Add safe starter battle crop guard
- [x] Add stable color confirmation for Torchic
- [x] Add stable color confirmation for Treecko
- [x] Add stable color confirmation for Mudkip
- [x] Add single-hit recovery for Treecko
- [x] Add single-hit recovery for Mudkip
- [x] Validate Torchic day detection
- [x] Validate Torchic night detection
- [x] Validate Treecko day detection
- [x] Validate Treecko night detection
- [x] Validate Mudkip day detection
- [x] Validate Mudkip night detection
- [x] Add Auto / Day / Night lighting profile
- [x] Add starter hunt stats
- [x] Add pause / resume support
- [x] Freeze elapsed time while paused or stopped
- [x] Freeze average attempt time while paused or stopped
- [x] Add Discord webhook ping support
- [x] Move Activity Log to separate window
- [x] Keep video output fixed size while app window is resizable
- [x] Set default bot layout to 1280x800

### Remaining validation

- [ ] Run one final Torchic non-shiny regression test with Auto Day/Night enabled
- [ ] Run one final Treecko non-shiny regression test with Auto Day/Night enabled
- [ ] Run one final Mudkip non-shiny regression test with Auto Day/Night enabled
- [ ] Confirm logs show correct Auto Day/Night profile selection
- [ ] Confirm Discord ping triggers only on safety hold
- [ ] Confirm pause/resume does not inflate elapsed time or average attempt time

### Acceptance criteria

- [ ] Treecko, Torchic, Mudkip, and Random can run without manual intervention
- [ ] Known shiny starters safety-hold
- [ ] Known non-shiny starters reset/continue
- [ ] Day and night lighting both work
- [ ] No false hold from normal send-out animation
- [ ] No reset-over on known shiny samples

---

## Milestone 2: Windows EXE Packaging

**Goal:** Build and test a shareable Windows executable.

### Tasks

- [ ] Build PyInstaller one-file EXE
- [ ] Confirm app launches on Windows without source files
- [ ] Confirm n3DS_view launches or embeds correctly
- [ ] Confirm assets load correctly in EXE mode
- [ ] Confirm settings save to writable user folder
- [ ] Confirm recordings save to writable user folder
- [ ] Confirm hunt logs save correctly
- [ ] Confirm stats files save correctly
- [ ] Confirm Discord webhook works from EXE
- [ ] Confirm Activity Log window works from EXE
- [ ] Confirm 1280x800 layout on target desktop
- [ ] Confirm fixed video output remains stable after resizing app

### Acceptance criteria

- [ ] A user can run the bot from `3DS Shiny Hunter.exe`
- [ ] No Python installation required for end user
- [ ] No source code folder required for normal use
- [ ] No missing-file errors on clean test machine

---

## Milestone 3: Random Encounter Mode v1

**Goal:** Add support for grass, cave, and surf random encounter shiny hunting.

### Core loop

- [ ] Add Hunt Mode selector
- [ ] Add Random Encounter mode option
- [ ] Add movement loop engine
- [ ] Add movement pattern presets
- [ ] Add custom movement timing settings
- [ ] Detect encounter or battle start
- [ ] Wait for Pokémon to appear
- [ ] Run shiny detection
- [ ] Safety-hold on shiny
- [ ] Run away or reset on non-shiny
- [ ] Increment encounter counter when battle starts

### Movement pattern presets

- [ ] LEFT / RIGHT
- [ ] UP / DOWN
- [ ] Circle
- [ ] Custom sequence

### Settings

- [ ] Movement hold time
- [ ] Movement release gap
- [ ] Encounter timeout
- [ ] Battle intro wait
- [ ] Run-away sequence
- [ ] Post-run wait
- [ ] Reset instead of run option

### Acceptance criteria

- [ ] Bot can walk until encounter starts
- [ ] Bot can check shiny state
- [ ] Bot can safely hold on possible shiny
- [ ] Bot can flee/reset on non-shiny
- [ ] Encounter count and seen/hour update correctly

---

## Milestone 4: Static and Gift Hunt Mode

**Goal:** Support non-starter soft reset hunts and gift Pokémon.

### Target examples

- [ ] Castform
- [ ] Beldum
- [ ] Fossils
- [ ] Wynaut egg
- [ ] Togepi egg
- [ ] Kecleon
- [ ] Voltorb / Electrode
- [ ] Spiritomb
- [ ] Latios / Latias
- [ ] Mirage Spot legendaries

### Core features

- [ ] Add Static / Gift hunt mode
- [ ] Add custom button sequence editor
- [ ] Add sequence presets
- [ ] Add pre-check delay per profile
- [ ] Add static encounter crop presets
- [ ] Add gift screen handling
- [ ] Add battle encounter handling

### Acceptance criteria

- [ ] User can define a repeatable button sequence
- [ ] Bot can reset and repeat sequence
- [ ] Bot can shiny-check after sequence completes
- [ ] Bot can safety-hold on shiny

---

## Milestone 5: Horde Encounter Mode

**Goal:** Automate Sweet Scent / Honey horde hunting.

### Core loop

- [ ] Use Sweet Scent or Honey
- [ ] Wait for horde battle
- [ ] Detect five Pokémon areas
- [ ] Run shiny detection across multiple crop zones
- [ ] Safety-hold on shiny
- [ ] Run away or reset on non-shiny
- [ ] Track Sweet Scent PP or usage count

### Settings

- [ ] Sweet Scent sequence
- [ ] Horde battle intro wait
- [ ] Horde crop presets
- [ ] Run-away sequence
- [ ] PP warning threshold

### Acceptance criteria

- [ ] Bot can trigger hordes repeatedly
- [ ] Bot can check multiple Pokémon locations
- [ ] Bot can stop safely on possible shiny

---

## Milestone 6: Chain Fishing Mode

**Goal:** Automate ORAS chain fishing hunts.

### Core loop

- [ ] Cast rod
- [ ] Detect bite prompt
- [ ] Press A on bite
- [ ] Detect encounter start
- [ ] Run shiny detection
- [ ] Run away on non-shiny
- [ ] Preserve chain when possible

### Stats

- [ ] Chain length
- [ ] Encounters
- [ ] Seen/hour
- [ ] Missed bites
- [ ] Longest chain

### Acceptance criteria

- [ ] Bot can fish repeatedly without moving
- [ ] Bot can react to bite timing
- [ ] Bot can track chain length
- [ ] Bot can safety-hold on shiny

---

## Milestone 7: Profile Manager

**Goal:** Make hunt setup easy and repeatable.

### Profiles to support

- [ ] ORAS Starters
- [ ] ORAS Random Encounter
- [ ] ORAS Static / Gift
- [ ] ORAS Horde
- [ ] ORAS Chain Fishing
- [ ] Custom profile

### Profile fields

- [ ] Hunt mode
- [ ] Target Pokémon
- [ ] Crop settings
- [ ] Detector settings
- [ ] Lighting profile
- [ ] Button timing settings
- [ ] Discord settings
- [ ] Recording settings
- [ ] Stats settings

### UI

- [ ] Save Profile
- [ ] Load Profile
- [ ] Export Profile
- [ ] Import Profile
- [ ] Reset to Recommended

### Acceptance criteria

- [ ] User can save and reload complete hunt setup
- [ ] Profiles can be shared between users
- [ ] Recommended profiles reduce manual setup

---

## Milestone 8: Reliability and Safety

**Goal:** Improve unattended long-run reliability.

### Safety features

- [ ] Viewer freeze detection
- [ ] No-frame timeout
- [ ] Connection lost detection
- [ ] Stuck-on-screen detection
- [ ] Long no-encounter warning
- [ ] Disk space warning
- [ ] Recording failure warning
- [ ] Discord failure warning
- [ ] Auto screenshot on safety hold
- [ ] Save short clip around safety hold

### Notifications

- [ ] Ping on possible shiny
- [ ] Ping on viewer freeze
- [ ] Ping on connection lost
- [ ] Ping after X attempts
- [ ] Ping after X hours

### Acceptance criteria

- [ ] Bot fails safely instead of silently continuing
- [ ] Important errors are visible in UI and Discord
- [ ] Safety holds include enough data to review the event

---

## Milestone 9: DexNav Experimental Mode

**Goal:** Explore automation for ORAS DexNav hunts.

### Core tasks

- [ ] Use DexNav search
- [ ] Detect search success or failure
- [ ] Sneak toward hidden Pokémon
- [ ] Start encounter
- [ ] Run shiny detection
- [ ] Recover from failed searches
- [ ] Track chain state if possible

### Known challenges

- [ ] Sneaking movement precision
- [ ] Target movement
- [ ] Grass positioning
- [ ] Failed search recovery
- [ ] Repel management
- [ ] Chain preservation

### Acceptance criteria

- [ ] Experimental DexNav loop works in a controlled test area
- [ ] Bot can recover from common DexNav failure states

---

## Milestone 10: Release Polish

**Goal:** Prepare a user-friendly public/shareable release.

### UI cleanup

- [ ] Simplify labels
- [ ] Hide advanced settings by default
- [ ] Add first-run setup wizard
- [ ] Add help buttons/tooltips
- [ ] Add recommended setup buttons per mode
- [ ] Clean up startup log noise

### Documentation

- [ ] README
- [ ] Quick Start Guide
- [ ] Troubleshooting Guide
- [ ] EXE build instructions
- [ ] Discord webhook setup guide
- [ ] Example profiles

### Testing

- [ ] Clean Windows test
- [ ] 1280x800 desktop test
- [ ] Fullscreen test
- [ ] Dark/light mode test
- [ ] EXE launch test
- [ ] Long-run starter test

### Acceptance criteria

- [ ] New user can launch and run a starter hunt from the README
- [ ] App has no obvious debug clutter
- [ ] EXE release package is ready to share

---

## Recommended Priority Order

1. Starter Mode final regression test
2. Build and test Windows EXE
3. Random Encounter Mode v1
4. Static / Gift Hunt Mode
5. Profile Manager
6. Reliability and Safety
7. Horde Mode
8. Chain Fishing Mode
9. DexNav Experimental Mode
10. Release Polish

