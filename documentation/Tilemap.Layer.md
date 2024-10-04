[Class Tree](index.md)

# Class: [Tilemap](Tilemap.md).Layer

## Superclass: [PIXI.Container](PIXI.Container.md)

A class that displays the lower layer (collision detection ○・×) and upper layer (collision detection ☆) of tiles used in the map. 
Starting from version 1.7.0, it has been incorporated into [Tilemap.CombinedLayer](Tilemap.CombinedLayer.md).

---

Main Path
```js
SceneManager._scene._spriteset._tilemap._upperLayer
SceneManager._scene._spriteset._tilemap._lowerLayer
```

---

Starting from version 1.7.0
```js
SceneManager._scene._spriteset._tilemap._upperLayer.childlen[n]
SceneManager._scene._spriteset._tilemap._lowerLayer.childlen[n]
```

---

Related Classes: [RPG.Map](RPG.Map.md), [RPG.Tileset](RPG.Tileset.md), [Game_Map](Game_Map.md), [Spriteset_Map](Spriteset_Map.md),
[Tilemap.Renderer](Tilemap.Renderer.md)

### new Tilemap.Layer ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `MAX_GL_TEXTURES` | [Number](Number.md) | [static] Maximum textures (default: 3) |
| `VERTEX_STRIDE` | [Number](Number.md) | [static] Vertex stride (default: 36) |
| `MAX_SIZE` | [Number](Number.md) | **@MZ1.7.0** [static] Maximum number of elements (default: 16000) |
| `_elements` | [Array](Array.md).&lt;[MV.TileRect](MV.TileRect.md)&gt;  | Array of rectangle data used for tile rendering |
| `_images` | [Array](Array.md).&lt;[HTMLImageElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement)&gt;  | Array of image data |
| `_vao` | [PIXI.Geometry](http://pixijs.download/v5.3.12/docs/PIXI.Geometry.html) | Geometry |
| `_indexArray` | Float32Array | Array of indices |
| `_indexBuffer` | [PIXI.Buffer](http://pixijs.download/v5.3.12/docs/PIXI.Buffer.html) | Index buffer |
| `_vertexArray` | Float32Array | One-dimensional array of `_elements` |
| `_vertexBuffer` | [PIXI.Buffer](http://pixijs.download/v5.3.12/docs/PIXI.Buffer.html) | Vertex buffer |
| `_needsTexturesUpdate` | Boolean | Whether texture update is needed |
| `_needsVertexUpdate` | Boolean | Whether vertex update is needed |
| `_state` | [PIXI.State](http://pixijs.download/v5.3.12/docs/PIXI.State.html) | State |
| `z` | [Number](Number.md) | z-index ((Reference: [Layer Arrangement](Tilemap.md#layer-arrangement)))|

### Methods Inherited from Superclass

#### [PIXI.DisplayObject](PIXI.DisplayObject.md)

* [(static) mixin (source)](PIXI.DisplayObject.md#static-mixin-source)
* [\_recursivePostUpdateTransform ()](PIXI.DisplayObject.md#_recursivepostupdatetransform-)
* [displayObjectUpdateTransform ()](PIXI.DisplayObject.md#displayobjectupdatetransform-)
* [getBounds (skipUpdate, rect)](PIXI.DisplayObject.md#getbounds-skipupdate-rect--pixirectangle)
* [getGlobalPosition (point, skipUpdate)](PIXI.DisplayObject.md#getglobalposition-point-skipupdate--pixipoint)
* [getLocalBounds (rect)](PIXI.DisplayObject.md#getlocalbounds-rect--pixirectangle)
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
* [renderAdvanced (renderer)](PIXI.Container.md#renderadvanced-renderer)
* [renderCanvas (renderer)](PIXI.Container.md#rendercanvas-renderer)
* [setChildIndex (child, index)](PIXI.Container.md#setchildindex-child-index)
* [sortChildren ()](PIXI.Container.md#sortchildren-)
* [swapChildren (child, child2)](PIXI.Container.md#swapchildren-child-child2)

---

### Methods

---

### _createVao ()
Generates the VAO.

---

### _updateIndexBuffer ()
Updates the index buffer.

---

### _updateVertexBuffer ()
Updates the vertex buffer.

---

#### addRect (setNumber, sx, sy, dx, dy, w, h)
Sets the rectangular (tile) range in the tileset. (Reference: [MV.TileRect](MV.TileRect.md))

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `setNumber` | [Number](Number.md) | Tileset section number (0–8)<br />A1:0, A2:1, A3:2, A4:3, A5:4, B:5, C:6, D:7, E:8 |
| `sx` | [Number](Number.md) | x position in the tileset image (pixels) |
| `sy` | [Number](Number.md) | y position in the tileset image (pixels) |
| `dx` | [Number](Number.md) | x coordinate in the layer (pixels) |
| `dy` | [Number](Number.md) | y coordinate in the layer (pixels) |
| `w` | [Number](Number.md) | width of the tile (pixels) |
| `h` | [Number](Number.md) | height of the tile (pixels) |

---

#### destroy ()
Override: [PIXI.Container](PIXI.Container.md#destroy-)

---

#### initialize ()
Override: [PIXI.Container](PIXI.Container.md#initialize-)

---

#### isReady () → {Boolean}
Checks if it is ready.

---

#### render (renderer)
Override: [PIXI.Container](PIXI.Container.md#render-renderer)

---

#### setBitmaps (bitmaps)
Sets the tileset image.

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `bitmaps` | [Array](Array.md).&lt;[Bitmap](Bitmap.md)&gt; | Array of bitmaps for the tileset |

---

#### size ()→ {[Number](Number.md)}
**@MZ1.7.0** Returns the number of elements contained (`_elements`).

---

#### clear ()
Clears the images.
