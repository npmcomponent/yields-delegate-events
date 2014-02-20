*This repository is a mirror of the [component](http://component.io) module [yields/delegate-events](http://github.com/yields/delegate-events). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/yields-delegate-events`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# delegate-events

  delegate events from one emitter to another

## Installation

  Install with [component(1)](http://component.io):

    $ component install yields/delegate-events

## API

#### delegate(a, b, events)

  Delegate array of `events` from emitter `a` to emitter `b`.

## Example

```js
delegate(a, b, ['test']);

b.on('test', function(a, b){
  assert('a' == a);
  assert('b' == b);
});

a.emit('test', 'a', 'b');
```

## Tests

```bash
$ make test
```

## License

  MIT
