[Class Tree](index.md)

# Class: [RPG](RPG.md).EventPage
JSON data that constitutes the event's [EV page].

Included in the pages property of [RPG.Event](RPG.Event.md).

Related classes: [RPG.BattleEventPage](RPG.BattleEventPage.md)

### Properties

| Identifier          | Type                                         | Description                                 |
|---------------------|----------------------------------------------|---------------------------------------------|
| `conditions`        | [RPG.EventPage.Conditions](RPG.EventPage.Conditions.md) | [Appearance Conditions]                     |
| `image`             | [RPG.EventPage.Image](RPG.EventPage.Image.md) | [Image]                                    |
| `moveType`          | [Number](Number.md)                          | [Autonomous Movement Type](RPG.EventPage.md#autonomous-movement-type) |
| `moveSpeed`         | [Number](Number.md)                          | [Autonomous Movement Speed](RPG.EventPage.md#autonomous-movement-speed) |
| `moveFrequency`     | [Number](Number.md)                          | [Autonomous Movement Frequency](RPG.EventPage.md#autonomous-movement-frequency) |
| `moveRoute`         | [Array](Array.md).&lt;[RPG.MoveRoute](RPG.MoveRoute.md)&gt; | [Route] (Valid when moveType is 3: Custom) |
| `walkAnime`         | Boolean                                      | [Walking Animation]                         |
| `stepAnime`         | Boolean                                      | [Footstep Animation]                        |
| `directionFix`      | Boolean                                      | [Direction Fix]                            |
| `through`           | Boolean                                      | [Through]                                  |
| `priorityType`      | [Number](Number.md)                          | [Priority](RPG.EventPage.md#priority)     |
| `trigger`           | [Number](Number.md)                          | [Trigger](RPG.EventPage.md#trigger)       |
| `list`              | [Array](Array.md).&lt;[RPG.EventCommand](RPG.EventCommand.md)&gt; | [Execution Contents]                        |

#### Autonomous Movement [Type]

| Number | [Type]      |
|--------|-------------|
| 0      | Fixed       |
| 1      | Random      |
| 2      | Approach    |
| 3      | Custom      |

#### Autonomous Movement [Speed]

| Number | [Speed]      |
|--------|--------------|
| 1      | 1/8 speed    |
| 2      | 1/4 speed    |
| 3      | 1/2 speed    |
| 4      | Normal speed |
| 5      | 2x speed     |
| 6      | 4x speed     |

#### Autonomous Movement [Frequency]

| Number | [Frequency]  |
|--------|--------------|
| 1      | Minimum      |
| 2      | Low          |
| 3      | Standard     |
| 4      | High         |
| 5      | Maximum      |

#### [Priority]

| Number | [Priority]  |
|--------|--------------|
| 0      | Below normal characters |
| 1      | Same as normal characters |
| 2      | Above normal characters |

#### [Trigger]

| Number | [Trigger]  |
|--------|------------|
| 0      | Confirm button |
| 1      | Contact from player |
| 2      | Contact from event |
| 3      | Automatic execution |
| 4      | Parallel processing |

### Inner Classes

* [RPG.EventPage.Conditions](RPG.EventPage.Conditions.md)
* [RPG.EventPage.Image](RPG.EventPage.Image.md)
