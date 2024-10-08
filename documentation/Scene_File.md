[Class Tree](index.md)

# Class: Scene_File

## Superclass: [Scene_MenuBase](Scene_MenuBase.md)

A scene for handling save files.

Related Classes: [DataManager](DataManager.md)

### new Scene_File ()

### Subclasses

* [Scene_Save](Scene_Save.md)
* [Scene_Load](Scene_Load.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_listWindow` | [Window_SavefileList](Window_SavefileList.md) | The list window for save files. |

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
* [createPageButtons ()](Scene_MenuBase.md#createpagebuttons-)
* [helpAreaBottom()](Scene_MenuBase.md#helpareabottom--number)
* [helpAreaTop() ](Scene_MenuBase.md#mainareatop--number)
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

#### activateListWindow ()
Activates the list window.

#### create ()
Override: [Scene_MenuBase](Scene_MenuBase.md#create-)

#### createHelpWindow ()
Override: [Scene_MenuBase](Scene_MenuBase.md#createhelpwindow-)

#### createListWindow ()
Generates the list window.

#### firstSavefileId () → {[Number](Number.md)}
**@MZ** Returns the ID of the first save file on the screen.

#### helpAreaHeight ()
**@MZ** Override: [Scene_MenuBase](Scene_MenuBase.md#helpareaheight--number)

#### helpWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Override: [Scene_MenuBase](Scene_MenuBase.md#helpwindowrect---rectangle)

#### helpWindowText () → {[String](String.md)}
Returns the text displayed in the help window, set in [System].

#### initialize ()
Override: [Scene_MenuBase](Scene_MenuBase.md#initialize-)

#### isSavefileEnabled (savefileId) → {Boolean}
**@MZ** Checks if the file with the specified ID is available.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `savefileId` | [Number](Number.md) | File ID |

#### listWindowRect() → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangle area of the save file list window.

#### mode () → {[String](String.md)}
Returns the mode ('save' or 'load').

#### needsAutosave () → {Boolean}
**@MZ** Checks if auto-saving is required.

#### onSavefileOk ()
Handler called when a save file is selected.

#### savefileId () → {[Number](Number.md)}
Returns the ID of the current save file.

#### start ()
Override: [Scene_Base](Scene_Base.md#start-)

### Deprecated MV Methods
firstSavefileIndex ()
