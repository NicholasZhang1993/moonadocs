# Voice Management

### Maximumm Voice Count

The maximum amount of "real voices" ie AudioSources spawned by Moona. This setting goes hand in hand with the menu option `Edit/ProjectSettings/Audio/Max Real Voices`. If the game uses "naked AudioSources" (not managed by Moona) the project settings should have their limit set higher than the MConfig. Otherwise they can be set to the same value.

### Culling Volume

The volume below which Voices will virtualize to save processing and free up AudioSources for other sounds to render audio.

### Culling Pitch

The pitch below which Voices will virtualize (see culling volume for more info).