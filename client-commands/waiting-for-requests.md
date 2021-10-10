# ⌚ Waiting for requests

By default, Puppeteer tells the browser to not wait for all the requests to be ran. Sometimes, you might want to wait for all of the requests to be ready:

```php
$clusteer = Clusteer::to('https://example.com')
    ->waitUntilAllRequestsFinish()
    ->withHtml()
    ->get();
```

If you want to see the triggered requests, call `withTriggeredRequests()`:

```php
$clusteer = Clusteer::to('https://example.com')
    ->waitUntilAllRequestsFinish()
    ->withTriggeredRequests()
    ->get();
```

```php
$requests = $clusteer->getTriggeredRequests();
```
