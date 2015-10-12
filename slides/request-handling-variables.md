##  Request handling

Variable parameters in the URL

    GET http://<your-url>/hello/AFT

```php
$app->get(
    '/hello/{name}',
    function (Request $request, $name) {
        return new Response('Hello ' . $name . '!');
    }
);
```

![Screenshot of /hello/{name} request](resources/hello-name.png)
