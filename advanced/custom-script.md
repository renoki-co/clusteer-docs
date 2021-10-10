# 🎀 Custom Script

The script that is used by the Clusteer server is shown in [server.js](https://github.com/renoki-co/clusteer/blob/master/server.js). You may customize the script parts the way you would like and instead of using the default script, you may pass to the `clusteer:serve` command the parameter the path to the script to run:

```bash
php artisan clusteer:serve --js-file-path="/path/to/server.js"
```

For vanilla PHP, you can use the `jsFilePath()` method:

```php
$server->jsFilePath('/path/to/server.js')->configureServer();
```

