[Class Tree](index.md)

# Class: Scene_Base

## Superclass: [Stage](Stage.md)

The base object for scenes.

In MZ, features related to button operations for tap input have been enhanced. <br />
The subclasses that were in MV, [Scene_Battle](Scene_Battle.md) and [Scene_Map](Scene_Map.md), are now subclasses of [Scene_Message](Scene_Message.md).

Related Classes: [SceneManager](SceneManager.md)

### new Scene_Base ()

### Subclasses

* [Scene_Boot](Scene_Boot.md)
* [Scene_Gameover](Scene_Gameover.md)
* [Scene_Title](Scene_Title.md)
* [Scene_Message](Scene_Message.md) **@MZ**
* [Scene_MenuBase](Scene_MenuBase.md)
* [Scene_Message](Scene_Message.md) **@MZ**

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_started` | Boolean | **@MZ** Indicates if it has started |
| `_active` | Boolean | Is it active? |
| `_fadeSign` | [Number](Number.md) | [Fade state](#fade-state) |
| `_fadeDuration` | [Number](Number.md) | Time taken for the fade |
| `_windowLayer` | [WindowLayer](WindowLayer.md) | Window layer |
| `_fadeWhite` | [Number](Number.md) | **@MZ** Time taken for the fade |
| `_fadeOpacity` | [Number](Number.md) | **@MZ** Time taken for the fade |

#### Fade State

| Number | Description |
| --- | --- |
| -1 | Fade out |
| 0 | None |
| 1 | Fade in |

### Deprecated MV Properties
`_fadeSprite`, `_imageReservationId`

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
* [destroy ()](PIXI.Container.md#destroy-)
* [getChildAt (index)](PIXI.Container.md#getchildat-index--pixidisplayobject)
* [getChildByName (name)](PIXI.Container.md#getchildbyname-name--pixidisplayobject)
* [getChildIndex (child)](PIXI.Container.md#getchildindex-child--pixidisplayobject)
* [onChildrenChange ()](PIXI.Container.md#onchildrenchange-)
* [removeChild (child)](PIXI.Container.md#removechild-child--pixidisplayobject)
* [removeChildAt (index)](PIXI.Container.md#removechildat-index--pixidisplayobject)
* [removeChildren (beginIndex, endIndex)](PIXI.Container.md#removechildren-beginindex-endindex--arraypixidisplayobject)
* [render (renderer)](PIXI.Container.md#render-renderer)
* [renderAdvanced (renderer)](PIXI.Container.md#renderadvanced-renderer)
* [renderCanvas (renderer)](PIXI.Container.md#rendercanvas-renderer)
* [setChildIndex (child, index)](PIXI.Container.md#setchildindex-child-index)
* [sortChildren ()](PIXI.Container.md#sortchildren-)
* [swapChildren (child, child2)](PIXI.Container.md#swapchildren-child-child2)
* [updateTransform ()](PIXI.Container.md#updatetransform-)

#### [Stage](Stage.md)

* [destroy ()](Stage.md#destroy-)

### Methods

#### addWindow (Window)
Adds a window to the window layer.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `Window` | [Window_Base](Window_Base.md) | The window to add |

#### attachReservation ()
Adds a reservation to the queue.

#### buttonAreaBottom () → {[Number](Number.md)}
**@MZ** Returns the bottom position of the button area (default: 52).

#### buttonAreaHeight () → {[Number](Number.md)}
**@MZ** Returns the height of the button area (default: 52).

#### buttonAreaTop () → {[Number](Number.md)}
**@MZ** Returns the top position of the button area (default: 0).

#### buttonY () → {[Number](Number.md)}
**@MZ** Returns the y position of the button (default: 2).

#### calcWindowHeight (numLines, selectable) → {[Number](Number.md)}
**@MZ** Returns the height of the window calculated based on the specified number of lines and type.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `numLines` | [Number](Number.md) | Number of lines |
| `selectable` | Boolean | Is it selectable? |

#### centerSprite (sprite)
**@MZ** Positions the sprite at the center of the screen.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sprite` | [Sprite](Sprite.md) | The target sprite |

#### checkGameover ()
Checks if the game is in a game over state.

#### create ()
Creates the scene.

#### createColorFilter ()
**@MZ** Generates a color filter.

#### createWindowLayer ()
Creates the window layer [WindowLayer](WindowLayer.md).

#### detachReservation ()
Removes a reservation from the queue.

#### executeAutosave ()
**@MZ** Executes the autosave.

#### fadeOutAll ()
Fades out all visuals and sounds at a slow speed.

#### fadeSpeed () → {[Number](Number.md)}
Returns the fade speed.

#### initialize ()
Override: [Stage](Stage.md#initialize-)

#### isActive () → {Boolean}
Is the scene active?

#### isAutosaveEnabled () → {Boolean}
**@MZ** Is the state autosave enabled?

#### isBottomButtonMode () → {Boolean}
**@MZ** Is the button position at the bottom? (default: false).

#### isBottomHelpMode () → {Boolean}
**@MZ** Is the help position at the bottom? (default: true).

#### isBusy () → {Boolean}
Is the fade operation ongoing?

#### isReady () → {Boolean}
Is the scene ready?

#### isRightInputMode () → {Boolean}
**@MZ** Is it in right-hand input mode? (default: true).

#### mainCommandWidth () → {[Number](Number.md)}
**@MZ** Returns the width of the main command (default: 240).

#### onAutosaveFailure ()
**@MZ** Handler for when the autosave fails. <br />
The core script is empty and reserved for plugins.

#### onAutosaveSuccess ()
**@MZ** Handler for when the autosave succeeds. <br />
The core script is empty and reserved for plugins.

#### popScene ()
Pulls the scene (pop).

#### requestAutosave ()
**@MZ** Requests an autosave.

#### scaleSprite (sprite)
**@MZ** Scales the sprite to screen size.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sprite` | [Sprite](Sprite.md) | The target sprite |

#### slowFadeSpeed () → {[Number](Number.md)}
Returns the slow fade speed.

#### start ()
Starts the scene.

#### startFadeIn (duration optional, white optional)
Requests a fade-in.

##### Arguments

| Name | Type | Optional | Default | Description |
| --- | --- | --- | --- | --- |
| `duration` | [Number](Number.md) | &lt;optional&gt; | 30 | Time taken for the fade-in |
| `white` | Boolean | &lt;optional&gt; | false | Fade to white (false means fade to black) |

#### startFadeOut (duration optional, white optional)
Requests a fade-out.

##### Arguments

| Name | Type | Optional | Default | Description |
| --- | --- | --- | --- | --- |
| `duration` | [Number](Number.md) | &lt;optional&gt; | 30 | Time taken for the fade-out |
| `white` | Boolean | &lt;optional&gt; | false | Fade to white (false means fade to black) |

#### stop ()
Stops the scene.

#### terminate ()
Aborts the current scene before the transition.

#### update ()
Updates every frame.

#### updateChildren ()
Updates child objects.

#### updateColorFilter ()
**@MZ** Updates the color filter.

#### updateFade ()
Updates the fade.

### Deprecated MV Methods
createFadeSprite ()
