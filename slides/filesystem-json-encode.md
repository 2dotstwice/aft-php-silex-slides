##  Filesystem

Storing data as JSON

```php
$users = [
    'john.doe' => [
        'password' => '662azd',
        'bio' => '...',
    ],
    'an0n' => [
        'password' => 'aazf959',
        'bio' => '...',
    ],
];

$json = json_encode($users);
file_put_contents('users.json', $json);
```
