# Random ordering of sounds

The order of sounds on the buttons is defined by their order in the test code. It is possible to change the order of the sounds by using the `randomstimuli` a `randomintuple` keywords.

## Random order of the sounds in a group defined by a row

The stimuli on a single row in the test code can be randomised using the `randomintuple` command either at the beginning of the test code or as part of the screen for the stimuli and task definition

```
  test CiselneStimuli
    randomintuple
  screen Random stimuli in a row
    stimulus 1.wav 2.wav 5.wav 7.wav
```

`randomintuple` at the test onset will randomise all following screens. The test will appear this way to the end user:

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption><p>Each stimulus is assigned to an individual button, but the probability of the first button having been assigned 1.wav is 25%</p></figcaption></figure>

`randomintuple` in the course of the test will cause the particular screen and all screens that follow to have a random order of the stimuli and rows. The `randomintuple` should be stated at the end of the screen.

```
  screen Random stimuli in a row
    stimulus 1.wav 2.wav 5.wav 7.wav
    randomintuple
```

{% hint style="info" %}
Beware, the order of stimuli defined using more rows will not be affected by the command. The following test display the buttons and playback the stimuli as they are in the test.
{% endhint %}

```
  test NumberedStimuli
    randomintuple
  screen Unrandomised stimuli
    stimulus 1.wav 
    stimulus 2.wav 
    stimulus 5.wav 
    stimulus 7.wav
```

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption><p>The buttons wil initiate playback of 1.wav, 2.wav, 5.wav and 7.wav</p></figcaption></figure>

It is therefore possible to create 2 groups. Each group will have a mixed oder but the groups will not be mixed at random.

```
  screen More stimuli, random columns (12) (57)
    stimulus 1.wav 2.wav 
    stimulus 5.wav 7.wav    
    randomintuple
```

<figure><img src="../../.gitbook/assets/image (14) (1).png" alt=""><figcaption><p>The buttons in the first column will initiate playback of sounds 1 and 2 in random order, the buttons in the second column will cause the same for sounds 5 and 7</p></figcaption></figure>

TODO: not functional as of yet

```bash
  test numbered stimuli
    randomstimuli
  screen More stimuli at random
    stimulus 1.wav 
    stimulus 2.wav 
    stimulus 5.wav 
    stimulus 7.wav

```
