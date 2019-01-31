## For sound designers

- runtime blending of `playable items`
- random `playable item` playback (do not repeat **x** variations)
- allow iteration on `MObjects` without dirtying any scene (no merge conflicts)
- custom attenuations for distance and/or input parameters,
- automated MObject creation via import using designated naming conventions (ie. creating MObject random asset from a list of sounds, create a blending playable item from a list of sounds)

## For game developers

- simple initialization via a single API call
- no-fuss audio playback via `MAudioOnStart` components
- easy control over continous & dynamic sounds by catching `MHandle` object wich return from `MObject.Play()` call
  - control volume, pitch, seek, playback state
  - control dynamic expression (ie intensity)
- basic voice management & instance limiting based on:
  - `MObject` settings
  - volume
  - priority offset
  - `MixerGroup` limits
- only active `voices` that are audible use an `AudioSource` (infinite virtual `voices`)
- scriptable audio mixer (no manual "expose volume parameter" required)