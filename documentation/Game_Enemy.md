[Class Tree](index.md)

# Class: Game_Enemy

## Superclass: [Game_Battler](Game_Battler.md)

| Database | JSON Data | Sprite |
| --- | --- | --- |
| [Enemy Characters] | [RPG.Enemy](RPG.Enemy.md) | [Sprite_Enemy](Sprite_Enemy.md) |

A class that retrieves parameters for [enemy characters] during combat and sets images.

Changes were made in version 1.5.0.

Related Classes: [RPG.Enemy.Action](RPG.Enemy.Action.md), [Game_Troop](Game_Troop.md), [Game_Actor](Game_Actor.md), [Game_Party](Game_Party.md), [Scene_Battle](Scene_Battle.md), [BattleManager](BattleManager.md), [Window_BattleEnemy](Window_BattleEnemy.md)

### new Game_Enemy ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_enemyId` | [Number](Number.md) | Enemy character ID |
| `_letter` | [String](String.md) | Suffix (A, B, etc.) |
| `_plural` | Boolean | Whether it's a group (two or more) |
| `_screenX` | [Number](Number.md) | X coordinate on the screen |
| `_screenY` | [Number](Number.md) | Y coordinate on the screen |

### Methods Inherited from Superclass

#### [Game_BattlerBase](Game_BattlerBase.md)

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
* [isBuffAffected (paramId)](Game_BattlerBase.md#isbuffaffected-paramid--boolean)
* [isBuffExpired (paramId)](Game_BattlerBase.md#isbuffexpired-paramid--boolean)
* [isBuffOrDebuffAffected (paramId)](Game_BattlerBase.md#isbuffordebuffaffected-paramid--boolean)
* [isConfused ()](Game_BattlerBase.md#isconfused---boolean)
* [isDead ()](Game_BattlerBase.md#isdead---boolean)
* [isDeathStateAffected ()](Game_BattlerBase.md#isdeathstateaffected---boolean)
* [isDebuffAffected (paramId)](Game_BattlerBase.md#isdebuffaffected-paramid--boolean)
* [isDualWield ()](Game_BattlerBase.md#isdualwield---boolean)
* [isDying ()](Game_BattlerBase.md#isdying---boolean)
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
* [paramBuffRate (paramId)](Game_BattlerBase.md#parambuffrate-paramid--number)
* [paramMax (paramId)](Game_BattlerBase.md#parammax-paramid--number)
* [paramMin (paramId)](Game_BattlerBase.md#parammin-paramid--number)
* [paramPlus (paramId)](Game_BattlerBase.md#paramplus-paramid--number)
* [paramRate (paramId)](Game_BattlerBase.md#paramrate-paramid--number)
* [partyAbility (abilityId)](Game_BattlerBase.md#partyability-abilityid--boolean)
* [paySkillCost (skill)](Game_BattlerBase.md#payskillcost-skill)
* [recoverAll ()](Game_BattlerBase.md#recoverall-)
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


#### [Game_Battler](Game_Battler.md)
* [action (index) ](Game_Battler.md#action-index--game_action)
* [addBuff (paramId, turns)](Game_Battler.md#addbuff-paramid-turns)
* [addDebuff (paramId, turns)](Game_Battler.md#adddebuff-paramid-turns)
* [addState (stateId)](Game_Battler.md#addstate-stateid)
* [chargeTpByDamage (damageRate)](Game_Battler.md#chargetpbydamage-damagerate)
* [clearActions ()](Game_Battler.md#clearactions-)
* [clearAnimations ()](Game_Battler.md#clearanimations-)
* [clearDamagePopup ()](Game_Battler.md#cleardamagepopup-)
* [clearEffect ()](Game_Battler.md#cleareffect-)
* [clearMotion ()](Game_Battler.md#clearmotion-)
* [clearTp ()](Game_Battler.md#cleartp-)
* [clearWeaponAnimation ()](Game_Battler.md#clearweaponanimation-)
* [consumeItem (item)](Game_Battler.md#consumeitem-item)
* [currentAction ()](Game_Battler.md#currentaction---game_action)
* [deselect ()](Game_Battler.md#deselect-)
* [effectType ()](Game_Battler.md#effecttype---string)
* [escape ()](Game_Battler.md#escape-)
* [forceAction (skillId, targetIndex)](Game_Battler.md#forceaction-skillid-targetindex)
* [gainHp (value)](Game_Battler.md#gainhp-value)
* [gainMp (value)](Game_Battler.md#gainmp-value)
* [gainSilentTp (value)](Game_Battler.md#gainsilenttp-value)
* [gainTp (value)](Game_Battler.md#gaintp-value)
* [initTp ()](Game_Battler.md#inittp-)
* [isActing ()](Game_Battler.md#isacting---boolean)
* [isAnimationRequested ()](Game_Battler.md#isanimationrequested---boolean)
* [isChanting ()](Game_Battler.md#ischanting---boolean)
* [isDamagePopupRequested ()](Game_Battler.md#isdamagepopuprequested---boolean)
* [isEffectRequested ()](Game_Battler.md#iseffectrequested---boolean)
* [isGuardWaiting ()](Game_Battler.md#isguardwaiting---boolean)
* [isInputting ()](Game_Battler.md#isinputting---boolean)
* [isMotionRefreshRequested ()](Game_Battler.md#ismotionrefreshrequested---boolean)
* [isMotionRequested ()](Game_Battler.md#ismotionrequested---boolean)
* [isSelected ()](Game_Battler.md#isselected---boolean)
* [isStateAddable (stateId)](Game_Battler.md#isstateaddable-stateid--boolean)
* [isStateRestrict (stateId)](Game_Battler.md#isstaterestrict-stateid--boolean)
* [isUndecided ()](Game_Battler.md#isundecided---boolean)
* [isWaiting ()](Game_Battler.md#iswaiting---boolean)
* [isWeaponAnimationRequested ()](Game_Battler.md#isweaponanimationrequested---boolean)
* [makeActionTimes ()](Game_Battler.md#makeactiontimes---number)
* [makeSpeed ()](Game_Battler.md#makespeed-)
* [maxSlipDamage ()](Game_Battler.md#maxslipdamage---number)
* [motionType ()](Game_Battler.md#motiontype---string)
* [numActions ()](Game_Battler.md#numactions---number)
* [onAllActionsEnd ()](Game_Battler.md#onallactionsend-)
* [onBattleEnd ()](Game_Battler.md#onbattleend-)
* [onBattleStart ()](Game_Battler.md#onbattlestart-)
* [onDamage (value)](Game_Battler.md#ondamage-value)
* [onRestrict ()](Game_Battler.md#onrestrict-)
* [onTurnEnd ()](Game_Battler.md#onturnend-)
* [performCounter ()](Game_Battler.md#performcounter-)
* [performEvasion ()](Game_Battler.md#performevasion-)
* [performMagicEvasion ()](Game_Battler.md#performmagicevasion-)
* [performMiss ()](Game_Battler.md#performmiss-)
* [performRecovery ()](Game_Battler.md#performrecovery-)
* [performReflection ()](Game_Battler.md#performreflection-)
* [performSubstitute (target)](Game_Battler.md#performsubstitute-target)
* [refresh ()](Game_Battler.md#refresh-)
* [regenerateAll ()](Game_Battler.md#regenerateall-)
* [regenerateHp ()](Game_Battler.md#regeneratehp-)
* [regenerateMp ()](Game_Battler.md#regeneratemp-)
* [regenerateTp ()](Game_Battler.md#regeneratetp-)
* [removeAllBuffs ()](Game_Battler.md#removeallbuffs-)
* [removeBattleStates ()](Game_Battler.md#removebattlestates-)
* [removeBuff (paramId)](Game_Battler.md#removebuff-paramid)
* [removeBuffsAuto ()](Game_Battler.md#removebuffsauto-)
* [removeCurrentAction ()](Game_Battler.md#removecurrentaction-)
* [removeState (stateId)](Game_Battler.md#removestate-stateid)
* [removeStatesAuto (timing)](Game_Battler.md#removestatesauto-timing)
* [removeStatesByDamage ()](Game_Battler.md#removestatesbydamage-)
* [requestEffect (effectType)](Game_Battler.md#requesteffect-effecttype)
* [requestMotion (motionType)](Game_Battler.md#requestmotion-motiontype)
* [requestMotionRefresh ()](Game_Battler.md#requestmotionrefresh-)
* [result () ](Game_Battler.md#result---game_actionresult)
* [select ()](Game_Battler.md#select-)
* [setAction (index, action)](Game_Battler.md#setaction-index-action)
* [setActionState (actionState)](Game_Battler.md#setactionstate-actionstate)
* [setLastTarget (target)](Game_Battler.md#setlasttarget-target)
* [shiftAnimation ()](Game_Battler.md#shiftanimation---mvbattleranimation)
* [speed ()](Game_Battler.md#speed---number)
* [startAnimation (animationId, mirror, delay)](Game_Battler.md#startanimation-animationid-mirror-delay)
* [startDamagePopup ()](Game_Battler.md#startdamagepopup-)
* [startWeaponAnimation (weaponImageId)](Game_Battler.md#startweaponanimation-weaponimageid)
* [useItem (item)](Game_Battler.md#useitem-item)
* [weaponImageId ()](Game_Battler.md#weaponimageid---number)

### Methods

#### battlerHue () → {[Number](Number.md)}
Returns the hue.

#### battlerName () → {[String](String.md)}
Returns the [name].

#### dropItemRate () → {[Number](Number.md)}
Returns the drop item occurrence rate.

#### enemy () → {[RPG.Enemy](RPG.Enemy.md)}
Returns the database information of the [enemy character].

#### enemyId () → {[Number](Number.md)}
Returns the ID of the [enemy character].

#### exp () → {[Number](Number.md)}
Returns the [experience points] of the [enemy character].

#### friendsUnit () → {[Game_Troop](Game_Troop.md)}
Returns the [enemy group].

#### gold () → {[Number](Number.md)}
Returns the [amount of money].

#### index () → {[Number](Number.md)}
Returns the number of the [enemy character].

#### initialize (enemyId, x, y)
Initializes with the specified [enemy character] and coordinates.
Override: [Game_Battler#initialize]

##### Arguments

| Name       | Type                | Description              |
|------------|---------------------|--------------------------|
| `enemyId`  | [Number](Number.md) | Enemy character ID       |
| `x`        | [Number](Number.md) | X-coordinate             |
| `y`        | [Number](Number.md) | Y-coordinate             |

#### initMembers ()
Override: [Game_Battler](Game_Battler.md#initmembers-)

#### isActionValid (action) → {Boolean}
Checks if the [action pattern] is executable.

##### Arguments

| Name      | Type                              | Description        |
|-----------|-----------------------------------|--------------------|
| `action`  | [RPG.Enemy.Action](RPG.Enemy.Action.md) | [Action pattern]   |

#### isBattleMember () → {Boolean}
Checks if participating in battle.

#### isEnemy () → {Boolean}
Override: [Game_BattlerBase](Game_BattlerBase.md#isenemy---boolean)

#### isLetterEmpty () → {Boolean}
Checks if the name does not have a suffix (A, B, etc.).

#### isSpriteVisible () → {Boolean}
Checks if the image is displayed.

#### itemObject (kind, dataId) → {[RPG.BaseItem](RPG.BaseItem.md)}
Returns the specified item.

##### Arguments

| Name     | Type                | Description             |
|----------|---------------------|-------------------------|
| `kind`   | [Number](Number.md) | Type (1: Item, 2: Weapon, 3: Armor) |
| `dataId` | Number              | Item ID                 |

#### makeActions ()
Override: [Game_Battler](Game_Battler.md#makeactions-)

#### makeDropItems () → {[Array](Array.md).&lt;[RPG.BaseItem](RPG.BaseItem.md)&gt;}
Generates and returns drop items.

#### meetsCondition (action) → {Boolean}
Checks if the [action pattern] meets the [condition].

##### Arguments

| Name     | Type                              | Description        |
|----------|-----------------------------------|--------------------|
| `action` | [RPG.Enemy.Action](RPG.Enemy.Action.md) | [Action pattern]   |

#### meetsHpCondition (param1, param2) → {Boolean}
Checks if it meets the [condition - HP].

##### Arguments

| Name     | Type                | Description            |
|----------|---------------------|------------------------|
| `param1` | [Number](Number.md) | Lower limit HP         |
| `param2` | [Number](Number.md) | Upper limit HP         |

#### meetsMpCondition (param1, param2) → {Boolean}
Checks if it meets the [condition - MP].

##### Arguments

| Name     | Type                | Description            |
|----------|---------------------|------------------------|
| `param1` | [Number](Number.md) | Lower limit MP         |
| `param2` | [Number](Number.md) | Upper limit MP         |

#### meetsPartyLevelCondition (param) → {Boolean}
Checks if it meets the [condition - Party Level].

##### Arguments

| Name     | Type                | Description            |
|----------|---------------------|------------------------|
| `param`  | [Number](Number.md) | Level                  |

#### meetsStateCondition (param) → {Boolean}
Checks if it meets the [condition - State].

##### Arguments

| Name     | Type                | Description                  |
|----------|---------------------|------------------------------|
| `param`  | [Number](Number.md) | [State ID](RPG.State.md#ステートid) |

#### meetsSwitchCondition (param) → {Boolean}
Checks if it meets the [condition - Switch].

##### Arguments

| Name     | Type                | Description |
|----------|---------------------|-------------|
| `param`  | [Number](Number.md) | Switch ID   |

#### meetsTurnCondition (param1, param2) → {Boolean}
Checks if it meets the [condition - Turn].

##### Arguments

| Name     | Type                | Description          |
|----------|---------------------|----------------------|
| `param1` | [Number](Number.md) | Lower limit Turn     |
| `param2` | [Number](Number.md) | Upper limit Turn     |

#### name () → {[String](String.md)}
Returns the name with a suffix.

#### opponentsUnit () → {[Game_Party](Game_Party.md)}
Returns the allied party.

#### originalName () → {[String](String.md)}
Returns the [name].

#### paramBase (paramId) → {[Number](Number.md)}
Override: [Game_BattlerBase](Game_BattlerBase.md#parambase-paramid--number)

#### performAction (action)
Override: [Game_Battler](Game_Battler.md#performaction-action)

#### performActionEnd ()
Override: [Game_Battler](Game_Battler.md#performactionend-)

#### performActionStart (action)
Override: [Game_Battler](Game_Battler.md#performactionstart-action)

#### performCollapse ()
Override: [Game_Battler](Game_Battler.md#performcollapse-)

#### performDamage ()
Override: [Game_Battler](Game_Battler.md#performdamage-)

#### screenX () → {[Number](Number.md)}
Returns the X-coordinate on the screen.

#### screenY () → {[Number](Number.md)}
Returns the Y-coordinate on the screen.

#### selectAction (actionList, ratingZero) → {[RPG.Enemy.Action](RPG.Enemy.Action.md)}
Returns the selected [action pattern] from the specified [action pattern] list.

##### Arguments

| Name         | Type                                                      | Description          |
|--------------|-----------------------------------------------------------|----------------------|
| `actionList` | [Array](Array.md).&lt;[RPG.Enemy.Action](RPG.Enemy.Action.md)&gt; | Array of [action patterns] |
| `ratingZero` | [Number](Number.md)                                       | Zero rating          |

#### selectAllActions (actionList)
Selects all actions based on the specified [action pattern] list.

##### Arguments

| Name         | Type                                                      | Description          |
|--------------|-----------------------------------------------------------|----------------------|
| `actionList` | [Array](Array.md).&lt;[RPG.Enemy.Action](RPG.Enemy.Action.md)&gt; | Array of [action patterns] |

#### setLetter (letter)
Sets the suffix (A, B, etc.).

##### Arguments

| Name    | Type                | Description      |
|---------|---------------------|------------------|
| `letter` | [String](String.md) | Suffix           |

#### setPlural (plural)
Sets if it is a group (two or more).

##### Arguments

| Name    | Type    | Description      |
|---------|---------|------------------|
| `plural` | Boolean | Is it a group?   |

#### setup (enemyId, x, y)
Sets up Game_Enemy with the specified enemy and coordinates.

##### Arguments

| Name      | Type                | Description            |
|-----------|---------------------|------------------------|
| `enemyId` | [Number](Number.md) | Enemy character ID     |
| `x`       | [Number](Number.md) | X-coordinate           |
| `y`       | [Number](Number.md) | Y-coordinate           |

#### traitObjects () → {[Array](Array.md).&lt;[RPG.State](RPG.State.md)&gt;}
Override: [Game_Battler](Game_Battler.mdr#traitobjects)

#### transform (enemyId)
Transforms into the specified [enemy character].

##### Arguments

| Name      | Type                | Description            |
|-----------|---------------------|------------------------|
| `enemyId` | [Number](Number.md) | Enemy character ID     |
