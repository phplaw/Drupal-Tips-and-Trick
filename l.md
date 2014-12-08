Allthough it's described, I thoughed the drupal 6 had some good examples.

There are three styles of placeholders:

``!variable``, which indicates that the text should be inserted as-is. This is useful for inserting variables into things like e-mail.
```php
<?php
    $message = t("If you don't want to receive such e-mails, you can change your settings at !url.", array('!url' => l(t('My account'), "user/$account->uid")));
  
?>
```
``@variable``, which indicates that the text should be run through check_plain, to escape HTML characters. Use this for any output that's displayed within a Drupal page.
```php
<?php
    $title = t("@name's blog", array('@name' => $account->name));
  
?>
```
``%variable``, which indicates that the string should be HTML escaped and highlighted with theme_placeholder() which shows up by default as emphasized.
```php
<?php
    $message = t('%name-from sent %name-to an e-mail.', array('%name-from' => $user->name, '%name-to' => $account->name));
  
?>
```
