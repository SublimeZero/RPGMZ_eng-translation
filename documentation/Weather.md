[Class Tree](index.md)

# Class: Weather

## Superclass: [PIXI.Container](PIXI.Container.md)

A class for displaying weather effect visuals.

Related Classes: [Spriteset_Map](Spriteset_Map.md)

---

### new Weather ()

---

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `type` | [String](String.md) | [Type of weather](Weather.md#weather-type) |
| `power` | [Number](Number.md) | Intensity of the weather (0 to 9) |
| `origin` | [Point](Point.md) | Scroll origin |
| `viewport` | [Bitmap](Bitmap.md) |  |
| `_width` | [Number](Number.md) | Width (in pixels) |
| `_height` | [Number](Number.md) | Height (in pixels) |
| `_sprites` | [Array](Array.md).&lt;[Sprite](Sprite.md)&gt; | Included sprites |
| `_rainBitmap` | [Bitmap](Bitmap.md) | Image for rain |
| `_stormBitmap` | [Bitmap](Bitmap.md) | Image for storm |
| `_snowBitmap` | [Bitmap](Bitmap.md) | Image for snow |
| `_dimmerSprite` | [ScreenSprite](ScreenSprite.md) | Dimmer sprite |

---

#### Weather Types

| type | Weather Type |
| --- | --- |
| "none" | None |
| "rain" | Rain |
| "storm" | Storm |
| "snow" | Snow |

---

### Methods

#### _addSprite ()
Adds a sprite.

---

#### _createBitmaps ()
Generates images.

---

#### _createDimmer ()
Generates the dimmer sprite.

---

#### _rebornSprite (sprite)
Repositions the sprite.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sprite` | [Sprite](Sprite.md) |  |

---

#### _removeSprite ()
Removes a sprite.

---

#### _updateAllSprites ()
Updates all sprites.

---

#### _updateDimmer ()
Updates the dimmer sprite.

---

#### _updateRainSprite (sprite)
Updates the rain sprite.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sprite` | [Sprite](Sprite.md) | Sprite |

---

#### _updateSnowSprite (sprite)
Updates the snow sprite.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sprite` | [Sprite](Sprite.md) | Sprite |

---

#### (static) _updateSprite (sprite)
Updates the sprite.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sprite` | [Sprite](Sprite.md) | Sprite |

---

#### (static) _updateStormSprite (sprite)
Updates the storm sprite.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sprite` | [Sprite](Sprite.md) | Sprite |

---

#### initialize ()
Initialization when the object is created.

---

#### update ()
Updates each frame.
