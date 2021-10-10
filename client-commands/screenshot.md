# 👨‍🎨 Screenshot

### Taking a screenshot

To screenshot a page, just call `withScreenshot()`:

```php
$clusteer = Clusteer::to('https://example.com')
    ->waitUntilAllRequestsFinish()
    ->withScreenshot()
    ->get();
```

```php
$screenshotAsBase64 = $clusteer->getScreenshot();
```

The image comes in base64 and gets decoded in the package automatically. If you wish to retrieve it as base64, just call `getScreenshot(false)` instead:

```php
$screenshotAsBinary = $clusteer->getScreenshot(false);
```

 You can also set the quality of the screenshot by calling `withScreenshot($quality)`, where `$quality` is a number between `0` and `100`:

```php
$clusteer = Clusteer::to('https://example.com')
    ->waitUntilAllRequestsFinish()
    ->withScreenshot(75) // 75% quality
    ->get();
```

### Setting the viewport

You may also change the viewport for the screenshot, and it can be done with `setViewport()`:

```php
$clusteer = Clusteer::to('https://example.com')
    ->waitUntilAllRequestsFinish()
    ->withScreenshot()
    ->setViewport(1280, 720)
    ->get();
```
