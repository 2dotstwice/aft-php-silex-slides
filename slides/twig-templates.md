##  Twig templates

```php
$app->register(
    new Silex\Provider\TwigServiceProvider(),
    ['twig.path' => __DIR__ . '/../templates']
);
```

```php
$app->get(
    'blog',
    function(Request $request) use ($app) {
        $posts = [
            1 => 'Just another Silex blog.',
            2 => 'My thoughts on PHP.',
            5 => 'AFT workshop review.',
        ];

        $html = $app['twig']->render('blog.twig', [
            'title' => 'My awesome blog.',
            'posts' => $posts,
        ]);

        return new Response($html);
    }
);
```
