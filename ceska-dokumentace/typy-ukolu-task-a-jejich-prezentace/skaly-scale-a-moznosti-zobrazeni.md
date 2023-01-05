# Škály (scale) a možnosti zobrazení

Škály zobrazí vodorovnou lištu s posuvníkem, uživatel může vybrat jednu z hodnot.

```
 	task T - celková porucha
 	   scale 0 3(0.5)
```

![Zobrazí task a posuvník s hodnotami od 0 do 3, s tím, že lze vybrat hodnoty po kroku 0.5](<../../.gitbook/assets/image (25).png>)

### Škály s popisy hodnot

Některé hodnoty ze škály lze označit slovně. za definicí škály jde po sobě `hodnota text_bez_mezer`. Text může obsahovat HTML tagy, tak lze první hodnotu podtrhnout `<u></u>`, další mít kurzívou `<i></i>` a nebo tučně `<b></b>`

```
    task R - chraplavost / drsnost    
 		scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
```

![Zobrazí task s popisy hodnot včetně HTML formátování](<../../.gitbook/assets/image (26).png>)

### Škály se zarovnáním přetékajících popisů hodnot

Pokud slovní hodnoty přetékají panel vymezený pro zobrazení tasku viz výše, lze změnit vnější odsazení škálového elementu zleva a zprava pomocí CSS stylu margin-left a margin-right takto pro všechny škály na obrazovce:`text <style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>`

```
screen per 1 RBASI a Plnost
  stimulus testyHLAS/F_MaKu/F1-ff1.wav
  text <style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>

  task G - celková porucha
	scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
   
```

![Škály se zarovnáním levé hodnoty o 10 pixelů a pravé hodnoty o 55 pixelů od okraje obdélníku tasku.](<../../.gitbook/assets/image (30).png>)

### Škály a jejich panely pod sebou

Další task se škálou se zobrazí pod první škálou v pořadí v jakém je definován.

```
screen RBASI a Plnost
    stimulus F1-ff1.wav
    text<style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>

    task R - chraplavost / drsnost
    scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
    
    task B - dyšnost
 		scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
```

![Tasky se škálama pod sebou](<../../.gitbook/assets/image (20).png>)

### Škály a jejich panely vedle sebe

Task se zobrazí v HTML jako `fieldset`. Lze upravit CSS styl tohoto elementu tak aby zabíral jen polovinu obrazovky (48%) pomocí dalšího `text <style>fieldset{width:48%;float:left;}</style>`

```
screen RBASI a Plnost
    stimulus F1-ff1.wav
    text<style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>
    text<style>fieldset{width:48%;float:left;}</style>

    task R - chraplavost / drsnost
    scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
    
    task B - dyšnost
 		scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
```

![Tasky a škály vedle sebe](<../../.gitbook/assets/image (27).png>)

### Panely a různé výšky jejich obsahu včetně škál

Někdy se stane, že výška polí pro tasky je různá od sousední a vzezření je nehezké viz další obrázek.

![](<../../.gitbook/assets/image (21).png>)

Je nutné nastavit výšku tasku pevně, např. CSS stylem `height` pro `fieldset`

```
screen RBASI a Plnost
  stimulus F1-ff1.wav
  text<style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>
  text<style>fieldset{width:48%;float:left;height:140px}</style>
  task Hodnocení stupně poruchy hlasu škál RBASI
 		text 0 - <u>norma</u>;  0.5 - <i>minimální poškození</i>;  1 - mírná;  1.5 - mírná až střední;  2 - <b>střední</b>;  2.5 - <b>stř. až těžká</b>;  3 - <b><u>velmi těžká</b></u>
  task G - celková porucha
    text pro tuto poruchu nehodnotíme
  task R - chraplavost / drsnost
    scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
  task B - dyšnost
	  scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
```

![Škály vedle sebe, výška tasku nastavena na 140 pixelů.](<../../.gitbook/assets/image (24).png>)

### Panely s různými barvami pozadí

Pro nastavení různých barev pozadí&#x20;

1. &#x20;nastavit `background:inherit` pro `fieldset`&#x20;
2. v každém tasku nastavit barvu pozadí např.: `#styleform background-color:peachpuff;`

```
screen RBASI a Plnost
  stimulus F1-ff1.wav
  text<style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>
  text<style>fieldset{width:48%;float:left;height:140px;background:inherit}</style>
  task Hodnocení stupně poruchy hlasu škál RBASI
 		text 0 - <u>norma</u>;  0.5 - <i>minimální poškození</i>;  1 - mírná;  1.5 - mírná až střední;  2 - <b>střední</b>;  2.5 - <b>stř. až těžká</b>;  3 - <b><u>velmi těžká</b></u>
  task G - celková porucha
  #styleform background-color:white; color:red
    text pro tuto poruchu nehodnotíme
  task R - chraplavost / drsnost
  #styleform background-color:peachpuff;
    scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
  task B - dyšnost
  #styleform background-color:lavenderblush;
	  scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
```

![](<../../.gitbook/assets/image (22).png>)
