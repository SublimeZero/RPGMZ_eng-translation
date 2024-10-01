[Class Tree](index.md)

# Class: [MV](MV.md).BattleLogMethod

## Type: Object
Parameters stored for calling methods from [Window_BattleLog](Window_BattleLog.md) at a later time.

Related class: [TextManager](TextManager.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `name` | [String](String.md) | [Method Name](MV.BattleLogMethod.md#method-name) |
| `params` | [Array](Array.md) | Array of arguments (see details in each method description) |

#### Method Names
The `BaseLine` is the line number used to separate the display, for example, when showing continuous damage. After displaying, the process returns to this line number.<br />
Note that when `popBaseLine` is used, the record of the line returns, but the display remains until the next line is shown.

Line numbers:

| Method | Description | param1 | param2 | param3 |
| --- | --- | --- | --- | --- |
| [addText](Window_BattleLog.md#addtext-text) | Adds a line | [String](String.md) |
| [clear](Window_BattleLog.md#clear-) | Clears the display |
| [performAction](Window_BattleLog.md#performaction-subject-action) | Applies an action | [Game_Battler](Game_Battler.md) | [Game_Action](Game_Action.md) |
| [performActionEnd](Window_BattleLog.md#performactionend-subject) | Applies the end of an action | [Game_Battler](Game_Battler.md) |
| [performActionStart](Window_BattleLog.md#performactionstart-subject-action) | Applies the start of an action | [Game_Battler](Game_Battler.md) | [Game_Action](Game_Action.md) |
| [performCollapse](Window_BattleLog.md#performcollapse-target) | Applies a collapse (defeat) | [Game_Battler](Game_Battler.md) |
| [performCounter](Window_BattleLog.md#performcounter-target) | Applies a counterattack | [Game_Battler](Game_Battler.md) |
| [performDamage](Window_BattleLog.md#performdamage-target) | Applies damage | [Game_Battler](Game_Battler.md) |
| [performEvasion](Window_BattleLog.md#performevasion-target) | Applies evasion | [Game_Battler](Game_Battler.md) |
| [performMagicEvasion](Window_BattleLog.md#performmagicevasion-target) | Applies magic evasion | [Game_Battler](Game_Battler.md) |
| [performMiss](Window_BattleLog.md#performmiss-target) | Applies a missed attack | [Game_Battler](Game_Battler.md) |
| [performRecovery](Window_BattleLog.md#performrecovery-target) | Applies recovery | [Game_Battler](Game_Battler.md) |
| [performReflection](Window_BattleLog.md#performreflection-target) | Applies reflection | [Game_Battler](Game_Battler.md) |
| [performSubstitute](Window_BattleLog.md#performsubstitute-target) | Applies a "cover" action | [Game_Battler](Game_Battler.md) |
| [popBaseLine](Window_BattleLog.md#popbaseline-) | Returns to the recorded baseline |
| [popupDamage](Window_BattleLog.md#popupdamage-target) | Displays damage popup | [Game_Battler](Game_Battler.md) |
| [pushBaseLine](Window_BattleLog.md#pushbaseline-) | Records the baseline |
| [showAnimation](Window_BattleLog.md#showanimation-subject-targets-animationid) | Displays an animation | [Game_Battler](Game_Battler.md) | [Array](Array.md).&lt;[Game_Battler](Game_Battler.md)&gt; | [Number](Number.md) |
| [wait](Window_BattleLog.md#wait-) | Waits |
| [waitForEffect](Window_BattleLog.md#waitforeffect-) | Waits for the effect |
| [waitForMovement](Window_BattleLog.md#waitformovement-) | Waits for movement |
| [waitForNewLine](Window_BattleLog.md#waitfornewline-) | Waits for a new line |
