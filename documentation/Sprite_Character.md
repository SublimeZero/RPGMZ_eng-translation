# Class: Sprite_Character

## Superclass: [Sprite](Sprite.md)

| Database       | JSON Data                  | Object                  |
|----------------|----------------------------|-------------------------|
| [Actor]        | [RPG.Actor](RPG.Actor.md)   | [Game_Actor](Game_Actor.md) |
| [Player]       | Same as Actor               | [Game_Player](Game_Player.md) |
| [Follower]     | Same as Actor               | [Game_Follower](Game_Follower.md) |
| [Event]        | [RPG.Event](RPG.Event.md)   | [Game_Event](Game_Event.md) |
| [Vehicle]      | [RPG.System.Vehicle](RPG.System.Vehicle.md) | [Game_Vehicle](Game_Vehicle.md) |

This class represents a sprite used to display characters on the map.

In MV, the superclass was `Sprite_Base`, but it has been removed. Additionally, balloon-related functionality has been moved to [Spriteset_Map](Spriteset_Map.md).

### Main Paths
```js
SceneManager._scene._spriteset._characterSprites[n]
SceneManager._scene._spriteset._tilemap.children[n]

// Extract JSON data from Sprite_Character
$gameParty.leader().actor() // Game_Player
this._character.actor().actor() // Game_Follower
this._character.event(); // Game_Event
this._character.vehicle(); // Game_Vehicle
```

# Class: Sprite_Character

## Superclass: [Sprite](Sprite.md)

Changes were made in versions 1.4.4 and 1.5.0.

### Related Classes:
- [Scene_Map](Scene_Map.md)
- [Sprite_Actor](Sprite_Actor.md)
- [Tilemap](Tilemap.md)
- [Spriteset_Map](Spriteset_Map.md)

---

### Constructor: `new Sprite_Character (character)`

#### Arguments

| Name        | Type                              | Description        |
|-------------|-----------------------------------|--------------------|
| `character` | [Game_Character](Game_Character.md) | Character data     |

---

### Properties

| Identifier       | Type                              | Description                          |
|------------------|-----------------------------------|--------------------------------------|
| `_character`     | [Game_Character](Game_Character.md) | Character data                      |
| `_balloonDuration` | [Number](Number.md)              | Duration of the balloon (unused)    |
| `_tilesetId`     | [Number](Number.md)               | ID of the tileset                   |
| `_upperBody`     | [Sprite](Sprite.md)               | Sprite for the upper body           |
| `_lowerBody`     | [Sprite](Sprite.md)               | Sprite for the lower body           |
| `_bushDepth`     | [Number](Number.md)               | Depth of the bush (in pixels)       |

---

### Deprecated MV Property:
- `_balloonSprite`

---

### Methods Inherited from the Superclass:

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

* [destroy ()](Sprite.md#destroy-)
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

---

#### `checkCharacter(character) → {boolean}`
**@MZ** Checks if the specified character is set.

##### Arguments

| Name       | Type                                | Description   |
|------------|-------------------------------------|---------------|
| `character`| [Game_Character](Game_Character.md) | Character     |

---

#### `characterBlockX() → {Number}`
Returns the x-coordinate of the character block.

---

#### `characterBlockY() → {Number}`
Returns the y-coordinate of the character block.

---

#### `characterPatternX() → {Number}`
Returns the x-coordinate of the character pattern.

---

#### `characterPatternY() → {Number}`
Returns the y-coordinate of the character pattern.

---

#### `createHalfBodySprites()`
Creates half-body sprites.

---

#### `initialize(character)`
Overrides: [Sprite](Sprite.md#initialize-)

##### Arguments

| Name       | Type                                | Description       |
|------------|-------------------------------------|-------------------|
| `character`| [Game_Character](Game_Character.md) | Character data    |

---

#### `initMembers()`
Initializes member variables.

---

#### `isEmptyCharacter() → {Boolean}`
**@MZ** Checks if the character image is not set.

---

#### `isImageChanged() → {Boolean}`
Checks if the image has changed.

---

#### `isObjectCharacter() → {boolean}`
**@MZ** Checks if the image is of an object character (file with '!' or tile).

---

#### `isTile() → {boolean}`
Checks if the character uses a tile image.

---

#### `patternHeight() → {Number}`
Returns the height of the pattern (in pixels).

---

#### `patternWidth() → {Number}`
Returns the width of the pattern (in pixels).

---

#### `setCharacter(character)`
Resets the character. Equivalent to the value passed in the constructor.

##### Arguments

| Name       | Type                                | Description   |
|------------|-------------------------------------|---------------|
| `character`| [Game_Character](Game_Character.md) | Character     |

---

#### `setCharacterBitmap()`
Sets the character's image.

---

#### `setTileBitmap()`
Sets the tile image.

---

#### `tilesetBitmap(tileId) → {Bitmap}`
Returns the tileset image (bitmap) for the specified tile ID.

##### Arguments

| Name     | Type     | Description       |
|----------|----------|-------------------|
| `tileId` | [Number](Number.md) | Tile ID [Reference](Tilemap.md#タイルID) |

---

#### `update()`
Overrides: [Sprite](Sprite.md#update-)

---

#### `updateBitmap()`
Updates the bitmap.

---

#### `updateCharacterFrame()`
Updates the character's frame.

---

#### `updateFrame()`
Updates the frame.

---

#### `updateHalfBodySprites()`
Updates the half-body sprites.

---

#### `updateOther()`
Performs other updates.

---

#### `updatePosition()`
Updates the character's position.

---

#### `updateTileFrame()`
Updates the tile's frame.

---

#### `updateVisibility()`
Overrides: [Sprite](Sprite.md#updateVisibility-)

---

### Deprecated MV Methods
- `endBalloon()`
- `isBalloonPlaying()`
- `setupAnimation()`
- `setupBalloon()`
- `startBalloon()`
- `updateAnimation()`
- `updateBalloon()`
