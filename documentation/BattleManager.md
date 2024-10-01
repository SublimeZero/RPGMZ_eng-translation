[Class Tree](index.md)

# Class: BattleManager
A static class that controls the progression of battles.

In "RPG Maker MZ," features related to time-progress battles have been mainly added.

Changes were made in v1.2.0, v1.4.0, v1.4.3, v1.7.0, v1.8.0, and v1.8.1.

Related classes: [Game_Actor](Game_Actor.md), [Game_Party](Game_Party.md), [Game_Enemy](Game_Enemy.md), [Game_Troop](Game_Troop.md), [Scene_Battle](Scene_Battle.md)


### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_phase` | [String](String.md) | [static] [Action State](#action-state) |
| `_canEscape` | Boolean | [static] [Can Escape] |
| `_canLose` | Boolean | [static] [Can Lose] |
| `_battleTest` | Boolean | [static] [Is Battle Test] |
| `_eventCallback` | function | [static] Callback function |
| `_inputting` | Boolean | **@MZ** [static] Is Inputting |
| `_preemptive` | Boolean | [static] [Preemptive Attack] |
| `_surprise` | Boolean | [static] [Surprise Attack] |
| `_actorIndex` | [Number](Number.md) | [static] Actor number |
| `_actionForcedBattler` | [Game_Battler](Game_Battler.md) | [static] Actor forced to act |
| `_mapBgm` | [MV.AudioParameters](MV.AudioParameters.md) | [static] Battle BGM |
| `_mapBgs` | [MV.AudioParameters](MV.AudioParameters.md) | [static] Battle BGS |
| `_actionBattlers` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | [static] Array of battlers taking action (action order) |
| `_subject` | [Game_Battler](Game_Battler.md) | [static] Target battler |
| `_action` | [Game_Action](Game_Action.md) | [static] Action |
| `_targets` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | [static] Array of target battlers |
| `_logWindow` | [Window_BattleLog](Window_BattleLog.md) | [static] Log window |
| `_spriteset` | [Spriteset_Battle](Spriteset_Battle.md) | [static] Sprite set |
| `_escapeRatio` | [Number](Number.md) | [static] Escape probability |
| `_escaped` | Boolean | [static] Did escape succeed |
| `_rewards` | [MV.BattleRewards](MV.BattleRewards.md) | [static] Rewards |
| `_tpbNeedsPartyCommand` | Boolean | [static] Is party command needed for TP battle |

#### Action State

| String | Description | update () |
| --- | --- | ---|
| "init" | Initialization |
| "start" | Start | yes |
| "input" | Input |
| "turn" | Turn progress | yes |
| "action" | Action | yes |
| "turnEnd" | Turn end | yes |
| "battleEnd" | Battle end | yes |
| "aborting" | Battle aborting |
| "waiting" | Waiting state |
| null | Not a battle scene | 

### Deprecated MV Properties
`_statusWindow`, `_turnForced`


### Methods

#### (static) abort ()
Abort.


#### (static) actor () → {[Game_Actor](Game_Actor.md)}
Returns the actor.


#### (static) allBattleMembers () → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns all battlers participating in the battle.


#### (static) applySubstitute (target) → {[Game_Battler](Game_Battler.md)}
If the target is dead or otherwise incapacitated, it selects and returns a substitute.
If there are no issues, it returns the target as is.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### (static) cancelActorInput ()
**@MZ** Cancel actor input.


#### (static) canEscape () → {Boolean}
Can [Escape].


#### (static) canLose () → {Boolean}
Can [Lose].


#### (static) checkAbort () → {Boolean}
If the party is absent or in a state that requires aborting, it aborts and returns whether the abort was executed.


#### (static) checkBattleEnd () → {Boolean}
If allies or enemies are all defeated, it ends the battle and returns whether the end was executed.


#### (static) checkSubstitute (target) → {Boolean}
Checks if a substitute is needed if the target is dead or otherwise incapacitated.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### (static) checkTpbInputClose ()
**@MZ** Checks to stop input for time-progress battles.


#### (static) checkTpbInputOpen ()
**@MZ** Checks to start input for time-progress battles.


#### (static) checkTpbTurnEnd ()
**@MZ** Checks to end the turn in time-progress battles.


#### (static) changeCurrentActor (forward)
**@MZ** Changes the current actor.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `forward` | Boolean | Move forward |


#### (static) displayBattlerStatus ()
**@MZ** Displays battle status.


#### (static) displayDefeatMessage ()
Displays [Defeat] message.


#### (static) displayDropItems ()
Displays [Item Acquired] message.


#### (static) displayEscapeFailureMessage ()
Displays [Escape Failure] message.


#### (static) displayEscapeSuccessMessage ()
Displays [Escape Success] message.


#### (static) displayExp ()
Displays [Experience Points Acquired] message.


#### (static) displayGold ()
Displays [Gold Acquired] message.


#### (static) displayRewards ()
Displays rewards (experience points, gold, items) message.


#### (static) displayStartMessages ()
Displays [Appearance] message.


#### (static) displayVictoryMessage ()
Displays [Victory] message.


#### (static) endAction ()
Ends action processing.


#### (static) endBattle (result)
Ends battle processing.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `result` | [Number](Number.md) | 0: Victory 1: Abort 2: Defeat |


#### (static) endBattlerActions ()
**@MZ** Ends battle actions.


#### (static) endAllBattlersTurn ()
**@MZ** Ends all battlers' turns.


#### (static) endTurn ()
Ends turn processing.


#### (static) finishActorInput ()
**@MZ** Ends actor input.


#### (static) forceAction (battler)
Force action.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `battler` | [Game_Battler](Game_Battler.md) | Target battler |


#### (static) gainDropItems ()
Returns [Drop Items].


#### (static) gainExp ()
Returns [Experience Points].


#### (static) gainGold ()
Returns [Gold].


#### (static) gainRewards ()
Returns rewards (Experience Points, Gold, Items).


#### (static) getNextSubject () → {[Game_Battler](Game_Battler.md)}
Returns the next target battler.


#### (static) initMembers ()
Initializes member variables.


#### (static) inputtingAction () → {[Game_Action](Game_Action.md)}
Returns the action of the actor currently inputting.


#### (static) invokeAction (subject, target)
Initiates an action from the specified subject against the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### (static) invokeCounterAttack (subject, target)
Initiates a counterattack action from the specified subject against the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### (static) invokeMagicReflection (subject, target)
Initiates a magic reflection action from the specified subject against the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### (static) invokeNormalAction (subject, target)
Initiates a normal action from the specified subject against the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |


#### (static) isActiveTpb () → {Boolean}
**@MZ** Is it active time-progress battle?


#### (static) isAborting () → {Boolean}
Is it in the process of aborting?


#### (static) isActionForced () → {Boolean}
Is it in forced action?


#### (static) isBattleEnd () → {Boolean}
Is it in a battle end state (all enemies or allies defeated)?


#### (static) isBattleTest () → {Boolean}
Is it executed in [Battle Test]?


#### (static) isBusy () → {Boolean}
Is it in the process of displaying messages or other operations?


#### (static) isEscaped () → {Boolean}
Has the escape been completed?


#### (static) isInputting () → {Boolean}
Is it inputting?


#### (static) isTpb () → {Boolean}
**@MZ** Is it a time-progress battle?


#### (static) isInTurn () → {Boolean}
Is it in the middle of a turn?


#### (static) isPartyTpbInputtable ()→ {Boolean}
**@MZ** Is there a party command in the time-progress battle?


#### (static) isTpbMainPhase () → {Boolean}
**@MZ** Is it in the main phase of time-progress battle ("turn", "turnEnd", "action")?


#### (static) isTurnEnd () → {Boolean}
Is it in a turn end state?


#### (static) makeActionOrders ()
Sets the order of actions.


#### (static) makeEscapeRatio ()
Sets the escape probability.


#### (static) makeRewards ()
Sets the rewards.


#### (static) needsActorInputCancel ()→ {Boolean}
**@MZ** Is cancellation of actor command input needed?


#### (static) onEncounter ()
Handler for encounters.
Determines [Preemptive Attack] and [Surprise Attack].


#### (static) onEscapeFailure ()
**@MZ** Handler for escape failure.


#### (static) onEscapeSuccess ()
**@MZ** Handler for escape success.


#### (static) playBattleBgm ()
Plays battle BGM.


#### (static) playDefeatMe ()
Plays defeat ME.


#### (static) playVictoryMe ()
Plays victory ME.


#### (static) processAbort ()
Processes abort.


#### (static) processDefeat ()
Processes defeat.


#### (static) processEscape () → {Boolean}
Executes escape processing and returns whether the escape was successful.


#### (static) processForcedAction ()
Processes forced action.


#### (static) processTurn ()
Processes turn continuation.


#### (static) processVictory ()
Processes victory.


#### (static) rateSurprise () → {[Number](Number.md)}
Returns the probability of [Surprise Attack].


#### (static) refreshStatus ()
Redraws [Status] display.

#### (static) replayBgmAndBgs ()
Replays the continuation of BGM and BGS.


#### (static) saveBgmAndBgs ()
Saves the state of BGM and BGS.


#### (static) selectNextActor ()
**@MZ** Selects the next actor.


#### (static) selectNextCommand ()
Selects the next command.


#### (static) selectPreviousActor ()
**@MZ** Selects the previous actor.


#### (static) selectPreviousCommand ()
Selects the previous command.


#### (static) setBattleTest (battleTest)
Sets whether it is in [Battle Test] state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `battleTest` | Boolean | Is it in [Battle Test] state? |


#### (static) setEventCallback (callback)
Sets a callback function to return from (endBattle).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `callback` | function | Callback function |


#### (static) setLogWindow (logWindow)
Sets the log window.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `logWindow` | [Window_BattleLog](Window_BattleLog.md) | Log window |


#### (static) setSpriteset (spriteset)
Sets the spriteset.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `spriteset` | [Spriteset_Battle](Spriteset_Battle.md) | Spriteset |


#### (static) setup (troopId, canEscape, canLose)
Sets up the battle.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `troopId` | [Number](Number.md) | Enemy group ID |
| `canEscape` | Boolean | [Can Escape] |
| `canLose` | Boolean | [Can Lose] |


#### (static) startAction ()
Starts the action.


#### (static) startActorInput ()
**@MZ** Starts actor input.


#### (static) startBattle ()
Starts the battle.


#### (static) startInput ()
Starts input.


#### (static) startTurn ()
Starts the turn.


#### (static) update (timeActive)
Updates each frame.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `timeActive` | Boolean | **@MZ** Is time progression active? |


#### (static) updateAction ()
Updates the action.


#### (static) updateAllTpbBattlers ()
**@MZ** Updates all battlers in time-progress battle.


#### (static) updateBattleEnd ()
Updates the battle end.


#### (static) updateEvent () → {Boolean}
Updates the event and returns whether something was executed.


#### (static) updateEventMain () → {Boolean}
Updates the main part of the event and returns whether something was executed.


#### (static) updatePhase (timeActive)
**@MZ** Updates the action state (phase).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `timeActive` | Boolean | Is time progression active? |


#### (static) updateTpb ()
**@MZ** Updates the time-progress battle.


#### (static) updateTpbBattler (battler)
**@MZ** Updates the specified battler in the time-progress battle.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `battler` | [Game_Battler](Game_Battler.md) | Battler |


#### (static) updateTpbInput ()
**@MZ** Updates the input for the time-progress battle.


#### (static) updateStart ()
**@MZ** Updates the starting state.


#### (static) updateTurn (timeActive)
Updates the turn.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `timeActive` | Boolean | **@MZ** Is time progression active? |


#### (static) updateTurnEnd ()
Updates the turn end.


### Deprecated MV Methods
[static] setStatusWindow (statusWindow), clearActor (), changeActor (newActorIndex, lastActorActionState), isForcedTurn ()
