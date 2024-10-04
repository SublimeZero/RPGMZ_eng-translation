[Class Tree](index.md)

# Class: Spriteset_Base

## Superclass: [Sprite](Sprite.md)

A class used to combine multiple sprites.

Changes were made in versions v1.1.1 and v1.2.0.

Related Classes: [Sprite_Picture](Sprite_Picture.md)

---

### new Spriteset_Base ()

---

### Subclasses

* [Spriteset_Battle](Spriteset_Battle.md)
* [Spriteset_Map](Spriteset_Map.md)

---

### Properties

| Identifier         | Type                      | Description        |
| ------------------ | ------------------------- | ------------------ |
| `_baseSprite`      | [Sprite](Sprite.md)       | The base sprite     |
| `_blackScreen`     | [ScreenSprite](ScreenSprite.md) | Black background  |
| `_pictureContainer` | [Sprite](Sprite.md)       | Picture container    |
| `_timerSprite`     | [Sprite_Timer](Sprite_Timer.md) | Timer sprite       |

---

### Deprecated MV Properties
`_flashSprite`, `_fadeSprite`, `_tone`, `_toneFilter`, `_toneSprite`

---

### Methods inherited from the superclass

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

---

### Methods

---

#### animationBaseDelay () → {[Number](Number.md)}
**@MZ** Returns the base delay time (default: 8).

---

#### animationNextDelay () → {[Number](Number.md)}
**@MZ** Returns the next delay time (default: 12).

---

#### animationShouldMirror (target) → {Boolean}
**@MZ** Checks if the animation needs to be mirrored.

##### Parameters

| Name    | Type                              | Description     |
| ------- | --------------------------------- | ---------------- |
| `target` | [Game_Character](Game_Character.md) | The character    |

---

#### createAnimation (request)
**@MZ** Generates an animation.

##### Parameters

| Name     | Type                                      | Description            |
| -------- | ----------------------------------------- | ---------------------- |
| `request` | [MV.AnimationRequest](MV.AnimationRequest.md) | Animation settings      |

---

#### createAnimationSprite (targets, animation, mirror, delay)
**@MZ** Generates an animation sprite.

##### Parameters

| Name                | Type                                                    | Description          |
| ------------------- | ------------------------------------------------------- | -------------------- |
| `_animationSprites` | [Array](Array.md).&lt;[Sprite](Sprite.md)&gt;        | **@MZ** Animation sprites |
| `targets`          | [Array](Array.md).&lt;[Game_Character](Game_Character.md)&gt; | The targets          |
| `animation`        | [RPG.Animation](RPG.Animation.md)                      | Animation data       |
| `mirror`           | Boolean                                               | Whether to mirror    |
| `delay`            | [Number](Number.md)                                  | Duration             |

---

#### createBaseFilters ()
**@MZ** Generates the base filters.

---

#### createBaseSprite ()
Generates the base sprite.

---

#### createCanvasToneChanger ()
Generates canvas tone changer.

---

#### createLowerLayer ()
Generates the lower layer containing the base sprite.

---

#### createOverallFilters ()
**@MZ** Generates the overall filters.

---

#### createPictures ()
Generates image sprites.

---

#### createTimer ()
Generates the timer sprite.

---

#### createUpperLayer ()
Generates the upper layer containing images, timers, and screen sprites.

---

#### destroy ()
**@MZ** Override: [Sprite](Sprite.md#destroy-)

---

#### findTargetSprite (target) → {[Sprite](Sprite.md)}
**@MZ** Searches for and returns the sprite associated with the specified character.

##### Parameters

| Name    | Type                              | Description     |
| ------- | --------------------------------- | ---------------- |
| `target` | [Game_Character](Game_Character.md) | The character    |

---

#### initialize ()
Override: [Sprite](Sprite.md#initialize-)

---

#### isAnimationForEach (animation) → {Boolean}
**@MZ** Checks if the specified animation data is for each target.

##### Parameters

| Name       | Type                              | Description          |
| ---------- | --------------------------------- | -------------------- |
| `animation` | [RPG.Animation](RPG.Animation.md) | Animation data       |

---

#### isAnimationPlaying ()
**@MZ** Checks if the animation is currently playing.

---

#### isMVAnimation (animation) → {Boolean}
**@MZ** Checks if the specified animation data is an MV animation.

##### Parameters

| Name       | Type                              | Description          |
| ---------- | --------------------------------- | -------------------- |
| `animation` | [RPG.Animation](RPG.Animation.md) | Animation data       |

---

#### lastAnimationSprite () → {[Sprite](Sprite.md)}
**@MZ** Returns the last animation sprite.  
Either [Sprite_Animation](Sprite_Animation.md) or [Sprite_AnimationMV](Sprite_AnimationMV.md)

---

#### loadSystemImages ()
**@MZ** Loads system images.

---

#### makeTargetSprites (targets) → {[Array](Array.md).&lt;[Sprite](Sprite.md)&gt;}
**@MZ** Searches for and returns the specified sprites.

##### Parameters

| Name    | Type                              | Description     |
| ------- | --------------------------------- | ---------------- |
| `targets` | [Array](Array.md).&lt;[Game_Character](Game_Character.md)&gt; | The targets      |

---

#### pictureContainerRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangle area of the drawing area.

---

#### processAnimationRequests ()
**@MZ** Executes the requested animations.

---

#### removeAllAnimations ()
**@MZ** Removes all animation sprites.

---

#### removeAnimation (sprite)
**@MZ** Removes the specified animation sprite.

##### Parameters

| Name    | Type                              | Description     |
| ------- | --------------------------------- | ---------------- |
| `sprite` | [Sprite](Sprite.md)              | The sprite to remove |

---

#### update ()
Override: [Sprite](Sprite.md#update-)

---

#### updateAnimations ()
**@MZ** Updates the animations.

---

#### updateBaseFilters ()
**@MZ** Updates the base filters.

---

#### updateOverallFilters ()
**@MZ** Updates the overall filters.

---

#### updatePosition ()
Updates the position.

---

### Deprecated MV Methods
createScreenSprites (), createToneChanger (), createWebGLToneChanger (), updateCanvasToneChanger (), updateScreenSprites (), updateToneChanger (), updateWebGLToneChanger ()
