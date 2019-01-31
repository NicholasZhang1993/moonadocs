## Controlling MHandles <a name="handles"></a>

The `MHandle` object is used to control sound behaviour of dynamic objects by updating their input parameter `handle.InputParameter = engineRpm` or stop looping sounds `handle.Stop()`.

Below you will find a section of a class that stores an MHandle so it can stop it at a later point in time. You can also see how an optional `MInstanceParameters` object is being passed in to override the volume of the resulting sound.

    public MObject sound;
    private MHandle handle;
    
    // volume is passed in in DeciBel (logarithmic unit for volume)
    public bool PlaySound(float volumeDB) {
      this.StopSound();
      
      if(sound!= null) {
        handle = sound.Play
        (
          this.gameobject.transform, 
          new MInstanceParameters {
            // converting the volume to a linear amplitude factor
            Volume = Moona.MUtil.DecibelToLinear(volumeDB)
          }
        );
      }
    }
    
    // fade-out time only applies when shorter than the MObjects define fade-out
    //    a value of '-1' uses the implementation fade time
    //    a value of '0' stops the MHandle immediatly
    public void StopSound(float fadeTime = -1) {
      if (handle != null) {
        handle.Stop(fadeTime);
        handle = null;
      }
    }

Re-Parenting a sound handle to another transform can be accomplished like so:
  
    handle.SetParent(transform);

Or if a `MHandle` is placed to a new static position or the positioning is being handled in a custom manner this can be done like so:

    handle.SetPosition(new Vector3(x, y, z));

For games that use custom positioning systems or need to override the distance an `MHandle` should be perceived at there is the option to pass a `double` value:

    handle.SetDistance(distanceFromSolarSystem);

To force the seek (/ playback) position of an `MHandle` one can use

    handle.SeekTo(battleProgressSeconds);

This might have unforeseen consequences. Use with care and seek advice from your sound designers.