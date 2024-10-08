[Class Tree](index.md)

# Class: Window_Message

## Superclass: [Window_Base](Window_Base.md)

A window that displays [messages]. 

The text to be displayed is set through [$gameMessage](global.md#gamemessage-game_message), not directly in `Window_Message`. Therefore, if you only need to display text, there's no need to manipulate this class.<br />
Additionally, `Window_Message` handles the activation of subwindows for choices and options. It acts more like a scene-related class.<br />
If you need a new window to display text, it’s better to either use [Window_Help](Window_Help.md) or create a new class that inherits from `Window_Base`.

Changes were made in versions v1.2.1 and v1.8.0.

Related Classes: [Scene_Message](Scene_Message.md), [Scene_Map](Scene_Map.md), [Scene_Battle](Scene_Battle.md), [Game_Message](Game_Message.md)

---

### new Window_Message (rect)
#### Arguments
There were no arguments in MV.

| Name    | Type                     | Description          |
| ------- | ------------------------ | -------------------- |
| `rect`  | [Rectangle](Rectangle.md) | Rectangle range (in pixels) |

---

### Properties

| Identifier           | Type                           | Description                                  |
| -------------------- | ------------------------------ | -------------------------------------------- |
| `_background`        | [Number](Number.md)            | Type of [background]                         |
| `_positionType`      | [Number](Number.md)            | Type of [window position]                    |
| `_waitCount`         | [Number](Number.md)            | Waiting frame count                          |
| `_faceBitmap`        | [Bitmap](Bitmap.md)            | Image of the face                            |
| `_pauseSkip`         | Boolean                        | Skip input waiting (effect of control character `\^`) |
| `_showFast`          | Boolean                        | Show all text at once (input-based skip)     |
| `_lineShowFast`      | Boolean                        | Display the line all at once (effect of control character `\>`) |
| `_goldWindow`        | [Window_Gold](Window_Gold.md)  | Window for displaying [Gold]                 |
| `_nameBoxWindow`     | [Window_NameBox](Window_NameBox.md) | **@MZ** Window for displaying [Name]         |
| `_choiceListWindow`  | [Window_ChoiceList](Window_ChoiceList.md) | **@MZ** Window for displaying [Choices]      |
| `_numberInputWindow` | [Window_NumberInput](Window_NumberInput.md) | **@MZ** Window for [Number Input]            |
| `_eventItemWindow`   | [Window_EventItem](Window_EventItem.md) | **@MZ** Window for [Item Selection]          |

---

### Deprecated MV Properties
`_choiceWindow`, `_imageReservationId`, `_itemWindow`, `_numberWindow`

---

# Inheritance Tree

- [**Window_Message**]
  - [Window_Base](Window_Base.md)
    - [Window](Window.md)
      - [PIXI.Container](PIXI.Container.md)
        - [PIXI.DisplayObject](PIXI.DisplayObject.md)

---

### Methods inherited from the superclass

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

#### [Window](Window.md)

* [addChildToBack (child)](Window.md#addchildtoback-child--object)
* [addInnerChild (child)](Window.md#addinnerchild-child--object)
* [drawShape (graphics)](Window.md#drawshape-graphics)
* [isClosed ()](Window.md#isclosed---boolean)
* [isOpen ()](Window.md#isopen---boolean)
* [move (x, y, width opt, height opt)](Window.md#move-x-y-width-opt-height-opt)
* [moveCursorBy (x, y)](Window.md#movecursorby-x-y)
* [moveInnerChildrenBy (x, y)](Window.md#moveinnerchildrenby-x-y)
* [setCursorRect (x, y, width, height)](Window.md#setcursorrect-x-y-width-height)
* [setTone (r, g, b)](Window.md#settone-r-g-b)
* [updateTransform ()](Window.md#updatetransform-)

#### [Window_Base](Window_Base.md)

* [activate ()](Window_Base.md#activate-)
* [actorName (actorIndex)](Window_Base.md#actorname-actorindex--string)
* [baseTextRect ()](Window_Base.md#basetextrect---rectangle)
* [calcTextHeight (textState)](Window_Base.md#calctextheight-textstate--number)
* [changeOutlineColor (color)](Window_Base.md#changeoutlinecolor-color)
* [changePaintOpacity (enabled)](Window_Base.md#changepaintopacity-enabled)
* [changeTextColor (color)](Window_Base.md#changetextcolor-color)
* [checkRectObject (rect)](Window_Base.md#checkrectobject-rect)
* [close ()](Window_Base.md#close-)
* [contentsHeight ()](Window_Base.md#contentsheight---number)
* [contentsWidth ()](Window_Base.md#contentswidth---number)
* [convertEscapeCharacters (text)](Window_Base.md#convertescapecharacters-text--string)
* [createContents ()](Window_Base.md#createcontents-)
* [createDimmerSprite () ](Window_Base.md#createdimmersprite-)
* [createTextBuffer (rtl)](Window_Base.md#createtextbuffer-rtl--string)
* [createTextState (text, x, y, width)](Window_Base.md#createtextstate-text-x-y-width--mvtextstate)
* [deactivate ()](Window_Base.md#deactivate-)
* [destroy (options)](Window_Base.md#destroy-options)
* [destroyContents ()](Window_Base.md#destroycontents-)
* [drawCharacter (characterName, characterIndex, x, y)](Window_Base.md#drawcharacter-charactername-characterindex-x-y)
* [drawCurrencyValue (value, unit, x, y, width)](Window_Base.md#drawcurrencyvalue-value-unit-x-y-width)
* [drawFace (faceName, faceIndex, x, y, width opt, height opt)](Window_Base.md#drawface-facename-faceindex-x-y-width-opt-height-opt)
* [drawIcon (iconIndex, x, y)](Window_Base.md#drawicon-iconindex-x-y)
* [drawItemName (item, x, y, width)](Window_Base.md#drawitemname-item-x-y-width)
* [drawRect ( x, y, width, height )](Window_Base.md#drawrect--x-y-width-height-)
* [drawText (text, x, y, maxWidth, align)](Window_Base.md#drawtext-text-x-y-maxwidth-align)
* [drawTextEx (text, x, y, width)](Window_Base.md#drawtextex-text-x-y-width--number)
* [fittingHeight (numLines)](Window_Base.md#fittingheight-numlines--number)
* [flushTextState (textState)](Window_Base.md#flushtextstate-textstate)
* [hide ()](Window_Base.md#hide-)
* [hideBackgroundDimmer ()](Window_Base.md#hidebackgrounddimmer-)
* [initialize (rect)](Window_Base.md#initialize-rect)
* [isClosing ()](Window_Base.md#isclosing---boolean)
* [isOpening ()](Window_Base.md#isopening---boolean)
* [itemHeight ()](Window_Base.md#itemheight---number)
* [itemPadding ()](Window_Base.md#itempadding---number)
* [itemWidth ()](Window_Base.md#itemwidth---number)
* [lineHeight ()](Window_Base.md#lineheight---number)
* [loadWindowskin ()](Window_Base.md#loadwindowskin-)
* [makeFontBigger ()](Window_Base.md#makefontbigger-)
* [makeFontSmaller ()](Window_Base.md#makefontsmaller-)
* [maxFontSizeInLine (line)](Window_Base.md#maxfontsizeinline-line--number)
* [obtainEscapeCode (textState)](Window_Base.md#obtainescapecode-textstate)
* [obtainEscapeParam (textState)](Window_Base.md#obtainescapeparam-textstate--numberstring)
* [open ()](Window_Base.md#open-)
* [partyMemberName (partyMemberIndex)](Window_Base.md#partymembername-partymemberindex--string)
* [playBuzzerSound ()](Window_Base.md#playbuzzersound-)
* [playCursorSound ()](Window_Base.md#playcursorsound-)
* [playOkSound ()](Window_Base.md#playoksound-)
* [processAllText (textState)](Window_Base.md#processalltext-textstate)
* [processCharacter (textState)](Window_Base.md#processcharacter-textstate)
* [processColorChange (colorIndex)](Window_Base.md#processcolorchange-colorindex)
* [processDrawIcon (iconIndex, textState)](Window_Base.md#processdrawicon-iconindex-textstate)
* [processEscapeCharacter (code, textState)](Window_Base.md#processescapecharacter-code-textstate)
* [refreshDimmerBitmap ()](Window_Base.md#refreshdimmerbitmap-)
* [resetFontSettings ()](Window_Base.md#resetfontsettings-)
* [resetTextColor ()](Window_Base.md#resettextcolor-)
* [setBackgroundType (type)](Window_Base.md#setbackgroundtype-type)
* [show ()](Window_Base.md#show-)
* [showBackgroundDimmer ()](Window_Base.md#showbackgrounddimmer-)
* [systemColor ()](Window_Base.md#systemcolor---mvcsscolor)
* [textSizeEx (text)](Window_Base.md#textsizeex-text--number)
* [textWidth (text)](Window_Base.md#textwidth-text--number)
* [translucentOpacity ()](Window_Base.md#translucentopacity---number)
* [updateBackgroundDimmer ()](Window_Base.md#updatebackgrounddimmer-)
* [updateBackOpacity ()](Window_Base.md#updatebackopacity-)
* [updateClose ()](Window_Base.md#updateclose-)
* [updateOpen ()](Window_Base.md#updateopen-)
* [updatePadding ()](Window_Base.md#updatepadding-)
* [updateTone ()](Window_Base.md#updatetone-)

---

### Methods

---

#### areSettingsChanged () → {Boolean}
Checks if the window settings have been changed.

---

#### canBreakHere (textState) → {Boolean}
**@MZ** Determines if a pause is possible.

##### Arguments

| Name        | Type                         | Description          |
| ----------- | ---------------------------- | -------------------- |
| `textState` | [MV.TextState](MV.TextState.md) | Text state to check |

---

#### cancelWait ()
**@MZ1.8.0** Cancels the waiting time.

---

#### canStart () → {Boolean}
Checks if the message can start.

---

#### checkToNotClose ()
Checks to prevent the window from closing.

---

#### clearFlags ()
Clears flags used during [message display].

---

#### doesContinue () → {Boolean}
Checks if there is still text and no settings have changed, i.e., whether the message should continue.

---

#### initialize ()
Overrides: [Window_Base](Window_Base.md#initialize-)

---

#### initMembers ()
Initializes member variables.

---

#### isAnySubWindowActive () → {Boolean}
Checks if any subwindow is active.

---

#### isEndOfText (textState) → {Boolean}
Checks if the specified text state is at the end of the message.

##### Arguments

| Name        | Type                         | Description          |
| ----------- | ---------------------------- | -------------------- |
| `textState` | [MV.TextState](MV.TextState.md) | Text state to check |

---

#### isTriggered () → {Boolean}
Checks if a trigger like OK or Cancel has been activated.

---

#### isWaiting () → {Boolean}
**@MZ1.2.1** Checks if the message window is waiting.

---

#### loadMessageFace ()
Loads the [face] image.

---

#### needsNewPage (textState) → {Boolean}
Checks if the specified text state requires a new page.

##### Arguments

| Name        | Type                         | Description          |
| ----------- | ---------------------------- | -------------------- |
| `textState` | [MV.TextState](MV.TextState.md) | Text state to check |

---

#### newLineX (textState) → {[Number](Number.md)}
Returns the starting position for a new line, considering whether a [face] is displayed or not.

##### Arguments
MV had no arguments, but it became necessary for Arabic support.

| Name        | Type                         | Description          |
| ----------- | ---------------------------- | -------------------- |
| `textState` | [MV.TextState](MV.TextState.md) | Text state to check |

---

#### newPage (textState)
Prepares a new page (window) based on the specified text state.

##### Arguments

| Name        | Type                         | Description          |
| ----------- | ---------------------------- | -------------------- |
| `textState` | [MV.TextState](MV.TextState.md) | Text state to check |

---

#### onEndOfText ()
Handler called when all the message text has been displayed.

---

#### processControlCharacter (textState, c)
Overrides: [Window_Base](Window_Base.md#processcontrolcharacter-textstate-c)

---

#### processNewLine (textState)
Overrides: [Window_Base](Window_Base.md#processnewline-textstate)

---

#### processNewPage (textState)
Overrides: [Window_Base](Window_Base.md#processnewpage-textstate)

---

#### setChoiceListWindow (choiceListWindow)
**@MZ** Sets the [Choice List] window.

##### Arguments

| Name             | Type                             | Description                      |
| ---------------- | -------------------------------- | -------------------------------- |
| `choiceListWindow` | [Window_ChoiceList](Window_ChoiceList.md) | Choice List window to set       |

---

#### setEventItemWindow (eventItemWindow)
**@MZ** Sets the [Event Item] window.

##### Arguments

| Name              | Type                             | Description                      |
| ----------------- | -------------------------------- | -------------------------------- |
| `eventItemWindow` | [Window_EventItem](Window_EventItem.md) | Event Item window to set        |

---

#### setGoldWindow (goldWindow)
**@MZ** Sets the [Gold] window.

##### Arguments

| Name        | Type                          | Description                |
| ----------- | ----------------------------- | -------------------------- |
| `goldWindow` | [Window_Gold](Window_Gold.md) | Gold window to set          |

---

#### setNameBoxWindow (nameBoxWindow)
**@MZ** Sets the [Name] window.

##### Arguments

| Name           | Type                          | Description                |
| -------------- | ----------------------------- | -------------------------- |
| `nameBoxWindow` | [Window_NameBox](Window_NameBox.md) | Name window to set         |

---

#### setNumberInputWindow (numberInputWindow)
**@MZ** Sets the [Number Input] window.

##### Arguments

| Name                | Type                            | Description                      |
| ------------------- | ------------------------------- | -------------------------------- |
| `numberInputWindow` | [Window_NumberInput](Window_NumberInput.md) | Number Input window to set     |

---

#### shouldBreakHere (textState) → {Boolean}
**@MZ** Determines if the message display loop should exit, i.e., if it's in character-by-character display mode.

##### Arguments

| Name        | Type                         | Description          |
| ----------- | ---------------------------- | -------------------- |
| `textState` | [MV.TextState](MV.TextState.md) | Text state to check |

---

#### startInput () → {Boolean}
Starts the input window.<br />
Checks [Game_Message](Game_Message.md) for [isChoice()](Game_Message.md#ischoice---boolean), [isNumberInput()](Game_Message.md#isnumberinput---boolean), or [isItemChoice()](Game_Message.md#isitemchoice---boolean), and opens the corresponding window.

---

#### startMessage ()
Prepares for [message display].

---

#### startPause ()
Begins the pause waiting state.

---

#### startWait (count)
Begins the wait state for the specified count.

##### Arguments

| Name    | Type                | Description           |
| ------- | ------------------- | --------------------- |
| `count` | [Number](Number.md)  | Wait time (in frames) |

---

#### synchronizeNameBox ()
**@MZ** Synchronizes the open/close state of the name window with the [message display] window.

---

#### terminateMessage ()
Stops the [message display] and closes the window.

---

#### update ()
Overrides: [Window_Base](Window_Base.md#update-)

---

#### updateBackground ()
Updates the background.

---

#### updateInput () → {Boolean}
Updates input.

---

#### updateLoading ()
Updates the loading process.

---

#### updateMessage () → {Boolean}
Updates the [message display].

---

#### updatePlacement ()
Updates the window's placement.

---

#### updateShowFast ()
Checks for fast-forward due to buttons, clicks, or taps.

---

#### updateSpeakerName ()
**@MZ** Updates the name of the speaker.

---

#### updateWait () → {Boolean}
Updates the wait state.

---

### Deprecated MV Methods
`createSubWindows()`, `numVisibleRows()`, `subWindows()`, `windowHeight()`, `windowWidth()`
