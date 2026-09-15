# GhostForge Project Map

GhostForge is a collection of connected Trackmania research systems rather than a single optimizer.

## Core GhostForge

### TAS optimization

- Trackmania-specific candidate generation
- steering / gas / brake / timing mutations
- native candidate scoring
- distributed search
- candidate banking and confirmation
- population optimizer integration

### Native physics authority

- nonvisual native Trackmania evaluation
- positive / negative controls
- distributed execution
- final Main-authority confirmation
- retail Trackmania / TICK verification

## Geometry and sensing research

### Track Geometry Engine

Research tooling for querying Trackmania scene geometry independently from the optimizer.

Current concepts include:

- one-time spatial indexing;
- local scene queries from arbitrary car poses;
- corridor / clearance measurements;
- lightweight runtime sensing;
- source-agnostic geometry access.

### Raycast / scene sensors

Local scene observations intended for research uses such as:

- TAS analysis;
- debugging;
- future Gymnasium / RL-style observations;
- technique recognition;
- map understanding.

## Telemetry and evidence

Research components cover:

- run identity;
- checkpoint / finish reconciliation;
- provenance and authority;
- synchronization between inputs, telemetry, and results;
- compact accepted-result evidence;
- fail-closed mismatch handling.

## Map research

GhostForge uses a canonical multi-surface map corpus rather than focusing on only one map style.

Research categories include:

- road;
- grass;
- plastic;
- dirt;
- ice;
- sustained-speed / speedslide maps;
- mixed and unusual surface conditions.

## Physics Lab — planned

A future controlled-map environment for studying Trackmania techniques and edge cases with native game physics.

Candidate areas:

- nose bugs;
- uber bugs;
- bounces;
- speedslides;
- ice behavior;
- surface transitions;
- wall and edge contacts.

## Product direction

The research stack is expected to become progressively easier to use through:

- automatic map / reference ingestion;
- single-machine default operation;
- optional distributed workers;
- a user-facing GhostForge UI;
- installers / packaged releases;
- clear separation between research internals and normal user workflows.

## Possible standalone public utilities

After separate publication reviews, some non-core research components may be suitable as independent open-source projects:

- Track Geometry Engine;
- Trackmania raycast / scene-sensor toolkit;
- map inspection utilities;
- telemetry / evidence helpers.

The GhostForge optimizer/oracle backend remains separate from those utilities.

## Proven benchmark

The first proven GhostForge benchmark is Summer 2026 - 06:

- starting reference: 24.944 s
- GhostForge result: 24.916 s
- improvement: 28 ms
- retail/TICK reproductions: 5 consecutive runs

Track06 is the development benchmark, not the scope of the overall project.
