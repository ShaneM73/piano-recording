# Piano Solo Recording: Setup and Post-Processing Guide

## Overview

This guide records a solo piano recital in the C. Minor Recital Hall (Ellis 220, Missouri State University) with three stereo pairs on two Zoom H6 recorders, and films it with one video camera. In DaVinci Resolve, the six audio tracks are then synchronised to the camera's sound track by waveform and mixed to stereo under the picture. An interactive 3D model of the layout is here: [Piano Recording Setup](https://shanem73.github.io/piano-recording/).

### Equipment

- Steinway concert grand (Model D, about 2.74 m long), lid on full stick
- 2 Zoom H6 recorders, each with its X/Y capsule (XYH-6)
- 2 AKG C214 condenser microphones with shock mounts
- 4 stands (two for the C214s, two for the H6s), all reaching 1.5 m
- 2 XLR cables, long enough to run from the tail of the piano to H6 #1 (about 5 m each)
- 2 SD cards, fresh batteries or USB power for both recorders, closed headphones, tape measure, gaffer tape
- 1 video camera or camcorder on a tripod, with its built-in microphone switched on, an empty memory card, and mains power or spare batteries

### Track map

| Recorder | Track | Source | Role | File on the card |
| --- | --- | --- | --- | --- |
| H6 #1 | L/R | X/Y capsule, 120°, facing the piano | Main stereo image | ZOOMnnnn_LR.WAV |
| H6 #1 | Input 3 | AKG C214 L (bass side) | Spaced pair, left | ZOOMnnnn_Tr34.WAV (stereo, input 3 = left) |
| H6 #1 | Input 4 | AKG C214 R (treble side) | Spaced pair, right | same file (input 4 = right) |
| H6 #2 | L/R | X/Y capsule, 120°, facing the back of the hall | Hall reverb ("echo") | ZOOMnnnn_LR.WAV |
| Camera | Built-in audio | Camera microphone | Sync reference only, muted in the final mix | Inside the video file |

Inputs 1 and 2 on H6 #1 stay empty and switched off. The Tr34 file name assumes inputs 3 and 4 are stereo-linked, as set in the recorder settings below.

## Part 1: Setup

### 1. Place the piano

1. Turn the piano sideways to the audience: keyboard at stage left, tail pointing stage right. The curved side then faces the seats and the straight (bass) side faces the back of the stage.
2. Open the lid on its full stick, so it throws the sound toward the audience.
3. Lock the casters and place the bench.

### 2. Place the microphones

Every microphone sits 1.5 m above the floor it stands on, about ear height. Measure distances from the piano's rim with the tape measure.

| Microphone | Position | Aim |
| --- | --- | --- |
| H6 #1 (main) | 6 ft (1.83 m) out from the curved side, shifted a little to the right, toward the tail | Tilted slightly left onto the sweet spot: the middle of the open lid, where the sound is loudest |
| C214 L | 6 ft (1.83 m) beyond the tail, on the bass side (toward the back of the stage) | Front of the mic toward the piano, angled slightly toward its centre |
| C214 R | Same distance beyond the tail, 1.5 to 1.6 m from C214 L, on the treble side (toward the audience) | Same |
| H6 #2 (room) | In the seat zone, past the edge of the stage | X/Y capsule pointing at the back of the hall, away from the piano |

Notes:

- **H6 mounting.** The X/Y mics point out of the top end of the recorder. Mount each H6 so its top end points at its target: H6 #1 at the sweet spot, H6 #2 at the rear wall.
- **X/Y field.** At the 120° setting the two mic elements point 60° to each side of the recorder's centre line. Their pickup fields overlap in the middle, so the sweet spot is heard by both. The field has no hard edge: sound from outside it is still recorded, only quieter.
- **C214 front.** The C214 picks up from its side, not its top. The side with the logo is the front and must face the piano. Stand each mic upright in its shock mount.
- **C214 spacing.** 1.5 to 1.6 m is a little wider than the keyboard (1.22 m). L and R are named for what the pianist hears: bass on the left, treble on the right.
- **Sweet spot.** While someone plays, listen to H6 #1 on headphones and adjust its height and tilt in small steps until the sound is fullest. The best spot is often slightly above 1.5 m.
- **H6 #2 distance.** The plan does not fix how far into the seats it goes. Start around the fourth row and move it back if you want more reverb.

### 3. Run the cables

1. Connect C214 L to **input 3** and C214 R to **input 4** on H6 #1.
2. Both inputs are on the right side of the recorder, with input 3 above input 4. Run both cables along the floor, around the tail and the audience side of the piano, away from the pianist's path. Tape them down.
3. Leave a loose loop at each mic stand so a tug on the cable cannot move the mic.

### 4. Set up the recorders

Use the same format on both recorders, so the files line up in editing. Menu names below are from the [Zoom H6 operation manual](https://zoomcorp.com/documents/153/E_H6.pdf).

| Setting | H6 #1 (main) | H6 #2 (room) | Where to set it |
| --- | --- | --- | --- |
| Recording format | WAV 48 kHz / 24-bit | WAV 48 kHz / 24-bit | MENU > REC > Rec Format |
| X/Y capsule angle | 120° | 120° | Rotate both mic elements by hand to the 120° position |
| Tracks armed | L/R, 3 and 4 | L/R only | Track buttons (lit red) |
| Stereo link | Inputs 3 + 4 linked | Not used | Hold track button 3 and press track button 4 |
| Phantom power | On for inputs 3 and 4, +48 V | Off | MENU > INPUT&OUTPUT > Phantom |
| PAD switches (inputs 3, 4) | Off (0) | Not used | Switches beside the inputs |
| Low cut | Off | Off | MENU > INPUT&OUTPUT > Lo Cut |
| Compressor / limiter | Off | Off | MENU > INPUT&OUTPUT > Comp/Limiter |
| Backup recording | On | On | MENU > REC > Backup Rec |
| Auto record | Off | Off | MENU > REC > Auto Rec |

Notes:

- **Phantom power.** The C214s give no signal without +48 V. Plug the mics in first, then turn phantom on.
- **Stereo link.** With inputs 3 and 4 linked, the recorder writes one stereo file with input 3 (C214 L) as left and input 4 (C214 R) as right. Each input keeps its own gain knob.
- **Backup recording.** The recorder saves a second copy of the X/Y tracks 12 dB lower (ZOOMnnnn_BU.WAV). It covers the X/Y capsule only, not inputs 3 and 4, and is your safety net if a loud passage clips.
- **C214 switches.** Leave the pad and bass-cut switches on each C214 in the flat (off) position.
- **Power.** Phantom power drains batteries quickly. Run H6 #1 from a USB power adapter if an outlet is in reach, and put fresh batteries in both recorders anyway.
- **Cards.** Use empty, formatted SD cards. One hour of six tracks at 48 kHz / 24-bit needs about 3 GB on H6 #1 (backup included) and about 2 GB on H6 #2.

### 5. Set up the video camera

Most piano recordings are delivered as video. The camera's own sound is too weak to use in the final result, but it is essential: it is the reference that every H6 track is synchronised to in editing.

1. Put the camera on a tripod in the seat zone, on the keyboard side of the hall (the audience's left), raised enough to see over the seats. From there it sees the pianist's hands, the keys and the pianist's face. Treat this as a starting point and adjust it to the picture you want.
2. Frame the whole piano and the pianist, with a little space around them. Leave the camera fixed during the performance.
3. Keep the camera and its tripod out of the line between the piano and H6 #2, and away from the audience's feet.
4. Set the video format, for example 1080p or 4K at 30 frames per second. Write the frame rate down. You need it when you create the editing project.
5. Switch the camera's microphone on and set its audio to 48 kHz if the camera offers a choice. Never record the video silent. Without camera sound there is nothing to synchronise to.
6. Set focus, exposure and white balance by hand and lock them, so the picture does not shift during the performance.
7. Check how long the camera can record without stopping. Some cameras stop after about 30 minutes or split long recordings into several files. Use mains power, or a fresh battery and a spare, and an empty card.
8. Record one minute as a test and play it back. Check the picture and that the camera's sound is there.

### 6. Check the levels

Set the gain on both recorders so the loudest passage of the programme stays well below clipping.

1. Ask the pianist to play the loudest passage of the piece at full performance strength, lid open, for at least 30 seconds.
2. On H6 #1, turn the L/R knob on the X/Y capsule and the knobs for inputs 3 and 4 until the loudest peaks reach about −12 dB on the meters.
3. Set inputs 3 and 4 to the same knob position, so the C214 pair stays balanced left to right.
4. On H6 #2, set the X/Y knob the same way. The room is quieter than the stage, so this knob will sit higher.
5. Repeat the loud passage. No peak should pass −6 dB and no clip light should flash. If one does, turn that knob down and test again.
6. Record 30 seconds as a test, play it back on headphones from each recorder, and listen for distortion, hum or a dead channel.
7. Write down the knob positions and do not touch them during the performance.

Pianists usually play louder in concert than in a soundcheck. The −12 dB target leaves room for that.

### 7. Record

1. Check that the camera and both recorders show enough card space and battery.
2. Press record on the camera first, then on H6 #1, then on H6 #2. Confirm all three are running.
3. Slide the HOLD switch on each recorder, so nothing can be pressed by accident.
4. Stand beside the piano, in view of the camera, and clap once, sharply. This is the sync mark for editing.
5. Leave the stage and stay quiet for about 10 seconds before the pianist begins. That silence is useful later as clean room tone.
6. Let the camera and both recorders run through the whole programme. Do not stop between pieces.
7. After the last note has died away, wait 10 seconds, then clap once more. The second clap shows whether the camera and the recorders drifted apart.
8. Release HOLD, stop both recorders, then stop the camera. Check that each device shows the new files.

### 8. After the session

1. Copy the whole project folder from each SD card to a computer, into two folders named H6-1 and H6-2. Copy the camera's video files into a third folder named Camera. Both recorders use the same file names, so separate folders prevent mix-ups.
2. Make a second copy on another drive before erasing any card.
3. Note which take is which piece while you still remember.

## Part 2: Post-processing in DaVinci Resolve

The free version of DaVinci Resolve does everything in this part. Menu names follow recent versions (18 to 21) and may differ slightly in yours. Work on headphones or good speakers, never laptop speakers. The result is a video file carrying the mixed stereo sound, plus an audio-only WAV master.

### 1. Create the project and import the files

1. Open DaVinci Resolve and create a new project, for example "Piano recital 2026".
2. Before importing anything, open File > Project Settings > Master Settings. Set the timeline frame rate and resolution to match the camera, for example 30 frames per second at 1920 × 1080. The frame rate cannot be changed once clips are on a timeline.
3. In Project Settings > Fairlight, set the timeline sample rate to 48000 Hz, the same as the recordings.
4. On the Edit page, make three bins in the Media Pool named Camera, H6-1 and H6-2, and drag each device's files into its own bin.
5. Rename the clips in the Media Pool so they are easy to tell apart:

| File | Rename to |
| --- | --- |
| Camera / video file | Camera |
| H6-1 / ZOOMnnnn_LR.WAV | Main XY |
| H6-1 / ZOOMnnnn_Tr34.WAV | C214 pair |
| H6-2 / ZOOMnnnn_LR.WAV | Room XY |
| ZOOMnnnn_BU.WAV (both recorders) | Leave as backups. Use one only if its main file clipped. |

### 2. Build the timeline

1. Create a new, empty timeline (File > New Timeline) with one video track and four stereo audio tracks.
2. Name the audio tracks: A1 Camera sound, A2 Main XY, A3 C214 pair, A4 Room XY.
3. Drag the Camera clip to the start of the timeline. Its picture lands on V1 and its sound on A1. If the camera split the recording into several files, place them end to end in order.
4. Drag Main XY onto A2, roughly under the camera clip.
5. Drag Room XY onto A4, roughly under the camera clip.
6. Leave the C214 pair in the Media Pool for now. It goes in after the sync.

The camera sound must sit on A1. Auto Align moves every other clip to match the clip on the lowest-numbered track, and the picture must not move.

### 3. Synchronise the audio to the video by waveform

This step decides whether the finished video looks right. The camera's sound track is locked to the picture, so every H6 recording is slid until its waveform matches the camera's. Resolve's Auto Align Clips command does this ([Resolve manual](https://www.steakunderwater.com/VFXPedia/__man/Resolve18-6/DaVinciResolve18_Manual_files/part962.htm)).

1. Stay on the Edit page. The command is not offered on the Fairlight page.
2. Click the Camera clip, then Ctrl-click (Cmd-click on Mac) Main XY on A2 and Room XY on A4. Select one clip per track only.
3. Right-click one of the selected clips and choose Auto Align Clips > Based on Waveform.
4. Wait for the analysis. Main XY and Room XY slide into place under the camera clip.
5. Turn snapping on (the magnet icon). Drag the C214 pair onto A3 so its start snaps exactly to the start of Main XY.

Main XY and the C214 pair came from the same recorder and the same press of the record button. They are in perfect sync when they start at the same point, which is more exact than a waveform match, so never move one without the other.

Check the result:

1. Zoom in on the first clap. Its spike should sit at the same point on all four audio tracks.
2. Step through the picture one frame at a time. The hands should meet on the frame where the spike begins.
3. Play a passage with clear, separate notes and watch the fingers and hammers. Sound and picture should feel like one event.
4. Go to the clap at the end and check it the same way.

If something is off:

- **Auto Align did nothing or landed wrong.** This happens when the camera's sound is very quiet or noisy. Line up the first clap by hand: zoom in, turn snapping off, and drag each H6 clip until its clap spike sits under the camera's spike. Move Main XY and the C214 pair together.
- **The first clap matches but the last one does not.** The devices' clocks drifted. Cut all tracks in the silence between pieces (step 6), then run Auto Align again on each piece separately.

When the sync is right:

1. Select the camera clip and all three H6 clips, right-click and choose Link Clips. Picture and sound now move and cut together.
2. Mute track A1 with its M button. The camera sound stays on the timeline as a reference but must not be heard in the mix.

One optional refinement: in the hall, sound reached the room mic later than the stage mics, roughly 3 milliseconds for every metre of extra distance. Waveform sync removes that delay. If the mix sounds flat, slide Room XY 10 to 20 ms later and compare.

### 4. Arrange left and right

The three pairs looked at the piano from three directions, so their left and right channels do not agree as recorded. The goal is one consistent picture: the pianist's view, with bass on the left and treble on the right.

| Track | As recorded | What to do | Result |
| --- | --- | --- | --- |
| C214 pair | Left = bass side, right = treble side | Keep | Bass left, treble right |
| Main XY | Faced the piano from the audience side: left = keyboard end, right = tail end. The long bass strings run to the tail, so bass leans right. | Swap left and right | Bass leans left, matching the C214 pair |
| Room XY | Faced the back of the hall, so its left and right are mirrored compared with the stage | Swap left and right | Hall reverb matches the stage picture |

To swap the channels of a clip:

1. Right-click the clip in the timeline and choose Clip Attributes.
2. Open the Audio tab and check that Format is Stereo.
3. In the Source Channel column, set the left row to Embedded Channel 2 and the right row to Embedded Channel 1.
4. Click OK. If you already cut the clip into pieces, select all the pieces first so the change applies to every one.

Check by ear:

1. Solo the C214 pair (the S button on the track) and play a passage with clear low and high notes. Low notes should come from the left.
2. Solo Main XY and play the same passage. Then switch its swap on and off and keep the setting where it agrees with the C214 pair. From the side of the piano the left-to-right difference is small, so trust your ears over the table.
3. Un-solo, play all three together, and listen for a stable picture that does not jump between sides.

Stereo tracks play at full width: the left channel fully left and the right channel fully right. Leave it that way to start. If the picture sounds too wide or has a weak centre, lower the C214 pair a little against Main XY (next step) before changing any pan settings.

### 5. Balance the amplitudes

Open the Fairlight page and show the Mixer. Each track has a fader, and the Main bus (Bus 1) carries the stereo mix. Track A1, the camera sound, stays muted throughout.

1. Set the three faders to these starting points:

   | Track | Starting fader level | What it adds |
   | --- | --- | --- |
   | Main XY | 0 dB | The core sound and a solid centre |
   | C214 pair | −4 dB | Width, warmth and bass |
   | Room XY | −12 dB | The hall's reverb |

2. Play the loudest passage and a quiet passage. Adjust by ear, one fader at a time:
   - Raise the C214 pair for a wider, warmer sound. Lower it if the centre goes thin.
   - Raise Room XY for more hall. Lower it if the piano turns distant or blurred.
3. Listen for a hollow, "phasey" tone when Main XY and the C214 pair play together. If you hear it, lower one of the two by a few dB until it clears.
4. Watch the Main bus meter on the loudest passage. Peaks should stay at or below −1 dB. If they go higher, lower all three faders by the same amount, so the balance stays the same.
5. If the whole mix is too quiet, raise the Main bus fader until the loudest peak reaches about −2 dB. Do not add a compressor. A piano recital should keep its full range from soft to loud.
6. Leave the faders fixed for the whole programme. Changing the balance between pieces makes the piano seem to move.

If a passage clipped on the Main XY or Room XY recording, replace that clip with its backup file (ZOOMnnnn_BU.WAV), placed at the same start point, and raise its level by 12 dB to match.

### 6. Cut

Return to the Edit page. With the clips linked, every cut and trim applies to the picture and all the audio tracks at once.

1. Trim the start. Drag the left edge of the clips to the moment the video should begin, at least one second before the first note. This removes the clap and the walking noise.
2. Trim the end. Let the last note and the hall's reverb die away fully, then cut about two seconds later.
3. Add a short fade at each end. Drag the small fade handle at the top corner of each clip inward: about half a second at the start and two to three seconds at the end. Fade the picture in and out the same way, with the fade handles on the video clip.
4. For a programme with several pieces, place the playhead in the silence between two pieces and split all tracks (Ctrl+B, or Cmd+B on Mac). Remove coughs, page turns and applause between pieces as you wish, and give each cut the same short fades. The picture jumps at a cut, so fade it through black there too.
5. Never cut inside a sustained note or its reverb tail. Cut only in silence.
6. To export each piece as its own file, set In and Out points around one piece at a time in step 7.

### 7. Export the video and the audio master

1. Play the whole timeline once from start to finish. Check that A1 is muted, and watch and listen for clicks at the cuts, a wrong balance, or sound that has slipped against the picture.
2. Open the Deliver page and choose Custom Export.
3. Set the video options: Format MP4, Codec H.264, with the resolution and frame rate of the timeline.
4. Set the audio options: Codec AAC at the highest bit rate offered, and Output Track 1 set to Bus 1 (the stereo Main bus).
5. Set Render to Single clip, name the file, choose a folder, click Add to Render Queue, then Render All.
6. Play the exported video in an ordinary player. Check that sound and picture match at the beginning, in the middle and at the end.
7. Export the audio master as well. On the Deliver page choose the Audio Only preset, then set Format Wave, Codec Linear PCM, Sample Rate 48000, Bit Depth 24 and Output Track 1 to Bus 1, and render it as a single clip.

The MP4 is the file to share or upload. The 24-bit WAV is the full-quality audio master. Keep the project, the camera files and the original recorder files, so the mix can be changed later.

## Sources

- [Zoom H6 operation manual](https://zoomcorp.com/documents/153/E_H6.pdf): menu paths, file names, stereo link, phantom power, backup recording, −12 dB level guidance
- [Zoom H6 product page](https://www.zoom.co.jp/node/7): X/Y capsule 90° and 120° positions
- [DaVinci Resolve 18 manual, Auto Align Clips](https://www.steakunderwater.com/VFXPedia/__man/Resolve18-6/DaVinciResolve18_Manual_files/part962.htm): waveform alignment on the timeline
- [DaVinci Resolve 18 manual, Audio Only preset](https://www.steakunderwater.com/VFXPedia/__man/Resolve18-6/DaVinciResolve18_Manual_files/part3941.htm): audio-only rendering
- [Missouri State music department facilities](https://www.missouristate.edu/Music/Facilities.htm): the hall and its seating
