[Class Tree](index.md)

# Class: [RPG](RPG.md).Event

## Superclass: [RPG.MetaData](RPG.MetaData.md)

| Database    | Object          | Sprite                 |
|-------------|------------------|------------------------|
| [Event]     | [Game_Event](Game_Event.md) | [Sprite_Character](Sprite_Character.md) |

JSON data that constitutes map [events].

Included in the events property of [RPG.Map](RPG.Map.md) and can also be obtained through the [Game_Event.event()](Game_Event.md#event---rpgevent) method.

Main paths:
```js
$dataMap.events[eventId]
$gameMap.event(eventId).event()
```

Related classes: [RPG.CommonEvent](RPG.CommonEvent.md), [RPG.Troop](RPG.Troop.md)

### Properties

| Identifier | Type                                    | Description               |
|------------|-----------------------------------------|---------------------------|
| id         | [Number](Number.md)                    | Event ID                  |
| name       | [String](String.md)                    | Event Name                |
| x          | [Number](Number.md)                    | X-coordinate (tiles)      |
| y          | [Number](Number.md)                    | Y-coordinate (tiles)      |
| pages      | [Array](Array.md).&lt;[RPG.EventPage](RPG.EventPage.md)&gt; | Array of [Event Pages]    |
