[Class Tree](index.md)

# Class: [RPG](RPG.md).Damage
Data related to [Damage].

Related Classes: [RPG.UsableItem](RPG.UsableItem.md), [Game_Action](Game_Action.md)

### Properties

| Identifier   | Type                                    | Description                                              |
|--------------|-----------------------------------------|----------------------------------------------------------|
| `type`       | [Number](Number.md)                    | [Type](RPG.Damage.md#type)                             |
| `elementId`  | [Number](Number.md)                    | [Element ID](RPG.Damage.md#element-id)                 |
| `formula`    | [String](String.md)                    | [[Formula](RPG.Damage.md#formula)]                      |
| `variance`   | [Number](Number.md)                    | [Variance] % (0–100)                                   |
| `critical`   | Boolean                                 | Whether it is a [Critical Hit]                          |

#### Type

| Number | [Type]         |
|--------|----------------|
| 0      | None           |
| 1      | HP Damage      |
| 2      | MP Damage      |
| 3      | HP Recovery     |
| 4      | MP Recovery     |
| 5      | HP Absorption  |
| 6      | MP Absorption  |

#### Element ID

The ID set in [Database] - [Type] - [Element]. It is registered in the elements property of [System](RPG.System.md). The -1 and 0 in the table below are fixed, while the values from 1 onwards are defaults.

| ID  | [Element]     |
|-----|---------------|
| -1  | Normal Attack |
| 0   | None          |
| 1   | Physical      |
| 2   | Fire          |
| 3   | Ice           |
| 4   | Thunder       |
| 5   | Water         |
| 6   | Earth         |
| 7   | Wind          |
| 8   | Light         |
| 9   | Darkness      |

#### [Formula]
The formula is processed by eval ([Game_Action.evalDamageFormula](Game_Action.md#evaldamageformula-target--number)), so you can directly use JavaScript methods like Math.random(). <br />
Additionally, the following variables are available:

| Variable | Value                                          |
|----------|------------------------------------------------|
| a        | Attacker's [Game_BattlerBase](Game_BattlerBase.md) |
| b        | Defender's [Game_BattlerBase](Game_BattlerBase.md) (can be replaced with target) |
| v        | _data property of [Game_Variables](Game_Variables.md) |
| item     | [RPG.UsableItem](RPG.UsableItem.md)         |
| this     | [Game_Action](Game_Action.md)                 |
