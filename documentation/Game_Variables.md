[Class Tree](index.md)

# Class: Game_Variables

| Global Variables | Save Data |
| --- | --- |
| [$gameVariables](global.md#gamevariables-game_variables) | Saved |

A class for handling [variables] used in condition checks.

Variables are managed by ID, but the `variables` property of [RPG.System](RPG.System.md) ([$dataSystem](global.md#datasystem-rpgsystem)) also contains strings of variable names.

Related classes: [Game_Switches](Game_Switches.md), [Game_SelfSwitches](Game_SelfSwitches.md)

### new Game_Variables ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_data` | [Array](Array.md).&lt;[Number](Number.md)&gt; | An array of variable values |


### Methods

#### clear ()
Initializes the values.


#### initialize ()
Initialization during object creation.


#### onChange ()
Handler called when a variable changes. <br />
(Reserves a check for [event] [appearance conditions])


#### setValue (variableId, value)
Sets the value of the specified [variable]. <br />
The `value` can be set to non-numeric values, but if a falsy value like an empty string ("") is set, it will return 0 when retrieved using [value ()](#value-variableid--).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `variableId` | [Number](Number.md) | Variable ID |
| `value` | * | Value |


#### value (variableId) → {*}
Returns the value of the specified [variable].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `variableId` | [Number](Number.md) | Variable ID |
