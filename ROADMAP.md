# Bob's Game Online - Architectural Roadmap

## Phase 1: Ecosystem Governance & Standards Unification (Current)
- [x] Establish single global version tracking in `VERSION.md`.
- [x] Standardize governance and documentation suite (`VISION.md`, `ROADMAP.md`, `TODO.md`, `MEMORY.md`, `DEPLOY.md`, `IDEAS.md`, `CHANGELOG.md`, `HANDOFF.md`).
- [x] Define single-page consolidated operator dashboard specifications.
- [x] Create automated documentation and ecosystem validation tooling.

## Phase 2: Web & Java Engine Protocol Harmonization
- [ ] Align packet serialization schemas between `bobsgameonlinejava` server and `bobsgameweb` client.
- [ ] Map binary protocol messages to typed TypeScript interfaces and Java records/DTOs.
- [ ] Build end-to-end integration test harness simulating headless player connections and chat broadcasts.

## Phase 3: Unified Operator Dashboard Redesign
- [ ] Consolidate fragmented web admin subpages into a single high-density dashboard.
- [ ] Implement hierarchical sectioning prioritized by operational value:
  1. Primary Server Lifecycle & Status (Status banner, Start/Stop/Restart, CCU gauge).
  2. Live Telemetry & Health (Memory usage, TPS/FPS, bandwidth, active WebSocket sessions).
  3. Player Management & Moderation (Live search, session kick, mute, message dispatch).
  4. World & Entity State Inspector (Loaded maps, entity counts, trigger zones).
  5. Configuration & System Settings (Ports, tick rate, auth tokens, debug flags).
- [ ] Add comprehensive tooltip markers and explanatory guidance for all dashboard controls.
- [ ] Wire desktop / system tray controls for local server daemon monitoring and graceful quit.

## Phase 4: Asset Pipeline & Monorepo Submodule Integration
- [ ] Link `bobsgameonlinejava`, `bobsgameweb`, and `okgame` under the `bg` umbrella workspace via git submodules or package workspaces.
- [ ] Standardize tile, sprite, and sound effect pipelines into cross-engine asset formats.
- [ ] Automate continuous deployment pipelines for web builds and server container images.
