# The sound stimuli as buttons

A `stimulus` followed by one or more `mp3` or `wav` files will be rendered as a button that will play a sound file on being pressed.

The visible form can be set by a description after the `stimulus` keyword (this can be folowed by the form of display. The `stimulus(button)` will display a button. This is a predefined behavior and does not have to be defined.

```
test demo1zvuky
  screen First screen
  stimulus 1.wav
```

<figure><img src="../../.gitbook/assets/image (6) (1).png" alt=""><figcaption><p>The stimuli represented as buttons on the screens</p></figcaption></figure>

### Play a part of the sound only

A playback start and stop time can be defined in squared brackets (in miliseconds). This defines the played part of the sound file eg.'stimulus 1.wav \[200,500]' will play a part of the sound in the 200 to 500 milisecond interval.

```
test demo1sounds
  screen First screen
  stimulus 1.wav [200,500]
```

### Playback of multiple sounds on a single page

Multiple buttons will appear if more than one sound files are defined in a single row. Unless otherwise stated, it will appear in order according to the test definition.

```
screen Sounds on a line
  stimulus 1.wav 2.wav
```

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption><p>Multiple stimuli on a single row will render buttons in a column (the first button will play the 1.wav, the second one 2.wav files)</p></figcaption></figure>

```
screen Sounds on multiple rows
  stimulus 1.wav 
  stimulus 2.wav
```

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption><p>Multiple stimuli in a list will render as buttons in a row (the first button will play the 1.wav and the second one 2.wav files).</p></figcaption></figure>
