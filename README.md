# MINGO Live Universe

A living story world and immersive storytelling device where NPC presences inhabit a continuous simulated reality, generate story through behavior, and are surfaced through a live 3D observer interface.

## Core idea

MINGO is structured as a live universe platform:

- **simulation-server** runs the world
- **world-renderer** turns world state into a 3D view
- **story-translator** converts state into scenes and beats
- **automation-engine** runs the ordered engine pipeline
- **user-hub** is the personal tracking layer for stories, timelines, and characters

## Monorepo layout

```text
apps/
  demo-world/         # live 3D observer
  simulation-server/  # world runtime + WS/SSE bridge
  user-hub/           # tracking and management UI

packages/
  contracts/          # shared types
  canon/              # naming, tone, force signatures
  asset-library/      # asset registry
  scene-grammar/      # zone + scene mapping
  procedural-worldgen/# spatial generation
  world-renderer/     # 3D rendering package
  runtime-bridge/     # client/server runtime connection helpers
  automation-engine/  # tick pipeline
  attention-engine/   # sensing, attention, interpretation
  decision-engine/    # action scoring + selection
  relationship-engine/# trust/conflict/resonance
  memory-engine/      # event/place/emotional memory
  event-engine/       # event generation
  story-translator/   # data -> scene packets
  narrative-engine/   # arcs, beats, highlights
```

## Install

```bash
npm install
```

If you are using the live simulation server with WebSockets:

```bash
npm install ws
```

## Start dev apps

```bash
npm run dev:world
npm run dev:sim
```

## GitHub publish

See `GITHUB_PUBLISH_GUIDE.md` for the exact steps.
