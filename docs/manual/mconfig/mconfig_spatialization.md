# 2D Panning

This section controls various behaviours for MObjects which have their spatialization mode set to `channel` and those played with the `MObject.Play2D()` call.

### 2D Threshold

### Pan Depth

The amount of panning allowed. If this value is reduced hard panning left or right will result in crossover to the opposing audio channel.

### Distance Factor

This option allows multiplying all distances with a certain factor. It is useful for when the game world or the player get scaled.

### Distance Factor affects override

This option determines if the distance factor affects override distances (`MHandle.SetDistance()`).

## Flat Panning

Flat Pannin is a spatialization sceme that pans sound based on where their 3D position map onto the camera viewport. Some of the flat panning options can be visualized by enableg "Debug Gizmos".

### Center %

This option determines the size of the inner box, within which sounds are played at full volume.

### Outer %

This option determines the size of the outer box, outside of which sounds are attenuated by "Flat Range" as a distance value.

### Flat Range

This option determines the range covered for linearly interpolating between the inner and outer box.

### Flat Pannin Depth

This option determines how the sceen based panning value (y axis) maps to an output panning value (y axis).