[Class Tree](index.md)

# Class: Array

### new Array ()
Some RPG Maker MZ-specific methods have been added to JavaScript arrays.

For more details, please refer to the [MDN Array page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array).
Here, only the added methods will be explained.

### Methods

#### clone () → {[Array](Array.md)}
Returns a (shallow) copy of the array.
In practice, this is equivalent to the standard slice(0), so there is no need to use it intentionally.

#### contains (element) → {Boolean}
Checks if the specified value is included in the array.
**It is recommended to use the built-in JS function, includes().**

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `element` | * | The value to search in the array |


#### equals (array) → {Boolean}
Checks if the arrays are the same.

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `array` | [Array](Array.md) | The array to compare |


#### remove(element)
**@MZ** Removes the specified element from the array.

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `element` | * | The value to remove from the array |
