# Class: Sprite_Gauge

## Superclass: [Sprite](Sprite.md)

**@MZ** A sprite for displaying gauges. Composed of labels, gauges, and values.

It is added to the `_clientArea` held by the [Window](Window.md) class and managed by the `_additionalSprites` property in the [Window_StatusBase](Window_StatusBase.md) class.

Changes were made in v1.1.0, v1.2.0, v1.3.3, and v1.4.0.

Related Classes: [Window_StatusBase](Window_StatusBase.md)

### new Sprite_Gauge ()

### Properties

| Identifier      | Type                     | Description  |
|-----------------|--------------------------|--------------|
| `_battler`      | [Game_Battler](Game_Battler.md) | Battler      |
| `_statusType`   | [String](String.md)      | [Type of status](#ステータスの種類) |
| `_value`        | [Number](Number.md)      | Current value |
| `_maxValue`     | [Number](Number.md)      | Maximum value |
| `_targetValue`  | [Number](Number.md)      | Target value  |
| `_targetMaxValue`| [Number](Number.md)     | Target maximum value |
| `_duration`     | [Number](Number.md)      | Delay time    |
| `_flashingCount`| [Number](Number.md)      | Count         |

#### Types of Status

| String | Label | Description    |
|--------|-------|----------------|
| "hp"   | [HP (abbreviation)] | Value of HP   |
| "mp"   | [MP (abbreviation)] | Value of MP   |
| "tp"   | [TP (abbreviation)] | Value of TP   |
| "time" | None  | Elapsed time in TPB |

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
* [_renderCanvas (renderer)](PIXI.Container.md#_rendercanvas-renderer)
* [setChildIndex (child, index)](PIXI.Container.md#setchildindex-child-index)
* [sortChildren ()](PIXI.Container.md#sortchildren-)
* [swapChildren (child, child2)](PIXI.Container.md#swapchildren-child-child2)
* [updateTransform ()](PIXI.Container.md#updatetransform-)

#### [PIXI.Sprite](PIXI.Sprite.md)

* [(static) from (source, options)](PIXI.Sprite.md#static-from-source-options--pixisprite)
* [\_calculateBounds ()](PIXI.Sprite.md#_calculatebounds-)
* [\_render (renderer)](PIXI.Sprite.md#_render-renderer)
* [calculateTrimmedVertices ()](PIXI.Sprite.md#calculatetrimmedvertices-)
* [calculateVertices ()](PIXI.Sprite.md#calculatevertices-)
* [containsPoint (point)](PIXI.Sprite.md#containspoint-point--boolean)
* [getLocalBounds (rect)](PIXI.Sprite.md#getlocalbounds-rect--pixirectangle)
* [renderCanvas (renderer)](PIXI.Sprite.md#rendercanvas-renderer)

#### [Sprite](Sprite.md)

* [getBlendColor ()](Sprite.md#getblendcolor---mvcolor)
* [getColorTone ()](Sprite.md#getcolortone---mvcolor)
* [hide ()](Sprite.md#hide-)
* [move (x, y)](Sprite.md#Sprite.md#move-x-y)
* [setBlendColor (color)](Sprite.md#setblendcolor-color)
* [setColorTone (tone)](Sprite.md#setcolortone-tone)
* [setFrame (x, y, width, height)](Sprite.md#setframe-x-y-width-height)
* [setHue (hue)](Sprite.md#sethue-hue)
* [show ()](Sprite.md#show-)
* [updateVisibility ()](Sprite.md#updatevisibility-)

---

### Methods

#### bitmapHeight () → {[Number](Number.md)}
Returns the height of the image display area (default: 32 pixels).<br />
**@MZ 1.3.2** Until then, the default was: 24 pixels.

---

#### bitmapWidth () → {[Number](Number.md)}
Returns the width of the image display area (default: 128 pixels).

---

#### createBitmap ()
Generates the image display area.

---

#### currentMaxValue () → {[Number](Number.md)}
Returns the current maximum value.

---

#### currentValue () → {[Number](Number.md)}
Returns the current value.

---

#### destroy ()
Override: [Sprite](Sprite.md#destroy-)

---

#### drawLabel ()
Draws the label.

---

#### drawGauge ()
Draws the gauge.

---

#### drawValue ()
Draws the value.

---

#### drawGaugeRect (x, y, width, height)
Draws the gauge bar.

##### Arguments

| Name   | Type                     | Description         |
|--------|--------------------------|---------------------|
| `x`    | [Number](Number.md)      | x-coordinate (pixels) |
| `y`    | [Number](Number.md)      | y-coordinate (pixels) |
| `width`| [Number](Number.md)      | Width (pixels)      |
| `height`| [Number](Number.md)     | Height (pixels)     |

---

#### flashingColor1 () → {[MV.Color](MV.Color.md)}
Returns the color 1 for flashing (default: [255, 255, 255, 64]).

---

#### flashingColor2 () → {[MV.Color](MV.Color.md)}
Returns the color 2 for flashing (default: [0, 0, 255, 48]).

---

#### gaugeBackColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the color of the gauge's background.

---

#### gaugeColor1 () → {[MV.CssColor](MV.CssColor.md)}
Returns gauge color 1.

---

#### gaugeColor2 () → {[MV.CssColor](MV.CssColor.md)}
Returns gauge color 2.

---

#### gaugeHeight () → {[Number](Number.md)}
Returns the height of the gauge (default: 12 pixels).

---

#### gaugeRate () → {[Number](Number.md)}
Returns the gauge ratio (current value / maximum value).

---

#### gaugeX () → {[Number](Number.md)}
Returns the x-coordinate of the gauge (time: 0, otherwise: 30).

---

#### initialize ()
Override: [Sprite](Sprite.md#initialize-)

---

#### initMembers ()
Initializes properties.

---

#### isValid () → {Boolean}
Checks if the gauge settings are appropriate.

---

#### label () → {[String](String.md)}
Returns the label name.

---

#### labelColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the label's color.

---

#### labelFontFace () → {[String](String.md)}
Returns the font name for the label.

---

#### labelFontSize () → {[Number](Number.md)}
Returns the font size for the label.

---

#### labelOpacity () → {[Number](Number.md)}
Returns the opacity of the label (changes based on the state of [isValid()](#isValid---boolean)).

---

#### labelOutlineColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the outline color of the label.

---

#### labelOutlineWidth () → {[Number](Number.md)}
Returns the outline width of the label (default: 3).

---

#### labelY () → {[Number](Number.md)}
Returns the y-coordinate of the label (default: 3).

---

#### measureLabelWidth () → {[Number](Number.md)}
**@MZ1.2.0** Returns the width of the label.

---

#### redraw ()
Redraws the gauge.

---

#### setup (battler, statusType)
Sets up the gauge.

##### Arguments

| Name        | Type                     | Description         |
|-------------|--------------------------|---------------------|
| `battler`   | [Game_Battler](Game_Battler.md) | Battler             |
| `statusType`| [String](String.md)      | [Type of status](#ステータスの種類) |

---

#### setupLabelFont ()
Prepares the label font.

---

#### setupValueFont ()
Prepares the value font.

---

#### smoothness () → {[Number](Number.md)}
Returns the animation interval for the gauge.

---

#### textHeight () → {[Number](Number.md)}
**@MZ 1.3.3** Returns the height of the text (default: 24 pixels).

---

#### update ()
Override: [Sprite](Sprite.md#update-)

---

#### updateBitmap ()
Updates the image display area.

---

#### updateFlashing ()
Updates the flashing.

---

#### updateGaugeAnimation ()
Updates the gauge animation.

---

#### updateTargetValue (value, maxValue)
Updates the target value.

##### Arguments

| Name   | Type                     | Description         |
|--------|--------------------------|---------------------|
| `value`| [Number](Number.md)      | Current value       |
| `maxValue`| [Number](Number.md)   | Maximum value       |

---

#### valueColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the color of the value.

---

#### valueFontFace () → {[String](String.md)}
Returns the font name for the value.

---

#### valueFontSize () → {[Number](Number.md)}
Returns the font size for the value.

---

#### valueOutlineColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the outline color of the value (default: "rgba(0, 0, 0, 1)").

---

#### valueOutlineWidth () → {[Number](Number.md)}
Returns the outline width of the value (default: 2).
