# Seřazovací \(třídící\) úkol

`ranking2d` vytvoří seřazovací \(třídící\) úkol, který nabízí 2 dimenzionální pole, do kterého lze umístit stimuli a setřídit je dle až 2 různých veličin.

Příklad:

```text
screen Ranking2D s kontrolkami
    stimulus(controls) 1.wav
    stimulus(controls) 2.wav
    stimulus(controls) 5.wav     
  	task Serazeni velikosti
      text Seřaďte od nejmenšího po největší
  	   ranking2d hlasitost(nejmenší-největší);drsnost(žádná-střední-velká)

```

Se zobrazí jako následující obrazovka s kontrolkami pro možnost zastevení přehrávání nebo pro možnost přehrát jen část zvuku.

![Klik \(lev&#xFD;m tla&#x10D;&#xED;tkem\) na ikonu p&#x159;ehr&#xE1;v&#xE1;n&#xED; p&#x159;ehraje stimul. Stisknut&#xED; a podr&#x17E;en&#xED; p&#x159;et&#xE1;hne ikonu.](../.gitbook/assets/rlo53va1m2.gif)

Jednotlivé stimuli lze opatřit anotací \(poznámkou\), která se ve výsledcích objeví jako volitelné pole. Poznámky jsou přiřazeny ke zvukům, viz následující náhled obrazovky.

![Prav&#xE9; tla&#x10D;&#xED;tko na ikonu vyvol&#xE1; dioalog s mo&#x17E;nost&#xED; p&#x159;idat anotaci ke zvuku.](../.gitbook/assets/inogt6lzml.gif)









