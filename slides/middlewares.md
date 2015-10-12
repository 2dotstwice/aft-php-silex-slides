##  Middlewares

Perform additional actions on each route...

```php
$app->after(function (Request $request, Response $response) {
    $response->headers->set('X-Generated-By', 'Silex');
});
```

... or on specific routes

```php
$app->get(...)
    ->after(
        function (Request $request, Response $response) {
            $response->headers->set('X-Generated-By', 'Silex');
        }
    );
```
