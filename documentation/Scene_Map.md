[Class Tree](index.md)

# Class: Scene_Map

## Superclass: [Scene_Message](Scene_Message.md)

Map display scene.

In MV, [Scene_Base](Scene_Base.md) was the superclass, but it has been changed to [Scene_Message](Scene_Message.md).

Main Path
```js
SceneManager._scene
```

Changes were made in v1.5.0 and v1.8.0.

Related Classes: [SceneManager](SceneManager.md), [Tilemap](Tilemap.md), [Game_Timer](Game_Timer.md), [Game_Screen](Game_Screen.md), [Game_Map](Game_Map.md)  
Related Scenes: [Scene_Title](Scene_Title.md), [Scene_Boot](Scene_Boot.md), [Scene_ItemBase](Scene_ItemBase.md), [Scene_Battle](Scene_Battle.md), [Scene_Load](Scene_Load.md)

### new Scene_Map ()

### Properties

| Identifier             | Type                     | Description                  |
|------------------------|--------------------------|------------------------------|
| `menuCalling`          | Boolean                  | Whether the menu is called   |
| `_waitCount`          | [Number](Number.md)      | Wait count                   |
| `_encounterEffectDuration` | [Number](Number.md)      | Remaining time of encounter effect |
| `_mapLoaded`           | Boolean                  | Whether the map is loaded    |
| `_touchCount`          | [Number](Number.md)      | Touch duration                |
| `_transfer`            | Boolean                  | Whether transitioning         |
| `_spriteset`           | [Spriteset_Map](Spriteset_Map.md) | Sprite set                  |
| `_mapNameWindow`       | [Window_MapName](Window_MapName.md) | Map name display window    |

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

#### callMenu ()
Calls the menu.

#### create ()
Override: [Scene_Base](Scene_Base.md#create-)

#### createAllWindows ()
Generates windows.

#### createButtons ()
**@MZ** Generates buttons.

#### createMenuButton ()
**@MZ** Generates the menu button.

#### createDisplayObjects ()
Generates all display objects needed for the scene.

#### createMapNameWindow ()
Generates the map name display window.

#### createSpriteset ()
Generates map sprites ([Spriteset_Map](Spriteset_Map.md)).

#### encounterEffectSpeed () → {[Number](Number.md)}
Returns the speed of the encounter effect (default: 60).

#### fadeInForTransfer ()
Fade in during transition.

#### fadeOutForTransfer ()
Fade out during transition.

#### hideMenuButton ()
**@MZ** Hides the menu button.

#### initialize ()
Override: [Scene_Message](Scene_Message.md#initialize-)

#### isBusy () → {Boolean}
Override: [Scene_Base](Scene_Base.md#isbusy---boolean)

#### isDebugCalled () → {Boolean}
Whether the debug window is called.

#### isFastForward () → {Boolean}
Whether it is in fast forward mode.

#### isMapTouchOk () → {Boolean}
Whether touch movement is possible.

#### isAnyButtonPressed () → {Boolean}
**@MZ** Whether any button is pressed.

#### isMenuCalled () → {Boolean}
Whether the menu is called.

#### isMenuEnabled () → {Boolean}
Whether the menu can be used.

#### isPlayerActive () → {Boolean}
**@MZ** Whether the player can be controlled.

#### isReady () → {Boolean}
Override: [Scene_Base](Scene_Base.md#isready---boolean)

#### isSceneChangeOk () → {Boolean}
Whether scene changes are possible.

#### launchBattle ()
Starts the battle scene.

#### mapNameWindowRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the map name window.

#### needsFadeIn () → {Boolean}
Whether a fade-in is needed.

#### needsSlowFadeOut () → {Boolean}
Whether a fade-out is needed.

#### onMapLoaded ()
Handler when the scene loading is complete.

#### onTransfer ()
**@MZ** Handler when map transition begins.

#### onTransferEnd ()
**@MZ** Handler when map transition ends.

#### processMapTouch ()
Converts touch to character movement.

#### shouldAutosave () → {Boolean}
**@MZ** Whether an auto-save is needed.

#### snapForBattleBackground ()
Displays a snapshot of the map when the battle background is not specified.

#### start ()
Override: [Scene_Base](Scene_Base.md#start-)

#### startEncounterEffect ()
Starts the display of the effect during an encounter.

#### startFlashForEncounter (duration)
Starts the flash during an encounter.

##### Arguments

| Name      | Type                     | Description |
|-----------|--------------------------|-------------|
| `duration` | [Number](Number.md)      |             |

#### stop ()
Override: [Scene_Base](Scene_Base.md#stop-)

#### stopAudioOnBattleStart ()
Stops audio before battle starts.

#### terminate ()
Override: [Scene_Base](Scene_Base.md#terminate-)

#### update ()
Override: [Scene_Base](Scene_Base.md#update-)

#### updateCallDebug ()
Updates the debug window call.

#### updateCallMenu ()
Updates the menu call.

#### updateDestination ()
Updates the display of the touch position.

#### updateEncounter ()
Updates the encounter.

#### updateEncounterEffect ()
Updates the effect during an encounter.

#### updateMain ()
Updates [$gameMap](global.md#gamemap-game_map), [$gamePlayer](global.md#gameplayer-game_player), [$gameTimer](global.md#gametimer-game_timer), [$gameScreen](global.md#gamescreen-game_screen).

#### updateMainMultiply ()
Updates the main. Updates twice in fast forward mode.

#### updateMapNameWindow ()
**@MZ** Updates the map name window.

#### updateMenuButton ()
**@MZ** Updates the menu button.

#### updateScene ()
Updates the scene.

#### updateTransferPlayer ()
Updates the player's map movement.

#### updateWaitCount () → {Boolean}
Updates the wait count.

### Deprecated MV Methods
createMessageWindow (), createScrollTextWindow ()
