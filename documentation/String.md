[Class Tree](index.md)

# Class: String

Some custom methods unique to "RPG Maker MZ" have been added to JavaScript strings.

For details, please refer to the [MDN String page](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String). 
Here, only the added methods are explained.

### new String ()

### Methods

#### contains (string) → {Boolean}
Checks if the specified string is contained.

##### Arguments:

| Identifier | Type       | Description         |
|------------|------------|---------------------|
| `string`   | [String](String.md) | The string to search for |

---

#### format (...args) → {[String](String.md)}
Replaces placeholders like %1, %2 with the specified arguments and returns the result.<br />
Pass multiple arguments instead of an array.

##### Arguments:

| Identifier | Type  | Description          |
|------------|-------|----------------------|
| `...args`  | Any   | Values for replacement |

---

#### padZero (length) → {[String](String.md)}
Pads the string with zeros to return a string of the specified length.

##### Arguments:

| Identifier | Type          | Description        |
|------------|---------------|--------------------|
| `length`   | [Number](Number.md) | The length of the string |
