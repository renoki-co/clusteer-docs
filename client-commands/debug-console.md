# 🐞 Debug console

You can get the output from the console with `withConsoleLines()`:

```php
$clusteer = Clusteer::to('https://example.com')
    ->waitUntilAllRequestsFinish()
    ->withConsoleLines()
    ->get();
```

```php
$lines = $clusteer->getConsoleLines();
```
