# Class: [RPG](RPG.md).Troop

| Database      | JSON File   | Global Variable                            | Object                 |
|---------------|-------------|-------------------------------------------|------------------------|
| [Enemy Group] | Troops.json | [$dataTroops](global.md#datatroops-arrayrpgtroop) (array) | [Game_Troop](Game_Troop.md) |

Related Classes: [RPG.Event](RPG.Event.md), [RPG.CommonEvent](RPG.CommonEvent.md)

### Properties

| Identifier | Type                                           | Description          |
|------------|------------------------------------------------|----------------------|
| `id`      | [Number](Number.md)                          | Enemy group ID       |
| `name`    | [String](String.md)                          | Enemy group name     |
| `members` | [Array](Array.md).&lt;[RPG.Troop.Member](RPG.Troop.Member.md)&gt; | Members              |
| `pages`   | [Array](Array.md).&lt;[RPG.BattleEventPage](RPG.BattleEventPage.md)&gt; | [Battle Events]      |

### Inner Class

* [RPG.Troop.Member](RPG.Troop.Member.md)
