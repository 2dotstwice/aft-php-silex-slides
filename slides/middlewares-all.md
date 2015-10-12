##  Available middlewares

```php
$app->before(
    function (Request $request) {
        // Modify $request before it is handled...
    }
);
```

```php
$app->after(
    function (Request $request, Response $response) {
        // Modify $response before it is sent back... 
    }
);
```

```php
$app->finish(
    function (Request $request, Response $response) {
        // Additional actions such as logging...
        // Changes to $request or $response will be ignored here.
    }
);
```
