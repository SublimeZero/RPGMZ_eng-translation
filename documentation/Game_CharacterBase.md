[Class Tree](index.md)

# Class: Game_CharacterBase

A class that handles common processes for characters on the map.

It can check not only the character's state but also the state of the map it is on and whether it can move.

When using [script] in [move route settings], `this` refers to this class, so for example, <code>this.setPattern(0)</code> can be used to specify the walking pattern.

Related classes: [Sprite_Balloon](Sprite_Balloon.md), [Sprite_Animation](Sprite_Animation.md), [Game_Map](Game_Map.md)

### new Game_CharacterBase ()

### Subclasses

* [Game_Character](Game_Character.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | [read-only] X-coordinate on the map (in tiles) |
| `y` | [Number](Number.md) | [read-only] Y-coordinate on the map (in tiles) |
| `_x` | [Number](Number.md) | |
| `_y` | [Number](Number.md) | |
| `_realX` | [Number](Number.md) | Non-integer x (in tiles) |
| `_realY` | [Number](Number.md) | Non-integer y (in tiles) |
| `_moveSpeed` | [Number](Number.md) | Movement [speed] |
| `_moveFrequency` | [Number](Number.md) | Movement [frequency] |
| `_opacity` | [Number](Number.md) | Opacity (0 to 255) |
| `_blendMode` | [Number](Number.md) | [[Blend Mode]](Sprite.md#blend-mode) |
| `_direction` | [Number](Number.md) | Direction (ten-key compatible) |
| `_pattern` | [Number](Number.md) | Walking pattern (0 to 2) |
| `_priorityType` | [Number](Number.md) | [Priority](#priority) |
| `_tileId` | [Number](Number.md) | Foot tile [ID](Tilemap.md#tile-id) |
| `_characterName` | [String](String.md) | Character file name |
| `_characterIndex` | [Number](Number.md) | Character number (0 to 7) |
| `_isObjectCharacter` | Boolean | Is it an object (file or tile with a "!" prefix)? |
| `_walkAnime` | Boolean | [Walking Animation] |
| `_stepAnime` | Boolean | [Footstep Animation] |
| `_directionFix` | Boolean | [Fixed Direction] |
| `_through` | Boolean | [Through] |
| `_transparent` | Boolean | [Transparent] |
| `_bushDepth` | [Number](Number.md) | Depth of [bushes] |
| `_animationId` | [Number](Number.md) | Animation ID |
| `_balloonId` | [Number](Number.md) | Balloon ID |
| `_animationPlaying` | Boolean | Is the animation playing? |
| `_balloonPlaying` | Boolean | Is the balloon displayed? |
| `_animationCount` | [Number](Number.md) | Animation count |
| `_stopCount` | [Number](Number.md) | Stop count |
| `_jumpCount` | [Number](Number.md) | Jump count |
| `_jumpPeak` | [Number](Number.md) | Jump peak |
| `_movementSuccess` | Boolean | Was the movement successful? |

### [Priority]

| Number | Description |
| --- | --- |
| 2 | Above normal characters |
| 1 | Same as normal characters |
| 0 | Below normal characters |

### Methods

#### animationWait () → {[Number](Number.md)}
Returns the wait time for the animation (in frames).

#### blendMode () → {[Number](Number.md)}
Returns the [[Blend Mode]](Sprite.md#blend-mode).

#### bushDepth () → {[Number](Number.md)}
Returns the depth of [bushes] (in pixels).<br />
If there are bushes, it returns 1/4 of the tile height (default: 12px); otherwise, it returns 0.

#### canPass (x, y, d) → {Boolean}
Checks if passage is possible from the specified position in the specified direction.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Tiles |
| `y` | [Number](Number.md) | Tiles |
| `d` | [Number](Number.md) | Direction (ten-key compatible) |

#### canPassDiagonally (x, y, horz, vert) → {Boolean}
Checks if passage is possible diagonally from the specified position in the specified direction.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Tiles |
| `y` | [Number](Number.md) | Tiles |
| `horz` | [Number](Number.md) | Horizontal direction (ten-key compatible) |
| `vert` | [Number](Number.md) | Vertical direction (ten-key compatible) |

#### characterIndex () → {[Number](Number.md)}
Returns the character image number (0 to 7).

#### characterName () → {[String](String.md)}
Returns the character image file name (without extension).

#### checkEventTriggerTouch (x, y) → {Boolean}
Activates the event trigger at the specified position.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X-coordinate (in tiles) |
| `y` | [Number](Number.md) | Y-coordinate (in tiles) |

#### checkEventTriggerTouchFront (d)
Activates the event trigger in the specified direction.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `d` | [Number](Number.md) | Direction (ten-key compatible) |

#### checkStop (threshold) → {Boolean}
Checks if the stop state has exceeded the threshold.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `threshold` | [Number](Number.md) | Stop count threshold (in frames) |

#### copyPosition (character)
Copies the position of the specified character to its own position.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `character` | [Game_CharacterBase](Game_CharacterBase.md) | The character to copy from |

#### direction () → {[Number](Number.md)}
Returns the direction (ten-key compatible).

#### distancePerFrame () → {[Number](Number.md)}
Returns the distance moved per frame.

#### endAnimation ()
Ends the [animation] display.

#### endBalloon ()
Ends the display of the [balloon icon].

#### hasStepAnime () → {Boolean}
Checks if there is [footstep animation].

#### hasWalkAnime () → {Boolean}
Checks if there is [walking animation].

#### increaseSteps ()
Starts walking (increases step count).

#### initialize ()
Initialization when creating the object.

#### initMembers ()
Initializes member variables.

#### isAnimationPlaying () → {Boolean}
Checks if an [animation] is currently displayed.

#### isBalloonPlaying () → {Boolean}
Checks if the [balloon icon] is currently displayed.

#### isCollidedWithCharacters (x, y) → {Boolean}
Checks if the specified position is blocked by characters.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Tiles |
| `y` | [Number](Number.md) | Tiles |

#### isCollidedWithEvents (x, y) → {Boolean}
Checks if the specified position is blocked by [events].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Tiles |
| `y` | [Number](Number.md) | Tiles |

#### isCollidedWithVehicles (x, y) → {Boolean}
Checks if the specified position is blocked by [vehicles].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Tiles |
| `y` | [Number](Number.md) | Tiles |

#### isDashing () → {Boolean}
Checks if currently dashing.

#### isDebugThrough () → {Boolean}
Checks if currently passing through for debugging.

#### isDirectionFixed () → {Boolean}
Checks if the [direction is fixed].

#### isJumping () → {Boolean}
Checks if currently jumping.

#### isMapPassable (x, y, d) → {Boolean}
Checks if passage is possible on the map from the specified position in the specified direction, ignoring character and [event] obstacles.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Tiles |
| `y` | [Number](Number.md) | Tiles |
| `d` | [Number](Number.md) | Direction (ten-key compatible) |

#### isMovementSucceeded (x opt, y opt) → {Boolean}
Checks if the movement was successful.

##### Arguments

| Name | Type | Properties | Description |
| --- | --- | --- | --- |
| `x` | [Number](Number.md) | <optional> |  |
| `y` | [Number](Number.md) | <optional> |  |

#### isMoving () → {Boolean}
Checks if currently moving (not based on tile coordinates).

#### isNearTheScreen () → {Boolean}
Checks if near the edge of the screen, or if at a position where scrolling will stop.

#### isNormalPriority () → {Boolean}
Checks if the [priority] is [the same as normal characters].

#### isObjectCharacter () → {Boolean}
Checks if it is an object (image of a file or tile with a "!").

#### isOnBush () → {Boolean}
Checks if on a [bush].

#### isOnLadder () → {Boolean}
Checks if on a [ladder].

#### isOriginalPattern () → {Boolean}
Checks if it is the original pattern.

#### isStopping () → {Boolean}
Checks if it is stopped (at tile coordinates).

#### isThrough () → {Boolean}
Checks if in the [through] state.

#### isTile () → {Boolean}
Checks if it is an image for tiles (under the tilesets folder).

#### isTransparent () → {Boolean}
Checks if in the [transparent] state.

#### jump (xPlus, yPlus)
[Jump].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `xPlus` | [Number](Number.md) | Movement in the x direction (in tiles) |
| `yPlus` | [Number](Number.md) | Movement in the y direction (in tiles) |

#### jumpHeight () → {[Number](Number.md)}
Returns the current jump height (in pixels).

#### locate (x, y)
Sets the [event position] within the current map. Unlike [setPosition](Game_CharacterBase.md#setposition-x-y), it initializes posture and other aspects.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Tiles |
| `y` | [Number](Number.md) | Tiles |

#### maxPattern () → {[Number](Number.md)}
Returns the maximum number of patterns.

#### moveDiagonally (horz, vert)
Moves diagonally in the specified direction. Following the ten-key configuration, moving right-up corresponds to 9, but horizontal and vertical must be specified separately.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `horz` | [Number](Number.md) | Horizontal direction (4: left, 6: right) |
| `vert` | [Number](Number.md) | Vertical direction (2: down, 8: up) |

#### moveFrequency () → {[Number](Number.md)}
Returns the movement [frequency]. 
1: Minimum, 2: Low, 3: Normal, 4: High, 5: Maximum.

#### moveSpeed () → {[Number](Number.md)}
Returns the movement [speed].
1: 1/8 speed, 2: 1/4 speed, 3: 1/2 speed, 4: Normal speed, 5: 2x speed, 6: 4x speed.

#### moveStraight (d)
Moves [one step forward] in the specified direction.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `d` | [Number](Number.md) | Direction (ten-key compatible) |

#### opacity () → {[Number](Number.md)}
Returns the [opacity] (0 to 255).

#### pattern () → {[Number](Number.md)}
Returns the walking pattern (0 to 2).

#### pos (x, y) → {Boolean}
Checks if at the specified position.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) |  |
| `y` | [Number](Number.md) |  |

#### posNt (x, y) → {Boolean}
Checks if at the specified position and if passage is not possible (probably Nt = No Through).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) |  |
| `y` | [Number](Number.md) |  |

#### realMoveSpeed () → {[Number](Number.md)}
Returns the current movement speed, considering the dash state.

#### refreshBushDepth ()
Updates the depth of the [bushes].

#### regionId () → {[Number](Number.md)}
Returns the region ID that it is on.

#### resetPattern ()
Resets to the original pattern.

#### resetStopCount ()
Resets the stop counter.

#### reverseDir (d) → {[Number](Number.md)}
Returns the opposite direction of the specified direction (ten-key compatible).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `d` | [Number](Number.md) | Direction (ten-key compatible) |

#### screenX () → {[Number](Number.md)}
Returns the character's x-coordinate on the screen (in pixels).

#### screenY () → {[Number](Number.md)}
Returns the character's y-coordinate on the screen (in pixels).

#### screenZ () → {[Number](Number.md)}
Returns the overlapping position derived from `_priorityType * 2 + 1`. <br />
Used as the `z` property to determine the [overlapping priority](#overlapping-priority) of [Sprite](Sprite.md).

#### scrolledX () → {[Number](Number.md)}
Returns the character's x position on the screen (in tiles).

#### scrolledY () → {[Number](Number.md)}
Returns the character's y position on the screen (in tiles).

#### setBlendMode (blendMode)
Sets the [[blending method]](Sprite.md#blending-method).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `blendMode` | [Number](Number.md) | [[Blending method]](Sprite.md#blending-method) |

#### setDirection (d)
Sets the direction.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `d` | [Number](Number.md) | Direction (ten-key compatible) |

#### setDirectionFix (directionFix)
Sets the [direction fix].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `directionFix` | Boolean |  |

#### setImage (characterName, characterIndex)
Sets the character image (cannot be set simultaneously with tile images).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `characterName` | [String](String.md) | File name without the extension |
| `characterIndex` | [Number](Number.md) | Number (0 to 7) |

#### setMoveFrequency (moveFrequency)
Sets the movement [frequency].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `moveFrequency` | [Number](Number.md) | 1: Minimum, 2: Low, 3: Normal, 4: High, 5: Maximum |

#### setMovementSuccess (success)
Sets whether it can move. It won't move while `false` is set.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `success` | Boolean | Movement possible |

#### setMoveSpeed (moveSpeed)
Sets the movement [speed].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `moveSpeed` | [Number](Number.md) | 1: 1/8 speed, 2: 1/4 speed, 3: 1/2 speed, 4: Normal speed, 5: 2x speed, 6: 4x speed |

#### setOpacity (opacity)
Sets the [opacity].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `opacity` | [Number](Number.md) | 0 to 255 |

#### setPattern (pattern)
Sets the specified pattern number.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `pattern` | [Number](Number.md) |  |

#### setPosition (x, y)
Sets the [event position] within the current map.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Number of tiles |
| `y` | [Number](Number.md) | Number of tiles |

#### setPriorityType (priorityType)
Sets the [priority].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `priorityType` | [Number](Number.md) | 0: Below normal characters, 1: Same as normal characters, 2: Above normal characters |

#### setStepAnime (stepAnime)
Sets whether to do [step animation].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `stepAnime` | Boolean |  |

#### setThrough (through)
Sets the [through] state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `through` | Boolean |  |

#### setTileImage (tileId)
Sets the tile image (cannot be set simultaneously with character images).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `tileId` | [Number](Number.md) | [Tile ID](Tilemap.md#tile-id) |

#### setTransparent (transparent)
Sets the [transparent] state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `transparent` | Boolean |  |

#### setWalkAnime (walkAnime)
Sets whether to do [walking animation].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `walkAnime` | Boolean |  |

#### shiftY () → {[Number](Number.md)}
Returns the shift amount in the vertical direction (in pixels). <br />
Typically returns 6, returns 0 for objects (files or tiles with a !).

#### startAnimation ()
Starts displaying [animation].

#### startBalloon ()
Starts displaying the [balloon icon].

#### straighten ()
Straightens the character to an upright position (not during walking or stepping).

#### terrainTag () → {[Number](Number.md)}
Returns the [terrain tag] that it is on.

#### tileId () → {[Number](Number.md)}
Returns the [Tile ID](Tilemap.md#tile-id).

#### update ()
Updates the character.

#### updateAnimation ()
Updates the animation.

#### updateAnimationCount ()
Updates the animation counter.

#### updateJump ()
Updates the jump state.

#### updateMove ()
Updates the movement state.

#### updatePattern ()
Updates the pattern.

#### updateStop ()
Updates the stop state.

### Deprecated MV Methods
animationId (), balloonId (), requestAnimation (animationId), requestBalloon (balloonId)
