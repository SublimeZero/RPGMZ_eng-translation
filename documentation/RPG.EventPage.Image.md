[Class Tree](index.md)

# Class: [RPG](RPG.md).[EventPage](RPG.EventPage.md).Image
JSON data that constitutes the [image] of the event's [EV page].

Included in the image property of [RPG.EventPage](RPG.EventPage.md).

### Properties

| Identifier           | Type               | Description                                  |
|---------------------|--------------------|----------------------------------------------|
| `tileId`            | [Number](Number.md) | [Tile ID](Tilemap.md#tile-id) (0: not a tile) |
| `characterName`     | [String](String.md) | Image file name (excluding .png in the characters folder) |
| `characterIndex`    | [Number](Number.md) | Character number in the file (0 to 7)       |
| `direction`         | [Number](Number.md) | Character's direction (2: down, 4: left, 6: right, 8: up) |
| `pattern`           | [Number](Number.md) | Character's animation pattern (0, 1, 2)      |
