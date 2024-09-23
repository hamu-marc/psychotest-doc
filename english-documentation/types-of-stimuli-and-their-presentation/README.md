# Types of stimuli and their presentation

The stimuli are added immediately after the `screen` command using the `stimulus` keyword which is followed by 1 or more files with a stimuli. The stimuli can be classed by their file format:

* `mp3` and `wav` represent sound stimuli. A test screen will feature a button allowing playback of the given file.
  * `stimulus(controls) 1.wav` will add a further control elements enabling to set the volume and to change the position in the playback of the file.
  * `stimulus(waveform) 1.wav` will present a sound signál and control elements (volume control and position in the file).
  * Square brackets can contain the start and stop times in miliseconds and can define the onset and ending moments of the audio playback `stimulus 1.wav [200,500]`.
* `mp4` files represent video stimuli (picture with a sound). The screen with a video stimuli will be displayed as a frame with playback control buttons
* `png`, `jpg` represent image stimuli. They are displayed as a freame with a picture.

Example:

```
test StimuliExample
screen Evaluation of a picture
  stimulus stimuli/tomas/IMG_4604.JPG
  task ...
screen Evaluation of the sound
  stimulus(waveform) 1.wav 
  stimulus(controls) 2.wav
  stimulus 5.wav 
  stimulus 7.wav [200,500] 
  task ...
screen Evaluation of a video
  stimulus stimuli/yamaha/clavinovapianoharmonica.mp4
  task ...
```
