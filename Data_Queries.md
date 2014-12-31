join Query with many conditions

```php
$query->leftjoin('votingapi_cache', 'fivestar', "fivestar.entity_id = n.nid AND fivestar.function = 'average'");
```

I've seen this before, I can't remember why it's this way but you can fix it by swapping out which types of quote you use.

Changing your code to this will fix the problem:
```php
$query = db_select( 'node', 'n' )
  ->fields( 'n', array('created', 'title', 'type'));

// Change wrapping quotes to "" and internal to '' for 3rd arg here
$query->leftJoin( 'url_alias', 'ua', "ua.source = CONCAT('node/', n.nid)");

$query->addField('ua', 'alias');
$results = $query->execute();
```
