# Class: Window_Scrollable

## Superclass: [Window_Base](Window_Base.md)

**@MZ** A window that displays scrollable items.

### new Window_Scrollable (rect)
#### Arguments

| Name  | Type           | Description                      |
|-------|----------------|----------------------------------|
| `rect`| [Rectangle](Rectangle.md) | Rectangle area (in pixels) |

### Subclasses

* [Window_Selectable](Window_Selectable.md)

### Properties

| Identifier                | Type           | Description                      |
|---------------------------|----------------|----------------------------------|
| `_scrollX`               | [Number](Number.md) | Amount of scroll in the x direction |
| `_scrollY`               | [Number](Number.md) | Amount of scroll in the y direction |
| `_scrollAccelX`          | [Number](Number.md) | Scroll acceleration in the x direction |
| `_scrollAccelY`          | [Number](Number.md) | Scroll acceleration in the y direction |
| `_scrollBaseX`           | [Number](Number.md) | Scroll base point in the x direction |
| `_scrollBaseY`           | [Number](Number.md) | Scroll base point in the y direction |
| `_scrollDuration`        | [Number](Number.md) | Duration of the scroll |
| `_scrollTargetX`         | [Number](Number.md) | Target scroll position in the x direction |
| `_scrollTargetY`         | [Number](Number.md) | Target scroll position in the y direction |
| `_scrollTouching`        | Boolean         | Indicates if the item is being touched |
| `_scrollLastCursorVisible`| Boolean        | Indicates if the last touch cursor should be visible |
| `_scrollLastTouchX`      | [Number](Number.md) | Last touch x position |
| `_scrollLastTouchY`      | [Number](Number.md) | Last touch y position |

---

# Inheritance Tree

- [**Window_Scrollable**]
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

---

### Methods

#### clearScrollStatus ()
Initializes the scroll status.

---

#### initialize (rect)
Override: [Window_Base](Window_Base.md#initialize-rect)

---

#### isScrollEnabled () → {Boolean}
Checks if scrolling is enabled.

---

#### isTouchedInsideFrame () → {Boolean}
Checks if the frame was touched.

---

#### isTouchScrollEnabled () → {Boolean}
Checks if touch scrolling is enabled.

---

#### isWheelScrollEnabled () → {Boolean}
Checks if scrolling with the wheel is enabled.

---

#### maxScrollX () → {[Number](Number.md)}
Returns the maximum scroll amount in the x direction.

---

#### maxScrollY () → {[Number](Number.md)}
Returns the maximum scroll amount in the y direction.

---

#### onTouchScroll ()
Handler for touch scrolling.

---

#### onTouchScrollEnd ()
Handler for when touch scrolling ends.

---

#### onTouchScrollStart ()
Handler for when touch scrolling starts.

---

#### overallHeight () → {[Number](Number.md)}
Returns the overall height.

---

#### overallWidth () → {[Number](Number.md)}
Returns the overall width.

---

#### paint ()
Draws the content.

---

#### processTouchScroll ()
Executes touch scrolling.

---

#### processWheelScroll ()
Executes scrolling with the wheel.

---

#### scrollBaseX () → {[Number](Number.md)}
Returns the x direction scroll base point.

---

#### scrollBaseY () → {[Number](Number.md)}
Returns the y direction scroll base point.

---

#### scrollBlockHeight () → {[Number](Number.md)}
Returns the height of the scroll unit.

---

#### scrollBlockWidth () → {[Number](Number.md)}
Returns the width of the scroll unit.

---

#### scrollTo (x, y)
Scrolls to the specified position.

##### Arguments

| Name | Type           | Description     |
|------|----------------|-----------------|
| `x`  | [Number](Number.md) | x position     |
| `y`  | [Number](Number.md) | y position     |

---

#### scrollX () → {[Number](Number.md)}
Returns the scroll amount in the x direction.

---

#### scrollY () → {[Number](Number.md)}
Returns the scroll amount in the y direction.

---

#### setScrollAccel (x, y)
Sets the acceleration.

##### Arguments

| Name | Type           | Description     |
|------|----------------|-----------------|
| `x`  | [Number](Number.md) | x acceleration  |
| `y`  | [Number](Number.md) | y acceleration  |

---

#### smoothScrollBy (x, y)
Scrolls smoothly by the specified amount.

##### Arguments

| Name | Type           | Description     |
|------|----------------|-----------------|
| `x`  | [Number](Number.md) | x movement      |
| `y`  | [Number](Number.md) | y movement      |

---

#### smoothScrollDown (n)
Scrolls down smoothly.

##### Arguments

| Name | Type           | Description     |
|------|----------------|-----------------|
| `n`  | [Number](Number.md) | Number of rows to scroll |

---

#### smoothScrollTo (x, y)
Scrolls smoothly to the specified position.

##### Arguments

| Name | Type           | Description     |
|------|----------------|-----------------|
| `x`  | [Number](Number.md) | x position      |
| `y`  | [Number](Number.md) | y position      |

---

#### smoothScrollUp (n)
Scrolls up smoothly.

##### Arguments

| Name | Type           | Description     |
|------|----------------|-----------------|
| `n`  | [Number](Number.md) | Number of rows to scroll |

---

#### update ()
Override: [Window_Base](Window_Base.md#update-)

---

#### updateArrows ()
Updates arrows indicating if there are more items above or below.

---

#### updateOrigin ()
Updates the origin point.

---

#### updateScrollAccel ()
Updates the scroll acceleration.

---

#### updateScrollBase ()
Updates the scroll base.

---

#### updateSmoothScroll ()
Updates the smooth scrolling.
