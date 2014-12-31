join Query with many conditions

```php
$query->leftjoin('votingapi_cache', 'fivestar', "fivestar.entity_id = n.nid AND fivestar.function = 'average'");
```
