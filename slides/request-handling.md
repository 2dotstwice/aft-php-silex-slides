##  Request handling

Hello world

```php
$app->get(
    '/hello',
    function (Request $request) {
        return new Response('Hello world!');
    }
);
```

![Screenshot of /hello request](resources/hello-world.png)
