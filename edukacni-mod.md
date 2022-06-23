# Edukační mód

V definici testu lze zvolit tzv. edukační mód, který na začátku nahraje vzorové hodnoty pro úkoly (tasky) a pak je uživateli zobrazí v průběhu testu. Těsně za prvním řádkem definice testu musí následovat:

`type educational [soubor se vzorem vysledku]`

Poté následuje běžná definice obrazovek např:

```
test demo9.edu.ptest
type educational demo9.edu.ptest..2022-06-23T07-49-45.432Z.presult
  screen First Screen Description
  stimulus 1.wav
  task G - celková porucha
	scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
  task R - chraplavost / drsnost    
 		scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
  task diagnóza
  values "mírná porucha se střední drsností","norma","střední celková porucha s mírnou drsností","střední celková porucha s těžkou drsností"
```

Při vykonávání testu se při stisknutí tlačítka Next nebo Finish zobrazí v tzv. edukačním módu vzorové výsledky, na škále se objeví v zelené barvě, ve výčtu se zobrazí zvýrazněné zelenou barvou, viz obrázek.

![](.gitbook/assets/firefox\_yMll0glZSf.png)
