# Class: Spriteset_Map

## Superclass: [Spriteset_Base](Spriteset_Base.md)

| Database | JSON Data | Object |
| --- | --- | --- |
| Map | [RPG.Map](RPG.Map.md) | [Game_Map](Game_Map.md) |

A sprite set for displaying maps.

Changes were made in versions 1.1.1, 1.2.0, 1.4.3, and 1.4.4.

Main paths
```js
SceneManager._scene._spriteset
```

Related classes: [Scene_Map](Scene_Map.md)

### new Spriteset_Map ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_balloonSprites` | [Array](Array.md).&lt;[Sprite_Balloon](Sprite_Balloon.md)&gt; | **@MZ** Sprites for [balloons] |
| `_characterSprites` | [Array](Array.md).&lt;[Sprite_Character](Sprite_Character.md)&gt; | Sprites for [actors] and [events] |
| `_destinationSprite` | [Sprite_Destination](Sprite_Destination.md) | Touch position sprite |
| `_effectsContainer` | [Tilemap](Tilemap.md) | **@MZ** Container for displaying balloon effects |
| `_parallax` | [TilingSprite](TilingSprite.md) | [Parallax] sprite |
| `_parallaxName` | [String](String.md) | [Parallax] image file name |
| `_tilemap` | [Tilemap](Tilemap.md) | The main map image |
| `_tileset` | [RPG.Tileset](RPG.Tileset.md) | [Tileset] |
| `_shadowSprite` | [Sprite](Sprite.md) | Shadow sprite |
| `_weather` | [Weather](Weather.md) | Weather |

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

#### animationBaseDelay ()
**@MZ** Returns the base delay time for animations (default: 0).

---

#### createBalloon (request)
**@MZ** Requests the creation of a [balloon] sprite.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `request` | [BalloonRequest](MV.BalloonRequest.md) | [Balloon] parameters |

---

#### createCharacters ()
Generates character sprites ([Sprite_Character](Sprite_Character.md)).

---

#### createDestination ()
Generates a touch position display sprite ([Sprite_Destination](Sprite_Destination.md)).

---

#### createLowerLayer ()
Overrides: [Spriteset_Base](Spriteset_Base.md#createLowerLayer-)

Generates the lower layer including the basic sprite, [parallax], [tilemap], characters, shadows, touch position display, and weather.

---

#### createParallax ()
Generates a [parallax] sprite.

---

#### createShadow ()
Generates a shadow sprite.

---

#### createTilemap ()
Generates a tilemap ([Tilemap](Tilemap.md)).

---

#### createWeather ()
Generates a weather sprite ([Weather](Weather.md)).

---

#### destroy ()
**@MZ** [Spriteset_Base](Spriteset_Base.md#destroy-)

---

#### hideCharacters ()
Hides character sprites.

---

#### findTargetSprite (target)
Overrides: [Spriteset_Base](Spriteset_Base.md#findtargetsprite-target--sprite)

---

#### initialize ()
Overrides: [Spriteset_Base](Spriteset_Base.md#initialize-)

---

#### loadSystemImages ()
**@MZ** Overrides: [Spriteset_Base](Spriteset_Base.md#loadsystemimages-)

---

#### loadTileset ()
Loads the tileset ([RPG.Tileset](RPG.Tileset.md)).

---

#### processBalloonRequests ()
**@MZ** Executes the drawing of requested [balloons].

---

#### removeAllBalloons ()
**@MZ** Removes all [balloons].

---

#### removeBalloon (sprite)
**@MZ** Removes a [balloon].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sprite` | [Sprite_Balloon](Sprite_Balloon.md) | [Balloon] sprite |

---

#### update ()
Overrides: [Spriteset_Base](Spriteset_Base.md#update-)

---

#### updateBalloons ()
**@MZ** Updates [balloons].

---

#### updateParallax ()
Updates the [parallax].

---

#### updateShadow ()
Updates the shadow.

---

#### updateTilemap ()
Updates the tilemap.

---

#### updateTileset ()
Updates the tileset.

---

#### updateWeather ()
Updates the weather.

---

### Deprecated MV Methods
_canvasReAddParallax ()
