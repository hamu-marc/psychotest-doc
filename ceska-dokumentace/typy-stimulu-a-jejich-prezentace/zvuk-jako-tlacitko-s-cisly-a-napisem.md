# Zvuk jako tlačítko s čísly a nápisem

### Jazyk nápisu na tlačítku

Stimul se zvukovým souborem zobrazí standardně tlačítko s nápisem `play`. Je možné změnit nápis na tlačítku do těchto jazykových mutací.

* `stimulus(buttoncz)` ukáže český nápis `přehrát`
* `stimulus(buttonsk)` ukáže slovenský nápis `prehrať`
* `stimulus(buttonde)` ukáže německý nápis `spielen`
* `stimulus(buttonen)` (přednastavené chování) ukáže anglický nápis `play`

```
screen národní nápisy u tlačítek zvuku
  stimulus(buttoncz) 1.wav
  stimulus(buttonsk) 2.wav
  stimulus(buttonde) 3.wav
  stimulus(buttonen) 4.wav
```

![Národní nápisy u tlačítek](<../../.gitbook/assets/image (16).png>)

### Malé číslíčko udávající pořadí stimulu na obrazovce

U tlačítka stimulu, lze zapnout příponou `1`za klíčovým slovem `button` případně s národní mutací návěští `buttoncz` , aby se zobrazilo malé číslíčko u tlačítka udávající pořadí na obrazovce. Vygenerované číslo v žádném případě neurčuje pořadí v jakém jsou definice, neboť předchozí definicce `randomintuple` toto pořadí náhodně promíchá.

###

```
screen pořadové nápisy u tlačítek zvuku
  stimulus(button1) 1.wav
  stimulus(button1) 2.wav
  stimulus(button1) 3.wav
  stimulus(button1) 4.wav   
```

![Malé číslíčka u tlačítek](<../../.gitbook/assets/image (5).png>)

### Kombinace jazyku nápisu a číslíčka

Příklad lokalizovaná verze tlačítek s číslíčky

```
screen pořadové nápisy u lokalizovaných tlačítek zvuku
  stimulus(buttoncz1) 1.wav
  stimulus(buttoncz1) 2.wav
  stimulus(buttoncz1) 3.wav
  stimulus(buttoncz1) 4.wav    
```

![Malé číslíčka u lokalizovaných tlačítek.](<../../.gitbook/assets/image (17).png>)
