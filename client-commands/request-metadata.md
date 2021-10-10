# 🧵 Request metadata

You may change the request metadata that contains user agent or extra headers:

```php
$clusteer = Clusteer::to('https://example.com')
    ->setExtraHeaders(['X-My-Header' => 'Value'])
    ->setUserAgent('My Fake/1.0 User-Agent')
    ->get();
```

### Blocking Extensions

You may block certain extensions from running when the page loads. This can easily block all CSS or JavaScript, to achieve greater performance:

```php
$clusteer = Clusteer::to('https://example.com')
    ->waitUntilAllRequestsFinish()
    ->blockExtensions(['.css'])
    ->get();
    
foreach ($clusteer->getTriggeredRequests() as $request) {
    // dump($request['url'])
}
```
