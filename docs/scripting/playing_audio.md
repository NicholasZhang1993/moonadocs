## Playing Audio <a name="audio"></a>

Sound designers can implement dynamic audio in `MObject` assets (deriving from the `UnityEngine.ScriptableObject` class). `MObjects` define audio behaviour and can play both [AudioClips](https://docs.unity3d.com/ScriptReference/AudioClip.html) and/or other `MObjects`.

All `MObjects` expose the `Play()` method which takes a position as `Transform` (the sound follows) or `Vector3` (static 3D position). passing a `Vector3` has the tiniest of performance benefits.

    // passing a transform
    carEngine.Play(this.gameobject.transform);
  
    // passing a Vector3
    firePlace.Play(new Vector3(x, y, z);

For user interface sound we can simply use `Play2D()` which takes an optional floating point value for panning (-1 left, 0, center, 1 right)

    // forcing a sound to play in 2D mode
    buttonSelect.Play2D();

The Play methods each return an `MHandle` object which is used to control the sound after it has been played (see [Controlling MHandles](#handles))

These Play methods also take an `MInstanceParameters` which can be used to control the initial state of the sound, blending of container items and change the **Pitch** or **Volume** of a sound according to the parameters passed & the sound designer's implementation.

This allows the sound designer to create intricate audio behaviour without coding and enables more artistic control over how the sound changes depending on the game state.