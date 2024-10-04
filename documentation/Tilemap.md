[Class Tree](index.md)

# Class: [Tilemap](Tilemap.md).CombinedLayer

## Superclass: [PIXI.Container](PIXI.Container.md)

Introduced in version 1.7.0, this class displays the lower layer (passability ○・×) and upper layer (passability ☆) of tiles handled in the map. 
Contains [Tilemap.Layer](Tilemap.Layer.md) in the `children` property.

Main Path
```js
SceneManager._scene._spriteset._tilemap._upperLayer
SceneManager._scene._spriteset._tilemap._lowerLayer
```

Related Classes: [RPG.Map](RPG.Map.md), [RPG.Tileset](RPG.Tileset.md), [Game_Map](Game_Map.md), [Spriteset_Map](Spriteset_Map.md),
[Tilemap.Renderer](Tilemap.Renderer.md)

### new Tilemap.CombinedLayer ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `children` | [Array](Array.md).&lt;[Tilemap.Layer](Tilemap.Layer.md)&gt; | Layers |


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

#### addRect (setNumber, sx, sy, dx, dy, w, h)
Sets a rectangular (tile) area in the tileset. (Reference: [MV.TileRect](MV.TileRect.md))

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `setNumber` | [Number](Number.md) | The section number of the tileset (0-8)<br />A1:0, A2:1, A3:2, A4:3, A5:4, B:5, C:6, D:7, E:8 |
| `sx` | [Number](Number.md) | X position of the tileset image (pixels) |
| `sy` | [Number](Number.md) | Y position of the tileset image (pixels) |
| `dx` | [Number](Number.md) | X coordinate within the layer (pixels) |
| `dy` | [Number](Number.md) | Y coordinate within the layer (pixels) |
| `w` | [Number](Number.md) | Width of the tile (pixels) |
| `h` | [Number](Number.md) | Height of the tile (pixels) |

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

#### setBitmaps (bitmaps)
Sets the tileset images.

##### Arguments:

| Identifier | Type | Description |
| --- | --- | --- |
| `bitmaps` | [Array](Array.md).&lt;[Bitmap](Bitmap.md)&gt; | An array of bitmaps for the tileset |

---

#### size () → {[Number](Number.md)}
Returns the number of elements with content (`children`).

---

#### clear ()
Clears the images.
