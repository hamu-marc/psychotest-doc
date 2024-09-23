# Paired test

Paired test command will generate pairs from a set of stimuli. Each pair is then presented in buttons on one screen.

```
screen per 2
  stimulus 1.wav
  stimulus 2.wav
  stimulus 5.wav
  task loudness
  values 1 2
  taskforstimuli fullness
  values 0 1 2 3 4 5
```

The definition for the above 3 stimuli will generate a total of 3 screens with the following pairs

* 1.wav,2.wav
* 1.wav,5.wav
* 2.wav,5.wav

Each stimuli in a pair will have its task (taskforstimuli) presented in a left and right column

<figure><img src="../../.gitbook/assets/image (13) (1).png" alt=""><figcaption><p> </p></figcaption></figure>
