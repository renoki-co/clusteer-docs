# 🙌 Basic example

The client relies on the already existent Clusteer server. You can get it locally by starting the server or having a remote one and manually change the config. Below you have a brief example:

```php
use RenokiCo\Clusteer\Clusteer;

$clusteer = Clusteer::to('https://example.com')
    ->setViewport(1280, 720)
    ->setDevice(Clusteer::MOBILE_DEVICE)
    ->setExtraHeaders([
        'My-Header' => 'Value',
    ])
    ->blockExtensions(['.css'])
    ->withHtml()
    ->get();
```
