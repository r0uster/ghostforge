# GhostForge

## Trackmania Optimization & Research Platform

> **The server searches. Trackmania decides.**

GhostForge is a Trackmania 2020 research and optimization platform built around one idea: use **native Trackmania physics** to search, test, and understand driving inputs without making the rendered game the inner optimization loop.

It started as a TAS search project, but the work now spans several connected Trackmania research areas: optimization, native-physics evaluation, distributed execution, geometry and raycast sensing, telemetry/evidence tooling, map analysis, retail/TICK verification, and future controlled physics experiments.

## Proven result

On **Summer 2026 - 06**, GhostForge improved a **24.944 s** reference run to **24.916 s** — a **28 ms improvement**.

The 24.916 s candidate was:

- found by automated distributed search;
- independently reconfirmed by the native oracle;
- verified as legal for the accepted steering domain;
- reproduced **five consecutive times** in retail Trackmania using TICK.

This is a tool-assisted research result, not a claim of a human leaderboard record.

## What exists today

GhostForge is more than one optimizer. The research stack currently includes:

### Optimization and TAS search

- legal steering / gas / brake / timing candidate generation;
- Trackmania-specific mutation operators;
- distributed candidate evaluation;
- incumbent banking and confirmation;
- population-based optimizer experiments, including Nevergrad;
- compact ephemeral retention so losing search scratch does not accumulate indefinitely.

### Native Trackmania physics evaluation

- a qualified nonvisual native-physics oracle;
- repeatable positive / negative controls;
- distributed evaluation across multiple machines;
- Main-authority confirmation before accepting an improvement;
- retail/TICK verification for finalists.

### Geometry and scene understanding

- **Track Geometry Engine** work for offline scene queries;
- lightweight spatial indexing;
- arbitrary-pose local scene sensing;
- raycast / clearance / corridor-style observations;
- map and geometry inspection research;
- sensor profiles intended for TAS, debugging, and future learning systems.

### Telemetry and evidence

- run identity and synchronization concepts;
- provenance / freshness / authority-aware telemetry;
- checkpoint and finish-state reconciliation;
- compact evidence for accepted results;
- fail-closed handling when identities or result authority disagree.

### Map research

The project maintains a multi-surface research corpus covering road, grass, plastic, dirt, ice, speed-oriented maps, and unusual surface combinations. Track06 is the first proven optimization benchmark, not the only target.

## How the pieces fit together

```text
Maps + reference runs
        ↓
Map / geometry understanding
        ↓
Trackmania-specific candidate generation
        ↓
Optimizer / search strategy
        ↓
Native nonvisual Trackmania physics
        ↓
Distributed evaluation
        ↓
Bank + confirm real improvements
        ↓
Retail Trackmania / TICK verification
        ↓
Verified TAS result
```

Supporting research can also branch off from the same foundation:

```text
Map geometry + car pose
        ↓
Raycast / scene sensing
        ↓
Controlled physics experiments
        ↓
Technique datasets / future learned models
```

## Current status

| Capability | Status |
| --- | --- |
| Native nonvisual Trackmania physics oracle | **Qualified** |
| Distributed evaluation | **Qualified** |
| Automated TAS search | **Working** |
| 24.944 → 24.916 improvement | **Verified in retail** |
| Ephemeral search retention | **Implemented** |
| Nevergrad integration | **Qualified end-to-end** |
| 30-minute Nevergrad Gate D search | **Completed — no gain** |
| Track Geometry Engine | **Research implementation exists** |
| Raycast / scene sensing | **Research implementation exists** |
| Multi-map generalization | **Next major step** |
| Physics Lab / synthetic technique maps | **Planned** |
| End-user installer and UI | **Planned** |

## What we are working toward

### 1. Prove GhostForge on more than one map

The next important question is not whether Track06 can be searched again. It is whether the same GhostForge workflow generalizes cleanly to a second map without rebuilding the system around it.

### 2. Turn research tooling into reusable Trackmania tools

Some non-core systems may eventually become standalone public utilities after publication audits, including:

- Track Geometry Engine;
- Trackmania raycast / scene-sensing toolkit;
- map inspection utilities;
- telemetry / evidence helpers;
- research adapters useful outside GhostForge itself.

### 3. Build a GhostForge Physics Lab

Purpose-built maps could isolate difficult Trackmania mechanics and let us systematically vary geometry, speed, angle, car orientation, and control timing.

Possible research targets include:

- nose bugs;
- uber bugs;
- bounces and landings;
- speedslides;
- ice behavior;
- plastic / surface transitions;
- wall and edge contacts.

The goal is not just to reproduce tricks, but to map the conditions under which Trackmania's own physics says they succeed or fail.

### 4. Make GhostForge usable by normal players and researchers

The eventual product experience should look much simpler than the research environment:

```text
Install GhostForge
      ↓
Select / import a map
      ↓
Provide or discover a reference run
      ↓
Choose an optimization or analysis mode
      ↓
Run
      ↓
Review verified results
```

Users should not need to understand worker VMs, internal ledgers, milestone names, or research coordination.

## Design principles

- **Trackmania decides.** Native and retail physics remain authoritative.
- **Search, do not render.** Rendering is not required for the inner optimization loop.
- **Reuse before rebuilding.** Generic infrastructure should come from mature libraries when practical.
- **Keep Trackmania-specific intelligence in GhostForge.** Candidate semantics, objectives, verification, and technique logic remain project-owned.
- **Fail closed.** Identity, legality, or authority mismatches stop evaluation.
- **Keep evidence small.** Losing candidates are ephemeral by default.
- **Offline research only.** Automated multiplayer driving and leaderboard submission are outside normal project scope.

## Public / private boundary

This public repository is intentionally a project overview and showcase.

It does **not** include private backend implementation, worker credentials, machine paths, VM configuration, raw Ghost corpora, internal ledgers, private prompts / coordination files, proprietary game/server assets, or sensitive runtime data.

The private engineering repository remains the development workspace. Public material focuses on capabilities, verified results, architecture, research directions, and eventually approved releases.

## More

- [Project map](docs/project-map.md)
- [Architecture](docs/architecture.md)
- [Results](docs/results.md)
- [Roadmap](docs/roadmap.md)

---

### GhostForge

**Trackmania Optimization & Research Platform**  
*The server searches. Trackmania decides.*
