# Deer Crossings — v1.0.0-alpha.1 Release Notes

## Official Alpha v1

This is the first official public alpha of Deer Crossings. It packages the proven development runtime under a clean public-release version and documentation set.

## Highlights

- Broad cross-map spawn and locomotion compatibility using a shared multi-probe surface solver.
- Speed-dependent placement with additional high-speed lead distance for long, fast open-road maps.
- Deer approach the road using gait rules and normally transition to Walk on the roadway.
- Authored Walk and Run jump animations for recognized low fences and guardrails, with pass-through fallback when recognition is uncertain.
- Road-facing turns and conservative visible-deer cleanup behavior.
- Hybrid articulated ragdoll with constrained neck/limbs, distributed spine flex and terminal hoof segments.
- Multi-ragdoll quality budgeting to reduce performance cost when several deer are hit.
- Impact/deer sounds, optional vehicle damage and impact jolt.
- Two-tab Main / Debug UI with Frenzy Mode and a 4–18 active-deer limit.
- Custom app icon and dark-blue interactive UI accents.

## Known issues

- Barrier recognition still depends on collision geometry exposed by the track.
- Multiple active ragdolls remain one of the most expensive parts of the mod.
- Rare extreme ragdoll/contact situations can still produce clipping.
- Minimum CSP-version compatibility still needs wider testing.

## Best feedback to send

- Map/layout name
- Normal or Frenzy Mode
- Short description of the failure
- Whether it reproduces consistently
- Screenshot/video
- Relevant Debug-tab diagnostic lines when available
