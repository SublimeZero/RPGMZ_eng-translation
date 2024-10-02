[Class Tree](index.md)

# Class: [RPG](RPG.md).Map

## Superclass: [RPG.MetaData](RPG.MetaData.md)

| Database  | JSON File   | Global Variable                          | Object           | Sprite Set         |
|-----------|-------------|-----------------------------------------|------------------|--------------------|
| Map       | MapXXX.json | [$dataMap](global.md#datamap-rpgmap) | [Game_Map](Game_Map.md) | [Spriteset_Map](Spriteset_Map.md) |

The XXX in the JSON file is a three-digit number.

`$dataMap` is loaded every time the map is moved and is always replaced with the data of the current map.

Related Classes: [Scene_Map](Scene_Map.md), [RPG.MapInfo](RPG.MapInfo.md)

### Properties

| Identifier       | Type                                         | Description                              |
|-------------------|----------------------------------------------|------------------------------------------|
| `displayName`    | [String](String.md)                          | [Display Name]                           |
| `tilesetId`      | [Number](Number.md)                          | [Tileset] ID                            |
| `width`          | [Number](Number.md)                          | Width of the map (in tiles)             |
| `height`         | [Number](Number.md)                          | Height of the map (in tiles)            |
| `scrollType`     | [Number](Number.md)                          | [[Scroll Type]](RPG.Map.md#スクロールタイプ)  |
| `specifyBattleback` | Boolean                                    | Specify [battle background]              |
| `battleback1Name`| [String](String.md)                          | Filename of the battle background image 1 (ground) |
| `battleback2Name`| [String](String.md)                          | Filename of the battle background image 2 (wall)   |
| `autoplayBgm`    | Boolean                                      | Automatically play [BGM]                |
| `bgm`            | [RPG.AudioFile](RPG.AudioFile.md)          | BGM audio                               |
| `autoplayBgs`    | Boolean                                      | Automatically play [BGS]                |
| `bgs`            | [RPG.AudioFile](RPG.AudioFile.md)          | BGS audio                               |
| `disableDashing` | Boolean                                      | [Disable dashing]?                       |
| `encounterList`  | [Array](Array.md).&lt;[RPG.Map.Encounter](RPG.Map.Encounter.md)&gt; | Array of [encounters]                   |
| `encounterStep`  | [Number](Number.md)                          | [Enemy appearance steps]                 |
| `parallaxName`   | [String](String.md)                          | Filename of the [parallax] image        |
| `parallaxLoopX`  | Boolean                                      | Does the [parallax] [loop horizontally]? |
| `parallaxLoopY`  | Boolean                                      | Does the [parallax] [loop vertically]?   |
| `parallaxSx`     | [Number](Number.md)                          | [Scroll] amount for horizontal parallax  |
| `parallaxSy`     | [Number](Number.md)                          | [Scroll] amount for vertical parallax    |
| `parallaxShow`   | Boolean                                      | Show [parallax] in the editor?          |
| `data`           | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of [tile IDs](Tilemap.md#tile-ids) for [map data](RPG.Map.md#map-data) |
| `events`         | [Array](Array.md).&lt;[RPG.Event](RPG.Event.md)&gt; | Array of [event] data                   |

#### [Scroll Type]

| Number | [Scroll Type]                 |
|--------|-------------------------------|
| 0      | Does not loop                 |
| 1      | Loops vertically              |
| 2      | Loops horizontally             |
| 3      | Loops both vertically and horizontally |

#### Map Data
The data property is a one-dimensional array and can be accessed in the form of `<code>data[x + (y + z*h)*w]</code>`.  
x: x-coordinate, y: y-coordinate, w: map width, h: map height, z: map layer

##### z: Map Layer

| z | Description                 |
|---|-----------------------------|
| 5 | Region                      |
| 4 | Shadow Pen                  |
| 3 | B-E Tiles                   |
| 2 | B-E Tiles                   |
| 1 | A2 Right Tiles              |
| 0 | A Tiles                     |

### Inner Classes

* [RPG.Map.Encounter](RPG.Map.Encounter.md)
