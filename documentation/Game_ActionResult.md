[Class Tree](index.md)

# Class: Game_ActionResult

An object that describes the result of a [Game_Action](Game_Action.md).

### new Game_ActionResult ()

### Properties

| Name             | Type                                                        | Description                              |
| ---------------- | ----------------------------------------------------------- | ---------------------------------------- |
| `used`           | Boolean                                                    | Whether it was used                     |
| `missed`         | Boolean                                                    | Whether it missed                       |
| `evaded`         | Boolean                                                    | Whether it was [evaded]                |
| `physical`       | Boolean                                                    | Whether it was a [physical attack]      |
| `drain`          | Boolean                                                    | Whether it was a [drain]                |
| `critical`       | Boolean                                                    | Whether it was [critical]               |
| `success`        | Boolean                                                    | Whether it was successful                |
| `hpAffected`     | Boolean                                                    | Whether there was a change in HP       |
| `hpDamage`       | [Number](Number.md)                                       | Amount of HP damage                     |
| `mpDamage`       | [Number](Number.md)                                       | Amount of MP damage                     |
| `tpDamage`       | [Number](Number.md)                                       | Amount of TP damage                     |
| `addedStates`    | [Array](Array.md).&lt;[Number](Number.md)&gt;           | Array of added [states]                 |
| `removedStates`  | [Array](Array.md).&lt;[Number](Number.md)&gt;           | Array of removed [states]               |
| `addedBuffs`     | [Array](Array.md).&lt;[Number](Number.md)&gt;           | Array of added [buffs]                  |
| `addedDebuffs`   | [Array](Array.md).&lt;[Number](Number.md)&gt;           | Array of added [debuffs]                |
| `removedBuffs`   | [Array](Array.md).&lt;[Number](Number.md)&gt;           | Array of removed [buffs] and [debuffs]  |

### Methods

#### addedStateObjects () → {[Array](Array.md).<[RPG.State](RPG.State.md)>}
Returns an array of added [states].

#### clear ()
Clears the result information.

#### initialize ()
Initialization upon object creation.

#### isBuffAdded (paramId) → {Boolean}
Checks if a [buff] was added to the specified parameter.

##### Arguments

| Name      | Type                | Description                        |
| --------- | ------------------- | ---------------------------------- |
| `paramId` | [Number](Number.md) | [Parameter ID](RPG.Enemy.md#parameter-id) |

#### isBuffRemoved (paramId) → {Boolean}
Checks if a [buff] was removed from the specified parameter.

##### Arguments

| Name      | Type                | Description                        |
| --------- | ------------------- | ---------------------------------- |
| `paramId` | [Number](Number.md) | [Parameter ID](RPG.Enemy.md#parameter-id) |

#### isDebuffAdded (paramId) → {Boolean}
Checks if a [debuff] was added to the specified parameter.

##### Arguments

| Name      | Type                | Description                        |
| --------- | ------------------- | ---------------------------------- |
| `paramId` | [Number](Number.md) | [Parameter ID](RPG.Enemy.md#parameter-id) |

#### isHit () → {Boolean}
Checks if the attack hit.

#### isStateAdded (stateId) → {Boolean}
Checks if the specified state was added.

##### Arguments

| Name      | Type                | Description                        |
| --------- | ------------------- | ---------------------------------- |
| `stateId` | [Number](Number.md) | [State ID](RPG.State.md#state-id) |

#### isStateRemoved (stateId) → {Boolean}
Checks if the specified state was removed.

##### Arguments

| Name      | Type                | Description                        |
| --------- | ------------------- | ---------------------------------- |
| `stateId` | [Number](Number.md) | [State ID](RPG.State.md#state-id) |

#### isStatusAffected () → {Boolean}
Checks if the specified state took effect.

#### pushAddedBuff (paramId)
Adds a [buff] addition for the specified parameter.

##### Arguments

| Name      | Type                | Description                        |
| --------- | ------------------- | ---------------------------------- |
| `paramId` | [Number](Number.md) | [Parameter ID](RPG.Enemy.md#parameter-id) |

#### pushAddedDebuff (paramId)
Adds a [debuff] addition for the specified parameter.

##### Arguments

| Name      | Type                | Description                        |
| --------- | ------------------- | ---------------------------------- |
| `paramId` | [Number](Number.md) | [Parameter ID](RPG.Enemy.md#parameter-id) |

#### pushAddedState (stateId)
Adds a [state] addition for the specified state.

##### Arguments

| Name      | Type                | Description                        |
| --------- | ------------------- | ---------------------------------- |
| `stateId` | [Number](Number.md) | [State ID](RPG.State.md#state-id) |

#### pushRemovedBuff (paramId)
Adds a [buff] removal for the specified parameter.

##### Arguments

| Name      | Type                | Description                        |
| --------- | ------------------- | ---------------------------------- |
| `paramId` | [Number](Number.md) | [Parameter ID](RPG.Enemy.md#parameter-id) |

#### pushRemovedState (stateId)
Adds a [state] removal for the specified state.

##### Arguments

| Name      | Type                | Description                        |
| --------- | ------------------- | ---------------------------------- |
| `stateId` | [Number](Number.md) | [State ID](RPG.State.md#state-id) |

#### removedStateObjects () → {[Array](Array.md).<[RPG.State](RPG.State.md)>}
Returns an array of removed states.
