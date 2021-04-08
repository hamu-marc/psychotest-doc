# Zvuk jako tlačítko

`stimulus` po kterém následuje 1 nebo více souborů s příponou`mp3` nebo `wav` se zobrazí tlačítko, které po stisknutí přehraje daný zvukový soubor.

Za klíčovým výrazem `stimulus` lze v závorce nastavit způsob zobrazení.  `stimulus(button)` zobrazí tlačítko, to je předvolené chování a nemusí se specifikovat

```text
test demo1zvuky
  screen První obrazovka
  stimulus 1.wav
```

![Zobrazen&#xED; stimulu na obrazovce jako tla&#x10D;&#xED;tko](../.gitbook/assets/image%20%286%29.png)

### Přehrání jen části zvuku

V hranatých závorkách za souborem lze specifikovat start a stop v milisekundách, jaká část zvukového soboru se přehraje např.`stimulus 1.wav [200,500]` přehraje část zvuku od 200 po 500 milisekund.

```text
test demo1zvuky
  screen První obrazovka
  stimulus 1.wav [200,500]
```

### Přehrání více zvuků na stránce

pokud následuje na 1 řádku více souborů se zvuky, pak se zobrazí více tlačítek se zvuky. Pokud není definované jinak, pak v pořadí v jakém se vyskytují v definici testu.

```text
screen Zvuky na radku
  stimulus 1.wav 2.wav
```

![V&#xED;ce stimul&#x16F; na jednom &#x159;&#xE1;dku se zobraz&#xED; jako tla&#x10D;&#xED;tka ve sloupci, prvn&#xED; tla&#x10D;&#xED;tko p&#x159;ehraje 1.wav, druh&#xE9; 2.wav](../.gitbook/assets/image%20%2812%29.png)



```text
screen Zvuky na vice radkach
  stimulus 1.wav 
  stimulus 2.wav
```

![Stimuli postupn&#x11B; se zobraz&#xED; jako tla&#x10D;&#xED;tka vedle sebe, prvn&#xED; tla&#x10D;&#xED;tko p&#x159;ehraje 1.wav, druh&#xE9; p&#x159;ehraje 2.wav](../.gitbook/assets/image%20%2813%29.png)

