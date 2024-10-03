[Class Tree](index.md)

# Class: Sprite_Battleback

## Superclass: [TilingSprite](TilingSprite.md)

**@MZ** A sprite for battle [backgrounds].

- Background Image 1 (ground) for the farthest layer
- Background Image 2 (wall) for the front layer

These two images are combined to form the battle background.

Related Classes: [Spriteset_Battle](Spriteset_Battle.md), [Scene_Battle](Scene_Battle.md)

### new Sprite_Battleback (type)

#### Arguments

| Name  | Type                | Description                                  |
|-------|---------------------|----------------------------------------------|
| `type` | [Number](Number.md) | Type (0: battlebacks1, 1: battlebacks2)      |


### Methods Inherited from the Superclass

#### [TilingSprite](TilingSprite.md)

- [destroy ()](TilingSprite.md#destroy-)
- [initialize (bitmap)](TilingSprite.md#initialize-bitmap)
- [move (x, y, width, height)](TilingSprite.md#move-x-y-width-height)
- [setFrame (x, y, width, height)](TilingSprite.md#setframe-x-y-width-height)
- [update ()](TilingSprite.md#update-)
- [updateTransform ()](TilingSprite.md#updatetransform-)

### Methods

#### adjustPosition ()
Adjusts the position.

#### autotileType (z) → {[Number](Number.md)}
Returns the type of autotile at the current location (returns -1 if not an autotile).

##### Arguments

| Name | Type                | Description           |
|------|---------------------|-----------------------|
| `z`  | [Number](Number.md)  | Layer (0 to 3)        |

#### battleback1Bitmap () → {[Bitmap](Bitmap.md)}
Returns Background Image 1.

#### battleback2Bitmap () → {[Bitmap](Bitmap.md)}
Returns Background Image 2.

#### battleback1Name () → {[String](String.md)}
Returns the name of Background Image 1.

#### battleback2Name () → {[String](String.md)}
Returns the name of Background Image 2.

#### defaultBattleback1Name () → {[String](String.md)}
Returns the default name for Background Image 1 ("Grassland").

#### defaultBattleback2Name () → {[String](String.md)}
Returns the default name for Background Image 2 ("Grassland").

#### initialize (type)
Initializes the object when created.

##### Arguments

| Name  | Type                | Description                                  |
|-------|---------------------|----------------------------------------------|
| `type` | [Number](Number.md) | Type (0: battlebacks1, 1: battlebacks2)      |

#### normalBattleback1Name () → {[String](String.md)}
Returns the name of the normal Background Image 1 on the world map.

#### normalBattleback2Name () → {[String](String.md)}
Returns the name of the normal Background Image 2 on the world map.

#### overworldBattleback1Name () → {[String](String.md)}
Returns the name of Background Image 1 on the world map.

#### overworldBattleback2Name () → {[String](String.md)}
Returns the name of Background Image 2 on the world map.

#### shipBattleback1Name () → {[String](String.md)}
Returns the name of Background Image 1 at sea ("Ship").

#### shipBattleback2Name () → {[String](String.md)}
Returns the name of Background Image 2 at sea ("Ship").

#### terrainBattleback1Name (type) → {[String](String.md)}
Returns the name of the normal Background Image 1 on the specified tile.
Used when the tileset's [field type] is set.

##### Arguments

| Name  | Type                | Description        |
|-------|---------------------|--------------------|
| `type` | [Number](Number.md) | Terrain type       |

| `type` | Background Name    |
|--------|--------------------|
| 4,5    | "PoisonSwamp"      |
| 24,25  | "Wasteland"        |
| 26,27  | "DirtField"        |
| 32,33  | "Desert"           |
| 34     | "Lava1"            |
| 35     | "Lava2"            |
| 40,41  | "Snowfield"        |
| 42     | "Clouds"           |

#### terrainBattleback2Name (type) → {[String](String.md)}
Returns the name of the normal Background Image 2 on the specified tile.
Used when the tileset's [field type] is set.

##### Arguments

| Name  | Type                | Description        |
|-------|---------------------|--------------------|
| `type` | [Number](Number.md) | Terrain type       |

| `type` | Background Name    |
|--------|--------------------|
| 4,5    | "PoisonSwamp"      |
| 20,21  | "Forest"           |
| 22,30,38 | "Cliff"          |
| 24,25,26,27 | "Wasteland"   |
| 32,33  | "Desert"           |
| 34,35  | "Lava"             |
| 40,41  | "Snowfield"        |
| 42     | "Clouds"           |
