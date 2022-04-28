# Edukační mód pro obrázek

V definici testu lze zvolit možnost aby se při zobrazení stimulu zobrazili i body, které odpovídají vyplněnému úkolu. Za stimul mezi `{ .... }` hodnoty jsou oddělené `|` x,y jsou oddelené `:` a  v případě většího počtu bodů v rámci jedné barvy lze oddělit lomítkem  `/`&#x20;

```
  screen Výběr bodu na obrázku
  stimulus stimuli/tomas/IMG_4687.JPG {44.24:37.04|21.50:53.10|59.22:66.98/59.22:53.04}
  task Označte oko
  imagepoint
  task Označte zobák
  imagepoint
  task Vyznačte nohy
  imagemultipoint
```

![](<../.gitbook/assets/image (37).png>)
