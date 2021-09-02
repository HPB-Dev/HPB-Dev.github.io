[Home Page](https://dev.hpbdev.cf/) **>** [docs](https://dev.hpbdev.cf/docs/base) **>** Sintassi di PHP

# HPB - Sintassi di PHP
HPB è basato su PHP quindi la sintassi è la stessa.
In questa pagina della documentazione vi spiego bene la Sintassi di PHP

## Definire uno script PHP
Il file va aperto così
```php
<?php
```
E chiuso così 
```php
?>
```

```markdown
RICORDA!
Se nel file non sono presenti elementi HTML puoi anche non chiudere il file con ?>
```

## Definire una variabile con PHP
Per definire una variabile con PHP basta fare
```php
$variabile = "Mamma";
```
Stessa cosa per Definire un numero (intero)
```php
$variabile = 12345;
```
Per i decimali e quelli con tanti 0 bisogna provvedere a trattarli come stringhe
```php
$variabile = "12,594";
$variabiledue = "000000000397";
```

## Commenti
In PHP si possono inserire i commenti nei file.<br>
Commento singolo:
```php
// Commento di una riga
```
Commento multiplo:
```php
/*
Questo è
Un bellissimo
Commento multi linea
*/
```

## Definire il tipo delle Variabili
PHP non ha bisogno che venga definito il tipo delle variabili come su java `int ciao` (Intero)<br>
ma basta utilizzare i simboli
```php
// Stringa:
$var = 'CIAONE';
// Intero:
$var = 1234;
// Decimale:
$var = '1,1234';
```

## Fusione delle Variabili
In PHP è possibile includere più variabili in una variabile
```php
$nome = 'Marco';
$anni = 15;
$cibo = 'pizza';

$text = "$nome ha $anni anni e gli piace la $cibo";
```
Risultato: `Marco ha 15 anni e gli piace la pizza`<br>
Come avrai notato non ho utilizzato `'` ma le `"` per Definire Definire variabile `$text`<br>
Questo è perchè le variabili definite con `"` possono contenere altre variabili.<br>
Ecco come sarebbe stato il codice usando solo `'`:
```php
$nome = 'Marco';
$anni = 15;
$cibo = 'pizza';

$text = $nome . ' ha ' .$anni . ' anni e gli piace la ' . $cibo;
```
Come avrai notato è molto più scomodo!


## ;
In PHP ogni stringa (tranne i commenti) va conclusa con `;`:
```php
// Corretto
$php = "PHP è bello";
$sus = 1234;
// Errato
$php = "PHP è bello"
$sus = 1234
```

## Condizioni
### if ed else
`if`, tradotto in italiano `se` è l'operazione base di PHP
```
$nome = 'Marco';

if ($nome === 'Marco') {
   echo "Ciao $nome!";
} else {
   echo 'Non ti conosco!';
}
```
Analizziamo:<br>
`if` Inizia l'istruzione se <br>
`( )` Le condizioni devono stare dentro delle parentesi<br>
`$nome` Parametro 1 della condizione<br>
`'Marco'` Parametro 2 della condizione (ha le `'` poichè è una stringa)<br>
`===` Operatore (`===` è case sensitive quindi distingue maiuscole dalle minuscole)
`else` Istruziobi da fare se l'`if` si risulta falso

## Operatori
`==` Uguale<br>
`===` Uguale (case sensitive)<br>
`<` Minore<br>
`>` Maggiore<br>
`>=` Maggiore o uguale<br>
`<=` Minore o uguale


Sei pronto per programmare in HPB!<br>
Dai uno sguardo a [questa](https://dev.hpbdev.cf/docs/Funzioni) wiki per iniziare!



