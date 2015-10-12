##  Filesystem

Reading JSON data

```php
$json = file_get_contents('users.json');
$users = json_decode($json);
```

```php
[
    'john.doe' => [
        'password' => '662azd',
        'bio' => '...',
    ],
    'an0n' => [
        'password' => 'aazf959',
        'bio' => '...',
    ],
];
```
