# Zvuk jako tlačítko

`stimulus` po kterém následuje 1 nebo více souborů s příponou`mp3` nebo `wav` se zobrazí tlačítko, které po stisknutí přehraje daný zvukový soubor.

Za klíčovým výrazem `stimulus` lze v závorce nastavit způsob zobrazení.  `stimulus(button)` zobrazí tlačítko, to je předvolené chování a nemusí se specifikovat

```
test demo1zvuky
  screen První obrazovka
  stimulus 1.wav
```

<div align="center">

<img src="../../.gitbook/assets/image (6) (1).png" alt="Zobrazení stimulu na obrazovce jako tlačítko">

</div>

### Přehrání jen části zvuku

V hranatých závorkách za souborem lze specifikovat start a stop v milisekundách, jaká část zvukového soboru se přehraje např.`stimulus 1.wav [200,500]` přehraje část zvuku od 200 po 500 milisekund.

```
test demo1zvuky
  screen První obrazovka
  stimulus 1.wav [200,500]
```

### Přehrání více zvuků na stránce

pokud následuje na 1 řádku více souborů se zvuky, pak se zobrazí více tlačítek se zvuky. Pokud není definované jinak, pak v pořadí v jakém se vyskytují v definici testu.

```
screen Zvuky na radku
  stimulus 1.wav 2.wav
```

![Více stimulů na jednom řádku se zobrazí jako tlačítka ve sloupci, první tlačítko přehraje 1.wav, druhé 2.wav](<../../.gitbook/assets/image (12).png>)



```
screen Zvuky na vice radkach
  stimulus 1.wav 
  stimulus 2.wav
```

![Stimuli postupně se zobrazí jako tlačítka vedle sebe, první tlačítko přehraje 1.wav, druhé přehraje 2.wav](<../../.gitbook/assets/image (13).png>)
