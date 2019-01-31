## Setting MInstanceParameters

In the above section we've seen the use of the `MInstanceParameters` class. This is used to define audio behaviour when initially playing an `MObject`, but also to control it's behaviour while it's playing back.

You can create a parameter object and initialize it's values like so:

    MInstanceParameters parameters = new MInstanceParameters()
    {
      Volume = 0.5f,
        InputParameter = this.objectSize,
        Velocity = impctMagnitudeNormalized
    };

You can generate these objects freely and pass them to a `MHandle` like so:

    handle.SetParameters(parameters);

These parameters control only a single instance of a sound at a time.

**A** (discouraged) **alternative to MInstanceParameters**

Alternatively one can use specific function on the `MHandle` to control one aspect of it at a time but this is discouraged for optimization reasons and might be deprecated at a later point in time.

If a 2D sound needs a panning update one can call 

    handle.SetPanning(-0.3f);
    handle.SetVolume(0.5f);
    SetPitch(0.75f);


## Setting Global Parameters

Depending on how the sound designers have implemented their sounds there might also be global parameters which can be set to control many aspects of the sound at once. This can be done via the parameter name as a string or the hash of that string.

    // setting an RTPC via a string
    MRtpcManager.SetRtpc("weatherIntensity", normalizedIntensity);

Calling this function with a string is has a slight performance overhead so it is reccommended to cache the hash of the string instead.

    // setting an RTPC via an int
    int rtpcHash = Animator.StringToHash("enemyCount");
    MRtpcManager.SetRtpc(rtpcHash, this.Enimies.Count / this.MaxEnimies);