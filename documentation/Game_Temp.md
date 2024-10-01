[Class Tree](index.md)

# Class: Game_Temp

| Global Variables |
| --- |
| [$GameTemp](global.md#gametemp-game_temp) |

A class that holds temporary data for the game.

Changes were made in v1.4.0.

Related Classes: [Game_CommonEvent](Game_CommonEvent.md), [Spriteset_Base](Spriteset_Base.md), [Spriteset_Map](Spriteset_Map.md), [Sprite_Destination](Sprite_Destination.md),

### new Game_Temp ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_isPlaytest` | Boolean | Is it a playtest? |
| `_destinationX` | [Number](Number.md) | The x position of the touch movement target (in tiles) |
| `_destinationY` | [Number](Number.md) | The y position of the touch movement target (in tiles) |
| `_touchTarget` | Object | **@MZ** The touch target |
| `_touchState` | [String](String.md) | **@MZ** The touch state |
| `_needsBattleRefresh` | Boolean | **@MZ** Does it need a battle refresh? |
| `_commonEventQueue` | [Array](Array.md).&lt;[Number](Number.md)&gt; | **@MZ** Common event queue |
| `_animationQueue` | [Array](Array.md).&lt;[MV.AnimationRequest](MV.AnimationRequest.md)&gt; | **@MZ** Animation queue |
| `_balloonQueue` | [Array](Array.md).&lt;[MV.BalloonRequest](MV.BalloonRequest.md)&gt; | **@MZ** Balloon queue |
| `_lastActionData` | [Array](Array.md).&lt;[Number](Number.md)&gt; | **@MZ** Last action data |

#### Action Types
The action type is saved corresponding to the index of the `_lastActionData` array.

| Number | Description |
| --- | ---|
| 0 | Skill ID |
| 1 | Item ID |
| 2 | Actor ID who acted |
| 3 | Enemy ID who acted |
| 4 | Actor ID targeted |
| 5 | Enemy ID targeted |

### Deprecated MV Properties
`_commonEventId`

### Methods

#### clearBattleRefreshRequest () 
**@MZ** Clears the request for a battle refresh.

#### clearCommonEventReservation ()
**@MZ 1.4.0** Clears the temporarily saved [common event].

#### clearDestination ()
Clears the player's touch movement target data.

#### clearTouchState ()
**@MZ** Clears the touch state.

#### destinationX () → {[Number](Number.md)}
Returns the x position of the touch movement target (in tiles).

#### destinationY () → {[Number](Number.md)}
Returns the y position of the touch movement target (in tiles).

#### initialize ()
Initialization when creating the object.

#### isBattleRefreshRequested () → {Boolean}
**@MZ** Is a battle refresh requested?

#### isCommonEventReserved () → {Boolean}
Is a [common event] reserved?

#### isDestinationValid () → {Boolean}
Is the touch movement target valid?

#### isPlaytest () → {Boolean}
Is it in playtest mode?

#### lastActionData (type) → {Object}
**@MZ** Returns the last action of the specified type.

##### Arguments

| Name | Type |  Description |
| --- | --- | --- |
| `type` | [Number](Number.md)  | [Action Type](#action-types) |

#### reserveCommonEvent (commonEventId)
Holds the specified [common event] for later processing.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `commonEventId` | [Number](Number.md) | Common event ID |

#### requestBattleRefresh () 
**@MZ** Requests a battle refresh.

#### requestAnimation (targets, animationId, mirror opt)
**@MZ** Requests an animation.

##### Arguments

| Name | Type | Properties | Description |
| --- | --- | --- | --- |
| `targets` | [Array](Array.md).&lt;[Game_Character](Game_Character.md)&gt; | | Targets |
| `animationId` | [Number](Number.md) | | Animation ID |
| `mirror` | Boolean | &lt;optional&gt;  | Should it mirror (default: false) |

#### requestBalloon (target, balloonId)
**@MZ** Requests the display of a balloon.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Character](Game_Character.md) | Target |
| `balloonId` | [Number](Number.md) | Balloon ID |

#### retrieveAnimation () → {[MV.AnimationRequest](MV.AnimationRequest.md)}
**@MZ** Returns the registered animation settings.

#### retrieveBalloon () → {[MV.BalloonRequest](MV.BalloonRequest.md)}
**@MZ** Returns the registered balloon settings.

#### retrieveCommonEvent () → {[Number](Number.md)}
**@MZ** Returns the registered common event ID.|

#### setDestination (x, y)
Sets the position of the touch movement target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `y` | [Number](Number.md) | y position (in tiles) |

#### setLastActionData (type, value)
**@MZ** Sets the last action data.
Action data corresponds to the ID of the action type.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `type` | [Number](Number.md) | [Action Type](#action-types) |
| `value` | [Number](Number.md) | Action data |

#### setLastSubjectActorId (actorID)
**@MZ** Sets the last actor who acted.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actorID` | [Number](Number.md) | Actor ID |

#### setLastSubjectEnemyIndex (enemyIndex)
**@MZ** Sets the index of the last enemy who acted.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `enemyIndex` | [Number](Number.md) | Enemy index |

#### setLastTargetActorId (actorID)
**@MZ** Sets the last actor who was targeted.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actorID` | [Number](Number.md) | Actor ID |

#### setLastTargetEnemyIndex (enemyIndex)
**@MZ** Sets the index of the last enemy who was targeted.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `enemyIndex` | [Number](Number.md) | Enemy index |

#### setLastUsedSkillId (skillID)
**@MZ** Sets the last used skill.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `skillID` | [Number](Number.md) | Skill ID |

#### setLastUsedItemId (itemID)
**@MZ** Sets the last used item.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `itemID` | [Number](Number.md) | Item ID |

#### setTouchState (target, state)
**@MZ** Sets the touch state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | Object | Target |
| `state` | [String](String.md) | Touch state |

#### touchTarget () → {Object}
**@MZ** Returns the touch target.

#### touchState () → {[String](String.md)}
**@MZ** Returns the touch state.

### Deprecated MV Methods
clearCommonEvent (), reservedCommonEvent ()
