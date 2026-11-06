# Bob's Game Online - Architectural Memory & Codebase Traits

## Architectural Context
- **Repository Nature**: `bobsgameonline` is the flagship naming repository in Robert Pelloni's GitHub organization. While created as a placeholder pointer, it functions as the central governance, architecture specification, and documentation authority for the online multiplayer games.
- **Sister Repositories**:
  - `bobsgameonlinejava`: The complete original MMORPG server and client codebase written in Java. Heavy networking, custom packet handling, world state simulation, and OpenGL rendering.
  - `bobsgameweb`: The modern web port written in TypeScript using PixiJS and WebSocket networking.
  - `okgame`: Native C++ engine core.
  - `bg`: The umbrella workspace tying the engines and asset tools together.
- **Single Source of Version Truth**: Always source version strings from `VERSION.md` rather than hardcoding numbers into multiple files.
- **UI Consolidation Philosophy**:
  - Do not fragment administrative, monitoring, and operator tools across disparate subpages or deep navigation trees.
  - Prioritize a single, high-density, scrollable or modular master page with collapsible accordions or tabs arranged strictly by operational priority (Server Lifecycle > Live Health & Telemetry > Player Moderation > World Inspector > Config).
  - Every button, metric, toggle, and form element must feature tooltips or contextual help text explaining its function, expected values, and operational hazards.
