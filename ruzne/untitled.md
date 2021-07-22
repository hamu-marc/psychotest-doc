# Umístění testů a stimulů

Definice testu je umístěna v datovém uložišti. Stimuli, na které test odkazuje jsou umístěny buď ve stejném uložišti jako definice testu, nebo lze jejich umístění předefinovat klíčovým slovem `base` a přesměrovat načítání stimulů z jiného např. sdíleného zdroje.

Např. `base https://filedn.com/lHGc7w3H4jOpIe46u1nPt57/Psychotest/stimuli` nastaví, že všechny stimuli na dalších obrazovkách se načítají z tohoto uložiště. Tj. stimul `1.wav` se načte z adresy `https://filedn.com/lHGc7w3H4jOpIe46u1nPt57/Psychotest/stimuli/1.wav`

Následuje příklad testu s definovaným `base` odkazujícím na jinou adresu.

```text
test demo4Base.ptest
base https://filedn.com/lHGc7w3H4jOpIe46u1nPt57/Psychotest/stimuli
screen Uvod
text Na nasledujicich obrazovkach se prehraji zvuky z jineho uložiště
screen per 1 stimul nahoře 
  stimulus(buttoncz1) 1.wav
  stimulus(buttoncz1) 2.wav
  stimulus(buttoncz1) 3.wav
  stimulus(buttoncz1) 5.wav
  stimulus(buttoncz1) 6.wav
  stimulus(buttoncz1) 7.wav
  #css.stimulus{position:sticky;top:0;z-index:1}
  
  text Po stlačení tlačítka <b>play</b> se spustí nahrávka hlasu.
    text Ohodnoťte ji v následujících vlastnostech, případně dopište významné projevy patologie hlasu do Poznámky.

    task G - celková porucha
    #styleform float:left; width:48%; background-color:lavenderblush;
 		scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>

```

{% hint style="info" %}
Adresa zkombinovaná jako `base/stimul` musí vrátit obsah souboru. Ověřte si např. v prohlížeči, jestli odkaz base/stimul vyvolá přehrání zvuku nebo stažení souboru. Pokud se zobrazí interaktivní formulář, kde uživatel opět musí kliknout na další tlačítko pro stažení souboru, pak taková kombinace base/stimul pravděpodobně nebude v testu fungovat a stimul se po kliknutí tlačítka nepřehraje.
{% endhint %}

