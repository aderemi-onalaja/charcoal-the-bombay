# 🐈‍⬛ Charcoal the Bombay

**Charcoal the Bombay** is a 2D side-scrolling platformer inspired by classic handheld platformers, built as a fast-moving prototype using **Lovable** and intended to ship as a mobile app via **Capacitor** (iOS-first).

The project stars **Charcoal**, a Bombay cat, navigating colourful environments, avoiding enemies, and collecting treats in a cozy, nostalgic platforming experience.

---

## 🎮 Purpose of the Game

The game is designed to:
- Recreate the **tight, simple fun** of classic handheld platformers
- Deliver a **low-friction, joyful experience** optimised for mobile touch controls
- Explore how far **AI-assisted tooling** can go in rapidly scaffolding a playable game MVP

Gameplay focuses on:
- Side-scrolling platform mechanics (run, jump, double-jump)
- Enemies such as mice and birds
- Power-ups like cat treats and scratch pads
- Colourful, friendly environments (trees, playgrounds, indoor cat spaces)

The tone is intentionally **cozy, playful, and accessible**, rather than competitive or complex.

---

## 🧪 Purpose of This Repository

This repository exists as:
- A **working prototype** of a mobile game
- A **learning and experimentation space** for AI-assisted game development
- A reference for **structured, phase-based prompting** to build software with AI tools

It is not intended to be a finished commercial game (yet), but rather a:
- Playable MVP
- Foundation for future expansion
- Case study in modern, prompt-driven development workflows

---


- ## Build approach

This project is being developed **web-first** for fast iteration (UI + gameplay loop), then packaged as a native mobile app using **Capacitor**.

The goal is to keep a single codebase that can run:
- In the browser for rapid development
- On iOS as a native-wrapped app (Capacitor)

---

## Tools & technology

### Primary build tooling
- **Lovable** — used to scaffold and iterate on the gameplay prototype (UI, game loop, core mechanics).
- **Capacitor** — intended for packaging the web build into a native iOS app shell (App Store path).

### Language / framework
- **TypeScript** (primary)
- Web runtime (canvas / DOM / web-based rendering depending on implementation)

### AI / models used
This project is developed with AI assistance for planning, prompting, and implementation guidance.

- **GPT-5.2** — used for game architecture, level design specs, mechanics breakdown, and prompt-driven iteration.

- ## Note on tooling

Early experiments used hosted AI app builders for rapid scaffolding, but the project moved to a **Lovable + Capacitor** workflow for smoother iteration, better performance control, and a clearer path to an App Store-ready build.

---

## 🧩 Development Approach

The project follows a **phase-based build strategy**:
1. Minimal playable scaffold
2. Core gameplay mechanics
3. Level design and environment depth
4. Visual identity and animation
5. Optional audio and polish

This approach prioritises:
- Fast feedback loops
- Stability over scope
- Clean iteration without regeneration overhead

---

## 🚀 Status

## Status

- Current: **Playable prototype (web-first)**
- Next: **Capacitor wrap for iOS**
- Scope: **Single-level MVP**

---

## 📄 License

This project is currently for **experimental and educational purposes**.  
Licensing may be updated if the project moves toward commercial release.

---

🐈‍⬛ Built with curiosity, nostalgia, and modern AI tooling.
