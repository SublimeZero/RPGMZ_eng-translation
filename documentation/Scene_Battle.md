[Class Tree](index.md)

# Class: Scene_Battle

## Superclass: [Scene_Message](Scene_Message.md)

A class that manages the command and message windows for the battle scene, as well as the images of [enemy characters] and side-view [actors].

In MV, the superclass was [Scene_Base](Scene_Base.md), but it has been changed to [Scene_Message](Scene_Message.md).

Main Path
```js
SceneManager._scene
```
Related Classes: [SceneManager](SceneManager.md), [Game_Actor](Game_Actor.md), [Game_Party](Game_Party.md), [Game_Enemy](Game_Enemy.md), [Game_Troop](Game_Troop.md), [Scene_Battle](Scene_Battle.md), [BattleManager](BattleManager.md), [Game_Timer](Game_Timer.md), [Game_Screen](Game_Screen.md)<br />
Related Scenes: [Scene_Boot](Scene_Boot.md), [Scene_Map](Scene_Map.md), [Scene_GameEnd](Scene_GameEnd.md), [Scene_Gameover](Scene_Gameover.md)

### new Scene_Battle ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_spriteset` | [Spriteset_Battle](Spriteset_Battle.md) | Battle sprite set |
| `_statusWindow` | [Window_BattleStatus](Window_BattleStatus.md) | [Status] window |
| `_partyCommandWindow` | [Window_PartyCommand](Window_PartyCommand.md) | [Party] command window |
| `_actorCommandWindow` | [Window_ActorCommand](Window_ActorCommand.md) | [Actor] command window |
| `_skillWindow` | [Window_BattleSkill](Window_BattleSkill.md) | [Skill] window |
| `_itemWindow` | [Window_BattleItem](Window_BattleItem.md) | [Item] window |
| `_actorWindow` | [Window_BattleActor](Window_BattleActor.md) | [Actor] selection window |
| `_enemyWindow` | [Window_BattleEnemy](Window_BattleEnemy.md) | [Enemy character] selection window |
| `_logWindow` | [Window_BattleLog](Window_BattleLog.md) | Log window |
| `_helpWindow` | [Window_Help](Window_Help.md) | Help window |

### Deprecated MV Properties
`_scrollTextWindow`, `_messageWindow` 

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

* [addChild (child)](PIXI.Container.md#addchild-child--pixidisplayobject)
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
* [updateChildren ()](Scene_Base.md#updatechildren-)
* [updateFade ()](Scene_Base.md#updatefade-)

#### [Scene_Message](Scene_Message.md)
* [associateWindows ()](Scene_Message.md#associatewindows-)
* [createAllWindows ()](Scene_Message.md#createallwindows-)
* [createChoiceListWindow ()](Scene_Message.md#createchoicelistwindow-)
* [createEventItemWindow ()](Scene_Message.md#createeventitemwindow-)
* [createGoldWindow ()](Scene_Message.md#creategoldwindow-)
* [createMessageWindow ()](Scene_Message.md#createmessagewindow-)
* [createNameBoxWindow ()](Scene_Message.md#createnameboxwindow-)
* [createNumberInputWindow ()](Scene_Message.md#createnumberinputwindow-)
* [createScrollTextWindow ()](Scene_Message.md#createscrolltextwindow-)
* [eventItemWindowRect()](Scene_Message.md#eventitemwindowrect--rectangle)
* [goldWindowRect()](Scene_Message.md#goldwindowrect--rectangle)
* [isMessageWindowClosing ()](Scene_Message.md#ismessagewindowclosing---boolean)
* [messageWindowRect()](Scene_Message.md#messagewindowrect--rectangle)
* [scrollTextWindowRect()](Scene_Message.md#scrolltextwindowrect--rectangle)

### Methods

#### actorCommandWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the [Actor] command window.

#### actorWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the [Actor] selection window.

#### buttonAreaTop() → {[Number](Number.md)}
**@MZ** Returns the top edge coordinate of the button area.

#### windowAreaHeight() → {[Number](Number.md)}
**@MZ** Returns the height of the window area.

#### changeInputWindow ()
Switches the selection and deselection state of the [Party] or [Actor] command window based on conditions.

#### closeCommandWindows ()
**@MZ** Closes the command windows.

#### commandAttack ()
Handler for the [Attack] command.

#### commandCancel ()
**@MZ** Handler for the [Cancel] command.

#### commandEscape ()
Handler for the [Escape] command.

#### commandFight ()
Handler for the [Fight] command.

#### commandGuard ()
Handler for the [Guard] command.

#### commandItem ()
Handler for the [Item] command.

#### commandSkill ()
Handler for the [Skill] command.

#### create ()
Override: [Scene_Base](Scene_Base.md#create-)

#### createActorCommandWindow ()
Generates the [Actor] command window ([Window_ActorCommand](Window_ActorCommand.md)).

#### createActorWindow ()
Generates the [Actor] selection window ([Window_BattleActor](Window_BattleActor.md)).

#### createAllWindows ()
Generates all the necessary windows for the battle scene.

#### createButtons ()
**@MZ** Generates buttons.

#### createCancelButton ()
**@MZ** Generates the cancel button.

#### createDisplayObjects ()
Generates the objects necessary for display, including sprite sets, window layers, and windows.

#### createEnemyWindow ()
Generates the [Enemy character] selection window ([Window_BattleEnemy](Window_BattleEnemy.md)).

#### createHelpWindow ()
Generates the help window ([Window_Help](Window_Help.md)).

#### createItemWindow ()
Generates the [Item] window ([Window_BattleItem](Window_BattleItem.md)).

#### createLogWindow ()
Generates the log window ([Window_BattleLog](Window_BattleLog.md)).

#### createPartyCommandWindow ()
Generates the [Party] command window ([Window_PartyCommand](Window_PartyCommand.md)).

#### createSkillWindow ()
Generates the [Skill] window ([Window_BattleSkill](Window_BattleSkill.md)).

#### createSpriteset ()
Generates the sprite set necessary for the battle scene, including [Actors] and [Enemies].

#### createStatusWindow ()
Generates the [Status] window ([Window_BattleStatus](Window_BattleStatus.md)).

#### endCommandSelection ()
Ends the command selection process.

#### enemyWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the [Enemy] selection window.

#### helpAreaTop() → {[Number](Number.md)}
**@MZ** Returns the top edge coordinate of the [Help] area.

#### helpAreaBottom() → {[Number](Number.md)}
**@MZ** Returns the bottom edge coordinate of the [Help] area.

#### helpAreaHeight() → {[Number](Number.md)}
**@MZ** Returns the height of the [Help] area.

#### helpWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the [Help] window.

#### hideSubInputWindows ()
**@MZ** Hides the sub-input windows.

#### itemWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the [Item] window.

#### initialize ()
Override: [Scene_Message](Scene_Message.md#initialize-)

#### isAnyInputWindowActive () → {Boolean}
Checks if any input window is active.

#### logWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the log window.

#### needsInputWindowChange () → {Boolean}
**@MZ** Checks if an input window change is needed.

#### needsSlowFadeOut () → {Boolean}
Checks if a slow fade-out is needed.

#### onActorCancel ()
Handler for when [Cancel] is selected in the [Actor] selection window.

#### onActorOk ()
Handler for when [OK] is selected in the [Actor] selection window.

#### onEnemyCancel ()
Handler for when [Cancel] is selected in the [Enemy character] selection window.

#### onEnemyOk ()
Handler for when [OK] is selected in the [Enemy character] selection window.

#### onItemCancel ()
Handler for when [Cancel] is selected in the [Item] window.

#### onItemOk ()
Handler for when [OK] is selected in the [Item] window.

#### onSelectAction ()
Handler for when an item or skill is selected.

#### onSkillCancel ()
Handler for when [Cancel] is selected in the [Skill] window.

#### onSkillOk ()
Handler for when [OK] is selected in the [Skill] window.

#### partyCommandWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the [Party] window.

#### selectNextCommand ()
Selects the next command.

#### selectPreviousCommand ()
Selects the previous command.

#### shouldAutosave() → {Boolean}
**@MZ** Checks if auto-saving is needed.

#### shouldOpenStatusWindow() → {Boolean}
**@MZ** Checks if the [Status] window needs to be opened.

#### skillWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the [Skill] window.

#### start ()
Override: [Scene_Base](Scene_Base.md#start-)

#### startActorCommandSelection ()
Starts the selection of [Actor] commands.

#### selectActorSelection ()
**@MZ** Starts the selection of the [Actor] selection window.

#### startEnemySelection ()
**@MZ** Starts the selection of the [Enemy character] selection window.

#### startPartyCommandSelection ()
Starts the selection of [Party] commands.

#### statusWindowX() → {[Number](Number.md)}
**@MZ** Returns the x-coordinate of the [Status] window.

#### statusWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the [Status] window.

#### stop ()
Override: [Scene_Base](Scene_Base.md#stop-)

#### terminate ()
Override: [Scene_Base](Scene_Base.md#terminate-)

#### update ()
Override: [Scene_Base](Scene_Base.md#update-)

#### updateBattleProcess ()
Updates the battle phase.

#### updateCancelButton ()
**@MZ** Updates the cancel button.

#### updateInputWindowVisibility ()
**@MZ** Updates the visibility state of the input window.

#### updateLogWindowVisibility ()
**@MZ** Updates the visibility state of the log window.

#### updateStatusWindowPosition ()
**@MZ** Updates the position of the [Status] window.

#### updateStatusWindowVisibility ()
**@MZ** Updates the visibility state of the [Status] window.

#### updateVisibility()
**@MZ** Updates the visibility state.

### Deprecated MV Methods
`createMessageWindow()`, `createScrollTextWindow()`, `refreshStatus()`, `selectActorSelection()`, `selectEnemySelection()`, `updateStatusWindow()`, `updateWindowPositions()`
