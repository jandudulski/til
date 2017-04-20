# Outdated Flash plugin

For some reasons Firefox could get stuck into old flash plugin after upgrade and raising popup that flash has been blocked because of security issues.

When you're sure that plugin has been upgraded you can close Firefox and remove plugin registry to force Firefox to rebuild it from scratch on next startup:

```
λ rm ~/.mozilla/firefox/[hash].default/pluginreg.dat
```
