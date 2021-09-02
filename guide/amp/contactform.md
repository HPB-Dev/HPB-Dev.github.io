[Home Page](https://dev.hpbdev.cf/) **>** [Guide](https://dev.hpbdev.cf/guide/) **>** Creare un Contact Form

# HPB - Guide
## Creare un Contact Form usando HTML e HPB

Iniziamo con la parte lato client, in html.<br>
Pagina `form.html`:
```html
<form method="post" action="c.php">
    Nome:<br>
    <input type="text" name="nome"><br>
    Cognome:<br>
    <input type="text" name="cognome"><br>
    Email:<br>
    <input type="email" name="email"><br>
    Messaggio:<br>
    <textarea name="text"></textarea><br><br>
    <input type="submit" value="Invia!">
</form>
```

E ora la parte lato server in HPB<br>
Pagina `c.php`:
```php
<?php
require_once("hpb.phar");

use hpb\Main;

$hpb = new Main();

$nome = $hpb->form("nome");
$come = $hpb->form("cognome");
$email = $hpb->form("email");
$text = $hpb->form("text");

if (empty($email)) {
    $hpb->stop;
}

$string = "Messaggio da: $nome $cognome - $email\n\nMessaggio: $text";

$hpb->mail("contact@example.com", "example.mail.text@gmail.com", "Nuovo Messaggio!", $string);

$hpb->reindirizzamento("done.php", "");
