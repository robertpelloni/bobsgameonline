# Bob's Game Online - Deployment & Environment Guide

## Ecosystem Deployment Overview

Because `bobsgameonline` oversees both the Java server backend and the modern TypeScript web client, deployments are organized into two primary targets: the Game Server and the Web Client.

---

### 1. Web Client Deployment (`bobsgameweb`)
- **Prerequisites**: Node.js 18+ or Bun, npm / yarn.
- **Build Steps**:
  ```bash
  git clone https://github.com/robertpelloni/bobsgameweb.git
  cd bobsgameweb
  npm install
  npm run build
  ```
- **Static Hosting**: Deploy output `dist/` or `build/` to any static hosting provider (e.g. Cloudflare Pages, Vercel, Netlify, or Nginx).
- **Environment Variables**:
  - `VITE_SERVER_WS_URL`: WebSocket endpoint for the game server (e.g., `wss://game.bobsgame.com/ws`).
  - `VITE_DASHBOARD_ENABLED`: Flag to enable operator dashboard UI overlay.

---

### 2. Game Server Deployment (`bobsgameonlinejava`)
- **Prerequisites**: OpenJDK 17 or 21, Gradle or Maven depending on build descriptor.
- **Build Steps**:
  ```bash
  git clone https://github.com/robertpelloni/bobsgameonlinejava.git
  cd bobsgameonlinejava
  ./gradlew build  # or mvn package
  ```
- **Execution**:
  ```bash
  java -Xms1G -Xmx4G -jar build/libs/bobsgameonline-server.jar --port 43594
  ```
- **System Tray Mode**: When run in desktop environments with GUI support, the server launches an optional system tray icon allowing real-time TPS monitoring, log console access, and graceful shutdown. In headless Linux server environments, run with `-Djava.awt.headless=true` and manage via systemd or Docker.

---

### 3. Containerized Stack Setup (Recommended)
```yaml
version: '3.8'
services:
  game-server:
    image: bobsgameonline/server:latest
    ports:
      - "43594:43594"
      - "8080:8080"
    environment:
      - SERVER_TICK_RATE=60
      - MAX_PLAYERS=500
    restart: always

  web-client:
    image: bobsgameonline/web:latest
    ports:
      - "80:80"
    environment:
      - SERVER_WS_URL=ws://game-server:8080/ws
    depends_on:
      - game-server
    restart: always
```
