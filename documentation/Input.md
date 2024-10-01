[Class Tree](index.md)

# Class: Input
A static class for handling keyboard and gamepad (controller) input.

Handles JavaScript's [KeyboardEvent](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent) and [Gamepad](https://developer.mozilla.org/en-US/docs/Web/API/Gamepad).

Related classes: [Window_Selectable](Window_Selectable.md), [TouchInput](TouchInput.md)


### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `keyRepeatWait` | [Number](Number.md) | [static] Wait time until key repeat (frames) |
| `keyRepeatInterval` | [Number](Number.md) | [static] Key repeat interval (frames) |
| `keyMapper` | Object | [static] [Keyboard Input Map](Input.md#keyboard-input-map) |
| `gamepadMapper` | Object | [static] [Gamepad Input Map](Input.md#gamepad-input-map) |

| `date` | [Number](Number.md) | [static][read-only] Time of the last input (milliseconds) |
| `dir4` | [Number](Number.md) | [static][read-only] Value for 4-direction input (supports numpad) |
| `dir8` | [Number](Number.md) | [static][read-only] Value for 8-direction input (supports numpad) |
| `_currentState` | Object | [static] Current input state {[key: string]: boolean} |
| `_previousState` | Object | [static] Previous input state {[key: string]: boolean} |
| `_gamepadStates` | [Array](Array.md).&lt;[Array](Array.md).&lt;Boolean&gt;&gt; | [static] State of the gamepad<br />(gamepad number, code, whether pressed) |
| `_latestButton` | [String](String.md) | [static] Latest button |
| `_pressedTime` | [Number](Number.md) | [static] Input time |
| `_date` | [Number](Number.md) | [static] Input time |
| `_dir4` | [Number](Number.md) | [static] Value for 4-direction input |
| `_dir8` | [Number](Number.md) | [static] Value for 8-direction input |
| `_preferredAxis` | [String](String.md) | [static] Preferred axis among x and y<br />(used to make 4-direction input more natural) |
| `_virtualButton` | [String](String.md) | [static] Virtual latest button |

#### Key Names
In "RPG Maker MZ," virtual key names are used instead of the actual names of keyboard keys or gamepad buttons.<br />
Note that the escape key has special handling, functioning as both cancel and menu.

| Key Name | Description |
| --- | --- |
| ok | Confirm |
| cancel | Cancel |
| shift | Dash |
| menu | Menu |
| pageup | Page Up |
| pagedown | Page Down |
| up | Move Up |
| down | Move Down |
| left | Move Left |
| right | Move Right |
| tab | N/A |
| control | N/A |
| escape | Used for both cancel and menu |
| debug | Debugging |

N/A indicates that the key has been mapped but is not used.


#### Keyboard Input Map
<code>{ code: 'Key Name', ...}</code> is a conversion table mapping key codes to [key names](Input.md#key-name).<br />
This is set in `keyMapper`. The following key names are defaults.

| code | Key Name | Keyboard |
| --- | --- | --- |
| 9 | tab | tab |
| 13 | ok | enter ※return |
| 16 | shift | shift |
| 17 | control | control |
| 18 | control | alt ※option |
| 27 | escape | escape |
| 32 | ok | space |
| 33 | pageup | pageup |
| 34 | pagedown | pagedown |
| 37 | left | left arrow |
| 38 | up | up arrow |
| 39 | right | right arrow |
| 40 | down | down arrow |
| 45 | escape | insert ※none |
| 81 | pageup | Q |
| 87 | pagedown | W |
| 88 | escape | X |
| 90 | ok | Z |
| 91 | | ※command |
| 96 | escape | numpad 0 |
| 98 | down | numpad 2 |
| 100 | left | numpad 4 |
| 102 | right | numpad 6 |
| 104 | up | numpad 8 |
| 120 | debug | F9 |

※ refers to the names on Mac keytops.<br />
Describing these keys using the names for either the Mac or Windows platforms may confuse players if their keyboards do not match the described keys.<br />
The command key is for reference.


#### Gamepad Input Map
<code>{ code: "Key Name", ...}</code> is a conversion table mapping gamepad button codes to [key names](Input.md#key-name).<br />
Analog stick inputs are converted to up, down, right, left.<br />
Button codes and button mappings vary by gamepad.<br />
This is set in `gamepadMapper`. The following key names are defaults.

| code | Key Name | Xbox Pad |
| --- | --- | --- |
| 0 | ok | A |
| 1 | cancel | B |
| 2 | shift | X |
| 3 | menu | Y |
| 4 | pageup | LB (bumper) |
| 5 | pagedown | RB (bumper) |
| 6 |  | LT (trigger) |
| 7 |  | RT (trigger) |
| 8 |  | back |
| 9 |  | Start |
| 10 |  | L stick push |
| 11 |  | R stick push |
| 12 | up | ↑ |
| 13 | down | ↓ |
| 14 | left | ← |
| 15 | right | → |

The Xbox pad is for reference.

### Methods

#### (static) _isEscapeCompatible (keyName) → {Boolean}
Checks if the key corresponds to the ESC key (cancel, menu).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `keyName` | [String](String.md) | [Key Name](Input.md#key-name) |


#### (static) _makeNumpadDirection (x, y) → {[Number](Number.md)}
Generates numpad direction from x and y input.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x-direction input (-1, 0, 1) |
| `y` | [Number](Number.md) | y-direction input (-1, 0, 1) |


#### (static) _onKeyDown (event)
Event handler called when a key is pressed down.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `event` | KeyboardEvent | Keyboard event |


#### (static) _onKeyUp (event)
Event handler called when a key is released.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `event` | KeyboardEvent | Keyboard event |


#### (static) _onLostFocus ()
Event handler called when focus is lost.


#### (static) _pollGamepads ()
Function to monitor (poll) gamepad states.


#### (static) _setupEventHandlers ()
Sets up event handlers.


#### (static) _shouldPreventDefault (keyCode)
Determines whether to prevent the default action of the event.<br/>
Returns true if `keyCode` is one of: 8: backspace, 9: tab, 33: pageup, 34: pagedown, 37: left, 38: up, 39: right, or 40: down.<br />
This helps to avoid some of the default browser behavior for keyboard input.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `keyCode` | [Number](Number.md) | Key code |


#### (static) _signX ()
Returns x-axis input (-1, 0, 1).


#### (static) _signY ()
Returns y-axis input (-1, 0, 1).


#### (static) _updateDirection ()
Updates direction.


#### (static) _updateGamepadState (gamepad, index)
Updates the state of the gamepad.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `gamepad` | Gamepad | Gamepad object |


#### (static) clear ()
Initializes input data.


#### (static) initialize ()
Initialization upon object creation.


#### (static) isLongPressed (keyName) → {Boolean}
Checks if the specified key is in a long-press state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `keyName` | [String](String.md) | [Key Name](Input.md#key-name) |


#### (static) isPressed (keyName) → {Boolean}
Checks if the specified key is currently pressed.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `keyName` | [String](String.md) | [Key Name](Input.md#key-name) |


#### (static) isRepeated (keyName) → {Boolean}
Checks if the specified key is in a key repeat state.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `keyName` | [String](String.md) | [Key Name](Input.md#key-name) |


#### (static) isTriggered (keyName) → {Boolean}
Checks if the specified key was pressed just now.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `keyName` | [String](String.md) | [Key Name](Input.md#key-name) |


#### (static) update ()
Updates every frame.


#### (static) virtualClick (buttonName)
**@MZ** Simulates the specified key being pressed virtually.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `buttonName` | [String](String.md) | [Key Name](Input.md#key-name) |


### MV Deprecated Methods
[static]
_wrapNwjsAlert ()
