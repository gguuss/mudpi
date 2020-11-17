# Shell

A few shell scripts to simplify testing connection to the pi.

1. Install Alsa Tools

```
sudo apt-get install alsa-utils
```

2. Test Sound playback

```
wget https://upload.wikimedia.org/wikipedia/commons/5/55/MIDI_sample.mid
aplaymidi -l
aplaymidi --port=MS-1 midi_sample.mig
```