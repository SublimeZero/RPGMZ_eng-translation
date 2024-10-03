[Class Tree](index.md)

# Class: Scene_MenuBase

## Superclass: [Scene_Base](Scene_Base.md)

Base class for menu-type scenes.

### new Scene_MenuBase ()

### Subclasses

* [Scene_Debug](Scene_Debug.md)
* [Scene_Equip](Scene_Equip.md)
* [Scene_GameEnd](Scene_GameEnd.md)
* [Scene_Menu](Scene_Menu.md)
* [Scene_Name](Scene_Name.md)
* [Scene_Options](Scene_Options.md)
* [Scene_Shop](Scene_Shop.md)
* [Scene_Status](Scene_Status.md)
* [Scene_File](Scene_File.md)
* [Scene_ItemBase](Scene_ItemBase.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_actor` | [Game_Actor](Game_Actor.md) | Selected actor |
| `_backgroundSprite` | [Sprite](Sprite.md) | Sprite for the scene's background |
| `_helpWindow` | [Window_Help](Window_Help.md) | Help window associated with the scene |
| `_backgroundFilter` | PIXI.filters.BlurFilter | **@MZ** Filter for the scene's background |
| `_cancelButton` | [Sprite_Button](Sprite_Button.md) | **@MZ** Cancel button |
| `_pageupButton` | [Sprite_Button](Sprite_Button.md) | **@MZ** Page up button |
| `_pagedownButton` | [Sprite_Button](Sprite_Button.md) | **@MZ** Page down button |

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
* [renderCanvas (renderer)](PIXI.Container.md#rendercanvas-renderer)
* [setChildIndex (child, index)](PIXI.Container.md#setchildindex-child-index)
* [sortChildren ()](PIXI.Container.md#sortchildren-)
* [swapChildren (child, child2)](PIXI.Container.md#swapchildren-child-child2)
* [updateTransform ()](PIXI.Container.md#updatetransform-)

#### [Stage](Stage.md)

* [destroy ()](Stage.md#destroy-)

#### [Scene_Base](Scene_Base.md)

* [addWindow (Window)](Scene_Base.md#addwindow-window)
* [attachReservation ()](Scene_Base.md#attachreservation-)
* [buttonAreaBottom ()](Scene_Base.md#buttonareabottom---number)
* [buttonAreaHeight ()](Scene_Base.md#buttonareaheight---number)
* [buttonAreaTop ()](Scene_Base.md#buttonareatop---number)
* [buttonY ()](Scene_Base.md#buttony---number)
* [calcWindowHeight (numLines, selectable)](Scene_Base.md#calcwindowheight-numlines-selectable--number)
* [centerSprite (sprite)](Scene_Base.md#centersprite-sprite)
* [checkGameover ()](Scene_Base.md#checkgameover-)
* [createColorFilter ()](Scene_Base.md#createcolorfilter-)
* [createWindowLayer ()](Scene_Base.md#createwindowlayer-)
* [detachReservation ()](Scene_Base.md#detachreservation-)
* [executeAutosave ()](Scene_Base.md#executeautosave-)
* [fadeOutAll ()](Scene_Base.md#fadeoutall-)
* [fadeSpeed ()](Scene_Base.md#fadespeed---number)
* [isActive ()](Scene_Base.md#isactive---boolean)
* [isAutosaveEnabled ()](Scene_Base.md#isautosaveenabled---boolean)
* [isBottomButtonMode ()](Scene_Base.md#isbottombuttonmode---boolean)
* [isBottomHelpMode ()](Scene_Base.md#isbottomhelpmode---boolean)
* [isBusy ()](Scene_Base.md#isbusy---boolean)
* [isReady ()](Scene_Base.md#isready---boolean)
* [isRightInputMode ()](Scene_Base.md#isrightinputmode---boolean)
* [mainCommandWidth ()](Scene_Base.md#maincommandwidth---number)
* [onAutosaveFailure ()](Scene_Base.md#onautosavefailure-)
* [onAutosaveSuccess ()](Scene_Base.md#onautosavesuccess-)
* [popScene ()](Scene_Base.md#popscene-)
* [requestAutosave ()](Scene_Base.md#requestautosave-)
* [scaleSprite (sprite)](Scene_Base.md#scalesprite-sprite)
* [slowFadeSpeed ()](Scene_Base.md#slowfadespeed---number)
* [start ()](Scene_Base.md#start-)
* [startFadeIn (duration opt, white opt)](Scene_Base.md#startfadein-duration-opt-white-opt)
* [startFadeOut (duration opt, white opt)](Scene_Base.md#startfadeout-duration-opt-white-opt)
* [stop ()](Scene_Base.md#stop-)
* [terminate ()](Scene_Base.md#terminate-)
* [updateChildren ()](Scene_Base.md#updatechildren-)
* [updateColorFilter ()](Scene_Base.md#updatecolorfilter-)
* [updateFade ()](Scene_Base.md#updatefade-)

### Methods

#### actor () → {[Game_Actor](Game_Actor.md)}
Returns the current actor.

#### arePageButtonsEnabled () → {Boolean}
**@MZ** Checks if the page buttons are available.

#### create ()
Override: [Scene_Base](Scene_Base.md#create-)

#### createButtons ()
**@MZ** Generates buttons.

#### createCancelButton ()
**@MZ** Generates a cancel button.

#### createHelpWindow ()
Generates a help window.

#### createPageButtons ()
**@MZ** Generates page buttons.

#### helpAreaBottom() → {[Number](Number.md)}
**@MZ** Returns the bottom coordinate of the [Help] area.

#### helpAreaHeight() → {[Number](Number.md)}
**@MZ** Returns the height of the [Help] area.

#### helpAreaTop() → {[Number](Number.md)}
**@MZ** Returns the top coordinate of the [Help] area.

#### helpWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular range of the [Help] area.

#### mainAreaBottom() → {[Number](Number.md)}
**@MZ** Returns the bottom coordinate of the main area.

#### mainAreaHeight() → {[Number](Number.md)}
**@MZ** Returns the height of the main area.

#### mainAreaTop() → {[Number](Number.md)}
**@MZ** Returns the top coordinate of the main area.

#### initialize ()
Override: [Scene_Base](Scene_Base.md#initialize-)

#### nextActor ()
Switches to the next actor in the party.

#### needsCancelButton () → {Boolean}
**@MZ** Checks if a cancel button is needed.

#### needsPageButtons () → {Boolean}
**@MZ** Checks if page buttons are needed.

#### onActorChange ()
Handler called when the actor changes.

#### previousActor ()
Switches to the previous actor in the party.

#### update ()
**@MZ** Override: [Scene_Base](Scene_Base.md#update-)

#### updatePageButtons ()
**@MZ** Updates the page buttons.

#### setBackgroundOpacity (opacity)
Sets the background opacity.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `opacity` | [Number](Number.md) | Opacity (0 to 255) |

#### updateActor ()
Updates the current actor.
