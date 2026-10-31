# SF5p2

**A first-person exploration game built in Unreal Engine 5.8.**

![Story Framework logo](SF5p2.png)

SF5p2 is a first-person exploration project centered on moving through spaces, examining objects, and uncovering information through interactions and narrative events. Its content is organized around the included **GameFramework** plugin, which provides the project’s player, interaction, inventory, dialogue, task, save, camera, and interface assets.

The repository contains framework examples and prototype maps as well as the project configuration. It is an in-progress game project; the included examples demonstrate systems and interactions, and should not be mistaken for a finished campaign.

## Gameplay foundation

The project’s assets point to a deliberate, hands-on exploration loop:

- **Explore from a first-person perspective.** First-person camera settings, player and controller Blueprints, camera presets, and movement camera shakes are included. Footstep audio assets cover dirt, metal, tile, water, and wood surfaces.
- **Inspect and interact with the environment.** Interaction settings cover inspection, pickup, item requirements, dragging, reach, prompts, and alternate interaction methods. Example objects include doors and keys, drawers, a briefcase, a cassette, a generator, a valve, a monitor, and a breakable wall prompt.
- **Collect and track discoveries.** Inventory, item combination, journal, memoir, and task assets provide a foundation for carrying objects, recording discoveries, and following objectives.
- **Support character and story scenes.** The framework includes dialogue tables, NPC examples, dialogue choices and reply data, sequence management, dialogue cameras, and quick-time-event data.
- **Build atmosphere through sound and presentation.** Flashlight flicker and toggle sounds, door sounds, note sounds, post-process materials, localized fog assets, and camera effects are available for environmental storytelling.

These are capabilities represented in the project assets, not a promise that every system is fully connected or polished in the current build.

## Project contents

Most of the game’s assets live in the plugin rather than the project-level `Content` folder.

```text
SF5p2/
├── Config/                         # Unreal project and input settings
├── Plugins/
│   └── GameFramework/
│       ├── GameFramework.uplugin
│       ├── Content/
│       │   ├── Camera/             # Camera settings, presets, and shakes
│       │   ├── Cinematics/         # Dialogue, sequences, and story-choice data
│       │   ├── Example/            # Demonstration characters, props, and dialogue
│       │   ├── Interaction/        # Interaction types and configuration assets
│       │   ├── Level/              # Example maps and level assets
│       │   ├── Player/             # Player, inventory, journal, and memoir assets
│       │   ├── Save/               # Save data and save manager assets
│       │   ├── Task/               # Task and objective data
│       │   └── UI/                 # Menus, prompts, widgets, fonts, and input art
│       └── Resources/
├── Content/                        # Project-specific content (currently sparse)
├── SF5p2.png                       # Story Framework project mark
└── SF5p2.uproject
```

### Included example maps

The plugin contains these maps and scenes:

- `GameFramework/Level/ExampleMap`
- `GameFramework/Level/ExampleMainMenu`
- `GameFramework/Level/InspectAnimation`
- Starter Content maps: `Advanced_Lighting`, `Minimal_Default`, and `StarterMap`

The example content includes interaction Blueprints, NPC examples, sample dialogue tables, and prototype-level assets. Use these to explore the included systems and as a starting point for project-specific spaces.

## Requirements and opening the project

- **Unreal Engine 5.8** (the version recorded in `SF5p2.uproject`)
- The `GameFramework` plugin included in this repository

To open the project, clone or download the repository, then open `SF5p2.uproject` with Unreal Engine 5.8. Let the editor finish loading assets and building its local cache on the first launch. The project is Blueprint and content based; there is no project `Source/` directory or C++ source currently included.

To inspect the included playable examples, open the maps from the Content Browser under the `GameFramework` plugin. The editor startup map is configured as `GameFramework/Level/ExampleMap`.

## Controls and input assets

The project includes input mappings and UI icon assets for keyboard and several controller families, including Xbox, PlayStation, Switch Pro, and Steam Deck layouts. The icons indicate available prompt artwork; check the project’s current input mappings and in-game prompts for the actual bindings. This README does not assume a final control scheme.

## Current development status

SF5p2 is still in development, and known bugs remain. The repository has framework and example content, but its assets alone do not establish that a complete story, final levels, or release-ready gameplay loop is present. Treat the example maps and framework content as a development foundation.

One configuration detail to check when launching the game: `Config/DefaultEngine.ini` sets the editor startup map to the included `GameFramework/Level/ExampleMap`, but the game startup map still points to `/Game/StoryFramework/Core/Example/Level/ExampleMainMenu`. The included menu map is under the `GameFramework` plugin. If runtime startup or packaging cannot find the configured map, update the game startup map setting to the intended included level.

## Repository

[Allurisma/Discovery](https://github.com/Allurisma/Discovery)
