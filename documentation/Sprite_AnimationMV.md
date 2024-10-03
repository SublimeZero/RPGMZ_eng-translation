[Class Tree](index.md)

# Class: Sprite_AnimationMV

## Superclass: [Sprite](Sprite.md)

| Database     | JSON Data                        | Global Variables                                        |
|--------------|----------------------------------|--------------------------------------------------------|
| [Animation]  | [RPG.Animation](RPG.Animation.md), [RPG.Animation.Timing](RPG.Animation.Timing.md) | [$dataAnimations](global.md#dataanimations-arrayrpganimation) (array) |

A sprite that displays [animations]. Primarily used in battle scenes.  
It can also be executed from the [Display Animation] script command.

This class was newly added in MZ, but in reality, it is a revised version of MV's Sprite_Animation.  
The [Sprite_Animation](Sprite_Animation.md) in MZ is effectively a newly added class.  
Thus, this section describes the changes made to MV's Sprite_Animation.  
It exists to maintain compatibility with MV animations; conversely, if you don't plan to port and use MV animations, this class is unnecessary.

Related classes: [Sprite_Base](Sprite_Base.md), [Sprite_Damage](Sprite_Damage.md), [RPG.UsableItem](RPG.UsableItem.md), [RPG.Weapon](RPG.Weapon.md), [Game_Interpreter](Game_Interpreter.md)

### new Sprite_AnimationMV ()

### Properties

| Identifier  | Type                                             | Description     |
|-------------|--------------------------------------------------|------------------|
| `_checker1` | Object                                           | [static] Object to check if already generated {key: [RPG.Animation](RPG.Animation.md)} |
| `_checker2` | Object                                           | [static] Object to check if already generated {key: [RPG.Animation](RPG.Animation.md)} |
| `_targets`  | [Array](Array.md).&lt;[Sprite_Base](Sprite_Base.md)&gt; | **@MZ** Targets  |
| `_animation`| [RPG.Animation](RPG.Animation.md)                | Animation data   |
| `_mirror`   | Boolean                                         | Whether to mirror horizontally |
| `_delay`    | [Number](Number.md)                             | Display time     |
| `_rate`     | [Number](Number.md)                             | Display rate (default: 4 frames) |
| `_duration` | [Number](Number.md)                             | Duration         |
| `_flashColor` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of flash colors [Red, Green, Blue, Intensity] |
| `_flashDuration` | [Number](Number.md)                         | Flash [time] (in units of 1/15 seconds) |
| `_screenFlashDuration` | [Number](Number.md)                    | Duration of the [screen] flash |
| `_hidingDuration` | [Number](Number.md)                        | Duration of [target deletion] |
| `_bitmap1`  | [Bitmap](Bitmap.md)                            | [Image] 1       |
| `_bitmap2`  | [Bitmap](Bitmap.md)                            | [Image] 2       |
| `_cellSprites` | [Array](Array.md).&lt;[Sprite](Sprite.md)&gt; | Array of sprites for the animation |
| `_screenFlashSprite` | [ScreenSprite](ScreenSprite.md)         | Sprite for the screen flash |
| `_duplicated` | Boolean                                      | Whether duplicated |
| `_reduceArtifacts` | Boolean                                   | Whether to reduce artifacts |

### Deprecated MV Property
`_target`

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
* [updateVisibility ()](Sprite.md#updatevisibility-)

### Methods

#### absoluteX () → {[Number](Number.md)}
Returns the absolute value of the x-coordinate.

#### absoluteY () → {[Number](Number.md)}
Returns the absolute value of the y-coordinate.

#### createCellSprites ()
Generates sprites for cells.

#### createScreenFlashSprite ()
Generates a sprite for flashing on the screen.

#### currentFrameIndex () → {[Number](Number.md)}
Returns the current frame number.

#### initialize ()
Overrides: [Sprite](Sprite.md#initialize-)

#### initMembers ()
Initializes member variables.

#### isPlaying () → {Boolean}
Checks if the animation is currently playing.

#### isReady () → {Boolean}
Checks if the animation is ready.

#### loadBitmaps ()
Loads images for the animation.

#### onEnd ()
**@MZ** Handler for when the animation ends.

#### processTimingData (timing)
Executes the [SE and Flash Timing] data.

##### Arguments

| Name    | Type                                             | Description                      |
|---------|--------------------------------------------------|----------------------------------|
| `timing`| [RPG.Animation.Timing](RPG.Animation.Timing.md) | [SE and Flash Timing]            |

#### setup (targets, animation, mirror, delay)
Prepares the animation.  
In MV, there was a single target, but now there are multiple.

##### Arguments

| Name       | Type                                             | Description                      |
|------------|--------------------------------------------------|----------------------------------|
| `targets`  | [Array](Array.md).&lt;[Sprite_Base](Sprite_Base.md)&gt; | **@MZ** Targets                  |
| `animation`| [RPG.Animation](RPG.Animation.md)                | Animation data                   |
| `mirror`   | Boolean                                         | Whether to mirror horizontally    |
| `delay`    | [Number](Number.md)                             | Display time                     |

#### setupDuration ()
Sets the duration.

#### setupRate ()
Sets the display rate (frames) (default: 4).

#### startFlash (color, duration)
Starts the flash.

##### Arguments

| Name       | Type                                             | Description                      |
|------------|--------------------------------------------------|----------------------------------|
| `color`    | [Array](Array.md).&lt;[Number](Number.md)&gt;  | Array of colors [Red, Green, Blue, Intensity] |
| `duration` | [Number](Number.md)                             | Duration                         |

#### startHiding (duration)
Hides the target.

##### Arguments

| Name       | Type                                             | Description                      |
|------------|--------------------------------------------------|----------------------------------|
| `duration` | [Number](Number.md)                             | Duration                         |

#### startScreenFlash (color, duration)
Starts the screen flash.

##### Arguments

| Name       | Type                                             | Description                      |
|------------|--------------------------------------------------|----------------------------------|
| `color`    | [Array](Array.md).&lt;[Number](Number.md)&gt;  | Array of colors [Red, Green, Blue, Intensity] |
| `duration` | [Number](Number.md)                             | Duration                         |

#### update ()
Overrides: [Sprite](Sprite.md#update-)

#### updateAllCellSprites (frame)
Updates all cell sprites.

##### Arguments

| Name    | Type                                             | Description                      |
|---------|--------------------------------------------------|----------------------------------|
| `frame` | [Array](Array.md).&lt;[Array](Array.md).&lt;[Number](Number.md)&gt;&gt; | Cell numbers from [frame information](RPG.Animation.md#フレーム情報) |

#### updateCellSprite (sprite, cell)

##### Arguments

| Name    | Type                                             | Description                      |
|---------|--------------------------------------------------|----------------------------------|
| `sprite`| [Sprite](Sprite.md)                             |                                  |
| `cell`  | [Array](Array.md).&lt;[Number](Number.md)&gt;  |                                  |

#### updateFlash ()
Updates the flash.

#### updateFrame ()
Updates the frame.

#### updateHiding ()
Updates the target deletion.

#### updateMain ()
Main update.

#### updatePosition ()
Updates the position.

#### updateScreenFlash ()
Updates the screen flash.

### Deprecated MV Methods
`createSprites ()`, `remove ()`
