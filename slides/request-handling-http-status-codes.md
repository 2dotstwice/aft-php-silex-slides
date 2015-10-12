##  Request handling 

HTTP status codes

```php
$app->get(
    '/blog/{postId}',
    function (Request $request, $postId) {
        $posts = [
            1 => 'Just another Silex blog.',
            2 => 'My thoughts on PHP.',
            5 => 'AFT workshop review.',
        ];

        if (!isset($posts[$postId])) {
            return new Response('Not found.', 404);
        } else {
            return new Response($posts[$postId], 200);
        }
    }
);
```
