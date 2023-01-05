# Přepínač - radio button (values)

Přepínač lze využít pro zobrazení tzv. radio buttons s jendotlivými možnostmi a uživatel vybere jen jednu z nich.

### Hodnoty pod sebe

`values` se seznamem možností oddělených mezerou (pokud hodnota má obsahovat mezeru, dejte ji do uvozovek `"`) zobrazí hodnoty pod sebou:

```
  screen Video
  stimulus pianoharmonica.mp4
  task kvalitu záznamu
  values "zvuk předbíhá video", "zvuk synchronizován s videem", "zvuk je opožděn"
```

![](<../../.gitbook/assets/image (32).png>)

### Hodnoty vedle sebe

`valuesonrow` se seznamem možností oddělených mezerou a nobe čárkou(pokud hodnota má obsahovat mezeru, dejte ji do uvozovek `"`) zobrazí se hodnoty vedle sebe:

```
screen Video 2
stimulus stimuli/yamaha/clavinovapianoharmonica.mp4
task kvalitu záznamu
valuesonrow "zvuk předbíhá video" "zvuk synchronizován s videem" "zvuk je opožděn"
```

![](../../.gitbook/assets/firefox\_xla2ba0vfl.png)
