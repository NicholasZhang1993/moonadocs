# Audio Properties

## Volume

The Volume slider allows changing the volume of the MObjects playback (in dB). If the chackbox below is enabled the random amount slider is anabled and can be used to define a range of volumes for each individual `Play()` call.

## Pitch

The Pitch slider allows changing the pitch of the MObjects playback (in semitones). If the chackbox below is enabled the random amount slider is anabled and can be used to define a range of pitches for each individual `Play()` call.

## Looping

Plays the MObject's items in looping mode. This requires the game code to call 'Stop()' on the sound instance.

## Mixer Group / Routing

The Mixer Group field can be used to assign an [UnityEngine.AudioMixerGroup](https://docs.unity3d.com/ScriptReference/Audio.AudioMixerGroup.html) to the MObject. Preferably this option stays blank and a `MMixerGroup` is assigned above the Audio Properties section instead.

## Fading

An Advanced Property is required to enabled fading. If one can be added a button will appear to do so.

Fading in and out are defined by two parameters each.

- The fade time is the amount of seconds it takes for the fade to complete.
- The fade curve determines the slope of the fade

As fading happens in volume factor (linear, not dB) space, a linear fade will sound rather loud at low levels and change little at high levels. To accomplish a smoother fade in an Ease-In option should be chosen. To accomplish a smoother fade out an ease out should be chosen. The easing options become more sloped (less linear) in the following order:

- Quad
- Qubic
- Sine
- Exponential

![Easing Curves Overview](http://vitiy.info/wp-content/uploads/2014/11/Screenshot-2014-11-27-16.22.22.png)
