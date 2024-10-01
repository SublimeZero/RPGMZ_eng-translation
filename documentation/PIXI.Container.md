[Class Tree](index.md)

# Class: PIXI.Container

## Superclass: [PIXI.DisplayObject](PIXI.DisplayObject.md)

A container that holds display objects for rendering.

For more details, refer to the official PixiJS documentation: [PIXI.Container](http://pixijs.download/v5.3.12/docs/PIXI.Container.html).

### new PIXI.Container ()

### Subclasses

* [PIXI.Sprite](PIXI.Sprite.md) 
* [PIXI.Graphics](PIXI.Graphics.md)
* [PIXI.tilemap.CompositeRectTileLayer](https://github.com/pixijs/pixi-tilemap/blob/master/src/CompositeRectTileLayer.ts)
* [PIXI.tilemap.RectTileLayer](https://github.com/pixijs/pixi-tilemap/blob/master/src/RectTileLayer.ts)
* [PIXI.tilemap.ZLayer](https://github.com/pixijs/pixi-tilemap/blob/master/src/ZLayer.ts)
* [ScreenSprite](ScreenSprite.md)
* [ToneSprite](ToneSprite.md)
* [Weather](Weather.md)
* [WindowLayer](WindowLayer.md)
* [Tilemap](Tilemap.md)
* [Stage](Stage.md)
* [Window](Window.md)

### Properties

| Name              | Type                                                                 | Description                                        |
| ----------------- | -------------------------------------------------------------------- | -------------------------------------------------- |
| `children`        | [Array](Array.md).&lt;[PIXI.DisplayObject](PIXI.DisplayObject.md)&gt; | [read-only] Child objects                          |
| `width`           | [Number](Number.md)                                                  | Width of the image before scaling (in pixels)      |
| `height`          | [Number](Number.md)                                                  | Height of the image before scaling (in pixels)     |
| `sortableChildren` | Boolean                                                              | Whether the children can be sorted by `zIndex`     |
| `sortDirty`       | Boolean                                                              | Whether sorting will occur during the next update  |


### Methods Inherited from Superclass

#### [PIXI.DisplayObject](PIXI.DisplayObject.md)

* [(static) mixin (source)](PIXI.DisplayObject.md#static-mixin-source)
* [\_recursivePostUpdateTransform ()](PIXI.DisplayObject.md#_recursivepostupdatetransform-)
* [displayObjectUpdateTransform ()](PIXI.DisplayObject.md#displayobjectupdatetransform-)
* [getBounds (skipUpdate, rect)](PIXI.DisplayObject.md#getbounds-skipupdate-rect--pixirectangle)
* [getGlobalPosition (point, skipUpdate)](PIXI.DisplayObject.md#getglobalposition-point-skipupdate--pixipoint)
* [getLocalBounds (rect)](PIXI.DisplayObject.md#getlocalbounds-rect--pixirectangle)
* [setParent (container)](PIXI.DisplayObject.md#setparent-container--pixicontainer)
* [setTransform (x, y, scaleX, scaleY, rotation, skewX, skewY, pivotX, pivotY)](PIXI.DisplayObject.md#settransform-x-y-scalex-scaley-rotation-skewx-skewy-pivotx-pivoty--pixidisplayobject)
* [toGlobal (position, point, skipUpdate)](PIXI.DisplayObject.md#toglobal-position-point-skipupdate--pixipoint)
* [toLocal (position, from, point, skipUpdate)](PIXI.DisplayObject.md#tolocal-position-from-point-skipupdate--pixipoint)

### Methods

#### _calculateBounds ()
Recalculates the bounding rectangle.

#### _render (renderer)
Renders the container.

##### Parameters

| Name       | Type                            | Description        |
| ---------- | ------------------------------- | ------------------ |
| `renderer` | [PIXI.Renderer](PIXI.Renderer.md) | Renderer to use    |

#### _renderCanvas (renderer)
Renders the container on a canvas.

##### Parameters

| Name       | Type                            | Description        |
| ---------- | ------------------------------- | ------------------ |
| `renderer` | [PIXI.Renderer](PIXI.Renderer.md) | Renderer to use    |

#### addChild (child) → {PIXI.DisplayObject}
Adds a child object to the container.

##### Parameters

| Name    | Type                                          | Description        |
| ------- | --------------------------------------------- | ------------------ |
| `child` | [PIXI.DisplayObject](PIXI.DisplayObject.md)    | Object to add      |

#### addChildAt (child, index) → {PIXI.DisplayObject}
Adds a child object to a specific position in the container.

##### Parameters

| Name    | Type                                          | Description        |
| ------- | --------------------------------------------- | ------------------ |
| `child` | [PIXI.DisplayObject](PIXI.DisplayObject.md)    | Object to add      |
| `index` | [Number](Number.md)                           | Position to add to |

#### calculateBounds ()
Recalculates the bounding rectangle.

#### destroy (options)
Overrides: [PIXI.DisplayObject](PIXI.DisplayObject.md#destroy-)

##### Parameters

| Name        | Type            | Description                                                  |
| ----------- | --------------- | ------------------------------------------------------------ |
| `options`   | Object \| Boolean | Options for destruction. Applies the same value to all options below |

Options for the `options` object:

| Name           | Type     | Default | Description                           |
| -------------- | -------- | ------- | ------------------------------------- |
| `children`     | Boolean  | false   | Whether to destroy child objects      |
| `texture`      | Boolean  | false   | Whether to destroy child textures     |
| `baseTexture`  | Boolean  | false   | Whether to destroy child base textures|

#### getChildAt (index) → {PIXI.DisplayObject}
Returns the child object at a specific position.

##### Parameters

| Name    | Type            | Description        |
| ------- | --------------- | ------------------ |
| `index` | [Number](Number.md) | Position of the child |

#### getChildByName (name) → {PIXI.DisplayObject}
Returns the child object by its name.

##### Parameters

| Name  | Type             | Description         |
| ----- | ---------------- | ------------------- |
| `name` | [String](String.md) | Name of the child  |

#### getChildIndex (child) → {PIXI.DisplayObject}
Returns the index of the child object.

##### Parameters

| Name    | Type                                          | Description           |
| ------- | --------------------------------------------- | --------------------- |
| `child` | [PIXI.DisplayObject](PIXI.DisplayObject.md)    | Child object to look up |

#### onChildrenChange () 
Handler for when the children of the container are modified.

#### removeChild (child) → {PIXI.DisplayObject}
Removes a child object.

##### Parameters

| Name    | Type                                          | Description        |
| ------- | --------------------------------------------- | ------------------ |
| `child` | [PIXI.DisplayObject](PIXI.DisplayObject.md)    | Object to remove   |

#### removeChildAt (index) → {PIXI.DisplayObject}
Removes the child object at a specific position.

##### Parameters

| Name    | Type            | Description        |
| ------- | --------------- | ------------------ |
| `index` | [Number](Number.md) | Position of the child |

#### removeChildren (beginIndex, endIndex) → {Array.&lt;PIXI.DisplayObject&gt;}
Removes child objects within a specific range of indices.

##### Parameters

| Name        | Type            | Description          |
| ----------- | --------------- | -------------------- |
| `beginIndex` | [Number](Number.md) | Starting index        |
| `endIndex`   | [Number](Number.md) | Ending index          |

#### render (renderer)
Overrides: [PIXI.DisplayObject](PIXI.DisplayObject.md#render-renderer)

##### Parameters

| Name       | Type                            | Description        |
| ---------- | ------------------------------- | ------------------ |
| `renderer` | [PIXI.Renderer](PIXI.Renderer.md) | Renderer to use    |

#### renderAdvanced (renderer)
Renders using WebGL.

##### Parameters

| Name       | Type                            | Description        |
| ---------- | ------------------------------- | ------------------ |
| `renderer` | [PIXI.Renderer](PIXI.Renderer.md) | WebGL renderer     |

#### renderCanvas (renderer)
Renders the container on a canvas.

##### Parameters

| Name       | Type                                        | Description           |
| ---------- | ------------------------------------------- | --------------------- |
| `renderer` | [PIXI.CanvasRenderer](http://pixijs.download/v5.3.12/docs/PIXI.CanvasRenderer.html) | Canvas renderer        |

#### setChildIndex (child, index)

##### Parameters

| Name    | Type                                          | Description        |
| ------- | --------------------------------------------- | ------------------ |
| `child` | [PIXI.DisplayObject](PIXI.DisplayObject.md)    | Child object       |
| `index` | [Number](Number.md)                           | New index for child|

#### sortChildren ()
Sorts the child objects based on their zIndex.

#### swapChildren (child, child2)
Swaps the positions of two child objects.

##### Parameters

| Name     | Type                                          | Description           |
| -------- | --------------------------------------------- | --------------------- |
| `child`  | [PIXI.DisplayObject](PIXI.DisplayObject.md)    | First child           |
| `child2` | [PIXI.DisplayObject](PIXI.DisplayObject.md)    | Second child          |

#### updateTransform ()
Overrides: [PIXI.DisplayObject](PIXI.DisplayObject.md#updateTransform-)
