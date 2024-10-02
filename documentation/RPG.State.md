[Class Tree](index.md)

# Class: [RPG](RPG.md).State

## Superclass: [RPG.MetaData](RPG.MetaData.md)

| Database         | JSON File    | Global Variable                          | Sprite                        |
|------------------|--------------|-----------------------------------------|-------------------------------|
| [State]          | States.json  | [$dataStates](global.md#datastates-arrayrpgstate)(Array) | [Sprite_StateIcon](Sprite_StateIcon.md) |

For information on how to use it in the editor, refer to the official [RPG Maker MV Beginner's Course: State Creation Example](https://tkool.jp/mv/guide/004_007c.html).

Related classes: [Game_BattlerBase](Game_BattlerBase.md), [Game_Battler](Game_Battler.md), [Game_Actor](Game_Actor.md), [Game_Enemy](Game_Enemy.md), [Game_ActionResult](Game_ActionResult.md), [Window_BattleLog](Window_BattleLog.md), [RPG.Effect](RPG.Effect.md), [RPG.Trait](RPG.Trait.md)

### Properties

| Identifier                  | Type                                           | Description                                   |
|-----------------------------|------------------------------------------------|-----------------------------------------------|
| `id`                        | [Number](Number.md)                           | [State ID](#state-id)                        |
| `name`                      | [String](String.md)                           | [Name]                                       |
| `restriction`               | [Number](Number.md)                           | [Action Restriction](#action-restriction)   |
| `priority`                  | [Number](Number.md)                           | [Priority] (0~100)                           |
| `removeAtBattleEnd`         | Boolean                                        | [Remove at Battle End]                        |
| `removeByRestriction`        | Boolean                                        | [Remove by Restriction]                       |
| `autoRemovalTiming`          | [Number](Number.md)                           | [Auto Removal Timing](#auto-removal-timing) |
| `minTurns`                  | [Number](Number.md)                           | Minimum number of [Turns] to last            |
| `maxTurns`                  | [Number](Number.md)                           | Maximum number of [Turns] to last            |
| `removeByDamage`            | Boolean                                        | [Remove by Damage]                           |
| `chanceByDamage`            | [Number](Number.md)                           | [Chance to Remove by Damage] in %           |
| `removeByWalking`           | Boolean                                        | [Remove by Steps]                           |
| `stepToRemove`              | [Number](Number.md)                           | [Steps to Remove]                            |
| `iconIndex`                 | [Number](Number.md)                           | [Icon] Index                                 |
| `message1`                  | [String](String.md)                           | [When Actor Enters this State]               |
| `message2`                  | [String](String.md)                           | [When Enemy Enters this State]               |
| `message3`                  | [String](String.md)                           | [When This State Persists]                   |
| `message4`                  | [String](String.md)                           | [When This State is Removed]                 |
| `motion`                    | [Number](Number.md)                           | [[SV] Motion](#sv-motion)                   |
| `overlay`                   | [Number](Number.md)                           | [[SV] Overlay](#sv-overlay)                 |
| `traits`                    | [Array](Array.md).&lt;[RPG.Trait](RPG.Trait.md)&gt; | Array of [Traits]                          |

#### State ID
ID 1 is the state automatically applied when HP reaches 0.  
Below, ID 0 is fixed; others are default values.

| ID | Description         |
|----|---------------------|
| 0  | Normal              |
| 1  | Unable to Battle    |
| 2  | Defense             |
| 3  | Immortal            |
| 4  | Poison              |
| 5  | Darkness            |
| 6  | Silence             |
| 7  | Rage                |
| 8  | Confusion           |
| 9  | Charm               |
| 10 | Sleep               |

#### [Action Restriction]

| Number | Description         |
|--------|---------------------|
| 0      | None                |
| 1      | Attack Enemy        |
| 2      | Attack Someone      |
| 3      | Attack Ally         |
| 4      | Cannot Act          |

#### [Auto Removal Timing]

| Number | Description         |
|--------|---------------------|
| 0      | None                |
| 1      | At Action End       |
| 2      | At Turn End         |

#### [SV] Overlay
The number specifying images included in img/system/States.png.  
By default, the images correspond to the descriptions, but they do not have to be used with that meaning.  
However, the representation and numbers in the editor cannot be changed.

| Number | Description         |
|--------|---------------------|
| 0      | None                |
| 1      | Poison              |
| 2      | Darkness            |
| 3      | Silence             |
| 4      | Rage                |
| 5      | Confusion           |
| 6      | Charm               |
| 7      | Sleep               |
| 8      | Paralysis           |
| 9      | Curse               |
| 10     | Fear                |
