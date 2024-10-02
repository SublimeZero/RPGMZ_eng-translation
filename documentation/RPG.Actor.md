[Class Tree](index.md)

# Class: [RPG](RPG.md).Actor

## Superclass: [RPG.MetaData](RPG.MetaData.md)

| Database   | JSON File     | Global Variable                                 | Object                 | Sprite                        |
|------------|----------------|------------------------------------------------|------------------------|-------------------------------|
| [Actor]    | Actors.json    | [$dataActors](global.md#dataactors-arrayrpgactor) (array) | [Game_Actor](Game_Actor.md) | [Sprite_Actor](Sprite_Actor.md) |
| [Player]   | Same           | Same                                           | [Game_Player](Game_Player.md) | [Sprite_Character](Sprite_Character.md) | 
| [Follower] | Same           | Same                                           | [Game_Follower](Game_Follower.md) | Same                           |

Main Access Paths
```js
$dataActors[actorId]
$gameActors.actor(actorId).actor()
```

Related Classes: [Game_Actors](Game_Actors.md), [Game_Followers](Game_Followers.md)

### Properties

| Identifier      | Type                                                 | Description                               |
|-----------------|------------------------------------------------------|-------------------------------------------|
| id              | [Number](Number.md)                                 | Actor ID                                  |
| name            | [String](String.md)                                 | [Name]                                    |
| nickname        | [String](String.md)                                 | [Alias]                                   |
| classId         | [Number](Number.md)                                 | Class ID                                  |
| initialLevel    | [Number](Number.md)                                 | [Initial Level]                           |
| maxLevel        | [Number](Number.md)                                 | [Max Level]                               |
| characterName   | [String](String.md)                                 | Name of the [Walking Character] image file (without extension) |
| characterIndex  | [Number](Number.md)                                 | Number specifying one of the [Walking Character] images divided into 8 parts (0 to 7) |
| faceName        | [String](String.md)                                 | Name of the [Face] image file (without extension) |
| faceIndex       | [Number](Number.md)                                 | Number specifying one of the [Face] images divided into 8 parts (0 to 7) |
| battlerName     | [String](String.md)                                 | Name of the [[SV] Battle Character] image file (without extension) |
| equips          | [Array](Array.md).&lt;[Number](Number.md)&gt;     | [Initial Equipment] (array of equipment item IDs) |
| profile         | [String](String.md)                                 | Sentence of the [Profile]                |
| traits          | [Array](Array.md).&lt;[RPG.Trait](RPG.Trait.md)&gt; | Array of [Traits]                        |

`faceName` and `faceIndex` are used to display face images in [Game_Message](Game_Message.md).
