# Body ve videu (videopoint, videomultipoint)

Pokud je stimulus zobrazen jako video 'mp4',  lze použít tyto dva typy úkolů:

* `videomultipoint` zobrazí barevně odlišené tlačítko, po jeho stisknutí lze vybrat v obrázku více bodů, pravým tlačítkem se poslední bod odebere.
* `videopoint` zobrazí barevně odlišené tlačítko, po jeho stisknutí lze vybrat v obrázku bod. Pravým tlačítkem se bod odebírá

```
screen Výběr bodu ve videu
  stimulus stimuli/yamaha/clavinovapianoharmonica.mp4
  task Označte umístění rukou na klaviatuře v 1. sekundě
  videomultipoint
  task Označte v 20 sekundě použitý přepínač
  videopoint
```

![](../.gitbook/assets/firefox\_CRCaKGiPnE.gif)
