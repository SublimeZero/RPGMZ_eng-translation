[Class Tree](index.md)

# Class: [RPG](RPG.md).[EventPage](RPG.EventPage.md).Conditions
JSON data that constitutes the [appearance conditions] of the event's [EV page].<br/>
Included in the conditions property of [RPG.EventPage](RPG.EventPage.md).

Related classes: [RPG.CommonEvent](RPG.CommonEvent.md), [RPG.BattleEventPage.Conditions](RPG.BattleEventPage.Conditions.md)

### Properties

| Identifier           | Type               | Description                              |
|---------------------|--------------------|------------------------------------------|
| `switch1Valid`      | Boolean            | Whether to use the first [switch]       |
| `switch1Id`         | [Number](Number.md) | ID of the first [switch]                |
| `switch2Valid`      | Boolean            | Whether to use the second [switch]      |
| `switch2Id`         | [Number](Number.md) | ID of the second [switch]               |
| `variableValid`     | Boolean            | Whether to use a [variable]             |
| `variableId`        | [Number](Number.md) | ID of the [variable]                    |
| `variableValue`     | [Number](Number.md) | Value of the [variable]                 |
| `selfSwitchValid`   | Boolean            | Whether to use a [self switch]          |
| `selfSwitchCh`      | [String](String.md) | Symbol of the [self switch] (A, B, C, D) |
| `itemValid`         | Boolean            | Whether to use an [item]                |
| `itemId`            | [Number](Number.md) | ID of the [item]                        |
| `actorValid`        | Boolean            | Whether to use an [actor]               |
| `actorId`           | [Number](Number.md) | ID of the [actor]                       |
