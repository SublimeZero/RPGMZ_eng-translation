[Class Tree](index.md)

# Class: Game_BattlerBase

Maintained by [BattleManager](BattleManager.md) and used for calculating parameters in battle scenes.

### new Game_BattlerBase ()

### Subclasses

* [Game_Battler](Game_Battler.md)

### Properties
Static constants with the prefix TRAIT_ are used to extract values included in [traits]. However, this class has methods available for each, so there's no need to use them directly. <br />
Refer to the values of [traits] in [RPG.Trait](RPG.Trait.md). When directly manipulating these values, use the constants with the TRAIT_ prefix.

Properties marked with [read-only] in the description are prepared for use in [formulas] such as those in [RPG.Damage](RPG.Damage.md). <br />
In the formula <code>a.atk * 4 - b.def * 2</code>, the `a` and `b` are assigned to instances of Game_BattlerBase (or its subclasses).

| Identifier                | Type               | Description                                   |
| ------------------------- | ------------------| --------------------------------------------- |
| `TRAIT_ELEMENT_RATE`      | [Number](Number.md) | [static] [Resistance] - [Elemental Efficacy] |
| `TRAIT_DEBUFF_RATE`       | [Number](Number.md) | [static] [Resistance] - [Debuff Efficacy]   |
| `TRAIT_STATE_RATE`        | [Number](Number.md) | [static] [Resistance] - [State Efficacy]    |
| `TRAIT_STATE_RESIST`      | [Number](Number.md) | [static] [Resistance] - [State Nullification] |
| `TRAIT_PARAM`             | [Number](Number.md) | [static] [Attributes] - [Normal Attributes]  |
| `TRAIT_XPARAM`            | [Number](Number.md) | [static] [Attributes] - [Additional Attributes] |
| `TRAIT_SPARAM`            | [Number](Number.md) | [static] [Attributes] - [Special Attributes] |
| `TRAIT_ATTACK_ELEMENT`     | [Number](Number.md) | [static] [Attack] - [Attack Element]        |
| `TRAIT_ATTACK_STATE`      | [Number](Number.md) | [static] [Attack] - [Attack State]          |
| `TRAIT_ATTACK_SPEED`      | [Number](Number.md) | [static] [Attack] - [Attack Speed Modifier] |
| `TRAIT_ATTACK_TIMES`      | [Number](Number.md) | [static] [Attack] - [Additional Attack Times] |
| `TRAIT_ATTACK_SKILL`      | [Number](Number.md) | **@MZ** [static] [Attack] - [Attack Skill]  |
| `TRAIT_STYPE_ADD`         | [Number](Number.md) | [static] [Skills] - [Add Skill Types]       |
| `TRAIT_STYPE_SEAL`        | [Number](Number.md) | [static] [Skills] - [Seal Skill Types]      |
| `TRAIT_SKILL_ADD`         | [Number](Number.md) | [static] [Skills] - [Add Skills]            |
| `TRAIT_SKILL_SEAL`        | [Number](Number.md) | [static] [Skills] - [Seal Skills]           |
| `TRAIT_EQUIP_WTYPE`       | [Number](Number.md) | [static] [Equipment] - [Equip Weapon Types] |
| `TRAIT_EQUIP_ATYPE`       | [Number](Number.md) | [static] [Equipment] - [Equip Armor Types]  |
| `TRAIT_EQUIP_LOCK`        | [Number](Number.md) | [static] [Equipment] - [Equip Lock]         |
| `TRAIT_EQUIP_SEAL`        | [Number](Number.md) | [static] [Equipment] - [Seal Equipment]     |
| `TRAIT_SLOT_TYPE`         | [Number](Number.md) | [static] [Equipment] - [Slot Type]          |
| `TRAIT_ACTION_PLUS`       | [Number](Number.md) | [static] [Others] - [Additional Actions]    |
| `TRAIT_SPECIAL_FLAG`      | [Number](Number.md) | [static] [Others] - [Special Flags]         |
| `TRAIT_COLLAPSE_TYPE`     | [Number](Number.md) | [static] [Others] - [Collapse Effects]      |
| `TRAIT_PARTY_ABILITY`     | [Number](Number.md) | [static] [Others] - [Party Abilities]       |
| `FLAG_ID_AUTO_BATTLE`     | [Number](Number.md) | [static] Special Flag ID for [Auto Battle]  |
| `FLAG_ID_GUARD`           | [Number](Number.md) | [static] Special Flag ID for [Guard]        |
| `FLAG_ID_SUBSTITUTE`      | [Number](Number.md) | [static] Special Flag ID for [Substitute]    |
| `FLAG_ID_PRESERVE_TP`     | [Number](Number.md) | [static] Special Flag ID for [TP Preservation] |
| `ICON_BUFF_START`         | [Number](Number.md) | [static] Start Position for Buff Icons       |
| `ICON_DEBUFF_START`       | [Number](Number.md) | [static] Start Position for Debuff Icons     |
| `hp`                       | [Number](Number.md) | [read-only] HP                               |
| `mp`                       | [Number](Number.md) | [read-only] MP                               |
| `tp`                       | [Number](Number.md) | [read-only] TP                               |
| `mhp`                      | [Number](Number.md) | [read-only] Max HP                           |
| `mmp`                      | [Number](Number.md) | [read-only] Max MP                           |
| `atk`                      | [Number](Number.md) | [read-only] Attack Power                     |
| `def`                      | [Number](Number.md) | [read-only] Defense Power                    |
| `mat`                      | [Number](Number.md) | [read-only] Magic Power                      |
| `mdf`                      | [Number](Number.md) | [read-only] Magic Defense Power              |
| `agi`                      | [Number](Number.md) | [read-only] Agility                          |
| `luk`                      | [Number](Number.md) | [read-only] Luck                              |
| `hit`                      | [Number](Number.md) | [read-only] Hit Rate                         |
| `eva`                      | [Number](Number.md) | [read-only] Evasion Rate                     |
| `cri`                      | [Number](Number.md) | [read-only] Critical Rate                    |
| `cev`                      | [Number](Number.md) | [read-only] Critical Evasion Rate            |
| `mev`                      | [Number](Number.md) | [read-only] Magic Critical Rate              |
| `mrf`                      | [Number](Number.md) | [read-only] Magic Reflection Rate            |
| `cnt`                      | [Number](Number.md) | [read-only] Counter Rate                     |
| `hrg`                      | [Number](Number.md) | [read-only] HP Recovery Rate                 |
| `mrg`                      | [Number](Number.md) | [read-only] MP Recovery Rate                 |
| `trg`                      | [Number](Number.md) | [read-only] TP Recovery Rate                 |
| `tgr`                      | [Number](Number.md) | [read-only] Target Rate                      |
| `grd`                      | [Number](Number.md) | [read-only] Guard Rate                       |
| `rec`                      | [Number](Number.md) | [read-only] Recovery Rate                    |
| `pha`                      | [Number](Number.md) | [read-only] Drug Effect Rate                 |
| `mcr`                      | [Number](Number.md) | [read-only] MP Consumption Rate              |
| `tcr`                      | [Number](Number.md) | [read-only] TP Charge Rate                   |
| `pdr`                      | [Number](Number.md) | [read-only] Physical Damage Rate             |
| `mdr`                      | [Number](Number.md) | [read-only] Magical Damage Rate              |
| `fdr`                      | [Number](Number.md) | [read-only] Floor Damage Rate                |
| `exr`                      | [Number](Number.md) | [read-only] Experience Rate                  |
| `_hp`                      | [Number](Number.md) | HP                                           |
| `_mp`                      | [Number](Number.md) | MP                                           |
| `_tp`                      | [Number](Number.md) | TP                                           |
| `_hidden`                  | Boolean           | Whether hidden                                |
| `_paramPlus`               | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of attribute enhancement amounts      |
| `_states`                  | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of [State IDs](RPG.State.md#state-id) |
| `_stateTurns`              | Object            | {[stateId: number]: number} Remaining turns for the state |
| `_buffs` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of ability enhancements |
| `_buffTurns` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Remaining turns of enhancements |

### Methods

#### actionPlusSet () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of [Other]-[Action Count Additions].

#### addedSkills () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of [Skills]-[Added Skills].

#### addedSkillTypes () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of [Skills]-[Added Skill Types].

#### addNewState (stateId)
Adds a new state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `stateId` | [Number](Number.md) | [State ID](RPG.State.md#state-id) |

#### addParam (paramId, value)
Adds the specified value to the specified ability.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `paramId` | [Number](Number.md) | [Ability ID](RPG.Enemy.md#ability-id) |
| `value` | [Number](Number.md) | Value |

#### allIcons () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of all icon numbers.

#### allTraits () → {[Array](Array.md).&lt;[RPG.Trait](RPG.Trait.md)&gt;}
Returns an array of all traits.

#### appear ()
Causes the battler to appear.

#### attackElements () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of [Attack Elements].

#### attackSkillId () → {[Number](Number.md)}
Returns the ID of the attack skill (default: 1).<br />
**@MZ** Returns the value if [Attack]-[Attack Skill] is set.

#### attackSpeed () → {[Number](Number.md)}
Returns [Attack]-[Attack Speed Adjustment].

#### attackStates () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of attack [State IDs](RPG.State.md#state-id).

#### attackStatesRate (stateId)
Returns the addition rate for the specified attack state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `stateId` | [Number](Number.md) | [State ID](RPG.State.md#state-id) |

#### attackTimesAdd () → {[Number](Number.md)}
Returns [Attack]-[Additional Attack Count].

#### buff (paramId) → {[Number](Number.md)}
Returns the enhancement amount of the specified ability.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `paramId` | [Number](Number.md) | [Ability ID](RPG.Enemy.md#ability-id) |

#### buffIconIndex (buffLevel, paramId) → {[Number](Number.md)}
Returns the icon number for [Buff].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `buffLevel` | [Number](Number.md) | Buff level |
| `paramId` | [Number](Number.md) | [Ability ID](RPG.Enemy.md#ability-id) |

#### buffIcons () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of active [Buff] icon numbers.

#### buffLength () → {[Number](Number.md)}
Returns the number of enhanced abilities.

#### canAttack () → {Boolean}
Checks if the battler can attack.

#### canEquip (item) → {Boolean}
Checks if the specified item can be equipped.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.EquipItem](RPG.EquipItem.md) | Equip item |

#### canEquipArmor (item) → {Boolean}
Checks if the specified armor can be equipped.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.EquipItem](RPG.EquipItem.md) | Equip item |

#### canEquipWeapon (item) → {Boolean}
Checks if the specified weapon can be equipped.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.EquipItem](RPG.EquipItem.md) | Equip item |

#### canGuard () → {Boolean}
Checks if the battler can guard.

#### canInput () → {Boolean}
Checks if input for action is possible.

#### canMove () → {Boolean}
Checks if movement is possible.

#### canPaySkillCost (skill) → {Boolean}
Checks if the specified skill can be used.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `skill` | [RPG.Skill](RPG.Skill.md) | Skill |

#### canUse (item) → {Boolean}
Checks if the specified item can be used.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.UsableItem](RPG.UsableItem.md) | Item |

#### clearBuffs ()
Resets ability [Buffs].

#### clearParamPlus ()
Resets ability enhancement amounts.

#### clearStates ()
Resets state changes.

#### collapseType () → {[Number](Number.md)}
Returns [Other]-[Collapse Effect].

#### confusionLevel () → {[Number](Number.md)}
Returns the confusion level.

#### deathStateId () → {[Number](Number.md)}
Returns the ID of the death state (default: 1).

#### debuffRate (paramId) → {[Number](Number.md)}
Returns the [Resistance]-[Debuff Effectiveness] for the specified ability value.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `paramId` | [Number](Number.md) | [Ability ID](RPG.Enemy.md#ability-id) |

#### decreaseBuff (paramId)
Decreases the [Buff] for the specified ability.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `paramId` | [Number](Number.md) | [Ability ID](RPG.Enemy.md#ability-id) |

#### die ()
Causes the battler to enter the death state.

#### elementRate (elementId) → {[Number](Number.md)}
Returns the [Resistance]-[Element Effectiveness] for the specified element.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `elementId` | [Number](Number.md) | [Element ID](RPG.Damage.md#element-id) |

#### eraseBuff (paramId)
Removes the [Buff] for the specified ability.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `paramId` | [Number](Number.md) | [Ability ID](RPG.Enemy.md#ability-id) |

#### eraseState (stateId)
Removes the specified state.

##### Arguments

| Name       | Type                          | Description                                    |
|------------|-------------------------------|------------------------------------------------|
| `stateId`  | [Number](Number.md)          | [State ID](RPG.State.md#state-id)             |


#### guardSkillId () → {[Number](Number.md)}
Returns the ID of the guard skill (default: 2).


#### hide ()
Hides the battler.


#### hpRate () → {[Number](Number.md)}
Returns the percentage of HP.


#### increaseBuff (paramId)
Increases the specified normal ability.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### initialize ()
Initializes when the object is created.


#### initMembers ()
Initializes member variables.


#### isActor () → {Boolean}
Is this an actor?


#### isAlive () → {Boolean}
Is this alive?


#### isAppeared () → {Boolean}
Is this appeared?


#### isAutoBattle () → {Boolean}
Is this [Auto Battle]?


#### isBuffAffected (paramId) → {Boolean}
Is the specified normal ability buffed?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### isBuffExpired (paramId) → {Boolean}
Is the buff for the specified normal ability expired?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### isBuffOrDebuffAffected (paramId) → {Boolean}
Is the specified normal ability buffed or debuffed?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### isConfused () → {Boolean}
Is this confused?


#### isDead () → {Boolean}
Is this in the death state?


#### isDeathStateAffected () → {Boolean}
Is this in the death state?


#### isDebuffAffected (paramId) → {Boolean}
Is the specified normal ability debuffed?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### isDualWield () → {Boolean}
Is this dual-wielding?


#### isDying () → {Boolean}
Is this dying (default: HP at or below 1/4 of max HP)?


#### isEnemy () → {Boolean}
Is this an enemy?


#### isEquipAtypeOk (atypeId) → {Boolean}
Is the specified armor type available for [Equipment]-[Armor Type]?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `atypeId` | [Number](Number.md)          | [Armor Type ID](RPG.Trait.md#52--armor-type-id) |


#### isEquipTypeLocked (etypeId) → {Boolean}
Is the specified equipment type [Equipment]-[Equipment Locked]?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `etypeId` | [Number](Number.md)          | [Equipment Type ID](RPG.Trait.md#53-54--equipment-type-id) |


#### isEquipTypeSealed (etypeId) → {Boolean}
Is the specified equipment type [Equipment]-[Equipment Sealed]?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `etypeId` | [Number](Number.md)          | [Equipment Type ID](RPG.Trait.md#53-54--equipment-type-id) |


#### isEquipWtypeOk (wtypeId) → {Boolean}
Is the specified weapon type available for [Equipment]-[Weapon Type]?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `wtypeId` | [Number](Number.md)          | [Weapon Type ID](RPG.Trait.md#51--weapon-type-id) |


#### isGuard () → {Boolean}
Is this guarding?


#### isHidden () → {Boolean}
Is this hidden?


#### isMaxBuffAffected (paramId) → {Boolean}
Is the specified normal ability at max buff?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### isMaxDebuffAffected (paramId) → {Boolean}
Is the specified normal ability at max debuff?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### isOccasionOk (item) → {Boolean}
Is the specified item usable?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `item`    | [RPG.UsableItem](RPG.UsableItem.md) | Item                                       |


#### isPreserveTp () → {Boolean}
Is this [TP Preservation]?


#### isRestricted () → {Boolean}
Is this under some action restriction state?


#### isSkillSealed (stypeId) → {Boolean}
Is the specified skill type [Skills]-[Skill Sealed]?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `stypeId` | [Number](Number.md)          | [Skill Type ID](RPG.Trait.md#skill-type-id)  |


#### isSkillTypeSealed (stypeId) → {Boolean}
Is the specified skill type [Skills]-[Skill Type Sealed]?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `stypeId` | [Number](Number.md)          | [Skill Type ID](RPG.Trait.md#skill-type-id)  |


#### isSkillWtypeOk (skill) → {Boolean}
Is the specified skill's activation conditions met by the equipped items?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `skill`   | [RPG.Skill](RPG.Skill.md)    | Skill                                          |


#### isStateAffected (stateId) → {Boolean}
Is the specified state active?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `stateId` | [Number](Number.md)          | [State ID](RPG.State.md#state-id)             |


#### isStateExpired (stateId) → {Boolean}
Is the specified state expired?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `stateId` | [Number](Number.md)          | [State ID](RPG.State.md#state-id)             |


#### isStateResist (stateId) → {Boolean}
Is the specified state resisted?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `stateId` | [Number](Number.md)          | [State ID](RPG.State.md#state-id)             |


#### isSubstitute () → {Boolean}
Is this a [Substitute] state?


#### maxTp () → {[Number](Number.md)}
Returns the maximum TP.


#### meetsItemConditions (item) → {Boolean}
Is the specified item available for use?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `item`    | [RPG.Item](RPG.Item.md)      | Item                                          |


#### meetsSkillConditions (skill) → {Boolean}
Is the specified skill available for use?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `skill`   | [RPG.Skill](RPG.Skill.md)    | Skill                                          |


#### meetsUsableItemConditions (item) → {Boolean}
Is the specified item usable?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `item`    | [RPG.UsableItem](RPG.UsableItem.md) | Item                                       |


#### mostImportantStateText () → {[String](String.md)}
Returns a message string representing the current state.


#### mpRate () → {[Number](Number.md)}
Returns the percentage of MP.


#### onRestrict ()
Handler called when action is restricted.


#### overwriteBuffTurns (paramId, turns)
Adds effective turns for the normal ability [buff].

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |
| `turns`   | [Number](Number.md)          | Additional turns                               |


#### param (paramId) → {[Number](Number.md)}
Returns the value after calculations for the specified normal ability, such as [buff] effects.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### paramBase (paramId) → {[Number](Number.md)}
Returns the base value of the specified normal ability (default: 0).

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### paramBasePlus (paramId) → {[Number](Number.md)}
**@MZ** Returns the base value + addition for the specified normal ability.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### paramBuffRate (paramId) → {[Number](Number.md)}
Returns the [buff] rate for the specified normal ability.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### paramMax (paramId) → {[Number](Number.md)}
Returns the maximum value of the specified normal ability.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### paramMin (paramId) → {[Number](Number.md)}
Returns the minimum value of the specified normal ability.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### paramPlus (paramId) → {[Number](Number.md)}
Returns the value added to the specified normal ability.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### paramRate (paramId) → {[Number](Number.md)}
Returns the value of the specified [Ability]-[Normal Ability].

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `paramId` | [Number](Number.md)          | [Ability ID](RPG.Enemy.md#ability-id)        |


#### partyAbility (abilityId) → {Boolean}
Is the specified party ability [Other]-[Party Ability]?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `abilityId` | [Number](Number.md)          | [Party Ability ID](RPG.Trait.md#64--party-ability-id) |


#### paySkillCost (skill)
Consumes the cost (MP, TP) required for the skill.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `skill`   | [RPG.Skill](RPG.Skill.md)    | Skill                                          |


#### recoverAll ()
Fully recovers HP and MP and removes states.


#### refresh ()
Processes to keep ability values and states within the default range.


#### resetStateCounts (stateId)
Resets the effective turn count for the specified state.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `stateId` | [Number](Number.md)          | [State ID](RPG.State.md#state-id)             |


#### restriction () → {[Number](Number.md)}
Returns a value indicating the state of action restriction.

0: None, 1: Attack enemy, 2: Random attack, 3: Attack ally, 4: Unable to act


#### revive ()
Revives the character.


#### setHp (hp)
Sets the HP.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `hp`      | [Number](Number.md)          | HP                                             |


#### setMp (mp)
Sets the MP.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `mp`      | [Number](Number.md)          | MP                                             |


#### setTp (tp)
Sets the TP.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `tp`      | [Number](Number.md)          | TP                                             |

#### skillMpCost (skill) → {[Number](Number.md)}
Returns the MP required for the specified skill.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `skill`   | [RPG.Skill](RPG.Skill.md)    | Skill                                          |


#### skillTpCost (skill) → {[Number](Number.md)}
Returns the TP required for the specified skill.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `skill`   | [RPG.Skill](RPG.Skill.md)    | Skill                                          |


#### slotType () → {[Number](Number.md)}
Returns the [Equipment]-[Slot Type].


#### sortStates ()
Sorts states by priority.


#### sparam (sparamId) → {[Number](Number.md)}
Returns the value of the specified [Ability]-[Special Ability].

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `sparamId` | [Number](Number.md)          | [Special Ability ID](RPG.Trait.md#23--special-ability-id) |


#### specialFlag (flagId) → {Boolean}
Is the specified flag [Other]-[Special Flag]?

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `flagId`  | [Number](Number.md)          | Flag ID                                       |


#### stateIcons () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of state icon numbers.


#### stateMotionIndex () → {[Number](Number.md)}
Returns the motion index of the state in SV.


#### stateOverlayIndex () → {[Number](Number.md)}
Returns the overlay index of the state in SV.


#### stateRate (stateId) → {[Number](Number.md)}
Returns the [Resistance]-[State Effectiveness] for the specified state.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `stateId` | [Number](Number.md)          | [State ID](RPG.State.md#state-id)             |


#### stateResistSet () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of [State IDs](RPG.State.md#state-id) corresponding to [Resistance]-[State Disable].


#### states () → {[Array](Array.md).&lt;[RPG.State](RPG.State.md)&gt;}
Returns an array of currently applied states.


#### tpRate () → {[Number](Number.md)}
Returns the percentage of TP.


#### traitObjects () → {[Array](Array.md).lt;*&gt;}
Returns an array of trait objects.


#### traits (code) → {[Array](Array.md).&lt;[RPG.Trait](RPG.Trait.md)&gt;}
Returns the traits for the specified trait code (TRAIT_CONSTANT).

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `code`    | [Number](Number.md)          | [Trait Code](RPG.Trait.md#code)               |


#### traitsPi (code, id) → {[Number](Number.md)}
Returns the value for the specified trait code (TRAIT_CONSTANT) and ID.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `code`    | [Number](Number.md)          | [Trait Code](RPG.Trait.md#code)               |
| `id`      | [Number](Number.md)          | Trait ID                                       |


#### traitsSet (code) → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of trait IDs for the specified trait code (TRAIT_CONSTANT).

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `code`    | [Number](Number.md)          | [Trait Code](RPG.Trait.md#code)               |


#### traitsSum (code, id) → {[Number](Number.md)}
Returns the sum of traits for the specified trait code (TRAIT_CONSTANT) and ID.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `code`    | [Number](Number.md)          | [Trait Code](RPG.Trait.md#code)               |
| `id`      | [Number](Number.md)          | Trait ID                                       |


#### traitsSumAll (code) → {[Number](Number.md)}
Returns the accumulated traits for the specified trait code (TRAIT_CONSTANT).

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `code`    | [Number](Number.md)          | [Trait Code](RPG.Trait.md#code)               |


#### traitsWithId (code, id) → {[Array](Array.md).&lt;[RPG.Trait](RPG.Trait.md)&gt;}
Returns an array of traits for the specified trait code (TRAIT_CONSTANT) and ID.

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `code`    | [Number](Number.md)          | [Trait Code](RPG.Trait.md#code)               |
| `id`      | [Number](Number.md)          | Trait ID                                       |


#### updateBuffTurns ()
Updates normal ability [buffs].


#### updateStateTurns ()
Updates state changes.


#### xparam (xparamId) → {[Number](Number.md)}
Returns the value of the specified [Ability]-[Additional Ability].

##### Arguments

| Name      | Type                          | Description                                    |
|-----------|-------------------------------|------------------------------------------------|
| `xparamId` | [Number](Number.md)          | [Additional Ability ID](RPG.Trait.md#additional-ability-id) |
