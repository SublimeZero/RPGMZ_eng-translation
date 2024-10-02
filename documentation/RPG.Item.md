[Class Tree](index.md)

# Class: [RPG](RPG.md).Item

## Superclass: [RPG.UsableItem](RPG.UsableItem.md)

| Database    | JSON File    | Global Variable | Object               |
|-------------|---------------|------------------|----------------------|
| [Items]     | Items.json   | [$dataItems](global.md#dataitems-arrayrpgitem) (Array) | [Game_Item](Game_Item.md) |

The _dataClass property of [Game_Item](Game_Item.md) will be 'item'.

### Properties

| Identifier       | Type                                         | Description                                  |
|-------------------|----------------------------------------------|----------------------------------------------|
| `itypeId`        | [Number](Number.md)                          | [Item Type ID](RPG.Item.md#item-type-id)   |
| `price`          | [Number](Number.md)                          | [Price]                                     |
| `consumable`     | Boolean                                      | Indicates if it is [consumable]             |

#### Item Type ID

| ID | [Item Type]      |
|----|-------------------|
| 1  | Normal Item       |
| 2  | Important Item    |
| 3  | Hidden Item A     |
| 4  | Hidden Item B     |
