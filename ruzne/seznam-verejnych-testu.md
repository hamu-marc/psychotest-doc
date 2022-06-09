# Seznam veřejných testů

Tento postup umožňuje modifikovat seznam veřejných testů dostupných komukoliv z adresy [https://psychoacoustic.hamu.cz/psychotest/](https://psychoacoustic.hamu.cz/psychotest/)

1. seznam testů je definován v souboru `dashboard.json`
2. Soubor je umístěn v repozitáři [https://github.com/hamu-marc/psychotest/tree/gh-pages/resources](https://github.com/hamu-marc/psychotest/tree/gh-pages/resources)
3. struktura je ve formátu JSON jako pole položek

```
[
  {
    "_id": "...generated suffix of URL beginning with N4gIg ...",
    "name": "... name to be displayed with bold font...",
    "description": "... description with normal font, HTML is allowed "
  },
  { ... }
 ]   
```

Po "Commit" úprav tohoto souboru do repozitáře GITHUB se během několika minut aktualizuje úvodní obrazovka.

![](../.gitbook/assets/firefox\_2Vk29HKBuP.gif)
