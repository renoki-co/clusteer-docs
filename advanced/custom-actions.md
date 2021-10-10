# 👩‍🚀 Custom Actions

Besides the built-in actions, you are free to extend them as you like. Before diving in, make sure to check the [Custom Script](custom-script.md) documentation, as the following example requires custom server.js file.

### Creating the class

All classes must extend the `\RenokiCo\Clusteer\Actions\Action` class and implement the `\RenokiCo\Clusteer\Contracts\Actionable` interface.

```php
use RenokiCo\Clusteer\Actions\Action;
use RenokiCo\Clusteer\Contracts\Actionable;

class TypeDunnoLolEmoji extends Action implements Actionable
{
    //
}
```

When processing your action, it requires the input data (such as what it should do), and on the other side, the formatted data that will be sent to the script is going to be placed in a `format()` method:

```php
use RenokiCo\Clusteer\Actions\Action;
use RenokiCo\Clusteer\Contracts\Actionable;

class TypeDunnoLolEmoji extends Action implements Actionable
{
    protected $selector;

    public function __construct(string $selector)
    {
        $this->selector = $selector;
    }
    
    /**
     * Format to an array that can instructm and be read
     * by the JS script to perform a specific action.
     *
     * @return array
     */
    public function format(): array
    {
        return [
            'name' => 'type-emoji', // required
            'selector' => $this->selector,
            'emoji' => '¯\_(ツ)_/¯',
        ];
    }
}
```

One last thing is to check our `server.js` file and add a new option to handle the action called `type-emoji`:

```javascript
await actions.reduce(async (promise, action) => {
  // ...

  if (action.name === 'type-emoji') {
    await page.type(action.selector, action.emoji);
  }
  
  // ...
});
```

In your PHP code, you may invoke the `action()` method. Additionally, all classes that extend the `Action` class will have a static `new` method that's useful:

```php
Clusteer::to('https://example.com')
    ->action(TypeDunnoLolEmoji::new('input[type="text"]'))
    ->get();
```
