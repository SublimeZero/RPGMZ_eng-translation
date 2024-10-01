[Class Tree](index.md)

# Class: Game_Timer

| Event Command | Global Variables | Save Data | Sprite |
| --- | --- | --- | --- |
| [Timer Operations] | [$gameTimer](global.md#gametimer-game_timer) | Saved | [Sprite_Timer](Sprite_Timer.md) |

Changes were made in v1.4.0.

Related Classes: [Scene_Map](Scene_Map.md), [Scene_Battle](Scene_Battle.md)

### new Game_Timer ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_frames` | [Number](Number.md) | Remaining time (in frames) |
| `_working` | Boolean | Is it working? |


### Methods

#### frames () → {[Number](Number.md)}
**@MZ 1.4.0** Returns the remaining time (in frames).

#### initialize ()
Initialization when creating the object.


#### isWorking () → {Boolean}
Is the timer working?


#### onExpire ()
Handler called when the timer completes.


#### seconds () → {[Number](Number.md)}
Returns the remaining time (in seconds).


#### start (count)
Starts the timer with the specified count.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `count` | [Number](Number.md) | Count time (in frames) |


#### stop ()
Stops the timer.


#### update (sceneActive)
Updates every frame.<br />
However, it does not update if the scene is active.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sceneActive` | Boolean | Is the scene active? |
