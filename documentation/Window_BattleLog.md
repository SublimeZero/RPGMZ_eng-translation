[Class Tree](index.md)

# Class: Window_BattleLog

## Superclass: [Window_Base](Window_Base.md)

A window for displaying the battle log.

Many of the methods in this window are stored in the `_methods` property by [push()](Window_BattleLog.md#push-methodname-args) and executed in sequence.

It not only displays messages but also plays a managerial role by handling actions like side-view actions.

In MV, the superclass (the parent class) was [Window_Selectable](Window_Selectable.md), but it has been changed to [Window_Base](Window_Base.md) in MZ.

---

Related classes: [Scene_Battle](Scene_Battle.md), [RPG.State](RPG.State.md), [Game_ActionResult](Game_ActionResult.md)

---

### new Window_BattleLog (rect)
#### Arguments
There were no arguments in MV.

| Name | Type | Description |
| --- | --- | --- |
| `rect` | [Rectangle](Rectangle.md) | Rectangular area (in pixels) |

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_backBitmap` | [Bitmap](Bitmap.md) | Background image |
| `_lines` | [Array](Array.md).&lt;[String](String.md)&gt; | Array of lines |
| `_methods` | [Array](Array.md).&lt;[MV.BattleLogMethod](MV.BattleLogMethod.md)&gt; | Array of methods |
| `_waitCount` | [Number](Number.md) | Wait time |
| `_waitMode` | [String](String.md) | [Wait state](Window_BattleLog.md#待機状態) |
| `_baseLineStack` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Stack of line separators |
| `_spriteset` | [Spriteset_Battle](Spriteset_Battle.md) | Battle spriteset |

#### Wait State

| Name | Description |
| --- | --- |
| "effect" | Effect |
| "movement" | Movement |

---

# Inheritance Tree

- [**Window_BattleLog**]
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

---

#### addText (text)
Adds a line.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `text` | [String](String.md) | The string of the line |

---

#### animationBaseDelay () → {[Number](Number.md)}
Returns the base delay time for animations (default: 8 frames).

---

#### animationNextDelay () → {[Number](Number.md)}
Returns the delay time until the next animation (default: 12 frames).

---

#### backColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the background color (default: "#000000").

---

#### backPaintOpacity () → {[Number](Number.md)}
Returns the opacity of the background (default: 64).

---

#### backRect () → {[Rectangle](Rectangle.md)}
Returns the rectangular area of the background.

---

#### callNextMethod ()
Calls the next method.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

---

#### clear ()
Clears the display and also clears the record of line separators.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

---

#### displayAction (subject, item)
Displays the specified action (using [skill][item]).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `item` | [RPG.UsableItem](RPG.UsableItem.md) | Usable item |

---

#### displayActionResults (subject, target)
Displays the results of the action.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayAddedStates (target)
Displays the added states.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayAffectedStatus (target)
Displays the changes in ability values.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayAutoAffectedStatus (target)
Displays the automatic changes in ability values.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayChangedBuffs (target)
Displays changes in [buffs][debuffs].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayChangedStates (target)
Displays changes in states.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayCounter (target)
Displays counterattacks.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayCritical (target)
Displays critical attacks.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayCurrentState (subject)
Displays the current state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayDamage (target)
Displays damage.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayEvasion (target)
Displays evasion.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayHpDamage (target)
Displays damage to HP.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayItemMessage (fmt, subject, item)
**@MZ** Displays the item message.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `fmt` | [String](String.md) | Format string for the message |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `item` | [RPG.UsableItem](RPG.UsableItem.md) | Usable item |

---

#### displayMiss (target)
Displays a missed attack.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayMpDamage (target)
Displays damage to MP.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayReflection (target)
Displays reflection.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayRemovedStates (target)
Displays when states are removed.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayRegeneration (subject)
Displays regeneration.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displaySubstitute (substitute, target)
Displays the [guard] action.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `substitute` | [Game_Battler](Game_Battler.md) | Substitute battler |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### displayTpDamage (target)
Displays damage to TP.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### drawBackground ()
Draws the background.

---

#### drawLineText (index)
Draws the text for the specified line.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `index` | [Number](Number.md) | Line position |

---

#### endAction (subject)
Ends the action.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### initialize (rect)
Override: [Window_Base](Window_Base.md#initialize-rect)

---

#### isBusy () → {Boolean}
Checks if busy.

---

#### isFastForward () → {Boolean}
Checks if fast-forwarding.

---

#### lineRect (index) → {[Rectangle](Rectangle.md)}
**@MZ** Returns the rectangular area for the specified line.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `index` | [Number](Number.md) | Line position |

---

#### makeHpDamageText (target)
Generates a message for damage to HP.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### makeMpDamageText (target) → {[String](String.md)}
Generates a message for damage to MP.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### makeTpDamageText (target) → {[String](String.md)}
Generates a message for damage to TP.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### maxLines () → {[Number](Number.md)}
Returns the maximum number of lines.

---

#### messageSpeed () → {[Number](Number.md)}
Returns the message speed.

---

#### numLines () → {[Number](Number.md)}
Returns the number of currently displayed lines.

---

#### performAction (subject, action)
Applies the action.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `action` | [Game_Action](Game_Action.md) | Action |

---

#### performActionEnd (subject)
Applies the end of the action.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### performActionStart (subject, action)
Applies the start of the action.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `action` | [Game_Action](Game_Action.md) | Action |

---

#### performCollapse (target)
Applies the collapse.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### performCounter (target)
Applies the counterattack.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### performDamage (target)
Applies damage.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### performEvasion (target)
Applies evasion.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### performMagicEvasion (target)
Applies magic reflection.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### performMiss (target)
Applies attack failure.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### performRecovery (target)
Applies recovery.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### performReflection (target)
Applies reflection.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### performSubstitute (target)
Applies the [guard] action.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### popBaseLine ()
Returns to the recorded separator line count.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

---

#### popupDamage (target)
Displays damage.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

---

#### push (methodName, args)
Reserves the behavior of the log.<br />
The contents of the arguments are the same as [MV.BattleLogMethod](MV.BattleLogMethod.md).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `methodName` | [String](String.md) | Name of the method to be called |
| `args` | [Array](Array.md).&lt;*&gt; | Arguments vary by method |

---

#### pushBaseLine ()
Records the number of separator lines.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

---

#### refresh ()
Redraws the display.

---

#### setSpriteset (spriteset)
Sets the sprite set.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `spriteset` | [Spriteset_Battle](Spriteset_Battle.md) | Sprite set |

---

#### setWaitMode (waitMode)
Sets the wait mode.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `waitMode` | [String](String.md) | Wait mode ("effect", "movement") |

---

#### showActorAttackAnimation (subject, targets)
Displays the actor's attack animation.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `targets` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | Array of target battlers |

---

#### showAttackAnimation (subject, targets)
Displays the attack animation.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `targets` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | Array of target battlers |

---

#### showAnimation (subject, targets, animationId)
Displays the animation.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `targets` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | Array of target battlers |
| `animationId` | [Number](Number.md) | Animation ID |

---

#### showEnemyAttackAnimation (subject, targets)
Displays the enemy's attack animation.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `targets` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | Array of target battlers |

---

#### showNormalAnimation (targets, animationId, mirror)
Displays the normal animation.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `targets` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | Array of target battlers |
| `animationId` | [Number](Number.md) | Animation ID |
| `mirror` | Boolean | Whether to mirror horizontally |

---

#### startAction (subject, action, targets)
Starts the action.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `action` | [Game_Action](Game_Action.md) | Action |
| `targets` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | Array of target battlers |

---

#### startTurn ()
Starts the turn.

---

#### update ()
Override: [Window_Base](Window_Base.md#update-)

---

#### updateWait () → {Boolean}
Updates the wait time.

---

#### updateWaitCount () → {Boolean}
Updates the wait count.

---

#### updateWaitMode () → {Boolean}
Updates the wait mode.

---

#### wait ()
Waits.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

---

#### waitForEffect ()
Waits for the effect.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

---

#### waitForMovement ()
Waits for movement.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

---

#### waitForNewLine ()
Waits for a new line.<br />
Reference: [MV.BattleLogMethod](MV.BattleLogMethod.md)

---

### Deprecated MV Methods
createBackBitmap (), createBackSprite (), windowHeight (), windowWidth ()
