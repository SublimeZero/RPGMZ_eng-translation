# Global

A list of global variables. Generated and managed by [DataManager](DataManager.md).

Many classes referenced in various places are stored in global variables starting with `$`, and they fall into the following categories:

* Data classes with names starting with "data" (JSON files located in the data folder)
* Management classes with names starting with "game"
* Other classes

Many `$gameXxx` variables correspond to saved data, but some are not saved.

---

## Database

#### $dataActors :[Array](Array.md).&lt;[RPG.Actor](RPG.Actor.md)&gt;
JSON for [Actors] (Actors.json).

---

#### $dataAnimations :[Array](Array.md).&lt;[RPG.Animation](RPG.Animation.md)&gt;
JSON for [Animations] (Animations.json).

---

#### $dataArmors :[Array](Array.md).&lt;[RPG.Armor](RPG.Armor.md)&gt;
JSON for [Armors] (Armors.json).

---

#### $dataClasses :[Array](Array.md).&lt;[RPG.Class](RPG.Class.md)&gt;
JSON for [Classes] (Classes.json).

---

#### $dataCommonEvents :[Array](Array.md).&lt;[RPG.CommonEvent](RPG.CommonEvent.md)&gt;
JSON for [Common Events] (CommonEvents.json).

---

#### $dataEnemies :[Array](Array.md).&lt;[RPG.Enemy](RPG.Enemy.md)&gt;
JSON for [Enemies] (Enemies.json).

---

#### $dataItems :[Array](Array.md).&lt;[RPG.Item](RPG.Item.md)&gt;
JSON for [Items] (Items.json).

---

#### $dataMap :[RPG.Map](RPG.Map.md)
JSON for the current map (MapXXX.json, where XXX is a three-digit number).

---

#### $dataMapInfos :[Array](Array.md).&lt;[RPG.MapInfo](RPG.MapInfo.md)&gt;
JSON for the list of maps (MapInfo.json).

---

#### $dataSkills :[Array](Array.md).&lt;[RPG.Skill](RPG.Skill.md)&gt;
JSON for [Skills] (Skills.json).

---

#### $dataStates :[Array](Array.md).&lt;[RPG.State](RPG.State.md)&gt;
JSON for [States] (States.json).

---

#### $dataSystem :[RPG.System](RPG.System.md)
JSON for the [System] (System.json).

---

#### $dataTilesets :[Array](Array.md).&lt;[RPG.Tileset](RPG.Tileset.md)&gt;
JSON for [Tilesets] (Tilesets.json).

---

#### $dataTroops :[Array](Array.md).&lt;[RPG.Troop](RPG.Troop.md)&gt;
JSON for [Troops] (Troops.json).

---

#### $dataWeapons :[Array](Array.md).&lt;[RPG.Weapon](RPG.Weapon.md)&gt;
JSON for [Weapons] (Weapons.json).

---

## Game Data

#### $gameActors :[Game_Actors](Game_Actors.md)
Class for managing [Actors]. ※Saved

---

#### $gameMap :[Game_Map](Game_Map.md)
Class for managing [Maps]. ※Saved

---

#### $gameMessage :[Game_Message](Game_Message.md)
Class for managing [Messages].

---

#### $gameParty :[Game_Party](Game_Party.md)
Class for managing the [Party]. ※Saved

---

#### $gamePlayer :[Game_Player](Game_Player.md)
Class for managing the [Player]. ※Saved

---

#### $gameScreen :[Game_Screen](Game_Screen.md)
Class for managing the screen. ※Saved

---

#### $gameSelfSwitches :[Game_SelfSwitches](Game_SelfSwitches.md)
Class for managing [Self Switches]. ※Saved

---

#### $gameSwitches :[Game_Switches](Game_Switches.md)
Class for managing [Switches]. ※Saved

---

#### $gameSystem :[Game_System](Game_System.md)
Class for managing the [System]. ※Saved

---

#### $gameTemp :[Game_Temp](Game_Temp.md)
Class for holding temporary game data.

---

#### $gameTimer :[Game_Timer](Game_Timer.md)
Class for managing the timer. ※Saved

---

#### $gameTroop :[Game_Troop](Game_Troop.md)
Class for managing [Troops].

---

#### $gameVariables :[Game_Variables](Game_Variables.md)
Class for managing [Variables]. ※Saved

---

## Others

#### $plugins :[Array](Array.md).&lt;[MV.PluginSettings](MV.PluginSettings.md)&gt;
Plugin settings for "RPG Maker MZ" (js/plugins.js).

---

#### $testEvent :[Array](Array.md).&lt;[RPG.EventCommand](RPG.EventCommand.md)&gt;
[Events] passed when a [Test] is executed.

---

#### scriptUrls :[Array](Array.md).&lt;[String](String.md)&gt;
An array of file paths for core script JavaScript files in **@MZ**.

---

#### effekseerWasmUrl :[String](String.md)
The file path for **@MZ** effekseer.wasm.

---

#### main :[Main](Main.md)
**@MZ** Main object.

Other global variables, such as `effekseer` and `process`, are provided by libraries, but details can be referenced on the official sites for Effekseer, NW.js, Pixi.js, etc.
