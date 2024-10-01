[Class Tree](index.md)

# Class: Game_Party

## Superclass: [Game_Unit](Game_Unit.md)

| Global Variable | Save Data |
| --- | --- |
| [$gameParty](global.md#gameparty-game_party) | Saved |

A class that defines the [Party].

Changes were made in v1.4.0 and v1.4.4.

Related Classes: [Game_Troop](Game_Troop.md), [Game_Player](Game_Player.md), [Game_Follower](Game_Follower.md), [Game_Actor](Game_Actor.md), [Game_Actors](Game_Actors.md), [Scene_Battle](Scene_Battle.md), [BattleManager](BattleManager.md)

### new Game_Party ()

### Properties

Static constants that begin with ABILITY_ are used for [Party Ability IDs](RPG.Trait.md#party-ability-id).

| Identifier | Type | Description |
| --- | --- | --- |
| `ABILITY_ENCOUNTER_HALF` | [Number](Number.md) | [static] Halves encounters |
| `ABILITY_ENCOUNTER_NONE` | [Number](Number.md) | [static] Disables encounters |
| `ABILITY_CANCEL_SURPRISE` | [Number](Number.md) | [static] Disables surprise attacks |
| `ABILITY_RAISE_PREEMPTIVE` | [Number](Number.md) | [static] Increases preemptive attack rate |
| `ABILITY_GOLD_DOUBLE` | [Number](Number.md) | [static] Doubles acquired gold |
| `ABILITY_DROP_ITEM_DOUBLE` | [Number](Number.md) | [static] Doubles item acquisition rate |
| `_gold` | [Number](Number.md) | Amount of gold |
| `_steps` | [Number](Number.md) | Number of steps taken |
| `_lastItem` | [Game_Item](Game_Item.md) | Last item used |
| `_menuActorId` | [Number](Number.md) | Actor ID for the menu |
| `_targetActorId` | [Number](Number.md) | Target actor ID |
| `_actors` | [Array](Array.md) | Array of actor IDs |
| `_items` | Object | {[itemId: number]: number} |
| `_weapons` | Object | {[itemId: number]: number} |
| `_armors` | Object | {[itemId: number]: number} |


### Methods Inherited from Superclass

#### [Game_Unit](Game_Unit.md)

* [agility ()](Game_Unit.md#agility---number)
* [aliveMembers ()](Game_Unit.md#alivemembers---arraygame_battler)
* [clearActions ()](Game_Unit.md#clearactions-)
* [clearResults ()](Game_Unit.md#clearresults-)
* [deadMembers ()](Game_Unit.md#deadmembers---arraygame_battler)
* [inBattle ()](Game_Unit.md#inbattle---boolean)
* [makeActions ()](Game_Unit.md#makeactions-)
* [movableMembers ()](Game_Unit.md#movablemembers---arraygame_battler)
* [onBattleEnd ()](Game_Unit.md#onbattleend-)
* [onBattleStart ()](Game_Unit.md#onbattlestart-)
* [randomDeadTarget ()](Game_Unit.md#randomdeadtarget---game_battler)
* [randomTarget ()](Game_Unit.md#randomtarget---game_battler)
* [select (activeMember)](Game_Unit.md#select-activemember)
* [smoothDeadTarget (index)](Game_Unit.md#smoothdeadtarget-index--game_battler)
* [smoothTarget (index)](Game_Unit.md#smoothtarget-index--game_battler)
* [substituteBattler (target)](Game_Unit.md#substitutebattler-target--game_battler)
* [tgrSum ()](Game_Unit.md#tgrsum---number)


### Methods

#### addActor (actorId)
Adds the specified actor.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actorId` | [Number](Number.md) | Actor ID |


#### allBattleMembers () → {[Array](Array.md).&lt;[Game_Actor](Game_Actor.md)&gt;}
**@MZ 1.4.0** Returns an array of all actors that are battle members.


#### allItems () → {[Array](Array.md).&lt;[RPG.BaseItem](RPG.BaseItem.md)&gt;}
Returns an array of all items held by the party.


#### allMembers () → {[Array](Array.md).&lt;[Game_Actor](Game_Actor.md)&gt;}
Returns an array of all actors in the party.


#### armors () → {[Array](Array.md).&lt;[RPG.Armor](RPG.Armor.md)&gt;}
Returns an array of all armors held by the party.


#### battleMembers () → {[Array](Array.md).&lt;[Game_Actor](Game_Actor.md)&gt;}
Returns an array of all actors participating in battle.


#### canInput () → {Boolean}
Whether input is possible.


#### canUse (item) → {Boolean}
Whether the specified item can be used.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |


#### charactersForSavefile () → {[Array](Array.md).&lt;[Array](Array.md).&lt;*&gt;&gt;}
Returns an array of character image information recorded in the save file.<br />
An array containing pairs of values [ "filename", character number ] for the number of characters.

#### consumeItem (item)
Consumes the specified item.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |


#### discardMembersEquip (item, amount)
Discards the specified equipment.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.EquipItem](RPG.EquipItem.md) | Equipment item |
| `amount` | [Number](Number.md) | Quantity |


#### equipItems () → {[Array](Array.md).&lt;[RPG.EquipItem](RPG.EquipItem.md)&gt;}
Returns an array of all equippable items held by the party.


#### exists () → {Boolean}
Checks if the party exists (if there is at least one member).


#### facesForSavefile () → {[Array](Array.md).&lt;[Array](Array.md).&lt;*&gt;&gt;}
Returns an array of face image information recorded in the save file.<br />
An array containing pairs of values [ "filename", face number ] for the number of characters.


#### gainGold (amount)
Increases the amount of gold by the specified amount.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `amount` | [Number](Number.md) | Amount |


#### gainItem (item, amount, includeEquip)
Increases the specified item.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |
| `amount` | [Number](Number.md) | Quantity |
| `includeEquip` | Boolean | Whether to include equipped items |


#### gold () → {[Number](Number.md)}
Returns the amount of gold held.


#### hasCancelSurprise () → {Boolean}
Checks if the party has the [Cancel Surprise] ability.


#### hasDropItemDouble () → {Boolean}
Checks if the party has the [Item Acquisition Rate Doubled] ability.


#### hasEncounterHalf () → {Boolean}
Checks if the party has the [Half Encounters] ability.


#### hasEncounterNone () → {Boolean}
Checks if the party has the [No Encounters] ability.


#### hasGoldDouble () → {Boolean}
Checks if the party has the [Gold Doubled] ability.


#### hasItem (item, includeEquip) → {Boolean}
Checks if the specified item is held by the party.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |
| `includeEquip` | Boolean | Whether to include equipped items |


#### hasMaxItems (item) → {Boolean}
Checks if the specified item is held in maximum quantity.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |


#### hasRaisePreemptive () → {Boolean}
Checks if the party has the [Raise Preemptive Attack Rate] ability.


#### hiddenBattleMembers () → {[Array](Array.md).&lt;[Game_Actor](Game_Actor.md)&gt;}
**@MZ 1.4.0** Returns an array of all actors hidden among the battle members.


#### highestLevel () → {[Number](Number.md)}
Returns the highest level among the party members.


#### increaseSteps ()
Increases the number of steps.


#### initAllItems ()
Initializes all items.


#### initialize ()
Override: [Game_Unit](Game_Unit.md#initialize-)


#### isAllDead () → {Boolean}
Override: [Game_Unit](Game_Unit.md#isalldead---boolean)


#### isAnyMemberEquipped (item) → {Boolean}
Checks if any member is equipped with the specified item.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.EquipItem](RPG.EquipItem.md) | Equipment item |


#### isEmpty () → {Boolean}
Checks if the party has 0 members.


#### isEscaped () → {Boolean}
**@MZ1.4.0** Checks if escaped.<br />
**@MZ1.4.4** The unused argument `item` was removed.


#### itemContainer (item) → {[Array](Array.md).&lt;[RPG.BaseItem](RPG.BaseItem.md)&gt;}
Returns an array containing the entire category that includes the specified item.<br />
The category can be [Items], [Weapons], or [Armors].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |


#### items () → {[Array](Array.md).&lt;[RPG.Item](RPG.Item.md)&gt;}
Returns an array of items (excluding weapons and armors).


#### lastItem () → {[RPG.BaseItem](RPG.BaseItem.md)}
Returns the last selected item.


#### leader () → {[Game_Actor](Game_Actor.md)}
Returns the actor that is the leader.


#### loseGold (amount)
Decreases the amount of gold by the specified amount.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `amount` | [Number](Number.md) | Amount |


#### loseItem (item, amount, includeEquip)
Decreases the specified item.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |
| `amount` | [Number](Number.md) | Quantity |
| `includeEquip` | Boolean | Whether to include equipped items |


#### makeMenuActorNext ()
Generates the menu for the next actor.


#### makeMenuActorPrevious ()
Generates the menu for the previous actor.


#### maxBattleMembers () → {[Number](Number.md)}
Returns the maximum number of members participating in battle (default value: 4).


#### maxGold () → {[Number](Number.md)}
Returns the maximum amount of gold (default value: 99999999).

#### maxItems (item) → {[Number](Number.md)}
Returns the maximum quantity of the specified item (default: 99).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |


#### members () → {[Array](Array.md).&lt;[Game_Actor](Game_Actor.md)&gt;}
Override: [Game_Unit](Game_Unit.md#members---arraygame_battler)<br />
Returns `battleMembers()` if in battle, otherwise returns `allMembers()`.


#### menuActor () → {[Game_Actor](Game_Actor.md)}
Returns the actor currently selected in the menu.


#### name () → {[String](String.md)}
Returns the name of the party.<br />
When there is one member, it returns "Actor's Name"; when there are multiple members, it returns "Actors' Names" (default).


#### numItems (item) → {[Number](Number.md)}
Returns the quantity of the specified item held by the party.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |


#### onEscapeFailure ()
**@MZ** Handler for when escaping fails.


#### onPlayerWalk ()
Handler for when the player walks.


#### partyAbility (abilityId) → {Boolean}
Checks if there are any actors with the specified [Party Ability].

##### Arguments

| Name | Type | Description |
|------------|------------------------|---------------------------------------|
| `abilityId` | [Number](Number.md)    | [Party Ability ID](RPG.Trait.md#party-ability-id) |

#### performEscape ()
Starts the escape motion for the entire party.


#### performVictory ()
Starts the victory motion for the entire party.


#### ratePreemptive (troopAgi) → {[Number](Number.md)}
Returns the probability of a preemptive attack against the specified enemy speed.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `troopAgi` | [Number](Number.md) | Speed |


#### rateSurprise (troopAgi) → {[Number](Number.md)}
Returns the probability of a surprise attack against the specified enemy speed.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `troopAgi` | [Number](Number.md) | Speed |


#### removeActor (actorId)
Removes the specified actor.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actorId` | [Number](Number.md) | Actor ID |


#### removeBattleStates ()
Removes all states from the party members.


#### removeInvalidMembers ()
**@MZ** Removes invalid actors.


#### requestMotionRefresh ()
Resets the motion of all party members.


#### reviveBattleMembers ()
Revives all battle participants.


#### setLastItem (item)
Sets the specified item as the last item.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |


#### setMenuActor (actor)
Sets the specified actor as the selected state in the menu.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actor` | [Game_Actor](Game_Actor.md) | Actor |


#### setTargetActor (actor)
Sets the specified actor as the target actor.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actor` | [Game_Actor](Game_Actor.md) | Actor |


#### setupBattleTest ()
Prepares for the battle test.


#### setupBattleTestItems ()
Prepares items for the battle test.


#### setupBattleTestMembers ()
Prepares members for the battle test.


#### setupStartingMembers ()
Prepares starting members.


#### size () → {[Number](Number.md)}
Returns the number of party members.


#### steps () → {[Number](Number.md)}
Returns the number of steps.


#### swapOrder (index1, index2)
Swaps the actors at the specified indices.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `index1` | [Number](Number.md) | Actor 1's index |
| `index2` | [Number](Number.md) | Actor 2's index |


#### targetActor () → {[Game_Actor](Game_Actor.md)}
Returns the target actor.


#### weapons () → {[Array](Array.md).&lt;[RPG.Weapon](RPG.Weapon.md)&gt;}
Returns an array of all weapons held by the party.
