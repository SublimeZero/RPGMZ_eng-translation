[Class Tree](index.md)

# Class: Game_Character

## Superclass: [Game_CharacterBase](Game_CharacterBase.md)

| Database            | JSON Data                | Object                   | Sprite                   |
|---------------------|--------------------------|--------------------------|--------------------------|
| [Event]             | [RPG.Event](RPG.Event.md) | [Game_Event](Game_Event.md) | [Sprite_Character](Sprite_Character.md) |
| [Player]            | [RPG.Actor](RPG.Actor.md) | [Game_Player](Game_Player.md) | 〃                       |
| [Follower]          | 〃                        | [Game_Follower](Game_Follower.md) | 〃                       |
| [Vehicle]           | [RPG.System.Vehicle](RPG.System.Vehicle.md) | [Game_Vehicle](Game_Vehicle.md) | 〃                       |

Class for characters displayed on the map.

Related Classes: [Game_Interpreter](Game_Interpreter.md), [Game_Actor](Game_Actor.md), [Game_Map](Game_Map.md)

### new Game_Character ()

### Subclasses

* [Game_Event](Game_Event.md)
* [Game_Follower](Game_Follower.md)
* [Game_Player](Game_Player.md)
* [Game_Vehicle](Game_Vehicle.md)

### Properties

Constants starting with ROUTE_ correspond to the [Movement Route Settings]-[Movement Commands].

| Identifier             | Type                          | Description                                  |
|------------------------|-------------------------------|----------------------------------------------|
| `ROUTE_END`            | [Number](Number.md)          | [static] End                                 |
| `ROUTE_MOVE_DOWN`      | [Number](Number.md)          | [static] Move Down                          |
| `ROUTE_MOVE_LEFT`      | [Number](Number.md)          | [static] Move Left                          |
| `ROUTE_MOVE_RIGHT`     | [Number](Number.md)          | [static] Move Right                         |
| `ROUTE_MOVE_UP`        | [Number](Number.md)          | [static] Move Up                            |
| `ROUTE_MOVE_LOWER_L`   | [Number](Number.md)          | [static] Move Lower Left                    |
| `ROUTE_MOVE_LOWER_R`   | [Number](Number.md)          | [static] Move Lower Right                   |
| `ROUTE_MOVE_UPPER_L`   | [Number](Number.md)          | [static] Move Upper Left                    |
| `ROUTE_MOVE_UPPER_R`   | [Number](Number.md)          | [static] Move Upper Right                   |
| `ROUTE_MOVE_RANDOM`     | [Number](Number.md)          | [static] Move Random                        |
| `ROUTE_MOVE_TOWARD`    | [Number](Number.md)          | [static] Move Toward Player                 |
| `ROUTE_MOVE_AWAY`      | [Number](Number.md)          | [static] Move Away from Player              |
| `ROUTE_MOVE_FORWARD`    | [Number](Number.md)          | [static] Move Forward                       |
| `ROUTE_MOVE_BACKWARD`   | [Number](Number.md)          | [static] Move Backward                      |
| `ROUTE_JUMP`           | [Number](Number.md)          | [static] Jump                               |
| `ROUTE_WAIT`           | [Number](Number.md)          | [static] Wait                               |
| `ROUTE_TURN_DOWN`      | [Number](Number.md)          | [static] Turn Down                          |
| `ROUTE_TURN_LEFT`      | [Number](Number.md)          | [static] Turn Left                          |
| `ROUTE_TURN_RIGHT`     | [Number](Number.md)          | [static] Turn Right                         |
| `ROUTE_TURN_UP`        | [Number](Number.md)          | [static] Turn Up                            |
| `ROUTE_TURN_90D_R`     | [Number](Number.md)          | [static] Rotate 90 Degrees Right            |
| `ROUTE_TURN_90D_L`     | [Number](Number.md)          | [static] Rotate 90 Degrees Left             |
| `ROUTE_TURN_180D`      | [Number](Number.md)          | [static] Rotate 180 Degrees                 |
| `ROUTE_TURN_90D_R_L`   | [Number](Number.md)          | [static] Rotate 90 Degrees Right or Left    |
| `ROUTE_TURN_RANDOM`    | [Number](Number.md)          | [static] Randomly Turn                       |
| `ROUTE_TURN_TOWARD`    | [Number](Number.md)          | [static] Turn Toward Player                  |
| `ROUTE_TURN_AWAY`      | [Number](Number.md)          | [static] Turn Away from Player               |
| `ROUTE_SWITCH_ON`      | [Number](Number.md)          | [static] Switch ON                          |
| `ROUTE_SWITCH_OFF`     | [Number](Number.md)          | [static] Switch OFF                         |
| `ROUTE_CHANGE_SPEED`    | [Number](Number.md)          | [static] Change Speed                        |
| `ROUTE_CHANGE_FREQ`     | [Number](Number.md)          | [static] Change Frequency                    |
| `ROUTE_WALK_ANIME_ON`   | [Number](Number.md)          | [static] Walking Animation ON                |
| `ROUTE_WALK_ANIME_OFF`  | [Number](Number.md)          | [static] Walking Animation OFF               |
| `ROUTE_STEP_ANIME_ON`   | [Number](Number.md)          | [static] Step Animation ON                   |
| `ROUTE_STEP_ANIME_OFF`  | [Number](Number.md)          | [static] Step Animation OFF                  |
| `ROUTE_DIR_FIX_ON`      | [Number](Number.md)          | [static] Direction Fix ON                    |
| `ROUTE_DIR_FIX_OFF`     | [Number](Number.md)          | [static] Direction Fix OFF                   |
| `ROUTE_THROUGH_ON`      | [Number](Number.md)          | [static] Through ON                          |
| `ROUTE_THROUGH_OFF`     | [Number](Number.md)          | [static] Through OFF                         |
| `ROUTE_TRANSPARENT_ON`   | [Number](Number.md)          | [static] Transparency ON                     |
| `ROUTE_TRANSPARENT_OFF`  | [Number](Number.md)          | [static] Transparency OFF                    |
| `ROUTE_CHANGE_IMAGE`     | [Number](Number.md)          | [static] Change Image                        |
| `ROUTE_CHANGE_OPACITY`   | [Number](Number.md)          | [static] Change Opacity                      |
| `ROUTE_CHANGE_BLEND_MODE` | [Number](Number.md)          | [static] Change Blend Mode                   |
| `ROUTE_PLAY_SE`          | [Number](Number.md)          | [static] Play SE                             |
| `ROUTE_SCRIPT`           | [Number](Number.md)          | [static] Script                              |
| `_moveRouteForcing`      | Boolean                     | Is [Move Route] being forced?               |
| `_moveRoute`             | [RPG.MoveRoute](RPG.MoveRoute.md) | [Move Route]                              |
| `_moveRouteIndex`        | [Number](Number.md)          | [Move Route] Number                         |
| `_originalMoveRoute`     | [RPG.MoveRoute](RPG.MoveRoute.md) | Original [Move Route]                       |
| `_originalMoveRouteIndex`| [Number](Number.md)          | Original [Move Route] Number                |
| `_waitCount`             | [Number](Number.md)          | Wait Count                                   |

### Methods Inherited from Superclass

#### [Game_CharacterBase](Game_CharacterBase.md)

* [animationId ()](Game_CharacterBase.md#animationid---number)
* [animationWait ()](Game_CharacterBase.md#animationwait---number)
* [balloonId ()](Game_CharacterBase.md#balloonid---number)
* [blendMode ()](Game_CharacterBase.md#blendmode---number)
* [bushDepth ()](Game_CharacterBase.md#bushdepth---number)
* [canPass (x, y, d)](Game_CharacterBase.md#canpass-x-y-d--boolean)
* [canPassDiagonally (x, y, horz, vert)](Game_CharacterBase.md#canpassdiagonally-x-y-horz-vert--boolean)
* [characterIndex ()](Game_CharacterBase.md#characterindex---number)
* [characterName ()](Game_CharacterBase.md#charactername---string)
* [checkEventTriggerTouch (x, y)](Game_CharacterBase.md#checkeventtriggertouch-x-y--boolean)
* [checkEventTriggerTouchFront (d)](Game_CharacterBase.md#checkeventtriggertouchfront-d)
* [checkStop (threshold)](Game_CharacterBase.md#checkstop-threshold--boolean)
* [copyPosition (character)](Game_CharacterBase.md#copyposition-character)
* [direction ()](Game_CharacterBase.md#direction---number)
* [distancePerFrame ()](Game_CharacterBase.md#distanceperframe---number)
* [endAnimation ()](Game_CharacterBase.md#endanimation-)
* [endBalloon ()](Game_CharacterBase.md#endballoon-)
* [hasStepAnime ()](Game_CharacterBase.md#hasstepanime---boolean)
* [hasWalkAnime ()](Game_CharacterBase.md#haswalkanime---boolean)
* [increaseSteps ()](Game_CharacterBase.md#increasesteps-)
* [isAnimationPlaying ()](Game_CharacterBase.md#isanimationplaying---boolean)
* [isBalloonPlaying ()](Game_CharacterBase.md#isballoonplaying---boolean)
* [isCollidedWithCharacters (x, y)](Game_CharacterBase.md#iscollidedwithcharacters-x-y--boolean)
* [isCollidedWithEvents (x, y)](Game_CharacterBase.md#iscollidedwithevents-x-y--boolean)
* [isCollidedWithVehicles (x, y)](Game_CharacterBase.md#iscollidedwithvehicles-x-y--boolean)
* [isDashing ()](Game_CharacterBase.md#isdashing---boolean)
* [isDebugThrough ()](Game_CharacterBase.md#isdebugthrough---boolean)
* [isDirectionFixed ()](Game_CharacterBase.md#isdirectionfixed---boolean)
* [isJumping ()](Game_CharacterBase.md#isjumping---boolean)
* [isMapPassable (x, y, d)](Game_CharacterBase.md#ismappassable-x-y-d--boolean)
* [isMovementSucceeded (x opt, y opt)](Game_CharacterBase.md#ismovementsucceeded-x-opt-y-opt--boolean)
* [isMoving ()](Game_CharacterBase.md#ismoving---boolean)
* [isNearTheScreen ()](Game_CharacterBase.md#isnearthescreen---boolean)
* [isNormalPriority ()](Game_CharacterBase.md#isnormalpriority---boolean)
* [isObjectCharacter ()](Game_CharacterBase.md#isobjectcharacter---boolean)
* [isOnBush ()](Game_CharacterBase.md#isonbush---boolean)
* [isOnLadder ()](Game_CharacterBase.md#isonladder---boolean)
* [isOriginalPattern ()](Game_CharacterBase.md#isoriginalpattern---boolean)
* [isStopping ()](Game_CharacterBase.md#isstopping---boolean)
* [isThrough ()](Game_CharacterBase.md#isthrough---boolean)
* [isTile ()](Game_CharacterBase.md#istile---boolean)
* [isTransparent ()](Game_CharacterBase.md#istransparent---boolean)
* [jump (xPlus, yPlus)](Game_CharacterBase.md#jump-xplus-yplus)
* [jumpHeight ()](Game_CharacterBase.md#jumpheight---number)
* [locate (x, y)](Game_CharacterBase.md#locate-x-y)
* [maxPattern ()](Game_CharacterBase.md#maxpattern---number)
* [moveDiagonally (horz, vert)](Game_CharacterBase.md#movediagonally-horz-vert)
* [moveFrequency ()](Game_CharacterBase.md#movefrequency---number)
* [moveSpeed ()](Game_CharacterBase.md#movespeed---number)
* [moveStraight (d)](Game_CharacterBase.md#movestraight-d)
* [opacity ()](Game_CharacterBase.md#opacity---number)
* [pattern ()](Game_CharacterBase.md#pattern---number)
* [pos (x, y)](Game_CharacterBase.md#pos-x-y--boolean)
* [posNt (x, y)](Game_CharacterBase.md#posnt-x-y--boolean)
* [realMoveSpeed ()](Game_CharacterBase.md#realmovespeed---number)
* [refreshBushDepth ()](Game_CharacterBase.md#refreshbushdepth-)
* [regionId ()](Game_CharacterBase.md#regionid---number)
* [requestAnimation (animationId)](Game_CharacterBase.md#requestanimation-animationid)
* [requestBalloon (balloonId)](Game_CharacterBase.md#requestballoon-balloonid)
* [resetPattern ()](Game_CharacterBase.md#resetpattern-)
* [resetStopCount ()](Game_CharacterBase.md#resetstopcount-)
* [reverseDir (d)](Game_CharacterBase.md#reversedir-d--number)
* [screenX ()](Game_CharacterBase.md#screenx---number)
* [screenY ()](Game_CharacterBase.md#screeny---number)
* [screenZ ()](Game_CharacterBase.md#screenz---number)
* [scrolledX ()](Game_CharacterBase.md#scrolledx---number)
* [scrolledY ()](Game_CharacterBase.md#scrolledy---number)
* [setBlendMode (blendMode)](Game_CharacterBase.md#setblendmode-blendmode)
* [setDirection (d)](Game_CharacterBase.md#setdirection-d)
* [setDirectionFix (directionFix)](Game_CharacterBase.md#setdirectionfix-directionfix)
* [setImage (characterName, characterIndex)](Game_CharacterBase.md#setimage-charactername-characterindex)
* [setMoveFrequency (moveFrequency)](Game_CharacterBase.md#setmovefrequency-movefrequency)
* [setMovementSuccess (success)](Game_CharacterBase.md#setmovementsuccess-success)
* [setMoveSpeed (moveSpeed)](Game_CharacterBase.md#setmovespeed-movespeed)
* [setOpacity (opacity)](Game_CharacterBase.md#setopacity-opacity)
* [setPattern (pattern)](Game_CharacterBase.md#setpattern-pattern)
* [setPosition (x, y)](Game_CharacterBase.md#setposition-x-y)
* [setPriorityType (priorityType)](Game_CharacterBase.md#setprioritytype-prioritytype)
* [setStepAnime (stepAnime)](Game_CharacterBase.md#setstepanime-stepanime)
* [setThrough (through)](Game_CharacterBase.md#setthrough-through)
* [setTileImage (tileId)](Game_CharacterBase.md#settileimage-tileid)
* [setTransparent (transparent)](Game_CharacterBase.md#settransparent-transparent)
* [setWalkAnime (walkAnime)](Game_CharacterBase.md#setwalkanime-walkanime)
* [shiftY ()](Game_CharacterBase.md#shifty---number)
* [startAnimation ()](Game_CharacterBase.md#startanimation-)
* [startBalloon ()](Game_CharacterBase.md#startballoon-)
* [straighten ()](Game_CharacterBase.md#straighten-)
* [terrainTag ()](Game_CharacterBase.md#terraintag---number)
* [tileId ()](Game_CharacterBase.md#tileid---number)
* [update ()](Game_CharacterBase.md#update-)
* [updateAnimation ()](Game_CharacterBase.md#updateanimation-)
* [updateAnimationCount ()](Game_CharacterBase.md#updateanimationcount-)
* [updateJump ()](Game_CharacterBase.md#updatejump-)
* [updateMove ()](Game_CharacterBase.md#updatemove-)
* [updatePattern ()](Game_CharacterBase.md#updatepattern-)

### Methods

#### advanceMoveRouteIndex ()
Advances the execution position of the [move route].

#### deltaXFrom (x) → {[Number](Number.md)}
Returns the difference (in tiles) between the specified x-coordinate and the object's own x-coordinate.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x-coordinate (in tiles) |

#### deltaYFrom (y) → {[Number](Number.md)}
Returns the difference (in tiles) between the specified y-coordinate and the object's own y-coordinate.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `y` | [Number](Number.md) | y-coordinate (in tiles) |

#### findDirectionTo (goalX, goalY) → {[Number](Number.md)}
Returns the direction (ten-key compatible) to reach the specified coordinates.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `goalX` | [Number](Number.md) | x-coordinate (in tiles) |
| `goalY` | [Number](Number.md) | y-coordinate (in tiles) |

#### forceMoveRoute (moveRoute)
Forces the [move route].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `moveRoute` | [RPG.MoveRoute](RPG.MoveRoute.md) | [move route] |

#### initialize ()
Override: [Game_CharacterBase](Game_CharacterBase.md#initialize-)

#### initMembers ()
Override: [Game_CharacterBase](Game_CharacterBase.md#initmembers-)

#### isMoveRouteForcing () → {Boolean}
Checks if the [move route] is being forced.

#### memorizeMoveRoute ()
Records the [move route].

#### moveAwayFromCharacter (character)
Moves away from the specified character.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `character` | [Game_Character](Game_Character.md) | Character |

#### moveAwayFromPlayer ()
Moves away from the player.

#### moveBackward ()
Moves one step backward.

#### moveForward ()
Moves one step forward.

#### moveRandom ()
Moves randomly [Type: Random].

#### moveTowardCharacter (character)
Moves closer to the specified character. [Type: Approaching].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `character` | [Game_Character](Game_Character.md) | Character |

#### moveTowardPlayer ()
Moves closer to the player.

#### processMoveCommand (command)
Executes the [move command].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `command` | [RPG.MoveCommand](RPG.MoveCommand.md) | [move command] |

#### processRouteEnd ()
Ends the [move route].

#### restoreMoveRoute ()
Restores to the recorded [move route].

#### searchLimit () → {[Number](Number.md)}
Returns the limit number for route searches.

#### setMoveRoute (moveRoute)
Sets the [move route].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `moveRoute` | [RPG.MoveRoute](RPG.MoveRoute.md) | [move route] |

#### swap (character)
Swaps positions with the specified character.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `character` | [Game_Character](Game_Character.md) | Character |

#### turn180 ()
Turns 180 degrees.

#### turnAwayFromCharacter (character)
Turns away from the specified character.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `character` | [Game_Character](Game_Character.md) | Character |

#### turnAwayFromPlayer ()
Turns away from the player.

#### turnLeft90 ()
Turns left 90 degrees.

#### turnRandom ()
Turns in a random direction.

#### turnRight90 ()
Turns right 90 degrees.

#### turnRightOrLeft90 ()
Turns right or left 90 degrees.

#### turnTowardCharacter (character)
Faces toward the specified character.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `character` | [Game_Character](Game_Character.md) | Character |

#### turnTowardPlayer ()
Faces toward the player.

#### updateRoutineMove ()
Updates the [move route].

#### updateStop ()
Override: [Game_CharacterBase](Game_CharacterBase.md#updatestop-)
