[Class Tree](index.md)

# Class: Sprite_Enemy

## Extends: [Sprite_Battler](Sprite_Battler.md)

| Database | JSON Data | Object |
| --- | --- | --- |
| [Enemy Character] | [RPG.Enemy](RPG.Enemy.md) | [Game_Enemy](Game_Enemy.md) |

Sprite for displaying [Enemy Character].

Changed in v1.0.2.

Related Classes: [Spriteset_Battle](Spriteset_Battle.md), [Game_Troop](Game_Troop.md)

### new Sprite_Enemy (enemy opt)
#### Arguments

| Name    | Type                        | Traits       | Description  |
| ------- | --------------------------- | ------------ | ------------ |
| `enemy` | [Game_Enemy](Game_Enemy.md) | <optional>   | [Enemy Character] |

### Properties

| Identifier         | Type                       | Description                 |
| ------------------ | -------------------------- | --------------------------- |
| `_enemy`           | [Game_Enemy](Game_Enemy.md) | Data of the [Enemy Character] |
| `_appeared`       | Boolean                    | Whether it has appeared     |
| `_battlerName`    | [String](String.md)        | Image file name (excluding extension) |
| `_battlerHue`     | [Number](Number.md)        | Hue (0-360)                 |
| `_effectType`     | [String](String.md)        | Effect type                 |
| `_effectDuration`  | [Number](Number.md)        | Effect duration             |
| `_shake`          | [Number](Number.md)        | Whether it is shaking       |
| `_stateIconSprite` | [Sprite_StateIcon](Sprite_StateIcon.md) | State icon               |

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
* [show ()](Sprite.md#show-)

#### [Sprite_Clickable](Sprite_Clickable.md)

* [hitTest (x, y)](Sprite_Clickable.md#hittest-x-y--boolean)
* [isBeingTouched ()](Sprite_Clickable.md#isbeingtouched---boolean)
* [isClickEnabled ()](Sprite_Clickable.md#isclickenabled---boolean)
* [isPressed ()](Sprite_Clickable.md#ispressed---boolean)
* [onMouseExit ()](Sprite_Clickable.md#onmouseexit-)
* [processTouch ()](Sprite_Clickable.md#processtouch-)

####  [Sprite_Battler](Sprite_Battler.md)

* [checkBattler (battler)](Sprite_Battler.md#checkbattler-battler--boolean)
* [createDamageSprite ()](Sprite_Battler.md#createdamagesprite-)
* [destroyDamageSprite ()](Sprite_Battler.md#destroydamagesprite-)
* [inHomePosition ()](Sprite_Battler.md#inhomeposition---boolean)
* [isMoving ()](Sprite_Battler.md#ismoving---boolean)
* [mainSprite ()](Sprite_Battler.md#mainsprite---sprite_battler)
* [onClick ()](Sprite_Battler.md#onclick-)
* [onMouseEnter ()](Sprite_Battler.md#onmouseenter-)
* [onMoveEnd ()](Sprite_Battler.md#onmoveend-)
* [onPress ()](Sprite_Battler.md#onpress-)
* [setHome (x, y)](Sprite_Battler.md#sethome-x-y)
* [setupDamagePopup ()](Sprite_Battler.md#setupdamagepopup-)
* [startMove (x, y, duration)](Sprite_Battler.md#startmove-x-y-duration)
* [updateDamagePopup ()](Sprite_Battler.md#updatedamagepopup-)
* [updateMain ()](Sprite_Battler.md#updateMain-)
* [updateMove ()](Sprite_Battler.md#updateMove-)
* [updateSelectionEffect ()](Sprite_Battler.md#updateselectioneffect-)
* [updateVisibility ()](Sprite_Battler.md#updatevisibility-)

### Methods

#### createStateIconSprite ()
  

---

#### damageOffsetX () → {[Number](Number.md)}
Overrides: [Sprite_Battler](Sprite_Battler.md#damageoffsetx---number)

---

#### damageOffsetY () → {[Number](Number.md)}
Overrides: [Sprite_Battler](Sprite_Battler.md#damageoffsety---number)

---

#### initialize (battler)
Overrides: [Sprite_Battler](Sprite_Battler.md#initialize-)

##### Arguments

| Name     | Type                      | Description |
| -------- | ------------------------- | ----------- |
| `battler`| [Game_Enemy](Game_Enemy.md) |           |

---

#### initMembers ()
Overrides: [Sprite_Battler](Sprite_Battler.md#initmembers-)

---

#### initVisibility ()
Initializes the visibility state.

---

#### isEffecting () → {Boolean}
Overrides: [Sprite_Battler](Sprite_Battler.md#iseffecting---boolean)

---

#### loadBitmap (name, hue)
Loads the specified bitmap image.

##### Arguments

| Name  | Type                      | Description |
| ----- | ------------------------- | ----------- |
| `name`| [String](String.md)       | File name (excluding extension) |
| `hue` | [Number](Number.md)       | Hue (0-360) |

---

#### revertToNormal ()
Resets the state to normal.

---

#### setBattler (battler)
Overrides: [Sprite_Battler](Sprite_Battler.md#setbattler-battler)

---

#### setHue (hue)
**@MZ** Overrides: [Sprite](Sprite.md#sethue-hue)

---

#### setupEffect ()
Prepares the effect.

---

#### startAppear ()
Starts the appearance.

---

#### startBlink ()
Starts the blinking.

---

#### startBossCollapse ()
Starts the [disappearance effect - boss].

---

#### startCollapse ()
Starts the [disappearance effect - normal].

---

#### startDisappear ()
Starts the disappearance.

---

#### startEffect (effectType)
Starts the specified effect.

The effect types are 'appear', 'disappear', 'whiten', 'blink', 'collapse', 'bossCollapse', 'instantCollapse'.

##### Arguments

| Name         | Type                      | Description |
| ------------ | ------------------------- | ----------- |
| `effectType` | [String](String.md)       | Effect type |

---

#### startInstantCollapse ()
Starts the [disappearance effect - instant collapse].

---

#### startWhiten ()
Starts the transition to white.

---

#### update ()
Overrides: [Sprite_Battler](Sprite_Battler.md#update-)

---

#### updateAppear ()
Updates the appearance effect.

---

#### updateBitmap ()
Overrides: [Sprite_Battler](Sprite_Battler.md#updatebitmap-)

---

#### updateBlink ()
Updates the blinking.

---

#### updateBossCollapse ()
Updates the [disappearance effect - boss].

---

#### updateCollapse ()
Updates the [disappearance effect - normal].

---

#### updateDisappear ()
Updates the disappearance effect.

---

#### updateEffect ()
Updates the effect.

---

#### updateFrame ()
Overrides: [Sprite_Battler](Sprite_Battler.md#updateframe-)

---

#### updateInstantCollapse ()
Updates the [disappearance effect - instant collapse].

---

#### updatePosition ()
Overrides: [updatePosition ()](Sprite_Battler.md#updateposition-)

---

#### updateStateSprite ()
Updates the state sprite.

---

#### updateWhiten ()
Updates the white effect.
