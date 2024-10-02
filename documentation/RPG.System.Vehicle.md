[Class Tree](index.md)

# Class: [RPG](RPG.md).[System](RPG.System.md).Vehicle

| Database       | JSON File    | Object                    | Sprite                     |
|----------------|---------------|---------------------------|----------------------------|
| [Vehicle]      | System.json   | [Game_Vehicle](Game_Vehicle.md) | [Sprite_Character](Sprite_Character.md) |

JSON data for [Vehicles](#).

The image specification is structured similarly to that of [RPG.Actor](RPG.Actor.md).

Main Path
```js
$dataSystem.boat;
$dataSystem.ship;
$dataSystem.airship;
```

Related Classes: [Game_Map](Game_Map.md), [Game_Player](Game_Player.md)

### Properties

| Identifier            | Type                               | Description                                |
|-----------------------|------------------------------------|--------------------------------------------|
| `characterName`       | [String](String.md)               | Image file name (excluding the extension) |
| `characterIndex`      | [Number](Number.md)               | Image number (0 to 7)                      |
| `bgm`                 | [RPG.AudioFile](RPG.AudioFile.md) | BGM                                        |
| `startMapId`          | [Number](Number.md)               | [Initial Position] Map ID                  |
| `startX`              | [Number](Number.md)               | [Initial Position] x-coordinate (tiles)    |
| `startY`              | [Number](Number.md)               | [Initial Position] y-coordinate (tiles)    |
