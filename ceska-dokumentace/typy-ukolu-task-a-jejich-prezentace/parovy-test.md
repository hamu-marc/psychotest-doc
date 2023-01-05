# Párový test

Párový test vygeneruje pro sadu stimulů páry, které se prezentují na obrazovce a pro každý pár se prezentují stejné úkoly na obrazovce.

```
screen per 2
  stimulus 1.wav
  stimulus 2.wav
  stimulus 5.wav
  task hlasitejsi
  values 1 2
  taskforstimuli plnost
  values 0 1 2 3 4 5
```

Předchozí definice pro 3 stimuli vygeneruje celkem obrazovky s páry&#x20;

* 1.wav,2.wav
* 1.wav,5.wav
* 2.wav,5.wav

a společný úkol (task). Pro každý z páru je pak vlastní úkol (taskforstimuli) prezentován v sloupečku vlevo nebo vpravo.

![](<../../.gitbook/assets/image (36).png>)
