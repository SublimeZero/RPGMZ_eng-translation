[Class Tree](index.md)

# Class: Scene_Skill

## Superclass: [Scene_ItemBase](Scene_ItemBase.md)

Scene for [Skills].

Main Path
```js
SceneManager._scene
```

Related Classes: [SceneManager](SceneManager.md), [Window_SkillList](Window_SkillList.md), [Window_SkillStatus](Window_SkillStatus.md) <br />
Related Scenes: [Scene_Menu](Scene_Menu.md)

### new Scene_Skill ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_skillTypeWindow` | [Window_SkillType](Window_SkillType.md) | Skill type selection window |


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
* [checkGameover ()](Scene_Base.md#checkgameover-)
* [createFadeSprite ()](Scene_Base.md#createfadesprite-)
* [createWindowLayer ()](Scene_Base.md#createwindowlayer-)
* [detachReservation ()](Scene_Base.md#detachreservation-)
* [fadeOutAll ()](Scene_Base.md#fadeoutall-)
* [fadeSpeed ()](Scene_Base.md#fadespeed---number)
* [isActive ()](Scene_Base.md#isactive---boolean)
* [isBusy ()](Scene_Base.md#isbusy---boolean)
* [isReady ()](Scene_Base.md#isready---boolean)
* [popScene ()](Scene_Base.md#popscene-)
* [slowFadeSpeed ()](Scene_Base.md#slowfadespeed---number)
* [startFadeIn (duration opt, white opt)](Scene_Base.md#startfadein-duration-opt-white-opt)
* [startFadeOut (duration opt, white opt)](Scene_Base.md#startfadeout-duration-opt-white-opt)
* [start ()](Scene_Base.md#start-)
* [stop ()](Scene_Base.md#stop-)
* [terminate ()](Scene_Base.md#terminate-)
* [updateChildren ()](Scene_Base.md#updatechildren-)
* [updateFade ()](Scene_Base.md#updatefade-)

#### [Scene_MenuBase](Scene_MenuBase.md)

* [actor ()](Scene_MenuBase.md#actor---game_actor)
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
* [nextActor ()](Scene_MenuBase.md#nextactor-)
* [onActorChange ()](Scene_MenuBase.md#onactorchange-)
* [previousActor ()](Scene_MenuBase.md#previousactor-)
* [setBackgroundOpacity (opacity)](Scene_MenuBase.md#setbackgroundopacity-opacity)
* [update ()](Scene_MenuBase.md#update-)
* [updateActor ()](Scene_MenuBase.md#updateactor-)
* [updatePageButtons ()](Scene_MenuBase.md#updatepagebuttons-)

#### [Scene_ItemBase](Scene_ItemBase.md)

* [activateItemWindow ()](Scene_ItemBase.md#activateitemwindow-)
* [actorWindowRect ()](Scene_ItemBase.md#actorwindowrect--rectangle)
* [applyItem ()](Scene_ItemBase.md#applyitem-)
* [canUse ()](Scene_ItemBase.md#canuse---boolean)
* [checkCommonEvent ()](Scene_ItemBase.md#checkcommonevent-)
* [createActorWindow ()](Scene_ItemBase.md#createactorwindow-)
* [determineItem ()](Scene_ItemBase.md#determineitem-)
* [hideActorWindow ()](Scene_ItemBase.md#hideactorwindow-)
* [isCursorLeft ()](Scene_ItemBase.md#iscursorleft---boolean)
* [isItemEffectsValid ()](Scene_ItemBase.md#isitemeffectsvalid---boolean)
* [item ()](Scene_ItemBase.md#item---rpgbusableitem)
* [itemTargetActors ()](Scene_ItemBase.md#itemtargetactors---game_actor)
* [onActorCancel ()](Scene_ItemBase.md#onactorcancel-)
* [onActorOk ()](Scene_ItemBase.md#onactorok-)
* [showActorWindow ()](Scene_ItemBase.md#showactorwindow-)

### Methods

#### arePageButtonsEnabled ()
**@MZ** Override: [Scene_MenuBase](Scene_MenuBase.md#arepagebuttonsenabled---boolean)

#### commandSkill ()
Starts skill selection.

#### create ()
Override: [Scene_ItemBase](Scene_ItemBase.md#create-)

#### createItemWindow ()
Generates the skill item window.

#### createSkillTypeWindow ()
Generates the skill type selection window.

#### createStatusWindow ()
Generates the status window.

#### initialize ()
Override: [Scene_ItemBase](Scene_ItemBase.md#initialize-)

#### itemWindowRect() → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangle area for the item window.

#### needsPageButtons ()
**@MZ** Override: [Scene_MenuBase](Scene_MenuBase.md#needspagebuttons---boolean)

#### onActorChange ()
Override: [Scene_MenuBase](Scene_MenuBase.md#onactorchange-)

#### onItemCancel ()
Handler called when the skill item is canceled.

#### onItemOk ()
Handler called when the skill item is confirmed.

#### playSeForItem ()
Plays the sound set for [Skill Use].

#### refreshActor ()
Redraws the actor.

#### skillTypeWindowRect() → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangle area for the skill type selection window.

#### start ()
Override: [Scene_Base](Scene_Base.md#start-)

#### statusWindowRect() → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangle area for the status window.

#### useItem ()
Override: [Scene_ItemBase](Scene_ItemBase.md#useitem-)

#### user () → {[Game_Actor](Game_Actor.md)}
Override: [Scene_ItemBase](Scene_ItemBase.md#user---gameactor)
