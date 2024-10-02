[Class Tree](index.md)

# Class: [RPG](RPG.md).[Enemy](RPG.Enemy.md).Action
JSON data for the [action patterns] of [enemy characters].

Related Classes: [Game_Enemy](Game_Enemy.md)

### Properties

| Identifier        | Type                                    | Description                                             |
|-------------------|-----------------------------------------|---------------------------------------------------------|
| `skillId`         | [Number](Number.md)                    | [Skill ID](RPG.Skill.md#skill-id)                      |
| `conditionType`   | [Number](Number.md)                    | [[Condition](RPG.Enemy.Action.md#condition)]          |
| `conditionParam1` | [Number](Number.md)                    | Condition Parameter 1                                   |
| `conditionParam2` | [Number](Number.md)                    | Condition Parameter 2                                   |
| `rating`          | [Number](Number.md)                    | [Rating] (1 to 10)                                     |

#### [Condition]

Italicized parts such as *0* are numbers that are present but unused.

| Number | [Condition]          | conditionParam1   | conditionParam2   |
|--------|----------------------|-------------------|-------------------|
| 0      | Always               | *0*               | *0*               |
| 1      | Turn                 | Starting Turn     | Turn Interval      |
| 2      | HP                   | Lower Limit %     | Upper Limit %      |
| 3      | MP                   | Lower Limit %     | Upper Limit %      |
| 4      | State                | [State ID](RPG.State.md#state-id) | *0*               |
| 5      | Party Level          | Lower Level       | *0*               |
| 6      | Switch               | Switch ID         | *0*               |
