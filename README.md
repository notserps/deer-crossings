# Deer Crossings — v1.0.04

**Deer Crossings** is a Custom Shaders Patch Lua app for Assetto Corsa singleplayer that adds animated deer encounters to compatible tracks. Deer can approach from the roadside, cross the road, hesitate, stop, turn back, react to headlights, jump some low roadside barriers, and enter an articulated ragdoll state when hit.

The latest build includes wall avoidance, updated jump animations, a persistent Main-tab ON/OFF switch, and brighter deer materials for darker lighting setups.

[Download v1.0.04](https://github.com/notserps/deer-crossings/releases/download/v1.0.04/DeerCrossings-v1.0.04.zip) — free to download. The [version graph](https://notserps.github.io/deer-crossings-graph/) shows how the mod developed.

## Requirements

- Assetto Corsa on PC
- Custom Shaders Patch with Lua apps enabled
- Content Manager recommended
- Singleplayer is the intended mode for this alpha

The exact minimum compatible CSP build has not yet been established.

## Installation

### Content Manager

1. Download [DeerCrossings-v1.0.04.zip](https://github.com/notserps/deer-crossings/releases/download/v1.0.04/DeerCrossings-v1.0.04.zip).
2. Drag the ZIP onto Content Manager.
3. Install it.
4. Start an Assetto Corsa singleplayer session.
5. Open the in-game app sidebar and select **Deer Crossings**.

### Manual installation

Extract the ZIP into your Assetto Corsa root folder. The final app path should be:

`assettocorsa/apps/lua/DeerCrossings/`

If an old development build exists at `apps/lua/DeerTest/`, disable or remove it so duplicate encounters are not created.

## Main tab

The Main tab contains normal player-facing controls and status:

- Deer Crossings ON/OFF (remembers your choice)
- Hit Sounds
- Vehicle Damage
- Frenzy Mode
- Frenzy active-deer limit from 4 to 18 while Frenzy is enabled
- Current-session information

## Debug tab

The Debug tab contains testing controls and diagnostics:

- Force Deer Encounter
- Clear All Deer
- Encounter/activity information
- Surface, road-width and spawn diagnostics
- Obstacle-jump and gait status
- Impact/ragdoll/COL diagnostics
- Headlight and performance information

## Major features

- Random animated deer encounters
- Time-of-day activity weighting
- Speed-dependent encounter placement with additional high-speed lead time
- Walk, Fast Walk and Run locomotion
- Start/stop, idle, look-around and turn animations
- Roadside approach behavior
- On-road hesitation, stop and double-back behavior
- Occasional groups of deer
- Headlight stun behavior at appropriate times of day
- Cross-map multi-probe surface solver
- Low fence/guardrail recognition with authored Walk/Run jump animations
- Pass-through fallback when an obstacle cannot be recognized confidently
- Player-car/deer impact detection
- Articulated ragdoll with spine, neck, legs and terminal hoof behavior
- Multiple-ragdoll performance budgeting
- Randomized impact/deer audio
- Optional cumulative vehicle damage and impact jolt
- Frenzy Mode with configurable active-deer cap
- Main / Debug UI with custom icon and dark-blue interactive accents

## Known alpha limitations

- Some custom-track fence/guardrail collision meshes can still be difficult to recognize consistently.
- Rare extreme ragdoll poses can still produce clipping or unnatural articulation.
- Several simultaneous ragdolls can still reduce frame rate.
- Track lighting can make the deer material look somewhat different from map to map.
- Minimum CSP-version compatibility still needs wider testing.
- Multiplayer/online use has not been validated.

## Updating

For updates, replace the entire `apps/lua/DeerCrossings` folder. Do not mix Lua/assets from different versions.

## Uninstall

Delete `assettocorsa/apps/lua/DeerCrossings/`.

## Feedback

See `BUG_REPORT_TEMPLATE.md` for the most useful information to include with a report.

## Usage rights and credits

Deer Crossings is distributed under a **use-only proprietary license**. Downloading or receiving the mod does not grant permission to edit, repackage, reupload, redistribute, resell, or reuse its code or bundled assets. See `CREDITS_AND_USAGE_RIGHTS.md` and `LICENSE.txt` for details and third-party credits.
