# Class: SoundManager
A static class that manages audio set in [sound effects].

Data is recorded in the sounds property of the global variable [$dataSystem](global.md#datasystem-rpgsystem).

Related Classes: [RPG.System](RPG.System.md), [WebAudio](WebAudio.md), [Html5Audio](Html5Audio.md), [RPG.AudioFile](RPG.AudioFile.md)

### Methods

#### (static) loadSystemSound (n)
Loads the audio with the specified number.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `n` | [Number](Number.md) | Audio number |

#### (static) playActorCollapse ()
Plays [ally collapse].

#### (static) playActorDamage ()
Plays [ally damage].

#### (static) playBattleStart ()
Plays [battle start].

#### (static) playBossCollapse1 ()
Plays [boss collapse 1].

#### (static) playBossCollapse2 ()
Plays [boss collapse 2].

#### (static) playBuzzer ()
Plays [buzzer].

#### (static) playCancel ()
Plays [cancel].

#### (static) playCursor ()
Plays [cursor].

#### (static) playEnemyAttack ()
Plays [enemy attack].

#### (static) playEnemyCollapse ()
Plays [enemy collapse].

#### (static) playEnemyDamage ()
Plays [enemy damage].

#### (static) playEquip ()
Plays [equip].

#### (static) playEscape ()
Plays [escape].

#### (static) playEvasion ()
Plays [evasion].

#### (static) playLoad ()
Plays [load].

#### (static) playMagicEvasion ()
Plays [magic evasion].

#### (static) playMiss ()
Plays [miss].

#### (static) playOk ()
Plays [ok].

#### (static) playRecovery ()
Plays [recovery].

#### (static) playReflection ()
Plays [magic reflection].

#### (static) playSave ()
Plays [save].

#### (static) playShop ()
Plays [shop].

#### (static) playSystemSound (n)
Plays the audio with the specified number.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `n` | [Number](Number.md) | Audio number |

#### (static) playUseItem ()
Plays [item use].

#### (static) playUseSkill ()
Plays [skill use].

#### (static) preloadImportantSounds ()
Preloads four types of audio: 0: cursor, 1: ok, 2: cancel, 3: buzzer.
