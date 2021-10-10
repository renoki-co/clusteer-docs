# 🐁 Mouse commands

Same as with the [keyboard](keyboard-commands.md), you may also mimick clicks.

**Note: the actions defined here are running before the request ends, so you may specify actions to run during the render.**

```php
Clusteer::to('https://example.com')
    ->leftClick('td[class="mouse-1"]')
    ->rightClick('td[class="mouse-2"]')
    ->middleClick('td[class="mouse-3"]')
    ->get();
```
