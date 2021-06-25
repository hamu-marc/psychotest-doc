# Styly prvků v generovaném testu

Pomocí tzv. CSS stylů lze měnit konečný vzhled vygenerovaných elementů. Pomocí speciální poznámky `#css` lze nastavit obecně CSS styl včetně selektorů, `#styleform` a `#style` nastavuje styl pro poslední formulář, nebo poslední element. Více obecně o CSS stylech viz [https://cs.wikipedia.org/wiki/Kask%C3%A1dov%C3%A9\_styly](https://cs.wikipedia.org/wiki/Kask%C3%A1dov%C3%A9_styly). Dále v textu jsou jen konkrétní příklady jak nastavit styl pro zobrazení.

### \#css

Stimuli jsou prezentovány v HTML tagu, který má třídu `stimulus`. Pomocí selektoru, lze nastavit např. pozici aby při skrolování byly vidět.

```text
#css .stimulus{position:sticky;top:0;z-index:1}
```

Více viz [Stimuli vždy na obrazovce](../typy-stimulu-a-jejich-prezentace/stimuli-vzdy-na-obrazovce.md).

### \#styleform

Task je prezentován v HTML jako element `<form>`. Definování stylu předchozím způsobem nastaví styl pro všechny form na obrazovce. Pro nastavení konkrétní - tj. jen posledního tasku lze použít speciální poznámku `#styleform`. Např. následující nastaví form plovoucí a zarovnání vlevo a pozadí na bílou barvu a text na červenou:

```text
task Hodnocení stupně poruchy hlasu škál RBASI
    #styleform float:left; width:100%; background-color:white; color:red
```

Více viz [Stimuli vždy na obrazovce](../typy-stimulu-a-jejich-prezentace/stimuli-vzdy-na-obrazovce.md).

### \#style

definuje CSS styl pro poslední vygenerovaný element







