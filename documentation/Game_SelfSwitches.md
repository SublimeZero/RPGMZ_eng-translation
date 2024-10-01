[Class Tree](index.md)

# Class: Game_SelfSwitches

| Global Variable | Save Data |
| --- | --- |
| [$gameSelfSwitches](global.md#gameselfswitches-game_selfswitches) | Saved |

A class for handling [self switches] used in condition evaluations for [event pages].

Related Classes: [Game_Variables](Game_Variables.md), [Game_Switches](Game_Switches.md), [RPG.EventPage](RPG.EventPage.md), [RPG.EventPage.Conditions](RPG.EventPage.Conditions.md), [RPG.BattleEventPage](RPG.BattleEventPage.md), [RPG.BattleEventPage.Conditions](RPG.BattleEventPage.Conditions.md)

### new Game_SelfSwitches ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_data` | Object | Shape of { [MV.SelfSwitch](MV.SelfSwitch.md): Boolean, …} |


### Methods

#### clear ()
Initializes the [self switch] data.


#### initialize ()
Initialization at the time of object creation.


#### onChange ()
Handler called when a switch changes. <br />
(Reserves map rewriting)


#### setValue (key, value)
Sets the value for the specified [self switch].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `key` | [MV.SelfSwitch](MV.SelfSwitch.md)  | The specified key of the [self switch] |
| `value` | Boolean | Whether the switch is ON |


#### value (key) → {Boolean}
Checks if the value of the specified key is ON.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `key` | [MV.SelfSwitch](MV.SelfSwitch.md)  | The specified key of the [self switch] |
