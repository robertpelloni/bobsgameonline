# Bob's Game Online - Vision & Core Foundational Architecture

## 1. Executive Summary & Purpose

`bobsgameonline` is the umbrella brand and public entry point for **bob's game online**, the ambitious 2D MMORPG universe created by Robert Pelloni.

Historically, the project evolved across multiple engine iterations:
1. **Original Java Client & Server** (`bobsgameonlinejava`): Custom engine, map editor, server daemon, custom packet protocols, and LWJGL/OpenGL graphics.
2. **Modern Web Client** (`bobsgameweb`): TypeScript, PixiJS, WebGL, WebSockets, playable in modern web browsers with zero installation friction.
3. **C++ Native Core** (`okgame`): High-performance native engine core targeting multi-platform deployment.
4. **Umbrella Workspace** (`bg`): The unified monorepo linking web, native, asset pipelines, and shared protocol specifications.

This repository serves as the definitive reference point, architecture coordination hub, and governance repository documenting how these components interact and how players and developers interface with the ecosystem.

---

## 2. Core Foundational Concepts

### 2.1 The Living MMORPG World
- **Persistent Retro Aesthetic**: 16-bit / 32-bit pixel art style, hand-crafted maps representing cities, arcades, secret rooms, and surreal landscapes.
- **Microgames & Meta-Gaming**: An arcade system where players can engage in mini-games (e.g. Bob's Game puzzle action) while embedded inside the larger persistent world.
- **Dynamic Multiplayer Sync**: Real-time position, state, emotes, and chat synchronization across players and NPCs.

### 2.2 Unified Operator & Player Dashboard
To prevent fragmented tooling and disparate admin dashboards, the unified system vision specifies a **Singular Dashboard Experience**:
- **Consolidated Single-Page Architecture**: Rather than scattering features across disconnected subpages, all server management, world inspection, player diagnostics, network telemetry, and system tray integration converge into a unified, high-density, categorized single-page interface.
- **Prominent High-Value Controls**:
  - Global Server Controls (Start, Stop, Restart, Graceful Shutdown, Player Kick/Broadcast).
  - Live Server Telemetry (CCU, TPS, Memory, Latency, Packet IO).
  - World & Map State Monitor (Loaded chunks, active entities, spawned NPCs).
  - Account & Player Manager (Bans, mute, permissions, inventory inspector).
- **Tooltips & Interactive Guidance**: Every setting, toggle, metric, and action button is equipped with explanatory tooltips detailing implications, side effects, and recommended defaults.

---

## 3. Architecture Convergence

```
                      +-----------------------------+
                      |     bobsgameonline (Hub)    |
                      |  Vision, Standards & Specs  |
                      +--------------+--------------+
                                     |
         +---------------------------+---------------------------+
         |                                                       |
         v                                                       v
+-------------------------+                             +-------------------------+
|   bobsgameweb           |                             |  bobsgameonlinejava     |
|   - TypeScript / PixiJS |                             |  - Original Java Engine |
|   - WebSockets / WebRTC |                             |  - LWJGL / Server Core  |
|   - Consolidated UI     |                             |  - World Data & Chunks  |
+-------------------------+                             +-------------------------+
         |                                                       |
         +---------------------------+---------------------------+
                                     |
                                     v
                        +-------------------------+
                        |      bg / okgame        |
                        |  - Monorepo Umbrella    |
                        |  - C++ Core Engine      |
                        |  - Asset Packaging      |
                        +-------------------------+
```

---

## 4. User Satisfaction & Developer Experience Directives
- **Zero-Barrier Play**: Browser-first launch path backed by high-performance WebSocket game relays.
- **Zero Ambiguity**: Clear error codes, inline UI tooltips, and real-time visual feedback for all administrative actions.
- **Resilient Automation**: Continuous integration, automated test runners, and synchronized version governance across all submodules and repositories.
