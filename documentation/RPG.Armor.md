[Class Tree](index.md)

# Class: [RPG](RPG.md).Armor

## Superclass: [RPG.EquipItem](RPG.EquipItem.md)

| Database   | JSON File  | Global Variable                                      | Object                        |
|------------|-------------|------------------------------------------------------|-------------------------------|
| [Armor]    | Armors.json | [$dataArmors](global.md#dataarmors-arrayrpgarmor)(array) | [Game_Item](Game_Item.md)     |

The `_dataClass` property of [Game_Item](Game_Item.md) will be set to 'armor'.

### Properties

| Identifier  | Type                                         | Description                            |
|-------------|----------------------------------------------|----------------------------------------|
| `atypeId`   | [Number](Number.md)                         | [Armor Type ID](RPG.Armor.md#armor-type-id) |

#### Armor Type ID

The ID set in [Database]-[Type]-[Armor Type].

It is registered in the `armorTypes` property of [System](RPG.System.md).

The table below shows the default values.

| ID | [Armor Type]   |
|----|-----------------|
| 1  | General Armor   |
| 2  | Magical Armor   |
| 3  | Light Armor     |
| 4  | Heavy Armor     |
| 5  | Small Shield    |
| 6  | Large Shield    |
