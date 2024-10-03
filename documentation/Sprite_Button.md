[Class Tree](index.md)

# Class: Sprite_Button

## Superclass: [Sprite_Clickable](Sprite_Clickable.md)

A sprite used for displaying buttons.

In MV, it was a subclass of [Sprite](Sprite.md), but in MZ, it inherits from [Sprite_Clickable](Sprite_Clickable.md).

Related Classes: [Window_ShopNumber](Window_ShopNumber.md), [Window_NumberInput](Window_NumberInput.md)

### new Sprite_Button (buttonType)
#### Arguments

| Name         | Type                           | Description                                       |
|--------------|--------------------------------|--------------------------------------------------|
| `buttonType` | [String](String.md)            | **@MZ** The [type of button](#Button_Types)       |

### Properties

| Identifier     | Type                           | Description                                |
|----------------|--------------------------------|--------------------------------------------|
| `_buttonType`  | [String](String.md)            | **@MZ** The [type of button](#Button_Types)|
| `_coldFrame`   | [Rectangle](Rectangle.md)      | The display frame                          |
| `_hotFrame`    | [Rectangle](Rectangle.md)      | The touch/click response frame             |
| `_clickHandler`| Function                       | The handler called on touch/click          |

### Button Types

| String     | Description                      |
|------------|-----------------------------------|
| "cancel"   | Cancel                            |
| "pageup"   | Page Up                           |
| "pagedown" | Page Down                         |
| "down"     | Down                              |
| "up"       | Up                                |
| "down2"    | Down 2                            |
| "up2"      | Up 2                              |
| "ok"       | OK                                |
| "menu"     | Menu                              |

### Deprecated MV Property
`_touching`

### Methods Inherited from Superclass

The following methods are inherited from [Sprite_Clickable](Sprite_Clickable.md):
- `initialize()`
- `update()`
- `onClick()`
- `onMouseEnter()`
- `onMouseExit()`
- `onPress()`
- `onRelease()`

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
* [_renderCanvas (renderer)](PIXI.Container.md#_rendercanvas-renderer)
* [setChildIndex (child, index)](PIXI.Container.md#setchildindex-child-index)
* [sortChildren ()](PIXI.Container.md#sortchildren-)
* [swapChildren (child, child2)](PIXI.Container.md#swapchildren-child-child2)
* [updateTransform ()](PIXI.Container.md#updatetransform-)

#### [PIXI.Sprite](PIXI.Sprite.md)

* [(static) from (source, options)](PIXI.Sprite.md#static-from-source-options--pixisprite)
* [\_calculateBounds ()](PIXI.Sprite.md#_calculatebounds-)
* [\_render (renderer)](PIXI.Sprite.md#_render-renderer)
* [calculateTrimmedVertices ()](PIXI.Sprite.md#calculatetrimmedvertices-)
* [calculateVertices ()](PIXI.Sprite.md#calculatevertices-)
* [containsPoint (point)](PIXI.Sprite.md#containspoint-point--boolean)
* [getLocalBounds (rect)](PIXI.Sprite.md#getlocalbounds-rect--pixirectangle)
* [renderCanvas (renderer)](PIXI.Sprite.md#rendercanvas-renderer)

#### [Sprite](Sprite.md)

* [destroy ()](Sprite.md#destroy-)
* [getBlendColor ()](Sprite.md#getblendcolor---mvcolor)
* [getColorTone ()](Sprite.md#getcolortone---mvcolor)
* [hide ()](Sprite.md#hide-)
* [move (x, y)](Sprite.md#Sprite.md#move-x-y)
* [setBlendColor (color)](Sprite.md#setblendcolor-color)
* [setColorTone (tone)](Sprite.md#setcolortone-tone)
* [setFrame (x, y, width, height)](Sprite.md#setframe-x-y-width-height)
* [setHue (hue)](Sprite.md#sethue-hue)
* [show ()](Sprite.md#show-)
* [updateVisibility ()](Sprite.md#updatevisibility-)

#### [Sprite_Clickable](Sprite_Clickable.md)

* [hitTest (x, y)](Sprite_Clickable.md#hittest-x-y--boolean)
* [isBeingTouched ()](Sprite_Clickable.md#isbeingtouched---boolean)
* [isClickEnabled ()](Sprite_Clickable.md#isclickenabled---boolean)
* [isPressed ()](Sprite_Clickable.md#ispressed---boolean)
* [onMouseEnter ()](Sprite_Clickable.md#onmouseenter-)
* [onMouseExit ()](Sprite_Clickable.md#onmouseexit-)
* [onPress ()](Sprite_Clickable.md#onpress-)
* [processTouch ()](Sprite_Clickable.md#processtouch-)

### Methods

#### blockHeight () → {number}
**@MZ** Returns the height of the block (default: 48 pixels).

#### blockWidth () → {number}
**@MZ** Returns the width of the block (default: 48 pixels).

#### buttonData () → {Object}
**@MZ** Returns data according to the button type, formatted as `{ x: xPosition, w: width }` (in block units).

#### checkBitmap ()
**@MZ** Checks the image and throws an error if the size is too small.

#### initialize ()
Overrides: [Sprite_Clickable](Sprite_Clickable.md#initialize-)

#### loadButtonImage ()
**@MZ** Loads the button image.

#### onClick ()
**@MZ** Overrides: [Sprite_Clickable](Sprite_Clickable.md#onclick-)

#### setClickHandler (method)
Sets the click handler.

##### Arguments

| Name    | Type     | Description         |
|---------|----------|---------------------|
| `method`| Function | The click handler   |

#### setColdFrame (x, y, width, height)
Sets the cold (inactive) frame.

##### Arguments

| Name    | Type      | Description            |
|---------|-----------|------------------------|
| `x`     | [Number](Number.md)  | x-coordinate (pixels)  |
| `y`     | [Number](Number.md)  | y-coordinate (pixels)  |
| `width` | [Number](Number.md)  | Width (pixels)         |
| `height`| [Number](Number.md)  | Height (pixels)        |

#### setHotFrame (x, y, width, height)
Sets the hot (active) frame.

##### Arguments

| Name    | Type      | Description            |
|---------|-----------|------------------------|
| `x`     | [Number](Number.md)  | x-coordinate (pixels)  |
| `y`     | [Number](Number.md)  | y-coordinate (pixels)  |
| `width` | [Number](Number.md)  | Width (pixels)         |
| `height`| [Number](Number.md)  | Height (pixels)        |

#### setupFrames ()
**@MZ** Prepares the frames.

#### update ()
Overrides: [Sprite_Clickable](Sprite_Clickable.md#update-)

#### updateFrame ()
Updates the button frame.

#### updateOpacity ()
**@MZ** Updates the opacity.

### Deprecated MV Methods
- `callClickHandler ()`
- `canvasToLocalX (x)`
- `canvasToLocalY (y)`
- `isActive ()`
- `isButtonTouched ()`
- `processTouch ()`
### Methods

#### blockHeight () → {number}
**@MZ** Returns the height of the block (default: 48 pixels).

#### blockWidth () → {number}
**@MZ** Returns the width of the block (default: 48 pixels).

#### buttonData () → {Object}
**@MZ** Returns data according to the button type, formatted as `{ x: xPosition, w: width }` (in block units).

#### checkBitmap ()
**@MZ** Checks the image and throws an error if the size is too small.

#### initialize ()
Overrides: [Sprite_Clickable](Sprite_Clickable.md#initialize-)

#### loadButtonImage ()
**@MZ** Loads the button image.

#### onClick ()
**@MZ** Overrides: [Sprite_Clickable](Sprite_Clickable.md#onclick-)

#### setClickHandler (method)
Sets the click handler.

##### Arguments

| Name    | Type     | Description         |
|---------|----------|---------------------|
| `method`| Function | The click handler   |

#### setColdFrame (x, y, width, height)
Sets the cold (inactive) frame.

##### Arguments

| Name    | Type      | Description            |
|---------|-----------|------------------------|
| `x`     | [Number](Number.md)  | x-coordinate (pixels)  |
| `y`     | [Number](Number.md)  | y-coordinate (pixels)  |
| `width` | [Number](Number.md)  | Width (pixels)         |
| `height`| [Number](Number.md)  | Height (pixels)        |

#### setHotFrame (x, y, width, height)
Sets the hot (active) frame.

##### Arguments

| Name    | Type      | Description            |
|---------|-----------|------------------------|
| `x`     | [Number](Number.md)  | x-coordinate (pixels)  |
| `y`     | [Number](Number.md)  | y-coordinate (pixels)  |
| `width` | [Number](Number.md)  | Width (pixels)         |
| `height`| [Number](Number.md)  | Height (pixels)        |

#### setupFrames ()
**@MZ** Prepares the frames.

#### update ()
Overrides: [Sprite_Clickable](Sprite_Clickable.md#update-)

#### updateFrame ()
Updates the button frame.

#### updateOpacity ()
**@MZ** Updates the opacity.

### Deprecated MV Methods
- `callClickHandler ()`
- `canvasToLocalX (x)`
- `canvasToLocalY (y)`
- `isActive ()`
- `isButtonTouched ()`
- `processTouch ()`
