[Class Tree](index.md)

# Class: [RPG](RPG.md).[System](RPG.System.md).Terms
JSON data for [Terms].

Related Class: [TextManager](TextManager.md)

### Properties

| Identifier                  | Type                                           | Description                             |
|-----------------------------|------------------------------------------------|-----------------------------------------|
| `basic`                     | [Array](Array.md).&lt;[String](String.md)&gt; | [Basic Status](#[Basic Status])       |
| `params`                    | [Array](Array.md).&lt;[String](String.md)&gt; | [Attributes](#[Attributes])            |
| `commands`                  | [Array](Array.md).&lt;[String](String.md)&gt; | [Commands](#[Commands])                |
| `messages`                  | Object.&lt;[String](String.md)&gt;          | [Messages](#[Messages])                |

#### [Basic Status]

| Number | Term          |
|--------|---------------|
| 0      | Level         |
| 1      | Level (Abbr.) |
| 2      | HP            |
| 3      | HP (Abbr.)    |
| 4      | MP            |
| 5      | MP (Abbr.)    |
| 6      | TP            |
| 7      | TP (Abbr.)    |
| 8      | Experience    |
| 9      | Experience (Abbr.) |

#### [Attributes]

| Number | Term          |
|--------|---------------|
| 0      | Max HP       |
| 1      | Max MP       |
| 2      | Attack Power  |
| 3      | Defense Power  |
| 4      | Magic Power   |
| 5      | Magic Defense  |
| 6      | Agility       |
| 7      | Luck          |
| 8      | Hit Rate      |
| 9      | Evasion Rate   |

#### [Commands]

| Number | Term          |
|--------|---------------|
| 0      | Fight         |
| 1      | Escape        |
| 2      | Attack        |
| 3      | Defense       |
| 4      | Item          |
| 5      | Skill         |
| 6      | Equip         |
| 7      | Status        |
| 8      | Sort          |
| 9      | Save          |
| 10     | Exit Game     |
| 11     | Options       |
| 12     | Weapon        |
| 13     | Armor         |
| 14     | Important Item|
| 15     | Equip         |
| 16     | Best Equipment |
| 17     | Remove All    |
| 18     | New Game      |
| 19     | Continue      |
| 20     | (Unused)      |
| 21     | Title         |
| 22     | Cancel        |
| 23     | (Unused)      |
| 24     | Buy           |
| 25     | Sell          |

#### [Messages]

| Identifier                  | Term                                 |
|-----------------------------|--------------------------------------|
| `alwaysDash`                | Always Dash                          |
| `commandRemember`           | Command Memory                       |
| `touchUI`                   | Touch UI                             |
| `bgmVolume`                 | BGM Volume                           |
| `bgsVolume`                 | BGS Volume                           |
| `meVolume`                  | ME Volume                            |
| `seVolume`                  | SE Volume                            |
| `possession`                | Number Owned                         |
| `expTotal`                  | Current %1                           |
| `expNext`                   | Until Next %1                       |
| `saveMessage`               | Which file would you like to save?  |
| `loadMessage`               | Which file would you like to load?  |
| `file`                      | File                                 |
| `autosave`                  | Auto Save                            |
| `partyName`                 | %1 and others                        |
| `emerge`                    | %1 appears!                         |
| `preemptive`                | %1 took the initiative!             |
| `surprise`                  | %1 was caught off guard!            |
| `escapeStart`               | %1 fled!                            |
| `escapeFailure`             | But could not escape!               |
| `victory`                   | %1's victory!                       |
| `defeat`                    | %1 was defeated in battle.          |
| `obtainExp`                 | Obtained %2 from %1!                |
| `obtainGold`                | Obtained %1\\G!                     |
| `obtainItem`                | Obtained %1!                        |
| `levelUp`                   | %1 leveled up to %2 %3!             |
| `obtainSkill`               | Learned %1!                         |
| `useItem`                   | %1 used %2!                         |
| `criticalToEnemy`           | Critical Hit!!                      |
| `criticalToActor`           | Devastating Blow!!                  |
| `actorDamage`               | %1 took %2 damage!                  |
| `actorRecovery`             | %1's %2 recovered by %3!            |
| `actorGain`                 | %1's %2 increased by %3!            |
| `actorLoss`                 | %1's %2 decreased by %3!            |
| `actorDrain`                | %1 lost %2 by %3!                   |
| `actorNoDamage`             | %1 took no damage!                  |
| `actorNoHit`                | Miss! %1 took no damage!            |
| `enemyDamage`               | Dealt %2 damage to %1!              |
| `enemyRecovery`             | %1's %2 recovered by %3!            |
| `enemyGain`                 | %1's %2 increased by %3!            |
| `enemyLoss`                 | %1's %2 decreased by %3!            |
| `enemyDrain`                | Took %3 from %1's %2!               |
| `enemyNoDamage`             | Cannot deal damage to %1!           |
| `enemyNoHit`                | Miss! Cannot deal damage to %1!     |
| `evasion`                   | %1 evaded the attack!               |
| `magicEvasion`              | %1 negated the magic!               |
| `magicReflection`           | %1 reflected the magic!             |
| `counterAttack`             | %1's counterattack!                 |
| `substitute`                | %1 protected %2!                    |
| `buffAdd`                   | %1's %2 increased!                   |
| `debuffAdd`                 | %1's %2 decreased!                   |
| `buffRemove`                | %1's %2 returned to normal!         |
| `actionFailure`             | Did not affect %1!                  |
