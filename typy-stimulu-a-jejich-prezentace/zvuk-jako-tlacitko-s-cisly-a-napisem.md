# Zvuk jako tlačítko s čísly a nápisem

### Jazyk nápisu na tlačítku

Stimul se zvukovým souborem zobrazí standardně tlačítko s nápisem `play`. Je možné změnit nápis na tlačítku do těchto jazykových mutací.

* `stimulus(buttoncz)` ukáže český nápis `přehrát`
* `stimulus(buttonsk)` ukáže slovenský nápis `prehrať`
* `stimulus(buttonde)` ukáže německý nápis `spielen`
* `stimulus(buttonen)` \(přednastavené chování\) ukáže anglický nápis `play`

```text
screen národní nápisy u tlačítek zvuku
  stimulus(buttoncz) 1.wav
  stimulus(buttonsk) 2.wav
  stimulus(buttonde) 3.wav
  stimulus(buttonen) 4.wav
```

![N&#xE1;rodn&#xED; n&#xE1;pisy u tla&#x10D;&#xED;tek](../.gitbook/assets/image%20%2816%29.png)

### Malé číslíčko udávající pořadí stimulu na obrazovce

U tlačítka stimulu, lze zapnout příponou `1`za klíčovým slovem `button` případně s národní mutací návěští `buttoncz` , aby se zobrazilo malé číslíčko u tlačítka udávající pořadí na obrazovce. Vygenerované číslo v žádném případě neurčuje pořadí v jakém jsou definice, neboť předchozí definicce `randomintuple` toto pořadí náhodně promíchá.

### 

```text
screen pořadové nápisy u tlačítek zvuku
  stimulus(button1) 1.wav
  stimulus(button1) 2.wav
  stimulus(button1) 3.wav
  stimulus(button1) 4.wav   
```

![Mal&#xE9; &#x10D;&#xED;sl&#xED;&#x10D;ka u tla&#x10D;&#xED;tek](../.gitbook/assets/image%20%285%29.png)

### Kombinace jazyku nápisu a číslíčka

Příklad lokalizovaná verze tlačítek s číslíčky

```text
screen pořadové nápisy u lokalizovaných tlačítek zvuku
  stimulus(buttoncz1) 1.wav
  stimulus(buttoncz1) 2.wav
  stimulus(buttoncz1) 3.wav
  stimulus(buttoncz1) 4.wav    
```

![Mal&#xE9; &#x10D;&#xED;sl&#xED;&#x10D;ka u lokalizovan&#xFD;ch tla&#x10D;&#xED;tek.](../.gitbook/assets/image%20%2817%29.png)

