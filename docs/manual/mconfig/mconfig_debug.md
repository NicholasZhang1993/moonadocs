# Debug Options

This section allws to enable certain tooling for in editor debug info.

### Enable Debug Mode

This is the basic debug on/off switch. without it many debug options will not funtion properly. One effect is that Moona will start printing important messages to the console so if Moona behaves odd in some way this would be the first thing to enable.

### Enable Verbose Logging

This option increases the amount of debug info. Moona will print lots of information about it's state. To use this information in depth knowledge might be required.

### Measure Listener Levels

This option captures the pieak and average volumes of the [AudioListener](https://docs.unity3d.com/ScriptReference/AudioListener.html) in the editor every frame. If **Draw Debug Gizmos** is enabled it will display the current values and displays them in the game view.

### Draw Debug Gizmos

toggles various gizmos for debugging (Listener levels, FlatPanning configuration, AudioSource lables).

### Draw AudioSource Labels

This option enables floating lables at the screen position of each AudioSource managed by Moona.