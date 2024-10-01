[Class Tree](index.md)

# Class: Game_Actors

| Database | JSON Data | Global Variable | Save Data |
| --- | --- | --- | --- |
| [Actors] | [RPG.Actor](RPG.Actor.md) | [$gameActors](global.md#gameactors-game_actors) | Saved |

A class that allows for bulk handling of [Game_Actor](Game_Actor.md). This is the object version of the database's [$dataActors](global.md#dataactors-arrayrpgactor).

Related classes: [Game_Party](Game_Party.md), [Game_Follower](Game_Follower.md)

### new Game_Actors ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_data` | [Array](Array.md).&lt;[Game_Actor](Game_Actor.md)&gt; | Array of actors |


### Methods

#### actor (actorId) → {[Game_Actor](Game_Actor.md)}
Returns the actor with the specified ID.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actorId` | [Number](Number.md) | Actor ID |


#### initialize ()
Initialization upon object creation.
