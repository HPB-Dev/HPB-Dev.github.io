[Home Page](https://dev.hpbdev.cf/) **>** Installazione

# HPB - Come installare HPB

## Linux
Per installare **HPB** su Linux basta scaricare l'utima build [da questo link](https://github.com/HPB-Dev/hpb/releases)<br>
Se non installato, inastalla `zip` con `apt install zip`(ubuntu) oppure `yum -y install zip` e decomprimi il file con<br>
```shell
unzip hpb-latest.zip
```
e copia  la cartella `hpb` nella web directory dove vuoi installare HPB<br>
Per esempio, se il sito web è in `/var/www/html/` allora la cartella HPB va messa in `/var/www/html/hpb/`<br>
e l'autoloader (`autoload.php`) in `/var/www/html/autoload.php`

## Windows
Per installare **HPB** su Windows basta scaricare l'utima build [da questo link](https://github.com/HPB-Dev/hpb/releases)<br>
Decomprimi la cartella hpb-latest.zip<br>
e copia  la cartella `hpb` nella web directory dove vuoi installare HPB<br>
Per esempio, se il sito web è in `C:\Web\html\` allora la cartella HPB va messa in `C:\Web\html\hpb\`<br>
e l'autoloader (`autoload.php`) in `C:\Web\html\autoload.php`

## MacOS
`Work in progress..`



Poi includere le [classi](https://dev.hpbdev.cf/docs/Pacchetti) basta fare così:
```php
<?php
require_once("autoload.php");

use hpb\Main;
use hpb\MySQL;

$hpb = new Main();
$mysql = new MySQL();

$hpb->info();
```

Vai alla documentazione:
### [Documentazione](https://dev.hpbdev.cf/docs/base)
