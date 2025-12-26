## Level 1 tile map (explicit)

### Level name
- **ID:** `l01_garden_path`
- **Theme:** Urban garden / park edge
- **Goal:** Teach movement + jumping + first enemy + first collectible
- **Length:** ~60–75 seconds for a first-time player

### Tile grid assumptions
- Tile size: **16×16 px**
- Viewport: **20 tiles wide × 12 tiles high** (typical mobile-friendly framing)
- Level width: **240 tiles** (split into 6 “screens” of 40 tiles each)

Legend:
- `#` = solid ground/platform
- `.` = empty
- `C` = Charcoal spawn
- `E` = exit/finish flag
- `m` = mouse enemy
- `b` = bird enemy (fly path marker)
- `t` = cat treat collectible
- `s` = scratch pad checkpoint
- `^` = spike/hazard (optional; keep minimal in Level 1)

### Screen-by-screen layout (6 segments)

#### Segment A (tiles x: 0–39) — Tutorial flat
- Teach: move, jump, collect
- Spawn at x=2, y=8

Placements:
- `C` at (2,8)
- Treats `t` at (8,8), (12,8), (16,8)
- Flat ground from x=0..39 at y=10

Notes:
- No enemies yet.

#### Segment B (x: 40–79) — First gap + small platforms
- Teach: timing jumps, safe recovery

Platforms:
- Ground y=10 except:
  - Gap from x=54..57 (4-tile gap)
- Floating platforms:
  - Platform 1: x=46..50 at y=8
  - Platform 2: x=60..64 at y=7
- Treats:
  - `t` on Platform 1 at (48,7)
  - `t` on Platform 2 at (62,6)

Enemy:
- Mouse `m` at (70,9) patrol 6 tiles (x=68..74)

#### Segment C (x: 80–119) — Checkpoint + gentle verticality
- Introduce: checkpoint + reward route

Checkpoint:
- Scratch pad `s` at (84,9)

Platforms:
- Ground y=10
- Step-up ledges:
  - x=92..98 at y=9
  - x=100..106 at y=8
  - x=108..114 at y=7

Collectibles:
- Treat trail: (92,8), (100,7), (108,6), (114,6)

Enemy:
- Bird `b` flight path across x=96..112 at y=5 (slow)

#### Segment D (x: 120–159) — First “choice” path (low vs high)
- Low path: safer, fewer treats
- High path: more treats, one extra enemy

Low path:
- Ground continues y=10
- One mouse at (138,9), patrol x=136..144

High path access:
- Jump-up platform chain:
  - x=124..128 at y=8
  - x=132..136 at y=7
  - x=140..144 at y=6

High path:
- Treats at (126,7), (134,6), (142,5)
- Bird flight path x=132..148 at y=4 (medium)

#### Segment E (x: 160–199) — Short “skill check”
- A couple of gaps + enemy positioning, still forgiving

Ground:
- Gap x=170..172 (3 tiles)
- Gap x=186..189 (4 tiles)

Platforms:
- x=166..169 at y=8
- x=176..179 at y=7
- x=182..185 at y=8

Enemies:
- Mouse at (178,6) on platform, patrol x=176..179
- Optional spikes `^` under second gap at y=11 (visual hazard only in v1 if you want it simple)

Treats:
- (166,7), (176,6), (184,7), (192,8)

#### Segment F (x: 200–239) — Finish + “victory runway”
- Give player momentum and a clean end

Checkpoint (optional):
- `s` at (204,9)

End:
- `E` at (236,9)

Enemies:
- None (keep it satisfying)

Collectibles:
- Treat arc leading to exit:
  - (210,8), (214,7), (218,6), (222,6), (226,7), (230,8)

### Level 1 success criteria
- First-time player reaches exit within **3 attempts**
- Controls feel responsive
- No unfair enemy placement at landing zones
- Clear visual language: ground vs platform vs hazard

---

## Charcoal sprite sheet spec

### Style + constraints
- Pixel art inspired by GBA, readable on mobile
- Keep sprite sheets small to maintain performance
- Use consistent pivot/anchor point at Charcoal’s feet (important for collision)

### Base sprite dimensions
- **Frame size:** 32×32 px (recommended)
- **Hitbox:** 18×20 px (tweak in code, not art)
- **Export format:** PNG with transparency

### Sheets to create (v1)
1) `charcoal_idle.png`
2) `charcoal_run.png`
3) `charcoal_jump.png`
4) `charcoal_fall.png`
5) `charcoal_land.png`
6) `charcoal_hurt.png`
7) `charcoal_attack.png` (optional, only if you add swipe/boop mechanic)

### Animation breakdown
**Idle**
- Frames: 6
- FPS: 8
- Notes: subtle tail flick, blink

**Run**
- Frames: 8
- FPS: 12
- Notes: smooth loop, slight head bob

**Jump (takeoff)**
- Frames: 3
- FPS: 12
- Notes: crouch → push → airborne

**Fall**
- Frames: 2
- FPS: 8
- Notes: ears slightly back, legs tucked

**Land**
- Frames: 2
- FPS: 12
- Notes: squash on impact, quick recovery

**Hurt**
- Frames: 4
- FPS: 10
- Notes: brief flash + recoil pose

### Optional v1 “power-up” variant
If treats change appearance:
- Add overlay glow in code OR
- Provide palette-swap version:
  - `charcoal_run_power.png` (same frame count)

### Export rules
- Transparent background
- No extra padding (stick to 32×32)
- Consistent baseline: feet always align to the same y within the frame grid

---

## App Store–ready v1 scope

### Goal
A polished, small iOS platformer that’s fun in 1–2 minutes, stable, and presentable.

### Must-have (v1)
**Gameplay**
- 1 complete level (`l01_garden_path`)
- Solid movement + jump + double-jump
- 2 enemy types (mouse, bird)
- 2 collectibles (treat, scratch pad checkpoint)
- Simple health system (e.g., 2 hits → restart at checkpoint)

**UX**
- Main menu:
  - Play
  - Settings (sound, haptics)
  - Credits
- Pause menu + restart
- Clear “Level Complete” screen

**Mobile**
- Touch controls with large tap targets
- Left-handed / right-handed toggle (optional but nice)
- 60 FPS target on modern iPhones

**Stability**
- No crashes on resume / lock screen
- Predictable physics (no random tunnelling through platforms)
- Consistent collisions across devices

### Nice-to-have (if time)
- Simple cosmetic unlock (colour collar, tiny charm)
- Level timer + best time
- “Treats collected” counter

### Not in v1 (avoid scope creep)
- Multiple worlds/levels
- Boss fights
- Online leaderboards
- Complex story mode
- Heavy particle systems or huge texture packs

### App Store checklist (practical)
- App icon + launch screen
- Privacy basics:
  - No tracking SDKs in v1 (easier)
  - Minimal data collection (ideally none)
- Age rating-friendly content
- Screenshots:
  - Menu
  - Level gameplay
  - Treat power-up moment
  - Level complete

---

## Next steps (execution order)
1. Build Level 1 using the placements above (placeholder tiles OK)
2. Implement Charcoal animations using the sprite spec
3. Add menu + pause + settings
4. Performance pass (frame rate + memory)
5. Export App Store assets (icon, screenshots, short description)
