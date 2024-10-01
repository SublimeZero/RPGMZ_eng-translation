[Class Tree](index.md)

# Class: Game_Interpreter

A class that executes event commands written in [execution content].

When executing the [script] of event commands, the instance of this object becomes `this`, making it somewhat convenient to add extended commands as methods.

Depending on the execution location and whether the [[trigger]](RPG.EventPage.md#トリガー) is [parallel execution], the object holding the Game_Interpreter can be one of the following:<br />
[Game_Troop](Game_Troop.md), [Game_Map](Game_Map.md), [Game_CommonEvent](Game_CommonEvent.md), [Game_Event](Game_Event.md), [Game_Interpreter](Game_Interpreter.md)

Changes were made in versions 1.1.1, 1.2.0, 1.3.2, 1.4.0, and 1.5.0.

Related Classes: [RPG.EventPage](RPG.EventPage.md), [Game_Character](Game_Character.md), [Game_Message](Game_Message.md), [ImageManager](ImageManager.md)

### new Game_Interpreter (depth)
#### Parameters

| Name   | Type     | Description                                  |
| ------ | -------- | -------------------------------------------- |
| `depth`| [Number](Number.md) | Generation (default: 0) depth of how many times called as a child |

### Properties

| Identifier  | Type     | Description                             |
| ----------- | -------- | --------------------------------------- |
| `_depth`    | [Number](Number.md) | Generation                             |
| `_branch`   | Object   | Status of branching processing by indent |
| `_indent`   | [Number](Number.md) | Depth of indent                       |
| `_frameCount` | [Number](Number.md) | Frame count (not the current frame, used for freeze checks) The current frame is [Graphics.frameCount](Graphics.md) |
| `_freezeChecker` | [Number](Number.md) | Counter for freeze checking           |
| `_mapId`    | [Number](Number.md) | Map ID where the command exists      |
| `_eventId`  | [Number](Number.md) | Event ID where the command exists    |
| `_list`     | [Array](Array.md).&lt;[RPG.EventCommand](RPG.EventCommand.md)&gt; | List of commands                      |
| `_index`    | [Number](Number.md) | Index of the currently processing command |
| `_waitCount` | [Number](Number.md) | Counter for [wait]                   |
| `_waitMode` | [String](String.md) | [Wait mode](Game_Interpreter#ウエイトモード) |
| `_comments` | [Array](Array.md) | Temporary storage for comment lines   |
| `_characterId` | [Number](Number.md) | **@MZ** Target event ID for commands  |
| `_childInterpreter` | [Game_Interpreter](Game_Interpreter.md) | Child interpreter                     |

#### Wait Modes

| String   | Description                               |
| -------- | ----------------------------------------- |
| "message" | Waits until the message ends             |
| "transfer" | Waits until the transition effect ends   |
| "scroll" | Waits until the scroll ends               |
| "route" | Waits until the movement ends             |
| "animation" | Waits until the animation ends           |
| "balloon" | Waits until the balloon ends              |
| "gather" | Waits until the followers have gathered   |
| "action" | Waits until the action ends               |
| "video" | Waits until the video ends                 |
| "image" | Waits until the image display ends        |

### Deprecated MV Properties
`_character`, `_params`

### Methods
The commandXxx methods corresponding to event commands are separated into [another file](Game_Interpreter_command.md).<br />
However, they simply list the commands, so for detailed information, please refer to Toriyakan's 
[RPG Maker MZ Script Reference](https://docs.google.com/spreadsheets/d/1aqY-xzFqT0vnZE-OkfsMYsP9Ud91vWTrBLU-uDkJ-Ls/edit#gid=2095105278).

#### changeHp (target, value, allowDeath)
Increases or decreases [HP] by a specified value.

##### Parameters

| Name         | Type     | Description                        |
| ------------ | -------- | ---------------------------------- |
| `target`     | [Game_Battler](Game_Battler.md) | Target actor or enemy            |
| `value`      | [Number](Number.md) | Amount of HP to change           |
| `allowDeath` | Boolean  | Whether to apply even if dead     |

#### character (param) → {[Game_Character](Game_Character.md)}
Returns the [Game_Event](Game_Event.md) with the specified ID.<br />
Returns itself (the event containing the command) if 0.
Returns [Game_Player](Game_Player.md) if a negative value.<br />
To get the [follower] objects, use [Game_Followers.follower()](Game_Followers.md#follower-index--game_follower).

##### Parameters

| Name   | Type     | Description   |
| ------ | -------- | ------------- |
| `param`| [Number](Number.md) | Event ID     |

#### checkFreeze () → {Boolean}
Checks if the interpreter is frozen.

#### checkOverflow ()
Checks if there is an overflow.

#### clear ()
Clears the state of the interpreter.

#### currentCommand () → {[RPG.EventCommand](RPG.EventCommand.md)}
Returns the command that is currently being processed.

#### eventId () → {[Number](Number.md)}
Returns the event ID of the command caller.

#### executeCommand () → {Boolean}
Executes the command being processed and returns the result.

#### fadeSpeed () → {[Number](Number.md)}
Returns the fade speed.

Reference: [command221](Game_Interpreter.md#command221---boolean), [command222](Game_Interpreter.md#command222---boolean)

#### gameDataOperand (type, param1, param2) → {[Number](Number.md)}
Returns the specified game data.

The meanings of `param1` and `param2` change depending on `type`. For example, if `type` is 7, then `param1` means: 
0: Map ID, 1: Party Members, 2: Gold, 3: Steps, 4: Play Time, 5: Timer, 6: Save Count, 7: Battle Count, 8: Win Count, 9: Escape Count.

Since this is a method for command execution, it’s better to use `$gameSystem.playtime()` rather than writing `this.gameDataOperand(7, 4)` if you want specific data.

##### Parameters

| Name   | Type     | Description                            |
| ------ | -------- | -------------------------------------- |
| `type` | [Number](Number.md) | 0: Item, 1: Weapon, 2: Armor, 3: Actor, 4: Enemy, 5: Character, 6: Party, 7: Other |
| `param1` | [Number](Number.md) | Meaning differs based on type      |
| `param2` | [Number](Number.md) | Meaning differs based on type      |

#### initialize ()
Initialization during object creation.

#### isRunning () → {Boolean}
Checks if the interpreter is running.

#### iterateActorEx (param1, param2, callback)
Performs iterative processing on actors.

##### Parameters

| Name   | Type     | Description                           |
| ------ | -------- | ------------------------------------- |
| `param1` | [Number](Number.md) | 0: Direct ID specification, otherwise variable specification |
| `param2` | [Number](Number.md) | If `param1` is 0, the actor ID; otherwise the index of the variable containing the ID |
| `callback` | function | Callback function                     |

#### iterateActorId (param, callback)
Performs iterative processing on actors.

##### Parameters

| Name   | Type     | Description                             |
| ------ | -------- | --------------------------------------- |
| `param` | [Number](Number.md) | ID of the actor to apply (0: all)   |
| `callback` | function | Callback function                      |

#### iterateActorIndex (param, callback)
Performs iterative processing on actors.

##### Parameters

| Name   | Type     | Description                            |
| ------ | -------- | -------------------------------------- |
| `param` | [Number](Number.md) | Index of the actor in the party (0: all) |
| `callback` | function | Callback function                      |

#### iterateBattler (param1, param2, callback)
Performs iterative processing on battlers.

##### Parameters

| Name   | Type     | Description                          |
| ------ | -------- | ------------------------------------ |
| `param1` | [Number](Number.md) | 0: Enemy                            |
| `param2` | [Number](Number.md) | Number of the battler to apply (0: all) |
| `callback` | function | Callback function                    |

#### iterateEnemyIndex (param, callback)
Performs iterative processing on enemies.

##### Parameters

| Name   | Type     | Description                           |
| ------ | -------- | ------------------------------------- |
| `param` | [Number](Number.md) | Number of the enemy to apply (0: all) |
| `callback` | function | Callback function                     |

#### jumpTo (index)
Moves the processing target to the specified index.

##### Parameters

| Name   | Type     | Description                          |
| ------ | -------- | ------------------------------------ |
| `index` | [Number](Number.md) | Command index                     |

#### loadImages ()
Preloads images for use in **@MZ** commands.

#### nextEventCode () → {[Number](Number.md)}
Returns the next event code (the XXX part of commandXXX).

#### operateValue (operation, operandType, operand) → {[Number](Number.md)}
Performs calculation with a sign and returns the result.

##### Parameters

| Name   | Type     | Description                             |
| ------ | -------- | --------------------------------------- |
| `operation` | [Number](Number.md) | 0: Plus, others are minus          |
| `operandType` | [Number](Number.md) | 0: Direct value, otherwise: variable |
| `operand` | [Number](Number.md) | If `operandType` is 0: value, otherwise: variable ID |

#### operateVariable (variableId, operationType, value)
Performs calculations with values and returns the result.

##### Parameters

| Name   | Type     | Description                             |
| ------ | -------- | --------------------------------------- |
| `variableId` | [Number](Number.md) | Variable ID                        |
| `operationType` | [Number](Number.md) | Operator type (0: =, 1: +, 2: -, 3: ×, 4: ÷, 5: %) |
| `value` | [Number](Number.md) | Value                                |

#### picturePoint (params)→ {[Point](Point.md)}
Returns the display position of the image for **@MZ** command232 [2] - [Picture] - [Move Picture...].

##### Parameters

| Name   | Type     | Description                      |
| ------ | -------- | -------------------------------- |
| `params` | [Array](Array.md).&lt;[String](String.md)&gt; | Same as the arguments of command232 |

#### pluginCommand (command, args)
Method for receiving plugin commands.<br />
This method allows you to add processing specific to each plugin. A style like Example is typical.

It is kept for compatibility with "RPG Maker MV," but is not usually used.<br />
In "RPG Maker MZ," you should use [PluginManager.registerCommand()](PluginManager.md#static-registercommand-pluginname-commandname-func).

##### Parameters

| Name   | Type     | Description                             |
| ------ | -------- | --------------------------------------- |
| `command` | [String](String.md) | Command name                        |
| `args` | [Array](Array.md).&lt;[String](String.md)&gt; | Array of arguments                  |

##### Example
```js
const _Game_Interpreter_pluginCommand = Game_Interpreter.prototype.pluginCommand;

Game_Interpreter.prototype.pluginCommand = function (command, args) {
   _Game_Interpreter_pluginCommand.call(this, command, args);
   // Write the command name checks and execution details for each plugin here
};
```

#### setup (list, eventId opt)
Prepares the interpreter.

##### Arguments

| Name      | Type                                       | Characteristics  | Description               |
|-----------|--------------------------------------------|-------------------|---------------------------|
| `list`    | [Array](Array.md).&lt;[RPG.EventCommand](RPG.EventCommand.md)&gt; |                   | List of commands          |
| `eventId` | [Number](Number.md)                       | &lt;optional&gt;  | Event ID (default: 0)     |


#### setupChild (list, eventId)
Prepares the child interpreter for [common events].

Reference: [command117](Game_Interpreter.md#command117---boolean)

##### Arguments

| Name      | Type                                       | Description               |
|-----------|--------------------------------------------|---------------------------|
| `list`    | [Array](Array.md).&lt;[RPG.EventCommand](RPG.EventCommand.md)&gt; | List of commands          |
| `eventId` | [Number](Number.md)                       | Event ID                  |


#### setupChoices (params)
Prepares the choice window.

##### Arguments

| Name      | Type                                       | Description               |
|-----------|--------------------------------------------|---------------------------|
| `params`  | [Array](Array.md).&lt;*&gt;               | Settings for the choice window |


#### setupItemChoice (params)
Prepares the item selection window.

##### Arguments

| Name      | Type                                       | Description               |
|-----------|--------------------------------------------|---------------------------|
| `params`  | [Array](Array.md).&lt;[Number](Number.md)&gt; | Settings for the item selection window |


#### setupNumInput (params)
Prepares the numeric input window.

##### Arguments

| Name      | Type                                       | Description               |
|-----------|--------------------------------------------|---------------------------|
| `params`  | [Array](Array.md).&lt;[Number](Number.md)&gt; | Settings for the numeric input window |


#### setupReservedCommonEvent () → {Boolean}
Prepares the common event if it was saved and returns whether it was saved.


#### setWaitMode (waitMode)
Sets the wait mode.

##### Arguments

| Name      | Type                                       | Description               |
|-----------|--------------------------------------------|---------------------------|
| `waitMode`| [String](String.md)                       | [Wait mode](Game_Interpreter.md#ウエイトモード) |


#### skipBranch ()
Skips the branching (indented part) based on conditions.


#### terminate ()
Performs termination processing.


#### update ()
Updates every frame.


#### updateChild () → {Boolean}
Updates the child interpreter.


#### updateWait () → {Boolean}
Updates the wait state.


#### updateWaitCount () → {Boolean}
Updates the wait count.


#### updateWaitMode () → {Boolean}
Updates the [wait mode](Game_Interpreter#wait-mode) and checks whether it is in a waiting state.


#### videoFileExt () → {[String](String.md)}
Returns the video file extension ".webm" or ".mp4".


#### wait (duration)
Pauses the interpreter's execution for a specified number of frames.

##### Arguments

| Name      | Type                                       | Description               |
|-----------|--------------------------------------------|---------------------------|
| `duration`| [Number](Number.md)                       | Number of frames          |



### Deprecated MV Methods
`requestImages (list, commonList opt)`
