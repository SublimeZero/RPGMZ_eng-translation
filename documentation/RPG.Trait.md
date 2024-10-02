[Class Tree](index.md)

# Class: [RPG](RPG.md).Trait
JSON data for [Traits], primarily used during battles.

Refer to the official beginner's guide for setting [Actor Traits](https://tkool.jp/mv/guide/004_003c.html), [Setting Enemy Traits](https://tkool.jp/mv/guide/004_008a.html#03), [Weapon Traits](https://tkool.jp/mv/guide/004_005b.html#03), [Armor Traits](https://tkool.jp/mv/guide/004_005c.html#03), and the main help documentation.

Related Classes: [RPG.Actor](RPG.Actor.md), [RPG.Enemy](RPG.Enemy.md), [RPG.EquipItem](RPG.EquipItem.md), [RPG.Armor](RPG.Armor.md), [RPG.Weapon](RPG.Weapon.md), [RPG.State](RPG.State.md)

### Properties

| Identifier | Type                      | Description                                          |
|------------|---------------------------|------------------------------------------------------|
| `code`     | [Number](Number.md)      | [Trait] code (refer to [the table below](RPG.Trait.md#code)) |
| `dataId`   | [Number](Number.md)      | ID with different meanings for each code              |
| `value`    | [Number](Number.md)      | Value with different meanings for each code           |

#### code

The numeric values for code are defined as static class constants in [Game_BattlerBase](Game_BattlerBase.md). For example, it is used in the form of `Game_BattlerBase.TRAIT_ELEMENT_RATE`.

In the tables below, the fluctuation rate, ratio, and increment/decrement value are represented with 1 as the value corresponding to 100%.

Italic portions like *0* or *1* have unused numbers.

##### [Resistances]

| code | Constant                    | Content                 | dataId | value             |
|------|-----------------------------|-------------------------|--------|-------------------|
| 11   | `TRAIT_ELEMENT_RATE`        | Element effectiveness    | [Element ID](RPG.Damage.md#element-id) | Fluctuation rate (0-10) |
| 12   | `TRAIT_DEBUFF_RATE`        | Debuff effectiveness     | [Parameter ID](RPG.Enemy.md#parameter-id) | Fluctuation rate (0-10) |
| 13   | `TRAIT_STATE_RATE`         | State effectiveness      | [State ID](RPG.State.md#state-id) | Fluctuation rate (0-10) |
| 14   | `TRAIT_STATE_RESIST`       | State nullification      | [State ID](RPG.State.md#state-id) | *1*                |

##### [Parameters]

| code | Constant                  | Content               | dataId | value             |
|------|---------------------------|-----------------------|--------|-------------------|
| 21   | `TRAIT_PARAM`            | Normal parameters      | [Parameter ID](RPG.Enemy.md#parameter-id) | Fluctuation rate (0-10) |
| 22   | `TRAIT_XPARAM`           | Additional parameters   | [Additional Parameter ID](RPG.Trait.md#additional-parameter-id) | Ratio (-10 to 10) |
| 23   | `TRAIT_SPARAM`           | Special parameters      | [Special Parameter ID](RPG.Trait.md#special-parameter-id) | Fluctuation rate (0-10) |

###### Additional Parameter IDs

| ID | Additional Parameter |
|----|---------------------|
| 0  | Hit rate           |
| 1  | Evasion rate       |
| 2  | Critical rate      |
| 3  | Critical evasion rate |
| 4  | Magic evasion rate  |
| 5  | Magic reflection rate |
| 6  | Counter rate       |
| 7  | HP regeneration rate |
| 8  | MP regeneration rate |
| 9  | TP regeneration rate |

###### Special Parameter IDs

| ID | Special Parameter |
|----|-------------------|
| 0  | Target rate       |
| 1  | Defense effectiveness rate |
| 2  | Healing effectiveness rate |
| 3  | Pharmacology      |
| 4  | MP consumption rate |
| 5  | TP charge rate    |
| 6  | Physical damage rate |
| 7  | Magic damage rate  |
| 8  | Floor damage rate  |
| 9  | Experience gain rate |

##### [Attack]

| code | Constant                  | Content                | dataId | value             |
|------|---------------------------|------------------------|--------|-------------------|
| 31   | `TRAIT_ATTACK_ELEMENT`    | Attack element         | [Element ID](RPG.Damage.md#element-id) | *1*                |
| 32   | `TRAIT_ATTACK_STATE`      | Attack state           | [State ID](RPG.State.md#state-id) | Fluctuation rate (0-10) |
| 33   | `TRAIT_ATTACK_SPEED`      | Attack speed adjustment | *0*    | Increment/decrement value (-10 to 10) |
| 34   | `TRAIT_ATTACK_TIMES`      | Additional attack count | *0*    | Additional attack count (-9.0 to 9.0) |
| 35   | `TRAIT_ATTACK_SKILL`      | **@MZ** Attack skill    | [Skill ID](RPG.Skill.md#skill-id) | *1*                |

##### [Skills]

| code | Constant                  | Content                | dataId | value             |
|------|---------------------------|------------------------|--------|-------------------|
| 41   | `TRAIT_STYPE_ADD`        | Add skill type         | [Skill Type ID](RPG.Skill.md#skill-type-id) | *1*                |
| 42   | `TRAIT_STYPE_SEAL`       | Seal skill type        | [Skill Type ID](RPG.Skill.md#skill-type-id) | *1*                |
| 43   | `TRAIT_SKILL_ADD`        | Add skill              | [Skill ID](RPG.Skill.md#skill-id) | *1*                |
| 44   | `TRAIT_SKILL_SEAL`       | Seal skill             | [Skill ID](RPG.Skill.md#skill-id) | *1*                |

##### [Equipment]

| code | Constant                  | Content                | dataId | value             |
|------|---------------------------|------------------------|--------|-------------------|
| 51   | `TRAIT_EQUIP_WTYPE`      | Equip weapon type      | [Weapon Type ID](RPG.Trait.md#weapon-type-id) | *1*                |
| 52   | `TRAIT_EQUIP_ATYPE`      | Equip armor type       | [Armor Type ID](RPG.Trait.md#armor-type-id) | *1*                |
| 53   | `TRAIT_EQUIP_LOCK`       | Lock equipment         | [Equipment Type ID](RPG.Trait.md#equipment-type-id) | *1*                |
| 54   | `TRAIT_EQUIP_SEAL`       | Seal equipment         | [Equipment Type ID](RPG.Trait.md#equipment-type-id) | *1*                |
| 55   | `TRAIT_SLOT_TYPE`        | Slot type              | [Slot Type ID](RPG.Trait.md#slot-type-id) | *1*                |

###### Weapon Type IDs

The ID set in [Database]-[Types]-[Weapon Types].

Names are registered in the weaponTypes property of [RPG.System](RPG.System.md).

The following table shows default values.

| ID | [Weapon Type] |
|----|----------------|
| 0  | None           |
| 1  | Dagger         |
| 2  | Sword          |
| 3  | Flail          |
| 4  | Axe            |
| 5  | Whip           |
| 6  | Staff          |
| 7  | Bow            |
| 8  | Crossbow       |
| 9  | Gun            |
| 10 | Claw           |
| 11 | Glove          |
| 12 | Spear          |

###### Armor Type IDs

The ID set in [Database]-[Types]-[Armor Types].

Names are registered in the armorTypes property of [RPG.System](RPG.System.md).

The following table shows default values.

| ID | [Armor Type]   |
|----|----------------|
| 1  | General armor  |
| 2  | Magical armor   |
| 3  | Light armor    |
| 4  | Heavy armor    |
| 5  | Small shield   |
| 6  | Large shield   |

###### Equipment Type IDs

The IDs set in [Database]-[Types]-[Equipment Types].

The names are registered in the equipTypes property of [RPG.System](RPG.System.md).

The following table shows default values.

| ID | [Equipment Type] |
|----|-------------------|
| 0  | None              |
| 1  | Shield            |
| 2  | Head              |
| 3  | Body              |
| 4  | Accessory         |

###### Slot Type IDs

| ID | [Slot Type]      |
|----|-------------------|
| 0  | Normal            |
| 1  | Dual Wield        |

##### [Others]

| code | Constant                | Content                   | dataId | value        |
|------|-------------------------|---------------------------|--------|--------------|
| 61   | `TRAIT_ACTION_PLUS`     | Additional action count    | *0*    | Probability (%) |
| 62   | `TRAIT_SPECIAL_FLAG`    | Special flag               | [Special Flag ID](RPG.Trait.md#special-flag-id) | *1*  |
| 63   | `TRAIT_COLLAPSE_TYPE`   | Disappearance effect       | [Disappearance Effect ID](RPG.Trait.md#disappearance-effect-id) | *1* |
| 64   | `TRAIT_PARTY_ABILITY`    | Party ability              | [Party Ability ID](RPG.Trait.md#party-ability-id) | *1* |

###### Special Flag IDs

| ID | Constant                     | [Special Flag]         |
|----|------------------------------|------------------------|
| 0  | `FLAG_ID_AUTO_BATTLE`       | Auto Battle            |
| 1  | `FLAG_ID_GUARD`             | Guard                  |
| 2  | `FLAG_ID_SUBSTITUTE`         | Substitute             |
| 3  | `FLAG_ID_PRESERVE_TP`       | Preserve TP            |

###### Disappearance Effect IDs

| ID | [Disappearance Effect]  |
|----|--------------------------|
| 0  | Normal                   |
| 1  | Boss                     |
| 2  | Instant Deletion         |
| 3  | Non-vanishing            |

###### Party Ability IDs

The constant IDs are defined in [Game_Party](Game_Party.md) and are used in the form of `Game_Party.ABILITY_ENCOUNTER_HALF`, for example.

| ID | Constant                     | [Party Ability]       |
|----|------------------------------|-----------------------|
| 0  | `ABILITY_ENCOUNTER_HALF`     | Halves encounters      |
| 1  | `ABILITY_ENCOUNTER_NONE`     | Disables encounters    |
| 2  | `ABILITY_CANCEL_SURPRISE`    | Disables surprise attacks |
| 3  | `ABILITY_RAISE_PREEMPTIVE`   | Increases preemptive attack rate |
| 4  | `ABILITY_GOLD_DOUBLE`        | Doubles obtained gold  |
| 5  | `ABILITY_DROP_ITEM_DOUBLE`   | Doubles item acquisition rate |

###### Skill Type IDs

The IDs set in [Database]-[Types]-[Skill Types].

The names are registered in the skillTypes property of [RPG.System](RPG.System.md).

The following table shows default values.

| ID | [Skill Type] |
|----|---------------|
| 0  | None          |
| 1  | Magic         |
| 2  | Special Move  |
