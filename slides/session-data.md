##  Session data

Storing data

    POST http://<your-url>/login
    
```php
$app->register(new Silex\Provider\SessionServiceProvider());

$app->post(
    '/login',
    function (Request $request) use ($app) {
        $username = $request->request->get('username');
        $password = $request->request->get('password');

        if ($username == 'john.doe' && $password == 'secret') {
            $app['session']->set('username', $username);
            return new Response('Logged in.', 200);
        } else {
            return new Response('Access denied.', 403);
        }
    }
);
```
