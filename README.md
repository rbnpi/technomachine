# technomachine

*Updates*

2021-05-10 - Robin Newman updarted fork for compatability with Sonic Pi 3.3.1

2018-02-12 - [Robin Newman](https://twitter.com/rbnman) contributed new features (zero all notes, drums off and all off)

2018-01-26 - Updated Techno Machine to work with Sonic Pi 3.1

2017-01-19 - Techno Machine v1.0 for Sonic Pi and Processing

## Description

Requires Sonic Pi 3.3.1 and Processing 3 (with OscP5 and ControlP5 libraries) in order to run. 

Techno Machine is a simple synth app made with Sonic Pi and Processing. It includes 4 drum channels, patterns and kits, a synth with two oscillators and really simple filter and amplitude controls. The most fun part of it is the 8-step note sequencer! Just hit randomize and create new note sequences on fly!

FYI: Sonic Pi uses localhost and port 4560 (updated from the olde 4559) to listen to incoming OSC messages. Check that you have OSC receiving toggled on in Sonic Pi settings. Reception of osc messages has information pm ip address and sending port prepended to received cues. These are accommodated by having /osc* placed before the received address. The * is a wild card that matches any ip-address/port combination.
Updates to Ruby and Sonic Pi mean that the original method of updating a list of the 8 note sequencer pattern gave a frozen list error. This is now amended to using a list of 8 individual variables. Also added, is a function parse_sync_address which allows just one live_loop to process incoming /noteN OSC cues. Finally, the code is very near to size limit for a Sonic Pi buffer. If you have problems, use run_file "path/to/Sonic Pi Techno Machine.rb" to run it 

## How to run it?

First, open "Sonic Pi Techno Machine.rb" in Sonic Pi and run it. At this point, you shouldn't hear any sound, but the patch should be initialized and running. Next, open "Sonic_Pi_Techno_Machine.pde" with Processing and run it. You're ready to go once you see the user interface!

Before you hear any drum sounds, you must toggle one of the drums ON. The synth doesn't play anything if all note sequencer sliders are set to 0. Try setting note sequencer slider values from 40 to 60 and start increasing the Synth Filter Cutoff value. Now at this point you should start to hear the synthesizer. 

More instructions maybe coming in the near future. Have fun playing with it!

Known oddities: FM bass uses randomly picked notes from the note step sequencer. If you don't hear the FM bass it is most likely because you don't have notes set in the step sequencer. 

## Keyboard shortcuts

1-4: triggers drum pattern 1-4

a,s,d,f: toggles drums on / off

g: switches all drum toggles off

r: randomizes the note sequence

t: all notes off (gives zero values to the sequencer notes)

y: switches all drum toggles off and zeros the note sequence. (no sounds)

x: toggles low freq kill switch on / off

