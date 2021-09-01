[Home Page](https://hpbdev.cf) **>** [docs](https://hpbdev.cs/docs/base) **>** [Funzioni](https://hpbdev.cf/docs/Funzioni)<br>


# HPB - Wiki

## Lista delle Funzioni
`Lista aggiornata per la versione v1.0 build2`


## Innovazione della build2
Dalla `v1.0 build2` le funzioni di HPB saranno in una classe.<br>
Per saperne di più leggi [questa pagina](https://hpbdev.cf/docs/Int)

## ATTENZIONE!
Ricordiamo che tutte le funzioni di HPB danno come risultato un `return` quindi per recuperare un risultato basterà impostare così il codice:<br>
Guardiamo!
```php
$codificato = codifica("ciao");
echo $codificato;
```
Come si può vedere si possono assegnare alla funzione *codifica* più variabili
#### Funzioni contrassegnate con `*`
Tutte le funzioni contrassegnate con `*` rilasciano 2 tipi di output sottoforma di `boolean`<br>
Ecco quali possono essere gli output:<br>
`true`: In caso sia vero<br>
`false`: In caso non sia vero<br>
Ecco alcuni esempi
```php
// Ora utilizzeremo la funzione uguale e recupereremo l'output
$chedire = uguale("banana", "ananas");
// Ora operiamo sulla funzione uguale
// Usiamo la variabile $uguale che sarà uguale a "non trovato" perchè banana non è uguale ad ananas
if ($uguale == true) {
   // Dopo questo commento bisogna inserire quello che bisogna fare se la funzione uguale è vera
   echo "Verooooo";
} else {
   // Dopo questo commento bisogna inserire quello che bisogna fare se la funzione uguale è falsa
   echo "Falsooooo";
}
```

***



### Funzione **`crea`**
La funzione `crea` crea una cartella nella directory desiderata<br>
Sintassi:
```php
// >> CREA <<
// Sintassi Universale
crea(<nome della cartella + directory (../test oppure ciao/test)>, <permessi (come 0777)>);
// In questo caso creiamo una cartella o in ../test oppure in ciao/test con i permessi a 0777

// Applicazione
// Metodo 1
crea("test", "0777");
```


### Funzione **`scrivi`**
La funzione `scrivi` crea un file nella directory desiderata<br>
Sintassi:
```php
// >> SCRIVI <<
// Sintassi Universale
scrivi(<nome del file + directory>, <il contenuto del file>, <metodo di apertura. usa "w+" per eliminare il testo precedente e invece "a+" per andare a capo senza eliminare niente);

// Applicazione
// Metodo 1
scrivi("test.txt", "Ciao il mio primo file!", "a+");
```


### Funzione **`leggi`** `**`
La funzione `leggi` legge un file nella directory desiderata<br>
Sintassi:
```php
// >> LEGGI <<
// Sintassi Universale
$lettore = leggi(<nome file + directory>); ;
// In questo caso leggiamo un file e salviamo il contenuto nella variabile $lettore. Per annunciarlo facciamo echo $lettore

// Applicazione
// Metodo 1
$lettore = leggi("test");
```


### Funzione **`vuoto`** `*`
La funzione `vuoto` verifica che una variabile non sia vuota
Sintassi:
```php
// >> VUOTO <<
// Sintassi Universale
$vuoto = vuoto(<variabile>);
// In questo caso verifichiamo che una variabile non sia vuota

// Applicazione
// Metodo 1
$vuoto = vuoto($var);
```

### Funzione **`codifica`** e **`decodifica`**

#### Funzione `codifica`
La funzione `codifica` codifica una variabile<br>
Sintassi:
```php
// >> CODIFICA <<
// Sintassi Universale
$codificato = codifica(<variabile o testo da codificare>);

// Applicazione
// Metodo 1
$codificato = codifica("Ciao!");
```

#### Funzione `decodifica`
La funzione `decodifica` decodifica una variabile<br>
Sintassi:
```php
// >> DECODIFICAA <<
// Sintassi Universale
$decodificato = decodifica(<variabile o testo>);

// Applicazione
// Metodo 1
$decodificato = decodifica("AJS7SOAH=");
```

### Funzione **`shell`**
La funzione `shell` invia un comando shell al server<br>
Sintassi:
```php
// >> SHELL <<
// Sintassi Universale
shell(<comando>);

// Applicazione
// Metodo 1
shell("chmod 770 start.sh");
```

### Funzione **`sostituisci`** `**`
La funzione `sostituisci` sostituisce un carattere con uno a scelta<br>
Sintassi:
```php
// >> SOSTITUISCI <<
// Sintassi Universale
$sost = sostituisci(<carattere da sostituire>, <carattere che sostituirà il carattere a sostituire>, <variabile o testo>);

// Applicazione
// Metodo 1
$sost = sostituisci("a", "9", "Ciao a tutti!")
// Output: Ci9o 9 tutti!
// Come si può notare ha sostituito la lettera a al numero 9
```

### Funzione **`reindirizzamento`**
La funzione `reindirizzamento` reindirizza l'utente all'url indicato con il ritardo indicato<br>
Sintassi:
```php
// >> REINDIRIZZAMENTO <<
// Sintassi Universale
reindirizzamento(<url dove reindirizzare l'utente>, <ritardo in secondi>);

// Applicazione
// Metodo 1
reindirizzamento("https://fcosma.it/HPB/en-us/", "5");
// In questo caso vengo reindirizzato alla pagina http://foxcode.ml/code/reindirizzato con 5 secondi di ritardo
// Se lasciassi vuoto il campo quindi function reindirizzamento("http://foxcode.ml/code/reindirizzato"); mi reindirizzerebbe immediatamente
```



### Funzione **`esiste`** `*`
La funzione `esiste` verifica che un file oppure una cartella esista<br>
Sintassi:
```php
// >> ESISTE <<
// Sintassi Universale
$esiste = esiste(<nome del file o della cartella includendo la directory>);

// Applicazione
// Metodo 1
$esiste = esiste("../../naopleone/bonaparte/test.txt");
```

### Funzione **`form`** `**`
La funzione `form` recupera un dato da un form **html**<br>
Sintassi:
```php
// >> FORM <<
// Sintassi Universale
$form = form(<nome del form>);

// Applicazione
// Metodo 1
$form = form("nome");
```

### Funzione **`url`**
La funzione `url` recupera una variabile presente nell'URL<br>
Esempio: `https://example.com/esempio/test?ciao=01`<br>
In questo caso questa funzione se noi inseriamo ciao ci tornerà come esito 01 perchè nell'url la variabile `ciao` è definita a `01`<br>
Sintassi:
```php
// >> URL <<
// Sintassi Universale
$url = url(<nome della variabile, nel caso dell'esempio "ciao">);

// Applicazione
// Metodo 1
// ..
// Supponiamo che l'url sia https://giancarlo.com/test?ciao=ciao
$url = url("ciao");
// Output: ciao perchè nell'url è definito ciao=ciao
```

### Funzione `json-codificatore` `*`
La funzione `json-codificatore` codifica un `array` in `json`
Esempio: `{"lol":"ciao","beh":"lol"}`
Sintassi:
```php
// >> JSON CODIFICATORE <<
$formatted_json = json_codificatore(<variabile o testo>);

// Applicazione
// Metodo 1
// ..
$codificare = array("ciao","ciao2");
$codificato = json_codificatore($codificare);
```

### Funzione `json-decodificatore` `*`
La funzione `json-decodificatore` decodifica in un `array` un testo `json`
Esempio: `[1] => "lol2",
         [2] => "lol3"`
Sintassi:
```php
// >> JSON DECODIFICATORE <<
$output = json_decodificatore(<variabile, testo o file>);
// Applicazione
// ..
$decodificato = json_decodificatore("json-text.txt");
```

### Funzione `sessioni` `*`
Le funzioni `sessioni` permettono di gestire le sessioni di PHP
Sintassi:
```php
// >> SESSIONI <<
sessione(); // Inizializzo la funzione delle sessioni
sessione_definisci(<nome della sessione>,<contenuto>); // Definisco il contenuto di una sessione
$sessione = sessione_recupera(<nome della sessione>); // Recupero il valore di una sessione
sessione_distruggi(); // Distrugge tutte le sessioni
```
