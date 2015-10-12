##  Request handling 

Posting data

    POST http://<your-url>/contact

```php
$app->post(
    '/contact',
    function (Request $request) {
        $filename = __DIR__ . '/files/contact-' . time() . '.txt';
        $content = $request->getContent();
        
        file_put_contents($filename, $content);
        
        return new Response($filename);
    }
);
```
