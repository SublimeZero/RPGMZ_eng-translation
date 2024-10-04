# Class: Spriteset_Battle

## Superclass: [Spriteset_Base](Spriteset_Base.md)

A sprite set for the battle scene, including [actors] and [enemies].

In MZ, functionality related to the [background] has been separated into [Sprite_Battleback](Sprite_Battleback.md).

Related class: [Scene_Battle](Scene_Battle.md)

### new Spriteset_Battle ()

### Properties

| Identifier           | Type                                                | Description                      |
| -------------------- | --------------------------------------------------- | -------------------------------- |
| `_battlebackLocated` | Boolean                                             | Whether the background image is displayed |
| `_backgroundSprite`  | [Sprite](Sprite.md)                                | The [background] sprite          |
| `_battleField`      | [Sprite](Sprite.md)                                | The battle field                 |
| `_back1Sprite`      | [Sprite_Battleback](Sprite_Battleback.md)        | Background 1 sprite              |
| `_back2Sprite`      | [Sprite_Battleback](Sprite_Battleback.md)        | Background 2 sprite              |
| `_enemySprites`     | [Array](Array.md).&lt;[Sprite_Enemy](Sprite_Enemy.md)&gt; | Array of [enemy] sprites         |
| `_actorSprites`     | [Array](Array.md).&lt;[Sprite_Actor](Sprite_Actor.md)&gt; | Array of [actor] sprites         |

The types of `_back1Sprite` and `_back2Sprite` were [TilingSprite](TilingSprite.md) in MV, but have been changed to [Sprite_Battleback](Sprite_Battleback.md) in MZ.

### Methods Inherited from the Superclass

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

#### [Spriteset_Base](Spriteset_Base.md)

* [animationBaseDelay ()](Spriteset_Base.md#animationbasedelay---number)
* [animationNextDelay ()](Spriteset_Base.md#animationnextdelay---number)
* [animationShouldMirror (target)](Spriteset_Base.md#animationshouldmirror-target--boolean)
* [createAnimation (request)](Spriteset_Base.md#createanimation-request)
* [createAnimationSprite (targets, animation, mirror, delay)](Spriteset_Base.md#createanimationsprite-targets-animation-mirror-delay)
* [createBaseFilters ()](Spriteset_Base.md#createbasefilters-)
* [createBaseSprite ()](Spriteset_Base.md#createbasesprite-)
* [createCanvasToneChanger ()](Spriteset_Base.md#createcanvastonechanger-)
* [createLowerLayer ()](Spriteset_Base.md#createlowerlayer-)
* [createOverallFilters ()](Spriteset_Base.md#createoverallfilters-)
* [createPictures ()](Spriteset_Base.md#createpictures-)
* [createTimer ()](Spriteset_Base.md#createtimer-)
* [createUpperLayer ()](Spriteset_Base.md#createupperlayer-)
* [destroy ()](Spriteset_Base.md#destroy-)
* [isAnimationForEach (animation)](Spriteset_Base.md#isanimationforeach-animation--boolean)
* [isAnimationPlaying ()](Spriteset_Base.md#isanimationplaying-)
* [isMVAnimation (animation)](Spriteset_Base.md#ismvanimation-animation--boolean)
* [lastAnimationSprite ()](Spriteset_Base.md#lastanimationsprite---sprite)
* [makeTargetSprites (targets)](Spriteset_Base.md#maketargetsprites-targets--arraysprite)
* [pictureContainerRect ()](Spriteset_Base.md#picturecontainerrect---rectangle)
* [processAnimationRequests ()](Spriteset_Base.md#processanimationrequests-)
* [removeAllAnimations ()](Spriteset_Base.md#removeallanimations-)
* [removeAnimation (sprite)](Spriteset_Base.md#removeanimation-sprite)
* [update ()](Spriteset_Base.md#update-)
* [updateAnimations ()](Spriteset_Base.md#updateanimations-)
* [updateBaseFilters ()](Spriteset_Base.md#updatebasefilters-)
* [updateOverallFilters ()](Spriteset_Base.md#updateoverallfilters-)
* [updatePosition ()](Spriteset_Base.md#updateposition-)

---

### Methods

#### autotileType (z) → {[Number](Number.md)}
Returns the autotile type (terrain type) of the specified layer at the battle start location.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `z` | [Number](Number.md) | Layer |

---

#### battleFieldOffsetY () → {[Number](Number.md)}
**@MZ** Returns the y-axis offset (default: 24 pixels).

---

#### battlerSprites () → {[Array](Array.md).&lt;[Sprite_Battler](Sprite_Battler.md)&gt;}
Returns an array of battlers (including [actors] + [enemies]).

---

#### compareEnemySprite (a, b) → {[Number](Number.md)}
Compares [enemy] sprites and returns the difference.
This is used as a callback function for overlap sorting.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `a` | [Sprite_Enemy](Sprite_Enemy.md) | [Enemy] Sprite A |
| `b` | [Sprite_Enemy](Sprite_Enemy.md) | [Enemy] Sprite B |

---

#### createActors ()
Generates [actor] sprites.

---

#### createBackground ()
Generates the [background].

---

#### createBattleback ()
Generates the background (far).

---

#### createBattleField ()
Generates the background (ground).

---

#### createEnemies ()
Generates [enemy] sprites.

---

#### createLowerLayer ()
Overrides: [Spriteset_Base](Spriteset_Base.md#createLowerLayer-).

---

#### findTargetSprite (target)
Overrides: [Spriteset_Base](Spriteset_Base.md#findtargetsprite-target--sprite).

---

#### initialize ()
Overrides: [Spriteset_Base](Spriteset_Base.md#initialize-).

---

#### isAnyoneMoving () → {Boolean}
Checks if any [actors] or [enemies] are currently moving.

---

#### isBusy () → {Boolean}
Checks if the system is busy.

---

#### isEffecting () → {Boolean}
Checks if an effect is currently in progress.

---

#### loadSystemImages ()
Overrides: [Spriteset_Base](Spriteset_Base.md#loadsystemimages-).

---

#### updateActors ()
Updates the [actors].

---

#### updateBattleback ()
Updates the [background].

---

### Deprecated MV Methods
battleback1Bitmap(), battleback1Name(), battleback2Bitmap(), battleback2Name(), defaultBattleback1Name(), defaultBattleback2Name(), isAnimationPlaying(), locateBattleback(), normalBattleback1Name(), normalBattleback2Name(), overworldBattleback1Name(), overworldBattleback2Name(), shipBattleback1Name(), shipBattleback2Name(), terrainBattleback1Name(type), terrainBattleback2Name(type).
