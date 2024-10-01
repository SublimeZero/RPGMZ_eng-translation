[Class Tree](index.md)

# Class: Game_System

| Global Variable | Save Data |
| --- | --- |
| [$gameSystem](global.md#gamesystem-game_system) | Saved |

A class for handling changing system data.<br />
It is often used as an object to store plugin data, but there is no particular measure against identifier collisions, so identifiers from plugins created by different authors may overlap.

Changes were made in v1.3.0, v1.7.0, and v1.8.1.

Related Classes: [RPG.System](RPG.System.md)

### new Game_System ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_saveEnabled` | Boolean | Whether the [Save] menu is available |
| `_menuEnabled` | Boolean | Whether the menu is displayed |
| `_encounterEnabled` | Boolean | Whether encounters are available |
| `_formationEnabled` | Boolean | Whether the [Formation] menu is available |
| `_battleCount` | [Number](Number.md) | Number of battles |
| `_winCount` | [Number](Number.md) | Number of victories |
| `_escapeCount` | [Number](Number.md) | Number of escapes |
| `_saveCount` | [Number](Number.md) | Number of saves |
| `_versionId` | [Number](Number.md) | Version ID |
| `_savefileId` | [Number](Number.md) | **@MZ** Save file ID |
| `_framesOnSave` | [Number](Number.md) | Accumulated frames on save |
| `_bgmOnSave` | [RPG.AudioFile](RPG.AudioFile.md) | Saved BGM |
| `_bgsOnSave` | [RPG.AudioFile](RPG.AudioFile.md) | Saved BGS |
| `_windowTone` | [MV.Tone](MV.Tone.md) | Window tone |
| `_battleBgm` | [RPG.AudioFile](RPG.AudioFile.md) | [Music - Type - Battle] |
| `_victoryMe` | [RPG.AudioFile](RPG.AudioFile.md) | [Music - Type - Victory] |
| `_defeatMe` | [RPG.AudioFile](RPG.AudioFile.md) | [Music - Type - Defeat] |
| `_savedBgm` | [RPG.AudioFile](RPG.AudioFile.md) | Saved BGM |
| `_walkingBgm` | [RPG.AudioFile](RPG.AudioFile.md) | Walking BGM |

### Methods

#### battleBgm () → {[RPG.AudioFile](RPG.AudioFile.md)}
Returns the battle BGM.


#### battleCount () → {[Number](Number.md)}
Returns the number of battles.


#### defeatMe () → {[RPG.AudioFile](RPG.AudioFile.md)}
Returns the defeat ME.


#### disableEncounter ()
Changes to no encounters.


#### disableFormation ()
Changes to no [Formation] menu.


#### disableMenu ()
Changes to no menu display.


#### disableSave ()
Changes to no [Save] menu.


#### enableEncounter ()
Changes to enable encounters.


#### enableFormation ()
Changes to enable [Formation] menu.


#### enableMenu ()
Changes to enable menu display.


#### enableSave ()
Changes to enable [Save] menu.


#### escapeCount () → {[Number](Number.md)}
Returns the number of escapes.


#### initialize ()
Initialization at the time of object creation.


#### isAutosaveEnabled () → {Boolean}
Whether **@MZ** auto-save is possible.


#### isChinese () → {Boolean}
Whether the locale is Chinese.


#### isCJK () → {Boolean}
Whether the locale is Japanese, Korean, or Chinese.


#### isEncounterEnabled () → {Boolean}
Whether encounters are enabled.


#### isFormationEnabled () → {Boolean}
Whether the [Formation] menu is available.


#### isJapanese () → {Boolean}
Whether the locale is Japanese.


#### isKorean () → {Boolean}
Whether the locale is Korean.


#### isMenuEnabled () → {Boolean}
Whether the menu display is enabled.


#### isMessageSkipEnabled () → {Boolean}
Whether [Enable Message Skip] is ON in **@MZ1.8.1**.


#### isRussian () → {Boolean}
Whether the locale is Russian.


#### isSaveEnabled () → {Boolean}
Whether the [Save] menu is available.


#### isSideView () → {Boolean}
Whether it is side-view combat.


#### mainFontFace () → {[String](String.md)}
Returns the main font (a list of font names separated by commas) for **@MZ**.


#### numberFontFace () → {[String](String.md)}
Returns the number font (a list of font names separated by commas) for **@MZ**.


#### onAfterLoad ()
Handler called after loading completes.


#### onBattleEscape ()
Handler called when escaping from battle.


#### onBattleStart ()
Handler called when a battle starts.


#### onBattleWin ()
Handler called when winning a battle.


#### onBeforeSave ()
Handler called before saving.


#### playtime () → {[Number](Number.md)}
Returns playtime.


#### playtimeText () → {[String](String.md)}
Returns playtime as a string.


#### replayBgm ()
Plays the saved BGM from where it left off.


#### replayWalkingBgm ()
Plays the walking BGM from where it left off.


#### saveBgm ()
Saves the current BGM.


#### saveCount () → {[Number](Number.md)}
Returns the number of saves.


#### saveWalkingBgm ()
Saves the walking BGM.


#### saveWalkingBgm2 ()
Saves the second walking BGM.


#### setBattleBgm (value)
Sets the specified battle BGM.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `value` | [RPG.AudioFile](RPG.AudioFile.md) | Battle BGM |


#### setDefeatMe (value)
Sets the defeat ME.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `value` | [RPG.AudioFile](RPG.AudioFile.md) | Defeat ME |


#### savefileId () → {[Number](Number.md)}
Returns the **@MZ** save file ID.


#### setSavefileId (savefileId)
Sets the **@MZ** save file ID.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `savefileId` | [Number](Number.md) | Save file ID |


#### setVictoryMe (value)
Sets the victory ME.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `value` | [RPG.AudioFile](RPG.AudioFile.md) | Victory ME |


#### setWindowTone (value)
Sets the specified [Window Color].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `value` | [Array](Array.md).<[Number](Number.md)> | An array of [r, g, b] values (each -255 to 255) |


#### versionId () → {[Number](Number.md)}
Returns the version ID.


#### victoryMe () → {[RPG.AudioFile](RPG.AudioFile.md)}
Returns the victory ME.


#### winCount () → {[Number](Number.md)}
Returns the number of victories.


#### windowOpacity () → {[Number](Number.md)}
**@MZ1.3.0** Returns the window's opacity (default: 192).


#### windowPadding () → {[Number](Number.md)}
**@MZ** Returns the width from the window edge to the content (default: 12 pixels).


#### windowTone () → {[MV.Tone](MV.Tone.md)}
Returns the [Window Color].<br />
The fourth gray value is always 0.
