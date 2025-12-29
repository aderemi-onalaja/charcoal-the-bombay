# 🎮 Charcoal the Bombay — Development Roadmap

## Project Vision
**Charcoal the Bombay** is a 2D side-scrolling platformer about a curious cat exploring increasingly larger worlds — from the safety of home to the unpredictability of nature.  
The game prioritises **feel, exploration, and charm** over complex mechanics.

The core philosophy:
> Simple mechanics, rich spaces, strong atmosphere.

---

## Phase 1 — Core Foundation ✅ (Completed / Stable)

**Goal:** Build a solid, extensible platformer engine.

- [x] Player movement using world-space physics
- [x] Stable AABB collision (axis-separated)
- [x] Solid platforms (no pass-through)
- [x] Enemies (mouse, bird)
- [x] Collectibles + score system
- [x] Camera system (render-only, no physics coupling)
- [x] Debug mode toggle
- [x] Game Over → tap/click anywhere to restart
- [x] Keyboard + touch controls

---

## Phase 2 — Level System & Progression

**Goal:** Transition from demo to structured game.

- [ ] Level loader / progression flow
- [ ] Level metadata (name, width, theme)
- [ ] Level Complete → load next level
- [ ] Level title overlay on level entry
- [ ] Reset logic per level (player, enemies, collectibles)

---

## Phase 3 — The World (Main Game Content)

### 🏠 House (Levels 1–2)
**Theme:** Safe, cosy, onboarding

Purpose:
- Introduce controls
- Establish tone
- Zero pressure

Design notes:
- Short levels (2–3 screens)
- Flat ground, gentle steps
- No enemies initially

Examples:
- Bedroom → living room
- Hallway → front door / window exit

---

### 🌿 Garden (Levels 3–5)
**Theme:** First danger, playful outdoors

Purpose:
- Introduce enemies
- Teach spacing and timing

Design notes:
- Grass + dirt platforms
- Small gaps and low floating platforms
- Optional higher routes with extra collectibles

Examples:
- Flower beds
- Garden furniture / logs
- Fence or shed exit

---

### 🐱 Neighbourhood (Levels 6–9)
**Theme:** Social exploration

Purpose:
- World feels alive
- Introduce friendly NPC cats

Design notes:
- Longer horizontal levels
- Rooftops, fences, bins, parked cars
- Friendly cat NPCs (no damage, idle animations)

Examples:
- Back alley
- Rooftop run
- Quiet residential street

---

### 🏙️ City (Levels 10–14)
**Theme:** Vertical challenge

Purpose:
- Increase difficulty through height and spacing
- Emphasise camera and parallax

Design notes:
- Tall buildings and stacked platforms
- Birds as primary threat
- Precision jumps, but fair layouts

Examples:
- Fire escapes
- Construction site
- Neon night street

---

### 🌲 Nature (Levels 15–20)
**Theme:** Calm, wild, exploratory

Purpose:
- Contrast the city
- Reward exploration

Design notes:
- Fewer enemies
- More hidden paths
- Scenic pacing

Sub-themes:
- Forest
- River crossings
- Park / jungle-like environments

---

## Phase 4 — Polish & Cohesion

**Goal:** Make the game feel finished and intentional.

- [ ] Consistent difficulty curve across levels
- [ ] Visual cohesion between themes
- [ ] Camera + parallax tuning per environment
- [ ] Sound hooks / effects
- [ ] Performance optimisation
- [ ] Mobile UX polish

---

## Phase 5 — Optional Extensions (Post-v1)

Ideas to explore after the core game ships:

- Save system
- Cat friendship / bonding system
- Collectibles with meaning
- Light narrative moments
- Environmental variants (night, rain, snow)

---

## 🎯 Level Count Philosophy

**Recommended total:** **18–22 levels**  
**Target:** **20 levels**

Breakdown:

| Theme          | Levels |
|---------------|--------|
| House         | 2 |
| Garden        | 3 |
| Neighbourhood | 4 |
| City          | 5 |
| Nature        | 6 |
| **Total**     | **20** |

Why this works:
- Less than 10 feels like a demo
- 10–15 feels rushed
- **20 lets themes breathe**
- Avoids solo-dev scope creep

---

## Core Design Rule
> **New levels remix space, not mechanics.**

- Jump stays jump
- Enemies remain readable
- Difficulty comes from layout, timing, and choice of path

---

## Shipping Mindset
- Build for **v1**
- Lock scope early
- Add depth through environments, not systems

---

**Charcoal the Bombay** is about a cat exploring the world —  
the roadmap ensures the world feels worth exploring.
