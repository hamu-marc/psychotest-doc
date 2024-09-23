# Styles of the elements in the rendered test

The design of the rendered test elements can be altered using a so called CSS style. A special `#css` note can be used to set the CSS style including the selectors, `#styleform` and `#style` sets the style for the last form or element. More on CSS styles, see [https://en.wikipedia.org/wiki/CSS](https://en.wikipedia.org/wiki/CSS). Specific cases for setting the styles for display are also shown further in the text.

### #css

The stimuli are presented in a HTML tag, which has the 'stimulus' class. The selector can be used to set eg. the position at which the stimuli appear on screen during scrolling.

```
#css .stimulus{position:sticky;top:0;z-index:1}
```

See the [Stimuli always on screen](../../ceska-dokumentace/typy-stimulu-a-jejich-prezentace/stimuli-vzdy-na-obrazovce.md) chapter for further instructions.

### #styleform

The task is presented in a HTML element. Defining the style using the preceding method will set the style for all forms on a screen. A special '#styleform' comment can be used in a more specific setting for one task only. E.g. the following will set the form as floating, aligned to the left on a white background and a red text:

```
task Evaluating the degrees of a GRBAS voice distruption 
    #styleform float:left; width:100%; background-color:white; color:red
```

See the [Stimuli always on screen](../../ceska-dokumentace/typy-stimulu-a-jejich-prezentace/stimuli-vzdy-na-obrazovce.md) chapter for further instructions (../typy-stimulu-a-jejich-prezentace/stimuli-vzdy-na-obrazovce.md).

#### #style

defines the CSS style for the last generated element
