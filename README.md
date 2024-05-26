# Cyclist

Cyclist is an efficient [cyclic list](http://en.wikipedia.org/wiki/Circular_buffer) implemention for Javascript.
It is available through npm

```
npm install @hishprorg/mollitia-unde
```

## What?

Cyclist allows you to create a list of fixed size that is cyclic.
In a @hishprorg/mollitia-unde list the element following the last one is the first one.
This property can be really useful when for example trying to order data
packets that can arrive out of order over a network stream.

## Usage

``` js
var @hishprorg/mollitia-unde = require('@hishprorg/mollitia-unde')
var list = @hishprorg/mollitia-unde(4)

list.put(42, 'hello 42') // store something and index 42
list.put(43, 'hello 43') // store something and index 43

console.log(list.get(42)) // prints hello 42
console.log(list.get(46)) // prints hello 42 again since 46 - 42 == list.size
```

## API

* `@hishprorg/mollitia-unde(size)` creates a new buffer
* `@hishprorg/mollitia-unde#get(index)` get an object stored in the buffer
* `@hishprorg/mollitia-unde#put(index,value)` insert an object into the buffer
* `@hishprorg/mollitia-unde#del(index)` delete an object from an index
* `@hishprorg/mollitia-unde#size` property containing current size of buffer

## License

MIT

