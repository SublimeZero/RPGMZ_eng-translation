[Class Tree](index.md)

# Class: [RPG](RPG.md).Animation

| Database        | JSON File        | Global Variable                                         | Sprite                                   |
|-----------------|-------------------|---------------------------------------------------------|------------------------------------------|
| [Animation]     | Animations.json   | [$dataAnimations](global.md#dataanimations-arrayrpganimation)(array) | [Sprite_Animation](Sprite_Animation.md) \| [Sprite_AnimationMV](Sprite_AnimationMV.md) |

The data for [Sprite_Animation](Sprite_Animation.md) includes Effekseer data.

The data for [Sprite_AnimationMV](Sprite_AnimationMV.md) contains two types of images that can be displayed simultaneously.<br />
Each image includes multiple patterns.<br />
The two images are concatenated, and the pattern numbers are shared.

Related Classes: [RPG.UsableItem](RPG.UsableItem.md), [RPG.Weapon](RPG.Weapon.md)

### Properties

| Identifier         | Type                                                                 | Description                                |
|--------------------|----------------------------------------------------------------------|--------------------------------------------|
| `id`               | [Number](Number.md)                                                | Animation ID                               |
| `name`             | [String](String.md)                                                | [Name] displayed in the editor            |
| `animation1Name`   | [String](String.md)                                                | File name of [Image] 1 (without extension) located in the img/animations/ folder |
| `animation1Hue`    | [Number](Number.md)                                                | Hue of [Image] 1 (0–360)                  |
| `animation2Name`   | [String](String.md)                                                | File name of [Image] 2 (without extension) located in the img/animations/ folder |
| `animation2Hue`    | [Number](Number.md)                                                | Hue of [Image] 2 (0–360)                  |
| `position`         | [Number](Number.md)                                                | [Position](#position) (for [Sprite_AnimationMV](Sprite_AnimationMV.md)) |
| `frameMax`         | [Number](Number.md)                                                | Maximum [Frame Count]                      |
| `frames`           | [Array](Array.md).&lt;[Array](Array.md).&lt;[Array](Array.md).&lt;[Number](Number.md)&gt;&gt;&gt; | [Frame Information](#frame-information)    |
| `timings`          | [Array](Array.md).&lt;[RPG.Animation.Timing](RPG.Animation.Timing.md)&gt; | Array of [SE and Flash Timing]            |
| `displayType`      | [String](String.md)                                                | **@MZ** Display Type                       |

#### Position
If [Above Head], [Center], or [Below Feet] is used for an area attack, it will be displayed on individual battlers.

| Number | [Position]       |
|--------|------------------|
| 0      | Above Head       |
| 1      | Center           |
| 2      | Below Feet       |
| 3      | Screen           |

#### Frame Information
The `frames` structure has a three-dimensional array format: frames[Frame Number][Cell Number][Data].<br />
MZ's Effekseer data does not have this `frames` property.

| Number | [Data]                            |
|--------|------------------------------------|
| 0      | [Pattern] Number                   |
| 1      | [X] Coordinate (pixels)            |
| 2      | [Y] Coordinate (pixels)            |
| 3      | [Scale] (%)                        |
| 4      | [Rotation Angle] (360 degrees)    |
| 5      | [Horizontal Flip] (0: None, 1: Yes) |
| 6      | [Opacity]                         |
| 7      | [[Blending Method]](Sprite.md#blending-method) |

### Inner Class

* [RPG.Animation.Timing](RPG.Animation.Timing.md)
