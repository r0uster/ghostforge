# Architecture

GhostForge separates public research concepts from private implementation details. The public architecture is:

```text
Map + reference runs
        → GhostForge search
        → native Trackmania physics
        → candidate confirmation
        → retail verification
```

The search explores structured input populations. Native Trackmania physics provides the offline scoring authority, while a distributed farm supplies parallel evaluation capacity. Promising candidates are then confirmed and reproduced in retail Trackmania using TICK.

This document intentionally omits private oracle implementation details, worker configuration, credentials, machine identifiers, nonpublic operational records, raw Ghost files, and private coordination mechanisms.
