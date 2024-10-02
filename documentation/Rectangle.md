# Class: Rectangle

## Superclass: [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html)

A class that represents a rectangular area.

This section includes the properties and methods of `PIXI.Rectangle`, but for more details, please refer to [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html).

Most methods return themselves for the purpose of method chaining.

Related classes: [Point](Point.md), [Window](Window.md), [Window_NameEdit](Window_NameEdit.md), [Window_NameInput](Window_NameInput.md), [Window_SavefileList](Window_SavefileList.md), [Window_Selectable](Window_Selectable.md), [Window_BattleLog](Window_BattleLog.md), [Window_BattleStatus](Window_BattleStatus.md), [Sprite_Button](Sprite_Button.md), [MV.Rectangle](MV.Rectangle.md), [MV.Size](MV.Size.md)

### new Rectangle (x opt, y opt, width opt, height opt)
#### Parameters

| Name     | Type           | Attributes    | Description                                |
|----------|----------------|----------------|--------------------------------------------|
| `x`      | [Number](Number.md) | <optional>    | The x-coordinate of the left side of the rectangle (default: 0) |
| `y`      | [Number](Number.md) | <optional>    | The y-coordinate of the top side of the rectangle (default: 0) |
| `width`  | [Number](Number.md) | <optional>    | The width of the rectangle (default: 0)  |
| `height` | [Number](Number.md) | <optional>    | The height of the rectangle (default: 0) |

### Properties

| Identifier | Type           | Description                                |
|------------|----------------|--------------------------------------------|
| `x`        | [Number](Number.md) | The x-coordinate of the left side of the rectangle |
| `y`        | [Number](Number.md) | The y-coordinate of the top side of the rectangle |
| `width`    | [Number](Number.md) | The width of the rectangle                |
| `height`   | [Number](Number.md) | The height of the rectangle               |
| `top`      | [Number](Number.md) | The y-coordinate of the top side of the rectangle (same as `y`) |
| `bottom`   | [Number](Number.md) | The y-coordinate of the bottom side of the rectangle |
| `left`     | [Number](Number.md) | The x-coordinate of the left side of the rectangle (same as `x`) |
| `right`    | [Number](Number.md) | The x-coordinate of the right side of the rectangle |
| `type`     | [Number](Number.md) | [read-only] Type (refer to: [PIXI.SHAPES](http://pixijs.download/v5.3.12/docs/PIXI.html#SHAPES)) |

### Deprecated MV Property
`emptyRectangle` (use the parent class `PIXI.Rectangle.EMPTY` instead)

### Methods

#### ceil (resolution opt, eps opt) → {[Rectangle](Rectangle.md)}
Rounds the values up to align with the grid and returns itself.<br />
Since its values change, if the return value is not needed, it can be discarded.

##### Parameters

| Name        | Type           | Attributes    | Description                                |
|-------------|----------------|----------------|--------------------------------------------|
| `resolution`| [Number](Number.md) | <optional>    | The resolution (default: 1)                |
| `eps`       | [Number](Number.md) | <optional>    | The precision (default: 0.001)             |

#### clone () → {[Rectangle](Rectangle.md)}
Copies and returns the values (not by reference).

#### contains (x, y) → {Boolean}
Checks if the specified coordinates are contained within the rectangular area.

##### Parameters

| Name | Type           | Description                                |
|------|----------------|--------------------------------------------|
| `x`  | [Number](Number.md) | The x-coordinate                           |
| `y`  | [Number](Number.md) | The y-coordinate                           |

#### copyFrom (rectangle) → {[Rectangle](Rectangle.md)}
Copies another rectangular area and sets it, returning itself.<br />
Since its values change, if the return value is not needed, it can be discarded.

##### Parameters

| Name       | Type           | Description                                |
|------------|----------------|--------------------------------------------|
| `rectangle`| [Rectangle](Rectangle.md) | The rectangular area to set                |

#### copyTo (rectangle) → {[Rectangle](Rectangle.md)}
Copies itself to another rectangular area and returns the set values.<br />
The value specified in the argument does not necessarily have to be a `Rectangle`; any object with x, y, width, and height properties will work.<br />
In most cases, it will be referenced by variable passing, so the return value can be discarded.

##### Parameters

| Name       | Type           | Description                                |
|------------|----------------|--------------------------------------------|
| `rectangle`| [Rectangle](Rectangle.md) | The rectangular area to set                |

#### enlarge (rectangle) → {[Rectangle](Rectangle.md)}
Expands itself to include the specified rectangular area and returns itself.<br />
Since its values change, if the return value is not needed, it can be discarded.

##### Parameters

| Name       | Type           | Description                                |
|------------|----------------|--------------------------------------------|
| `rectangle`| [Rectangle](Rectangle.md) | The rectangular area                      |

#### fit (rectangle) → {[Rectangle](Rectangle.md)}
Cuts itself down to the area contained within the specified rectangular area and returns itself.<br />
Since its values change, if the return value is not needed, it can be discarded.

##### Parameters

| Name       | Type           | Description                                |
|------------|----------------|--------------------------------------------|
| `rectangle`| [Rectangle](Rectangle.md) | The rectangular area                      |

#### initialize ()
Initialization when the object is created.

#### pad (paddingX opt, paddingY opt) → {[Rectangle](Rectangle.md)}
Expands in both directions according to the specified values and returns itself.<br />
Since its values change, if the return value is not needed, it can be discarded.

##### Parameters

| Name       | Type           | Attributes    | Description                                |
|------------|----------------|----------------|--------------------------------------------|
| `paddingX` | [Number](Number.md) | <optional>    | The amount of expansion in the x direction (default: 0) |
| `paddingY` | [Number](Number.md) | <optional>    | The amount of expansion in the y direction (default: 0; however, if `x` is specified, it will be the same as `x`) |
