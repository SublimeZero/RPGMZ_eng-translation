[Class Tree](index.md)

# Class: [RPG](RPG.md).EventCommand
JSON data that constitutes the [event command] described in the [execution content].

The described content is processed by the commandXXX methods of [Game_Interpreter](Game_Interpreter.md).

Related classes: [RPG.EventPage](RPG.EventPage.md), [RPG.BattleEventPage](RPG.BattleEventPage.md), [RPG.CommonEvent](RPG.CommonEvent.md)

### Properties

| Identifier  | Type                                    | Description                                                                                |
|-------------|-----------------------------------------|--------------------------------------------------------------------------------------------|
| `code`      | [Number](Number.md)                    | Event number                                                                               |
| `indent`    | [Number](Number.md)                    | Depth of hierarchy (indentation)<br />(Usually 0, and becomes deeper by 1 level with [conditional branch] commands) |
| `parameters` | [Array](Array.md).&lt;*&gt;           | Array of [arguments passed to the command](#arguments-passed-to-the-command)              |

#### Arguments Passed to the Command
The content of `parameters` varies for each command.

Refer to the table compiled by Triacontane for details.

[RPG Maker MZ Script Reference](https://docs.google.com/spreadsheets/d/1aqY-xzFqT0vnZE-OkfsMYsP9Ud91vWTrBLU-uDkJ-Ls/edit#gid=2095105278)

##### Note
In the plugin command (`Command357()`), the argument `parameters[0]` contains the path to the plugin.<br />
Since version 1.3.0, it includes not only the plugin name but also the folder name and separator.
