# Bob's Game Online - Granular TODO & Immediate Tasks

## Immediate Tasks (Short-Term)
- [x] Create centralized version tracking file `VERSION.md`.
- [x] Standardize root documentation (`VISION.md`, `ROADMAP.md`, `TODO.md`, `MEMORY.md`, `DEPLOY.md`, `IDEAS.md`, `CHANGELOG.md`, `HANDOFF.md`).
- [x] Provide cross-linking in `README.md` to guide developers across `bobsgameonlinejava`, `bobsgameweb`, `okgame`, and `bg`.
- [x] Build automated doc validation tool `/home/jules/self_created_tools/validate_docs.py`.
- [ ] Inspect upstream submodule configuration to determine whether `bobsgameonline` should directly submodule `bobsgameonlinejava` and `bobsgameweb` or maintain index pointer.
- [ ] Implement consolidated single-page dashboard prototype in web client repository.
- [ ] Review system tray icon specifications for native server runner (LWJGL/Java or C++/Qt/Tauri).

## Bug Fixes & Refactoring Needed Across Ecosystem
- [ ] Audit Java server connection handler for WebSocket compatibility handshake.
- [ ] Replace hardcoded IP/port bindings with environment-configured host variables in server entrypoints.
- [ ] Eliminate fragmented dashboard tabs and consolidate into single unified view with collapsible panels.
- [ ] Add explicit tooltips to administrative buttons (e.g. Force GC, Kill Server, Kick All).
