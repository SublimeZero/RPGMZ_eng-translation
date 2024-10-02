[Class Tree](index.md)

# Class: [RPG](RPG.md).Tileset

## Superclass: [RPG.MetaData](RPG.MetaData.md)

| Database     | JSON File    | Global Variable                                         |
|--------------|---------------|--------------------------------------------------------|
| [Tileset]    | Tilesets.json | [$dataTilesets](global.md#datatilesets-arrayrpgtileset) (array) |

Related Classes: [Game_Map](Game_Map.md), [Tilemap](Tilemap.md)

### Properties

| Identifier                  | Type                                           | Description                             |
|-----------------------------|------------------------------------------------|-----------------------------------------|
| `id`                        | [Number](Number.md) | Tileset ID                             |
| `name`                      | [String](String.md) | [Name]                                 |
| `mode`                      | [Number](Number.md) | [[Mode]](RPG.Tileset.md#mode)         |
| `tilesetNames`             | [Array](Array.md).&lt;[String](String.md)&gt; | Array of image file names used in the tileset<br />(0: A1, 1: A2, 2: A3, 3: A4, 4: A5, 5: B, 6: C, 7: D, 8: E) |
| `flags`                     | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of [Bit Flags](RPG.Tileset.md#bit-flags), indexed by [Tile ID](Tilemap.md#tile-id) |

#### [Mode]
Although it's referred to as VX compatible type, it is not used.

| Number | Description       |
|--------|-------------------|
| 0      | Field type        |
| 1      | Area type         |
| 2      | VX compatible type |

#### Bit Flags
Bit positions of flags that record the properties of tiles.

| Bit    | Description            |
|--------|------------------------|
| 0x0001 | Cannot pass below      |
| 0x0002 | Cannot pass left       |
| 0x0004 | Cannot pass right      |
| 0x0008 | Cannot pass above      |
| 0x0010 | Displayed on higher level [☆] |
| 0x0020 | Ladder                 |
| 0x0040 | Bush                   |
| 0x0080 | Counter                |
| 0x0100 | Damage floor           |
| 0x0200 | Cannot pass with small boat |
| 0x0400 | Cannot pass with large boat |
| 0x0800 | Cannot land with airship |
| 0xF000 | Terrain tag            |
