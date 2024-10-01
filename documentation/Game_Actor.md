[Class Tree](index.md)

# Class: Game_Actor

## Superclass: [Game_Battler](Game_Battler.md)

| Database   | JSON Data         | Sprite                                 |
|------------|--------------------|----------------------------------------|
| [Actor]    | [RPG.Actor](RPG.Actor.md) | [Sprite_Character](Sprite_Character.md), [Sprite_Actor](Sprite_Actor.md) |

A class that handles the retrieval of actor parameters, image settings, combat processing, and image processing during side-view battles.

Main path
```js
$gameActors.actor( actorId )
$gameParty.leader()
$gameParty.allMembers()
$gameParty.battleMembers()
$gameParty.members()
BattleManager.actor()
```

v1.1.0 and v1.2.0 have changes.

Related classes: [Game_Actors](Game_Actors.md), [Game_Party](Game_Party.md), [Game_Troop](Game_Troop.md), [Game_Enemy](Game_Enemy.md), [Scene_Battle](Scene_Battle.md), [BattleManager](BattleManager.md), [Game_Player](Game_Player.md), [Game_Follower](Game_Follower.md)

### new Game_Actor ()

### Properties

| Identifier          | Type                             | Description                  |
|---------------------|----------------------------------|------------------------------|
| `level`             | [Number](Number.md)             | [read-only] [Level]         |
| `_actorId`          | [Number](Number.md)             | Actor ID                     |
| `_name`             | [String](String.md)             | [Name]                       |
| `_nickname`         | [String](String.md)             | [Nickname]                   |
| `_profile`          | [String](String.md)             | [Profile]                    |
| `_classId`          | [Number](Number.md)             | Class ID                     |
| `_level`            | [Number](Number.md)             | [Level]                      |
| `_characterName`    | [String](String.md)             | [Walking Character] image filename (without extension) |
| `_characterIndex`    | [Number](Number.md)             | [Walking Character] image number |
| `_faceName`         | [String](String.md)             | [Face] image filename (without extension) |
| `_faceIndex`         | [Number](Number.md)             | [Face] image number         |
| `_battlerName`      | [String](String.md)             | [[SV] Battle Character] image filename (without extension) |
| `_exp`              | Object                           | [Class Experience Points](#class-experience-points) |
| `_skills`           | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of [Skills]          |
| `_equips`           | [Array](Array.md).&lt;[Game_Item](Game_Item.md)&gt; | Array of [Equipment]       |
| `_actionInputIndex` | [Number](Number.md)             | Action number                |
| `_lastMenuSkill`    | [Game_Item](Game_Item.md)       | Last menu skill             |
| `_lastBattleSkill`  | [Game_Item](Game_Item.md)       | Last battle skill           |
| `_lastCommandSymbol`| [String](String.md)             | Last command                |
| `_stateSteps`       | Object                           | [State Steps](#state-steps) |

#### Class Experience Points
An object that holds experience points corresponding to class IDs (identifier: [Number](Number.md)).

| Identifier | Type          | Description |
|------------|---------------|-------------|
| Class ID   | [Number](Number.md) | Experience Points |

#### State Steps
An object that holds steps corresponding to state IDs (identifier: [Number](Number.md)).

| Identifier | Type          | Description |
|------------|---------------|-------------|
| State ID   | [Number](Number.md) | Steps      |

### Methods Inherited from Superclass

#### [Game_BattlerBase](Game_BattlerBase.md)

* [actionPlusSet ()](Game_BattlerBase.md#actionplusset---arraynumber)
* [addedSkills ()](Game_BattlerBase.md#addedskills---arraynumber)
* [addedSkillTypes ()](Game_BattlerBase.md#addedskilltypes---arraynumber)
* [addNewState (stateId)](Game_BattlerBase.md#addnewstate-stateid)
* [addParam (paramId, value)](Game_BattlerBase.md#addparam-paramid-value)
* [allIcons ()](Game_BattlerBase.md#allicons---arraynumber)
* [allTraits ()](Game_BattlerBase.md#alltraits---arrayrpgtrait)
* [appear ()](Game_BattlerBase.md#appear-)
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
* [collapseType ()](Game_BattlerBase.md#collapsetype---number)
* [confusionLevel ()](Game_BattlerBase.md#confusionlevel---number)
* [deathStateId ()](Game_BattlerBase.md#deathstateid---number)
* [debuffRate (paramId)](Game_BattlerBase.md#debuffrate-paramid--number)
* [decreaseBuff (paramId)](Game_BattlerBase.md#decreasebuff-paramid)
* [die ()](Game_BattlerBase.md#die-)
* [elementRate (elementId)](Game_BattlerBase.md#elementrate-elementid--number)
* [eraseBuff (paramId)](Game_BattlerBase.md#erasebuff-paramid)
* [guardSkillId ()](Game_BattlerBase.md#guardskillid---number)
* [hpRate ()](Game_BattlerBase.md#hprate---number)
* [increaseBuff (paramId)](Game_BattlerBase.md#increasebuff-paramid)
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
* [isEnemy ()](Game_BattlerBase.md#isenemy---boolean)
* [isEquipAtypeOk (atypeId)](Game_BattlerBase.md#isequipatypeok-atypeid--boolean)
* [isEquipTypeLocked (etypeId)](Game_BattlerBase.md#isequiptypelocked-etypeid--boolean)
* [isEquipTypeSealed (etypeId)](Game_BattlerBase.md#isequiptypesealed-etypeid--boolean)
* [isEquipWtypeOk (wtypeId)](Game_BattlerBase.md#isequipwtypeok-wtypeid--boolean)
* [isGuard ()](Game_BattlerBase.md#isguard---boolean)
* [isHidden ()](Game_BattlerBase.md#ishidden---boolean)
* [isMaxBuffAffected (paramId)](Game_BattlerBase.md#ismaxbuffaffected-paramid--boolean)
* [isMaxDebuffAffected (paramId)](Game_BattlerBase.md#ismaxdebuffaffected-paramid--boolean)
* * [isOccasionOk (item)](Game_BattlerBase.md#isoccasionok-item--boolean)
* [isPreserveTp ()](Game_BattlerBase.md#ispreservetp---boolean)
* [isRestricted ()](Game_BattlerBase.md#isrestricted---boolean)
* [isSkillSealed (stypeId)](Game_BattlerBase.md#isskillsealed-stypeid--boolean)
* [isSkillTypeSealed (stypeId)](Game_BattlerBase.md#isskilltypesealed-stypeid--boolean)
* [isStateAffected (stateId)](Game_BattlerBase.md#isstateaffected-stateid--boolean)
* [isStateExpired (stateId)](Game_BattlerBase.md#isstateexpired-stateid--boolean)
* [isStateResist (stateId)](Game_BattlerBase.md#isstateresist-stateid--boolean)
* [isSubstitute ()](Game_BattlerBase.md#issubstitute---boolean)
* [maxTp ()](Game_BattlerBase.md#maxtp---number)
* [meetsItemConditions (item)](Game_BattlerBase.md#meetsitemconditions-item--boolean)
* [meetsSkillConditions (skill)](Game_BattlerBase.md#meetsskillconditions-skill--boolean)
* [mostImportantStateText ()](Game_BattlerBase.md#mostimportantstatetext---string)
* [mpRate ()](Game_BattlerBase.md#mprate---number)
* [overwriteBuffTurns (paramId, turns)](Game_BattlerBase.md#overwritebuffturns-paramid-turns)
* [param (paramId)](Game_BattlerBase.md#param-paramid--number)
* [paramBuffRate (paramId)](Game_BattlerBase.md#parambuffrate-paramid--number)
* [paramMin (paramId)](Game_BattlerBase.md#parammin-paramid--number)
* [paramMax(paramId)](Game_BattlerBase.md#parammax-paramid--number)
* [paramRate (paramId)](Game_BattlerBase.md#paramrate-paramid--number)
* [partyAbility (abilityId)](Game_BattlerBase.md#partyability-abilityid--boolean)
* [paySkillCost (skill)](Game_BattlerBase.md#payskillcost-skill)
* [recoverAll ()](Game_BattlerBase.md#recoverall-)
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

* [action (index)](Game_Battler.md#action-index--game_action)
* [addBuff (paramId, turns)](Game_Battler.md#addbuff-paramid-turns)
* [addDebuff (paramId, turns)](Game_Battler.md#adddebuff-paramid-turns)
* [addState (stateId)](Game_Battler.md#addstate-stateid)
* [chargeTpByDamage (damageRate)](Game_Battler.md#chargetpbydamage-damagerate)
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
* [performMiss ()](Game_Battler.md#performmiss-)
* [performRecovery ()](Game_Battler.md#performrecovery-)
* [performReflection ()](Game_Battler.md#performreflection-)
* [performSubstitute (target)](Game_Battler.md#performsubstitute-target)
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
* [result ()](Game_Battler.md#result---game_actionresult)
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

#### actor () → {[RPG.Actor](RPG.Actor.md)}
Returns the database information of the actor.

#### actorId () → {[Number](Number.md)}
Returns the actor ID.

#### armors () → {[Array](Array.md).&lt;[RPG.Armor](RPG.Armor.md)&gt;}
Returns the armors.

#### attackAnimationId1 () → {[Number](Number.md)}
Returns the animation ID for the first attack.

#### attackAnimationId2 () → {[Number](Number.md)}
Returns the animation ID for the second attack.

#### attackElements () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Override: [Game_BattlerBase](Game_BattlerBase.md#attackelements---arraynumber)

#### bareHandsAnimationId () → {[Number](Number.md)}
Returns the animation ID for bare-hand attacks.

#### bareHandsElementId () → {[Number](Number.md)}
Returns the attribute ID for bare-hand attacks.

#### basicFloorDamage () → {[Number](Number.md)}
Returns the basic floor damage (default value: 10).

#### battlerName () → {[String](String.md)}
Returns the name of the battler.

#### benchMembersExpRate () → {[Number](Number.md)}
Returns the experience rate for members not participating in battle.

#### bestEquipItem (slotId)
Returns the best equipment for the specified slot.

##### Arguments

| Name      | Type        | Description          |
|-----------|-------------|----------------------|
| `slotId`  | [Number](Number.md) | Slot ID             |

#### calcEquipItemPerformance (item) → {[Number](Number.md)}
Returns the difference in performance values between the specified item and equipped items.

##### Arguments

| Name      | Type                        | Description |
|-----------|-----------------------------|-------------|
| `item`    | [RPG.EquipItem](RPG.EquipItem.md) | The item to compare |

#### changeClass (classId, keepExp)
Changes to the specified class.

##### Arguments

| Name      | Type                       | Description             |
|-----------|----------------------------|-------------------------|
| `classId` | [Number](Number.md)       | Class ID                |
| `keepExp` | Boolean                    | Whether to keep experience points |

#### changeEquip (slotId, item)
Changes the specified slot to the specified equipment.

##### Arguments

| Name      | Type                        | Description               |
|-----------|-----------------------------|---------------------------|
| `slotId`  | [Number](Number.md)        | Slot ID                   |
| `item`    | [RPG.EquipItem](RPG.EquipItem.md) | The equipment item |

#### changeEquipById (etypeId, itemId)
Changes the specified equipment type to the specified equipment.

##### Arguments

| Name      | Type                        | Description               |
|-----------|-----------------------------|---------------------------|
| `etypeId` | [Number](Number.md)        | Equipment type ID         |
| `itemId`  | [Number](Number.md)        | Item ID                   |

#### changeExp (exp, show)
Adds experience points and performs level-up processing if necessary.

##### Arguments

| Name      | Type                        | Description               |
|-----------|-----------------------------|---------------------------|
| `exp`     | [Number](Number.md)        | Experience points to add  |
| `show`    | Boolean                     | Whether to show level-up display |

#### changeLevel (level, show)
Changes to the specified level.

##### Arguments

| Name      | Type                        | Description               |
|-----------|-----------------------------|---------------------------|
| `level`   | [Number](Number.md)        | Level to change to        |
| `show`    | Boolean                     | Whether to show the level |

#### characterIndex () → {[Number](Number.md)}
Returns the character index.

#### characterName () → {[String](String.md)}
Returns the character's name.

#### checkFloorEffect ()
Checks the floor effect.

#### clearActions ()
Override: [Game_Battler](Game_Battler.md#clearactions-)

#### clearEquipments ()
Removes all equipment.

#### clearStates ()
Override: [Game_BattlerBase](Game_BattlerBase.md#clearstates-)

#### currentClass () → {[RPG.Class](RPG.Class.md)}
Returns the current class.

#### currentExp () → {[Number](Number.md)}
Returns the current experience points.

#### currentLevelExp () → {[Number](Number.md)}
Returns the experience points required for the current level.

#### discardEquip (item)
Discards the equipment without leaving it in the inventory.

##### Arguments

| Name      | Type                        | Description               |
|-----------|-----------------------------|---------------------------|
| `item`    | [RPG.EquipItem](RPG.EquipItem.md) | The item to discard      |

#### displayLevelUp (newSkills)
Displays the message for acquiring specified skills and leveling up.

##### Arguments

| Name      | Type                        | Description               |
|-----------|-----------------------------|---------------------------|
| `newSkills` | [Array](Array.md).&lt;[RPG.Skill](RPG.Skill.md)&gt; | Array of skills         |

#### equips () → {[Array](Array.md).&lt;[RPG.EquipItem](RPG.EquipItem.md)&gt;}
Returns the array of equipped items.

#### equipSlots () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns the array of equipment slots.

#### eraseState (stateId)
Override: [Game_BattlerBase](Game_BattlerBase.md#erasestate-stateid)

#### executeFloorDamage ()
Deals floor damage.

#### expForLevel (level) → {[Number](Number.md)}
Returns the experience points required to level up to the specified level.

##### Arguments

| Name      | Type                        | Description               |
|-----------|-----------------------------|---------------------------|
| `level`   | [Number](Number.md)        | Level                     |

#### faceIndex () → {[Number](Number.md)}
Returns the face image index.

#### faceName () → {[String](String.md)}
Returns the face image file name (without extension).

#### finalExpRate () → {[Number](Number.md)}
Returns the experience rate that changes based on whether in battle or on the bench.

#### findNewSkills (lastSkills) → {[Array](Array.md).&lt;[RPG.Skill](RPG.Skill.md)&gt;}
Returns the newly acquired skills, assuming the specified skills are already learned.

##### Arguments

| Name         | Type                                         | Description                  |
|--------------|----------------------------------------------|------------------------------|
| `lastSkills` | [Array](Array.md).&lt;[RPG.Skill](RPG.Skill.md)&gt; | Array of skills              |

#### forceChangeEquip (slotId, item)
Forcibly changes the equipment of the specified slot (without returning it to the inventory).

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `slotId`  | [Number](Number.md)        | Slot ID                    |
| `item`    | [RPG.EquipItem](RPG.EquipItem.md) | The equipment item         |

#### forgetSkill (skillId)
Forgets the specified skill (unlearns it).

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `skillId` | [Number](Number.md)        | [Skill ID](RPG.Skill.md#スキルid) |

#### friendsUnit () → {[Game_Party](Game_Party.md)}
Returns the allied party.

#### gainExp (exp)
Adds the specified experience points.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `exp`     | [Number](Number.md)        | Experience points          |

#### hasArmor (armor) → {Boolean}
Checks if the specified armor is equipped.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `armor`   | [RPG.Armor](RPG.Armor.md)  | The armor item             |

#### hasNoWeapons () → {Boolean}
Checks if the character is unarmed (bare-handed).

#### hasSkill (skillId) → {Boolean}
Checks if the specified skill is possessed.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `skillId` | [Number](Number.md)        | [Skill ID](RPG.Skill.md#スキルid) |

#### hasWeapon (weapon) → {Boolean}
Checks if the specified weapon is possessed.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `weapon`  | [RPG.Weapon](RPG.Weapon.md) | The weapon item            |

#### hide ()
**@MZ** Override: [Game_BattlerBase](Game_BattlerBase.md#hide-)

#### index () → {[Number](Number.md)}
Returns the character index.

#### initEquips (equips)
Initializes the specified slot.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `equips`  | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of slot IDs         |

#### initExp ()
Initializes [experience points].

#### initialize (actorId)
Initializes with the specified actor.
Override: [Game_Battler](Game_Battler.md#initialize-)

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `actorId` | [Number](Number.md)        | Actor ID                   |

#### initImages ()
Initializes images.

#### initMembers ()
Override: [Game_Battler](Game_Battler.md#initmembers-)

#### initSkills ()
Initializes skills.

#### inputtingAction () → {[Game_Action](Game_Action.md)}
Returns the inputted action.

#### isActor () → {Boolean}
Override: [Game_BattlerBase](Game_BattlerBase.md#isactor---boolean)

#### isBattleMember () → {Boolean}
Checks if the character is participating in battle.

#### isClass (gameClass) → {Boolean}
Checks if the character belongs to the specified class.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `gameClass` | [RPG.Class](RPG.Class.md) | The class                  |

#### isEquipChangeOk (slotId) → {Boolean}
Checks if the equipment of the specified slot can be changed.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `slotId`  | [Number](Number.md)        | Slot ID                    |

#### isEquipped (item) → {Boolean}
Checks if the specified item is equipped.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `item`    | [RPG.EquipItem](RPG.EquipItem.md) | The item                 |

#### isFormationChangeOk () → {Boolean}
Checks if the formation can be changed.

#### isLearnedSkill (skillId) → {Boolean}
Checks if the specified skill is learned.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `skillId` | [Number](Number.md)        | [Skill ID](RPG.Skill.md#スキルid) |

#### isMaxLevel () → {Boolean}
Checks if the character has reached the maximum level.

#### isSkillWtypeOk (skill) → {Boolean}
Override: [Game_BattlerBase](Game_BattlerBase.md#isskillwtypeok-skill--boolean)

#### isSpriteVisible () → {Boolean}
Checks if the sprite (image) is visible.

#### isWtypeEquipped (wtypeId) → {Boolean}
Checks if the specified weapon type is equipped.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `wtypeId` | [Number](Number.md)        | Weapon type ID             |

#### lastSkill () → {[RPG.Skill](RPG.Skill.md)}
**@MZ** Returns the last skill used.

#### lastBattleSkill () → {[RPG.Skill](RPG.Skill.md)}
Returns the last battle skill used.

#### lastCommandSymbol () → {[String](String.md)}
Returns the last command.

#### lastMenuSkill () → {[RPG.Skill](RPG.Skill.md)}
Returns the last menu skill used.

#### learnSkill (skillId)
Learns the specified skill.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `skillId` | [Number](Number.md)        | [Skill ID](RPG.Skill.md#スキルid) |

#### levelDown ()
Executes level down.

#### levelUp ()
Executes level up.

#### makeActionList () → {[Array](Array.md).&lt;[Game_Action](Game_Action.md)&gt;}
Generates and returns an array of actions.

#### makeActions ()
Override: [Game_Battler](Game_Battler.md#makeactions-)

#### makeAutoBattleActions ()
Generates actions for auto battle.

#### makeConfusionActions ()
Generates actions for a confused state.

#### maxFloorDamage () → {[Number](Number.md)}
Returns the maximum floor damage.

#### maxLevel ()
Returns the maximum level.

#### meetsUsableItemConditions (item) → {Boolean}
Override: [Game_BattlerBase](Game_BattlerBase.md#meetsusableitemconditions-item--boolean)

#### name ()
Returns the [name].

#### nextLevelExp () → {[Number](Number.md)}
Returns the experience points required for the next level.

#### nextRequiredExp () → {[Number](Number.md)}
Returns the experience points required for [the next level].

#### nickname () → {[String](String.md)}
Returns the [nickname].

#### onPlayerWalk ()
Handler for when walking in the map scene.

#### onEscapeFailure ()
**@MZ** Handler for when escape fails.

#### opponentsUnit () → {[Game_Troop](Game_Troop.md)}
Returns the enemy group.

#### optimizeEquipments ()
Optimizes to the [best equipment].

#### paramBase (paramId) → {[Number](Number.md)}
Override: [Game_BattlerBase](Game_BattlerBase.md#parambase-paramid--number)

#### paramPlus (paramId) → {[Number](Number.md)}
Override: [Game_BattlerBase](Game_BattlerBase.md#paramplus-paramid--number)

#### performAction (action)
Override: [Game_Battler](Game_Battler.md#performaction-action)

#### performActionEnd ()
Override: [Game_Battler](Game_Battler.md#performactionend-)

#### performActionStart (action)
Override: [Game_Battler](Game_Battler.md#performactionstart-action)

#### performAttack ()
Executes the attack action.

#### performCollapse ()
Override: [Game_Battler](Game_Battler.md#performcollapse-)

#### performCounter ()
Override: [Game_Battler](Game_Battler.md#performcounter-)

#### performDamage ()
Override: [Game_Battler](Game_Battler.md#performdamage-)

#### performEscape ()
Executes the escape action.

#### performEvasion ()
Override: [Game_Battler](Game_Battler.md#performevasion-)

#### performMagicEvasion ()
Override: [Game_Battler](Game_Battler.md#performmagicevasion-)

#### performMapDamage ()
Executes damage action in the map scene.

#### performVictory ()
Executes victory action.

#### profile () → {[String](String.md)}
Returns the [profile].

#### refresh ()
Override: [Game_Battler](Game_Battler.md#refresh-)

#### releaseUnequippableItems (forcing)
Removes unequippable items.

##### Arguments

| Name      | Type                        | Description                |
|-----------|-----------------------------|----------------------------|
| `forcing` | Boolean                     | Whether to forcibly remove |

#### resetStateCounts (stateId)
Override: [Game_BattlerBase](Game_BattlerBase.md#resetstatecounts-stateid)

#### selectNextCommand () → {Boolean}
Selects the next command and returns whether it was successful.

#### selectPreviousCommand () → {Boolean}
Selects the previous command and returns whether it was successful.

#### setBattlerImage (battlerName)
Sets the SV battler image.

##### Arguments

| Name         | Type                        | Description                |
|--------------|-----------------------------|----------------------------|
| `battlerName` | [String](String.md)        | Name of the [SV] battle character image file (without extension) |

#### setCharacterImage (characterName, characterIndex)
Sets the top-down view character image.

##### Arguments

| Name              | Type                        | Description                |
|-------------------|-----------------------------|----------------------------|
| `characterName`   | [String](String.md)        | Character image file name (without extension) |
| `characterIndex`  | [Number](Number.md)        | Character image index      |

#### setFaceImage (faceName, faceIndex)
Sets the character's [face] image.

##### Arguments

| Name        | Type                        | Description                |
|-------------|-----------------------------|----------------------------|
| `faceName`  | [String](String.md)        | [Face] image file name (without extension) |
| `faceIndex` | [Number](Number.md)        | [Face] image index        |

#### setLastBattleSkill (skill)
Sets the last battle skill used.

##### Arguments

| Name   | Type                          | Description              |
|--------|-------------------------------|--------------------------|
| `skill`| [RPG.Skill](RPG.Skill.md)    | Skill                    |

#### setLastCommandSymbol (symbol)
Sets the last selected command.

##### Arguments

| Name   | Type                          | Description              |
|--------|-------------------------------|--------------------------|
| `symbol` | [String](String.md)         | Command symbol           |

#### setLastMenuSkill (skill)
Sets the last selected menu skill.

##### Arguments

| Name   | Type                          | Description              |
|--------|-------------------------------|--------------------------|
| `skill`| [RPG.Skill](RPG.Skill.md)    | Skill                    |

#### setName (name)
Sets the [name].

##### Arguments

| Name   | Type                          | Description              |
|--------|-------------------------------|--------------------------|
| `name` | [String](String.md)          | [Name]                   |

#### setNickname (nickname)
Sets the [nickname].

##### Arguments

| Name     | Type                          | Description              |
|----------|-------------------------------|--------------------------|
| `nickname`| [String](String.md)         | [Nickname]               |

#### setProfile (profile)
Sets the [profile].

##### Arguments

| Name      | Type                          | Description              |
|-----------|-------------------------------|--------------------------|
| `profile` | [String](String.md)          | [Profile]                |

#### setup (actorId)
Sets up the Game_Actor with the specified actor.

##### Arguments

| Name      | Type                          | Description              |
|-----------|-------------------------------|--------------------------|
| `actorId` | [Number](Number.md)          | Actor ID                 |

#### shouldDisplayLevelUp () → {Boolean}
Checks if the level-up message should be displayed.

#### showAddedStates ()
Checks if the message for added states should be displayed.

#### showRemovedStates ()
Checks if the message for removed states should be displayed.

#### skills () → {[Array](Array.md).&lt;[RPG.Skill](RPG.Skill.md)&gt;}
Returns the acquired skills.

#### skillTypes () → {[Array](Array.md).&lt;[RPG.Skill](RPG.Skill.md)&gt;}
**@MZ** Returns the skill types.

#### stepsForTurn () → {[Number](Number.md)}
Returns the number of steps equivalent to one turn in battle (default: 20).

#### testEscape (item)
Checks if the specified item has the [special effect - escape].

##### Arguments

| Name   | Type                          | Description              |
|--------|-------------------------------|--------------------------|
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item                   |

#### tradeItemWithParty (newItem, oldItem) → {Boolean}
Exchanges possessed items and returns whether the exchange was successful.

##### Arguments

| Name      | Type                          | Description              |
|-----------|-------------------------------|--------------------------|
| `newItem` | [RPG.EquipItem](RPG.EquipItem.md) | New item             |
| `oldItem` | [RPG.EquipItem](RPG.EquipItem.md) | Old item              |

#### traitObjects () → {[Array](Array.md).<*>}
Override: [Game_Battler](Game_Battler.md#traitobjects)

#### turnEndOnMap ()
Walks the number of steps equivalent to ending a turn on the map.

#### updateStateSteps (state)
Updates the number of steps for the specified state removal condition.

##### Arguments

| Name   | Type                          | Description              |
|--------|-------------------------------|--------------------------|
| `state`| [RPG.State](RPG.State.md)    | State                    |

#### usableSkills () → {[Array](Array.md).&lt;[RPG.Skill](RPG.Skill.md)&gt;}
Returns an array of usable skills.

#### weapons () → {[Array](Array.md).&lt;[RPG.Weapon](RPG.Weapon.md)&gt;}
Returns an array of equipped weapons.

### Deprecated MV Methods

`paramMax (paramId)`, `startAnimation (animationId, mirror, delay)`
