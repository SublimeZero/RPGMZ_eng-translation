[Class Tree](index.md)

# Class: Sprite_Battler

## Superclass: [Sprite_Clickable](Sprite_Clickable.md)

The character image displayed in the battle scene.

In MV, the superclass was `Sprite_Base`, but it has been changed to [Sprite_Clickable](Sprite_Clickable.md).

### new Sprite_Battler (battler opt)
#### Arguments

| Name      | Type                          | Attributes        | Description    |
|-----------|-------------------------------|-------------------|----------------|
| `battler` | [Game_Battler](Game_Battler.md) | &lt;optional&gt;  | The battler    |

### Subclasses

- [Sprite_Actor](Sprite_Actor.md)
- [Sprite_Enemy](Sprite_Enemy.md)

### Properties

| Identifier              | Type                                                 | Description                                   |
|-------------------------|------------------------------------------------------|-----------------------------------------------|
| `_battler`               | [Game_Battler](Game_Battler.md)                      | The battler                                   |
| `_damages`               | [Array](Array.md).&lt;[Sprite_Damage](Sprite_Damage.md)&gt; | For damage pop-ups                           |
| `_homeX`                 | [Number](Number.md)                                  | The x-coordinate of the home position         |
| `_homeY`                 | [Number](Number.md)                                  | The y-coordinate of the home position         |
| `_offsetX`               | [Number](Number.md)                                  | x-offset                                      |
| `_offsetY`               | [Number](Number.md)                                  | y-offset                                      |
| `_targetOffsetX`         | [Number](Number.md)                                  | Target's x-offset                             |
| `_targetOffsetY`         | [Number](Number.md)                                  | Target's y-offset                             |
| `_movementDuration`      | [Number](Number.md)                                  | Duration of movement                          |
| `_selectionEffectCount`  | [Number](Number.md)                                  | Count of the selection effect                 |

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

#### [Sprite_Clickable](Sprite_Clickable.md)

* [hitTest (x, y)](Sprite_Clickable.md#hittest-x-y--boolean)
* [isBeingTouched ()](Sprite_Clickable.md#isbeingtouched---boolean)
* [isClickEnabled ()](Sprite_Clickable.md#isclickenabled---boolean)
* [isPressed ()](Sprite_Clickable.md#ispressed---boolean)
* [onMouseExit ()](Sprite_Clickable.md#onmouseexit-)
* [processTouch ()](Sprite_Clickable.md#processtouch-)

### Methods

#### checkBattler (battler) → {Boolean}
**@MZ** Checks if the specified battler is the same.

##### Arguments

| Name     | Type                               | Description      |
|----------|------------------------------------|------------------|
| `battler`| [Game_Battler](Game_Battler.md)    | The battler      |

#### createDamageSprite ()
**@MZ** Creates a damage sprite.

#### damageOffsetX () → {[Number](Number.md)}
Returns the x-offset of the damage.

#### damageOffsetY () → {[Number](Number.md)}
Returns the y-offset of the damage.

#### destroyDamageSprite ()
**@MZ** Destroys the damage sprite.

#### inHomePosition () → {Boolean}
Checks if the sprite is in its home position.

#### initialize ()
Overrides: [Sprite_Clickable](Sprite_Clickable.md#initialize-)

#### initMembers ()
Initializes member variables.

#### isEffecting () → {Boolean}
Checks if an effect is applied (always false).

#### isMoving () → {Boolean}
Checks if the sprite is moving.

#### mainSprite () → {[Sprite_Battler](Sprite_Battler.md)}
**@MZ** Returns the reference to the sprite (default: `this`).

#### onClick ()
**@MZ** Overrides: [Sprite_Clickable](Sprite_Clickable.md#onclick-)

#### onMouseEnter ()
**@MZ** Overrides: [Sprite_Clickable](Sprite_Clickable.md#onmouseenter-)

#### onMoveEnd ()
Handles the event when the move ends.

#### onPress ()
**@MZ** Overrides: [Sprite_Clickable](Sprite_Clickable.md#onpress-)

#### setBattler (battler)
Sets the battler.

##### Arguments

| Name     | Type                               | Description      |
|----------|------------------------------------|------------------|
| `battler`| [Game_Battler](Game_Battler.md)    | The battler      |

#### setHome (x, y)
Sets the home position.

##### Arguments

| Name | Type                        | Description           |
|------|-----------------------------|-----------------------|
| `x`  | [Number](Number.md)          | The home x-coordinate  |
| `y`  | [Number](Number.md)          | The home y-coordinate  |

#### setupDamagePopup ()
Prepares the damage popup.

#### startMove (x, y, duration)
Starts moving to the specified coordinates.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `x`       | [Number](Number.md)          | Target x-coordinate         |
| `y`       | [Number](Number.md)          | Target y-coordinate         |
| `duration`| [Number](Number.md)          | Duration of the movement    |

#### update ()
Overrides: [Sprite_Clickable](Sprite_Clickable.md#update-)

#### updateBitmap ()
Updates the sprite's bitmap.

#### updateDamagePopup ()
Updates the damage popup.

#### updateFrame ()
Updates the frame.

#### updateMain ()
Updates the main state.

#### updateMove ()
Updates the movement.

#### updatePosition ()
Updates the position.

#### updateSelectionEffect ()
Updates the selection effect.

#### updateVisibility ()
Overrides: [Sprite](Sprite.md#updateVisibility-)

### Deprecated MV Methods
`updateAnimation()`, `setupAnimation()`
