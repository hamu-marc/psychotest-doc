# Location of the stimuli and test

The test definition files are loaded form a folder on a remote data storage. Stimuli linked to the test are located either in the same sotrage alongisde the test definition file, or can be additionally defined using a `base` keyword and loaded from a different source (such as a folder containing shared stimuli).

Eg. `base https://filedn.com/lHGc7w3H4jOpIe46u1nPt57/Psychotest/stimuli` will set all stimuli to load from this storage. Stimulus `1.wav` will load from the `https://filedn.com/lHGc7w3H4jOpIe46u1nPt57/Psychotest/stimuli/1.wav` address.

The following is an example of a test with defined 'base', which redirects to a different address.

```
test demo4Base.ptest
base https://filedn.com/lHGc7w3H4jOpIe46u1nPt57/Psychotest/stimuli
screen Introduction
text The following screens will present sounds from different data store
screen per 1 stimul upper 
  stimulus(buttoncz1) 1.wav
  stimulus(buttoncz1) 2.wav
  stimulus(buttoncz1) 3.wav
  stimulus(buttoncz1) 5.wav
  stimulus(buttoncz1) 6.wav
  stimulus(buttoncz1) 7.wav
  #css.stimulus{position:sticky;top:0;z-index:1}
  
  text The record of a voice will playback at the push of the <b>play</b> button.
    text Evaluate it on the following qualities and note all significant pathologies.

    task G - overall impairment
    #styleform float:left; width:48%; background-color:lavenderblush;
 		scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>

```

{% hint style="info" %}
The `base/stimul` address has to link to a file. Pleas make sure addressing it leads towards playback of a sound file or its download (e.g. in a browser). The base/stimul address will not work if the access is only indirect (such as through a web based service).
{% endhint %}
