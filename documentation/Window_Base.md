# Class: Window_Base

## Superclass: [Window](Window.md)

A window object that has many methods for drawing messages and images. <br />
Most features use [Bitmap](Bitmap.md) methods on `contents`.

In MZ, color-related functions have been moved to [ColorManager](ColorManager.md), and status rendering has been moved to [Window_StatusBase](Window_StatusBase.md). <br />
Additionally, the rendering of individual elements has been decomposed into sprites such as [Sprite_Gauge](Sprite_Gauge.md), [Sprite_StateIcon](Sprite_StateIcon.md), and [Sprite_Name](Sprite_Name.md). <br />
Properties such as image sizes have been moved to [ImageManager](ImageManager.md).

Changes were made in versions 1.1.1, 1.2.0, 1.3.0, and 1.6.0.

Related classes: [Graphics](Graphics.md), [Scene_Base](Scene_Base.md), [WindowLayer](WindowLayer.md), [Game_Message](Game_Message.md)

---

### new Window_Base (rect)
#### Arguments
In MV, the arguments were x, y, width, and height.

| Name   | Type              | Description      |
| ------ | ----------------- | ---------------- |
| `rect` | [Rectangle](Rectangle.md) | Rectangular area (pixels) |

---

### Subclasses

* [Window_BattleLog](Window_BattleLog.md)
* [Window_Help](Window_Help.md)
* [Window_MapName](Window_MapName.md)
* [Window_Message](Window_Message.md)
* [Window_NameBox](Window_NameBox.md)
* [Window_ScrollText](Window_ScrollText.md)
* [Window_Scrollable](Window_Scrollable.md)

---

### Properties

| Identifier      | Type               | Description                          |
| --------------- | ------------------ | ------------------------------------ |
| `_opening`      | Boolean            | Whether the window is currently opening |
| `_closing`      | Boolean            | Whether the window is currently closing |
| `_dimmerSprite` | [Sprite](Sprite.md) | Background that dims the window      |

---

### Deprecated MV Properties
`_iconHeight`, `_iconWidth`, `_faceHeight`, `_faceWidth`

---

# Inheritance Tree

- [**Window_Base**]
  - [**Window**](Window.md)
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

---

### Methods

---

#### activate ()
Activates the window.

---

#### actorName (actorIndex) → {[String](String.md)}
Returns the name of the [actor] with the specified index.

##### Arguments

| Name         | Type              | Description                     |
|--------------|-------------------|---------------------------------|
| `actorIndex` | [Number](Number.md) | Actor's index (starting from 1) |

---

#### baseTextRect () → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area for text display. <br />
Used in [Window_NameBox](Window_NameBox.md), [Window_Help](Window_Help.md), and [Window_ScrollText](Window_ScrollText.md) instead of [Window_Message](Window_Message.md).

---

#### calcTextHeight (textState) → {[Number](Number.md)}
Calculates and returns the height (in pixels) when displaying the specified text.

##### Arguments
The `all` argument has been deprecated in MZ.

| Name         | Type                      | Description                      |
|--------------|---------------------------|----------------------------------|
| `textState`  | [MV.TextState](MV.TextState.md) | Information about the text to calculate |

---

#### changeOutlineColor (color)
**@MZ** Sets the outline color of the text.

##### Arguments

| Name   | Type                   | Description            |
|--------|------------------------|------------------------|
| `color`| [MV.CssColor](MV.CssColor.md) | Color (CSS string)    |

---

#### changePaintOpacity (enabled)
Sets whether the drawing is opaque. <br />
Mainly used to express selection availability.

##### Arguments

| Name     | Type     | Description                          |
|----------|----------|--------------------------------------|
| `enabled`| Boolean  | true: Opaque (255), false: Semi-transparent (160) |

---

#### changeTextColor (color)
Sets the color of the text.

##### Arguments

| Name   | Type                   | Description            |
|--------|------------------------|------------------------|
| `color`| [MV.CssColor](MV.CssColor.md) | Color (CSS string)    |

---

#### checkRectObject (rect)
**@MZ** Checks if the argument is a Rectangle; raises an error if not.

##### Arguments

| Name   | Type                   | Description                     |
|--------|------------------------|---------------------------------|
| `rect` | [Rectangle](Rectangle.md) | Rectangular area (pixels)      |

---

#### close ()
Closes the window.

---

#### contentsHeight () → {[Number](Number.md)}
Returns the height of the contents included in the window.

---

#### contentsWidth () → {[Number](Number.md)}
Returns the width of the contents included in the window.

---

#### convertEscapeCharacters (text) → {[String](String.md)}
**@MZ** Converts escape characters and returns the result. <br />
**@MZ1.6.0** Removed the two-level limitation for \V[n] expansion.

##### Arguments

| Name   | Type                   | Description                      |
|--------|------------------------|----------------------------------|
| `text` | [String](String.md)    | The string to convert            |

---

#### createDimmerSprite ()
**@MZ** Generates the background to dim the window.

---

#### createTextBuffer (rtl) → {[String](String.md)}
**@MZ** Returns a string that matches the specified text direction.

##### Arguments
`rtl` stands for RIGHT-TO-LEFT.

| Name   | Type     | Description                        |
|--------|----------|------------------------------------|
| `rtl`  | Boolean  | Is the string right-to-left (Arabic, etc.)? |

---

#### createContents ()
Generates the content area for displaying text and more.

---

#### createTextState (text, x, y, width) → {[MV.TextState](MV.TextState.md)}
**@MZ** Generates and returns a text state.

##### Arguments

| Name   | Type                   | Description                     |
|--------|------------------------|---------------------------------|
| `text` | [String](String.md)    | The string                     |
| `x`    | [Number](Number.md)    | x-coordinate (pixels)          |
| `y`    | [Number](Number.md)    | y-coordinate (pixels)          |
| `width`| [Number](Number.md)    | Width (pixels)                 |

---

#### deactivate ()
Deactivates the window.

---

#### destroy (options)
**@MZ** Override: [Window](Window.md#destroy-)

##### Arguments

| Name     | Type    | Description                               |
|----------|---------|-------------------------------------------|
| `options`| Object  | { children: Boolean, texture: Boolean } (unused) |

---

#### destroyContents ()
**@MZ** Disposes of the contents.

---

#### drawCharacter (characterName, characterIndex, x, y)
Draws the character at the specified position using the filename and character number from the "img/characters/" folder. <br />
Character numbers start from the top-left and progress to the right, moving to the next row afterward. For $-prefixed characters, only 0 is valid. The displayed pattern is facing down in the center. <br />
Since the specified coordinates are for the feet, you need to adjust to specify the top-left corner by using x+24, y+48.

##### Arguments

| Name             | Type                   | Description                          |
|------------------|------------------------|--------------------------------------|
| `characterName`  | [String](String.md)    | Filename (excluding .png extension)  |
| `characterIndex` | [Number](Number.md)    | Character index (0 to 7)            |
| `x`              | [Number](Number.md)    | Feet's x-coordinate (pixels)        |
| `y`              | [Number](Number.md)    | Feet's y-coordinate (pixels)        |

---

#### drawCurrencyValue (value, unit, x, y, width)
Draws the amount of money at the specified position with the currency unit.

##### Arguments

| Name   | Type                   | Description                     |
|--------|------------------------|---------------------------------|
| `value`| [Number](Number.md)    | Amount of money                 |
| `unit` | [String](String.md)    | Currency unit                   |
| `x`    | [Number](Number.md)    | x-coordinate (pixels)          |
| `y`    | [Number](Number.md)    | y-coordinate (pixels)          |
| `width` | [Number](Number.md)   | Width of the drawing area (pixels) |

---

#### drawFace (faceName, faceIndex, x, y, width opt, height opt)
Draws the face image at the specified position using the filename and character number from the "img/faces/" folder. <br />
Character numbers start from the top-left and progress to the right.

##### Arguments

| Name       | Type                   | Properties | Description                        |
|------------|------------------------|------------|------------------------------------|
| `faceName` | [String](String.md)    |            | Filename (excluding .png extension) |
| `faceIndex`| [Number](Number.md)    |            | Character index (0 to 7)          |
| `x`       | [Number](Number.md)    |            | x-coordinate (pixels)             |
| `y`       | [Number](Number.md)    |            | y-coordinate (pixels)             |
| `width`   | [Number](Number.md)    | <optional> | Width (pixels)                    |
| `height`  | [Number](Number.md)    | <optional> | Height (pixels)                   |

---

#### drawIcon (iconIndex, x, y)
Draws the specified icon number at the designated position. <br />
The icon is drawn from the "img/system/IconSet.png" file, divided into 16×20 sections. 
Icon numbers start from the top-left and progress to the right, moving down to the next row when reaching the end.

##### Arguments

| Name      | Type                   | Description                      |
|-----------|------------------------|----------------------------------|
| `iconIndex` | [Number](Number.md)  | Icon index (0 to 319)           |
| `x`      | [Number](Number.md)    | x-coordinate (pixels)           |
| `y`      | [Number](Number.md)    | y-coordinate (pixels)           |

---

#### drawItemName (item, x, y, width)
Draws the [name] of the specified [item] at the designated position.

##### Arguments

| Name   | Type                   | Description                     |
|--------|------------------------|---------------------------------|
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Target [item]                   |
| `x`    | [Number](Number.md)    | x-coordinate (pixels)          |
| `y`    | [Number](Number.md)    | y-coordinate (pixels)          |
| `width`| [Number](Number.md)    | Width of the drawing area (pixels) |

---

#### drawRect ( x, y, width, height )
**@MZ** Draws a rectangle.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x-coordinate (pixels) |
| `y` | [Number](Number.md) | y-coordinate (pixels) |
| `width` | [Number](Number.md) | Width of the drawing area (pixels) |
| `height` | [Number](Number.md) | Height of the drawing area (pixels) |


---

#### drawText (text, x, y, maxWidth, align)
Draws the specified string at the specified position.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `text` | [String](String.md) \| [Number](Number.md) | The string to display |
| `x` | [Number](Number.md) | x-coordinate (pixels) |
| `y` | [Number](Number.md) | y-coordinate (pixels) |
| `maxWidth` | [Number](Number.md) | Maximum allowable width (pixels) |
| `align` | [String](String.md) | Text alignment (left, center, right) |


---

#### drawTextEx (text, x, y, width) → {[Number](Number.md)}
Draws a string with escape characters at the specified position and returns the difference in the x-coordinate.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `text` | [String](String.md) | The string to display |
| `x` | [Number](Number.md) | x-coordinate (pixels) |
| `y` | [Number](Number.md) | y-coordinate (pixels) |
| `width` | [Number](Number.md) | Width (pixels) |


---

#### fittingHeight (numLines) → {[Number](Number.md)}
Returns the height required for the specified number of lines.<br />
Height = Number of lines * Line height + Padding width * 2.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `numLines` | [Number](Number.md) | Number of lines |


---

#### flushTextState (textState)
**@MZ** Draws the characters accumulated in `textState.buffer`.<br />
Supports right-to-left display for languages like Arabic.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `textState` | [MV.TextState](MV.TextState.md) | The string with processing state |


---

#### hide ()
Hides the window (does not close it).


---

#### hideBackgroundDimmer ()
Hides the background dimmer.


---

#### initialize (rect)
Override: [Window](Window.md#initialize-)

##### Arguments
In MV, the arguments were x, y, width, height.

| Name | Type | Description |
| --- | --- | --- |
| `rect` | [Rectangle](Rectangle.md) | Rectangle area (pixels) |


---

#### isClosing () → {Boolean}
Checks if the window is in the process of closing.


---

#### isOpening () → {Boolean}
Checks if the window is in the process of opening.


---

#### itemHeight () → {[Number](Number.md)}
**@MZ** Returns the height of an item (default: 36 pixels).


---

#### itemPadding () → {[Number](Number.md)}
**@MZ** Returns the padding width of an item (default: 8 pixels).


---

#### itemWidth () → {[Number](Number.md)}
**@MZ** Returns the width of an item.


---

#### lineHeight () → {[Number](Number.md)}
Returns the line height (default: 36 pixels).


---

#### loadWindowskin ()
Loads the window skin from "img/system/Window.png".


---

#### makeFontBigger ()
Increases the font size by 12. Handles control character \\\{.


---

#### makeFontSmaller ()
Decreases the font size by 12. Handles control character \\\}.


---

#### maxFontSizeInLine (line) → {[Number](Number.md)}
**@MZ** Returns the maximum font size for the specified line.

---

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `line` | [String](String.md) | String containing control characters |


---

#### obtainEscapeCode (textState) → {[String](String.md)}
Returns the actual control character in uppercase from the index in textState.<br />
The index advances by the number of characters retrieved.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `textState` | [MV.TextState](MV.TextState.md) | The string with processing state |


---

#### obtainEscapeParam (textState) → {[Number](Number.md) | [String](String.md)}
Returns the index of the control character contained in textState from the index onward.<br />
The index advances by the number of characters retrieved.<br />
If an index exists, a number is returned; if not, an empty string is returned.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `textState` | [MV.TextState](MV.TextState.md) | The string with processing state |


---

#### open ()
Opens the window.


---

#### partyMemberName (partyMemberIndex) → {[String](String.md)}
Returns the name corresponding to the specified party member number.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `partyMemberIndex` | [Number](Number.md) | Party member number (starts from 1) |


---

#### playBuzzerSound ()
**@MZ** Plays the [buzzer] sound.


---

#### playCursorSound ()
**@MZ** Plays the [cursor] sound.


---

#### playOkSound ()
**@MZ** Plays the [ok] sound.


---

#### processAllText (textState)
**@MZ** Processes all characters.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `textState` | [MV.TextState](MV.TextState.md) | The string with processing state |


---

#### processCharacter (textState)
Processes characters including new lines, page breaks, and escape characters.<br />
The index advances by the number of characters processed.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `textState` | [MV.TextState](MV.TextState.md) | The string with processing state |


---

#### processColorChange (colorIndex)
**@MZ** Changes to the specified text color. Processes control character \\C[n].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `colorIndex` | [Number](Number.md) | Color number |


---

#### processControlCharacter (textState, c)
**@MZ** Processes control characters.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `textState` | [MV.TextState](MV.TextState.md) | The string with processing state |
| `c` | [String](String.md) | Control character |


---

#### processDrawIcon (iconIndex, textState)
Displays an icon. Processes control character \\I[n].<br />
The index advances by the number of characters processed.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `iconIndex` | [Number](Number.md) | Icon number (0 to 319) |
| `textState` | [MV.TextState](MV.TextState.md) | The string with processing state |


---

#### processEscapeCharacter (code, textState)
Processes control characters.<br />
The index advances by the number of characters processed.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `code` | [String](String.md) | Control character (C I PX PY FS \{ \}) |
| `textState` | [MV.TextState](MV.TextState.md) | The string with processing state |


---

#### processNewLine (textState)
Processes new lines.<br />
The index advances by the number of characters processed.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `textState` | [MV.TextState](MV.TextState.md) | The string with processing state |


---

#### refreshDimmerBitmap ()
Redraws the [dimming] background.


---

#### resetFontSettings ()
Resets font settings to defaults.


---

#### resetTextColor ()
Resets text color to defaults.


---

#### setBackgroundType (type)
Sets the type of background.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `type` | [Number](Number.md) | 0: opacity 255 (standard), 1: displayed dimly, others: opacity 0 |


---

#### show ()
Displays the window.


---

#### showBackgroundDimmer ()
Displays the [dimming] background.


---

#### systemColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the system color.


---

#### textSizeEx (text) → {[MV.Size](MV.Size.md)}
**@MZ** Returns the text size after modification by control characters.


---

#### textWidth (text) → {[Number](Number.md)}
Returns the width (in pixels) of the specified string when drawn.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `text` | [String](String.md) | The string to measure |


---

#### translucentOpacity () → {[Number](Number.md)}
Returns the opacity when inactive (default: 160).


---

#### update ()
Override: [Window](Window#update-)


---

#### updateBackgroundDimmer ()
Updates the [dimming] background.


---

#### updateBackOpacity ()
Updates the background opacity.


---

#### updateClose ()
Updates the state of the window as being closed.


---

#### updateOpen ()
Updates the state of the window as being opened.


---

#### updatePadding ()
Updates the padding width.


---

#### updateTone ()
Updates the [tone].


---

### Deprecated MV Methods
textColor (n), normalColor (), mpColor (actor), mpCostColor (), mpGaugeColor1 (), mpGaugeColor2 (), tpColor (actor), tpCostColor (), tpGaugeColor1 (), tpGaugeColor2 (), crisisColor (), deathColor (), dimColor1 (), dimColor2 (), gaugeBackColor (), hpColor (actor), hpGaugeColor1 (), hpGaugeColor2 (), paramchangeTextColor (change), pendingColor (), powerDownColor (), powerUpColor (),
canvasToLocalX (x), canvasToLocalY (y),
drawActorCharacter (actor, x, y), drawActorClass (actor, x, y, width), drawActorHp (actor, x, y, width), drawActorFace (actor, x, y, width, height), drawActorIcons (actor, x, y, width), drawActorLevel (actor, x, y), drawActorMp (actor, x, y, width), drawActorName (actor, x, y, width), drawActorNickname (actor, x, y, width), drawActorSimpleStatus (actor, x, y, width), drawActorTp (actor, x, y, width),
drawCurrentAndMax (current, max, x, y, width, color1, color2), drawGauge (x, y, width, rate, color1, color2),
processNewPage (textState), processNormalCharacter (textState), reserveFaceImages (), standardBackOpacity (), standardFontFace (), standardFontSize (), standardPadding (), textPadding ()
