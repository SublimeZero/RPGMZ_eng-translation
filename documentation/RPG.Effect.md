[Class Tree](index.md)

# Class: [RPG](RPG.md).Effect
Data related to the [usage effects] of items and skills.

Related Classes: [Game_Action](Game_Action.md), [RPG.UsableItem](RPG.UsableItem.md)

### Properties

| Identifier   | Type                                    | Description                                             |
|--------------|-----------------------------------------|---------------------------------------------------------|
| `code`       | [Number](Number.md)                    | [Usage Effect] Code (refer to the [table below](RPG.Effect.md#code)) |
| `dataId`     | [Number](Number.md)                    | ID that has different meanings depending on the code   |
| `value1`     | [Number](Number.md)                    | Value 1 that has different meanings depending on the code |
| `value2`     | [Number](Number.md)                    | Value 2 that has different meanings depending on the code |

In the table below, italicized parts such as *0* and *1* are numbers that are present but unused.

### code
The code is defined as a constant in [Game_Action](Game_Action.md). For example, it is used as `Game_Action.EFFECT_RECOVER_HP`.

### value1, value2
Values in percentage terms are represented as 1 for 100%. <br />
Therefore, 10 means 1000%.

#### [Recovery]

| code | Constant                  | Usage Effect | dataId | value1                   | value2                          |
|------|--------------------------|--------------|--------|--------------------------|----------------------------------|
| 11   | `EFFECT_RECOVER_HP`      | HP Recovery   | *0*    | Ratio % (-1 to 1)       | Fixed Value (-999999 to 999999) |
| 12   | `EFFECT_RECOVER_MP`      | MP Recovery   | *0*    | Ratio % (-1 to 1)       | Fixed Value (-999999 to 999999) |
| 13   | `EFFECT_GAIN_TP`         | TP Increase   | *0*    | Fixed Value (0 to 100)  | *0*                             |

#### [State]

| code | Constant                  | Usage Effect | dataId                   | value1                   | value2 |
|------|--------------------------|--------------|--------------------------|--------------------------|--------|
| 21   | `EFFECT_ADD_STATE`       | Add State    | [State ID](RPG.State.md#state-id) | Probability % (0 to 10) | *0*    |
| 22   | `EFFECT_REMOVE_STATE`    | Remove State | [State ID](RPG.State.md#state-id) | Probability % (0 to 1)  | *0*    |

#### [Parameter]

| code | Constant                  | Usage Effect | dataId                   | value1                   | value2 |
|------|--------------------------|--------------|--------------------------|--------------------------|--------|
| 31   | `EFFECT_ADD_BUFF`        | Buff         | [Parameter ID](RPG.Enemy.md#parameter-id) | Duration (1 to 1000)   | *0*    |
| 32   | `EFFECT_ADD_DEBUFF`      | Debuff       | [Parameter ID](RPG.Enemy.md#parameter-id) | Duration (1 to 1000)   | *0*    |
| 33   | `EFFECT_REMOVE_BUFF`     | Remove Buff  | [Parameter ID](RPG.Enemy.md#parameter-id) | *1*                     | *0*    |
| 34   | `EFFECT_REMOVE_DEBUFF`   | Remove Debuff| [Parameter ID](RPG.Enemy.md#parameter-id) | *1*                     | *0*    |

#### [Other]

| code | Constant                  | Usage Effect | dataId                   | value1                   | value2 |
|------|--------------------------|--------------|--------------------------|--------------------------|--------|
| 41   | `EFFECT_SPECIAL`         | [Special Effect] | [Special Effect ID](RPG.Effect.md#special-effect-id) | *1*                     | *0*    |
| 42   | `EFFECT_GROW`           | Growth       | [Parameter ID](RPG.Enemy.md#parameter-id) | Increase Value           | *0*    |
| 43   | `EFFECT_LEARN_SKILL`     | Learn Skill  | [Skill ID](RPG.Skill.md#skill-id) | *1*                     | *0*    |
| 44   | `EFFECT_COMMON_EVENT`     | Common Event | Common Event ID          | *1*                     | *0*    |

##### Special Effect ID

| dataId | Constant                     | Usage Effect |
|--------|------------------------------|--------------|
| 0      | `SPECIAL_EFFECT_ESCAPE`      | Escape       |

##### dataId: Common Event ID

The number from [$dataCommonEvents](global.md#datacommonevents-arrayrpgcommonevent) (an array of [CommonEvent](RPG.CommonEvent.md)).
