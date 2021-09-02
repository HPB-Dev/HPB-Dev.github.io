[Home Page](https://dev.hpbdev.cf) **>** [docs](https://dev.hpbdev.cf/docs/base) **>** [Pacchetti](https://dev.hpbdev.cf/docs/pacchetti/index)

# Pacchetti di HPB
HPB, poichè strutturato (dalla `v1.0 build2 ALPHA`) in funzioni<br>
ha bisogno di puntare e includere una funzione tramite `use`

## `use`
`use` è una funzione di PHP che permette di selezionare una classe da molti file PHP<br>
Esempio:
```
use hpb\Sus;
```

`hpb` -> Nome del file definito con `namespace`
`Sus` -> Nome della classe selezionata (del file)

## Pacchetti di HPB
[`Main`](https://dev.hpbdev.cf/docs/pacchetti/main) -> *Include tutte le funzioni base di HPB*<br>
[`MySQL`](https://dev.hpbdev.cf/docs/pacchetti/mysql) -> *Include l'interazione con MySQL*<br>
[`Curl`](https://dev.hpbdev.cf/docs/pacchetti/curl) -> *Include l'integrazione di CUrl*<br>
[`ShellOPT`](https://dev.hpbdev.cf/docs/pacchetti/shell) -> *Include l'integrazione con Shell (Linux - Ubuntu based)*<br>
[`Apes`](https://dev.hpbdev.cf/docs/pacchetti/apes) -> *Integrazione con l'automatismo Personalized Encrypt System*

## Includere un pacchetto
Per includere un pacchetto basta selezionarlo
```php
use hpb\Main;
use hpb\MySQL;
```
E poi attivarlo
```php
$hpb = new Main();
$mysql = new MySQL();
```
