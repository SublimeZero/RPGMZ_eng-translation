[Class Tree](index.md)

# Class: Sprite_Animation

## Superclass: [Sprite](Sprite.md)

| Database | JSON Data | Global Variable |
|----------|-----------|-----------------|
| [Animation] | [RPG.Animation](RPG.Animation.md), [RPG.Animation.Timing](RPG.Animation.Timing.md) | [$dataAnimations](global.md#dataanimations-arrayrpganimation) (Array) |

A sprite that displays [animations]. Mainly used in battle scenes.  
It can also be executed from the [Display Animation] script command.

The priority for overlap has a `z` property value of 8.

Although the name is the same, this class is newly created for [Effekseer](https://effekseer.github.io/jp/), and the class used in MV has been renamed to [Sprite_AnimationMV](Sprite_AnimationMV.md).  
Therefore, the properties and methods will not have the **@MZ** notation and will be documented as a new class.  
Please do not trust the contents as they are written based on guesswork. I wrote this without fully understanding, especially here (laughs).

Changes were made in v1.1.0, v1.2.0, v1.3.3, and v1.4.0.

Related classes: [EffectManager](EffectManager.md), [Spriteset_Base](Spriteset_Base.md), [Sprite_Damage](Sprite_Damage.md), [RPG.UsableItem](RPG.UsableItem.md), [RPG.Weapon](RPG.Weapon.md), [Game_Interpreter](Game_Interpreter.md)

### new Sprite_Animation ()

### Properties

| Identifier         | Type                                     | Description                                                   |
|--------------------|------------------------------------------|---------------------------------------------------------------|
| `_targets`         | [Array](Array.md).&lt;[Sprite](Sprite.md)&gt; | Targets                                                      |
| `_animation`       | [RPG.Animation](RPG.Animation.md)       | Animation data                                               |
| `_mirror`          | Boolean                                  | Whether to mirror horizontally                               |
| `_delay`           | [Number](Number.md)                     | Display time                                                 |
| `_previous`        | [Sprite_Animation](Sprite_Animation.md) | Previous animation class                                     |
| `_effect`          | EffekseerEffect                          | Effekseer effect                                            |
| `_handle`          | EffekseerHandle                          | Effekseer handle (a class holding position, rotation, scale, and speed data) |
| `_playing`         | Boolean                                  | Whether the animation is playing (including preparation)     |
| `_started`         | Boolean                                  | Whether the animation has started                            |
| `_frameIndex`      | [Number](Number.md)                     | Frame number                                                |
| `_maxTimingFrames` | [Number](Number.md)                     | Maximum frames                                              |
| `_flashColor`      | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of flash colors [Red, Green, Blue, Strength]          |
| `_flashDuration`   | [Number](Number.md)                     | Flash duration [time] (in 1/60 second units)               |
| `_viewportSize`    | [Number](Number.md)                     | Viewport size (default value: 4096)                         |
| `_originalViewport` | [Array](Array.md).&lt;[Number](Number.md)&gt; | **@MZ 1.3.3** Deprecated. Viewport [x, y, width, height]   |

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

#### _render (renderer) 
Executes rendering.

##### Arguments

| Name      | Type                       | Description   |
|-----------|----------------------------|---------------|
| `renderer`| [PIXI.Renderer](PIXI.Renderer.md) | The renderer |

#### canStart () → {Boolean}
Whether it can start.

#### checkEnd ()
Sets to the end state if the animation has finished.

#### destroy ()
Override: [Sprite](Sprite.md#destroy-)

#### initialize ()
Override: [Sprite](Sprite.md#initialize-)

#### initMembers ()
Initializes member variables.

#### isPlaying () → {Boolean}
Whether the animation is currently playing.

#### onAfterRender (renderer)
Handler after rendering.

##### Arguments

| Name      | Type                       | Description   |
|-----------|----------------------------|---------------|
| `renderer`| [PIXI.Renderer](PIXI.Renderer.md) | The renderer |

#### onBeforeRender (renderer)
Handler before rendering starts.

##### Arguments

| Name      | Type                       | Description   |
|-----------|----------------------------|---------------|
| `renderer`| [PIXI.Renderer](PIXI.Renderer.md) | The renderer |

#### processFlashTimings ()
Executes the flash for [SE and Flash Timing] data.

#### processSoundTimings ()
Executes the SE for [SE and Flash Timing] data.

#### resetViewport (renderer)
Reconfigures the viewport.

##### Arguments

| Name      | Type                       | Description   |
|-----------|----------------------------|---------------|
| `renderer`| [PIXI.Renderer](PIXI.Renderer.md) | The renderer |

#### saveViewport (renderer)
**@MZ 1.3.3** Deprecated.  
Saves the viewport to `_originalViewport`.

##### Arguments

| Name      | Type                       | Description   |
|-----------|----------------------------|---------------|
| `renderer`| [PIXI.Renderer](PIXI.Renderer.md) | The renderer |

#### setCameraMatrix (renderer) 
Sets the camera matrix to the renderer.

##### Arguments

| Name      | Type                       | Description   |
|-----------|----------------------------|---------------|
| `renderer`| [PIXI.Renderer](PIXI.Renderer.md) | The renderer (unused) |

#### setProjectionMatrix (renderer) 
Sets the projection matrix to the renderer.

##### Arguments

| Name      | Type                       | Description   |
|-----------|----------------------------|---------------|
| `renderer`| [PIXI.Renderer](PIXI.Renderer.md) | The renderer |

#### setRotation (x, y, z)
Sets the rotation to the handle.

##### Arguments

| Name | Type            | Description |
|------|-----------------|-------------|
| `x`  | [Number](Number.md) | x rotation |
| `y`  | [Number](Number.md) | y rotation |
| `z`  | [Number](Number.md) | z rotation |

#### setViewport (renderer) 
Sets the viewport to the renderer.

##### Arguments

| Name      | Type                       | Description   |
|-----------|----------------------------|---------------|
| `renderer`| [PIXI.Renderer](PIXI.Renderer.md) | The renderer |

#### setup (targets, animation, mirror, delay, previous)
Prepares the animation.

##### Arguments

| Name      | Type                                        | Description   |
|-----------|---------------------------------------------|---------------|
| `targets` | [Array](Array.md).&lt;[Sprite](Sprite.md)&gt; | Targets       |
| `animation` | [RPG.Animation](RPG.Animation.md)          | Animation data |
| `mirror`  | Boolean                                     | Whether to mirror horizontally |
| `delay`   | [Number](Number.md)                        | Display time  |
| `previous`| [Sprite_Animation](Sprite_Animation.md)    | Previous animation class |

#### shouldWaitForPrevious () → {Boolean}
Whether it needs to wait for the previous animation.

#### targetPosition (renderer) → {[Point](Point.md)}
Returns the target position of the renderer.

##### Arguments

| Name      | Type                       | Description   |
|-----------|----------------------------|---------------|
| `renderer`| [PIXI.Renderer](PIXI.Renderer.md) | The renderer |

#### targetSpritePosition (sprite) → {[Point](Point.md)}
Returns the position of the target sprite.

##### Arguments

| Name      | Type                       | Description   |
|-----------|----------------------------|---------------|
| `sprite`  | [Sprite](Sprite.md)       | The target sprite |

#### update ()
Override: [Sprite](Sprite.md#update-)

#### updateEffectGeometry ()
Updates the effect geometry.

#### updateFlash ()
Updates the flash.

#### updateMain ()
Main update.
