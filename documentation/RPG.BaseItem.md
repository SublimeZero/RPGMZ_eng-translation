[Class Tree](index.md)

# Class: [RPG](RPG.md).BaseItem

## Superclass: [RPG.MetaData](RPG.MetaData.md)

The base class used for [items], as well as [weapons], [armor], [enemies], and [states].

Related Class: [DataManager](DataManager.md)

### Subclasses

* [RPG.UsableItem](RPG.UsableItem.md)
* [RPG.EquipItem](RPG.EquipItem.md)

### Properties

| Identifier   | Type                                    | Description                  |
|--------------|-----------------------------------------|------------------------------|
| `id`         | [Number](Number.md)                    | [Item ID](RPG.BaseItem.md#item-id) |
| `name`       | [String](String.md)                    | [Name]                       |
| `iconIndex`  | [Number](Number.md)                    | [Icon] number                |
| `description`| [String](String.md)                    | [Description] text           |

#### Item ID

The number in the [database] - [items].
