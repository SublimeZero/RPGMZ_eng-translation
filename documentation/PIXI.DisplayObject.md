# Class: PIXI.DisplayObject

## Superclass: [PIXI.utils.EventEmitter](https://pixijs.download/v5.3.12/docs/PIXI.utils.EventEmitter.html)

The base object for everything displayed on the screen.

For modifying data such as `position` with multiple numeric values, it's more efficient to use:
`displayObject.position.set(0, 0)` instead of `displayObject.position = new PIXI.Point(0, 0)`. This approach is easier to write and reduces processing load.

To see which setting methods are available for each data type, refer to the relevant reference ([PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html), etc.).

For more details, visit the PixiJS documentation: [PIXI.DisplayObject](http://pixijs.download/v5.3.12/docs/PIXI.DisplayObject.html).

### new PIXI.DisplayObject()

### Subclasses
* [PIXI.Container](PIXI.Container.md)

### Properties

| Name                | Type                                                    | Description                                      |
| ------------------- | ------------------------------------------------------- | ------------------------------------------------ |
| `accessible`        | Boolean                                                 | Is it accessible?                                |
| `accessibleHint`    | [String](String.md)                                      | Hint text (if `accessible` is `true`)            |
| `accessibleTitle`   | [String](String.md)                                      | Title text (if `accessible` is `true`)           |
| `alpha`             | [Number](Number.md)                                      | Opacity                                          |
| `angle`             | [Number](Number.md)                                      | Rotation angle (in degrees)                      |
| `buttonMode`        | Boolean                                                 | Changes pointer on mouse hover                   |
| `cacheAsBitmap`     | Boolean                                                 | Is it cached as a bitmap?                        |
| `cursor`            | [String](String.md)                                      | Pointer type when mouse hovers                   |
| `filterArea`        | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html) | Filter area                                      |
| `filters`           | [Array](Array.md).&lt;[PIXI.Filter](PIXI.Filter.md)&gt; | Array of filters                                 |
| `hitArea`           | [PIXI.IHitArea](http://pixijs.download/v5.3.12/docs/PIXI.IHitArea.html) | Hit detection area                               |
| `interactive`       | Boolean                                                 | Is it interactive (clickable)?                   |
| `isSprite`          | Boolean                                                 | Is it a sprite?                                  |
| `localTransform`    | [PIXI.Matrix](http://pixijs.download/v5.3.12/docs/PIXI.Matrix.html) | [read-only] Local transform                      |
| `mask`              | [PIXI.Graphics](PIXI.Graphics.md) \| [PIXI.Sprite](PIXI.Sprite.md) \| null | Mask image                                       |
| `name`              | [String](String.md)                                      | Name of the object                               |
| `parent`            | [PIXI.Container](PIXI.Container.md)                      | [read-only] Parent container                     |
| `pivot`             | [PIXI.IPoint](http://pixijs.download/v5.3.12/docs/PIXI.IPoint.html) | Pivot point (in pixels)                          |
| `position`          | [PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html) | Position (x, y)                                  |
| `renderable`        | Boolean                                                 | Is it renderable?                                |
| `rotation`          | [Number](Number.md)                                      | Rotation (in radians)                            |
| `scale`             | [PIXI.IPoint](http://pixijs.download/v5.3.12/docs/PIXI.IPoint.html) | Scale factor (e.g. {1, 1} for normal size)       |
| `skew`              | [PIXI.ObservablePoint](http://pixijs.download/v5.3.12/docs/PIXI.ObservablePoint.html) | Skew                                              |
| `transform`         | [PIXI.Matrix](http://pixijs.download/v5.3.12/docs/PIXI.Matrix.html) | Transformation matrix                           |
| `visible`           | Boolean                                                 | Is it visible?                                   |
| `worldAlpha`        | [Number](Number.md)                                      | [read-only] Final opacity                        |
| `worldTransform`    | [PIXI.Matrix](http://pixijs.download/v5.3.12/docs/PIXI.Matrix.html) | [read-only] Final transformation matrix          |
| `worldVisible`      | Boolean                                                 | [read-only] Is it visible in the world?          |
| `x`                 | [Number](Number.md)                                      | x-coordinate (in pixels)                         |
| `y`                 | [Number](Number.md)                                      | y-coordinate (in pixels)                         |
| `zIndex`            | [Number](Number.md)                                      | Sorting index (higher numbers appear in front)   |
| `_accessibleDiv`    | Boolean                                                 | (Internal) Accessibility div                    |
| `_bounds`           | [PIXI.Bounds](http://pixijs.download/v5.3.12/docs/PIXI.Bounds.html) | Bounding box                                     |
| `_destroyed`        | Boolean                                                 | Has it been destroyed via `destroy()`?           |
| `_lastSortedIndex`  | [Number](Number.md)                                      | Last sorted index                                |
| `_mask`             | [PIXI.Graphics](PIXI.Graphics.md) \| [PIXI.Sprite](PIXI.Sprite.md) \| null | Internal mask                                    |
| `_tempDisplayObjectParent` | PIXI.DisplayObject                                  | Temporary parent object                         |
| `_zIndex`           | [Number](Number.md)                                      | Internal z-index                                |

### Methods

#### (static) mixin (source)
Mixes in all enumerable properties and methods from the specified object.

##### Arguments

| Name    | Type   | Description                                   |
| ------- | ------ | --------------------------------------------- |
| `source`| Object | The object to mix in properties from.        |


#### _recursivePostUpdateTransform ()
Recursively updates the transform from the root to this object.


#### destroy ()
Destroys the object.


#### displayObjectUpdateTransform ()
Updates the transform without updating child objects.


#### getBounds (skipUpdate opt, rect opt) → {PIXI.Rectangle}
Returns the bounding rectangle.

##### Arguments

| Name        | Type                              | Characteristics    | Description   |
| ----------- | --------------------------------- | ------------------- | ------------- |
| `skipUpdate`| Boolean                          | &lt;optional&gt;   |               |
| `rect`      | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html) | &lt;optional&gt;   |               |


#### getGlobalPosition (point opt, skipUpdate opt) → {PIXI.Point}
Returns the global position.

##### Arguments

| Name       | Type                              | Characteristics    | Description   |
| ---------- | --------------------------------- | ------------------- | ------------- |
| `point`    | [PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html) | &lt;optional&gt;   |               |
| `skipUpdate`| Boolean                          | &lt;optional&gt;   |               |


#### getLocalBounds (rect opt) → {PIXI.Rectangle}
Returns the local bounding rectangle.

##### Arguments

| Name       | Type                              | Characteristics    | Description   |
| ---------- | --------------------------------- | ------------------- | ------------- |
| `rect`     | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html) | &lt;optional&gt;   |               |


#### render (renderer)
Performs rendering.

##### Arguments

| Name     | Type                              | Description       |
| -------- | --------------------------------- | ------------------ |
| `renderer`| [PIXI.Renderer](PIXI.Renderer.md) |                   |


#### setParent (container) → {PIXI.Container}
Sets the parent object.

##### Arguments

| Name      | Type                             | Description                             |
| --------- | -------------------------------- | --------------------------------------- |
| `container`| [PIXI.Container](PIXI.Container.md) | The container object to be set as the parent |


#### setTransform (x, y, scaleX, scaleY, rotation, skewX, skewY, pivotX, pivotY) → {PIXI.DisplayObject}
Sets the transform values and returns itself.

##### Arguments

| Name      | Type       | Description                        |
| --------- | ---------- | ---------------------------------- |
| `x`       | [Number](Number.md) | x-coordinate                     |
| `y`       | [Number](Number.md) | y-coordinate                     |
| `scaleX`  | [Number](Number.md) | x scale factor                   |
| `scaleY`  | [Number](Number.md) | y scale factor                   |
| `rotation`| [Number](Number.md) | Rotation angle (in radians)      |
| `skewX`   | [Number](Number.md) | x skew angle                     |
| `skewY`   | [Number](Number.md) | y skew angle                     |
| `pivotX`  | [Number](Number.md) | Rotation pivot x-coordinate       |
| `pivotY`  | [Number](Number.md) | Rotation pivot y-coordinate       |


#### toGlobal (position, point opt, skipUpdate opt) → {PIXI.Point}
Converts to global coordinates.

##### Arguments

| Name       | Type                              | Characteristics    | Description                   |
| ---------- | --------------------------------- | ------------------- | ----------------------------- |
| `position` | [PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html) |                     | Coordinates to convert from   |
| `point`    | [PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html) | &lt;optional&gt;   |                               |
| `skipUpdate`| Boolean                          | &lt;optional&gt;   | (default: false)             |


#### toLocal (position, from opt, point opt, skipUpdate opt) → {PIXI.Point}
Converts to local coordinates.

##### Arguments

| Name       | Type                              | Characteristics    | Description                   |
| ---------- | --------------------------------- | ------------------- | ----------------------------- |
| `position` | [PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html) |                     | Coordinates to convert from    |
| `from`     | PIXI.DisplayObject               | &lt;optional&gt;   |                               |
| `point`    | [PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html) | &lt;optional&gt;   |                               |
| `skipUpdate`| Boolean                          | &lt;optional&gt;   | (default: false)             |


#### updateTransform ()
Updates the transform.


### Events

#### added(container)
Event triggered when a child object is added.

| Name      | Type                             | Description                              |
| --------- | -------------------------------- | ---------------------------------------- |
| `container`| [PIXI.Container](PIXI.Container.md) | The container to which the child was added |


#### click(event)
Event triggered when clicked.

| Name      | Type                                             | Description         |
| --------- | ----------------------------------------------- | ------------------- |
| `event`   | [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event    |

#### mousedown(event)
Event triggered when a button is pressed.

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### mousemove(event)
Event triggered when the pointer moves.

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### mouseout(event)
Event triggered when the pointer leaves the UI area.

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### mouseover(event)
Event triggered when the pointer enters the UI area.

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### mouseup(event)
Event triggered when a button is released.

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### mouseupoutside(event)
Event triggered when a button is released inside the UI area.

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### pointercancel(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### pointerdown(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### pointermove(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### pointerout(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### pointerover(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### pointertap(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### pointerup(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### pointerupoutside(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### removed(container)
Event triggered when a child object is removed.

| Name      | Type                                             | Description                             |
| --------- | ----------------------------------------------- | --------------------------------------- |
| `container`| [PIXI.Container](PIXI.Container.md)            | The container from which the child was removed |


#### rightclick(event)
Event triggered when a right click occurs.

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### rightdown(event)
Event triggered when the right button is pressed.

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### rightup(event)
Event triggered when the right button is released.

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### rightupoutside(event)
Event triggered when the right button is released outside the UI area.

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### tap(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### touchcancel(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### touchend(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### touchendoutside(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### touchmove(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |


#### touchstart(event)

| Name   | Type                                             | Description       |
| ------ | ----------------------------------------------- | ------------------ |
| `event`| [PIXI.interaction.InteractionEvent](http://pixijs.download/v5.3.12/docs/PIXI.interaction.InteractionEvent.html) | Interaction event   |
