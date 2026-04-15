# MINGO World Renderer Bundle

This bundle collects the current MINGO world-rendering direction into one saveable starter codebase.

Included:
- shared contracts
- canon labels
- asset library
- scene grammar
- procedural world generation
- React Three Fiber world renderer
- demo app shell

## What this is
A structured starter, not a full production app. It is designed so you can copy it into your existing Next.js / Vite / React workspace and keep building.

## Core flow
ZoneKind + ZoneSubtype + SceneType
-> Scene Grammar
-> Asset Selection
-> Procedural Placement
-> World Renderer

## Recommended runtime integration later
simulation-core
-> story-translator
-> renderer scene packet
-> world-renderer
-> observer-web


## Live simulation bridge
This bundle now includes a lightweight simulation server that emits live renderer packets over SSE.

### Start the simulation bridge
```bash
npm run sim
```

### Endpoints
- `http://localhost:8787/health`
- `http://localhost:8787/api/state`
- `http://localhost:8787/events`

### Demo-world live hookup
`apps/demo-world` now uses `useLiveScenePacket()` and will subscribe to the SSE stream when available. If the bridge is offline it falls back to the local demo packet.
