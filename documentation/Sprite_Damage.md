[Class Tree](index.md)

# Class: Sprite_Damage

## Superclass: [Sprite](Sprite.md)

A sprite that displays damage numbers as a popup.

In MV, the damage was displayed using images, but in MZ, it utilizes fonts.

Related classes: [Sprite_Animation](Sprite_Animation.md), [Sprite_Battler](Sprite_Battler.md)

### `new Sprite_Damage()`

### Properties

| Identifier       | Type                                  | Description                                                        |
|------------------|---------------------------------------|--------------------------------------------------------------------|
| `_colorType`     | [Number](Number.md)                  | **@MZ** Damage type (0: HP↓, 1: HP↑, 2: MP↓, 3: MP↑)             |
| `_duration`      | [Number](Number.md)                  | Duration                                                          |
| `_flashColor`    | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of flash colors [ Red, Green, Blue, Intensity ]            |
| `_flashDuration`  | [Number](Number.md)                  | Flash duration [time] (in 1/15 second units)                     |

### Deprecated MV Properties
`_damageBitmap` 

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

### Methods

#### `createBitmap(width, height) → {[Bitmap](Bitmap.md)}`
**@MZ** Generates and returns a bitmap.

##### Arguments

| Name     | Type                  | Description         |
|----------|-----------------------|---------------------|
| `width`  | [Number](Number.md)   | Width (in pixels)   |
| `height` | [Number](Number.md)   | Height (in pixels)  |

---

#### `createChildSprite(width, height) → {[Sprite](Sprite.md)}`
Generates a damage image sprite and adds it as a child, returning the sprite.

##### Arguments

| Name     | Type                  | Description         |
|----------|-----------------------|---------------------|
| `width`  | [Number](Number.md)   | Width (in pixels)   |
| `height` | [Number](Number.md)   | Height (in pixels)  |

---

#### `createDigits(value)`
Generates a number sprite at the specified row position.  
The `baseRow` argument from MV has been deprecated.

##### Arguments

| Name     | Type                  | Description         |
|----------|-----------------------|---------------------|
| `value`  | [Number](Number.md)   | Numeric value       |

---

#### `createMiss()`
Generates a miss sprite.

---

#### `damageColor() → {[MV.CssColor](MV.CssColor.md)}`
**@MZ** Returns the color of the damage value.

---

#### `destroy()`
**@MZ** Override: [Sprite](Sprite.md#destroy-)

---

#### `fontFace() → {[String](String.md)}`
**@MZ** Returns a string of the numeric font names, concatenated with commas.

---

#### `fontSize() → {[Number](Number.md)}`
**@MZ** Returns the numeric font size.

---

#### `initialize()`
Override: [Sprite](Sprite.md#initialize-)

---

#### `isPlaying() → {Boolean}`
Checks if the sprite is currently playing.

---

#### `outlineColor() → {[MV.CssColor](MV.CssColor.md)}`
**@MZ** Returns the outline color of the damage value (default: "rgba(0, 0, 0, 0.7)").

---

#### `outlineWidth() → {[Number](Number.md)}`
**@MZ** Returns the outline width of the damage value (default: 4).

---

#### `setup(target)`
Prepares for the target.

##### Arguments

| Name     | Type                     | Description         |
|----------|--------------------------|---------------------|
| `target` | [Game_Actor](Game_Actor.md) | Target actor        |

---

#### `setupCriticalEffect()`
Prepares for the critical effect.

---

#### `update()`
Override: [Sprite](Sprite.md#update-)

---

#### `updateChild(sprite)`
Updates the specified child sprite.

##### Arguments

| Name     | Type                  | Description         |
|----------|-----------------------|---------------------|
| `sprite` | [Sprite](Sprite.md)   | Child sprite        |

---

#### `updateFlash()`
Updates the flash effect.

---

#### `updateOpacity()`
Updates the opacity.

---

### Deprecated MV Methods
`digitHeight()`, `digitWidth()`
