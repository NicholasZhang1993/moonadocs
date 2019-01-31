# The List View

## Actions

The leadin and follow actions require an Advanced proprty to be present in the MObject. A button will appear if one can be added.

Each action will have an object field for the item to be played, an indicator of the MObjects fade times and a volume offset (dB).

### Leadin Action

The leadin action is triggered befor the main part of the MObject gets played back. This feature is useful for power up sounds (car engine starting).

The main sound will start playing right after the leadin is finished, unless a fade in time is set in which case it will be played that amount of time before the leadin finishes.


### Follow Action

This feature is useful for power down sounds or when we want to chan multiple MObjects together. It's also possible to set the follow action to the MObject itself in which case the MObject will retriger once it's done playing (useful for a music playlist).

The follow action is played the sound instance is stopped (`Stop()` is called) or once the sound reaches end of playback. When a fadeout time is set for the MObject the follow action will trigger that amount of time early to overlap the fadeout with the follow action.

## The Playlist

### Playmode

The Playmode determines how the playlist is evaluated. The options available are:

- Sequence
	- Each trigger will play the next
	- The playlist loops.
- Random
	- Each trigger will pick a random item to play.
	- Respects the "don't repeat" option.
- Weighted
	- Each trigger will pick a item according to their weights. If all weights are the same the behaviour is identical to "Random".
	- Respects the "don't repeat" option (which might affect weighting).
- Blending
	- Plays all items at once.
	- The RTPC properties diplay the container blending parameters for each item.

### Don't Repeat Last

This option ensure that a certain amount of item playback history will be kept to avoid repititions. This might interfere with weighted playback.

### Item List

Each MPlayable Item in the playlist is represented in one row.

- Object Field
	- Display the AudioClip/MObject to be played
- Length
	- Display the length of the current item
- Volume
	- Offset the items volume (dB)
- Weighted
	- Determines the items weight in weighted playback
- Play Button
	- Use to audiotion the item
