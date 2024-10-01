# Class: PIXI.Sprite

## Superclass: [PIXI.Container](PIXI.Container.md)

The basic object for rendering. For more details, refer to the official PixiJS site [PIXI.Sprite](http://pixijs.download/v5.3.12/docs/PIXI.Sprite.html).

### new PIXI.Sprite (texture opt)
#### Arguments

| Name      | Type                             | Characteristics    | Description                                |
|-----------|----------------------------------|---------------------|--------------------------------------------|
| `texture` | [PIXI.Texture](PIXI.Texture.md) | <optional>          | The image to set for the sprite            |

### Subclass

* [Sprite](Sprite.md) 

### Properties

| Identifier   | Type                                                 | Description                                |
|--------------|------------------------------------------------------|--------------------------------------------|
| `shader`     | [PIXI.Filter](PIXI.Filter.md) \| [PIXI.Shader](PIXI.Shader.md) | [static] Shader                           |
| `anchor`     | [PIXI.ObservablePoint](http://pixijs.download/v5.3.12/docs/PIXI.ObservablePoint.html) | The reference point of coordinates (e.g., top-left {0, 0} / bottom-right {1, 1}) (default: `texture.defaultAnchor` or top-left) |
| `blendMode`  | [Number](Number.md)                                 | [Blend mode](Sprite.md#blend-mode) (default: `PIXI.BLEND_MODES.NORMAL`) |
| `isSprite`   | Boolean                                             | Is it a sprite?                            |
| `pluginName` | [String](String.md)                                | `PIXI.Renderer`'s `plugins` name (default: "batch") |
| `roundPixels`| Boolean                                             | Whether to round pixels (default: `PIXI.settings.ROUND_PIXELS`) |
| `texture`    | [PIXI.Texture](PIXI.Texture.md)                    | The image set for the sprite               |
| `tint`       | [Number](Number.md)                                | The color to tint (default: does not process if 0xffffff) |
| `_cachedTint`| [Number](Number.md)                                | Cached color (default: 0xffffff)           |
| `_tintedCanvas` | [HTMLCanvasElement](https://developer.mozilla.org/ja/docs/Web/API/HTMLCanvasElement) | The tinted canvas                          |

### Methods Inherited from Superclass

#### [PIXI.DisplayObject](PIXI.DisplayObject.md)

* [(static) mixin (source)](PIXI.DisplayObject.md#static-mixin-source)
* [\_recursivePostUpdateTransform ()](PIXI.DisplayObject.md#_recursivepostupdatetransform-)
* [displayObjectUpdateTransform ()](PIXI.DisplayObject.md#displayobjectupdatetransform-)
* [getBounds (skipUpdate, rect)](PIXI.DisplayObject.md#getbounds-skipupdate-rect--pixirectangle)
* [getGlobalPosition (point, skipUpdate)](PIXI.DisplayObject.md#getglobalposition-point-skipupdate--pixipoint)
* [setParent (container)](PIXI.DisplayObject.md#setparent-container--pixicontainer)
* [setTransform (x, y, scaleX, scaleY, rotation, skewX, skewY, pivotX, pivotY)](PIXI.DisplayObject.md#settransform-x-y-scalex-scaley-rotation-skewx-skewy-pivotx-pivoty--pixidisplayobject)
* [toGlobal (position, point, skipUpdate)](PIXI.DisplayObject.md#toglobal-position-point-skipupdate--pixipoint)
* [toLocal (position, from, point, skipUpdate)](PIXI.DisplayObject.md#tolocal-position-from-point-skipupdate--pixipoint)

#### [PIXI.Container](PIXI.Container.md)

* [\_renderCanvas (renderer)](PIXI.Container.md#_rendercanvas-renderer)
* [addChild (child)](PIXI.Container.md#addchild-child--pixidisplayobject)
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

#### (static) from (source, options opt) → {PIXI.Sprite}
Generates and returns a `PIXI.Sprite` based on the specified data.  
The `source` can be a [Number](Number.md) (frame ID), [String](String.md) (image or video URL), [PIXI.Texture](PIXI.Texture.md), [HTMLCanvasElement](https://developer.mozilla.org/ja/docs/Web/API/HTMLCanvasElement), or [HTMLVideoElement](https://developer.mozilla.org/ja/docs/Web/API/HTMLVideoElement).

##### Arguments

| Name     | Type | Characteristics | Description                     |
|----------|------|------------------|---------------------------------|
| `source` | *    |                  | The data to generate from       |
| `options`| Object | <optional>     | Same format as the options for the [PIXI.BaseTexture](http://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html) constructor |

#### _calculateBounds ()
Overrides: [PIXI.Container](PIXI.Container.md#_calculatebounds-)

#### _render (renderer)
Overrides: [PIXI.Container](PIXI.Container.md#_render-renderer)

#### calculateTrimmedVertices ()
Calculates the trimmed vertex data.

#### calculateVertices ()
Calculates the vertex data.

#### containsPoint (point) → {Boolean}
Checks if the specified coordinates are contained.

##### Arguments

| Name   | Type                                         | Description     |
|--------|----------------------------------------------|------------------|
| `point`| [PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html) | Coordinates        |

#### destroy (options)
Overrides: [PIXI.Container](PIXI.Container.md#destroy-options)

#### getLocalBounds (rect) → {PIXI.Rectangle}
Overrides: [PIXI.DisplayObject](PIXI.DisplayObject.md#getlocalbounds-rect--pixirectangle)

#### renderCanvas (renderer)
Overrides: [PIXI.Container](PIXI.Container.md#rendercanvas-renderer)
