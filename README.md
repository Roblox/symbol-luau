## Symbol

A Symbol object to mimic [JavaScript's Symbol type](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol).

## API

### Symbol()
```
Symbol(name: string?): Symbol
```

Create a new symbol object. Symbols use the `newproxy` function under the hood to create an opaque, unique sentinel value. The optional string value will be included in value returned by calling `tostring` on the resulting symbol.

```
local Foo = Symbol("Foo")
print(tostring(Foo)) -- prints: 'Symbol("Foo")'
```

### Symbol.for_
```
Symbol.for_(name: string)
```

Returns globally-shared symbol for the provided name, creating it in a global registry if it has not yet been accessed. `Symbol.for_` uses a global registry for the lifetime of the lua execution.

## Types

### Symbol

Calling `Symbol.new` returns an object with type `Symbol`.

## License
Licensed under the MIT license ([LICENSE.txt](LICENSE.txt) or http://opensource.org/licenses/MIT).
