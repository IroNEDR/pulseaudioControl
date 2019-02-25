# pulseaudioControl
Volume controller for pulseaudio with bash without needing to identify the current sink being used.
I wrote this script for my i3 setup with pulseaudio. I wanted to be able to change the volume for all my devices at once.

## Functions
* increaseVolume(): Increases the volume for all sinks by 5%
* decreaseVolume(): Decreases the volume for all sinks by 5%
* toggleMute(): Mute or unmute all sinks

## Example
```bash
./setVolume functionName
```

Or inside the config file for your i3wm media keys:
```bash
# Pulse Audio controls
#increase sound volume:
bindsym XF86AudioRaiseVolume exec --no-startup-id /path/to/setVolume.sh increaseVolume
#decrease sound volume:
bindsym XF86AudioLowerVolume exec --no-startup-id /path/to//setVolume.sh decreaseVolume
# mute sound:
bindsym XF86AudioMute exec --no-startup-id /path/to/setVolume.sh toggleMute
```
