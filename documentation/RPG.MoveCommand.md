[Class Tree](index.md)

# Class: [RPG](RPG.md).MoveCommand
JSON data that constitutes [Move Commands].

Included as an array in the list of [RPG.MoveRoute](RPG.MoveRoute.md).

### Properties

| Identifier  | Type                                     | Description                       |
|-------------|------------------------------------------|-----------------------------------|
| `code`      | [Number](Number.md)                     | [Command code number](#command-code-number) |
| `parameters`| [Array](Array.md).&lt;[String](String.md)&gt; | Required arguments for each command |

#### Command Code Numbers
Constants are defined in the properties of [Game_Character](Game_Character.md), so when actually using them, write as <code>Game_Character.ROUTE_END</code>.

Additionally, **bold** and <u>underlined</u> highlights are personal notes like "this is commonly used," and they don't have any specific grammatical meaning.

| code | Constant                       | [Move Command]      |
|------|-------------------------------|----------------------|
| 0    | `ROUTE_END`                   | End                   |
| 1    | `ROUTE_MOVE_DOWN`             | <u>**Move Down**</u> |
| 2    | `ROUTE_MOVE_LEFT`             | <u>**Move Left**</u> |
| 3    | `ROUTE_MOVE_RIGHT`            | <u>**Move Right**</u>|
| 4    | `ROUTE_MOVE_UP`               | <u>**Move Up**</u>   |
| 5    | `ROUTE_MOVE_LOWER_L`          | Move Lower Left       |
| 6    | `ROUTE_MOVE_LOWER_R`          | Move Lower Right      |
| 7    | `ROUTE_MOVE_UPPER_L`          | Move Upper Left       |
| 8    | `ROUTE_MOVE_UPPER_R`          | Move Upper Right      |
| 9    | `ROUTE_MOVE_RANDOM`           | Move Randomly         |
| 10   | `ROUTE_MOVE_TOWARD`           | Move Toward Player    |
| 11   | `ROUTE_MOVE_AWAY`             | Move Away from Player |
| 12   | `ROUTE_MOVE_FORWARD`          | Move Forward One Step |
| 13   | `ROUTE_MOVE_BACKWARD`         | Move Backward One Step|
| 14   | `ROUTE_JUMP`                  | <u>Jump…</u>         |
| 15   | `ROUTE_WAIT`                  | **Wait…**            |
| 16   | `ROUTE_TURN_DOWN`             | <u>Face Down</u> (Set direction of teleport event) |
| 17   | `ROUTE_TURN_LEFT`             | <u>Face Left</u> (Set direction of teleport event) |
| 18   | `ROUTE_TURN_RIGHT`            | <u>Face Right</u> (Set direction of teleport event) |
| 19   | `ROUTE_TURN_UP`               | <u>Face Up</u> (Set direction of teleport event) |
| 20   | `ROUTE_TURN_90D_R`            | Turn Right 90 Degrees  |
| 21   | `ROUTE_TURN_90D_L`            | Turn Left 90 Degrees   |
| 22   | `ROUTE_TURN_180D`             | Turn 180 Degrees       |
| 23   | `ROUTE_TURN_90D_R_L`          | Turn Right or Left 90 Degrees |
| 24   | `ROUTE_TURN_RANDOM`           | Turn Randomly          |
| 25   | `ROUTE_TURN_TOWARD`           | Face Player            |
| 26   | `ROUTE_TURN_AWAY`             | Face Away from Player  |
| 27   | `ROUTE_SWITCH_ON`             | <u>Switch ON…</u>     |
| 28   | `ROUTE_SWITCH_OFF`            | <u>Switch OFF…</u>    |
| 29   | `ROUTE_CHANGE_SPEED`          | **Change Move Speed…** (EV settings: Autonomous movement) |
| 30   | `ROUTE_CHANGE_FREQ`           | Change Move Frequency… (EV settings) |
| 31   | `ROUTE_WALK_ANIME_ON`         | Walking Animation ON (EV settings: Options) |
| 32   | `ROUTE_WALK_ANIME_OFF`        | Walking Animation OFF (EV settings) |
| 33   | `ROUTE_STEP_ANIME_ON`         | Step Animation ON (EV settings) |
| 34   | `ROUTE_STEP_ANIME_OFF`        | Step Animation OFF (EV settings) |
| 35   | `ROUTE_DIR_FIX_ON`            | Direction Fix ON (EV settings) |
| 36   | `ROUTE_DIR_FIX_OFF`           | Direction Fix OFF (EV settings) |
| 37   | `ROUTE_THROUGH_ON`            | Pass Through ON (EV settings) |
| 38   | `ROUTE_THROUGH_OFF`           | Pass Through OFF (EV settings) |
| 39   | `ROUTE_TRANSPARENT_ON`        | Transparency ON        |
| 40   | `ROUTE_TRANSPARENT_OFF`       | Transparency OFF       |
| 41   | `ROUTE_CHANGE_IMAGE`          | <u>Change Image…</u> (EV settings: Image | Change Actor Image…) |
| 42   | `ROUTE_CHANGE_OPACITY`        | Change Opacity…       |
| 43   | `ROUTE_CHANGE_BLEND_MODE`     | Change Blend Mode…    |
| 44   | `ROUTE_PLAY_SE`               | <u>Play SE…</u>       |
| 45   | `ROUTE_SCRIPT`                | <u>Script…</u>        |
