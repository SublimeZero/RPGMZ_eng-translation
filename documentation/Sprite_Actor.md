[Class Tree](index.md)

# Class: Sprite_Actor

## Superclass: [Sprite_Battler](Sprite_Battler.md)

| Database | JSON Data        | Object              |
|----------|------------------|---------------------|
| [Enemy Character] | [RPG.Actor](RPG.Actor.md) | [Game_Actor](Game_Actor.md) |

Sprite for displaying actors in a side view.

Changes made in V1.2.1.

Related Class: [Spriteset_Battle](Spriteset_Battle.md)

### new Sprite_Actor (actor opt)
#### Arguments

| Name   | Type                | Trait      | Description          |
|--------|---------------------|------------|----------------------|
| `actor`| [Game_Actor](Game_Actor.md) | &lt;optional&gt; | Actor object         |

### Properties

| Identifier       | Type                | Description                                     |
|------------------|---------------------|-------------------------------------------------|
| `MOTIONS`        | Object              | See [static] [MOTIONS](Sprite_Actor.md#motions) for details |
| `_battlerName`   | [String](String.md) | Name of the SV image file (excluding the extension) |
| `_motion`        | [MV.Motion](MV.Motion.md) | Current motion                              |
| `_motionCount`   | [Number](Number.md) | Motion counter                                 |
| `_pattern`       | [Number](Number.md) | Motion pattern                                 |
| `_mainSprite`    | [Sprite](Sprite.md) | Main sprite                                    |
| `_shadowSprite`  | [Sprite](Sprite.md) | Shadow sprite                                   |
| `_weaponSprite`  | [Sprite_Weapon](Sprite_Weapon.md) | Weapon sprite                             |
| `_stateSprite`   | [Sprite_StateOverlay](Sprite_StateOverlay.md) | State sprite                             |
| `_actor`         | [Game_Actor](Game_Actor.md) | The originating actor                      |

###### MOTIONS
Constants for specifying motions in the side view.<br />
For example, it can be used as <code>Sprite_Actor.MOTIONS.walk</code>.

| Identifier | Type                | Description     |
|------------|---------------------|------------------|
| walk       | [MV.Motion](MV.Motion.md) | Walking        |
| wait       | [MV.Motion](MV.Motion.md) | Waiting        |
| chant      | [MV.Motion](MV.Motion.md) | Chanting       |
| guard      | [MV.Motion](MV.Motion.md) | Guarding       |
| damage     | [MV.Motion](MV.Motion.md) | Taking damage  |
| evade      | [MV.Motion](MV.Motion.md) | Evading        |
| thrust     | [MV.Motion](MV.Motion.md) | Thrusting      |
| swing      | [MV.Motion](MV.Motion.md) | Swinging       |
| missile    | [MV.Motion](MV.Motion.md) | Ranged attack  |
| skill      | [MV.Motion](MV.Motion.md) | Using skill    |
| spell      | [MV.Motion](MV.Motion.md) | Casting spell   |
| item       | [MV.Motion](MV.Motion.md) | Using item     |
| escape     | [MV.Motion](MV.Motion.md) | Escaping       |
| victory     | [MV.Motion](MV.Motion.md) | Victory        |
| dying      | [MV.Motion](MV.Motion.md) | Dying          |
| abnormal   | [MV.Motion](MV.Motion.md) | Abnormal state |
| sleep      | [MV.Motion](MV.Motion.md) | Sleeping       |
| dead       | [MV.Motion](MV.Motion.md) | Dead           |

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

####  [Sprite_Battler](Sprite_Battler.md)

* [checkBattler (battler)](Sprite_Battler.md#checkbattler-battler--boolean)
* [createDamageSprite ()](Sprite_Battler.md#createdamagesprite-)
* [destroyDamageSprite ()](Sprite_Battler.md#destroydamagesprite-)
* [inHomePosition ()](Sprite_Battler.md#inhomeposition---boolean)
* [isEffecting ()](Sprite_Battler.md#iseffecting---boolean)
* [isMoving ()](Sprite_Battler.md#ismoving---boolean)
* [onClick ()](Sprite_Battler.md#onclick-)
* [onMouseEnter ()](Sprite_Battler.md#onmouseenter-)
* [onPress ()](Sprite_Battler.md#onpress-)
* [setHome (x, y)](Sprite_Battler.md#sethome-x-y)
* [setupDamagePopup ()](Sprite_Battler.md#setupdamagepopup-)
* [startMove (x, y, duration)](Sprite_Battler.md#startmove-x-y-duration)
* [updateDamagePopup ()](Sprite_Battler.md#updatedamagepopup-)
* [updatePosition ()](Sprite_Battler.md#updateposition-)
* [updateSelectionEffect ()](Sprite_Battler.md#updateselectioneffect-)
* [updateVisibility ()](Sprite_Battler.md#updatevisibility-)

### Methods

#### createMainSprite ()
Generates the main sprite.

#### createShadowSprite ()
Generates the shadow sprite.

#### createStateSprite ()
Generates the state sprite.

#### createWeaponSprite ()
Generates the weapon sprite.

#### damageOffsetX () → {[Number](Number.md)}
Override: [Sprite_Battler](Sprite_Battler.md#damageoffsetx)

#### damageOffsetY () → {[Number](Number.md)}
Override: [Sprite_Battler](Sprite_Battler.md#damageoffsety)

#### initialize (battler opt)
Override: [Sprite_Battler](Sprite_Battler.md#initialize-)

##### Arguments

| Name     | Type                          | Trait      | Description      |
|----------|-------------------------------|------------|------------------|
| `battler`| [Game_Actor](Game_Actor.md) | &lt;optional&gt; | Battler         |

#### initMembers ()
Override: [Sprite_Battler](Sprite_Battler.md#initmembers-)

#### mainSprite () → {[Sprite](Sprite.md)}
**@MZ** Override: [Sprite_Battler](Sprite_Battler.md#mainsprite---sprite_battler)

#### motionSpeed () → {[Number](Number.md)}
Returns the speed of the motion.

#### moveToStartPosition ()
Moves to the starting point.

#### onMoveEnd ()
Override: [Sprite_Battler](Sprite_Battler.md#onmoveend-)

#### refreshMotion ()
Resets the motion.

#### retreat ()
Resumes the motion.

#### setActorHome (index)
Sets the base point from the specified formation number.

##### Arguments

| Name   | Type                | Description        |
|--------|---------------------|--------------------|
| `index`| [Number](Number.md) | Formation number    |

#### setBattler (battler)
Override: [Sprite_Battler](Sprite_Battler.md#setbattler-battler)

#### setupMotion ()
Prepares the motion.

#### setupWeaponAnimation ()
Prepares the weapon animation.

#### shouldStepForward () → {Boolean}
**@MZ** Determines if it is necessary to move forward.

#### startEntryMotion ()
Prepares the entry motion.

#### startMotion (motionType)
Starts the specified motion.

##### Arguments

| Name        | Type                | Description                                         |
|-------------|---------------------|-----------------------------------------------------|
| `motionType`| [String](String.md) | Motion type (specified as a string of the Name from [MOTIONS](Sprite_Actor.md#motions)) |

#### stepBack ()
Checks if it is retreating.

#### stepForward ()
Checks if it is advancing.

#### update ()
Override: [Sprite_Battler](Sprite_Battler.md#update-)

#### updateBitmap ()
Override: [Sprite_Battler](Sprite_Battler.md#updateBitmap-)

#### updateFrame ()
Override: [Sprite_Battler](Sprite_Battler.md#updateFrame-)

#### updateMain ()
Override: [Sprite_Battler](Sprite_Battler.md#updateMain-)

#### updateMotion ()
Updates the motion.

#### updateMotionCount ()
Updates the motion count.

#### updateMove ()
Override: [Sprite_Battler](Sprite_Battler.md#updateMove-)

#### updateShadow ()
Updates the shadow.

#### updateTargetPosition ()
Updates the target position.
