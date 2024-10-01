[Class Tree](index.md)

# Class: Game_Item

| Database | JSON Data |
| --- | --- |
| [Item][Weapon][Armor][Skill] | [RPG.BaseItem](RPG.BaseItem.md)  |

A class that handles items and skills in general.

Related Classes: [RPG.UsableItem](RPG.UsableItem.md), [RPG.Item](RPG.Item.md), [RPG.Skill](RPG.Skill.md), [RPG.EquipItem](RPG.EquipItem.md), [RPG.Weapon](RPG.Weapon.md), [RPG.Armor](RPG.Armor.md), [Game_Actor](Game_Actor.md), [Game_Action](Game_Action.md)

### new Game_Item ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_dataClass` | [String](String.md) | Type of item ('item', 'skill', 'weapon', 'armor', '') |
| `_itemId` | [Number](Number.md) | Item ID (varies by type) |

### Methods

#### initialize ()
 Initializes upon object creation.

#### isArmor () → {Boolean}
 Checks if it is armor.

#### isEquipItem () → {Boolean}
 Checks if it is an equipment item.

#### isItem () → {Boolean}
 Checks if it is an item.

#### isNull () → {Boolean}
 Checks if it is unset.

#### isSkill () → {Boolean}
 Checks if it is a skill.

#### isUsableItem () → {Boolean}
 Checks if it is a usable item.

#### isWeapon () → {Boolean}
 Checks if it is a weapon.

#### itemId () → {[Number](Number.md)}
 Returns the item ID.

#### object () → {[RPG.BaseItem](RPG.BaseItem.md)}
 Returns the JSON data.

#### setEquip (isWeapon, itemId)
 Sets the equipment with the specified item.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `isWeapon` | Boolean | Is it a weapon? |
| `itemId` | [Number](Number.md) | Item ID |

#### setObject (item)
 Overwrites with the specified JSON data.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `item` | [RPG.BaseItem](RPG.BaseItem.md) | Item |
