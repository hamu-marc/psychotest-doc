# Scales and options for their rendering (scale)

Scale will render a horizontal line with a moving slider. The user can move the slider over to one of the available positions.

```
task T - global impairment
  scale 0 3(0.5)
```

<figure><img src="../../.gitbook/assets/image (2) (3).png" alt=""><figcaption><p>A rendered scale: 0 to 3 slider values and a half-a-point step</p></figcaption></figure>

### Scales with labels

Values of the scale can be labeled as required and the labels can also be semantic. The `scale` command can be followed with `value text_without_spaces`. The text of each value can contain HTML tags and the values can be underlined '' or have italic or bold formating ('', '')

```
    task R - hoarsness / roughness    
 		scale 0 3(0.5) 0 <u>normal</u> 0.5 <i>minim.</i> 1 mírná  2 <b>medium</b> 3 <b><u>"high"</b></u>
```

<figure><img src="../../.gitbook/assets/image (6) (2).png" alt=""><figcaption><p>A scale with HTML formatting</p></figcaption></figure>

### Scales with alignment of oversize labels

Verbal values can be too long for the task panel (see above). This situation can be solved by altering the alignment of the scaled element using a CSS style command (margin-left a margin-right) for all scales on a screen:`text <style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>`

```
screen per 1 RBASI and fullness
  stimulus testyHLAS/F_MaKu/F1-ff1.wav
  text <style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>

  task G - total impairment
	scale 0 3(0.5) 0 <u>normal</u> 0.5 <i>minimal.</i> 1 low  2 <b>medium</b> 3 <b><u>"very high"</b></u>
   
```

<figure><img src="../../.gitbook/assets/image (3) (3).png" alt=""><figcaption><p>Scale with 10 pixel of offset alignment of the left value and 55 pixels from the edge of the task rectangle</p></figcaption></figure>

### A vertical panel of scales

Additional taks with a scale will be diplayed under a firs scale in an oder in which it has been defined.

```
screen RBASI and fullness
    stimulus F1-ff1.wav
    text<style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>

    task R - hoarsness / roughness
    scale 0 3(0.5) 0 <u>normal</u> 0.5 <i>minimal.</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
    
    task B - breathiness
 		scale 0 3(0.5) 0 <u>normal</u> 0.5 <i>minimal</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
```

<figure><img src="../../.gitbook/assets/image (4) (2).png" alt=""><figcaption><p>Task with vertical panel of scales</p></figcaption></figure>

### Horizontal panel of scales

The 'fieldset' command can be used for a HTML horizontal arrangement of the task. The element can also be styled using CSS so that it only covers half of a screen (48%) using additional text as follows 'text '

```
screen RBASI a fullness
    stimulus F1-ff1.wav
    text<style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>
    text<style>fieldset{width:48%;float:left;}</style>

    task R - hoarsness / roughness
    scale 0 3(0.5) 0 <u>normal</u> 0.5 <i>minimal</i> 1 mild  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
    
    task B - breathiness
 		scale 0 3(0.5) 0 <u>normal</u> 0.5 <i>minimal</i> 1 mild  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
```

<figure><img src="../../.gitbook/assets/image (7) (1).png" alt=""><figcaption><p>Tasks and scales adjacent to each other</p></figcaption></figure>

### Manipulating the heights of the panel content

The height of the answer fileds for tasks is different for adjacent task and this will have a unaesthetic and disordered appearance.&#x20;

The height can be set using the 'height' CSS style for the 'fieldset' command

```
screen RBASI a fullness
  stimulus F1-ff1.wav
  text<style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>
  text<style>fieldset{width:48%;float:left;height:140px}</style>
  task Evaluation of a degree of vocal impairment (RBASI scales)
   text 0 - <u>normal</u>;  0.5 - <i>minimal impairment</i>;  1 - low;  1.5 - low to medium;  2 - <b>medium</b>;  2.5 - <b>medium to high</b>;  3 - <b><u>high</b></u>
  task G - total impairment
    text not evaluated for this impairment
  task R - hoarsness / roughness
    scale 0 3(0.5) 0 <u>normal</u> 0.5 <i>minimal</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
  task B - breathiness
	  scale 0 3(0.5) 0 <u>normal</u> 0.5 <i>minimal</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
```

<figure><img src="../../.gitbook/assets/image (8) (1).png" alt=""><figcaption><p> </p></figcaption></figure>

### Panels with variable colour backgrounds

For setting different colours

1. define a `background:inherit` property for `fieldset`
2. set the background colour in each task eg.: `#styleform background-color:peachpuff;`

```
screen RBASI a Plnost
  stimulus F1-ff1.wav
  text<style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>
  text<style>fieldset{width:48%;float:left;height:140px;background:inherit}</style>
  task Evaliating the RBASI voice impairment scale
 		text 0 - <u>normal</u>;  0.5 - <i>minimal impairment</i>;  1 - mild;  1.5 - mild to medium;  2 - <b>medium</b>;  2.5 - <b>medium to high</b>;  3 - <b><u>very high</b></u>
  task G - total impairment
  #styleform background-color:white; color:red
    text not evaluated for this impairment
  task R - hoarsness / roughness
  #styleform background-color:peachpuff;
    scale 0 3(0.5) 0 <u>normal</u> 0.5 <i>minimal</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
  task B - breathiness
  #styleform background-color:lavenderblush;
	  scale 0 3(0.5) 0 <u>normal</u> 0.5 <i>minimal</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
```

<figure><img src="../../.gitbook/assets/image (9) (1).png" alt=""><figcaption><p> </p></figcaption></figure>
