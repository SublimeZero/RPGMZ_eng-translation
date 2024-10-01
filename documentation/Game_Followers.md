[Class Tree](index.md)

# Class: Game_Followers

A class that manages the lineup and other aspects of [party members] grouped as [Game_Follower](Game_Follower.md).

Main Path
```js
$gamePlayer.followers()
```

### new Game_Followers ()

### Properties

| Identifier  | Type | Description                          |
| ----------- | ---- | ------------------------------------ |
| `_visible`  | Boolean | Whether [party walking] is enabled  |
| `_gathering`| Boolean | Whether the party is gathering     |
| `_data`     | [Array](Array.md).&lt;[Game_Follower](Game_Follower.md)&gt; | Array of [party members] |

### Methods

#### areGathered () → {Boolean}
Returns whether the [party members] are gathered.

#### areGathering () → {Boolean}
Returns whether the [party members] are currently gathering.

#### areMoving () → {Boolean}
Returns whether the [party members] are moving.

#### data () → {[Array](Array.md).&lt;[Game_Follower](Game_Follower.md)&gt;}
**@MZ** Returns the array of [party members].

#### follower (index) → {[Game_Follower](Game_Follower.md)}
Returns the [party member] at the specified index.<br />
The player (the leading character) is not included as a party member, so indices start from 0 with the second character (0: second member, 1: third member, 2: fourth member, etc.).

##### Parameters

| Name    | Type     | Description      |
| ------- | -------- | ---------------- |
| `index` | [Number](Number.md) | Index of the [party member] |

#### gather ()
Gather all [party members].

#### hide ()
Hide the [party members].

#### initialize ()
Initializes the object upon creation.

#### isSomeoneCollided (x, y) → {Boolean}
Returns whether any [party member] is at the specified location.

##### Parameters

| Name | Type     | Description          |
| ---- | -------- | -------------------- |
| `x`  | [Number](Number.md) | X coordinate (in tiles) |
| `y`  | [Number](Number.md) | Y coordinate (in tiles) |

#### isVisible () → {Boolean}
Returns whether the [party members] are visible.

#### jumpAll ()
Makes all [party members] jump to match the player character's jump height.

#### refresh ()
Updates the [party members].

#### reverseData () → {[Array](Array.md).&lt;[Game_Follower](Game_Follower.md)&gt;}
**@MZ** Returns the array of [party members] in reverse order.

#### setup ()
**@MZ** Prepares the party member objects.

#### show ()
Shows the [party members].

#### synchronize (x, y, d)
Synchronizes the [party members] to the specified position and direction.

##### Parameters

| Name  | Type     | Description                   |
| ----- | -------- | ----------------------------- |
| `x`   | [Number](Number.md) | X coordinate (in tiles) |
| `y`   | [Number](Number.md) | Y coordinate (in tiles) |
| `d`   | [Number](Number.md) | Direction (corresponding to the numpad) |

#### update ()
Updates the [party members].

#### updateMove ()
Updates the movement of the [party members].

#### visibleFollowers () → {[Array](Array.md).&lt;[Game_Follower](Game_Follower.md)&gt;}
Returns the array of visible [party members].

### Deprecated MV Methods
- `forEach (callback, thisObject)`
- `reverseEach (callback, thisObject)`
