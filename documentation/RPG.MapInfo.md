[Class Tree](index.md)

# Class: [RPG](RPG.md).MapInfo

| Database       | JSON File      | Global Variable                          |
|----------------|----------------|-----------------------------------------|
| Map List       | MapInfos.json  | [$dataMapInfos](global.md#datamapInfos-arrayrpgmapInfo) (array) |

The information included is for the editor.

Changes were made in v1.7.0.

Related Class: [RPG.Map](RPG.Map.md)

### Properties

| Identifier       | Type                                         | Description                             |
|-------------------|----------------------------------------------|-----------------------------------------|
| `id`              | [Number](Number.md)                          | [ID] (probably unused)                 |
| `name`            | [String](String.md)                          | [Name]                                  |
| `parentId`       | [Number](Number.md)                          | Parent map ID                           |
| `order`           | [Number](Number.md)                          | Display order in the editor             |
| `expanded`       | Boolean                                      | Is the list expanded in the editor?    |
| `scrollX`        | [Number](Number.md)                          | X position when opened in the editor    |
| `scrollY`        | [Number](Number.md)                          | Y position when opened in the editor    |
| `quick`          | Boolean                                      | **@MZ1.7.0** Is it in quick access?     |

*Note: The `id` is implemented as an array index and does not seem to be used. Therefore, if the null entries in MapInfos.json are removed or the array index changes, the IDs will become misaligned.*
