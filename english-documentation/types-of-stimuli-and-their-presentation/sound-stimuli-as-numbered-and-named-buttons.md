# Sound stimuli as numbered and named buttons

### The language of the inscription on the button

Stimuli with audio files will present as play buttons as standard. It is possible to localise the inscription on the button into to following languages.

* `stimulus(buttoncz)` will show a czech instription `přehrát`
* `stimulus(buttonsk)` will show a slovak instription `prehrať`
* `stimulus(buttonde)` will show a german inscription `spielen`
* `stimulus(buttonen)`will show an english inscription `play` (reset behaviour)&#x20;

```
screen localised inscriptions of the sound buttons
  stimulus(buttoncz) 1.wav
  stimulus(buttonsk) 2.wav
  stimulus(buttonde) 3.wav
  stimulus(buttonen) 4.wav
```

### Subscript number depicting the order of the stimuli on the screen

A `1` suffix after the stimuli `button` or localised `buttoncz` command will display a subscript number of its order on the screen. The rendered number does not represent the order of the stimuli, since previous definitions `randomintuple` will change this order at random.

```
screen displaying the order of the buttons
  stimulus(button1) 1.wav
  stimulus(button1) 2.wav
  stimulus(button1) 3.wav
  stimulus(button1) 4.wav   
```

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption><p>Subscript numbers on buttons</p></figcaption></figure>

### A combination of localised button and subscript number

Example of a localised version of buttons with numbers

```
screen ordered inscriptions on localised sound stimuli buttons 
  stimulus(buttoncz1) 1.wav
  stimulus(buttoncz1) 2.wav
  stimulus(buttoncz1) 3.wav
  stimulus(buttoncz1) 4.wav    
```

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption><p>Subscript numbers on localised buttons</p></figcaption></figure>

