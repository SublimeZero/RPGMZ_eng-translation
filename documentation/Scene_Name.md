[Class Tree](index.md)

# Class: Scene_Name

## Superclass: [Scene_MenuBase](Scene_MenuBase.md)

Scene for [name input processing].

Main path
```js
SceneManager._scene
```

Related classes: [SceneManager](SceneManager.md), [Game_Interpreter](Game_Interpreter.md)

### new Scene_Name ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_actorId ` | [Number](Number.md) | Actor ID |
| `_maxLength ` | [Number](Number.md) | Maximum length of characters |
| `_actor` | [Game_Actor](Game_Actor.md) | Selected actor |
| `_inputWindow` | [Window_NameInput](Window_NameInput.md) | Input window |
| `_editWindow` | [Window_NameEdit](Window_NameEdit.md) | Edit window |

### Methods inherited from superclass

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
* [startFadeIn (duration opt, white opt)](Scene_Base.md#startfadein-duration-opt-white-opt)
* [startFadeOut (duration opt, white opt)](Scene_Base.md#startfadeout-duration-opt-white-opt)
* [stop ()](Scene_Base.md#stop-)
* [terminate ()](Scene_Base.md#terminate-)
* [updateChildren ()](Scene_Base.md#updatechildren-)
* [updateColorFilter ()](Scene_Base.md#updatecolorfilter-)
* [updateFade ()](Scene_Base.md#updatefade-)

#### [Scene_MenuBase](Scene_MenuBase.md)

* [actor ()](Scene_MenuBase.md#actor---game_actor)
* [arePageButtonsEnabled ()](Scene_MenuBase.md#arepagebuttonsenabled---boolean)
* [createButtons ()](Scene_MenuBase.md#createbuttons-)
* [createCancelButton ()](Scene_MenuBase.md#createcancelbutton-)
* [createHelpWindow ()](Scene_MenuBase.md#createhelpwindow-)
* [createPageButtons ()](Scene_MenuBase.md#createpagebuttons-)
* [helpAreaBottom()](Scene_MenuBase.md#helpareabottom--number)
* [helpAreaHeight() ](Scene_MenuBase.md#helpareaheight--number)
* [helpAreaTop() ](Scene_MenuBase.md#mainareatop--number)
* [helpWindowRect ()](Scene_MenuBase.md#helpwindowrect---rectangle)
* [mainAreaBottom()](Scene_MenuBase.md#mainareabottom--number)
* [mainAreaHeight()](Scene_MenuBase.md#mainareaheight--number)
* [mainAreaTop()](Scene_MenuBase.md#mainareatop--number)
* [needsCancelButton ()](Scene_MenuBase.md#needscancelbutton---boolean)
* [needsPageButtons ()](Scene_MenuBase.md#needspagebuttons---boolean)
* [nextActor ()](Scene_MenuBase.md#nextactor-)
* [onActorChange ()](Scene_MenuBase.md#onactorchange-)
* [previousActor ()](Scene_MenuBase.md#previousactor-)
* [setBackgroundOpacity (opacity)](Scene_MenuBase.md#setbackgroundopacity-opacity)
* [update ()](Scene_MenuBase.md#update-)
* [updateActor ()](Scene_MenuBase.md#updateactor-)
* [updatePageButtons ()](Scene_MenuBase.md#updatepagebuttons-)

### Methods

#### create ()
Override: [Scene_MenuBase](Scene_MenuBase.md#create-)

#### createEditWindow ()
Creates the edit window.

#### createInputWindow ()
Creates the input window.

#### editWindowRect() → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangle area for the edit window.

#### initialize ()
Override: [Scene_MenuBase](Scene_MenuBase.md#initialize-)

#### inputWindowRect() → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangle area for the input window.

#### onInputOk ()
Handler called when the input is confirmed.

#### prepare (actorId, maxLength)
Prepares the input field with the specified actor and character count.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actorId` | [Number](Number.md) | Actor ID |
| `maxLength` | [Number](Number.md) | Maximum character count |

#### start ()
Override: [Scene_Base](Scene_Base.md#start-)
