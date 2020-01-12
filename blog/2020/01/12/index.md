---
title: Useful daily bash/zsh command: avoid retype when sudoing
---
# Useful daily bash/zsh command: avoid retype when sudoing

To sell an often useless product, the advertising companies rely on distressing 
scenarios in which people find it difficult to complete certain tasks.

In a gloomy climate, a housewife tries to sweep in the most remote corners
of her kitchen, but her broom doesn't get through. The next scene is pure
frustration, with the desperate housewife launching herself into invectives 
of anger. But no problem, with the product "xy" this task is very easy, 
it follows demonstration and affordable price.

In the same way, I take the liberty of offering you this command which 
will make your life a wonder. All at a zero price.


```
carlo@raspberry:~ $ shutdown -h now
Failed to set wall message, ignoring: Interactive authentication required.
Failed to power off system via logind: Interactive authentication required.
Failed to open /dev/initctl: Permesso negato
Failed to talk to init daemon.
```

Avoid retyping all the command!

```
sudo !!
```

