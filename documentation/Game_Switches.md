[Class Tree](index.md)

# Class: Game_Switches

| Global Variable | Save Data |
| --- | --- |
| [$gameSwitches](global.md#gameswitches-game_switches) | Saved |

A class for handling [switches] used in condition evaluations.

Switches are managed by ID, but strings also exist in the switches property of [RPG.System](RPG.System.md) ([$dataSystem](global.md#datasystem-rpgsystem)).

Related Classes: [Game_Variables](Game_Variables.md), [Game_SelfSwitches](Game_SelfSwitches.md) 

### new Game_Switches ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_data` | [Array](Array.md).<Boolean> | An array of boolean values |


### Methods

#### clear ()
Initializes the values.


#### initialize ()
Initialization at the time of object creation.


#### onChange ()
Handler called when a switch changes.
(Reserves map rewriting)


#### setValue (switchId, value)
Sets the value for the specified [switch].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `switchId` | [Number](Number.md) | Switch ID |
| `value` | Boolean | Whether the switch is ON |


#### value (switchId)
Returns the value of the specified [switch].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `switchId` | [Number](Number.md) | Switch ID |
