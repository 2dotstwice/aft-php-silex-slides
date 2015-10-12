##  Services

Write your own service instantiation function ...

```php
$app['twitter'] = $app->share(
    function() {
        return new TwitterClient();
    }
);

// ...

$app['twitter']->getTweets(...);
```

... or use an existing ServiceProvider

```php
$app->register(new Silex\Provider\SessionServiceProvider());

// ...

$app['session']->set(...);
$app['session']->get(...);
```

