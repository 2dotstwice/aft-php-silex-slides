## Request handling 

Query parameters

    GET http://<your-url>/search?name=...

```php
$app->get('/search', function (Request $request) {
    $filter = $request->query->get('name');
    $names = ['Bill Gates', 'Steve Jobs', 'Steve Wozniak'];
    
    $matches = [];
    foreach ($names as $name) {
        if (stripos($name, $filter) !== false) {
            $matches[] = $name;
        }
    }

    return new Response(
        count($matches) . ' result(s): ' . implode(', ', $matches)
    );
});
```
