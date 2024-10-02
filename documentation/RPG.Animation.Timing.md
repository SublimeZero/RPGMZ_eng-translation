[Class Tree](index.md)

# Class: [RPG](RPG.md).[Animation](RPG.Animation.md).Timing
Data that describes the timing of [SE (Sound Effects)] and flashes in an [Animation].

Related Class: [Sprite_Animation](Sprite_Animation.md)

### Properties

| Identifier      | Type                                             | Description                               |
|-----------------|--------------------------------------------------|-------------------------------------------|
| `frame`         | [Number](Number.md)                             | [Frame] number (one less than displayed in the editor) |
| `se`            | [RPG.AudioFile](RPG.AudioFile.md)              | [SE (Sound Effect)]                      |
| `flashScope`    | [Number](Number.md)                             | [Flash Scope](RPG.Animation.Timing.md#flash-scope) |
| `flashColor`    | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of flash colors [Red, Green, Blue, Intensity] |
| `flashDuration`  | [Number](Number.md)                             | Duration of the flash [time] (in 1/15 second units) |

#### Flash Scope
The target erasure erases the image of the targeted battler.

| Number | Flash Scope     |
|--------|------------------|
| 0      | None             |
| 1      | Target (the battler flashes) |
| 2      | Screen (entire screen flashes) |
| 3      | Target Erasure (the value of flashColor is ignored) |
