# Class: ScreenSprite

## Superclass: [PIXI.Container](PIXI.Container.md)

Sprite for effects like fades that cover the entire screen.

Related Classes: [Spriteset_Base](Spriteset_Base.md)

### new ScreenSprite ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `opacity` | [Number](Number.md) | Opacity (0-255) |
| `_graphics` | [PIXI.Graphics](PIXI.Graphics.md) | Image management object |
| `_red` | [Number](Number.md) | Red (0-255) |
| `_green` | [Number](Number.md) | Green (0-255) |
| `_blue` | [Number](Number.md) | Blue (0-255) |

### Deprecated MV Properties
`YEPWarned`, `anchor`, `blendMode`, `_colorText`

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
* [\_calculateBounds ()](PIXI.Container.md#_calculatebounds-)
* [\_render (renderer)](PIXI.Container.md#_render-renderer)
* [addChild (child)](PIXI.Container.md#addchild-child--pixidisplayobject)
* [addChildAt (child, index)](PIXI.Container.md#addchildat-child-index--pixidisplayobject)
* [calculateBounds ()](PIXI.Container.md#calculatebounds-)
* [destroy (options)](PIXI.Container.md#destroy-options)
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

#### destroy ()
**@MZ** Disposes of the object.

#### initialize ()
Initialization during object creation.

#### setBlack ()
Sets to black.

#### setColor (r, g, b)
Sets to the specified color.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `r` | [Number](Number.md) | Red (0-255) |
| `g` | [Number](Number.md) | Green (0-255) |
| `b` | [Number](Number.md) | Blue (0-255) |

#### setWhite ()
Sets to white.

### Deprecated MV Methods
[static] warnYep ()
