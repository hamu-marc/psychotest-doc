# Škály \(scale\) a možnosti zobrazení

Škály zobrazí vodorovnou lištu s posuvníkem, uživatel může vybrat jednu z hodnot.

```text
 	task T - celková porucha
 	   scale 0 3(0.5)
```

![Zobraz&#xED; task a posuvn&#xED;k s hodnotami od 0 do 3, s t&#xED;m, &#x17E;e lze vybrat hodnoty po kroku 0.5](../.gitbook/assets/image%20%2825%29.png)

### Škály s popisy hodnot

Některé hodnoty ze škály lze označit slovně. za definicí škály jde po sobě `hodnota text_bez_mezer`. Text může obsahovat HTML tagy, tak lze první hodnotu podtrhnout `<u></u>`, další mít kurzívou `<i></i>` a nebo tučně `<b></b>`

```text
    task R - chraplavost / drsnost    
 		scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
```

![Zobraz&#xED; task s popisy hodnot v&#x10D;etn&#x11B; HTML form&#xE1;tov&#xE1;n&#xED;](../.gitbook/assets/image%20%2826%29.png)

### Škály se zarovnáním přetékajících popisů hodnot

Pokud slovní hodnoty přetékají obdélník vymezený pro zobrazení tasku viz výše, lze změnit vnější odsazení škálového elementu zleva a zprava pomocí CSS stylu margin-left a margin-right takto pro všechny škály na obrazovce:`text <style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>`

```text
screen per 1 RBASI a Plnost
  stimulus testyHLAS/F_MaKu/F1-ff1.wav
  text <style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>

  task G - celková porucha
	scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
   
```

![&#x160;k&#xE1;ly se zarovn&#xE1;n&#xED;m lev&#xE9; hodnoty o 10 pixel&#x16F; a prav&#xE9; hodnoty o 55 pixel&#x16F; od okraje obd&#xE9;ln&#xED;ku tasku.](../.gitbook/assets/image%20%2830%29.png)

### Škály pod sebou

Další task se škálou se zobrazí pod první škálou v pořadí v jakém je definován.

```text
screen RBASI a Plnost
    stimulus F1-ff1.wav
    text<style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>

    task R - chraplavost / drsnost
    scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
    
    task B - dyšnost
 		scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
```

![Tasky se &#x161;k&#xE1;lama pod sebou](../.gitbook/assets/image%20%2820%29.png)

### Škály vedle sebe

Task se zobrazí v HTML jako `fieldset`. Lze upravit CSS styl tohoto elementu tak aby zabíral jen polovinu obrazovky \(48%\) pomocí dalšího  `text <style>fieldset{width:48%;float:left;}</style>`

```text
screen RBASI a Plnost
    stimulus F1-ff1.wav
    text<style>.ui-slider-wrapper{margin-left:10px;margin-right:55px}</style>
    text<style>fieldset{width:48%;float:left;}</style>

    task R - chraplavost / drsnost
    scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
    
    task B - dyšnost
 		scale 0 3(0.5) 0 <u>norma</u> 0.5 <i>minim.</i> 1 mírná  2 <b>střední</b> 3 <b><u>"velmi těžká"</b></u>
```

![Tasky a &#x161;k&#xE1;ly vedle sebe](../.gitbook/assets/image%20%2827%29.png)

### Škály a různé výšky pole pro task

Někdy se stane, že výška polí pro tasky je různá od sousední a vzezření je nehezké viz další obrázek.

![](../.gitbook/assets/image%20%2821%29.png)

Je nutné nastavit výšku tasku pevně, např. CSS stylem `height` pro `fieldset`

```text
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

![&#x160;k&#xE1;ly vedle sebe, v&#xFD;&#x161;ka tasku nastavena na 140 pixel&#x16F;.](../.gitbook/assets/image%20%2824%29.png)

### Škály s různými barvami pozadí

Pro nastavení různých barev pozadí 

1.  nastavit `background:inherit` pro `fieldset` 
2. v každém tasku nastavit barvu pozadí např.: `#styleform background-color:peachpuff;`

```text
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

![](../.gitbook/assets/image%20%2822%29.png)

