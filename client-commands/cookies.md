# 🍘 Cookies

You can get the attached cookies during the rendering:

```php
$clusteer = Clusteer::to('https://example.com')
    ->waitUntilAllRequestsFinish()
    ->withCookies()
    ->get();
```

```php
$cookies = $clusteer->getCookies();
```
