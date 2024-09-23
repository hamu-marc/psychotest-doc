# Limiting the screen width

Some tests have a different appearance on small and large screens. The width of the screen can therefore be constrained using a 'template' keyword and selecting one of the defined widths.

* `template fixedscreenL` limits the width to 1024px, this best corresponds to tablet or small screen.
* `template fixedscreenM` limits the width to 768px, this corresponds to a tablet
* `template fixedscreenS` limits the width to 375px, this corresponds to a mobile phone.

`template` has to be used prior to defining the first screen or else it will not be accounted for and the test size will correspond to the actual sceen size.

```
test demo1PomuckyEduGSheet.ptest
  template fixedscreenL
  screen First screen
  ...
```

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption><p>Fixed screen L</p></figcaption></figure>

```

test demo1PomuckyEduGSheet.ptest
  template fixedscreenM
  screen First screen
  ...
```

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Fixed screen M</p></figcaption></figure>

```
test demo1PomuckyEduGSheet.ptest
  template fixedscreenS
  screen First screen
  ...
```

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption><p>Fixed screen S</p></figcaption></figure>
