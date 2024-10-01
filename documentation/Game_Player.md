[Class Tree](index.md)

# Class: Game_Player

## Superclass: [Game_Character](Game_Character.md)

| Database | Global Variable | Save Data | JSON Data | Sprite |
| --- | --- | --- | --- | --- |
| [Player] | [$gamePlayer](global.md#gameplayer-game_player) | Saved | [RPG.Actor](RPG.Actor.md) | [Sprite_Character](Sprite_Character.md) |

A class that defines the player character (including vehicles). It also includes processing for [location movement] on the map.<br />
Note that JSON data requires looking at the `$gameParty.leader()` method in the [Game_Party](Game_Party.md) class.

Changes were made in v1.1.0 and v1.2.0.

Main Path
```js
$gamePlayer
```
The path used when writing [Script] event commands with the [Game_Interpreter.character()](Game_Interpreter.md#character-param--game_character) method.
```js
this.character(-1)
```

Related Classes: [Game_Vehicle](Game_Vehicle.md), [Game_Event](Game_Event.md), [Game_Map](Game_Map.md)

### new Game_Player ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_vehicleType` | [String](String.md) | Type of [vehicle] |
| `_vehicleGettingOn` | Boolean | Whether the player is getting on a [vehicle] |
| `_vehicleGettingOff` | Boolean | Whether the player is getting off a [vehicle] |
| `_dashing` | Boolean | Whether the player is dashing |
| `_needsMapReload` | Boolean | Whether a map reload is needed |
| `_transferring` | Boolean | Whether the player is transferring between maps |
| `_newMapId` | [Number](Number.md) | ID of the new map to move to |
| `_newX` | [Number](Number.md) | X position on the new map (in tiles) |
| `_newY` | [Number](Number.md) | Y position on the new map (in tiles) |
| `_newDirection` | [Number](Number.md) | Direction upon arrival at the new location (numeric keypad) |
| `_fadeType` | [Number](Number.md) | Type of [fade](#fade-types) |
| `_followers` | [Game_Followers](Game_Followers.md) | Followers in the party |
| `_encounterCount` | [Number](Number.md) | Encounter count |

#### Fade Types

| Number | Description |
| --- | --- |
| 0 | Black |
| 1 | White |
| 2 | None |

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
* [checkEventTriggerTouchFront (d)](Game_CharacterBase.md#checkeventtriggertouchfront-d)
* [checkStop (threshold)](Game_CharacterBase.md#checkstop-threshold--boolean)
* [copyPosition (character)](Game_CharacterBase.md#copyposition-character)
* [direction ()](Game_CharacterBase.md#direction---number)
* [distancePerFrame ()](Game_CharacterBase.md#distanceperframe---number)
* [endAnimation ()](Game_CharacterBase.md#endanimation-)
* [endBalloon ()](Game_CharacterBase.md#endballoon-)
* [hasStepAnime ()](Game_CharacterBase.md#hasstepanime---boolean)
* [hasWalkAnime ()](Game_CharacterBase.md#haswalkanime---boolean)
* [isAnimationPlaying ()](Game_CharacterBase.md#isanimationplaying---boolean)
* [isBalloonPlaying ()](Game_CharacterBase.md#isballoonplaying---boolean)
* [isCollidedWithCharacters (x, y)](Game_CharacterBase.md#iscollidedwithcharacters-x-y--boolean)
* [isCollidedWithEvents (x, y)](Game_CharacterBase.md#iscollidedwithevents-x-y--boolean)
* [isCollidedWithVehicles (x, y)](Game_CharacterBase.md#iscollidedwithvehicles-x-y--boolean)
* [isDirectionFixed ()](Game_CharacterBase.md#isdirectionfixed---boolean)
* [isJumping ()](Game_CharacterBase.md#isjumping---boolean)
* [isMovementSucceeded (x opt, y opt)](Game_CharacterBase.md#ismovementsucceeded-x-opt-y-opt--boolean)
* [isMoving ()](Game_CharacterBase.md#ismoving---boolean)
* [isNearTheScreen ()](Game_CharacterBase.md#isnearthescreen---boolean)
* [isNormalPriority ()](Game_CharacterBase.md#isnormalpriority---boolean)
* [isObjectCharacter ()](Game_CharacterBase.md#isobjectcharacter---boolean)
* [isOnBush ()](Game_CharacterBase.md#isonbush---boolean)
* [isOnLadder ()](Game_CharacterBase.md#isonladder---boolean)
* [isOriginalPattern ()](Game_CharacterBase.md#isoriginalpattern---boolean)
* [isThrough ()](Game_CharacterBase.md#isthrough---boolean)
* [isTile ()](Game_CharacterBase.md#istile---boolean)
* [isTransparent ()](Game_CharacterBase.md#istransparent---boolean)
* [jumpHeight ()](Game_CharacterBase.md#jumpheight---number)
* [maxPattern ()](Game_CharacterBase.md#maxpattern---number)
* [moveFrequency ()](Game_CharacterBase.md#movefrequency---number)
* [moveSpeed ()](Game_CharacterBase.md#movespeed---number)
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
* [updateAnimation ()](Game_CharacterBase.md#updateanimation-)
* [updateAnimationCount ()](Game_CharacterBase.md#updateanimationcount-)
* [updateJump ()](Game_CharacterBase.md#updatejump-)
* [updateMove ()](Game_CharacterBase.md#updatemove-)
* [updatePattern ()](Game_CharacterBase.md#updatepattern-)

#### [Game_Character](Game_Character)

* [advanceMoveRouteIndex ()](Game_Character.md#advancemoverouteindex-)
* [deltaXFrom (x)](Game_Character.md#deltaxfrom-x--number)
* [deltaYFrom (y)](Game_Character.md#deltayfrom-y--number)
* [findDirectionTo (goalX, goalY)](Game_Character.md#finddirectionto-goalx-goaly--number)
* [forceMoveRoute (moveRoute)](Game_Character.md#forcemoveroute-moveroute)
* [isMoveRouteForcing ()](Game_Character.md#ismoverouteforcing---boolean)
* [memorizeMoveRoute ()](Game_Character.md#memorizemoveroute-)
* [moveAwayFromCharacter (character)](Game_Character.md#moveawayfromcharacter-character)
* [moveAwayFromPlayer ()](Game_Character.md#moveawayfromplayer-)
* [moveBackward ()](Game_Character.md#movebackward-)
* [moveForward ()](Game_Character.md#moveforward-)
* [moveRandom ()](Game_Character.md#moverandom-)
* [moveTowardCharacter (character)](Game_Character.md#movetowardcharacter-character)
* [moveTowardPlayer ()](Game_Character.md#movetowardplayer-)
* [processMoveCommand (command)](Game_Character.md#processmovecommand-command)
* [processRouteEnd ()](Game_Character.md#processrouteend-)
* [restoreMoveRoute ()](Game_Character.md#restoremoveroute-)
* [searchLimit ()](Game_Character.md#searchlimit---number)
* [setMoveRoute (moveRoute)](Game_Character.md#setmoveroute-moveroute)
* [swap (character)](Game_Character.md#swap-character)
* [turn180 ()](Game_Character.md#turn180-)
* [turnAwayFromCharacter (character)](Game_Character.md#turnawayfromcharacter-character)
* [turnAwayFromPlayer ()](Game_Character.md#turnawayfromplayer-)
* [turnLeft90 ()](Game_Character.md#turnleft90-)
* [turnRandom ()](Game_Character.md#turnrandom-)
* [turnRight90 ()](Game_Character.md#turnright90-)
* [turnRightOrLeft90 ()](Game_Character.md#turnrightorleft90-)
* [turnTowardCharacter (character)](Game_Character.md#turntowardcharacter-character)
* [turnTowardPlayer ()](Game_Character.md#turntowardplayer-)
* [updateRoutineMove ()](Game_Character.md#updateroutinemove-)
* [updateStop ()](Game_Character.md#updatestop-)

  ### Methods

#### areFollowersGathered () → {Boolean}
Checks if the [followers] are gathered.

#### areFollowersGathering () → {Boolean}
Checks if the [followers] are currently gathering.

#### canEncounter () → {Boolean}
Checks if the player can encounter enemies (be in an encounter state).

#### canMove () → {Boolean}
Checks if the player character can be controlled.

#### canStartLocalEvents () → {Boolean}
Checks if surface [events] can be executed. Events cannot be executed while flying in airships, etc.

#### center (x, y)
Displays the map based on the screen center. [Game_Map.setDisplayPos()](Game_Map.md#setDisplayPos-x-y) is based on the top-left corner.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Number of tiles |
| `y` | [Number](Number.md) | Number of tiles |

#### centerX () → {[Number](Number.md)}
Returns the center x-coordinate of the screen (in tiles).

#### centerY () → {[Number](Number.md)}
Returns the center y-coordinate of the screen (in tiles).

#### checkEventTriggerHere (triggers)
Executes the specified [trigger] events at the current location.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `triggers` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of [[triggers]](RPG.EventPage.md#トリガー) |

#### checkEventTriggerThere (triggers)
Executes the specified [trigger] events one step ahead of the current location.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `triggers` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of [[triggers]](RPG.EventPage.md#トリガー) |

#### checkEventTriggerTouch (x, y) → {Boolean}
Override: [Game_CharacterBase](Game_CharacterBase.md#checkeventtriggertouch-x-y--boolean)

#### clearTransferInfo ()
Clears [transfer] information.

#### encounterProgressValue () → {[Number](Number.md)}
Returns the countdown value for [encounter] occurrences. This may decrease in certain conditions, such as using skills or being on a ship.<br />
Densities in the [bushes] setting can double this value (making it easier to encounter enemies).

#### executeEncounter () → {Boolean}
Executes an encounter and returns whether it was successful.

#### executeMove (direction)
Moves forward one step in the specified direction.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `direction` | [Number](Number.md) | Direction (numeric keypad compatible) |

#### fadeType () → {[Number](Number.md)}
Returns the [fade type](#fade-types) during [transfer].

#### followers () → {[Game_Followers](Game_Followers.md)}
Returns the [followers].

#### forceMoveForward ()
Forcibly moves the player character forward.

#### gatherFollowers ()
Gathers the [followers].

#### getInputDirection () → {[Number](Number.md)}
Returns the direction inputted (numeric keypad compatible).

#### getOffVehicle () → {Boolean}
Gets off the [vehicle] and returns whether it was successful.

#### getOnOffVehicle () → {Boolean}
Executes getting on or off a [vehicle]. Gets off if already on, and gets on if currently off.

#### getOnVehicle () → {Boolean}
Gets on the [vehicle] and returns whether it was successful.

#### hideFollowers ()
Prevents [followers] from walking.

#### isCollided (x, y) → {Boolean}
Checks if the specified position is impassable.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | Number of tiles |
| `y` | [Number](Number.md) | Number of tiles |

#### increaseSteps ()
Override: [Game_CharacterBase](Game_CharacterBase.md#increasesteps-)

#### initialize ()
Override: [Game_CharacterBase](Game_CharacterBase.md#initialize-)

#### initMembers ()
Override: [Game_CharacterBase](Game_CharacterBase.md#initmembers-)

#### isDashButtonPressed () → {Boolean}
Checks if the dash button (Shift) is pressed.

#### isDashing () → {Boolean}
Override: [Game_CharacterBase](Game_CharacterBase.md#isdashing---boolean)

#### isDebugThrough () → {Boolean}
Override: [Game_CharacterBase](Game_CharacterBase.md#isdebugthrough---boolean)

#### isInAirship () → {Boolean}
Checks if the player is in an [airship].

#### isInBoat () → {Boolean}
Checks if the player is in a [small boat].

#### isInShip () → {Boolean}
Checks if the player is in a [large ship].

#### isInVehicle () → {Boolean}
Checks if the player is in a [vehicle].

#### isMapPassable (x, y, d) → {Boolean}
Override: [Game_CharacterBase](Game_CharacterBase.md#ismappassable-x-y-d--boolean)

#### isNormal () → {Boolean}
Checks if the player is in walking state and not being forcibly moved.

#### isOnDamageFloor () → {Boolean}
Checks if the player is on a [damage floor].

#### isStopping () → {Boolean}
Override: [Game_CharacterBase](Game_CharacterBase.md#isstopping---boolean)

#### isTransferring () → {Boolean}
Checks if the player is currently [transferring].

#### jump (xPlus, yPlus)
Override: [Game_CharacterBase](Game_CharacterBase.md#jump-xplus-yplus)

#### locate (x, y)
Override: [Game_CharacterBase](Game_CharacterBase.md#locate-x-y)

#### makeEncounterCount ()
Sets the count until the next [encounter].

#### makeEncounterTroopId () → {[Number](Number.md)}
Generates and returns the enemy group ID for the next [encounter].

#### meetsEncounterConditions (encounter) → {Boolean}
*Please let me know the meaning of this term if you understand it.*

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `encounter` | [RPG.Map.Encounter](RPG.Map.Encounter.md) |  |

#### moveByInput ()
Moves according to input.

#### moveDiagonally (horz, vert)
Override: [Game_CharacterBase](Game_CharacterBase.md#movediagonally-horz-vert)

#### moveStraight (d)
Override: [Game_CharacterBase](Game_CharacterBase.md#movestraight-d)

#### newMapId () → {[Number](Number.md)}
Returns the ID of the map to be moved to.

#### performTransfer ()
Executes [transfer].

#### refresh ()
Updates the player character.

#### requestMapReload ()
Requests the map to be reloaded.

#### reserveTransfer (mapId, x, y, d opt, fadeType opt)
Reserves [transfer] with the specified values.

##### Arguments

| Name | Type | Traits | Description |
| --- | --- | --- | --- |
| `mapId` | [Number](Number.md) |  | Map ID |
| `x` | [Number](Number.md) |  | x position on the map (in tiles) |
| `y` | [Number](Number.md) |  | y position on the map (in tiles) |
| `d` | [Number](Number.md) | <optional> | Direction (numeric keypad compatible) |
| `fadeType` | [Number](Number.md) | <optional> | [Fade type](#fade-types) |

#### setupForNewGame ()
**@MZ** Prepares for a new game (sets up the map and coordinates).

#### showFollowers ()
Enables [followers] to walk.

#### startMapEvent (x, y, triggers, normal)
Starts the [event] corresponding to the specified position and [trigger].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position on the map (in tiles) |
| `y` | [Number](Number.md) | y position on the map (in tiles) |
| `triggers` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of [[triggers]](RPG.EventPage.md#トリガー) |
| `normal` | Boolean |  |

#### triggerAction () → {Boolean}
Executes an action corresponding to the [decision button] [trigger] and returns whether the action was performed.

#### triggerButtonAction () → {Boolean}
Executes the action corresponding to the decision button and returns whether the action was performed.

#### triggerTouchAction () → {Boolean}
Executes an action based on screen touch (click) and returns whether the action was performed.

#### triggerTouchActionD1 (x1, y1) → {Boolean}
*Please let me know the meaning of this term if you understand it.*

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x1` | [Number](Number.md) |  |
| `y1` | [Number](Number.md) |  |

#### triggerTouchActionD2 (x2, y2) → {Boolean}
*Please let me know the meaning of this term if you understand it.*

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x2` | [Number](Number.md) |  |
| `y2` | [Number](Number.md) |  |

#### triggerTouchActionD3 (x2, y2) → {Boolean}
*Please let me know the meaning of this term if you understand it.*

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x2` | [Number](Number.md) |  |
| `y2` | [Number](Number.md) |  |

#### update ()
Override: [Game_CharacterBase](Game_CharacterBase.md#update-)

#### updateDashing ()
Updates the dash state.

#### updateEncounterCount ()
Updates the count for [encounter].

#### updateNonmoving (wasMoving)
Updates the movement state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `wasMoving` | Boolean | (true: moved, false: stopped) |

#### updateScroll (lastScrolledX, lastScrolledY)
Handles scrolling.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `lastScrolledX` | [Number](Number.md) |  |
| `lastScrolledY` | [Number](Number.md) |  |

#### updateVehicle ()
Updates the [vehicle].

#### updateVehicleGetOff ()
Updates the state of getting off the [vehicle].

#### updateVehicleGetOn ()
Updates the state of getting on the [vehicle].

#### vehicle () → {[Game_Vehicle](Game_Vehicle.md)}
Returns the [vehicle].
