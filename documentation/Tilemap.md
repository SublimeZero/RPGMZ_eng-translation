[Class Tree](index.md)

# Class: Tilemap

## Superclass: [PIXI.Container](PIXI.Container.md)

A container class for displaying 2D-based tile maps. <br />
It is also used to manage effect-related sprites, such as speech bubbles.

It is also a utility class with many static methods.

With the introduction of the new inner class [Tilemap.Layer](Tilemap.Layer.md) in MZ, the draw-related methods have been rewritten to add-related methods. <br />
In version 1.5.0, significant changes were made due to the addition of tile size adjustment functionality. Special attention is required for `tileWidth` and `tileHeight`.

Main Path
```js
SceneManager._scene._spriteset._tilemap
SceneManager._scene._spriteset._effectsContainer
```

Changes were made in v1.5.0 and v1.7.0.

Related classes: [RPG.Map](RPG.Map.md), [RPG.Tileset](RPG.Tileset.md), [Game_Map](Game_Map.md), [Spriteset_Map](Spriteset_Map.md)

### new Tilemap ()

### Inner Classes

* [Tilemap.Layer](Tilemap.Layer.md) **@MZ**
* [Tilemap.Renderer](Tilemap.Renderer.md) **@MZ**
* [Tilemap.CombinedLayer](Tilemap.CombinedLayer.md) **@MZ1.7.0**

### Subclasses
In "RPG Maker MV," the rendering modes were separate, so the following WebGL class existed, but in "RPG Maker MZ," it has been consolidated to WebGL and is now deprecated.

* `ShaderTilemap` (deprecated)

### Properties
Constants starting with TILE_ represent the starting number for the tile block [Tile ID](#タイルID).

| Identifier | Type | Description |
| --- | --- | --- |
| `TILE_ID_A1` | [Number](Number.md) | [static] Starting number for A1 (animation) tile ID (2048) |
| `TILE_ID_A2` | [Number](Number.md) | [static] Starting number for A2 (ground) tile ID (2816) |
| `TILE_ID_A3` | [Number](Number.md) | [static] Starting number for A3 (building) tile ID (4352) |
| `TILE_ID_A4` | [Number](Number.md) | [static] Starting number for A4 (wall) tile ID (5888) |
| `TILE_ID_A5` | [Number](Number.md) | [static] Starting number for A5 (normal) tile ID (1536) |
| `TILE_ID_B` | [Number](Number.md) | [static] Starting number for B tile ID (0) |
| `TILE_ID_C` | [Number](Number.md) | [static] Starting number for C tile ID (256) |
| `TILE_ID_D` | [Number](Number.md) | [static] Starting number for D tile ID (512) |
| `TILE_ID_E` | [Number](Number.md) | [static] Starting number for E tile ID (768) |
| `TILE_ID_MAX` | [Number](Number.md) | [static] Ending number for tile ID (8192) |
| `FLOOR_AUTOTILE_TABLE` | [Array](Array.md).&lt;[Array](Array.md).&lt;[Array](Array.md).&lt;[Number](Number.md)&gt;&gt;&gt; | [static] Floor autotile assembly table |
| `WALL_AUTOTILE_TABLE` | [Array](Array.md).&lt;[Array](Array.md).&lt;[Array](Array.md).&lt;[Number](Number.md)&gt;&gt;&gt; | [static] Wall autotile assembly table |
| `WATERFALL_AUTOTILE_TABLE` | [Array](Array.md).&lt;[Array](Array.md).&lt;[Array](Array.md).&lt;[Number](Number.md)&gt;&gt;&gt; | [static] Waterfall autotile assembly table |
| `parent` | Object | [read-only][super] Parent object (the [Spriteset_Map](Spriteset_Map.md) that holds the tile map) |
| `children` | [Array](Array.md).&lt;[Sprite](Sprite.md)&gt; | [read-only][super] Array of child objects (including [Sprite](Sprite.md), [Sprite_Character](Sprite_Character.md), [Sprite_Destination](Sprite_Destination.md)) |
| `animationCount` | [Number](Number.md) | Count of autotile animations |
| `animationFrame` | [Number](Number.md) | Value where 30 animationCount = 1 |
| `bitmaps` | [Array](Array.md).&lt;[Bitmap](Bitmap.md)&gt; | Array of tile set images (0–8)<br />(0:A1, 1:A2, 2:A3, 3:A4, 4:A5, 5:B, 6:C, 7:D, 8:E) |
| `origin` | [Point](Point.md) | Reference point for scrolling |
| `flags` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Flags (see: [RPG.Tileset](RPG.Tileset.md)) |
| `tileWidth` | [Number](Number.md) | **@MZ1.5.0** Tile width (default: 48 pixels) |
| `tileHeight` | [Number](Number.md) | **@MZ1.5.0** Tile height (default: 48 pixels) |
| `width` | [Number](Number.md) | Screen width (default: 624 pixels) (see: [Graphics.width](Graphics.md)) |
| `height` | [Number](Number.md) | Screen height (default: 816 pixels) (see: [Graphics.height](Graphics.md)) |
| `horizontalWrap` | Boolean | Should it loop horizontally? |
| `verticalWrap` | Boolean | Should it loop vertically? |
| `_tileWidth` | [Number](Number.md) | **@MZ1.5.0** Deprecated |
| `_tileHeight` | [Number](Number.md) | **@MZ1.5.0** Deprecated |
| `_width` | [Number](Number.md) | |
| `_height` | [Number](Number.md) | |
| `_margin` | [Number](Number.md) | Margin (default: 20) |
| `_mapWidth` | [Number](Number.md) | Map width (in tiles) |
| `_mapHeight` | [Number](Number.md) | Map height (in tiles) |
| `_mapData` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Map data as a one-dimensional array (see: [RPG.Map.data](RPG.Map.md#マップデータ)) |
| `_bitmaps` | [Array](Array.md).&lt;[Bitmap](Bitmap.md)&gt; | Array of tile set images |
| `_upperLayer` | [Tilemap.CombinedLayer](Tilemap.CombinedLayer.md) | Upper [☆] tiles (z = 4) **@MZ1.6.0** was [Tilemap.Layer](Tilemap.Layer.md) |
| `_lowerLayer` | [Tilemap.CombinedLayer](Tilemap.CombinedLayer.md) | Lower layer (z = 0) **@MZ1.6.0** was [Tilemap.Layer](Tilemap.Layer.md) |
| `_lastStartX` | [Number](Number.md) | Last starting x coordinate |
| `_lastStartY` | [Number](Number.md) | Last starting y coordinate |
| `_lastAnimationFrame` | [Number](Number.md) | Last animation frame position |
| `_needsRepaint` | Boolean | Is a repaint needed? |

---

#### Layer Placement
Types and positions of layers included in children.<br />
The [layer] specified in the editor is drawn on 0: lower layer tiles.<br />
If the passage setting is [☆], it is 4: upper [☆] tiles.

| z Number | Type | Description |
| --- | --- | --- |
| 9 | [Sprite_Destination](Sprite_Destination.md) | Touch position display |
| 8 | [Sprite_Animation](Sprite_Animation.md) | Animation |
| 7 | [Sprite_Balloon](Sprite_Balloon.md) | Speech balloon |
| 6 | [Sprite_Character](Sprite_Character.md) | Airship shadow |
| 5 | [Sprite_Character](Sprite_Character.md) | Upper layer character (for overpasses) |
| 4 | [Tileset.Layer](Tileset.Layer.md) | Upper [☆] tiles |
| 3 | [Sprite_Character](Sprite_Character.md) | Normal character |
| 2 |  | Unused |
| 1 | [Sprite_Character](Sprite_Character.md) | Lower layer character |
| 0 | [Tileset.Layer](Tileset.Layer.md) | Lower layer tiles |

#### Tile ID
Values representing the type of tile.<br />
Using various isXXX() methods like isAutotile(), the type can be determined based on the assignments in the table below.

| Set | Description |
| --- | --- |
| A1 | Sea: 0, Deep Sea: 1, Shallow Water Obstacle: 2,3, Water Surface: 4,6,8,10,12,14, Waterfall: 5,7,9,11,13,15 |
| A2 | Ground: 16–19, 24–27, 32–35, 40–43, Stacked Placement: 20–23, 28–31, 36–39, 44–47 |
| A3 | Roof: 48–55, 64–71, Wall: 56–63, 72–79 |
| A4 | Above Wall: 80–87, 96–103, 112–119, Wall: 88–95, 104–111, 120–127 |

### Deprecated MV Properties
`upperZLayer`, `lowerZLayer`, `_upperBitmap`, `_lowerBitmap`, `_layerWidth`, `_layerHeight`, `_lastTiles`

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
* [render (renderer)](PIXI.Container.md#render-renderer)
* [renderAdvanced (renderer)](PIXI.Container.md#renderadvanced-renderer)
* [renderCanvas (renderer)](PIXI.Container.md#rendercanvas-renderer)
* [setChildIndex (child, index)](PIXI.Container.md#setchildindex-child-index)
* [sortChildren ()](PIXI.Container.md#sortchildren-)
* [swapChildren (child, child2)](PIXI.Container.md#swapchildren-child-child2)

---

### Methods

---

#### (static) getAutotileKind (tileId) → {[Number](Number.md)}
Returns the kind of autotile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) getAutotileShape (tileId) → {[Number](Number.md)}
Returns the shape of the autotile.
Values for ground, floor, and wall top: 0–47, roof and wall: 0–15, waterfall: 0–3.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isAutotile (tileId) → {Boolean}
Checks if it is an autotile (A1–A4).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isFloorTypeAutotile (tileId) → {Boolean}
Checks if it is a surface type autotile (with shape 48).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isGroundTile (tileId) → {Boolean}
Checks if it is a ground tile (A1, A2, A5).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isRoofTile (tileId) → {Boolean}
Checks if it is a roof tile (A3 odd rows).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isSameKindTile (tileID1, tileID2) → {Boolean}
Checks if the specified tiles are of the same kind (regardless of autotile shape).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileID1` | [Number](Number.md) | [Tile ID](#tile-id) |
| `tileID2` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isShadowingTile (tileId) → {Boolean}
Checks if the tile automatically casts a shadow when placed (A3 and A4).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isTileA1 (tileId) → {Boolean}
Checks if it is an A1 (animation) tile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isTileA2 (tileId) → {Boolean}
Checks if it is an A2 (ground) tile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isTileA3 (tileId) → {Boolean}
Checks if it is an A3 (building) tile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isTileA4 (tileId) → {Boolean}
Checks if it is an A4 (wall) tile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isTileA5 (tileId) → {Boolean}
Checks if it is an A5 (normal) tile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isVisibleTile (tileId) → {Boolean}
Checks if it is a visible tile (included in 0–TILE_ID_MAX).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isWallSideTile (tileId) → {Boolean}
Checks if it is a wall side tile (A3 even rows and A4 even rows).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isWallTile (tileId) → {Boolean}
Checks if it is a wall tile (A3 even rows and A4).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

### Methods

---

#### (static) getAutotileKind (tileId) → {[Number](Number.md)}
Returns the kind of autotile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) getAutotileShape (tileId) → {[Number](Number.md)}
Returns the shape of the autotile.
Values for ground, floor, and wall top: 0–47, roof and wall: 0–15, waterfall: 0–3.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isAutotile (tileId) → {Boolean}
Checks if it is an autotile (A1–A4).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isFloorTypeAutotile (tileId) → {Boolean}
Checks if it is a surface type autotile (with shape 48).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isGroundTile (tileId) → {Boolean}
Checks if it is a ground tile (A1, A2, A5).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isRoofTile (tileId) → {Boolean}
Checks if it is a roof tile (A3 odd rows).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isSameKindTile (tileID1, tileID2) → {Boolean}
Checks if the specified tiles are of the same kind (regardless of autotile shape).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileID1` | [Number](Number.md) | [Tile ID](#tile-id) |
| `tileID2` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isShadowingTile (tileId) → {Boolean}
Checks if the tile automatically casts a shadow when placed (A3 and A4).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isTileA1 (tileId) → {Boolean}
Checks if it is an A1 (animation) tile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isTileA2 (tileId) → {Boolean}
Checks if it is an A2 (ground) tile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isTileA3 (tileId) → {Boolean}
Checks if it is an A3 (building) tile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isTileA4 (tileId) → {Boolean}
Checks if it is an A4 (wall) tile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isTileA5 (tileId) → {Boolean}
Checks if it is an A5 (normal) tile.

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isVisibleTile (tileId) → {Boolean}
Checks if it is a visible tile (included in 0–TILE_ID_MAX).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isWallSideTile (tileId) → {Boolean}
Checks if it is a wall side tile (A3 even rows and A4 even rows).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isWallTile (tileId) → {Boolean}
Checks if it is a wall tile (A3 even rows and A4).

##### Arguments:

| Name     | Type            | Description             |
| -------- | --------------- | ----------------------- |
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### (static) isWallTopTile (tileId) → {Boolean}
 Is it a wall top tile (A4 odd rows)?

##### Arguments:

| Name     | Type                 | Description                    |
|----------|----------------------|--------------------------------|
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id)           |

---

#### (static) isWallTypeAutotile (tileId) → {Boolean}
 Is it a wall type tile (with 16 shapes)?

##### Arguments:

| Name     | Type                 | Description                    |
|----------|----------------------|--------------------------------|
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id)           |

---

#### (static) isWaterfallTile (tileId) → {Boolean}
 Is it a waterfall tile (A1 even columns from the second onward)?

##### Arguments:

| Name     | Type                 | Description                    |
|----------|----------------------|--------------------------------|
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id)           |

---

#### (static) isWaterfallTypeAutotile (tileId) → {Boolean}
 Is it a waterfall type autotile (with 4 shapes)?

##### Arguments:

| Name     | Type                 | Description                    |
|----------|----------------------|--------------------------------|
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id)           |

---

#### (static) isWaterTile (tileId) → {Boolean}
 Is it a water surface tile (excluding shallow obstacles in A1)?

##### Arguments:

| Name     | Type                 | Description                    |
|----------|----------------------|--------------------------------|
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id)           |

---

#### (static) makeAutotileId (kind, shape) → {[Number](Number.md)}
 Returns a tile ID from the specified autotile kind and shape.

##### Arguments:

| Name     | Type                 | Description                                                            |
|----------|----------------------|------------------------------------------------------------------------|
| `kind`   | [Number](Number.md) | Kind (refer to: [getAutotileKind](#static-getautotilekind-tileid--number)) |
| `shape`  | [Number](Number.md) | Shape (refer to: [getAutotileShape](#static-getautotileshape-tileid--number)) |

---

#### _compareChildOrder (a, b)
 Callback function for sorting conditions used in [_sortChildren](#_sortchildren-).<br />
 Child objects included in the children property are passed to a and b.<br />
 The order is evaluated by the z, y, and spriteId properties of the passed objects.<br />
 For the content of z, refer to [Overlap Priority](Sprite.md#overlay-priority).

##### Arguments:

| Name | Type   | Description                                 |
|------|--------|---------------------------------------------|
| `a`  | Object | Object with z, y, and spriteId properties. |
| `b`  | Object | Object with z, y, and spriteId properties. |

---

#### _addAllSpots (startX, startY) 
**@MZ** Add all spots.

##### Arguments:

| Name     | Type                 | Description                      |
|----------|----------------------|----------------------------------|
| `startX` | [Number](Number.md) | Starting x-coordinate (in tiles) |
| `startY` | [Number](Number.md) | Starting y-coordinate (in tiles) |

---

#### _addSpot (startX, startY, x, y) 
**@MZ** Add a spot.

##### Arguments:

| Name     | Type                 | Description                                 |
|----------|----------------------|---------------------------------------------|
| `startX` | [Number](Number.md) | Starting x-coordinate (in tiles)           |
| `startY` | [Number](Number.md) | Starting y-coordinate (in tiles)           |
| `x`      | [Number](Number.md) | Relative x-coordinate from the start position (in tiles) |
| `y`      | [Number](Number.md) | Relative y-coordinate from the start position (in tiles) |

---

#### _addSpotTile (tileId, dx, dy) 
**@MZ** Add a spot tile by separating it into layers (_upperLayer or _lowerLayer) based on the tile ID.

##### Arguments:

| Name     | Type                 | Description                       |
|----------|----------------------|-----------------------------------|
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id)               |
| `dx`     | [Number](Number.md) | x-coordinate within the layer (in pixels) |
| `dy`     | [Number](Number.md) | y-coordinate within the layer (in pixels) |

---

#### _addTile (layer, tileId, dx, dy) 
**@MZ** Add a tile to the tile layer.

##### Arguments:

| Name     | Type                     | Description                       |
|----------|--------------------------|-----------------------------------|
| `layer`  | [Tilemap.Layer](Tilemap.Layer.md) | Tile layer                        |
| `tileId` | [Number](Number.md)     | [Tile ID](#tile-id)               |
| `dx`     | [Number](Number.md)     | x-coordinate within the layer (in pixels) |
| `dy`     | [Number](Number.md)     | y-coordinate within the layer (in pixels) |

---

#### _addNormalTile (layer, tileId, dx, dy) 
**@MZ** Add a normal tile to the tile layer.

##### Arguments:

| Name     | Type                     | Description                       |
|----------|--------------------------|-----------------------------------|
| `layer`  | [Tilemap.Layer](Tilemap.Layer.md) | Tile layer                        |
| `tileId` | [Number](Number.md)     | [Tile ID](#tile-id)               |
| `dx`     | [Number](Number.md)     | x-coordinate within the layer (in pixels) |
| `dy`     | [Number](Number.md)     | y-coordinate within the layer (in pixels) |

---

#### _addAutotile (layer, tileId, dx, dy) 
**@MZ** Add an autotile to the tile layer.

##### Arguments:

| Name     | Type                     | Description                       |
|----------|--------------------------|-----------------------------------|
| `layer`  | [Tilemap.Layer](Tilemap.Layer.md) | Tile layer                        |
| `tileId` | [Number](Number.md)     | [Tile ID](#tile-id)               |
| `dx`     | [Number](Number.md)     | x-coordinate within the layer (in pixels) |
| `dy`     | [Number](Number.md)     | y-coordinate within the layer (in pixels) |

---

#### _addTableEdge (layer, tileId, dx, dy) 
**@MZ** Add the bottom edge of a table to the tile layer.

##### Arguments:

| Name     | Type                     | Description                       |
|----------|--------------------------|-----------------------------------|
| `layer`  | [Tilemap.Layer](Tilemap.Layer.md) | Tile layer                        |
| `tileId` | [Number](Number.md)     | [Tile ID](#tile-id)               |
| `dx`     | [Number](Number.md)     | x-coordinate within the layer (in pixels) |
| `dy`     | [Number](Number.md)     | y-coordinate within the layer (in pixels) |

---

#### _addShadow (layer, shadowBits, dx, dy) 
**@MZ** Add shadow pen data to the tile layer.

##### Arguments:

| Name        | Type                     | Description                                                           |
|-------------|--------------------------|-----------------------------------------------------------------------|
| `layer`     | [Tilemap.Layer](Tilemap.Layer.md) | Tile layer                                                           |
| `shadowBits`| [Number](Number.md)     | Specifies the position to draw within the divided tile (lower bits indicate left top/right top/left bottom/right bottom) |
| `dx`        | [Number](Number.md)     | x-coordinate within the layer (in pixels)                           |
| `dy`        | [Number](Number.md)     | y-coordinate within the layer (in pixels)                           |

---

#### _createLayers ()
 Generates low layers × 4 + high layers × 4 (z: 0 to 7).
 (Refer to: [Layer Arrangement](#layer-arrangement)

---

#### _isHigherTile (tileId) → {Boolean}
 Is it a high layer [☆] tile?

##### Arguments:

| Name     | Type                 | Description                    |
|----------|----------------------|--------------------------------|
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id)           |

---

####  _isOverpassPosition (mx, my) → {Boolean}
 Is it an overpass?<br />
 By default, this is an empty method that does nothing and functionality is added by plugins.<br />
 Used in the OverpassTile.js plugin.

##### Arguments:

| Name | Type                 | Description                   |
|------|----------------------|-------------------------------|
| `mx` | [Number](Number.md) | Map x-coordinate (in tiles)  |
| `my` | [Number](Number.md) | Map y-coordinate (in tiles)  |

---

#### _isTableTile (tileId) → {Boolean}
Is it a table tile?

##### Parameters:

| Name     | Type               | Description           |
|----------|--------------------|-----------------------|
| `tileId` | [Number](Number.md) | [Tile ID](#tile-id) |

---

#### _readMapData (x, y, z) → {[Number](Number.md)}
Returns the tile ID at the specified position.<br />
However, if z is 4, the return value corresponds to the shadowBits argument of [\_drawShadow](#_drawshadow-bitmap-shadowbits-dx-dy).

##### Parameters:

| Name | Type               | Description                                     |
|------|--------------------|-------------------------------------------------|
| `x`  | [Number](Number.md) | Map x-coordinate (in tiles)                    |
| `y`  | [Number](Number.md) | Map y-coordinate (in tiles)                    |
| `z`  | [Number](Number.md) | 0: A tiles, 1: A2 tiles right, 2-3: B-E tiles, 4: shadow pen, 5: region |

---

#### _sortChildren ()
Sorts child objects. The sorting criteria are described in [\_compareChildOrder](#_comparechildorder-a-b).

---

#### _updateBitmaps()
**@MZ** Updates the bitmaps.

---

#### destroy ()
**@MZ** Override: [PIXI.Container](PIXI.Container.md#destroy-).

---

#### initialize ()
Initialization when the object is created.

---

#### isReady () → {Boolean}
Is it ready for rendering?

---

#### refresh ()
Updates the tile map.

---

#### setBitmaps (bitmaps)
**@MZ** Sets the tile set images.

##### Parameters:

| Name     | Type                                             | Description                            |
|----------|--------------------------------------------------|----------------------------------------|
| `bitmaps` | [Array](Array.md).&lt;[Bitmap](Bitmap.md)&gt; | An array of bitmaps for the tile set. |

---

#### setData (width, height, data)
Sets the data for the tile map.

##### Parameters:

| Name     | Type               | Description                                                 |
|----------|--------------------|-------------------------------------------------------------|
| `width`  | [Number](Number.md) | Width of the map (in tiles)                                |
| `height` | [Number](Number.md) | Height of the map (in tiles)                               |
| `data`   | [Array](Array.md).&lt;[Number](Number.md)&gt; | 1D array of the map data (refer to [RPG.Map.data](RPG.Map.md#map-data)). |

---

#### update ()
Updates every frame.

---

#### updateTransform ()
Override: [PIXI.Container](PIXI.Container.md#updatetransform-).

---

### MV Deprecated Methods
_drawAutotile (bitmap, tileId, dx, dy), _drawNormalTile (bitmap, tileId, dx, dy), _drawShadow (bitmap, shadowBits, dx, dy), _drawTableEdge (bitmap, tileId, dx, dy), _drawTile (bitmap, tileId, dx, dy), _paintAllTiles (startX, startY), _paintTiles (startX, startY, x, y), _readLastTiles (i, x, y), refreshTileset (), _updateLayerPositions (startX, startY), _writeLastTiles (i, x, y, tiles)
