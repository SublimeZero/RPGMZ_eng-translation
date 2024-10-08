# RPG Maker MZ Unofficial JavaScript Reference - Class Tree

## Table of Contents

* [Main](#main)
* [JavaScript Extensions](#javascript_extensions)
* [Managers](#managers)
* [Utilities](#utilities)
* [Input](#input)
* [Files](#files)
* [Audio](#audio)

### Object Structure Data

* [Objects](#objects) 
* [Arrays](#arrays) 
* [Strings](#strings) 

### Database (JSON)

* [Event Commands](#event_commands)
* [MetaData](#metadata)
* [Other Databases](#other_databases)

### Objects

* [System](#system)
* [Switches & Variables](#switches_and_variables)
* [Map Characters](#map_characters)
* [Battle Characters](#battle_characters)
* [Other Objects](#other_objects)

### Images

* [Core Features](#core_features)
* [Container (PIXI.Container)](#container_pixicontainer)
	* [Sprite](#sprite)
	* [Scene (Scene_Base)](#scene_scene_base)

### Windows

* [Window](#window)
	* [Selectable Window (Window_Selectable)](#selectable_window)
    * [Item List Window (Window_ItemList)](#item_list_window)
    * [Status Base Window (Window_StatusBase)](#status_base_window)
	* [Command Window (Window_Command)](#command_window)

### Annotations

* **@MZ** indicates classes that have been added in "RPG Maker MZ".
* "→ Inheritance" that appears below is a link to the inherited class.

---

## Main

* [Main](Main.md) **@MZ** 

---

## JavaScript Extensions
namespace JsExtensions

* [Array](Array.md)
* [Math](Math.md)
* [Number](Number.md)
* [String](String.md)

---

## Managers

* [AudioManager](AudioManager.md)
* [BattleManager](BattleManager.md)
* [ColorManager](ColorManager.md) **@MZ**
* [ConfigManager](ConfigManager.md)
* [DataManager](DataManager.md)
* [EffectManager](EffectManager.md) **@MZ**
* [FontManager](FontManager.md) **@MZ**
* [ImageManager](ImageManager.md)
* [PluginManager](PluginManager.md) ([Plugin File Settings](MV.PluginSettings.md#Plugin_File_Settings))
* [PluginManagerEx](PluginManagerEx.md) **@MZ PluginCommonBase.js** 
* [SceneManager](SceneManager.md)
* [SoundManager](SoundManager.md)
* [StorageManager](StorageManager.md)
* [TextManager](TextManager.md)

---

## Utilities

* [JsonEx](JsonEx.md)
* [Utils](Utils.md)
* [Video](Video.md) **@MZ**

---

## Input

* [Input](Input.md)
* [TouchInput](TouchInput.md)

---

## Audio

* [WebAudio](WebAudio.md)

---

## Object Structure Data
[RPG MV Namespace](MV.md) 

### Objects

* [MV.AnimationRequest](MV.AnimationRequest.md)
* [MV.AudioParameters](MV.AudioParameters.md)
* [MV.BalloonRequest](MV.BalloonRequest.md)
* [MV.BattleLogMethod](MV.BattleLogMethod.md)
* [MV.BattlerAnimation](MV.BattlerAnimation.md)
* [MV.BattleRewards](MV.BattleRewards.md)
* [MV.CommandItem](MV.CommandItem.md)
* [MV.ConfigData](MV.ConfigData.md)
* [MV.DatabaseFile](MV.DatabaseFile.md)
* [MV.Matrix](MV.Matrix.md)
* [MV.Motion](MV.Motion.md)
* [MV.PluginSettings](MV.PluginSettings.md)
* [MV.Rectangle](MV.Rectangle.md)
* [MV.SaveContents](MV.SaveContents.md)
* [MV.SaveFileInfo](MV.SaveFileInfo.md)
* [MV.Size](MV.Size.md)
* [MV.TextState](MV.TextState.md)
* [MV.TouchInputEvents](MV.TouchInputEvents.md)

---

### Arrays

* [MV.Color](MV.Color.md)
* [MV.SelfSwitch](MV.SelfSwitch.md)
* [MV.TileRect](MV.TileRect.md)
* [MV.Tone](MV.Tone.md)

---

### Strings

* [MV.CssColor](MV.CssColor.md)

---

## Database (JSON)
[RPG Namespace](RPG.md) 

### Event Commands

* [RPG.BattleEventPage](RPG.BattleEventPage.md) 
* [RPG.BattleEventPage.Conditions](RPG.BattleEventPage.Conditions.md)
* [RPG.CommonEvent](RPG.CommonEvent.md)([$dataCommonEvents](global.md#datacommonevents-arrayrpgcommonevent))
* [RPG.EventCommand](RPG.EventCommand.md)([$testEvent](global.md#testevent-arrayrpgeventcommand))
* [RPG.EventPage](RPG.EventPage.md) 
* [RPG.EventPage.Conditions](RPG.EventPage.Conditions.md) 
* [RPG.EventPage.Image](RPG.EventPage.Image.md)
* [RPG.MoveCommand](RPG.MoveCommand.md)
* [RPG.MoveRoute](RPG.MoveRoute.md)

---

### MetaData

* [RPG.MetaData](RPG.MetaData.md)
	* [RPG.Actor](RPG.Actor.md)([$dataActors](global.md#dataactors-arrayrpgactor))
	* [RPG.Class](RPG.Class.md)([$dataClasses](global.md#dataclasses-arrayrpgclass))
    * [RPG.Class.Learning](RPG.Class.Learning.md)
	* [RPG.Enemy](RPG.Enemy.md)([$dataEnemies](global.md#dataenemies-arrayrpgenemy))
    * [RPG.Enemy.Action](RPG.Enemy.Action.md)
    * [RPG.Enemy.DropItem](RPG.Enemy.DropItem.md)
	* [RPG.Event](RPG.Event.md)
	* [RPG.Map](RPG.Map.md)([$dataMap](global.md#datamap-rpgmap))
    * [RPG.Map.Encounter](RPG.Map.Encounter.md)
	* [RPG.State](RPG.State.md)([$dataStates](global.md#datastates-arrayrpgstate))
	* [RPG.Tileset](RPG.Tileset.md)([$dataTilesets](global.md#datatilesets-arrayrpgtileset))
	* [RPG.BaseItem](RPG.BaseItem.md)
	    * [RPG.UsableItem](RPG.UsableItem.md)
	        * [RPG.Item](RPG.Item.md)([$dataItems](global.md#dataitems-arrayrpgitem))
	        * [RPG.Skill](RPG.Skill.md)([$dataSkills](global.md#dataskills-arrayrpgskill))
	    * [RPG.EquipItem](RPG.EquipItem.md)
	        * [RPG.Armor](RPG.Armor.md)([$dataArmors](global.md#dataarmors-arrayrpgarmor))
	        * [RPG.Weapon](RPG.Weapon.md)([$dataWeapons](global.md#dataweapons-arrayrpgweapon))

---

### Other Databases

* [RPG.Animation](RPG.Animation.md)([$dataAnimations](global.md#dataanimations-arrayrpganimation))
* [RPG.Animation.Timing](RPG.Animation.Timing.md)
* [RPG.AudioFile](RPG.AudioFile.md)
* [RPG.MapInfo](RPG.MapInfo.md)([$dataMapInfos](global.md#datamapinfos-arrayrpgmapinfo))
* [RPG.System](RPG.System.md)([$dataSystem](global.md#datasystem-rpgsystem)) 
* [RPG.System.Advanced](RPG.System.Advanced.md) **@MZ** 
* [RPG.System.titleCommandWindow](RPG.System.titleCommandWindow.md) **@MZ** 
* [RPG.System.AttackMotion](RPG.System.AttackMotion.md)
* [RPG.System.Terms](RPG.System.Terms.md) 
* [RPG.System.TestBattler](RPG.System.TestBattler.md)
* [RPG.System.Vehicle](RPG.System.Vehicle.md)
* [RPG.Troop](RPG.Troop.md)([$dataTroops](global.md#datatroops-arrayrpgtroop))
* [RPG.Troop.Member](RPG.Troop.Member.md)
* [RPG.Damage](RPG.Damage.md)
* [RPG.Effect](RPG.Effect.md)
* [RPG.Trait](RPG.Trait.md)

---

## Objects

### System

* [Game_CommonEvent](Game_CommonEvent.md)
* [Game_Interpreter](Game_Interpreter.md)([Event command methods](Game_Interpreter_command.md))
* [Game_System](Game_System.md)([$gameSystem](global.md#gamesystem-game_system))
* [Game_Temp](Game_Temp.md)([$gameTemp](global.md#gametemp-game_temp))
* [Game_Timer](Game_Timer.md)([$gameTimer](global.md#gametimer-game_timer))

---

### Switches & Variables

* [Game_Switches](Game_Switches.md)([$gameSwitches](global.md#gameswitches-game_switches))
* [Game_SelfSwitches](Game_SelfSwitches.md)([$gameSelfSwitches](global.md#gameselfswitches-game_selfswitches))
* [Game_Variables](Game_Variables.md)([$gameVariables](global.md#gamevariables-game_variables))

---

### Map Characters

* [Game_Followers](Game_Followers.md)
* [Game_CharacterBase](Game_CharacterBase.md)
    * [Game_Character](Game_Character.md)
        * [Game_Player](Game_Player.md)([$gamePlayer](global.md#gameplayer-game_player))
        * [Game_Follower](Game_Follower.md)
        * [Game_Event](Game_Event.md)
        * [Game_Vehicle](Game_Vehicle.md)

---

### Battle Characters

* [Game_Action](Game_Action.md)
* [Game_ActionResult](Game_ActionResult.md)
* [Game_Actors](Game_Actors.md)([$gameActors](global.md#dataactors-arrayrpgactor))
* [Game_Unit](Game_Unit.md)
    * [Game_Party](Game_Party.md)([$gameParty](global.md#gameparty-game_party))
    * [Game_Troop](Game_Troop.md)([$gameTroop](global.md#gametroop-game_troop))
* [Game_BattlerBase](Game_BattlerBase.md)
    * [Game_Battler](Game_Battler.md)
        * [Game_Actor](Game_Actor.md)
        * [Game_Enemy](Game_Enemy.md)

---

### Other Objects

* [Game_Item](Game_Item.md)
* [Game_Map](Game_Map.md)([$gameMap](global.md#gamemap-game_map))
* [Game_Message](Game_Message.md)([$gameMessage](global.md#gamemessage-game_message))
* [Game_Picture](Game_Picture.md)
* [Game_Screen](Game_Screen.md)([$gameScreen](global.md#gamescreen-game_screen))

---

## Images

### Core Functions

* [Bitmap](Bitmap.md)
* [Graphics](Graphics.md)
* [PIXI.Application](PIXI.Application.md)
* [PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html)
    * [Point](Point.md)
* [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html)
    * [Rectangle](Rectangle.md)

* [PIXI.utils.EventEmitter](http://pixijs.download/v5.3.12/docs/PIXI.utils.EventEmitter.html)
    * [PIXI.BaseTexture](http://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html)
    * [PIXI.Texture](PIXI.Texture.md)
    * [PIXI.AbstractRenderer](http://pixijs.download/v5.3.12/docs/PIXI.AbstractRenderer.html) 
        * [PIXI.Renderer](PIXI.Renderer.md)
    * [PIXI.DisplayObject](PIXI.DisplayObject.md)
        * [PIXI.Container](PIXI.Container.md) → [Inheritance](#Container_pixicontainer)

* [PIXI.System](https://pixijs.download/release/docs/PIXI.System.html)
    * [PIXI.ObjectRenderer](https://pixijs.download/release/docs/PIXI.ObjectRenderer.html)
        * [Tilemap.Renderer](Tilemap.Renderer.md)  **@MZ**

* [PIXI.Shader](PIXI.Shader.md)
    * [PIXI.Filter](PIXI.Filter.md)
        * [ColorFilter](ColorFilter.md) **@MZ**

---

### [Container (PIXI.Container)](PIXI.Container.md)

* [ScreenSprite](ScreenSprite.md)
* [Weather](Weather.md)
* [WindowLayer](WindowLayer.md)
* [PIXI.Graphics](PIXI.Graphics.md)
* [Tilemap](Tilemap.md)
* [Tilemap.Layer](Tilemap.Layer.md)  **@MZ**
* [Tilemap.CombinedLayer](Tilemap.CombinedLayer.md)   **@MZ1.7.0**
* [PIXI.Sprite](PIXI.Sprite.md)
    * [Sprite](Sprite.md) → [Inheritance](#Sprite_sprite)
    * [PIXI.TilingSprite](http://pixijs.download/v5.3.12/docs/PIXI.TilingSprite.html)
        * [TilingSprite](TilingSprite.md) (Inheritance position changed)
            * [Sprite_Battleback](Sprite_Battleback.md) **@MZ**
* [Stage](Stage.md)
    * [Scene_Base](Scene_Base.md) → [Inheritance](#Scene_scene_base)
* [Window](Window.md) → [Inheritance](#Window_window)

---

### [Sprite (Sprite)](Sprite.md)

* [Sprite_Animation](Sprite_Animation.md)
* [Sprite_AnimationMV](Sprite_AnimationMV.md) **@MZ**
* [Sprite_Balloon](Sprite_Balloon.md) (Inheritance position changed)
* [Sprite_Character](Sprite_Character.md) (Inheritance position changed)
* [Sprite_Damage](Sprite_Damage.md)
* [Sprite_Destination](Sprite_Destination.md)
* [Sprite_Gauge](Sprite_Gauge.md) **@MZ**
* [Sprite_Name](Sprite_Name.md) **@MZ**
* [Sprite_StateIcon](Sprite_StateIcon.md)
* [Sprite_StateOverlay](Sprite_StateOverlay.md) (Inheritance position changed)
* [Sprite_Timer](Sprite_Timer.md)
* [Sprite_Weapon](Sprite_Weapon.md) (Inheritance position changed)
* [Sprite_Clickable](Sprite_Clickable.md) **@MZ**
    * [Sprite_Button](Sprite_Button.md) (Inheritance position changed)
    * [Sprite_Picture](Sprite_Picture.md) (Inheritance position changed)
    * [Sprite_Battler](Sprite_Battler.md) (Inheritance position changed)
        * [Sprite_Actor](Sprite_Actor.md)
        * [Sprite_Enemy](Sprite_Enemy.md)
* [Spriteset_Base](Spriteset_Base.md)
    * [Spriteset_Battle](Spriteset_Battle.md)
    * [Spriteset_Map](Spriteset_Map.md)

---

### [Scene (Scene_Base)](Scene_Base.md)

* [Scene_Boot](Scene_Boot.md)
* [Scene_Gameover](Scene_Gameover.md)
* [Scene_Title](Scene_Title.md)
* [Scene_Splash](Scene_Splash.md) **@MZ1.8.0**
* [Scene_Message](Scene_Message.md) **@MZ**
    * [Scene_Battle](Scene_Battle.md) (Inheritance position changed)
    * [Scene_Map](Scene_Map.md) (Inheritance position changed)
* [Scene_MenuBase](Scene_MenuBase.md)
    * [Scene_Debug](Scene_Debug.md)
    * [Scene_Equip](Scene_Equip.md)
    * [Scene_GameEnd](Scene_GameEnd.md)
    * [Scene_Menu](Scene_Menu.md)
    * [Scene_Name](Scene_Name.md)
    * [Scene_Options](Scene_Options.md)
    * [Scene_Shop](Scene_Shop.md)
    * [Scene_Status](Scene_Status.md)
    * [Scene_File](Scene_File.md)
        * [Scene_Load](Scene_Load.md)
        * [Scene_Save](Scene_Save.md)
    * [Scene_ItemBase](Scene_ItemBase.md)
        * [Scene_Item](Scene_Item.md)
        * [Scene_Skill](Scene_Skill.md)

---

## Windows

### [Window (Window)](Window.md)

 * [Window_Base](Window_Base.md)
    * [Window_BattleLog](Window_BattleLog.md) (Inheritance position changed)
    * [Window_Help](Window_Help.md)
    * [Window_MapName](Window_MapName.md)
    * [Window_Message](Window_Message.md)
    * [Window_NameBox](Window_NameBox.md) **@MZ**
    * [Window_ScrollText](Window_ScrollText.md)
    * [Window_Scrollable](Window_Scrollable.md) **@MZ**
        * [Window_Selectable](Window_Selectable.md) → [Inheritance](#Selectable_Window_window_selectable) (Inheritance position changed)

---

### [Selectable Window (Window_Selectable)](Window_Selectable.md)

* [Window_BattleEnemy](Window_BattleEnemy.md)
* [Window_DebugEdit](Window_DebugEdit.md)
* [Window_DebugRange](Window_DebugRange.md)
* [Window_Gold](Window_Gold.md) (Inheritance position changed)
* [Window_NameInput](Window_NameInput.md)
* [Window_NumberInput](Window_NumberInput.md)
* [Window_SavefileList](Window_SavefileList.md)
* [Window_ShopBuy](Window_ShopBuy.md)
* [Window_ShopNumber](Window_ShopNumber.md)
* [Window_SkillList](Window_SkillList.md)
    * [Window_BattleSkill](Window_BattleSkill.md)
* [Window_ItemList](Window_ItemList.md) → [Inheritance](#item-display-windowwindow_itemlist)
* [Window_StatusBase](Window_StatusBase.md) **@MZ** → [Inheritance](#status-display-windowwindow_statusbase)
* [Window_Command](Window_Command.md) → [Inheritance](#command-windowwindow_command)

---

### [Item Display Window (Window_ItemList)](Window_ItemList.md)

* [Window_BattleItem](Window_BattleItem.md)
* [Window_EquipItem](Window_EquipItem.md)
* [Window_EventItem](Window_EventItem.md)
* [Window_ShopSell](Window_ShopSell.md)

---

### [Status Display Window (Window_StatusBase)](Window_StatusBase.md)

* [Window_BattleStatus](Window_BattleStatus.md) (Inheritance position changed)
    * [Window_BattleActor](Window_BattleActor.md)
* [Window_EquipSlot](Window_EquipSlot.md) (Inheritance position changed)
* [Window_EquipStatus](Window_EquipStatus.md) (Inheritance position changed)
* [Window_MenuStatus](Window_MenuStatus.md) (Inheritance position changed)
    * [Window_MenuActor](Window_MenuActor.md)
* [Window_NameEdit](Window_NameEdit.md) (Inheritance position changed)
* [Window_ShopStatus](Window_ShopStatus.md) (Inheritance position changed)
* [Window_SkillStatus](Window_SkillStatus.md) (Inheritance position changed)
* [Window_Status](Window_Status.md) (Inheritance position changed)
* [Window_StatusParams](Window_StatusParams.md) **@MZ**
* [Window_StatusEquip](Window_StatusEquip.md) **@MZ**

---

### [Command Window (Window_Command)](Window_Command.md)

* [Window_ActorCommand](Window_ActorCommand.md)
* [Window_ChoiceList](Window_ChoiceList.md)
* [Window_GameEnd](Window_GameEnd.md)
* [Window_MenuCommand](Window_MenuCommand.md)
* [Window_Options](Window_Options.md)
* [Window_PartyCommand](Window_PartyCommand.md)
* [Window_SkillType](Window_SkillType.md)
* [Window_TitleCommand](Window_TitleCommand.md)
* [Window_HorzCommand](Window_HorzCommand.md)
    * [Window_EquipCommand](Window_EquipCommand.md)
    * [Window_ItemCategory](Window_ItemCategory.md)
    * [Window_ShopCommand](Window_ShopCommand.md)

---

## Deprecated MV Classes
`CacheEntry`, `CacheMap`, `ImageCache`, `RequestQueue`, `Decrypter`, `Html5Audio`, `ResourceHandler`, `ToneFilter`, `PIXI.tilemap.ZLayer`, `ShaderTilemap`, `ToneSprite`, `Sprite_Base`
