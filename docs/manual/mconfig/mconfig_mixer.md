# Mixer Assignments

This section provides accessible references to impotant MMixerGroups

### Mixer

The Unity AudioMixer that handles the audio routing

### Master

The master bus. All audio should be routed through here, either directly or by a MMixerGroup hierarchy.

### SFX

The main MMixerGroup for Sound Effects. These sounds should be related to the game world.

### Music

Music should be routed through this MMixergroup.

### UI / FE

This MMixerGroup should route all user interface sound that are related to the game, not the game world.

### VO

All voice over and dialogue should be routed through here. It might make sense to feed the VO group with seperate MMixerGroup for world VO and front end VO.