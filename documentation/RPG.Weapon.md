# Class: [RPG](RPG.md).Weapon

## Superclass: [RPG.EquipItem](RPG.EquipItem.md)

| Database   | JSON File     | Global Variable                               | Object                 |
|------------|----------------|-----------------------------------------------|------------------------|
| [Weapon]   | Weapons.json   | [$dataWeapons](global.md#dataweapons-arrayrpgweapon) (array) | [Game_Item](Game_Item.md) |

The _dataClass property of [Game_Item](Game_Item.md) will be 'weapon'.

Related Class: [RPG.BaseItem](RPG.BaseItem.md)

### Properties

| Identifier    | Type                                      | Description                            |
|---------------|-------------------------------------------|----------------------------------------|
| `wtypeId`     | [Number](Number.md)                      | [Weapon Type ID](RPG.Weapon#weapon-type-id) |
| `animationId` | [Number](Number.md)                      | [[Animation](RPG.Animation.md)] ID     |

#### Weapon Type ID

The ID set in [Database]-[Type]-[Weapon Type].

Registered in the weaponTypes property of [System](RPG.System.md).

The following table shows the default values.

| ID | [Weapon Type] |
|----|----------------|
| 0  | None           |
| 1  | Dagger         |
| 2  | Sword          |
| 3  | Flail          |
| 4  | Axe            |
| 5  | Whip           |
| 6  | Staff          |
| 7  | Bow            |
| 8  | Crossbow       |
| 9  | Gun            |
| 10 | Claw           |
| 11 | Glove          |
| 12 | Spear          |
