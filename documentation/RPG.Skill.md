[Class Tree](index.md)

# Class: [RPG](RPG.md).Skill

## Superclass: [RPG.UsableItem](RPG.UsableItem.md)

| Database   | JSON File     | Global Variable                                    | Object               |
|------------|----------------|---------------------------------------------------|----------------------|
| [Skills]   | Skills.json    | [$dataSkills](global.md#dataskills-arrayrpgskill)(array) | [Game_Item](Game_Item.md) |

The _dataClass property of [Game_Item](Game_Item.md) will be 'skill'.

### Properties

| Identifier                  | Type                                           | Description                             |
|-----------------------------|------------------------------------------------|-----------------------------------------|
| `stypeId`                   | [Number](Number.md)                           | [Skill Type ID](RPG.Skill.md#skill-type-id) |
| `mpCost`                    | [Number](Number.md)                           | [MP Cost]                              |
| `tpCost`                    | [Number](Number.md)                           | [TP Cost]                              |
| `message1`                  | [String](String.md)                           | Upper message [Message]                |
| `message2`                  | [String](String.md)                           | Lower message [Message]                |
| `requiredWtypeId1`         | [Number](Number.md)                           | [Required Weapon] [Weapon Type 1]     |
| `requiredWtypeId2`         | [Number](Number.md)                           | [Required Weapon] [Weapon Type 2]     |

#### Skill ID

The ID set in [Database] - [Skills]. It also corresponds to the index in the global variable [$dataSkills](global.md#dataskills-arrayrpgskill).<br />
The table below shows IDs 0 to 2 as fixed, while others can be changed to default values.

| ID | [Skill]          |
|----|------------------|
| 0  | None             |
| 1  | Attack           |
| 2  | Defense          |
| 3  | Continuous Attack |
| 4  | Double Attack    |
| 5  | Triple Attack    |
| 6  | Escape           |
| 7  | Observe          |
| 8  | Heal             |
| 9  | Fire             |
| 10 | Spark            |

#### Skill Type ID

The ID set in [Database] - [Type] - [Skill Type].<br />
The skill type names are registered in the skillTypes property of [System](RPG.System.md).

The table below shows ID 0 as fixed, while others can be changed to default values.

| ID | [Skill Type]   |
|----|-----------------|
| 0  | None            |
| 1  | Magic           |
| 2  | Special Move    |
