[Home Page](https://dev.hpbdev.cf) **>** [docs](https://dev.hpbdev.cf/docs/base) **>**  [Integrazione](https://dev.hpbdev.cf/docs/Int)

# Includere HPB

HPB è un file PHP che va aggiunto alla pagina con require (include è sconsigliato)

```php
require_once("hpb.php");
```

Poi, essendo un insieme di classi bisogna decidere la libreria base.

```
use hpb\Main;
```

E infine bisogna avviare la classe
```
$hpb = new Main();
```

Ora per eseguire ogni funzione basterà fare:

```php
$hpb->funzione();
```

La stessa cosa per recuperare un valore da una funzione

```php
$lol = $hpb->funzione();
```
