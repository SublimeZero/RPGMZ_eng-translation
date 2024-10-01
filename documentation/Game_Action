[Class Tree](index.md)

# Class: Game_Action

A class that describes combat actions such as attacks, defenses, and the use of skills or items.

The `_actions` property of [Game_Battler](Game_Battler.md) holds this, and conversely, you can obtain the Game_Battler using the [subject()](Game_Action.md#subject-) method.

Related classes: [BattleManager](BattleManager.md), [Game_Actor](Game_Actor.md), [Game_Enemy](Game_Enemy.md), [Game_ActionResult](Game_ActionResult.md), [RPG.Effect](RPG.Effect.md), [RPG.UsableItem](RPG.UsableItem.md), [RPG.Damage](RPG.Damage.md)

### new Game_Action (subject, forcing)
#### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | The entity performing the action |
| `forcing` | Boolean | Is it a forced action? |


### Properties

* Constants starting with EFFECT\_ are used to specify [[Usage Effects](RPG.Effect.md#code)].
* SPECIAL\_EFFECT\_ESCAPE is used to specify the dataId of [[Usage Effect - Other - Special Effects](RPG.Effect.md#その他)].
* Constants starting with HITTYPE\_ are used to specify [[Hit Types](RPG.UsableItem.md#命中タイプ)].

| Identifier | Type | Description |
| --- | --- | --- |
| `EFFECT_RECOVER_HP` | [Number](Number.md) | [static] HP recovery |
| `EFFECT_RECOVER_MP` | [Number](Number.md) | [static] MP recovery |
| `EFFECT_GAIN_TP` | [Number](Number.md) | [static] TP increase |
| `EFFECT_ADD_STATE` | [Number](Number.md) | [static] Add state |
| `EFFECT_REMOVE_STATE` | [Number](Number.md) | [static] Remove state |
| `EFFECT_ADD_BUFF` | [Number](Number.md) | [static] Buff |
| `EFFECT_ADD_DEBUFF` | [Number](Number.md) | [static] Debuff |
| `EFFECT_REMOVE_BUFF` | [Number](Number.md) | [static] Remove buff |
| `EFFECT_REMOVE_DEBUFF` | [Number](Number.md) | [static] Remove debuff |
| `EFFECT_SPECIAL` | [Number](Number.md) | [static] Special effect |
| `EFFECT_GROW` | [Number](Number.md) | [static] Growth |
| `EFFECT_LEARN_SKILL` | [Number](Number.md) | [static] Learn skill |
| `EFFECT_COMMON_EVENT` | [Number](Number.md) | [static] Common event |
| `SPECIAL_EFFECT_ESCAPE` | [Number](Number.md) | [static] Special effect - Escape |
| `HITTYPE_CERTAIN` | [Number](Number.md) | [static] Certain hit |
| `HITTYPE_PHYSICAL` | [Number](Number.md) | [static] Physical attack |
| `HITTYPE_MAGICAL` | [Number](Number.md) | [static] Magical attack |
| `_subjectActorId` | [Number](Number.md) | Actor ID of the subject |
| `_subjectEnemyIndex` | [Number](Number.md) | Enemy index of the subject |
| `_targetIndex` | [Number](Number.md) | Target index |
| `_forcing` | Boolean | Is it a forced action? |
| `_item` | [Game_Item](Game_Item.md) | Skill or item |


### Methods

#### (static) initialize (subject, forcing)
Initialization during object creation.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `forcing` | Boolean | Is it a forced action? |


#### apply (target)
Applies the result ([Game_ActionResult](Game_ActionResult.md)) to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### applyCritical (damage) → {[Number](Number.md)}
Applies a [critical] attack with the specified damage.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `damage` | [Number](Number.md) | Damage amount |


#### applyGlobal ()
Extracts the [common events] included in [usage effects] and stores them in [$GameTemp](global.md#gametemp-game_temp) ([Game_Temp](Game_Temp.md)).


#### applyGuard (damage, target) → {[Number](Number.md)}
The target battler defends against the specified damage, returning the damage reduced by the defense.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `damage` | [Number](Number.md) | Damage amount |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### applyItemEffect (target, effect)
Applies the effect to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | Effect |


#### applyItemUserEffect (target)
Applies the item effect to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### applyVariance (damage, variance) → {[Number](Number.md)}
Returns the damage after applying the [variance] to the specified damage.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `damage` | [Number](Number.md) | Damage amount |
| `variance` | [Number](Number.md) | [Variance] % (0 to 100) |


#### calcElementRate (target) → {[Number](Number.md)}
Returns the effect rate of the [element] against the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

#### checkDamageType (list) → {Boolean}
Checks if the damage type of the _item property exists in the specified array.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `list` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of damage [[types](RPG.Damage.md#type)] |


#### checkItemScope (list) → {Boolean}
Checks if the [scope] of the _item property exists in the specified array.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `list` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of [[scopes](RPG.UsableItem.md#scope)] |


#### clear ()
Clears the item and target ID.


#### confusionTarget () → {[Game_Battler](Game_Battler.md)}
Selects and returns the target battler when confused.


#### decideRandomTarget ()
Randomly determines a target based on the [scope].


#### elementsMaxRate (target, elements) → {[Number](Number.md)}
Returns the maximum [resistance - attribute effectiveness] of the specified attribute against the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `elements` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of [attribute IDs](RPG.Damage.md#attribute-id) |


#### evalDamageFormula (target) → {[Number](Number.md)}
Applies the [[damage]](RPG.Damage.md) [formula] and returns the damage amount.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler (b in the [formula]) |


#### evaluate () → {[Number](Number.md)}
Applies effects to all targets and returns the total damage amount.


#### evaluateWithTarget (target) → {[Number](Number.md)}
Applies effects to the specified target and returns the damage amount.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### executeDamage (target, value)
Deals damage to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `value` | [Number](Number.md) | Damage amount |


#### executeHpDamage (target, value)
Deals HP damage to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `value` | [Number](Number.md) | HP damage amount |


#### executeMpDamage (target, value)
Deals MP damage to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `value` | [Number](Number.md) | MP damage amount |


#### friendsUnit () → {[Game_Unit](Game_Unit.md)}
Returns the allied party.


#### gainDrainedHp (value)
Returns the HP absorbed from the enemy.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `value` | [Number](Number.md) | HP recovery amount |


#### gainDrainedMp (value)
Returns the MP absorbed from the enemy.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `value` | [Number](Number.md) | MP recovery amount |


#### hasItemAnyValidEffects (target) → {Boolean}
Checks if the specified target can trigger any [[usage effects](RPG.Effect.md)].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### isAttack () → {Boolean}
Checks if the action is an [attack].


#### isCertainHit () → {Boolean}
Checks if the [[hit type](RPG.UsableItem.md#hit-type)] is a [certain hit].


#### isDamage () → {Boolean}
Checks if the damage [[type](RPG.Damage.md#type)] is [HP damage] or [MP damage].


#### isDrain () → {Boolean}
Checks if the damage [[type](RPG.Damage.md#type)] is [HP drain] or [MP drain].


#### isForAll () → {Boolean}
Checks if the [[scope](RPG.UsableItem.md#scope)] targets all, regardless of allies or enemies, including incapacitated ones.


#### isForEveryone () → {Boolean}
**@MZ** Checks if the [[scope](RPG.UsableItem.md#scope)] targets all surviving allies.


#### isForEveryone () → {Boolean}
**@MZ** Checks if the [[scope](RPG.UsableItem.md#scope)] targets all allies without conditions.


#### isForDeadFriend () → {Boolean}
Checks if the [[scope](RPG.UsableItem.md#scope)] targets incapacitated allies.


#### isForFriend () → {Boolean}
Checks if the [[scope](RPG.UsableItem.md#scope)] targets allies (including oneself).


#### isForOne () → {Boolean}
Checks if the [[scope](RPG.UsableItem.md#scope)] targets a single entity, regardless of allies or enemies (not including multiple hits).


#### isForOpponent () → {Boolean}
Checks if the [[scope](RPG.UsableItem.md#scope)] targets a single enemy (including multiple hits).


#### isForRandom () → {Boolean}
Checks if the [[scope](RPG.UsableItem.md#scope)] targets a random enemy.


#### isForUser () → {Boolean}
Checks if the [[scope](RPG.UsableItem.md#scope)] targets oneself.


#### isGuard () → {Boolean}
Checks if the action is [guard].


#### isHpEffect () → {Boolean}
Checks if the damage [[type](RPG.Damage.md#type)] is related to HP.

#### isHpRecover () → {Boolean}
Checks if the damage [[type](RPG.Damage.md#type)] is [HP recovery].


#### isItem () → {Boolean}
Checks if it is an [item].


#### isMagical () → {Boolean}
Checks if the [[hit type](RPG.UsableItem.md#hit-type)] is [magical attack].


#### isMagicSkill () → {Boolean}
Checks if it is a [magic] skill.


#### isMpEffect () → {Boolean}
Checks if the damage [[type](RPG.Damage.md#type)] is related to MP.


#### isMpRecover () → {Boolean}
Checks if the damage [[type](RPG.Damage.md#type)] is [MP recovery].


#### isPhysical () → {Boolean}
Checks if the [[hit type](RPG.UsableItem.md#hit-type)] is [physical attack].


#### isRecover () → {Boolean}
Checks if the damage [[type](RPG.Damage.md#type)] is [MP recovery].


#### isSkill () → {Boolean}
Checks if it is a [skill].


#### isValid () → {Boolean}
Checks if it is possible to act.


#### item () → {[RPG.UsableItem](RPG.UsableItem.md)}
Returns an object that describes the action's information.<br />
This is used in a sense closer to an item than a tool, and is applied to attacks, skills, and more.


#### itemCnt (target) → {[Number](Number.md)}
Returns the [counter rate] of the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### itemCri (target) → {[Number](Number.md)}
Returns the [critical rate] of the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### itemEffectAddAttackState (target, effect)
Adds an attack [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectAddBuff (target, effect)
Adds a [buff] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectAddDebuff (target, effect)
Adds a [debuff] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectAddNormalState (target, effect)
Adds a normal [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectAddState (target, effect)
Adds a [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectCommonEvent (target, effect)
Adds a [common event] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectGainTp (target, effect)
Adds a [TP increase] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectGrow (target, effect)
Adds a [growth] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectLearnSkill (target, effect)
Adds a [skill acquisition] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |

#### itemEffectRecoverHp (target, effect)
Adds an [HP recovery] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectRecoverMp (target, effect)
Adds an [MP recovery] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectRemoveBuff (target, effect)
Adds a [remove buff] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectRemoveDebuff (target, effect)
Adds a [remove debuff] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectRemoveState (target, effect)
Adds a [remove state] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEffectSpecial (target, effect)
Adds a [special effect] [usage effect] to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### itemEva (target) → {[Number](Number.md)}
Returns the [evasion rate] of the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### itemHit (target) → {[Number](Number.md)}
Returns the [hit rate] of the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### itemMrf (target) → {[Number](Number.md)}
Returns the [magic reflection rate] of the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### itemTargetCandidates () → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns an array of potential target battlers.


#### lukEffectRate (target) → {[Number](Number.md)}
Returns the application rate of [luck] for the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### makeDamageValue (target, critical) → {[Number](Number.md)}
Calculates and returns the damage amount to the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `critical` | Boolean | Is it [critical]? |


#### makeSuccess (target)
Sets a success flag for the specified target's action for the action result.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### makeTargets () → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns an array of potential target battlers.


#### needsSelection () → {Boolean}
Checks if the [[range](RPG.UsableItem.md#range)] requires selection for a single target.


#### numRepeats () → {[Number](Number.md)}
Returns the number of repeat actions.


#### numTargets () → {[Number](Number.md)}
Returns the number of single attack targets.


#### opponentsUnit () → {[Game_Unit](Game_Unit.md)}
Returns the opposing group.


#### prepare ()
Prepares (only sets [confusion] by default)


#### repeatTargets (targets) → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns an array of targets for repeat actions.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `targets` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | Array of target battlers |


#### setAttack ()
Sets [attack] for the action.


#### setConfusion ()
Sets [confusion] for the action.


#### setEnemyAction (action)
Sets the specified [action pattern] for the enemy.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `action` | [RPG.Enemy.Action](RPG.Enemy.Action.md) | [Action pattern] |


#### setGuard ()
Sets [guard] for the action.


#### setItem (itemId)
Sets an [item] for the action.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `itemId` | [Number](Number.md) | Item ID |


#### setItemObject (object)
Sets an [item][skill] for the action.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `object` | [RPG.UsableItem](RPG.UsableItem.md) | Item or skill |


#### setSkill (skillId)
Sets a [skill] for the action.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `skillId` | [Number](Number.md) | [Skill ID](RPG.Skill.md#skill-id) |


#### setSubject (subject)
Changes the specified action subject.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Action subject battler |


#### setTarget (targetIndex)
Sets the action target by specified number.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `targetIndex` | [Number](Number.md) | Target number |


#### speed () → {[Number](Number.md)}
Returns the speed.


#### subject () → {[Game_Battler](Game_Battler.md)}
Returns the action subject.


#### targetsForAlive (unit) → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
**@MZ** Returns an array of living battlers.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `unit` | [Game_Unit](Game_Unit.md) | Target unit (enemy or ally) |


#### targetsForDead (unit) → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
**@MZ** Returns an array of incapacitated battlers.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `unit` | [Game_Unit](Game_Unit.md) | Target unit (enemy or ally) |


#### targetsForDeadAndAlive (unit) → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
**@MZ** Returns an array of incapacitated and living battlers.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `unit` | [Game_Unit](Game_Unit.md) | Target unit (enemy or ally) |


#### targetsForEveryone () → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
**@MZ** Returns an array of all battlers.


#### targetsForFriends () → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns an array of ally battlers.


#### targetsForOpponents () → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns an array of enemy battlers.


#### testApply (target) → {Boolean}
Tests the application of the action on the target and checks if it is executable.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### testLifeAndDeath (target) → {Boolean}
**@MZ** Checks if the state of incapacitation or life is applicable for the skill or item.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### testItemEffect (target, effect) → {Boolean}
Tests the application of [usage effect] on the target and checks if it is executable.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
| `effect` | [RPG.Effect](RPG.Effect.md) | [Usage effect] |


#### updateLastSubject ()
**@MZ** Updates the last battler that acted.


#### updateLastUsed ()
**@MZ** Updates the last used skill or item.


#### updateLastTarget (target)
**@MZ** Updates the last targeted battler.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |
