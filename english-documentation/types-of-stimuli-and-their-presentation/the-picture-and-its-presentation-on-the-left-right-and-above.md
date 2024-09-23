# The picture and its presentation on the left, right and above

A `stimulus` followed by 1 or more files with a 'png' suffix will be displayed as a picture on a test page.

```
test demo2picture
  screen Fourth screen
  stimulus IMG_4604.JPG
  task Choose form of the animal
  text The picture presents an animal or its form
  values reptile, amphibian, fish, bird, mammal
```

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Presentation of an image and adjecent task</p></figcaption></figure>

The stimuli will be displayed on the left and the tasks will be displayed on the right and below

### Picture on the right

Changing the display of the picture to the right can be done using a css style and insert it as text into the screen: `text <style>.stimulus{float:right}</style>`

```

screen Picture stimuli on the right
  stimulus IMG_4604.JPG
  text <style>.stimulus{float:right}</style>
   task Choose form of the animal
  text The picture presents an animal or its form
  values reptile, amphibian, fish, bird, mammal
```

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Presenting an image on the right relative to the remaining task</p></figcaption></figure>

### Picture in the middle

The following CSS style can be used to display the picture above and in the middle. It needs to be inserted as _text_ into the screen: `text <style>.stimulus{width:100%} .stimulus img{margin-left:auto;margin-right:auto;display:block}</style>`

```
screen Picture stimuli on the right
  stimulus IMG_4604.JPG
  text <style>.stimulus{width:100%} .stimulus img{margin-left:auto;margin-right:auto;display:block}</style>
  task Choose form of the animal
  text The picture presents an animal or its form
  values reptile, amphibian, fish, bird, mammal
```

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption><p>Presenting an image in the middle and above position</p></figcaption></figure>

### The picture in the middle and above is affixed during window scrolling.

The centered and above position of the the picture can also be set to remain stable during scrolling using the following CSS style. The text needs to be inserted as _text_ into the screen: `text <style>.stimulus{width:100%;position:sticky;top:0;z-index:1} .stimulus img{margin-left:auto;margin-right:auto;display:block}</style>`

```
screen The stimuli placed above and centered
  stimulus IMG_4604.JPG
  text <style>.stimulus{width:100%;position:sticky;top:0;z-index:1} .stimulus img{margin-left:auto;margin-right:auto;display:block}</style>
  task Choose form of the animal
  text The picture presents an animal or its form
  values reptile, amphibian, fish, bird, mammal
```

<figure><img src="../../.gitbook/assets/1lmroyhxiw.gif" alt=""><figcaption><p>Presenting an image in the middle and above position so that it remains fixed during scrolling </p></figcaption></figure>
