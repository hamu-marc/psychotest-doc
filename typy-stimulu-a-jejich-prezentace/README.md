# Typy stimulů a jejich prezentace

Stimuli se přidávají hned za definici obrazovky `screen` pomocí klíčového slova `stimulus` po kterém následuje 1 nebo více souborů obsahující daný stimul. Typ stimulů se rozliší podle přípony souboru takto:

* `mp3` a `wav` jsou zvukové stimuli. V testovací obrazovce se zobrazí tlačítko, které po stisknutí přehraje daný soubor. Je možno zvolit místo tlačítka řídící prvky pro nastavení hlasitosti a pozice v přehrávaném souboru.
* `mp4` jsou video stimuli \(obraz se zvukem\). V testovací obrazovce se zobrazí jako rámeček a pod ním řídící tlačítka, která pouští/zastaví přehrávání videa
* `png`, `jpg` je obrázek. V testovací obrazovce se zobrazí rámeček s obrázkem

Příklad:

```text
test UkazkaStimulu
screen Hodnoceni obrazku
  stimulus stimuli/tomas/IMG_4604.JPG
  task ...
screen Hodnoceni zvuku
  stimulus 1.wav 
  stimulus 2.wav
  stimulus 5.wav 
  stimulus 7.wav
  task ...
screen Hodnoceni videa
  stimulus stimuli/yamaha/clavinovapianoharmonica.mp4
  task ...
```



