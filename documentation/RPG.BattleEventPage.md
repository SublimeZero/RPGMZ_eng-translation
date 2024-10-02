[Class Tree](index.md)

# Class: [RPG](RPG.md).BattleEventPage
JSON data that constitutes the [EV page] of [RPG.Troop](RPG.Troop.md).

Related Class: [RPG.EventPage](RPG.EventPage.md)

### Properties

| Identifier    | Type                                                  | Description                      |
|---------------|-------------------------------------------------------|----------------------------------|
| `conditions`  | [RPG.BattleEventPage.Conditions](RPG.BattleEventPage.Conditions.md) | [conditions]                     |
| `list`        | [Array](Array.md).&lt;[RPG.EventCommand](RPG.EventCommand.md)&gt; | [execution content]              |
| `span`        | [Number](Number.md)                                  | [[span]](RPG.BattleEventPage.md#span) |

#### [Span]

| Number | [Span]       |
|--------|--------------|
| 0      | Battle       |
| 1      | Turn         |
| 2      | Moment       |

### Inner Class

* [RPG.BattleEventPage.Conditions](RPG.BattleEventPage.Conditions.md)
