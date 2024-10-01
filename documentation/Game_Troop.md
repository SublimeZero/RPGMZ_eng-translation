[Class Tree](index.md)

# Class: Game_Troop

## Superclass: [Game_Unit](Game_Unit.md)

| Database | JSON Data | Global Variables |
| --- | --- | --- |
| [Enemy Group] | [RPG.Troop](RPG.Troop.md) | [$gameTroop](global.md#gametroop-game_troop) |

Class that defines the [enemy group] in the battle scene.

Related Classes: [Game_Enemy](Game_Enemy.md), [Game_Actor](Game_Actor.md), [Game_Party](Game_Party.md), [Scene_Battle](Scene_Battle.md), [BattleManager](BattleManager.md)

### new Game_Troop ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `LETTER_TABLE_HALF` | [Array](Array.md).&lt;[String](String.md)&gt; | [static] Name suffixes (half-width symbols A-Z) |
| `LETTER_TABLE_FULL` | [Array](Array.md).&lt;[String](String.md)&gt; | [static] Name suffixes (full-width symbols A-Z) |
| `_interpreter` | [Game_Interpreter](Game_Interpreter.md) | Command interpreter |
| `_troopId` | [Number](Number.md) | Enemy group ID |
| `_eventFlags` | Object | {[page: Number]: Boolean} |
| `_enemies` | [Array](Array.md).&lt;[Game_Enemy](Game_Enemy.md)&gt; | Array of [enemy characters] |
| `_turnCount` | [Number](Number.md) | Turn counter |
| `_namesCount` | Object | {[name: String]: Number} |


### Inherited Methods from Superclass

#### [Game_Unit](Game_Unit.md)

* [agility ()](Game_Unit.md#agility---number)
* [aliveMembers ()](Game_Unit.md#alivemembers---arraygame_battler)
* [clearActions ()](Game_Unit.md#clearactions-)
* [clearResults ()](Game_Unit.md#clearresults-)
* [deadMembers ()](Game_Unit.md#deadmembers---arraygame_battler)
* [inBattle ()](Game_Unit.md#inbattle---boolean)
* [isAllDead ()](Game_Unit.md#isalldead---boolean)
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

#### clear ()
Initializes the data.

#### enemyNames () → {[Array](Array.md).<[String](String.md)>}
Returns an array of names of [enemy characters].


#### expTotal () → {[Number](Number.md)}
Returns the total EXP of [enemy characters].


#### goldRate () → {[Number](Number.md)}
Returns the acquisition rate of the amount of gold held by the player party. It fluctuates due to skills and item effects.


#### goldTotal () → {[Number](Number.md)}
Returns the total amount of gold obtained from [enemy characters].


#### increaseTurn ()
Advances the turn.


#### initialize ()
Override: [Game_Unit](Game_Unit.md#initialize-)


#### isEventRunning () → {Boolean}
Is an event currently running?


#### isTpbTurnEnd () → {Boolean}
**@MZ** Is the turn of time progress battle ended?


#### letterTable () → {[Array](Array.md).<[String](String.md)>}
Returns an array of name suffixes (A-Z).


#### makeDropItems () → {[Array](Array.md).<[RPG.BaseItem](RPG.BaseItem.md)>}
Creates drop items and returns them as an array.


#### makeUniqueNames ()
Assigns unique names (A-Z) to all [enemy characters].


#### meetsConditions (page) → {Boolean}
Checks if the specified page meets the conditions.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `page` | [RPG.BattleEventPage](RPG.BattleEventPage.md) | Battle event page |


#### members () → {[Array](Array.md).<[Game_Enemy](Game_Enemy.md)>}
Override: [Game_Unit](Game_Unit.md#members---arraygame_battler)


#### setup (troopId)
Prepares the specified [enemy group].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `troopId` | [Number](Number.md) | Enemy group ID |


#### setupBattleEvent ()
Prepares the battle event.


#### troop () → {[RPG.Troop](RPG.Troop.md)}
Returns the definition information of the [enemy group].


#### turnCount () → {[Number](Number.md)}
Returns the turn count.


#### updateInterpreter ()
Updates the command interpreter.
