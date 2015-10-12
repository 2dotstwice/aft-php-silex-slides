##  Session data

Retrieving stored data

    GET http://<your-url>/user
    
```php
$app->get(
    '/user',
    function (Request $request) use ($app) {
        $username = $app['session']->get('username');

        if (!empty($username)) {
            return new Response('Logged in as ' . $username);
        } else {
            return new Response('Not logged in.');
        }
    }
);
```
