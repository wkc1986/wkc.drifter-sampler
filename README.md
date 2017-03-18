# wkc.drifter-sampler
Max for Live sampler instrument. Granulates with 2d.wave~ with random motion between slices.  
4-voice.  
This is intended for sustained droney purposes (long notes).  
`wkc.drifter-sampler.amxd` is the main file.  
Open `drifter-sampler.maxproj` for an overview of all files.  
Subpatchers in `/patchers` including some factory abstractions copied to local.  

## Instructions
1. Drop audio file to load.
2. Select section to be played with `rslider` (overlaid on top of `waveform~`).
3. Set root MIDI note with `kslider` below (C4 = no transpose).
4. Choose # of slices to chop selection into with knob.
5. **Motion** panel:
  * *Drift*: interval at which random positions in the selection are generated.
  * *Jitter*: interval at which displacements around the current position are generated.
  * *Amount*: max displacement around the current position.
6. Set note envelope with the `function` and the envelope length with the *Length* knob.
7. Set pans for each of the voices. Top `rslider` sets all pans at once. *Scram* button randomizes all pans at once.

## Isomorphism
One principle is that you should be able to easily stretch or contract the time scale.
The playback section selection and Drift parameter control the static-ness of the sound.
If the selection is small and/or the Drift is large, it should sound more 'frozen.'
The Length parameter isomorphically time-stretches the envelope, so you can go from a quick note to a drawn-out note with the same 'shape.'

At least, this is how things are supposed to be.
