##  Handling errors

```php
$app->get(
    '/search',
    function (Request $request) {
        $filter = $request->query->get('name');
        if (empty($filter)) {
            throw new Exception(
                'Please provide a name to filter on.',
                400
            );
        }
        
        // ...
    }
);
```

```php
$app->error(
    function (Exception $e) {
        return new Response($e->getMessage(), $e->getCode());
    }
);
```
