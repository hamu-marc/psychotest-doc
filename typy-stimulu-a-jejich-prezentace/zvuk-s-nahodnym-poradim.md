# Zvuk s náhodným pořadím

Pořadí zvuků na tlačítkách je určeno pořadím v definici testu. Je ale možné zamíchat pořadím zvuků definovaným na řádku pomocí klíčového slova `randomstimuli` a `randomintuple` .

## Náhodné pořadí zvuků ve skupině \(na řádku\)

Pomocí `randomintuple` buď na začátku definice testu nebo v rámci obrazovky po definici stimulu a tasku je možné určit, že soubory v rámci jednoho řádku stimulu je možno náhodně zamíchat.

```text
  test CiselneStimuli
    randomintuple
  screen Více stimulů náhodně na řádku
    stimulus 1.wav 2.wav 5.wav 7.wav
```

`randomintuple` na začátku testu nastaví, že všechny následující obrazovky budou promíchávat stimuli definované na jednom řádku. Test se zobrazí uživateli takto:

![Ka&#x17E;d&#xFD; stimul m&#xE1; jedno tla&#x10D;&#xED;tko, nicm&#xE9;n&#x11B; prvn&#xED; tla&#x10D;&#xED;tko m&#xE1; 25% pravd&#x11B;podobnost, &#x17E;e p&#x159;ehraje 1.wav](../.gitbook/assets/image%20%289%29.png)

`randomintuple` v průběhu testu způsobí, že tato a všechny následující obrazovky budou mít náhodné pořadí stimulů na řádků. Uveďte randomintuple na konci definice obrazovky.

```text
  screen Více stimulů náhodně na řádku
    stimulus 1.wav 2.wav 5.wav 7.wav
    randomintuple
```

{% hint style="info" %}
Pozor, pořadí stimulů definované pomocí více řádků není tímto přepínačem dotknuto proto následující test zobrazí tlačítka a pustí stimuli v pořadí jak jsou v testu.
{% endhint %}

```text
  test CiselneStimuli
    randomintuple
  screen Více stimulů ne náhodně
    stimulus 1.wav 
    stimulus 2.wav 
    stimulus 5.wav 
    stimulus 7.wav
```

![Tla&#x10D;&#xED;tka pou&#x161;t&#xED; zvuky v po&#x159;ad&#xED; 1.wav, 2.wav, 5.wav, 7.wav](../.gitbook/assets/image%20%2811%29.png)

Je tedy možné vytvořit 2 skupiny, v každé skupině se pořadí zamíchá ale skupiny se navzájem nepromíchájí náhodně.

```text
  screen Více stimulů, náhodně sloupce (12) (57)
    stimulus 1.wav 2.wav 
    stimulus 5.wav 7.wav    
    randomintuple
```

![V prvn&#xED;m sloupci tla&#x10D;&#xED;tka p&#x159;ehraj&#xED; zvuky 1 a 2 po&#x159;ad&#xED; n&#xE1;hodn&#xE9;, druh&#xFD; sloupce obdobn&#x11B; pro zvuky 5 a 7](../.gitbook/assets/image%20%2814%29.png)

```text

TODO
### Náhodné pořadí stimulů v rámci obrazovky

`randomstimuli` nastaví, že se řádky obsahující definici stimulů promíchají v rámci obrazovky náhodně.

```text
  test CiselneStimuli
    randomstimuli
  screen Více stimulů náhodně
    stimulus 1.wav 
    stimulus 2.wav 
    stimulus 5.wav 
    stimulus 7.wav
```
```

