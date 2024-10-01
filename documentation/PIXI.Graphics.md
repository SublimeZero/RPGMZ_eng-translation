[Class Tree](index.md)

# Class: PIXI.Graphics

## Superclass: [PIXI.Container](PIXI.Container.md)

A class for drawing images using lines, circles, and other shapes. <br />
Many methods return the `PIXI.Graphics` instance itself, allowing method chaining by using the dot (.) notation.

For more details, refer to the official PixiJS site [PIXI.Graphics](http://pixijs.download/v5.3.12/docs/PIXI.Graphics.html). <br />
Additionally, there are many common methods with the [CanvasRenderingContext2D](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D), which is the drawing context of the [HTMLCanvasElement](https://developer.mozilla.org/ja/docs/Web/API/HTMLCanvasElement) class in JavaScript, so you may also want to look into that.

Related classes: [ScreenSprite](ScreenSprite.md), [WindowLayer](WindowLayer.md), [PIXI.Texture](PIXI.Texture.md)

### new PIXI.Graphics (geometry opt)
#### Arguments

| Name       | Type                                                   | Traits        | Description                |
|------------|--------------------------------------------------------|---------------|----------------------------|
| `geometry` | [PIXI.GraphicsGeometry](http://pixijs.download/v5.3.12/docs/PIXI.GraphicsGeometry.html) | <optional>    | Geometry                   |

### Properties

| Name          | Type                                                   | Description                           |
|---------------|--------------------------------------------------------|---------------------------------------|
| `batches`     | [Array](Array.md).<Object>                            | Batches                               |
| `batchTint`   | [Number](Number.md)                                   | (default: -1)                        |
| `blendMode`   | [Number](Number.md)                                   | [Blend mode](Sprite.md#blend-mode) (default: [PIXI.BLEND_MODES](http://pixijs.download/v5.3.12/docs/PIXI.html#.BLEND_MODES).NORMAL) |
| `currentPath` | [PIXI.Polygon](http://pixijs.download/v5.3.12/docs/PIXI.Polygon.html) | Current path                          |
| `fill`        | [PIXI.FillStyle](http://pixijs.download/v5.3.12/docs/PIXI.FillStyle.html) | [read-only] Fill style               |
| `geometry`    | [PIXI.GraphicsGeometry](http://pixijs.download/v5.3.12/docs/PIXI.GraphicsGeometry.html) | Geometry                             |
| `line`        | [PIXI.LineStyle](http://pixijs.download/v5.3.12/docs/PIXI.LineStyle.html) | [read-only] Line style               |
| `pluginName`  | [String](String.md)                                   | Default: "batch"                     |
| `shader`      | [PIXI.Shader](PIXI.Shader.md)                        | Shader                                |
| `state`       | [PIXI.State](http://pixijs.download/v5.3.12/docs/PIXI.State.html) | State                                  |
| `tint`        | [Number](Number.md)                                   | Outline color (default: 0xffffff)    |
| `vertexData`  | Float32Array                                          | Vertex data                           |
| `graphicsData` | [Array](Array.md).<[PIXI.GraphicsData](http://pixijs.download/v5.3.12/docs/PIXI.GraphicsData.html)> | Image data                           |
| `_fillStyle`  | [PIXI.FillStyle](http://pixijs.download/v5.3.12/docs/PIXI.FillStyle.html) | Fill style                           |
| `_holeMode`   | Boolean                                              | Whether in hole mode (default: false) |
| `_lineStyle`  | [PIXI.LineStyle](http://pixijs.download/v5.3.12/docs/PIXI.LineStyle.html) | Line style                           |
| `_matrix`     | [PIXI.Matrix](http://pixijs.download/v5.3.12/docs/PIXI.Matrix.html) | Transformation matrix                 |

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


#### [PIXI.Container](PIXI.Container.md)

* [\_renderCanvas (renderer)](PIXI.Container.md#_rendercanvas-renderer)
* [addChild (child) ](PIXI.Container.md#addchild-child--pixidisplayobject)
* [addChildAt (child, index)](PIXI.Container.md#addchildat-child-index--pixidisplayobject)
* [calculateBounds ()](PIXI.Container.md#calculatebounds-)
* [getChildAt (index)](PIXI.Container.md#getchildat-index--pixidisplayobject)
* [getChildByName (name)](PIXI.Container.md#getchildbyname-name--pixidisplayobject)
* [getChildIndex (child)](PIXI.Container.md#getchildindex-child--pixidisplayobject)
* [onChildrenChange ()](PIXI.Container.md#onchildrenchange-)
* [removeChild (child)](PIXI.Container.md#removechild-child--pixidisplayobject)
* [removeChildAt (index)](PIXI.Container.md#removechildat-index--pixidisplayobject)
* [removeChildren (beginIndex, endIndex)](PIXI.Container.md#removechildren-beginindex-endindex--arraypixidisplayobject)
* [render (renderer)](PIXI.Container.md#render-renderer)
* [renderAdvanced (renderer)](PIXI.Container.md#renderadvanced-renderer)
* [setChildIndex (child, index)](PIXI.Container.md#setchildindex-child-index)
* [sortChildren ()](PIXI.Container.md#sortchildren-)
* [swapChildren (child, child2)](PIXI.Container.md#swapchildren-child-child2)
* [updateTransform ()](PIXI.Container.md#updatetransform-)

### Methods

#### _calculateBounds ()
Override: [PIXI.Container.md](PIXI.Container.md#_calculatebounds-)

#### _initCurve (x opt, y opt)
Initializes a curve.

##### Arguments

| Name | Type | Traits | Description |
| --- | --- | --- | --- |
| `x` | [Number](Number.md) | <optional> | X-coordinate (default: 0 pixels) |
| `y` | [Number](Number.md) | <optional> | Y-coordinate (default: 0 pixels) |

#### _render (renderer)
Override: [_render (renderer)](PIXI.Container.md#_render-renderer)

#### arc (cx, cy, radius, startAngle, endAngle, anticlockwise opt) →  {PIXI.Graphics}
Draws an arc and returns itself.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `cx` | [Number](Number.md) | Center X-coordinate (pixels) |
| `cy` | [Number](Number.md) | Center Y-coordinate (pixels) |
| `radius` | [Number](Number.md) | Radius (pixels) |
| `startAngle` | [Number](Number.md) | Start angle |
| `endAngle` | [Number](Number.md) | End angle |
| `anticlockwise` | [Number](Number.md) | <optional> | Whether it is anticlockwise (default: false) |

#### arcTo (x1, y1, x2, y2, radius) →  {PIXI.Graphics}
Draws a rounded corner and returns itself. <br />
The procedure is to draw a line from the last point to the midpoint, then from the midpoint to the endpoint, and finally draw an arc with a radius that touches both lines.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x1` | [Number](Number.md) | Midpoint X-coordinate (pixels) |
| `y1` | [Number](Number.md) | Midpoint Y-coordinate (pixels) |
| `x2` | [Number](Number.md) | Endpoint X-coordinate (pixels) |
| `y2` | [Number](Number.md) | Endpoint Y-coordinate (pixels) |
| `radius` | [Number](Number.md) | Rounded corner radius (pixels) |

#### beginFill (color opt, alpha opt) →  {PIXI.Graphics}
Starts filling and returns itself.

##### Arguments

| Name | Type | Traits | Description |
| --- | --- | --- | --- |
| `color` | [Number](Number.md) | <optional> | Color (default: 0) |
| `alpha` | [Number](Number.md) | <optional> | Opacity (default: 1) |

#### beginHole () →  {PIXI.Graphics}
Starts to create a hole inside the last drawn shape and returns itself.

#### beginTextureFill (color opt, alpha opt) →  {PIXI.Graphics}
Starts filling with a texture and returns itself.

##### Arguments

| Name | Type | Traits | Description |
| --- | --- | --- | --- |
| `color` | [Number](Number.md) \| [PIXI.Texture](PIXI.Texture.md) | <optional> | Fill color (default: 0xffffff) |
| `alpha` | [Number](Number.md) \| [PIXI.Matrix](http://pixijs.download/v5.3.12/docs/PIXI.Matrix.html) | <optional> | Opacity (default: 1) |

#### bezierCurveTo (cpX, cpY, cpX2, cpY2, toX, toY) →  {PIXI.Graphics}
Draws a cubic Bezier curve and returns itself.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `cpX` | [Number](Number.md) | Control point 1 X-coordinate (pixels) |
| `cpY` | [Number](Number.md) | Control point 1 Y-coordinate (pixels) |
| `cpX2` | [Number](Number.md) | Control point 2 X-coordinate (pixels) |
| `cpY2` | [Number](Number.md) | Control point 2 Y-coordinate (pixels) |
| `toX` | [Number](Number.md) | Endpoint X-coordinate (pixels) |
| `toY` | [Number](Number.md) | Endpoint Y-coordinate (pixels) |

#### calculateTints ()
Calculates the tints.

#### calculateVertices ()
Calculates the vertices.

#### clear () →  {PIXI.Graphics}
Clears the graphics and returns itself.

#### clone () →  {PIXI.Graphics}
Creates a duplicate and returns it.

#### closePath () →  {PIXI.Graphics}
Closes the path and returns itself.

#### containsPoint (point) →  {Boolean}
Checks if a specified point is contained.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `point` | [PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html) | |

#### destroy (options opt)
Override: [PIXI.Container](PIXI.Container.md#destroy-options)

##### Arguments

| Name | Type | Traits | Description |
| --- | --- | --- | --- |
| `options` | Object \| Boolean | <optional> | Boolean value that applies to all the following options |
| `options.children` | Boolean | <optional> | Whether to destroy children (default: false) |
| `options.texture` | Boolean | <optional> | If both children and texture are true, it will destroy the children's textures (default: false) |
| `options.baseTexture` | Boolean | <optional> | If both children and baseTexture are true, it will destroy the children's base textures (default: false) |

#### drawCircle (x, y, radius) →  {PIXI.Graphics}
Draws a circle and returns itself.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Center X-coordinate (pixels) |
| `y` | [Number](Number.md) | Center Y-coordinate (pixels) |
| `radius` | [Number](Number.md) | Radius (pixels) |

#### drawEllipse (x, y, width, height) →  {PIXI.Graphics}
Draws an ellipse and returns itself.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Center X-coordinate (pixels) |
| `y` | [Number](Number.md) | Center Y-coordinate (pixels) |
| `width` | [Number](Number.md) | Width (pixels) |
| `height` | [Number](Number.md) | Height (pixels) |

#### drawPolygon (path) →  {PIXI.Graphics}
Draws a polygon and returns itself.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `path` | [Array](Array.md).<[Number](Number.md)> \| [Array](Array.md).<[PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html)> \| [Array](Array.md).<[PIXI.Polygon](http://pixijs.download/v5.3.12/docs/PIXI.Polygon.html)> | Path |

#### drawRect (x, y, width, height) →  {PIXI.Graphics}
Draws a rectangle and returns itself.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Center X-coordinate (pixels) |
| `y` | [Number](Number.md) | Center Y-coordinate (pixels) |
| `width` | [Number](Number.md) | Width (pixels) |
| `height` | [Number](Number.md) | Height (pixels) |

#### drawRoundedRect (x, y, width, height, radius) →  {PIXI.Graphics}
Draws a rounded rectangle and returns itself.

##### Arguments

| Name     | Type                                             | Description                          |
|----------|--------------------------------------------------|--------------------------------------|
| `x`      | [Number](Number.md)                             | Center x-coordinate (in pixels)     |
| `y`      | [Number](Number.md)                             | Center y-coordinate (in pixels)     |
| `width`  | [Number](Number.md)                             | Width (in pixels)                   |
| `height` | [Number](Number.md)                             | Height (in pixels)                  |
| `radius` | [Number](Number.md)                             | Radius (in pixels)                  |


#### drawShape (shape) →  {PIXI.Graphics}
Draws the specified shape and returns itself.

##### Arguments

| Name   | Type                                                                                           | Description                             |
|--------|------------------------------------------------------------------------------------------------|-----------------------------------------|
| `shape`| [PIXI.Circle](http://pixijs.download/v5.3.12/docs/PIXI.Circle.html) \| [PIXI.Ellipse](http://pixijs.download/v5.3.12/docs/PIXI.Ellipse.html) \| [PIXI.Polygon](http://pixijs.download/v5.3.12/docs/PIXI.Polygon.html) \| [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html) \| [PIXI.RoundedRectangle](http://pixijs.download/v5.3.12/docs/PIXI.RoundedRectangle.html) | Object that specifies the shape to draw |


#### drawStar (x, y, points, radius, innerRadius opt, rotation opt) →  {PIXI.Graphics}
Draws a star-shaped figure and returns itself.

##### Arguments

| Name         | Type                | Optional | Description                          |
|--------------|---------------------|----------|--------------------------------------|
| `x`          | [Number](Number.md) |          | Center x-coordinate (in pixels)      |
| `y`          | [Number](Number.md) |          | Center y-coordinate (in pixels)      |
| `points`     | [Number](Number.md) |          | Number of points                     |
| `radius`     | [Number](Number.md) |          | Radius (in pixels)                   |
| `innerRadius`| [Number](Number.md) | Yes      | Inner radius (default: radius / 2 pixels) |
| `rotation`   | [Number](Number.md) | Yes      | Rotation angle (default: 0 radians) |


#### endFill () →  {PIXI.Graphics}
Ends the fill and returns itself.


#### endHole () →  {PIXI.Graphics}
Ends the hole drawing and returns itself.


#### finishPoly () →  {PIXI.Graphics}
Finishes the polygon and returns itself.


#### generateCanvasTexture (scaleMode, resolution) →  {[PIXI.Texture](PIXI.Texture.md)}
Generates and returns a texture with the specified settings.

##### Arguments

| Name         | Type                  | Description                         |
|--------------|-----------------------|-------------------------------------|
| `scaleMode`  | [Number](Number.md)   | [PIXI.SCALE_MODES](http://pixijs.download/v5.3.12/docs/PIXI.html#.SCALE_MODES) |
| `resolution`  | [Number](Number.md)   | Resolution                          |


#### isFastRect () →  {Boolean}
Checks if it is the first corner.


#### lineStyle (options opt) →  {PIXI.Graphics}
Sets the line style with the specified values and returns itself.

##### Arguments

| Name             | Type                | Optional | Description                            |
|------------------|---------------------|----------|----------------------------------------|
| `options`        | Object              | Yes      | See details below                     |
| `options.width`  | [Number](Number.md) | Yes      | Width (default: 0 pixels)            |
| `options.color`  | [Number](Number.md) | Yes      | Color (default: 0)                   |
| `options.alpha`  | [Number](Number.md) | Yes      | Opacity (default: 1)                 |
| `options.alignment` | [Number](Number.md) | Yes      | (default: 0.5)                      |
| `options.native` | Boolean             | Yes      | (default: false)                     |


#### lineTextureStyle (options opt) →  {PIXI.Graphics}
Sets the line texture style with the specified values and returns itself.

##### Arguments

| Name             | Type                                         | Optional | Description                             |
|------------------|----------------------------------------------|----------|-----------------------------------------|
| `options`        | Object                                       | Yes      | See details below                       |
| `options.width`  | [Number](Number.md)                          | Yes      | Width (default: 0 pixels)              |
| `options.texture`| [PIXI.Texture](PIXI.Texture.md)              | Yes      | Texture (default: PIXI.Texture.WHITE)   |
| `options.color`  | [Number](Number.md)                          | Yes      | Color (default: 0)                      |
| `options.alpha`  | [Number](Number.md)                          | Yes      | Opacity (default: 1)                    |
| `options.matrix` | [PIXI.Matrix](http://pixijs.download/v5.3.12/docs/PIXI.Matrix.html) | Yes      |                                         |
| `options.alignment` | [Number](Number.md)                        | Yes      | (default: 0.5)                        |
| `options.native` | Boolean                                      | Yes      | (default: false)                      |


#### lineTo (x, y) →  {PIXI.Graphics}
Draws a line to the specified coordinates and returns itself.

##### Arguments

| Name | Type                | Description                       |
|------|---------------------|-----------------------------------|
| `x`  | [Number](Number.md) | x-coordinate (in pixels)          |
| `y`  | [Number](Number.md) | y-coordinate (in pixels)          |


#### moveTo (x, y) →  {PIXI.Graphics}
Moves the drawing position to the specified coordinates and returns itself.

##### Arguments

| Name | Type                | Description                       |
|------|---------------------|-----------------------------------|
| `x`  | [Number](Number.md) | x-coordinate (in pixels)          |
| `y`  | [Number](Number.md) | y-coordinate (in pixels)          |


#### quadraticCurveTo (cpX, cpY, toX, toY) →  {PIXI.Graphics}
Draws a quadratic Bézier curve and returns itself.

##### Arguments

| Name | Type                | Description                       |
|------|---------------------|-----------------------------------|
| `cpX`| [Number](Number.md) | Control point x-coordinate (in pixels) |
| `cpY`| [Number](Number.md) | Control point y-coordinate (in pixels) |
| `toX`| [Number](Number.md) | x-coordinate (in pixels)          |
| `toY`| [Number](Number.md) | y-coordinate (in pixels)          |


#### setMatrix (matrix) →  {PIXI.Graphics}
Sets the matrix and returns itself.

##### Arguments

| Name    | Type                                           | Description     |
|---------|------------------------------------------------|------------------|
| `matrix`| [PIXI.Matrix](http://pixijs.download/v5.3.12/docs/PIXI.Matrix.html) | Matrix          |


#### startPoly ()
Begins the drawing of a polygon.
