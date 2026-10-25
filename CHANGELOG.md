# Deer Crossings Changelog

## v1.0.04 — Lighting Compatibility

- Material-only compatibility pass for stock Assetto Corsa / CSP-only lighting setups where deer could render excessively dark in shade.
- Raises deer material ksAmbient from 0.10 to 0.17.
- Raises deer material ksDiffuse from 0.30 to 0.33.
- Keeps ksSpecular at 0.00.
- Keeps the calibrated deer albedo texture unchanged.
- No gameplay, physics, surface, jump, wall avoidance, ragdoll, damage/audio, UI, animation, collision, or persistence behavior changes.

## v1.0.03 — Steep Wall Avoidance

- Adds generic retaining/roadside-wall avoidance without map-specific exceptions.
- Low verified guardrails/fences keep the existing authored jump behavior.
- Confidently detected solid wall faces now trigger the existing natural Stop -> 180-degree Turn -> Restart sequence instead of letting deer climb the wall.
- Wall detection is geometry-first and includes slanted retaining walls at roughly 50 degrees or steeper from horizontal, measured relative to the deer's current walking surface.
- Requires multi-height and multi-lane confirmation plus two consecutive detector checks before turning, reducing false reactions to bushes, posts, road banks and irregular collision triangles.
- Explicit jumpable fence/guardrail labels remain excluded from wall-turn classification.
- Each deer performs at most one automatic wall-avoidance turnaround to prevent ping-pong behavior between parallel walls; later uncertain obstacles retain pass-through behavior.
- Keeps all v1.0.02 jump-animation, persistent master-toggle, surface, ragdoll, damage/audio, UI and asset behavior unchanged.

## v1.0.02 — Revised Jumps + Persistent Master Toggle

- Replaces both authored guardrail jump clips with revision-2 exports from the supplied jump package.
- Updates Run Jump trigger distance from 4.1067 m to 2.720 m.
- Updates Walk Jump trigger distance from 3.6527 m to 2.505 m and replaces its horizontal distance curve (9.3925 m total).
- Adds a persistent Main-tab master ON/OFF switch using CSP `ac.storage`.
- OFF clears active deer/pending encounters and pauses the complete Deer Crossings runtime until re-enabled.
- Keeps the v1.0.01 model, materials, surface solver, high-speed timing, ragdoll, damage/audio behavior and visual theme unchanged.

# Deer Crossings — Public Changelog

## v1.0.01 — Alpha v1 Update

- Removed Fast Walk from normal deer behavior; ordinary walkers now use Run for the off-road approach and return to Walk at road entry.
- Increased surface-solver peel depth from 3 to 6 layers for stacked/double-sided roadside fence collision.
- Increased temporary moving surface hold from 0.22 s to 0.55 s to reduce fence-related locomotion freezes.
- Added generic wire/railing/netting surface labels to roadside-prop filtering.
- Retains the official Alpha v1 high-speed timing, ragdoll, jump, UI, audio, damage, model and licensing systems.

## v1.0.0-alpha.1 — Official Alpha v1


- First official public alpha release.
- Promotes the proven development runtime into the official public Alpha v1 package.
- Universal multi-probe surface handling retained.
- High-speed walker and runner lead-distance improvements retained for fast/open-road maps.
- Authored guardrail/fence jump system retained.
- Articulated ragdoll and multi-ragdoll performance budgeting retained.
- Main / Debug UI retained with polished compact layout, custom app icon and dark-blue interactive accents.
- Public documentation, credits and use-only distribution terms finalized.

## Development lineage

The v0.9.73 RC/Alpha test series was used to develop and validate surface handling, animation transitions, barrier jumping, impact/ragdoll behavior, high-speed encounter timing, UI and packaging before the official v1 Alpha release. Internal/test-build details are intentionally omitted from the public package.
