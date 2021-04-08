# Zvuk jako tlačítko

`stimulus` po kterém následuje 1 nebo více souborů s příponou`mp3` nebo `wav` se zobrazí tlačítko, které po stisknutí přehraje daný zvukový soubor.

Za klíčovým výrazem `stimulus` lze v závorce nastavit způsob zobrazení.  `stimulus(button)` zobrazí tlačítko, to je předvolené chování a nemusí se specifikovat

```text
test demo1zvuky
  screen První obrazovka
  stimulus 1.wav
```

![Zobrazen&#xED; stimulu na obrazovce jako tla&#x10D;&#xED;tko](../.gitbook/assets/image%20%286%29.png)

V hranatých závorkách za souborem lze specifikovat start a stop v milisekundách, jaká část zvukového soboru se přehraje např.`stimulus 1.wav [200,500]` přehraje část zvuku od 200 po 500 milisekund.

```text
test demo1zvuky
  screen První obrazovka
  stimulus 1.wav [200,500]
```

