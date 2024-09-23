# Permanent presence of stimuli on a screen

A screen containing multiple concurrent tasks can display a scrolling column which will make the stimuli disappear when scrolling (the button will leave the bounds of the screen. The position of the buttons can therefore be fixed using the following '#css' code:

```
#css .stimulus{position:sticky;top:0;z-index:1}
```

{% hint style="warning" %}
The code will add a CSS style. The `.stimulus` is a selector. It marks the elements of a `stimulus` class. Those will be assigned a`postion:sticky` style which will make the element stick to the screen during scrolling at a "top:0" position. It will also be visible as it will also cover different elements if they reach below "z-index:1".
{% endhint %}

The below screen can serve as an example of its use for evaluating voice pathology:

```
test demo2Scrolling.ptest
screen the roll of long content, 1 stimuli above 
  stimulus(buttoncz1) 1.wav
  #css .stimulus{position:sticky;top:0;z-index:1}
  
  text Triggering the <b>play</b> button will start a playback of vocal record.
    text Please evaluate and describe it in terms of the following qualities
          
    task Evaluating a voice impairment RBASI
    #styleform float:left; width:100%; background-color:white; color:red
 		text 0 - <u>norma</u>;  0.5 - <i>minimal imparment</i>;  1 - low;  1.5 - low to average;  2 - <b>average</b>;  2.5 - <b>average to hard</b>;  3 - <b><u>very hard</b></u> 
    
    task G – overall impairment
    #styleform float:left; width:48%; background-color:peachpuff;
 		text <i>A global impairment is not evaluated for this type of stimuli.</i>
    
    
    task R - hoarsness / roughness
    #styleform float:left; width:48%; background-color:lavenderblush;
 		scale 0 3(0.5) 0 <u>null</u> 0.5 <i>minimal</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
    
    task B - breathiness
    #styleform float:left; width:48%; background-color:lightcyan;
 		scale 0 3(0.5) 0 <u>null</u> 0.5 <i>minimal</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>u>
    
    task A - weakness
    #styleform float:left; width:48%; background-color:cornsilk;
 		scale 0 3(0.5) 0 <u>null</u> 0.5 <i>minimal</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
    
    task S - tension
    #styleform float:left; width:48%; background-color:snow;
 		scale 0 3(0.5) 0 <u>null</u> 0.5 <i>minimal</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
    
    task I - instability
    #styleform float:left; width:48%; background-color:gainsboro;
 		scale 0 3(0.5) 0 <u>null</u> 0.5 <i>minimal</i> 1 low  2 <b>medium</b> 3 <b><u>"heavy"</b></u>
    
    task fullness / sonority
    #styleform float:left; width:100%; background-color:white; color:blue
 		text The quality of <b>fullness / sonority</b> represents the richness and healthiness of voice, <i>it is the opposite of weak or sharp voice.</i>
        
    task fullness / sonority
    #styleform float:left; width:96%;background-color:honeydew;
 		scale 0 3(0.5) 0 "weak" 0.5 "" 1 "" 1.5 "medium" 2 "" 2.5 "" 3 "sonorous"
  	
    task Notes
    #styleform float:left; width:100%;background-color:white;color:DarkOliveGreen
    text Describe the prominent qualities  of sound, in particular <i>nestability</i>
		edit?

```

<figure><img src="../../.gitbook/assets/atc3dmhnok.gif" alt=""><figcaption><p>The play button will remain visible in the upper part of the screen during scrolling</p></figcaption></figure>
