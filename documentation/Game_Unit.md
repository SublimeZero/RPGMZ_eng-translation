[Class Tree](index.md)

# Class: Game_Unit

A class that handles groups during combat.

Methods that retrieve members returning [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; should be written like `$gameParty.members[0]`, but you need to first invoke the method with `()` like `$gameParty.members()[0]` and then select from the returned array. <br />
Also, note that the index starts from `0`.

Changes were made in v1.8.1.

### new Game_Unit ()

### Subclasses

* [Game_Party](Game_Party.md)
* [Game_Troop](Game_Troop.md)


### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_inBattle` | Boolean | Whether in battle |


### Methods

#### agility () → {[Number](Number.md)}
Returns the unit's agility.


#### aliveMembers () → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns an array of living battlers.


#### clearActions ()
Cancels actions.


#### clearResults ()
Cancels action results.


#### deadMembers () → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns an array of dead battlers.


#### inBattle () → {Boolean}
Whether in battle.


#### initialize ()
Initialization during object creation.


#### isAllDead () → {Boolean}
Whether all battlers are dead.


#### makeActions ()
Creates combat actions.


#### members () → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns an array of all battlers, living or dead, during combat.


#### movableMembers () → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns an array of movable battlers (not dead or paralyzed).


#### onBattleEnd ()
Handler called at the end of battle.


#### onBattleStart ()
Handler called at the start of battle.


#### randomDeadTarget () → {[Game_Battler](Game_Battler.md)}
Returns one random dead battler.


#### randomTarget () → {[Game_Battler](Game_Battler.md)}
Returns one random battler from those included.


#### select (activeMember)
Selects the specified battler.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `activeMember` | [Game_Battler](Game_Battler.md) | Battler |


#### smoothDeadTarget (index) → {[Game_Battler](Game_Battler.md)}
Returns a prioritized dead member based on the specified index.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `index` | [Number](Number.md) | Member index |


#### smoothTarget (index) → {[Game_Battler](Game_Battler.md)}
Returns a prioritized living member based on the specified index.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `index` | [Number](Number.md) | Member index |


#### substituteBattler (target) → {[Game_Battler](Game_Battler.md)}
Returns a substitute battler.
**@MZ1.8.1** Added argument `target`.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### tgrSum () → {[Number](Number.md)}
Returns the total [target rate] of living members.


#### tpbBaseSpeed () → {[Number](Number.md)}
**@MZ** Returns the base speed of time progress battle.


#### tpbReferenceTime () → {[Number](Number.md)}
**@MZ** Returns the reference speed of time progress battle.


#### updateTpb ()
**@MZ** Updates the time progress battle.
