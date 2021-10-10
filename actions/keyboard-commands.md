# #️⃣ Keyboard commands

Keyboard commands are available by specifying the query string for the element, as well as the text and the delay between keystrokes.

**Note: the actions defined here are running before the request ends, so you may specify actions to run during the render.**

```php
// Note: 100 ms between keystrokes

$clusteer = Clusteer::to('https://example.com')
    ->type('john.doe@gmail.com', 'input[type="email"]', 100)
    ->get();
```

### Press & Press Down/Up

For convenience, you perhaps might want some extra combination of keys, so this is where press down and press up actions come into place:

```php
// Press down Ctrl and with it, press only once 'V' to paste,
// then release Ctrl.

$clusteer = Clusteer::to('https://example.com')
    ->pressDown('Ctrl')
    ->press('V')
    ->pressUp('Ctrl')
    ->get();
```

