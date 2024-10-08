# Class: Window_Selectable

## Superclass: [Window_Scrollable](Window_Scrollable.md)

A window that handles the movement of the command cursor and input detection.

In MV, the superclass was [Window_Base](Window_Base.md), but it has been changed to [Window_Scrollable](Window_Scrollable.md) in MZ.

Related classes: [Input](Input.md), [TouchInput](TouchInput.md)

---

### new Window_Selectable (rect)

#### Arguments
In MV, the arguments were x, y, width, height.

| Name   | Type              | Description                   |
|--------|-------------------|-------------------------------|
| `rect` | [Rectangle](Rectangle.md) | Rectangular area (in pixels) |

---

### Subclasses

* [Window_BattleEnemy](Window_BattleEnemy.md)
* [Window_Command](Window_Command.md)
* [Window_DebugEdit](Window_DebugEdit.md)
* [Window_DebugRange](Window_DebugRange.md)
* [Window_ItemList](Window_ItemList.md)
* [Window_NameInput](Window_NameInput.md)
* [Window_NumberInput](Window_NumberInput.md)
* [Window_SavefileList](Window_SavefileList.md)
* [Window_ShopBuy](Window_ShopBuy.md)
* [Window_ShopNumber](Window_ShopNumber.md)
* [Window_SkillList](Window_SkillList.md)
* [Window_StatusBase](Window_StatusBase.md)

---

### Properties

| Name              | Type              | Description                                     |
|-------------------|-------------------|-------------------------------------------------|
| `_index`          | [Number](Number.md) | Index of the selected item                      |
| `_cursorFixed`    | Boolean           | Whether the cursor is fixed                     |
| `_cursorAll`      | Boolean           | Whether all items are selected                  |
| `_helpWindow`     | [Window_Help](Window_Help.md) | Help window                                |
| `_handlers`       | Object            | \{[Input key name](#入力キー名): Handler function, …\} |
| `_doubleTouch`     | Boolean           | **@MZ** Whether the currently selected item is clicked/touched |
| `_canRepeat`      | Boolean           | **@MZ** Whether it can be repeated              |

---

#### Input Key Names

Major input key names in "RPG Maker MZ".<br />
These are converted into common symbolic strings for keyboard, gamepad, touch panel, and mouse inputs.

| String      | Description     |
|-------------|-----------------|
| "ok"       | OK              |
| "cancel"   | Cancel          |
| "up"       | ↑               |
| "down"     | ↓               |
| "left"     | ←               |
| "right"    | →               |
| "pageup"   | Page Up         |
| "pagedown" | Page Down       |

---

### Deprecated MV Properties

`_scrollX`, `_scrollY`, `_stayCount`, `_touching`

---

# Inheritance Tree

- [**Window_Selectable**]
  - [Window_Scrollable](Window_Scrollable.md)
    - [Window_Base](Window_Base.md)
      - [Window](Window.md)
        - [PIXI.Container](PIXI.Container.md)
          - [PIXI.DisplayObject](PIXI.DisplayObject.md)

---

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
* [isClosing ()](Window_Base.md#isclosing---boolean)
* [isOpening ()](Window_Base.md#isopening---boolean)
* [itemPadding ()](Window_Base.md#itempadding---number)
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
* [processControlCharacter (textState, c)](Window_Base.md#processcontrolcharacter-textstate-c)
* [processDrawIcon (iconIndex, textState)](Window_Base.md#processdrawicon-iconindex-textstate)
* [processEscapeCharacter (code, textState)](Window_Base.md#processescapecharacter-code-textstate)
* [processNewLine (textState)](Window_Base.md#processnewline-textstate)
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

#### [Window_Scrollable](Window_Scrollable.md)

* [clearScrollStatus ()](Window_Scrollable.md#clearscrollstatus-)
* [isTouchedInsideFrame ()](Window_Scrollable.md#istouchedinsideframe---boolean)
* [isTouchScrollEnabled ()](Window_Scrollable.md#istouchscrollenabled---boolean)
* [isWheelScrollEnabled ()](Window_Scrollable.md#iswheelscrollenabled---boolean)
* [maxScrollX ()](Window_Scrollable.md#maxscrollx---number)
* [maxScrollY ()](Window_Scrollable.md#maxscrolly---number)
* [onTouchScroll ()](Window_Scrollable.md#ontouchscroll-)
* [onTouchScrollEnd ()](Window_Scrollable.md#ontouchscrollend-)
* [onTouchScrollStart ()](Window_Scrollable.md#ontouchscrollstart-)
* [overallHeight ()](Window_Scrollable.md#overallheight---number)
* [overallWidth ()](Window_Scrollable.md#overallwidth---number)
* [processTouchScroll ()](Window_Scrollable.md#processtouchscroll-)
* [processWheelScroll ()](Window_Scrollable.md#processwheelscroll-)
* [scrollBaseX ()](Window_Scrollable.md#scrollbasex---number)
* [scrollBaseY ()](Window_Scrollable.md#scrollbasey---number)
* [scrollBlockHeight ()](Window_Scrollable.md#scrollblockheight---number)
* [scrollBlockWidth ()](Window_Scrollable.md#scrollblockwidth---number)
* [scrollTo (x, y)](Window_Scrollable.md#scrollto-x-y)
* [scrollX ()](Window_Scrollable.md#scrollx---number)
* [scrollY ()](Window_Scrollable.md#scrolly---number)
* [setScrollAccel (x, y)](Window_Scrollable.md#setscrollaccel-x-y)
* [smoothScrollBy (x, y)](Window_Scrollable.md#smoothscrollby-x-y)
* [smoothScrollDown (n)](Window_Scrollable.md#smoothscrolldown-n)
* [smoothScrollTo (x, y)](Window_Scrollable.md#smoothscrollto-x-y)
* [smoothScrollUp (n)](Window_Scrollable.md#smoothscrollup-n)
* [updateArrows ()](Window_Scrollable.md#updatearrows-)
* [updateOrigin ()](Window_Scrollable.md#updateorigin-)
* [updateScrollAccel ()](Window_Scrollable.md#updatearrows-)
* [updateScrollBase ()](Window_Scrollable.md#updatescrollbase-)
* [updateSmoothScroll ()](Window_Scrollable.md#updatesmoothscroll-)

---

### Methods

#### activate ()
Override: [Window_Base](Window_Base.md#activate-)

---

#### callCancelHandler ()
Calls the cancel handler.

---

#### callHandler (symbol)
Calls the specified handler.

##### Arguments

| Name    | Type              | Description                      |
|---------|-------------------|----------------------------------|
| `symbol`| [String](String.md) | [Input handler name](#input-handler-name) |

---

#### callOkHandler ()
Calls the OK handler.

---

#### callUpdateHelp ()
Calls the update for the help.

---

#### clearItem (index)
Deletes the item at the specified index.

##### Arguments

| Name   | Type              | Description       |
|--------|-------------------|-------------------|
| `index`| [Number](Number.md) | Item number      |

---

#### colSpacing () → {[Number](Number.md)}
**@MZ** Returns the column spacing (default: 8 pixels).

---

#### contentsHeight () → {[Number](Number.md)}
**@MZ** Returns the height of the contents (in pixels).

---

#### cursorAll () → {Boolean}
Checks if all items are selected.

---

#### cursorDown (wrap)
Moves the cursor down.

##### Arguments

| Name   | Type      | Description                       |
|--------|-----------|-----------------------------------|
| `wrap` | Boolean   | Whether to wrap the list         |

---

#### cursorFixed () → {Boolean}
Checks if the cursor is fixed.

---

#### cursorLeft (wrap)
Moves the cursor left.

##### Arguments

| Name   | Type      | Description                       |
|--------|-----------|-----------------------------------|
| `wrap` | Boolean   | Whether to wrap the list         |

---

#### cursorPagedown ()
Moves the cursor to the next page.

---

#### cursorPageup ()
Moves the cursor to the previous page.

---

#### cursorRight (wrap)
Moves the cursor right.

##### Arguments

| Name   | Type      | Description                       |
|--------|-----------|-----------------------------------|
| `wrap` | Boolean   | Whether to wrap the list         |

---

#### cursorUp (wrap)
Moves the cursor up.

##### Arguments

| Name   | Type      | Description                       |
|--------|-----------|-----------------------------------|
| `wrap` | Boolean   | Whether to wrap the list         |

---

#### deactivate ()
Override: [Window_Base](Window_Base.md#deactivate-)

---

#### deselect ()
Deselects all items.

---

#### drawAllItems ()
Draws all items.

---

#### drawBackgroundRect (rect)
**@MZ** Draws the background in the specified area.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `rect` | [Rectangle](Rectangle.md) | Background drawing area |

---

#### drawItem (index)
Draws the item at the specified index.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `index`| [Number](Number.md) | Item number                      |

---

#### drawItemBackground (index)
**@MZ** Draws the background of the item at the specified index.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `index`| [Number](Number.md) | Item number                      |

---

#### ensureCursorVisible (smooth)
Displays the selection cursor.

##### Arguments

In MV, there are no arguments.

| Name   | Type      | Description                       |
|--------|-----------|-----------------------------------|
| `smooth`| Boolean   | Whether to scroll smoothly        |

---

#### forceSelect (index)
**@MZ** Selects the item at the specified index (cursor hidden).

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `index`| [Number](Number.md) | Item number                      |

---

#### hideHelpWindow ()
Hides the help window.

---

#### hitIndex () → {[Number](Number.md)}
**@MZ** Returns the number of the item currently being touched.

---

#### hitTest (x, y) → {[Number](Number.md)}
Determines if the specified coordinates are within the item range and returns the first matching item index from the top.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `x`    | [Number](Number.md) | x-coordinate (in pixels)        |
| `y`    | [Number](Number.md) | y-coordinate (in pixels)        |

---

#### index () → {[Number](Number.md)}
Returns the index of the selected item.

---

#### initialize (rect)
Override: [Window_Scrollable](Window_Scrollable.md#initialize-rect)

---

#### isCancelEnabled () → {Boolean}
Checks if cancellation is possible.

---

#### isCancelTriggered () → {Boolean}
Checks if cancellation has been triggered.

---

#### isCurrentItemEnabled () → {Boolean}
Checks if the currently selected item is available.

---

#### isCursorMovable () → {Boolean}
Checks if the cursor can be moved.

---

#### isHandled (symbol) → {Boolean}
Checks if the specified handler is available.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `symbol`| [String](String.md) | [Input handler name](#input-handler-name) |

---

#### isHorizontal () → {Boolean}
Checks if the commands are arranged in a horizontal row.

---

#### isHoverEnabled () → {Boolean}
**@MZ** Checks if hover is possible.

---

#### isOkEnabled () → {Boolean}
Checks if OK is possible.

---

#### isOkTriggered () → {Boolean}
Checks if OK has been triggered.

---

#### isOpenAndActive () → {Boolean}
Checks if the window is open and active.

---

#### isScrollEnabled () → {Boolean}
**@MZ** Override: [Window_Scrollable](Window_Scrollable.md#isscrollenabled---boolean)

---

#### isTouchOkEnabled () → {Boolean}
Checks if OK is possible via touch input.

---

#### itemHeight () → {[Number](Number.md)}
Override: [Window_Base](Window_Base.md#itemheight---number)

---

#### itemLineRect (index) → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the specified item row.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `index`| [Number](Number.md) | Item number                      |

---

#### itemRect (index) → {[Rectangle](Rectangle.md)}
Returns the rectangular area of the specified item.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `index`| [Number](Number.md) | Item number                      |

---

#### itemRectWithPadding (index) → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area of the item including padding.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `index`| [Number](Number.md) | Item number                      |

---

#### itemWidth () → {[Number](Number.md)}
Override: [Window_Base](Window_Base.md#itemwidth---number)

---

#### maxCols () → {[Number](Number.md)}
Returns the maximum number of columns (counters) the window can hold.

---

#### maxItems () → {[Number](Number.md)}
Returns the maximum number of items the window can hold.

---

#### maxPageItems () → {[Number](Number.md)}
Returns the maximum number of items per page.

---

#### maxPageRows () → {[Number](Number.md)}
Returns the maximum number of rows per page.

---

#### maxRows () → {[Number](Number.md)}
Returns the maximum number of rows the window can hold.

---

#### maxTopRow () → {[Number](Number.md)}
Returns the number of the last topmost row.

---

#### maxVisibleItems () → {[Number](Number.md)}
**@MZ** Returns the maximum number of items that can be displayed in the window.

---

#### onTouchCancel ()
**@MZ** Handler for when the item selection is canceled.

---

#### onTouchOk ()
**@MZ** Handler for when the item is confirmed.

---

#### onTouchSelect (trigger)
**@MZ** Handler for when the item is selected.

##### Arguments

| Name    | Type      | Description                               |
|---------|-----------|-------------------------------------------|
| `trigger`| Boolean   | Whether the touch or confirm (left) button was pressed immediately |

---

#### overallHeight () → {[Number](Number.md)}
**@MZ** Returns the overall height (in pixels).

---

#### processCancel ()
Processes cancellation.

---

#### paint ()
**@MZ** Override: [Window_Scrollable](Window_Scrollable.md#paint-)

---

#### processCursorMove ()
Processes cursor movement.

---

#### processHandling ()
Processes added handlers.

---

#### processOk ()
Processes OK.

---

#### processPagedown ()
Processes page down.

---

#### processPageup ()
Processes page up.

---

#### processTouch ()
Processes touch input.

---

#### processWheel ()
Processes wheel input.

---

#### redrawCurrentItem ()
Redraws the current item.

---

#### redrawItem (index)
Redraws the item at the specified index.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `index`| [Number](Number.md) | Item number                      |

---

#### refresh ()
Redraws the content.

---

#### refreshCursor ()
**@MZ** Redraws the cursor.

---

#### refreshCursorForAll ()
**@MZ** Redraws the all-select cursor.

---

#### reselect ()
Reselects the item.

---

#### row () → {[Number](Number.md)}
Returns the current row number.

---

#### rowSpacing () → {[Number](Number.md)}
**@MZ** Returns the row spacing (default: 4 pixels).

---

#### smoothSelect (index)
**@MZ** Selects the item at the specified index.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `index`| [Number](Number.md) | Item number                      |

---

#### select (index)
Selects the item at the specified index.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `index`| [Number](Number.md) | Item number (starting from 0)    |

---

#### setCursorAll (cursorAll)
Sets the state of all item selection.

##### Arguments

| Name       | Type      | Description                       |
|------------|-----------|-----------------------------------|
| `cursorAll`| Boolean   | Whether all are selected         |

---

#### setCursorFixed (cursorFixed)
Sets the fixed state of the cursor.

##### Arguments

| Name        | Type      | Description                       |
|-------------|-----------|-----------------------------------|
| `cursorFixed`| Boolean   | Whether the cursor is fixed      |

---

#### setHandler (symbol, method)
Sets a handler.

##### Arguments

| Name    | Type              | Description                       |
|---------|-------------------|-----------------------------------|
| `symbol`| [String](String.md) | [Input handler name](#input-handler-name) |
| `method`| Function          | Handler function                  |

---

#### setHelpWindow (helpWindow)
Sets the help window.

##### Arguments

| Name        | Type                  | Description                       |
|-------------|-----------------------|-----------------------------------|
| `helpWindow`| [Window_Help](Window_Help.md) | Help window                   |

---

#### setHelpWindowItem (item)
Displays the specified item in the help window.

##### Arguments

| Name   | Type                                              | Description                |
|--------|---------------------------------------------------|----------------------------|
| `item` | [RPG.BaseItem](RPG.BaseItem.md) \| [String](String.md) | Item to be set            |

---

#### setTopRow (row)
Sets the top row.

##### Arguments

| Name   | Type              | Description                       |
|--------|-------------------|-----------------------------------|
| `row`  | [Number](Number.md) | Row number                      |

---

#### showHelpWindow ()
Displays the help window.

---

#### topIndex () → {[Number](Number.md)}
Returns the number of the item at the top of the scroll list.

---

#### topRow () → {[Number](Number.md)}
Returns the number of the top row.

---

#### update ()
Override: [Window_Scrollable](Window_Scrollable.md#update-)

---

#### updateHelp ()
Updates the help window.

---

#### updateInputData ()
Updates the input data.

---

### Deprecated MV Methods
`bottomRow()`, `isContentsArea(x, y)`, `isCursorVisible()`, `isTouchedInsideFrame()`, `itemRectForText(index)`, `onTouch(triggered)`, `playBuzzerSound()`, `playOkSound()`, `resetScroll()`, `scrollDown()`, `scrollUp()`, `setBottomRow(row)`, `spacing()`, `updateCursor()`, `updateArrows()`
