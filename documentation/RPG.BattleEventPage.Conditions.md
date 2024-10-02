[Class Tree](index.md)

# Class: [RPG](RPG.md).[BattleEventPage](RPG.BattleEventPage.md).Conditions
JSON data that constitutes the [conditions] of the [EV page] of an [enemy group].

Related Classes: [RPG.BattleEventPage](RPG.BattleEventPage.md), [RPG.EventPage.Conditions](RPG.EventPage.Conditions.md), [RPG.CommonEvent](RPG.CommonEvent.md)

### Properties

| Identifier    | Type                                     | Description                      |
|---------------|------------------------------------------|----------------------------------|
| `turnEnding`  | Boolean                                  | Use [turn end]                  |
| `turnValid`   | Boolean                                  | Use [turn]                      |
| `turnA`      | [Number](Number.md)                     | Number before [turn] +          |
| `turnB`      | [Number](Number.md)                     | Number after [turn] +           |
| `enemyValid`  | Boolean                                  | Use [enemy character HP]        |
| `enemyIndex`  | [Number](Number.md)                     | Enemy character number for [enemy character HP] |
| `enemyHp`     | [Number](Number.md)                     | [Enemy character HP] (%)        |
| `actorValid`  | Boolean                                  | Use [actor HP]                  |
| `actorId`     | [Number](Number.md)                     | Actor ID for [actor HP]         |
| `actorHp`     | [Number](Number.md)                     | [Actor HP] (%)                  |
| `switchValid` | Boolean                                  | Use [switch]                    |
| `switchId`    | [Number](Number.md)                     | ID of [switch]                  |
