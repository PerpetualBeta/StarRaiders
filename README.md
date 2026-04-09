# Star Raiders

A browser-based recreation of the classic Atari Star Raiders. Defend the galaxy from alien fleets across a 128-sector star map, managing energy, shields, and ship systems while hunting down enemy ships in full 3D combat.

## How to Play

Open `star-raiders.html` in any modern web browser. No installation, server, or dependencies required — everything runs in a single self-contained HTML file.

## Quick Start

1. Open the game — you'll see the title screen
2. Select a difficulty with **Up/Down arrows** and press **Enter**
3. Press **G** to open the Galactic Chart
4. Move the cursor to a sector with red dots (enemies) and press **H** to hyperwarp there
5. Use **arrow keys** to steer, **Space** to fire torpedoes
6. Destroy all enemies across the galaxy to advance to the next wave

## Controls

### Keyboard

| Key | Action |
|-----|--------|
| **Arrow Keys** | Steer (pitch and yaw) |
| **Space** | Fire photon torpedo |
| **+ / =** | Increase speed |
| **- / _** | Decrease speed |
| **S** | Toggle shields on/off |
| **C** | Toggle attack computer on/off |
| **F** | Front view |
| **A** | Aft (rear) view |
| **G** | Galactic Chart |
| **L** | Long Range Scan |
| **H** | Hyperwarp to selected sector (from Galactic Chart) |

### Gamepad

| Input | Action |
|-------|--------|
| **Left Stick / D-Pad** | Steer |
| **A** | Fire / Confirm |
| **B** | Toggle shields |
| **X** | Toggle computer |
| **Y** | Hyperwarp |
| **LB / RB** | Decrease / Increase speed |
| **Select** | Galactic Chart |
| **Start** | Cycle front/aft view |

## Views

### Front View (F)
Your primary combat view. Shows the starfield, enemy ships, torpedoes, and your targeting crosshair. The attack computer overlay highlights enemies when active.

### Aft View (A)
Rear-facing camera — useful for spotting enemies behind you.

### Galactic Chart (G)
A 16×8 grid showing the entire galaxy.
- **Red dots/numbers** — enemy groups (the number indicates how many)
- **Green diamond** — starbase (dock here for repairs and energy)
- **White cross** (blinking) — your position
- **Yellow box** (blinking) — your cursor

Move the cursor with arrow keys and press **H** to hyperwarp to that sector. Warp costs 100 energy per sector of distance.

### Long Range Scan (L)
Shows the 3×3 grid of sectors surrounding your current position. Useful for planning your next move without opening the full chart.

## Combat

### Torpedoes
- Cost **50 energy** per shot
- 0.3-second cooldown between shots
- Travel forward from your ship and despawn after 2 seconds

### Enemies

| Type | Hit Points | Speed | Points |
|------|-----------|-------|--------|
| Warrior | 1 | Fast | 40 |
| Cruiser | 2 | Medium | 80 |
| Basestar | 3 | Slow | 120 |
| Mothership | 3 | Slow | 1,000 |

The **Mothership** is a rare bonus enemy that appears during combat and flees after 8–14 seconds — destroy it quickly for 1,000 points.

## Ship Systems

Your ship has six systems that can be damaged in combat. System health is shown as coloured squares in the HUD:
- **Green** (≥70%) — nominal
- **Yellow** (<70%) — damaged
- **Red** (0%) — destroyed

| System | Effect When Damaged |
|--------|-------------------|
| **Engines** | Slower turning, reduced max speed, less accurate hyperwarps |
| **Shields** | Reduced damage protection |
| **Computer** | Reduced targeting accuracy |
| **L.R.Scan** | Long Range Scan shows static |
| **Radio** | No starbase attack alerts |
| **Photons** | Cannot fire torpedoes |

## Energy Management

- **Maximum**: 9,999 energy
- **Shields drain**: 10 energy/second when active
- **Movement drains**: 3 × speed per second
- **Torpedoes cost**: 50 energy each
- **Hyperwarp costs**: 100 energy × distance in sectors
- **Running out of energy ends the mission**

Toggle shields off (**S**) when not in combat to conserve energy.

## Starbases

Starbases (green diamonds on the Galactic Chart) are your lifeline.

**To dock:**
1. Warp to a sector containing a starbase
2. Clear all enemies in the sector
3. Reduce speed to 1 or below
4. Fly within docking range of the starbase

**Docking fully restores** your energy and repairs all damaged systems.

**Starbase defence:** If enemies are present in a starbase sector, a timer starts. If you don't destroy all enemies before the timer expires, the starbase is destroyed (300-point penalty).

## Scoring

| Action | Points |
|--------|--------|
| Destroy Warrior | 40 |
| Destroy Cruiser | 80 |
| Destroy Basestar | 120 |
| Destroy Mothership | 1,000 |

### End-of-Mission Penalties

| Penalty | Calculation |
|---------|-------------|
| Time | Stardates elapsed × 5 |
| Energy | Energy consumed ÷ 500 |
| Starbases lost | Starbases destroyed × 300 |

### Ranks

| Minimum Score | Rank |
|---------------|------|
| — | Garbage Scow Captain |
| 0 | Galactic Cook |
| 1,000 | Ensign |
| 3,000 | Lieutenant |
| 5,000 | Warrior |
| 8,000 | Commander |
| 12,000 | Star Commander |

## Difficulty Levels

| Level | Enemy Groups | Enemy Accuracy | Starbase Timer |
|-------|-------------|----------------|----------------|
| Novice | 8 | 30% | 60s |
| Pilot | 12 | 45% | 50s |
| Warrior | 20 | 60% | 40s |
| Commander | 28 | 75% | 30s |

## Waves

Destroying all enemies in the galaxy advances you to the next wave with more enemy groups and an extended time limit. The game continues indefinitely with increasing difficulty.

## High Scores

- Top 10 scores are saved in your browser's local storage
- Enter up to 12 characters for your name when you qualify
- Press **T** from the title screen to view the high score table

## Mission End Conditions

- **All enemies destroyed** — advance to next wave
- **Time expires** — mission ends, score calculated
- **Energy depleted** — mission failure
- **All systems destroyed** — ship lost, mission failure

## Sound

All sound effects are synthesised in real-time using the Web Audio API — no audio files are loaded.

## Browser Requirements

Any modern browser with HTML5 Canvas, Web Audio API, and Gamepad API support (Chrome, Firefox, Safari, Edge).

---

Star Raiders is provided by [Jorvik Software](https://jorviksoftware.cc/). If you find it useful, consider [buying me a coffee](https://jorviksoftware.cc/donate).
