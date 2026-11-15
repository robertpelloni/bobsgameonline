# bob's game online

This repository is a **name placeholder** — it currently holds only this
README and no code.

## Status

**Parked / placeholder.** Created 2026-06-19; the only other commit is a
README rewrite on 2026-10-22. No code has ever been pushed here.

## Where the actual code lives

- The original "bob's game online" codebase — Java client and server, a 2D
  MMORPG engine and world — is in
  [bobsgameonlinejava](https://github.com/robertpelloni/bobsgameonlinejava).
- The modern engines are
  [bobsgameweb](https://github.com/robertpelloni/bobsgameweb)
  (TypeScript/PixiJS) and [okgame](https://github.com/robertpelloni/okgame)
  (C++), tied together in the [bg](https://github.com/robertpelloni/bg)
  umbrella workspace.

## About bob's game

bob's game is a 2D action RPG / puzzle game with a custom engine by Robert
Pelloni. Note: its Kickstarter campaign was a **failure** — it was not
funded. The game itself remains in development across the repos above.

## Links

- Author: https://robertpelloni.com
- Game site: https://bobsgame.com

Welcome to the **bob's game online** ecosystem portal and governance repository.

This repository serves as the definitive reference point, architecture coordination hub, and governance standard for Robert Pelloni's 2D retro MMORPG universe.

---

## 🧭 Repository Ecosystem Map

The "bob's game online" codebase is distributed across specialized repositories:

- 🎮 **[`bobsgameweb`](https://github.com/robertpelloni/bobsgameweb)**: The modern web client powered by TypeScript, PixiJS, WebGL, and WebSockets for instant in-browser play.
- ☕ **[`bobsgameonlinejava`](https://github.com/robertpelloni/bobsgameonlinejava)**: The original Java client and authoritative game server daemon, custom packet protocols, and LWJGL/OpenGL graphics engine.
- ⚡ **[`okgame`](https://github.com/robertpelloni/okgame)**: High-performance native C++ engine core.
- 📦 **[`bg`](https://github.com/robertpelloni/bg)**: The umbrella monorepo workspace tying engines, tools, and asset pipelines together.

---

## 📚 Ecosystem Documentation & Governance

- **[`VISION.md`](./VISION.md)**: Foundational vision, MMORPG universe concepts, and consolidated single-page dashboard architecture.
- **[`ROADMAP.md`](./ROADMAP.md)**: Multi-phase milestones from protocol synchronization to asset pipeline unification.
- **[`TODO.md`](./TODO.md)**: Granular task list, bug fixes, and immediate feature items.
- **[`MEMORY.md`](./MEMORY.md)**: Architectural patterns, repository traits, and design preferences.
- **[`DEPLOY.md`](./DEPLOY.md)**: Detailed deployment guides for web clients, Java servers, and Docker Compose environments.
- **[`IDEAS.md`](./IDEAS.md)**: Aggressive proposals for WebAssembly migration, Tauri tray apps, and P2P sharding.
- **[`CHANGELOG.md`](./CHANGELOG.md)**: Historical tracking of changes against the global version.
- **[`HANDOFF.md`](./HANDOFF.md)**: Autopilot handoff and continuity documentation for successor engineering sessions.
- **[`VERSION.md`](./VERSION.md)**: Single source of truth for global versioning.

