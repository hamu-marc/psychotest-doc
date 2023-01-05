# Zaškrtávací políčka (checkboxvalues)

Zaškrtávací políčka lze využít pro výběr více než jedné hodnoty.&#x20;

### Hodnoty pod sebou

`checkboxvalues`po němž následuje seznam možností oddělených mezerou (pokud hodnota má obsahovat mezeru, dejte ji do uvozovek `"`) zobrazí hodnoty pod sebou:

```
screen výběr z více možností
  stimulus 1.wav
  task vyberte všechny poruchy, které jsou v hlasu patrné
  checkboxvalues "vše v normě" "porucha dyšnosti" "hlasová slabost" "hlasové napětí" "chraplavost" "nestabilita"
```

![](../../.gitbook/assets/firefox\_ch2m8h2pgr.png)

### Hodnoty vedle sebe

`checkboxvaluesonrow` zobrazí hodnoty na jeden řádek vedle sebe

```
screen výběr z více možností
  stimulus 1.wav
  task vyberte poruchy, které jsou v hlasu patrné
  checkboxvaluesonrow "vše v normě" "porucha dyšnosti" "hlasová slabost" "hlasové napětí" "chraplavost" "nestabilita"
```

![](<../../.gitbook/assets/image (33) (1).png>)
