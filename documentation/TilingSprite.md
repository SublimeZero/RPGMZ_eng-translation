[Class Tree](index.md)

# Class: TilingSprite

## Superclass: [PIXI.TilingSprite](http://pixijs.download/v5.3.12/docs/PIXI.TilingSprite.html)

Sprite for tiled (repeating) images.<br />
Used for [background] and window backgrounds.

Modified from the MV inheritance source `PIXI.extras.PictureTilingSprite`.

Related classes: [Spriteset_Map](Spriteset_Map.md), [Window](Window.md)

---

### new TilingSprite (bitmap)
#### Arguments

| Name     | Type                 | Description      |
|----------|----------------------|------------------|
| `bitmap` | [Bitmap](Bitmap.md) | Image for tiling  |

---

### Subclasses

* [Sprite_Battleback](Sprite_Battleback.md) 

---

### Properties

| Identifier | Type                 | Description        |
|------------|----------------------|--------------------|
| `bitmap`   | [Bitmap](Bitmap.md) | Image for tiling    |
| `opacity`  | [Number](Number.md)  | Opacity (0 to 255)  |
| `spriteId` | [Number](Number.md)  | Sprite ID           |
| `origin`   | [Point](Point.md)    | Scroll origin       |
| `x`       | [Number](Number.md)  | X coordinate (pixels)|
| `y`       | [Number](Number.md)  | Y coordinate (pixels)|
| `_bitmap`  | [Bitmap](Bitmap.md) | Image for tiling    |
| `_width`   | [Number](Number.md)  | Width               |
| `_height`  | [Number](Number.md)  | Height              |
| `_frame`   | [Rectangle](Rectangle.md) | Frame         |

---

### Deprecated MV Properties
`visibility` 

---

### Methods

#### _onBitmapChange ()
**@MZ** Handler for when the image changes.

---

#### _onBitmapLoad ()
Handler for when the image is loaded.

---

#### _refresh ()
Redraw.

---

#### destroy ()
**@MZ** Dispose of the object.

---

#### initialize (bitmap)
Initialization when the object is created.

##### Arguments

| Name     | Type                 | Description      |
|----------|----------------------|------------------|
| `bitmap` | [Bitmap](Bitmap.md) | Image for tiling  |

---

#### move (x, y, width, height)
Move.

##### Arguments

| Name     | Type                 | Description      |
|----------|----------------------|------------------|
| `x`      | [Number](Number.md)  | X coordinate (pixels) |
| `y`      | [Number](Number.md)  | Y coordinate (pixels) |
| `width`  | [Number](Number.md)  | Width (pixels)   |
| `height` | [Number](Number.md)  | Height (pixels)  |

---

#### setFrame (x, y, width, height)
Set the display frame.

##### Arguments

| Name     | Type                 | Description      |
|----------|----------------------|------------------|
| `x`      | [Number](Number.md)  | X coordinate (pixels) |
| `y`      | [Number](Number.md)  | Y coordinate (pixels) |
| `width`  | [Number](Number.md)  | Width (pixels)   |
| `height` | [Number](Number.md)  | Height (pixels)  |

---

#### update ()
Update every frame.

---

#### updateTransform ()
Update the transformation.

---

### Deprecated MV Methods
_renderCanvas (renderer), _renderWebGL (renderer)
