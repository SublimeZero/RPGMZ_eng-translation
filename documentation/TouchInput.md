[Class Tree](index.md)

# Class: TouchInput
A static class that handles touch input from mouse and touch screens.

Related classes: [Input](Input.md), [Sprite_Destination](Sprite_Destination.md)

---

### Properties

| Identifier      | Type                   | Description                              |
|------------------|------------------------|------------------------------------------|
| `keyRepeatWait`  | [Number](Number.md)    | [static] The wait time of the pseudo key repeat in frames. |
| `keyRepeatInterval` | [Number](Number.md)  | [static] The interval of the pseudo key repeat in frames. |
| `wheelX`        | [Number](Number.md)    | [static][read-only] The horizontal scroll amount. |
| `wheelY`        | [Number](Number.md)    | [static][read-only] The vertical scroll amount. |
| `x`             | [Number](Number.md)    | [static][read-only] The x coordinate on the canvas area of the latest touch event. |
| `y`             | [Number](Number.md)    | [static][read-only] The y coordinate on the canvas area of the latest touch event. |
| `date`          | [Number](Number.md)    | [static][read-only] The time of the last input in milliseconds. |
| `_mousePressed`  | Boolean                | [static]                                  |
| `_screenPressed` | Boolean                | [static]                                  |
| `_pressedTime`   | [Number](Number.md)    | [static]                                  |
| `_moved`        | Boolean                | [static]                                  |
| `_released`     | Boolean                | [static]                                  |
| `_x`            | [Number](Number.md)    | [static]                                  |
| `_y`            | [Number](Number.md)    | [static]                                  |
| `_date`         | [Number](Number.md)    | [static]                                  |

---

### Deprecated MV Properties
[static]  
`_events`, `_triggered`, `_cancelled`, `_wheelX`, `_wheelY`

---

### Methods

#### (static) _createNewState ()
**@MZ** Create a new state.

---

#### (static) _onCancel (x, y)
Event when two-finger touch or the cancel (right) button is pressed.

##### Arguments

| Name | Type                 | Description |
|------|----------------------|-------------|
| `x`  | [Number](Number.md)  |             |
| `y`  | [Number](Number.md)  |             |

---

#### (static) _onHover (x, y)
**@MZ** Event when moving while the button is released.

##### Arguments

| Name | Type                 | Description |
|------|----------------------|-------------|
| `x`  | [Number](Number.md)  |             |
| `y`  | [Number](Number.md)  |             |

---

#### (static) _onLeftButtonDown (event)
Event when the confirm (left) button is pressed.

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | MouseEvent |             |

---

#### (static) _onLostFocus ()
**@MZ** Event when focus is lost.

---

#### (static) _onMiddleButtonDown (event)
Event when the auxiliary (middle) button (wheel) is pressed.  
No implementation in core script.

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | MouseEvent |             |

---

#### (static) _onMouseDown (event)
Event when any mouse button is pressed.

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | MouseEvent |             |

---

#### (static) _onMouseMove (event)
Event when the mouse moves.

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | MouseEvent |             |

---

#### (static) _onMouseUp (event)
Event when any mouse button is released.

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | MouseEvent |             |

---

#### (static) _onMove (x, y)
Event when the touched finger or mouse moves.

##### Arguments

| Name | Type                 | Description |
|------|----------------------|-------------|
| `x`  | [Number](Number.md)  |             |
| `y`  | [Number](Number.md)  |             |

---

#### (static) _onRelease (x, y)
Event when the touched finger or button is released.

##### Arguments

| Name | Type                 | Description |
|------|----------------------|-------------|
| `x`  | [Number](Number.md)  |             |
| `y`  | [Number](Number.md)  |             |

---

#### (static) _onRightButtonDown (event)
Event when the cancel (right) button is pressed.

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | MouseEvent |             |

---

#### (static) _onTouchCancel (event)
Event when the touch is cancelled (two-finger touch).

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | TouchEvent |             |

---

#### (static) _onTouchEnd (event)
Event when the touched finger is released.

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | TouchEvent |             |

---

#### (static) _onTouchMove (event)
Event when the finger moves while touching.

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | TouchEvent |             |

---

#### (static) _onTouchStart (event)
Event when touched.

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | TouchEvent |             |

---

#### (static) _onTrigger (x, y)
Event when triggered.

##### Arguments

| Name | Type                 | Description |
|------|----------------------|-------------|
| `x`  | [Number](Number.md)  |             |
| `y`  | [Number](Number.md)  |             |

---

#### (static) _onWheel (event)
Event when the wheel is scrolled.

##### Arguments

| Name   | Type       | Description |
|--------|------------|-------------|
| `event` | WheelEvent |             |

---

#### (static) _setupEventHandlers ()
Set up event handlers.

---

#### (static) clear ()
Clear data related to touch and click input.

---

#### (static) initialize ()
Class initialization.

---

#### (static) isCancelled () → {Boolean}
Whether the cancel (right) button has been pressed.

---

#### (static) isClicked () → {Boolean}
**@MZ** Whether it has been pressed.

---

#### (static) isHovered () → {Boolean}
**@MZ** Whether it has moved without pressing the button.

---

#### (static) isLongPressed () → {Boolean}
Whether the touch or confirm (left) button has been long-pressed.

---

#### (static) isMoved () → {Boolean}
Whether the touched finger or mouse cursor is moving.

---

#### (static) isPressed () → {Boolean}
Whether the touch or confirm (left) button is pressed.

---

#### (static) isReleased () → {Boolean}
Whether the touch or confirm (left) button is released.

---

#### (static) isRepeated () → {Boolean}
Whether the touch or confirm (left) button is pressed, or if a virtual key repeat has occurred.

---

#### (static) isTriggered () → {Boolean}
Whether the touch or confirm (left) button was pressed at that moment.

---

#### (static) update ()
Update touch and click input.

---

### Deprecated MV Methods
[static]  
_onPointerDown (event)
