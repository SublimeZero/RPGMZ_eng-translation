[Class Tree](index.md)

# Class: Game_Battler

## Superclass: [Game_BattlerBase](Game_BattlerBase.md)

Controls the icons and actions of battlers in the battle scene.

In MZ, animation control for non-weapon items has been removed, and many properties and methods related to time progress battles have been added.

Changes were made in v1.1.0 and v1.2.0.

### new Game_Battler ()

### Subclasses

* [Game_Actor](Game_Actor.md)
* [Game_Enemy](Game_Enemy.md)


### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_actions` | [Array](Array.md).&lt;[Game_Action](Game_Action.md)&gt; | Array of actions |
| `_speed` | [Number](Number.md) | Speed (determines action order) |
| `_result` | [Game_ActionResult](Game_ActionResult.md) | Result of the action |
| `_actionState` | [String](String.md) | [Action state](#action-state) |
| `_lastTargetIndex` | [Number](Number.md) | Last target index |
| `_damagePopup` | Boolean | Whether to show damage popup |
| `_effectType` | [String](String.md) | Effect type |
| `_motionType` | [String](String.md) | Motion type |
| `_weaponImageId` | [Number](Number.md) | Weapon image ID |
| `_motionRefresh` | Boolean | Whether to refresh motion |
| `_selected` | Boolean | Whether selected |
| `_tpbState` | [String](String.md) | [Time progress battle state](#time-progress-battle-state) |
| `_tpbChargeTime` | [Number](Number.md) | Time progress battle charge time |
| `_tpbCastTime` | [Number](Number.md) | Time progress battle cast time |
| `_tpbIdleTime` | [Number](Number.md) | Time progress battle idle time |
| `_tpbTurnCount` | [Number](Number.md) | Time progress battle turn count |
| `_tpbTurnEnd` | Boolean | Whether time progress battle turn has ended |

#### Action States

| String | Description |
| --- | --- |
| "undecided" | Action undecided |
| "inputting" | Inputting |
| "waiting" | Waiting state |
| "acting" | Acting |

#### Time Progress Battle States

| String | Description |
| --- | --- |
| "charging" | Charging |
| "casting" | Casting |
| "acting" | Acting |
| "charged" | Charged |
| "ready" | Ready |


### Deprecated MV Property
`_animations`


### Inherited Methods from Superclass

#### [Game_BattlerBase](Game_BattlerBase.md)

* [actionPlusSet ()](Game_BattlerBase.md#actionplusset---arraynumber)
* [addedSkills ()](Game_BattlerBase.md#addedskills---arraynumber)
* [addedSkillTypes ()](Game_BattlerBase.md#addedskilltypes---arraynumber)
* [addNewState (stateId)](Game_BattlerBase.md#addnewstate-stateid)
* [addParam (paramId, value)](Game_BattlerBase.md#addparam-paramid-value)
* [allIcons ()](Game_BattlerBase.md#allicons---arraynumber)
* [allTraits ()](Game_BattlerBase.md#alltraits---arrayrpgtrait)
* [appear ()](Game_BattlerBase.md#appear-)
* [attackElements ()](Game_BattlerBase.md#attackelements---arraynumber)
* [attackSkillId ()](Game_BattlerBase.md#attackskillid---number)
* [attackSpeed ()](Game_BattlerBase.md#attackspeed---number)
* [attackStates ()](Game_BattlerBase.md#attackstates---arraynumber)
* [attackStatesRate (stateId)](Game_BattlerBase.md#attackstatesrate-stateid)
* [attackTimesAdd ()](Game_BattlerBase.md#attacktimesadd---number)
* [buff (paramId)](Game_BattlerBase.md#buff-paramid--number)
* [buffIconIndex (buffLevel, paramId)](Game_BattlerBase.md#bufficonindex-bufflevel-paramid--number)
* [buffIcons ()](Game_BattlerBase.md#bufficons---arraynumber)
* [buffLength ()](Game_BattlerBase.md#bufflength---number)
* [canAttack ()](Game_BattlerBase.md#canattack---boolean)
* [canEquip (item)](Game_BattlerBase.md#canequip-item--boolean)
* [canEquipArmor (item)](Game_BattlerBase.md#canequiparmor-item--boolean)
* [canEquipWeapon (item)](Game_BattlerBase.md#canequipweapon-item--boolean)
* [canGuard ()](Game_BattlerBase.md#canguard---boolean)
* [canInput ()](Game_BattlerBase.md#caninput---boolean)
* [canMove ()](Game_BattlerBase.md#canmove---boolean)
* [canPaySkillCost (skill)](Game_BattlerBase.md#canpayskillcost-skill--boolean)
* [canUse (item)](Game_BattlerBase.md#canuse-item--boolean)
* [clearBuffs ()](Game_BattlerBase.md#clearbuffs-)
* [clearParamPlus ()](Game_BattlerBase.md#clearparamplus-)
* [clearStates ()](Game_BattlerBase.md#clearstates-)
* [collapseType ()](Game_BattlerBase.md#collapsetype---number)
* [confusionLevel ()](Game_BattlerBase.md#confusionlevel---number)
* [deathStateId ()](Game_BattlerBase.md#deathstateid---number)
* [debuffRate (paramId)](Game_BattlerBase.md#debuffrate-paramid--number)
* [decreaseBuff (paramId)](Game_BattlerBase.md#decreasebuff-paramid)
* [die ()](Game_BattlerBase.md#die-)
* [elementRate (elementId)](Game_BattlerBase.md#elementrate-elementid--number)
* [eraseBuff (paramId)](Game_BattlerBase.md#erasebuff-paramid)
* [eraseState (stateId)](Game_BattlerBase.md#erasestate-stateid)
* [guardSkillId ()](Game_BattlerBase.md#guardskillid---number)
* [hide ()](Game_BattlerBase.md#hide-)
* [hpRate ()](Game_BattlerBase.md#hprate---number)
* [increaseBuff (paramId)](Game_BattlerBase.md#increasebuff-paramid)
* [isActor ()](Game_BattlerBase.md#isactor---boolean)
* [isAlive ()](Game_BattlerBase.md#isalive---boolean)
* [isAppeared ()](Game_BattlerBase.md#isappeared---boolean)
* [isAutoBattle ()](Game_BattlerBase.md#isautobattle---boolean)
* [isBuffAffected (paramId)](Game_BattlerBase.md#isbuffaffected-paramid---boolean)
* [isBuffExpired (paramId)](Game_BattlerBase.md#isbuffexpired-paramid---boolean)
* [isBuffOrDebuffAffected (paramId)](Game_BattlerBase.md#isbuffordebuffaffected-paramid---boolean)
* [isConfused ()](Game_BattlerBase.md#isconfused---boolean)
* [isDead ()](Game_BattlerBase.md#isdead---boolean)
* [isDeathStateAffected ()](Game_BattlerBase.md#isdeathstateaffected---boolean)
* [isDebuffAffected (paramId)](Game_BattlerBase.md#isdebuffaffected-paramid---boolean)
* [isDualWield ()](Game_BattlerBase.md#isdualwield---boolean)
* [isDying ()](Game_BattlerBase.md#isdying---boolean)
* [isEnemy ()](Game_BattlerBase.md#isenemy---boolean)
* [isEquipAtypeOk (atypeId)](Game_BattlerBase.md#isequipatypeok-atypeid--boolean)
* [isEquipTypeLocked (etypeId)](Game_BattlerBase.md#isequiptypelocked-etypeid--boolean)
* [isEquipTypeSealed (etypeId)](Game_BattlerBase.md#isequiptypesealed-etypeid--boolean)
* [isEquipWtypeOk (wtypeId)](Game_BattlerBase.md#isequipwtypeok-wtypeid--boolean)
* [isGuard ()](Game_BattlerBase.md#isguard---boolean)
* [isHidden ()](Game_BattlerBase.md#ishidden---boolean)
* [isMaxBuffAffected (paramId)](Game_BattlerBase.md#ismaxbuffaffected-paramid--boolean)
* [isMaxDebuffAffected (paramId)](Game_BattlerBase.md#ismaxdebuffaffected-paramid--boolean)
* [isOccasionOk (item)](Game_BattlerBase.md#isoccasionok-item--boolean)
* [isPreserveTp ()](Game_BattlerBase.md#ispreservetp---boolean)
* [isRestricted ()](Game_BattlerBase.md#isrestricted---boolean)
* [isSkillSealed (stypeId)](Game_BattlerBase.md#isskillsealed-stypeid--boolean)
* [isSkillTypeSealed (stypeId)](Game_BattlerBase.md#isskilltypesealed-stypeid--boolean)
* [isSkillWtypeOk (skill)](Game_BattlerBase.md#isskillwtypeok-skill--boolean)
* [isStateAffected (stateId)](Game_BattlerBase.md#isstateaffected-stateid--boolean)
* [isStateExpired (stateId)](Game_BattlerBase.md#isstateexpired-stateid--boolean)
* [isStateResist (stateId)](Game_BattlerBase.md#isstateresist-stateid--boolean)
* [isSubstitute ()](Game_BattlerBase.md#issubstitute---boolean)
* [maxTp ()](Game_BattlerBase.md#maxtp---number)
* [meetsItemConditions (item)](Game_BattlerBase.md#Game_BattlerBase.md#meetsitemconditions-item--boolean)
* [meetsSkillConditions (skill)](Game_BattlerBase.md#meetsskillconditions-skill--boolean)
* [meetsUsableItemConditions (item)](Game_BattlerBase.md#meetsusableitemconditions-item--boolean)
* [mostImportantStateText ()](Game_BattlerBase.md#mostimportantstatetext---string)
* [mpRate ()](Game_BattlerBase.md#mprate---number)
* [overwriteBuffTurns (paramId, turns)](Game_BattlerBase.md#overwritebuffturns-paramid-turns)
* [param (paramId)](Game_BattlerBase.md#param-paramid--number)
* [paramBase (paramId)](Game_BattlerBase.md#parambase-paramid--number)
* [paramBuffRate (paramId)](Game_BattlerBase.md#parambuffrate-paramid--number)
* [paramMax (paramId)](Game_BattlerBase.md#parammax-paramid--number)
* [paramMin (paramId)](Game_BattlerBase.md#parammin-paramid--number)
* [paramPlus (paramId)](Game_BattlerBase.md#paramplus-paramid--number)
* [paramRate (paramId)](Game_BattlerBase.md#paramrate-paramid--number)
* [partyAbility (abilityId)](Game_BattlerBase.md#partyability-abilityid--boolean)
* [paySkillCost (skill)](Game_BattlerBase.md#payskillcost-skill)
* [recoverAll ()](Game_BattlerBase.md#recoverall-)
* [refresh ()](Game_BattlerBase.md#refresh-)
* [resetStateCounts (stateId)](Game_BattlerBase.md#resetstatecounts-stateid)
* [restriction ()](Game_BattlerBase.md#restriction---number)
* [revive ()](Game_BattlerBase.md#revive-)
* [setHp (hp)](Game_BattlerBase.md#sethp-hp)
* [setMp (mp)](Game_BattlerBase.md#setmp-mp)
* [setTp (tp)](Game_BattlerBase.md#settp-tp)
* [skillMpCost (skill)](Game_BattlerBase.md#skillmpcost-skill--number)
* [skillTpCost (skill)](Game_BattlerBase.md#skilltpcost-skill--number)
* [slotType ()](Game_BattlerBase.md#slottype---number)
* [sortStates ()](Game_BattlerBase.md#sortstates-)
* [specialFlag (flagId)](Game_BattlerBase.md#specialflag-flagid--boolean)
* [stateIcons ()](Game_BattlerBase.md#stateicons---arraynumber)
* [stateMotionIndex ()](Game_BattlerBase.md#statemotionindex---number)
* [stateOverlayIndex ()](Game_BattlerBase.md#stateoverlayindex---number)
* [stateRate (stateId)](Game_BattlerBase.md#staterate-stateid--number)
* [stateResistSet ()](Game_BattlerBase.md#stateresistset---arraynumber)
* [states ()](Game_BattlerBase.md#states---arrayrpgstate)
* [tpRate ()](Game_BattlerBase.md#tprate---number)
* [traitObjects ()](Game_BattlerBase.md#traitobjects---array)
* [traits (code)](Game_BattlerBase.md#traits-code--arrayrpgtrait)
* [traitsPi (code, id)](Game_BattlerBase.md#traitspi-code-id--number)
* [traitsSet (code)](Game_BattlerBase.md#traitsset-code--arraynumber)
* [traitsSum (code, id)](Game_BattlerBase.md#traitssum-code-id--number)
* [traitsSumAll (code)](Game_BattlerBase.md#traitssumall-code--number)
* [traitsWithId (code, id)](Game_BattlerBase.md#traitswithid-code-id--arrayrpgtrait)
* [updateBuffTurns ()](Game_BattlerBase.md#updatebuffturns-)
* [updateStateTurns ()](Game_BattlerBase.md#updatestateturns-)
* [xparam (xparamId)](Game_BattlerBase.md#xparam-xparamid--number)

### Methods

#### action (index) → {[Game_Action](Game_Action.md)}
Returns the action with the specified index.

##### Arguments

| Name   | Type               | Description    |
| ------ | ------------------| ---------------|
| `index`| [Number](Number.md)| Action number  |


#### addBuff (paramId, turns)
Adds a [buff] to the specified normal ability for a specified number of turns.

##### Arguments

| Name     | Type               | Description                     |
| -------- | ------------------| --------------------------------|
| `paramId`| [Number](Number.md)| [Ability ID](RPG.Enemy.md#ability-id) |
| `turns`  | [Number](Number.md)| Number of turns                |


#### addDebuff (paramId, turns)
Adds a [debuff] to the specified normal ability for a specified number of turns.

##### Arguments

| Name     | Type               | Description                     |
| -------- | ------------------| --------------------------------|
| `paramId`| [Number](Number.md)| [Ability ID](RPG.Enemy.md#ability-id) |
| `turns`  | [Number](Number.md)| Number of turns                |


#### addState (stateId)
Adds the specified state.

##### Arguments

| Name     | Type               | Description                     |
| -------- | ------------------| --------------------------------|
| `stateId`| [Number](Number.md)| [State ID](RPG.State.md#state-id) |


#### applyTpbPenalty ()
**@MZ** Applies a penalty in time progress combat.


#### cancelMotionRefresh ()
**@MZ1.2.0** Sets to not update motion.


#### canInput () → {Boolean}
**@MZ** Checks if input is possible in time progress combat.


#### chargeTpByDamage (damageRate)
Increases TP according to the damage rate.

##### Arguments

| Name        | Type               | Description                              |
| ----------- | ------------------| -----------------------------------------|
| `damageRate`| [Number](Number.md)| (Damage percentage with maximum HP as 1) |


#### clearActions ()
Clears actions.


#### clearDamagePopup ()
Clears damage popups.


#### clearEffect ()
Clears effects.


#### clearMotion ()
Clears motion.


#### clearTp ()
Sets TP to 0.


#### clearTpbChargeTime ()
**@MZ** Clears charge time in time progress combat.


#### clearWeaponAnimation ()
Clears weapon animation.


#### consumeItem (item)
Consumes the specified item.

##### Arguments

| Name   | Type                             | Description |
| ------ | -------------------------------- | ----------- |
| `item` | [RPG.UsableItem](RPG.UsableItem.md) | Item        |


#### currentAction () → {[Game_Action](Game_Action.md)}
Returns the current action.


#### deselect ()
Deselects.


#### effectType () → {[String](String.md)}
Returns the effect type.


#### escape ()
Escapes from combat.


#### finishTpbCharge ()
**@MZ** Completes charge in time progress combat.


#### forceAction (skillId, targetIndex)
Forcibly executes the specified skill.

##### Arguments

| Name        | Type               | Description                       |
| ----------- | ------------------| ---------------------------------|
| `skillId`   | [Number](Number.md)| [Skill ID](RPG.Skill.md#skill-id) |
| `targetIndex`| [Number](Number.md)| Target number                    |


#### gainHp (value)
Recovers the specified amount of HP.

##### Arguments

| Name   | Type               | Description      |
| ------ | ------------------| -----------------|
| `value`| [Number](Number.md)| Amount of HP recovery |


#### gainMp (value)
Recovers the specified amount of MP.

##### Arguments

| Name   | Type               | Description      |
| ------ | ------------------| -----------------|
| `value`| [Number](Number.md)| Amount of MP recovery |


#### gainSilentTp (value)
Recovers the specified amount of TP without displaying it.

##### Arguments

| Name   | Type               | Description      |
| ------ | ------------------| -----------------|
| `value`| [Number](Number.md)| Amount of TP recovery |


#### gainTp (value)
Recovers the specified amount of TP.

##### Arguments

| Name   | Type               | Description      |
| ------ | ------------------| -----------------|
| `value`| [Number](Number.md)| Amount of TP recovery |


#### initialize ()
Override: [Game_BattlerBase](Game_BattlerBase.md#initialize-)


#### initMembers ()
Override: [Game_BattlerBase](Game_BattlerBase.md#initmembers-)


#### initTp ()
Initializes TP to a random value up to 25.


#### initTpbChargeTime (advantageous)
**@MZ** Initializes charge time in time progress combat.

##### Arguments

| Name        | Type      | Description                     |
| ----------- | --------- | ------------------------------- |
| `advantageous`| Boolean | Whether there is an advantage   |


#### initTpbTurn ()
**@MZ** Initializes the turn in time progress combat.


#### isActing () → {Boolean}
Checks if currently acting.


#### isChanting () → {Boolean}
Checks if currently chanting a spell.


#### isDamagePopupRequested () → {Boolean}
Checks if a damage popup is requested.


#### isEffectRequested () → {Boolean}
Checks if an effect is requested.


#### isGuardWaiting () → {Boolean}
Checks if currently waiting while [guarding].


#### isInputting () → {Boolean}
Checks if currently inputting combat commands.


#### isMotionRefreshRequested () → {Boolean}
Checks if motion initialization is requested.


#### isMotionRequested () → {Boolean}
Checks if motion is requested.


#### isSelected () → {Boolean}
Checks if currently selected.


#### isStateAddable (stateId) → {Boolean}
Checks if the specified state can be added.

##### Arguments

| Name    | Type               | Description            |
| ------- | ------------------| -----------------------|
| `stateId` | [Number](Number.md) | [State ID](RPG.State.md#state-id) |


#### isStateRestrict (stateId) → {Boolean}
Checks if the specified state is [released by action restriction] and if currently under action restriction.

##### Arguments

| Name    | Type               | Description            |
| ------- | ------------------| -----------------------|
| `stateId` | [Number](Number.md) | [State ID](RPG.State.md#state-id) |


#### isTpbCharged () → {Boolean}
**@MZ** Checks if the charge is complete in time progress combat.


#### isTpbReady () → {Boolean}
**@MZ** Checks if it is in a ready state in time progress combat.


#### isTpbTimeout () → {Boolean}
**@MZ** Checks if it has timed out in time progress combat.


#### isTpbTurnEnd () → {Boolean}
**@MZ** Checks if the turn has ended in time progress combat.


#### isUndecided () → {Boolean}
Checks if the action is undecided.


#### isWaiting () → {Boolean}
Checks if currently waiting.


#### isWeaponAnimationRequested () → {Boolean}
Checks if a weapon animation is requested.


#### makeActions ()
Generates animations.


#### makeActionTimes () → {[Number](Number.md)}
Sets and returns the number of actions.


#### makeSpeed ()
Sets the speed (determines the action order).


#### makeTpbActions ()
**@MZ** Generates actions in time progress combat.


#### maxSlipDamage () → {[Number](Number.md)}
Returns the maximum slip damage amount.


#### motionType () → {[String](String.md)}
Returns the action type.


#### numActions () → {[Number](Number.md)}
Returns the action number.


#### onAllActionsEnd ()
Handler for when all actions end.


#### onBattleEnd ()
Handler for when the battle ends.


#### onBattleStart (advantageous)
Handler for when the battle starts.

##### Arguments

| Name          | Type      | Description                     |
| ------------- | --------- | ------------------------------- |
| `advantageous`| Boolean   | **@MZ** Whether there is an advantage |


#### onDamage (value)
Handler for taking damage.

##### Arguments

| Name   | Type               | Description        |
| ------ | ------------------| -------------------|
| `value`| [Number](Number.md)| Amount of HP damage |


#### onRestrict ()
Override: [Game_BattlerBase](Game_BattlerBase.md#onrestrict-)


#### onTpbCharged ()
**@MZ** Handler for when the charge is complete in time progress combat.


#### onTpbTimeout ()
**@MZ** Handler for when the timeout occurs in time progress combat.


#### onTurnEnd ()
Handler for when the turn ends.


#### performAction (action)
Executes the specified action.

##### Arguments

| Name   | Type               | Description            |
| ------ | ------------------| -----------------------|
| `action`| [Game_Action](Game_Action.md) | Action               |


#### performActionEnd ()
Executes the end of the action.


#### performActionStart (action)
Executes the start of the specified action.

##### Arguments

| Name   | Type               | Description            |
| ------ | ------------------| -----------------------|
| `action`| [Game_Action](Game_Action.md) | Action               |


#### performCollapse ()
Executes the collapse action.


#### performCounter ()
Executes the counter action.


#### performDamage ()
Executes the damage action.


#### performEvasion ()
Executes the evasion action.


#### performMagicEvasion ()
Executes the magic evasion action.


#### performMiss ()
Executes the miss action.


#### performRecovery ()
Executes the recovery action.


#### performReflection ()
Executes the magic reflection action.


#### performSubstitute (target)
Executes the substitute action.

##### Arguments

| Name   | Type               | Description            |
| ------ | ------------------| -----------------------|
| `target`| [Game_Battler](Game_Battler.md) | Substitute target      |


#### refresh ()
Override: [Game_BattlerBase](Game_BattlerBase.md)


#### regenerateAll ()
Applies automatic recovery and damage.


#### regenerateHp ()
Applies HP automatic recovery.


#### regenerateMp ()
Applies MP automatic recovery.


#### regenerateTp ()
Applies TP automatic recovery.


#### removeAllBuffs ()
Removes all [buffs] to abilities.


#### removeBattleStates ()
Removes states.


#### removeBuff (paramId)
Removes the [buff] from the specified normal ability.

##### Arguments

| Name     | Type               | Description                   |
| -------- | ------------------| -------------------------------|
| `paramId`| [Number](Number.md)| [Ability ID](RPG.Enemy.md#ability-id) |


#### removeBuffsAuto ()
Removes [buffs] and [debuffs] that have ended their turns.


#### removeCurrentAction ()
Removes the current action.

#### removeState (stateId)
Removes the specified state.

##### Arguments

| Name    | Type               | Description            |
| ------- | ------------------| -----------------------|
| `stateId` | [Number](Number.md) | [State ID](RPG.State.md#state-id) |


#### removeStatesAuto (timing)
Removes states based on specified conditions.

##### Arguments

| Name    | Type               | Description            |
| ------- | ------------------| -----------------------|
| `timing` | [Number](Number.md) | Condition for removal (1: at the end of action, 2: at the end of turn) |


#### removeStatesByDamage ()
Removes states [released by damage].


#### requestEffect (effectType)
Requests the specified effect.

##### Arguments

| Name       | Type               | Description         |
| ---------- | ------------------| --------------------|
| `effectType` | [String](String.md) | Effect type        |


#### requestMotion (motionType)
Requests the specified motion.

##### Arguments

| Name        | Type               | Description         |
| ----------- | ------------------| --------------------|
| `motionType`| [String](String.md) | Motion type        |


#### requestMotionRefresh ()
Requests the initialization of motion.


#### result () → {[Game_ActionResult](Game_ActionResult.md)}
Returns the result of the action.


#### select ()
Selection of the battler.


#### setAction (index, action)
Sets the action for the specified battler.

##### Arguments

| Name    | Type               | Description            |
| ------- | ------------------| -----------------------|
| `index` | [Number](Number.md) | Battler number       |
| `action`| [Game_Action](Game_Action.md) | Action               |


#### setActionState (actionState)
Sets the specified action state.

##### Arguments

| Name         | Type               | Description                     |
| ------------ | ------------------| ------------------------------- |
| `actionState`| [String](String.md) | [Action State](Game_Battler.md#action-state) |


#### setLastTarget (target)
Sets the target battler.

##### Arguments

| Name   | Type               | Description            |
| ------ | ------------------| -----------------------|
| `target`| [Game_Battler](Game_Battler.md) | Target battler       |


#### shouldDelayTpbCharge () → {Boolean}
**@MZ** Checks if a delay is needed for charging in time progress combat.


#### speed () → {[Number](Number.md)}
Returns the speed (determines the action order).


#### startDamagePopup ()
Starts the damage popup.


#### startWeaponAnimation (weaponImageId)
Starts the animation for the specified weapon.

##### Arguments

| Name         | Type               | Description            |
| ------------ | ------------------| -----------------------|
| `weaponImageId` | [Number](Number.md) | Weapon ID            |


#### startTpbTurn ()
**@MZ** Starts the turn in time progress combat.


#### shouldPopupDamage () → {Boolean}
**@MZ** Checks if damage popup is needed.


#### tpbChargeTime () → {[Number](Number.md)}
**@MZ** Returns the charge time in time progress combat.


#### startTpbCasting ()
**@MZ** Starts casting in time progress combat.


#### startTpbAction ()
**@MZ** Starts action in time progress combat.


#### tpbAcceleration () → {[Number](Number.md)}
**@MZ** Returns the acceleration in time progress combat.


#### tpbBaseSpeed () → {[Number](Number.md)}
**@MZ** Returns the base speed in time progress combat.


#### tpbRelativeSpeed () → {[Number](Number.md)}
**@MZ** Returns the relative speed in time progress combat.


#### tpbSpeed () → {[Number](Number.md)}
**@MZ** Returns the speed in time progress combat.


#### tpbRequiredCastTime () → {[Number](Number.md)}
**@MZ** Returns the required casting time in time progress combat.


#### turnCount () → {[Number](Number.md)}
**@MZ** Returns the turn count in time progress combat.


#### updateTpb ()
**@MZ** Updates time progress combat.


#### updateTpbAutoBattle ()
**@MZ** Updates auto battle in time progress combat.


#### updateTpbCastTime ()
**@MZ** Updates casting time in time progress combat.


#### updateTpbChargeTime ()
**@MZ** Updates charge time in time progress combat.


#### updateTpbIdleTime ()
**@MZ** Updates idle time in time progress combat.


#### useItem (item)
Uses the specified item.

##### Arguments

| Name   | Type                     | Description       |
| ------ | ------------------------| ------------------|
| `item` | [RPG.UsableItem](RPG.UsableItem.md) | Item            |


#### weaponImageId () → {[Number](Number.md)}
Returns the weapon image ID.


### Deprecated MV Methods
clearAnimations (), isAnimationRequested (), shiftAnimation (), startAnimation (animationId, mirror, delay)
