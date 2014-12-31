Preprocessing Fields From A Module In Drupal 7
=========
If you're looking to preprocess a field in Drupal 7, you can use hook_preprocess_HOOK. The first "hook" is the name of your module. The second "HOOK" is the theme hook you want to preprocess (e.g. theme_node, theme_block, theme_link, theme_field). You can fine an exhustive list of the Drupal theme hooks by searching the Drupal API.
Here is a simple example of how to use it with fields.
```php
function mymodule_preprocess_field(&$variables) {
   if ($variables['element']['#field_name'] == 'field_myfield') {
   // do something
   }
}
```
Voila! Now you have access to preprocess fields... even ones you didn't create.
A quick tip: In order to preprocess a single field, use a conditional statement to check the "#field_name".
