[Class Tree](index.md)

# Class: [RPG](RPG.md).MetaData
Data for [notes] included in many data types.

The conversion from note to meta is done using the [DataManager.extractMetadata](DataManager.md#static-extractmetadata-data) method.<br />
Data recorded in the meta property is used as parameters for plugins.

### Subclasses

* [RPG.Actor](RPG.Actor.md)
* [RPG.Class](RPG.Class.md)
* [RPG.Enemy](RPG.Enemy.md)
* [RPG.Event](RPG.Event.md)
* [RPG.BaseItem](RPG.BaseItem.md)
* [RPG.Map](RPG.Map.md)
* [RPG.State](RPG.State.md)
* [RPG.Tileset](RPG.Tileset.md)

### Properties

| Identifier | Type      | Description                      |
|------------|-----------|----------------------------------|
| `note`     | [String](String.md) | Contents of the [note]      |
| `meta`     | Object    | Result of parsing data in the format <name:value> from note |

#### Format of meta

Write in the note in the form of <name:value> or <name>.<br />
For <name:value>, the value returned is a String.<br />
For <name>, the value returned is a Boolean `true`.

To extract values from a variable `e` that contains RPG.MetaData:<br />
Use <code>e.name</code> or <code>e['name']</code>.

The standard processing method is to extract the value of meta in the initialization method (initialize) of each object and save it in the object's variables.
