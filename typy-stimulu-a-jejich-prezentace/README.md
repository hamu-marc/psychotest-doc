# Typy stimulů a jejich prezentace

Stimuli se přidávají hned za definici obrazovky `screen` pomocí klíčového slova `stimulus` po kterém následuje 1 nebo více souborů obsahující daný stimul. Typ stimulů se rozliší podle přípony souboru takto:

* `mp3` a `wav` jsou zvukové stimuli. V testovací obrazovce se zobrazí tlačítko, které po stisknutí přehraje daný soubor.
  *  `stimulus(controls) 1.wav` zobrazí místo tlačítka řídící prvky pro nastavení hlasitosti a pozice v přehrávaném souboru. 
  * `stimulus(waveform) 1.wav` zobrazí místo tlačítka zvukový signál a řídící prvky pro nastavení hlasitosti a pozice v přehrávaném souboru. 
  * V hranatých závorkách za souborem lze specifikovat start a stop v milisekundách, jaká část zvukového soboru se přehraje`stimulus 1.wav [200,500]`. 
* `mp4` jsou video stimuli \(obraz se zvukem\). V testovací obrazovce se zobrazí jako rámeček a pod ním řídící tlačítka, která pouští/zastaví přehrávání videa
* `png`, `jpg` je obrázek. V testovací obrazovce se zobrazí rámeček s obrázkem

Příklad:

```text
test UkazkaStimulu
screen Hodnoceni obrazku
  stimulus stimuli/tomas/IMG_4604.JPG
  task ...
screen Hodnoceni zvuku
  stimulus(waveform) 1.wav 
  stimulus(controls) 2.wav
  stimulus 5.wav 
  stimulus 7.wav [200,500] 
  task ...
screen Hodnoceni videa
  stimulus stimuli/yamaha/clavinovapianoharmonica.mp4
  task ...
```



