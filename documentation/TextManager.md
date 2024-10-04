[Class Tree](index.md)

# Class: TextManager
A static class that manages text related to [terms].

It provides an easier way to access the [RPG.System.Terms](RPG.System.Terms.md) stored in the global variable [$dataSystem](global.md#datasystem-rpgsystem). 

The available methods are intended for preparing properties, and it is usually sufficient to directly access the necessary properties.

---

### Properties

| Identifier       | Type                | Description               |
|------------------|---------------------|---------------------------|
| `currencyUnit`   | [String](String.md) | [static][read-only] [Currency Unit] |
| `level`          | [String](String.md) | [static][read-only] [Level] |
| `levelA`        | [String](String.md) | [static][read-only] [Level (Abbreviation)] |
| `hp`             | [String](String.md) | [static][read-only] [HP] |
| `hpA`            | [String](String.md) | [static][read-only] [HP (Abbreviation)] |
| `mp`             | [String](String.md) | [static][read-only] [MP] |
| `mpA`            | [String](String.md) | [static][read-only] [MP (Abbreviation)] |
| `tp`             | [String](String.md) | [static][read-only] [TP] |
| `tpA`            | [String](String.md) | [static][read-only] [TP (Abbreviation)] |
| `exp`            | [String](String.md) | [static][read-only] [Experience Points] |
| `expA`           | [String](String.md) | [static][read-only] [Experience Points (Abbreviation)] |
| `fight`          | [String](String.md) | [static][read-only] [Fight] |
| `escape`         | [String](String.md) | [static][read-only] [Escape] |
| `attack`         | [String](String.md) | [static][read-only] [Attack] |
| `guard`          | [String](String.md) | [static][read-only] [Guard] |
| `item`           | [String](String.md) | [static][read-only] [Item] |
| `skill`          | [String](String.md) | [static][read-only] [Skill] |
| `equip`          | [String](String.md) | [static][read-only] [Equip] (Main Menu) |
| `status`         | [String](String.md) | [static][read-only] [Status] |
| `formation`      | [String](String.md) | [static][read-only] [Formation] |
| `save`           | [String](String.md) | [static][read-only] [Save] |
| `gameEnd`       | [String](String.md) | [static][read-only] [End Game] |
| `options`        | [String](String.md) | [static][read-only] [Options] |
| `weapon`         | [String](String.md) | [static][read-only] [Weapon] |
| `armor`          | [String](String.md) | [static][read-only] [Armor] |
| `keyItem`        | [String](String.md) | [static][read-only] [Key Item] |
| `equip2`         | [String](String.md) | [static][read-only] [Equip] (Equip Menu) |
| `optimize`       | [String](String.md) | [static][read-only] [Optimize Equipment] |
| `clear`          | [String](String.md) | [static][read-only] [Clear All] |
| `newGame`        | [String](String.md) | [static][read-only] [New Game] |
| `continue_`      | [String](String.md) | [static][read-only] [Continue] |
| `toTitle`        | [String](String.md) | [static][read-only] [To Title] |
| `cancel`         | [String](String.md) | [static][read-only] [Cancel] |
| `buy`            | [String](String.md) | [static][read-only] [Buy] |
| `sell`           | [String](String.md) | [static][read-only] [Sell] |
| `alwaysDash`     | [String](String.md) | [static][read-only] [Always Dash] |
| `commandRemember` | [String](String.md) | [static][read-only] [Command Remember] |
| `touchUI`        | [String](String.md) | **@MZ** [static][read-only] [Touch UI] |
| `bgmVolume`      | [String](String.md) | [static][read-only] [BGM Volume] |
| `bgsVolume`      | [String](String.md) | [static][read-only] [BGS Volume] |
| `meVolume`       | [String](String.md) | [static][read-only] [ME Volume] |
| `seVolume`       | [String](String.md) | [static][read-only] [SE Volume] |
| `possession`     | [String](String.md) | [static][read-only] [Possessed Amount] |
| `expTotal`       | [String](String.md) | [static][read-only] [Current Experience Points] |
| `expNext`        | [String](String.md) | [static][read-only] [Next Level] |
| `saveMessage`    | [String](String.md) | [static][read-only] [Save Message] |
| `loadMessage`    | [String](String.md) | [static][read-only] [Load Message] |
| `autosave`       | [String](String.md) | **@MZ** [static][read-only] [Auto Save] |
| `file`           | [String](String.md) | [static][read-only] [File] |
| `partyName`      | [String](String.md) | [static][read-only] [Party Name] |
| `emerge`         | [String](String.md) | [static][read-only] [Emerge] |
| `preemptive`     | [String](String.md) | [static][read-only] [Preemptive Attack] |
| `surprise`       | [String](String.md) | [static][read-only] [Surprise Attack] |
| `escapeStart`    | [String](String.md) | [static][read-only] [Escape Start] |
| `escapeFailure`   | [String](String.md) | [static][read-only] [Escape Failure] |
| `victory`        | [String](String.md) | [static][read-only] [Victory] |
| `defeat`         | [String](String.md) | [static][read-only] [Defeat] |
| `obtainExp`      | [String](String.md) | [static][read-only] [Experience Points Obtained] |
| `obtainGold`     | [String](String.md) | [static][read-only] [Gold Obtained] |
| `obtainItem`     | [String](String.md) | [static][read-only] [Item Obtained] |
| `levelUp`        | [String](String.md) | [static][read-only] [Level Up] |
| `obtainSkill`    | [String](String.md) | [static][read-only] [Skill Acquired] |
| `useItem`        | [String](String.md) | [static][read-only] [Item Used] |
| `criticalToEnemy`| [String](String.md) | [static][read-only] [Critical Hit to Enemy] |
| `criticalToActor`| [String](String.md) | [static][read-only] [Critical Hit to Ally] |
| `actorDamage`    | [String](String.md) | [static][read-only] [Ally Damage] |
| `actorRecovery`   | [String](String.md) | [static][read-only] [Ally Recovery] |
| `actorGain`      | [String](String.md) | [static][read-only] [Ally Points Increase] |
| `actorLoss`      | [String](String.md) | [static][read-only] [Ally Points Decrease] |
| `actorDrain`     | [String](String.md) | [static][read-only] [Ally Points Absorb] |
| `actorNoDamage`  | [String](String.md) | [static][read-only] [Ally No Damage] |
| `actorNoHit`     | [String](String.md) | [static][read-only] [Missed Ally Attack] |
| `enemyDamage`    | [String](String.md) | [static][read-only] [Enemy Damage] |
| `enemyRecovery`   | [String](String.md) | [static][read-only] [Enemy Recovery] |
| `enemyGain`      | [String](String.md) | [static][read-only] [Enemy Points Increase] |
| `enemyLoss`      | [String](String.md) | [static][read-only] [Enemy Points Decrease] |
| `enemyDrain` | [String](String.md) | [static][read-only] [Enemy Point Drain] |
| `enemyNoDamage` | [String](String.md) | [static][read-only] [No Damage to Enemy] |
| `enemyNoHit` | [String](String.md) | [static][read-only] [Missed Hit on Enemy] |
| `evasion` | [String](String.md) | [static][read-only] [Evasion] |
| `magicEvasion` | [String](String.md) | [static][read-only] [Magic Evasion] |
| `magicReflection` | [String](String.md) | [static][read-only] [Magic Reflection] |
| `counterAttack` | [String](String.md) | [static][read-only] [Counter Attack] |
| `substitute` | [String](String.md) | [static][read-only] [Substitute] |
| `buffAdd` | [String](String.md) | [static][read-only] [Buff Add] |
| `debuffAdd` | [String](String.md) | [static][read-only] [Debuff Add] |
| `buffRemove` | [String](String.md) | [static][read-only] [Remove Buff/Debuff] |
| `actionFailure` | [String](String.md) | [static][read-only] [Action Failure] |

---

### Methods

#### (static) basic (basicId) → {[String](String.md)}
Returns the term for the specified ID of [[Basic Status]](RPG.System.Terms.md#基本ステータス).

##### Arguments

| Name | Type | Description |
|------|------|-------------|
| `basicId` | [Number](Number.md) | Basic Status ID |

---

#### (static) command (commandId) → {[String](String.md)}
Returns the term for the specified ID of [[Command]](RPG.System.Terms.md#コマンド).

##### Arguments

| Name | Type | Description |
|------|------|-------------|
| `commandId` | [Number](Number.md) | Command ID |

---

#### (static) getter (method, param) → {Object}
Returns a getter object { get: Function, configurable: Boolean } for the specified method and ID.  
Used when properties are read.

##### Arguments

| Name | Type | Description |
|------|------|-------------|
| `method` | [String](String.md) | Method name ("basic", "param", "command", "message") |
| `param` | [Number](Number.md) \| [String](String.md) | ID for each method |

---

#### (static) message (messageId) → {[String](String.md)}
Returns the term for the specified ID of [[Message]](RPG.System.Terms.md#メッセージ).

##### Arguments

| Name | Type | Description |
|------|------|-------------|
| `messageId` | [String](String.md) | Message ID |

---

#### (static) param (paramId) → {[String](String.md)}
Returns the term for the specified ID of [[Parameter]](RPG.System.Terms.md#能力値).

##### Arguments

| Name | Type | Description |
|------|------|-------------|
| `paramId` | [Number](Number.md) | Parameter ID |
