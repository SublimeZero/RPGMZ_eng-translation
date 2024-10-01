[Class Tree](index.md)

# Class: Number

The JavaScript `Number` object has several custom methods added for **RPG Maker MZ**.

For more details, refer to the [MDN Number page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number).  
Here, only the additional methods are explained.

### new Number ()

### Methods

#### clamp (min, max) → {[Number](Number.md)}
Returns a value within the specified range.

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `min` | [Number](Number.md) | Minimum value |
| `max` | [Number](Number.md) | Maximum value |


#### mod (n) → {[Number](Number.md)}
Returns the remainder of the division.

Similar to `%`, but always returns a positive value.

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `n` | [Number](Number.md) | The divisor |


#### padZero (length) → {[String](String.md)}
Pads the number with leading zeros and returns it as a string of the specified length.

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `length` | [Number](Number.md) | The length of the resulting string |
