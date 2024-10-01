[Class Tree](index.md)

# Class: BattleManager
A static class that controls the progress of battles.

In "RPG Maker MZ", features related to time progress battles have been primarily added.

Changes have been made in v1.2.0, v1.4.0, v1.4.3, v1.7.0, v1.8.0, and v1.8.1.

Related Classes: [Game_Actor](Game_Actor.md), [Game_Party](Game_Party.md), [Game_Enemy](Game_Enemy.md), [Game_Troop](Game_Troop.md), [Scene_Battle](Scene_Battle.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_phase` | [String](String.md) | [static] [Action State](#action-state) |
| `_canEscape` | Boolean | [static] [Can Escape] |
| `_canLose` | Boolean | [static] [Can Lose] |
| `_battleTest` | Boolean | [static] Is this a [Battle Test]? |
| `_eventCallback` | function | [static] Callback function |
| `_inputting` | Boolean | **@MZ** [static] Is inputting? |
| `_preemptive` | Boolean | [static] Is it a [Preemptive Attack]? |
| `_surprise` | Boolean | [static] Is it a [Surprise Attack]? |
| `_actorIndex` | [Number](Number.md) | [static] Actor number |
| `_actionForcedBattler` | [Game_Battler](Game_Battler.md) | [static] Actor for forced action |
| `_mapBgm` | [MV.AudioParameters](MV.AudioParameters.md) | [static] Battle BGM |
| `_mapBgs` | [MV.AudioParameters](MV.AudioParameters.md) | [static] Battle BGS |
| `_actionBattlers` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | [static] Array of battlers performing actions (in order) |
| `_subject` | [Game_Battler](Game_Battler.md) | [static] Target battler |
| `_action` | [Game_Action](Game_Action.md) | [static] Action |
| `_targets` | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | [static] Array of target battlers |
| `_logWindow` | [Window_BattleLog](Window_BattleLog.md) | [static] Log window |
| `_spriteset` | [Spriteset_Battle](Spriteset_Battle.md) | [static] Sprite set |
| `_escapeRatio` | [Number](Number.md) | [static] Escape probability |
| `_escaped` | Boolean | [static] Was the escape successful? |
| `_rewards` | [MV.BattleRewards](MV.BattleRewards.md) | [static] Rewards |
| `_tpbNeedsPartyCommand` | Boolean | [static] Does TP battle need a party command? |

#### Action State

| String | Description | update() |
| --- | --- | --- |
| "init" | Initialization |
| "start" | Start | yes |
| "input" | Input |
| "turn" | Turn progress | yes |
| "action" | Action | yes |
| "turnEnd" | Turn end | yes |
| "battleEnd" | Battle end | yes |
| "aborting" | Battle abort |
| "waiting" | Waiting state |
| null | Not in a battle scene |

### Deprecated MV Properties
`_statusWindow`, `_turnForced`

### Methods

#### (static) abort()
Abort.

#### (static) actor() → {[Game_Actor](Game_Actor.md)}
Returns the actor.

#### (static) allBattleMembers() → {[Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt;}
Returns all battlers participating in the battle.

#### (static) applySubstitute(target) → {[Game_Battler](Game_Battler.md)}
Returns a substitute if the target is dead or otherwise; returns the target as is if no issues.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

#### (static) cancelActorInput()
**@MZ** Cancel actor input.

#### (static) canEscape() → {Boolean}
Is it [Can Escape]?

#### (static) canLose() → {Boolean}
Is it [Can Lose]?

#### (static) checkAbort() → {Boolean}
If in a state where cancellation is needed, such as no party members, abort and return whether the cancellation was executed.

#### (static) checkBattleEnd() → {Boolean}
If in a battle end state, such as all allies or enemies being defeated, end the battle and return whether the end was executed.

#### (static) checkSubstitute(target) → {Boolean}
Returns whether a substitute is needed if the target is dead or otherwise.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

#### (static) checkTpbInputClose()
**@MZ** Check for stopping input in time progress battles.

#### (static) checkTpbInputOpen()
**@MZ** Check for starting input in time progress battles.

#### (static) checkTpbTurnEnd()
**@MZ** Check for ending the turn in time progress battles.

#### (static) changeCurrentActor(forward)
**@MZ** Change the current actor.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `forward` | Boolean | Move forward? |

#### (static) displayBattlerStatus()
**@MZ** Display battle status.

#### (static) displayDefeatMessage()
Display [Defeat] message.

#### (static) displayDropItems()
Display [Item Acquired] message.

#### (static) displayEscapeFailureMessage()
Display [Escape Failure] message.

#### (static) displayEscapeSuccessMessage()
Display [Escape Success] message.

#### (static) displayExp()
Display [Experience Acquired] message.

#### (static) displayGold()
Display [Gold Acquired] message.

#### (static) displayRewards()
Display rewards (experience, gold, items) message.

#### (static) displayStartMessages()
Display [Appearance] message.

#### (static) displayVictoryMessage()
Display [Victory] message.

#### (static) endAction()
End action processing.

#### (static) endBattle(result)
End battle processing.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `result` | [Number](Number.md) | 0: Victory 1: Abort 2: Defeat |

#### (static) endBattlerActions()
**@MZ** End battle actions.

#### (static) endAllBattlersTurn()
**@MZ** End all battlers' turns.

#### (static) endTurn()
End turn processing.

#### (static) finishActorInput()
**@MZ** Finish actor input.

#### (static) forceAction(battler)
Force action.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `battler` | [Game_Battler](Game_Battler.md) | Target battler |

#### (static) gainDropItems()
Return [Drop Items].

#### (static) gainExp()
Return [Experience].

#### (static) gainGold()
Return [Gold].

#### (static) gainRewards()
Return rewards (experience, gold, items).

#### (static) getNextSubject() → {[Game_Battler](Game_Battler.md)}
Returns the next target battler.

#### (static) initMembers()
Initialize member variables.

#### (static) inputtingAction() → {[Game_Action](Game_Action.md)}
Returns the action of the actor that is inputting.

#### (static) invokeAction(subject, target)
Invoke the action of the specified subject against the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

#### (static) invokeCounterAttack(subject, target)
Invoke the counter-attack action of the specified subject against the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

#### (static) invokeMagicReflection(subject, target)
Invoke the magic reflection action of the specified subject against the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

#### (static) invokeNormalAction(subject, target)
Invoke the normal action of the specified subject against the specified target.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `subject` | [Game_Battler](Game_Battler.md) | Target battler |
| `target` | [Game_Battler](Game_Battler.md) | Target battler |

#### (static) isBattleTest() → {Boolean}
Is this a [Battle Test]?

#### (static) isBattleEnd() → {Boolean}
Is it the end of the battle?

#### (static) isInputting() → {Boolean}
Is it currently inputting?

#### (static) isInputtingActor() → {Boolean}
**@MZ** Is the actor currently inputting?

#### (static) isLastActor() → {Boolean}
**@MZ** Is it the last actor?

#### (static) isPreemptive() → {Boolean}
Is it a [Preemptive Attack]?

#### (static) isSurprise() → {Boolean}
Is it a [Surprise Attack]?

#### (static) loadBgmAndBgs()
**@MZ** Load BGM and BGS.

#### (static) onBattleStart()
Process when the battle starts.

#### (static) onTurnStart()
Process when the turn starts.

#### (static) refreshStatus()
**@MZ** Refresh status.

#### (static) setActorInputting(actor)
Set inputting actor.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actor` | [Game_Actor](Game_Actor.md) | Target actor |

#### (static) setInputting(value)
Set inputting state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `value` | Boolean | Inputting state |

#### (static) startBattle()
Start the battle.

#### (static) startInput()
**@MZ** Start input.

#### (static) startTurn()
Start the turn.

#### (static) subject() → {[Game_Battler](Game_Battler.md)}
Returns the subject battler.

#### (static) tpbTurnEnd()
**@MZ** Time progress battle end.

#### (static) update()
Update processing.
