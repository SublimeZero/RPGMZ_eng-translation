[Class Tree](index.md)

# Class: [RPG](RPG.md).CommonEvent

| Database        | JSON File          | Global Variable                           | Object                     |
|-----------------|--------------------|------------------------------------------|----------------------------|
| [Common Events] | CommonEvents.json   | [$dataCommonEvents](global.md#datacommonevents-arrayrpgcommonevent)(Array) | [Game_CommonEvent](Game_CommonEvent.md) |

Related Classes: [RPG.Event](RPG.Event.md), [RPG.Troop](RPG.Troop.md), [RPG.EventPage.Conditions](RPG.EventPage.Conditions.md), [RPG.BattleEventPage.Conditions](RPG.BattleEventPage.Conditions.md)

### Properties

| Identifier  | Type                                      | Description                                                       |
|-------------|-------------------------------------------|-------------------------------------------------------------------|
| `id`        | [Number](Number.md)                      | [Common Event ID](RPG.CommonEvent.md#common-event-id)          |
| `name`      | [String](String.md)                      | [Name]                                                           |
| `trigger`   | [Number](Number.md)                      | [[Trigger](RPG.CommonEvent.md#trigger)]                         |
| `switchId`  | [Number](Number.md)                      | [[Switch](RPG.CommonEvent.md#switch)]                           |
| `list`      | [Array](Array.md).&lt;[RPG.EventCommand](RPG.EventCommand.md)&gt; | [Execution Contents]                                             |

#### Common Event ID
The number in the [Database] - [Common Events].

#### [Trigger]

| Number | Description   |
|--------|---------------|
| 0      | [None]       |
| 1      | [Automatic Execution] |
| 2      | [Parallel Processing] |

#### [Switch]
The number specified in the value() of [Game_Switches](Game_Switches.md) when the trigger is 1 or 2.
