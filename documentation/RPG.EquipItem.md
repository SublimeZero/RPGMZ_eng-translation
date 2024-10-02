[Class Tree](index.md)

# Class: [RPG](RPG.md).EquipItem

## Superclass: [RPG.BaseItem](RPG.BaseItem.md)

### Subclasses

* [RPG.Armor](RPG.Armor.md)
* [RPG.Weapon](RPG.Weapon.md)

### Properties

| Identifier       | Type                                    | Description                                           |
|------------------|-----------------------------------------|-------------------------------------------------------|
| `price`          | [Number](Number.md)                    | [Price]                                             |
| `etypeId`        | [Number](Number.md)                    | [Equipment Type ID](RPG.EquipItem.md#equipment-type-id) |
| `params`         | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of [Parameter Changes] in the order of [Parameter IDs](RPG.Enemy.md#parameter-id) |
| `traits`         | [Array](Array.md).&lt;[RPG.Trait](RPG.Trait.md)&gt; | Array of [Traits]                                   |

#### Equipment Type ID

The ID set in the [Database]-[Type]-[Equipment Type].

Registered in the equipTypes property of [System](RPG.System.md).

The following table shows the default values.

| ID | [Equipment Type] |
|----|-------------------|
| 0  | None              |
| 1  | Shield            |
| 2  | Head              |
| 3  | Body              |
| 4  | Accessory         |
