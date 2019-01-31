# Spatial Properties

## Spatial Mode

The spatial mode determines how the sound gets spatialized (ie how it's 3D position translates to panning etc). The options are:

- Channel
	- 2D playback - No spatialization applied.
- Spatial
	- 3D playback - Use the default vector based amplitude panning supplied by Unity.
	- Use this if you want to also apply HRTF spatialization.
- Flat
	- Uses the 2D position in the camera's view port to determine distnace from the center, and panning. See [MConfig: Spatialization](../mconfig/mconfig_spatialization.md) for information on configuring "Flat Panning".

## Panning Options

When set to Channel or Flat mode, or when the "3D Spatial Blend" option is less that **1** the panning options are visible.

The Pan determines the left/right panning of the sound.

The Pan Depth below it limits the amount of panning that the sound can have applied. Limiting the pan depth to **0.5** makes it so if the soudn instance is panned har left, the MObject's panning will only be panned to the left a little.

## Spatial Options

### Spatial Blend

The 3D spatial blend determines how much the spatialization of the sound should be based on the 3D position, and how much of the panning should happen in 2D space.

### Static Position

Even when passing in a Tranform as position data to an `MObject.Play()` call, the MObject will be played in 3D space, but not follow the transform if it moves.

### HRTF

This option will enable the "Head Related Transfer Function" (HRTF) to be applied to the sound. This only has an effect if the sound is played with a spatial blend of greater than **0** and a Spatialization plugin is set.

Depending on the project this might use one of the Unity builtin spatializers such as "Oculus", or use a 3rd party plugin such as "Steam Audio" (which needs additional setup to work properly).

### Attenuation

The attenuation mode determines the math used to transform the 3D position of the sound to a distance attenuation.

- Linear
	- The amplitude halfway betwen min and max distance is half (-6 dB)
- Logarithmic
	- An approximation of a Logarithmic falloff curve. Models reality a bit.
- Custom
	- Set a custum curve in the Curve editor.

The minimum distance determines at which distance the attenuation begins. When the distance is lower than this value the sound will play at full volume.

The maximum distance determines at which poit the sound will go silent. If the the attenuation is set to "Custom" the value at the very right of the attenuation curve will be used.