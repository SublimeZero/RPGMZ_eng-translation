[Class Tree](index.md)

# Class: [RPG](RPG.md).Enemy

## Superclass: [RPG.MetaData](RPG.MetaData.md) 

| Database         | JSON File      | Global Variable                          | Object                     |
|------------------|----------------|-----------------------------------------|----------------------------|
| [Enemy Character] | Enemies.json   | [$dataEnemies](global.md#dataenemies-arrayrpgenemy) (array) | [Game_Enemy](Game_Enemy.md) |

### Properties

| Identifier       | Type                                    | Description                                           |
|------------------|-----------------------------------------|-------------------------------------------------------|
| `battlerName`    | [String](String.md)                    | Image file name (without extension)                   |
| `battlerHue`     | [Number](Number.md)                    | [Hue](0~360)                                         |
| `name`           | [String](String.md)                    | [Name]                                               |
| `id`             | [Number](Number.md)                    | Enemy character ID                                   |
| `params`         | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of values recorded in the order of [Parameter IDs](RPG.Enemy.md#parameter-id) |
| `exp`            | [Number](Number.md)                    | [Experience]                                        |
| `gold`           | [Number](Number.md)                    | [Gold]                                              |
| `dropItems`      | [Array](Array.md).&lt;[RPG.Enemy.DropItem](RPG.Enemy.DropItem.md)&gt; | Array of [Drop Items]                               |
| `actions`        | [Array](Array.md).&lt;[RPG.Enemy.Action](RPG.Enemy.Action.md)&gt; | Array of [Action Patterns]                           |
| `traits`         | [Array](Array.md).&lt;[RPG.Trait](RPG.Trait.md)&gt; | Array of [Traits]                                   |

#### Parameter IDs

| ID | [Parameter]       |
|----|-------------------|
| 0  | Max HP            |
| 1  | Max MP            |
| 2  | Attack Power      |
| 3  | Defense Power     |
| 4  | Magic Power       |
| 5  | Magic Defense     |
| 6  | Agility           |
| 7  | Luck              |

### Inner Classes

* [RPG.Enemy.Action](RPG.Enemy.Action.md)
* [RPG.Enemy.DropItem](RPG.Enemy.DropItem.md)
