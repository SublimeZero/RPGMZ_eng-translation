[Class Tree](index.md)

# Class: DataManager
A static class that manages the [database].

Handles global variables set with \$XXX and manages save data.

For more details about global variables, see the [Global](global.md) page.

Related Class: [JsonEx](JsonEx.md)

Changes were made in v1.7.0.

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_globalInfo` | Object | [static] System information to be saved |
| `_errors` | [Array](Array.md) | **@MZ** [static] Array of errors |
| `_databaseFiles` | [Array](Array.md).&lt;[MV.DatabaseFile](MV.DatabaseFile.md)&gt; | [static] Information about data files to load |

### Deprecated MV Properties
`_globalId`, `_lastAccessedId`, `_errorUrl`

### Methods

#### (static) checkError ()
Displays errors if any are recorded.

#### (static) correctDataErrors ()
**@MZ** Corrects errors contained in save data.

#### (static) createGameObjects ()
Generates and assigns corresponding objects to global variables starting with $game.

#### (static) earliestSavefileId () → {[Number](Number.md)}
**@MZ** Returns the ID of the oldest save file.

#### (static) emptySavefileId () → {[Number](Number.md)}
**@MZ** Returns the ID of an empty save file.

#### (static) extractArrayMetadata (array)
**@MZ** Decomposes notes contained in the passed data array into metadata and adds it to the data.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `array` | [Array](Array.md)&lt;[RPG.MetaData](RPG.MetaData.md)&gt; | Array of data |

#### (static) extractMetadata (data)
Decomposes the data written in data.note and sets it in data.meta.<br />
The passed data itself is rewritten, so there is no return value.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `data` | Object | [RPG.MetaData](RPG.MetaData.md) |

#### (static) extractSaveContents (contents)
Sets values to global variables starting with $game from the passed object.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `contents` | [MV.SaveContents](MV.SaveContents.md) | Object for global variables |

#### (static) isAnySavefileExists () → {Boolean}
Checks if there is (at least one) save file exists.

#### (static) isArmor (item) → {Boolean}
Checks if the specified item is included in [Armor].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | Object | Such as [RPG.Armor](RPG.Armor.md) |

#### (static) isBattleTest () → {Boolean}
Checks if in [Battle Test] mode.

#### (static) isDatabaseLoaded () → {Boolean}
Checks if the database has finished loading.

#### (static) isEventTest () → {Boolean}
Checks if in [Event Test] mode.

#### (static) isGlobalInfoLoaded () → {Boolean}
**@MZ** Checks if `_globalInfo` has been loaded.

#### (static) isItem (item) → {Boolean}
Checks if the specified item is included in [Items].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | Object | Such as [RPG.Item](RPG.Item.md) |

#### (static) isMapLoaded () → {Boolean}
Checks if the map has finished loading.

#### (static) isMapObject (object) → {Boolean}
**@MZ** Checks if the passed object is a map object.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `object` | Object | Object storing the data |

#### (static) isSkill (item) → {Boolean}
Checks if the specified item is included in [Skills].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | Object | Such as [RPG.Skill](RPG.Skill.md) |

#### (static) isTitleSkip () → {Boolean}
**@MZ1.7.0** Checks if "Skip Title Screen" is selected in the menu.

#### (static) isWeapon (item) → {Boolean}
Checks if the specified item is included in [Weapons].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | Object | Such as [RPG.Weapon](RPG.Weapon.md) |

#### (static) latestSavefileId () → {[Number](Number.md)}
Returns the ID of the latest save file.

#### (static) loadAllSavefileImages ()
Loads images for all save files.

#### (static) loadDatabase ()
Loads database files (JSON assigned to global variables starting with $data). However, $dataMap is treated separately.

#### (static) loadDataFile (name, src)
Loads the specified data. The onLoad function is called when loading is complete.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `name` | [String](String.md) | Global variable name for data assignment $dataXXX |
| `src` | [String](String.md) | Filename under data/ |

#### (static) loadGame (savefileId)
Loads data from the specified save file ID.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `savefileId` | [Number](Number.md) | Save file ID |

#### (static) loadGlobalInfo ()
Loads the information of the save file ("global").<br />
The information is saved in `_globalInfo`.

#### (static) loadMapData (mapId)
Loads map data. On completion, onLoad is called.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `mapId` | [Number](Number.md) | 1: Creates an empty map |

#### (static) loadSavefileImages (info)
Loads necessary images for the save file.<br />
The loaded images are stored in [ImageManager](ImageManager.md).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `info` | [MV.SaveFileInfo](MV.SaveFileInfo.md) | Save file information |

#### (static) makeEmptyMap ()
Creates an empty map.

#### (static) makeSaveContents () → {[MV.SaveContents](MV.SaveContents.md)}
Creates data for saving. Returns an object that summarizes global variables starting with $game.

#### (static) makeSavefileInfo () → {[MV.SaveFileInfo](MV.SaveFileInfo.md)}
Creates and returns new save file information.

#### (static) maxSavefiles () → {[Number](Number.md)}
Returns the maximum number of files that can be saved.

#### (static) makeSavename (savefileId)
**@MZ** Returns the save name from the specified save file ID.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `savefileId` | [Number](Number.md) | Save file ID |

#### (static) onLoad (object)
Handler called when data loading is complete.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `object` | Object | Object that contains the data |

#### (static) onXhrLoad (xhr, name, src, url)
**@MZ** Handler called when xhr (XMLHttpRequest) data loading is complete.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `xhr` | XMLHttpRequest | Object that contains the data |
| `name` | [String](String.md) | Global variable name for data assignment $dataXXX |
| `src` | [String](String.md) | Filename under data/ |
| `url` | [String](String.md) | Path including data/ |

#### (static) onXhrError (name, src, url)
**@MZ** Handler called when an error occurs during xhr (XMLHttpRequest) data loading.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `name` | [String](String.md) | Global variable name for data assignment $dataXXX |
| `src` | [String](String.md) | Filename under data/ |
| `url` | [String](String.md) | Path including data/ |

#### (static) removeInvalidGlobalInfo ()
**@MZ** Removes invalid information from `_globalInfo`.

#### (static) savefileExists (savefileId)
**@MZ** Checks if a save file with the specified ID exists.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `savefileId` | [Number](Number.md) | Save file ID |

#### (static) saveGame (savefileId) → {Boolean}
Saves game data to the save file and indicates whether the save was successful.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `savefileId` | [Number](Number.md) | Save file ID |

#### (static) savefileInfo (savefileId) → {[MV.SaveFileInfo](MV.SaveFileInfo.md)}
**@MZ** Gets the save file information for the specified ID.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `savefileId` | [Number](Number.md) | Save file ID |

#### (static) saveGlobalInfo (info)
Saves save file information.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `info` | [MV.SaveFileInfo](MV.SaveFileInfo.md) | Save file information |

#### (static) selectSavefileForNewGame ()
Selects a save file for a new game.

#### (static) setupBattleTest ()
Prepares for [Battle Test].

#### (static) setupEventTest ()
Prepares for [Event Test].

#### (static) setupNewGame ()
Prepares for a new game.

### Deprecated MV Methods
[static] loadGameWithoutRescue (savefileId), isThisGameFile (savefileId), loadSavefileInfo (savefileId), lastAccessedSavefileId (), saveGameWithoutRescue (savefileId)
