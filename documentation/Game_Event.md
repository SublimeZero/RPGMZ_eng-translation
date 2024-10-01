[Class Tree](index.md)

# Class: Game_Event

## Superclass: [Game_Character](Game_Character.md)

| Database | JSON Data | Sprite |
| --- | --- | --- |
| [Event] | [RPG.Event](RPG.Event.md) | [Sprite_Character](Sprite_Character.md) |

An object that defines the [events] placed on the map.

Includes methods such as [Game_Event.event()](Game_Event.md#event---rpgevent) that return [RPG.Event](RPG.Event.md).

Additionally, methods added by the official plugin PluginCommonBase.js are also described.

Main Path
```js
$gameMap.event( eventId )
```
A path that uses the [Game_Interpreter.character()](Game_Interpreter.md#character-param--game_character) method when writing in a [Script] event command.

```js
this.character( eventId )
this.character( 0 ) // The event itself where the [Script] event command is written
```

Related Class: [Game_Map](Game_Map.md)

### new Game_Event ()

### Properties

| Identifier          | Type                                 | Description                                            |
| ------------------- | ------------------------------------ | ------------------------------------------------------ |
| `_mapId`            | [Number](Number.md)                  | Map ID                                                 |
| `_eventId`          | [Number](Number.md)                  | Event ID                                               |
| `_moveType`         | [Number](Number.md)                  | [Autonomous movement type](RPG.EventPage.md#自律移動のタイプ) |
| `_trigger`          | [Number](Number.md)                  | [Trigger](RPG.EventPage.md#トリガー)                   |
| `_starting`         | Boolean                              | Whether the event has started                          |
| `_erased`           | Boolean                              | Whether the event has been erased                      |
| `_pageIndex`        | [Number](Number.md)                  | Page number                                            |
| `_originalPattern`  | [Number](Number.md)                  | Original pattern                                       |
| `_originalDirection`| [Number](Number.md)                  | Original direction                                     |
| `_prelockDirection` | [Number](Number.md)                  | Previously locked direction                            |
| `_locked`           | Boolean                              | Whether it is locked                                   |
| `_interpreter`      | [Game_Interpreter](Game_Interpreter.md) | Command interpreter                                   |

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
* [isStopping ()](Game_CharacterBase.md#isstopping---boolean)
* [isThrough ()](Game_CharacterBase.md#isthrough---boolean)
* [isTile ()](Game_CharacterBase.md#istile---boolean)
* [isTransparent ()](Game_CharacterBase.md#istransparent---boolean)
* [jump (xPlus, yPlus)](Game_CharacterBase.md#jump-xplus-yplus)
* [jumpHeight ()](Game_CharacterBase.md#jumpheight---number)
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

### Methods

#### checkEventTriggerAuto ()
Executes [event] with [trigger: auto-execute].

#### checkEventTriggerTouch (x, y)
Overrides: [Game_Character](Game_Character.md#checkeventtriggertouch-x-y--boolean)

#### clearPageSettings ()
Clears the settings of the [event page](RPG.EventPage).

#### clearStartingFlag ()
Clears the starting flag for the [event].

#### erase ()
Erases the [event].

#### event () → {[RPG.Event](RPG.Event.md)}
Returns the [event] information object.

#### eventId () → {[Number](Number.md)}
Returns the event ID.

#### findProperPageIndex () → {[Number](Number.md)}
Returns the page number of the event that matches [appearance conditions] (-1 if not found).

#### (static) findMeta (metaNames) → {*}
**@MZ PluginCommonBase.js**  
Returns the value of the metadata in the memo field of this event.

##### Parameters

| Name        | Type                                              | Description          |
| ----------- | ------------------------------------------------- | -------------------- |
| `metaNames` | [Array](Array.md).&lt;[String](String.md)&gt; \| [String](String.md) | Tag name (or array)   |

#### forceMoveRoute (moveRoute)
Overrides: [Game_Character](Game_Character.md#forcemoveroute-moveroute)

#### initialize ()
Overrides: [Game_Character](Game_Character.md#initialize-)

#### initMembers ()
Overrides: [Game_Character](Game_Character.md#initmembers-)

#### isCollidedWithCharacters (x, y) → {Boolean}
Overrides: [Game_CharacterBase](Game_CharacterBase.md#iscollidedwithcharacters-x-y--boolean)

#### isCollidedWithEvents (x, y) → {Boolean}
Overrides: [Game_CharacterBase](Game_CharacterBase.md#iscollidedwithevents-x-y--boolean)

#### isCollidedWithPlayerCharacters (x, y) → {Boolean}
Checks if the specified position is blocked by player characters.

##### Parameters

| Name | Type               | Description    |
| ---- | ------------------ | -------------- |
| `x`  | [Number](Number.md) | Tile count     |
| `y`  | [Number](Number.md) | Tile count     |

#### isNearThePlayer () → {Boolean}
Checks if it is near the player character.

#### isOriginalPattern () → {Boolean}
Overrides: [Game_CharacterBase](Game_CharacterBase.md#isoriginalpattern---boolean)

#### isStarting () → {Boolean}
Checks if the [event] has started.

#### isTriggerIn (triggers) → {Boolean}
Checks if the [trigger] of this [event] is included in the specified array.

##### Parameters

| Name      | Type                                              | Description                                      |
| --------- | ------------------------------------------------- | ------------------------------------------------ |
| `triggers`| [Array](Array.md).&lt;[Number](Number.md)&gt;     | Array of [triggers](RPG.EventPage.md#トリガー)     |

#### list () → {[Array](Array.md).&lt;[RPG.EventCommand](RPG.EventCommand.md)&gt;}
Returns the array of [event commands] of the current [event page](RPG.EventPage).

#### locate (x, y)
Overrides: [Game_CharacterBase](Game_CharacterBase.md#locate-x-y)

#### lock ()
Locks the event to face the player.

#### meetsConditions (page) → {Boolean}
Checks if the [appearance conditions] of the specified page are met.

##### Parameters

| Name   | Type                                 | Description |
| ------ | ------------------------------------ | ----------- |
| `page` | [RPG.EventPage](RPG.EventPage.md)    | Event page  |

#### moveTypeCustom ()
Moves with [type: custom].

#### moveTypeRandom ()
Moves with [type: random].

#### moveTypeTowardPlayer ()
Moves with [type: move toward player].

#### page () → {[RPG.EventPage](RPG.EventPage.md)}
Returns the information object of the current [event page].

#### refresh ()
Refreshes the [event].

#### resetPattern ()
Overrides: [Game_CharacterBase](Game_CharacterBase.md#resetpattern-)

#### setupPage ()
Sets up the [event page](RPG.EventPage).

#### setupPageSettings ()
Sets up the settings of the [event page](RPG.EventPage).

#### start ()
Starts the [execution content].

#### stopCountThreshold () → {[Number](Number.md)}
Returns the stop count threshold, which varies by [frequency].

#### unlock ()
Unlocks the event from facing the player.

#### update ()
Overrides: [Game_CharacterBase](Game_CharacterBase.md#update-)

#### updateParallel ()
Updates [trigger: parallel processing].

#### updateSelfMovement ()
Updates [autonomous movement].

#### updateStop ()
Overrides: [Game_Character](Game_Character.md#updatestop-)
