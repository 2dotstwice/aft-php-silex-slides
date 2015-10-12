##  Handling errors

```php
$app->post(
    '/login',
    function (Request $request) use ($app) {
        $username = $request->request->get('username');
        $password = $request->request->get('password');
        
        if (empty($username) || empty($password)) {
            throw new Exception(
                'Missing username and/or password.', 
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
