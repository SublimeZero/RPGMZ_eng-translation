[Class Tree](index.md)

# Class: [RPG](RPG.md).System

| Database       | JSON File     | Global Variable                           | Object |
|----------------|----------------|------------------------------------------|--------|
| [System]       | System.json    | [$dataSystem](global.md#datasystem-rpgsystem) |        |

Related Classes: [Game_System](Game_System.md), [Game_Variables](Game_Variables.md), [Game_Switches](Game_Switches.md), [TextManager](TextManager.md)


### Properties

| Identifier                  | Type                                           | Description                                  |
|-----------------------------|------------------------------------------------|----------------------------------------------|
| `gameTitle`                 | [String](String.md) | [Game Title]                               |
| `versionId`                 | [Number](Number.md) | Version ID automatically saved by "RPG Maker MZ" |
| `locale`                    | [String](String.md) | Locale settings ja_JP, en_US, zh_CN, zh_TW, ko_KR, ru_RU |
| `partyMembers`              | [Array](Array.md).&lt;[Number](Number.md)&gt; | [Initial Party] Array of Actor IDs         |
| `currencyUnit`              | [String](String.md) | [Currency Unit]                           |
| `windowTone`                | [Array](Array.md).&lt;[Number](Number.md)&gt; | [Window Color]                             |
| `attackMotions`             | [Array](Array.md).&lt;[RPG.System.AttackMotion](RPG.System.AttackMotion.md)&gt; | Array of [SV] Attack Motions               |
| `battleSystem`              | [Number](Number.md) | **@MZ** [Battle System]                    |
| `elements`                  | [Array](Array.md).&lt;[String](String.md)&gt; | Array of names corresponding to [Attribute ID](RPG.Damage.md#attribute-id) |
| `equipTypes`                | [Array](Array.md).&lt;[String](String.md)&gt; | Array of names corresponding to [Equipment Type ID](RPG.Trait.md#equipment-type-id) |
| `skillTypes`                | [Array](Array.md).&lt;[String](String.md)&gt; | Array of names corresponding to [Skill Type ID](RPG.Trait.md#skill-type-id) |
| `weaponTypes`               | [Array](Array.md).&lt;[String](String.md)&gt; | Array of names corresponding to [Weapon Type ID](RPG.Trait.md#weapon-type-id) |
| `armorTypes`                | [Array](Array.md).&lt;[String](String.md)&gt; | Array of names corresponding to [Armor Type ID](RPG.Trait.md#armor-type-id) |
| `switches`                  | [Array](Array.md).&lt;[String](String.md)&gt; | Array of names for [Switches] (0 position is an empty string) |
| `variables`                 | [Array](Array.md).&lt;[String](String.md)&gt; | Array of names for [Variables] (0 position is an empty string) |
| `boat`                      | [RPG.System.Vehicle](RPG.System.Vehicle.md) | Settings for [Small Boat]                   |
| `ship`                      | [RPG.System.Vehicle](RPG.System.Vehicle.md) | Settings for [Large Ship]                   |
| `airship`                   | [RPG.System.Vehicle](RPG.System.Vehicle.md) | Settings for [Airship]                      |
| `title1Name`                | [String](String.md) | Background image for the title screen (without extension) |
| `title2Name`                | [String](String.md) | Frame image for the title screen (without extension) |
| `optDrawTitle`              | Boolean            | [Draw Game Title]                         |
| `optTransparent`            | Boolean            | [Start in Transparent State]               |
| `optFollowers`              | Boolean            | [Party Member Formation Walking]           |
| `optSlipDeath`              | Boolean            | [Knocked Out by Slip Damage]               |
| `optFloorDeath`             | Boolean            | [Knocked Out by Floor Damage]              |
| `optDisplayTp`              | Boolean            | [Display TP in Window]                     |
| `optExtraExp`               | Boolean            | [Reserve Members Also Gain Experience]     |
| `optKeyItemsNumber`         | Boolean            | **@MZ** [Display Number of Key Items]      |
| `optSideView`               | Boolean            | [Use Side View Battle]                     |
| `optAutosave`               | Boolean            | **@MZ** [Enable Autosave]                  |
| `titleBgm`                  | [RPG.AudioFile](RPG.AudioFile.md) | [Music]-[Type]-[Title]                     |
| `battleBgm`                 | [RPG.AudioFile](RPG.AudioFile.md) | [Music]-[Type]-[Battle]                     |
| `victoryMe`                 | [RPG.AudioFile](RPG.AudioFile.md) | **@MZ** [Music]-[Type]-[Victory]           |
| `defeatMe`                  | [RPG.AudioFile](RPG.AudioFile.md) | **@MZ** [Music]-[Type]-[Defeat]            |
| `gameoverMe`                | [RPG.AudioFile](RPG.AudioFile.md) | [Music]-[Type]-[Game Over]                  |
| `sounds`                    | [Array](Array.md).&lt;[RPG.AudioFile](RPG.AudioFile.md)&gt; | Array of sound data for [Sound Effects]    |
| `startMapId`                | [Number](Number.md) | Map ID for the Player's [Starting Position] |
| `startX`                    | [Number](Number.md) | x-coordinate (in tiles) for Player's [Starting Position] |
| `startY`                    | [Number](Number.md) | y-coordinate (in tiles) for Player's [Starting Position] |
| `terms`                     | [RPG.System.Terms](RPG.System.Terms.md) | Contents of the [Terms] tab                |
| `testBattlers`              | [Array](Array.md).&lt;[RPG.System.TestBattler](RPG.System.TestBattler.md)&gt; | Party for Combat Testing                     |
| `testTroopId`               | [Number](Number.md) | Enemy group ID for Combat Testing           |
| `battleback1Name`           | [String](String.md) | Background image 1 for Combat Testing (without extension) |
| `battleback2Name`           | [String](String.md) | Background image 2 for Combat Testing (without extension) |
| `battlerName`               | [String](String.md) | Background image during Animation Production (without extension) |
| `battlerHue`                | [Number](Number.md) | Hue of the [Enemy Character] during Animation Production (0–360) |
| `editMapId`                 | [Number](Number.md) | Map ID of the last edited map               |
| `advanced`                  | [RPG.System.Advanced](RPG.System.Advanced.md) | **@MZ** [Advanced Settings]                 |
| `menuCommands`              | [Array](Array.md).&lt;Boolean&gt; | **@MZ** [Menu Commands]                     |
| `itemCategories`            | [Array](Array.md).&lt;Boolean&gt; | **@MZ** [Item Categories]                   |
| `magicSkills`               | [Array](Array.md).&lt;[Number](Number.md)&gt; | **@MZ** [SV Magic Skills]                   |
| `titleCommandWindow`        | [RPG.System.titleCommandWindow](RPG.System.titleCommandWindow.md) | **@MZ** [Command Window]                    |

### Deprecated MV Properties
`battleEndMe`

### Inner Classes

* [RPG.System.Advanced](RPG.System.Advanced.md) **@MZ**
* [RPG.System.AttackMotion](RPG.System.AttackMotion.md)
* [RPG.System.titleCommandWindow](RPG.System.titleCommandWindow.md) **@MZ**
* [RPG.System.Terms](RPG.System.Terms.md)
* [RPG.System.TestBattler](RPG.System.TestBattler.md)
* [RPG.System.Vehicle](RPG.System.Vehicle.md)
