[Class Tree](index.md)

# Class: Game_CommonEvent

| Database | JSON Data |
| --- | --- |
| [Common Event] | [RPG.CommonEvent](RPG.CommonEvent.md) |

Main path
```js
$gameMap._commonEvents[n]
```

Related Class: [Game_Map](Game_Map.md)

### new Game_CommonEvent ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_commonEventId` | [Number](Number.md) | Common event ID |
| `_interpreter` | [Game_Interpreter](Game_Interpreter.md) | Command interpreter |

### Methods

#### event () → {[RPG.CommonEvent](RPG.CommonEvent.md)}
Returns the JSON definition data.

#### initialize ()
Initialization upon object creation.

#### isActive () → {Boolean}
Checks if this [common event] is active.

#### list () → {[Array](Array.md).&lt;[RPG.EventCommand](RPG.EventCommand.md)&gt;}
Returns an array of [event commands].

#### refresh ()
Reupdates the [common event].

#### update ()
Updates every frame.
