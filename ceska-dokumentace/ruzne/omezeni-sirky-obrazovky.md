# Omezení šířky obrazovky

Některé testy se mohou na malých nebo velkých obrazovkách zobrazit rozdílně. Je možné omezit šířku zobrazení testu globálně pomocí klíčového slova 'template' a zvolit jednu z předdefinovaných šířek

* `template fixedscreenL` nastaví šířku na 1024px, odpovídá tabletu na šířku nebo malé obrazovce.
* `template fixedscreenM` nastaví šířku na 768px, odpovídá tabletu
* `template fixedscreenS` nastaví šířku na 375px, odpovídá mobilnímu telefonu

`template` může být jen před definicí první obrazovky, jinak není brán v potaz a šířka obrazovky testu se neomezuje.

```
test demo1PomuckyEduGSheet.ptest
  template fixedscreenL
  screen První obrazovka
  ...
```

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption><p>fixedscreenL</p></figcaption></figure>

```

test demo1PomuckyEduGSheet.ptest
  template fixedscreenM
  screen První obrazovka
  ...
```

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>fixedscreenM</p></figcaption></figure>

```
test demo1PomuckyEduGSheet.ptest
  template fixedscreenS
  screen První obrazovka
  ...
```

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption><p>fixedscreenS</p></figcaption></figure>
