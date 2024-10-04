------------------------------------------------------------

[Class Tree](index.md)

# Class: Window

## Superclass: [PIXI.Container](PIXI.Container.md)

A window used in the game. Not a window from a browser or other applications.<br />
Typically included in [WindowLayer](WindowLayer.md), it contains images in the following way. They are arranged in order of layering, with the pause sign being the closest to the screen and the window background being the furthest back.

* `_pauseSignSprite` Pause sign
* `_upArrowSprite` Upward arrow
* `_downArrowSprite` Downward arrow
* `_clientArea` Client area
    * `_contentsSprite` Content
        * `contents` (`_contentsSprite.bitmap`)
    * `_cursorSprite` Command selection cursor
        * `_cursorSprite.children` ([Sprite](Sprite.md) × 9) Parts that make up the cursor frame, composed of 9 slices
    * `_contentsBackSprite` Item background
        * `contentsBack` (`_contentsBackSprite.bitmap`)
* `_container` Window
    * `_frameSprite` Window frame
        * `_frameSprite.children` ([Sprite](Sprite.md) × 8) Parts that make up the window frame, composed of 9 slices
    * `_backSprite` Window background
        * `_backSprite.children` ([TilingSprite](TilingSprite.md) × 1) For repeating patterns

By rewriting `contents`, you can change the displayed content such as messages and icons.<br />
While it shares almost the same elements as 'RPG Maker MV', the structure has changed significantly.

`contentsBack` was added in MZ and is the background displayed behind commands and status items shown in the window.

The opacity-related properties only read and write the alpha property of the target sprite.

Changes were made in v1.2.0 and v1.3.0.

Related classes: [Graphics](Graphics.md), [Scene_Base](Scene_Base.md)

### new Window ()

### Subclasses

* [Window_Base](Window_Base.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `active` | Boolean | Is the window active? |
| `openness` | [Number](Number.md) | Openness of `_container` (0 - 255) |
| `contents` | [Bitmap](Bitmap.md) | Image of content (`_contentsSprite`) |
| `contentsBack` | [Bitmap](Bitmap.md) | **@MZ** Background of items (`_contentsBackSprite`) |
| `windowskin` | [Bitmap](Bitmap.md) | Window skin image (img/system/Window.png) |
| `pause` | Boolean | Is the pause sign displayed? |
| `downArrowVisible` | Boolean | Is the downward scroll arrow visible? |
| `upArrowVisible` | Boolean | Is the upward scroll arrow visible? |
| `opacity` | [Number](Number.md) | Opacity of the window (`_container`) (0 - 255) |
| `backOpacity` | [Number](Number.md) | Opacity of the window background (`_backSprite`) (0 - 255) (default: 192) |
| `contentsOpacity` | [Number](Number.md) | Opacity of content (`_contentsSprite`) (0 - 255) |
| `origin` | [Point](Point.md) | Origin of the window during scrolling |
| `margin` | [Number](Number.md) | Width from the window edge to the background (default: 4 pixels) |
| `padding` | [Number](Number.md) | Width from the window edge to the content (default: 12 pixels) |
| `width` | [Number](Number.md) | Width (pixels) |
| `height` | [Number](Number.md) | Height (pixels) |
| `innerWidth` | [Number](Number.md) | **@MZ** [read-only] Width of the client area (width - padding * 2) |
| `innerHeight` | [Number](Number.md) | **@MZ** [read-only] Height of the client area (height - padding * 2) |
| `innerRect` | [Rectangle](Rectangle.md) | **@MZ** [read-only] Rectangular range of the client area |
| `_isWindow` | Boolean | Is it a window? |
| `_windowskin` | [Bitmap](Bitmap.md) |  |
| `_width` | [Number](Number.md) |  |
| `_height` | [Number](Number.md) |  |
| `_innerChildren` | [Array](Array.md).&lt;Object&gt; | **@MZ** Array of child objects in the client area |
| `_cursorRect` | [Rectangle](Rectangle.md) | Rectangular range of the item selection cursor |
| `_openness` | [Number](Number.md) |  |
| `_animationCount` | [Number](Number.md) | Animation count |
| `_padding` | [Number](Number.md) |  |
| `_margin` | [Number](Number.md) |  |
| `_colorTone` | [MV.Tone](MV.Tone.md) | [Color tone] |
| `_container` | [PIXI.Container](http://pixijs.download/v5.3.12/docs/PIXI.Container.html) | **@MZ** Window image container |
| `_backSprite` | [Sprite](Sprite.md) | **@MZ** Window background |
| `_cursorSprite` | [Sprite](Sprite.md) | **@MZ** Command selection cursor |
| `_frameSprite` | [Sprite](Sprite.md) | **@MZ** Window frame |
| `_clientArea` | [PIXI.Container](http://pixijs.download/v5.3.12/docs/PIXI.Container.html) | **@MZ** Content (including `contents`) |
| `_contentsBackSprite` | [Sprite](Sprite.md) | **@MZ** Item background |
| `_contentsSprite` | [Sprite](Sprite.md) | **@MZ** Content |
| `_pauseSignSprite` | [Sprite](Sprite.md) | **@MZ** Pause sign |
| `_downArrowSprite` | [Sprite](Sprite.md) | Downward arrow |
| `_upArrowSprite` | [Sprite](Sprite.md) | Upward arrow |

### Deprecated MV Properties
In MZ, similar properties have been adopted in a way that omits "window".

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

---

### Methods

---

####  _createAllParts ()
Generates the parts necessary for displaying the window.

---

####  _createArrowSprites ()
**@MZ** Generates the arrows (_downArrowSprite, _upArrowSprite).

---

####  _createBackSprite ()
**@MZ** Generates the window background (_backSprite).

---

####  _createContainer ()
**@MZ** Generates the window container (_container).

---

####  _createClientArea ()
**@MZ** Generates the client area (_clientArea).

---

####  _createContentsSprite ()
**@MZ** Generates the content (_contentsSprite).

---

####  _createContentsBackSprite ()
**@MZ** Generates the background of the items (_contentsBackSprite).

---

####  _createCursorSprite ()
**@MZ** Generates the cursor (_cursorSprite).

---

####  _createFrameSprite ()
**@MZ** Generates the window frame (_frameSprite).

---

####  _createPauseSignSprites ()
**@MZ** Generates the pause sign (_pauseSignSprite).

---

####  _makeCursorAlpha () → {Number}
**@MZ** Changes the opacity of the cursor according to the animation count and returns the base opacity (0 - 1).

---

####  _onWindowskinLoad ()
Handler when the skin is downloaded.

---

####  _refreshAllParts ()
Redraws the parts.

---

####  _refreshArrows ()
Redraws the arrows.

---

####  _refreshBack ()
Redraws the background.

---

####  _refreshCursor ()
Redraws the cursor.

---

####  _refreshFrame ()
Redraws the frame.

---

####  _refreshPauseSign ()
Redraws the pause sign.

---

####  _setRectPartsGeometry (sprite, srect, drect, m)
**@MZ** Sets the border for the specified sprite.  
`sprite` must be an object that has 8 [Sprite](Sprite.md) objects prepared in `children`.  
Specifically, either the `_cursorSprite` or `_frameSprite` property must be specified.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sprite` | [Sprite](Sprite.md)  | Sprite for the 9-slice border |
| `srect` | [MV.Rectangle](MV.Rectangle.md) | Rectangle area to cut from the skin image |
| `drect` | [MV.Rectangle](MV.Rectangle.md) | Rectangle area to place |
| `m` | [Number](Number.md) | Width of the border image (in pixels) |

---

####  _updateArrows ()
Updates the arrows.

---

####  _updateClientArea ()
**@MZ** Updates the client area.

---

####  _updateContents ()
Updates the content.

---

####  _updateContentsBack ()
**@MZ** Updates the background of the items.

---

####  _updateCursor ()
Updates the cursor.

---

####  _updateFilterArea ()
**@MZ** Updates the filter for the client area.

---

####  _updateFrame ()
**@MZ** Updates the window frame.

---

####  _updatePauseSign ()
Updates the pause sign.

---

#### addChildToBack (child) → {Object}
Adds a child object between the window (_container) and the client area, returning the added object.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `child` | [PIXI.DisplayObject](PIXI.DisplayObject.md)  | Object to add |

---

#### addInnerChild (child) → {Object}
**@MZ** Adds a child object to the client area and returns the added object.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `child` | [PIXI.DisplayObject](PIXI.DisplayObject.md)  | Object to add |

---

#### destroy ()
**@MZ** Override: [PIXI.Container](PIXI.Container.md#destroy-)

---

#### drawShape (graphics)
**@MZ** Fills the specified graphic with a white rectangle of the window's size.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `graphics` | [PIXI.Graphics](PIXI.Graphics.md)  | Object to draw |

---

#### initialize ()
Initialization during object creation.

---

#### isClosed () → {Boolean}
Checks if the window is completely closed.  
In other words, if openness === 0.

---

#### isOpen () → {Boolean}
Checks if the window is completely open.  
In other words, if openness === 255.

---

#### move (x, y, width opt, height opt)
Changes the window to the specified position and size.

##### Arguments

| Name | Type | Characteristics | Default | Description |
| --- | --- | --- | --- | --- |
| `x` | [Number](Number.md) |  |  | Window x-coordinate (in pixels) |
| `y` | [Number](Number.md) |  |  | Window y-coordinate (in pixels) |
| `width` | [Number](Number.md) | &lt;optional&gt; | 0 | Window width (in pixels) |
| `height` | [Number](Number.md) | &lt;optional&gt; | 0 | Window height (in pixels) |

---

#### moveCursorBy (x, y)
**@MZ** Moves the cursor by the specified distance.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Cursor x movement distance (in pixels) |
| `y` | [Number](Number.md) | Cursor y movement distance (in pixels) |

---

#### moveInnerChildrenBy (x, y)
**@MZ** Moves all child objects of the client area by the specified distance.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Child object x movement distance (in pixels) |
| `y` | [Number](Number.md) | Child object y movement distance (in pixels) |

---

#### setCursorRect (x, y, width, height)
Sets the position and size of the command cursor.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Cursor x-coordinate (in pixels) |
| `y` | [Number](Number.md) | Cursor y-coordinate (in pixels) |
| `width` | [Number](Number.md) | Cursor width (in pixels) |
| `height` | [Number](Number.md) | Cursor height (in pixels) |

---

#### setTone (r, g, b)
Sets the color tone of the background.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `r` | [Number](Number.md) | Red (-255 to 255) |
| `g` | [Number](Number.md) | Green (-255 to 255) |
| `b` | [Number](Number.md) | Blue (-255 to 255) |

---

#### update ()
Updates every frame.

---

#### updateTransform ()
Override: [PIXI.Container](PIXI.Container.md#updatetransform-)

---

### MV Deprecated Methods
_refreshContents ()


`_windowPauseSignSprite`, `_windowCursorSprite`, `_windowSpriteContainer`, `_windowFrameSprite`, `_windowContentsSprite`, `_windowBackSprite`, `_arrowSprites`

### Methods Inherited from Superclass
