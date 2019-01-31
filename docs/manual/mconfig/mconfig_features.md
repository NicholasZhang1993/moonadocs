# Feature Toggles

### Instance Updates

This option disables the Moona internal entity updates.

**Only touch this if you know what you are doing**

### Limit Instance Update Rate

This option reduces the frequency of entity updates to a certain "frame rate" (assuming that value is lower than the actual render frame rate).

### Culling

This option disables voice management and object pooling. 

**Only touch this if you know what you are doing**

### Schene Checks

This option determines if Moona detects scene changes without game code callbacks. Some custom systems realy on this feature.

###  Mute On Focus Lost

Mute the game's audio when the game looses focus.

### Static Listener

This option places the AudioListener at `Vector3(0, 0, 0)` and expects the game to handle distance attenuation.