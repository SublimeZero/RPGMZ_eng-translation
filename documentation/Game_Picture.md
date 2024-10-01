[Class Tree](index.md)

# Class: Game_Picture

| Data                | Sprite                            |
|---------------------|-----------------------------------|
| [Picture]           | [Sprite_Picture](Sprite_Picture.md) |

Used in event commands related to [Picture] (images in the img/pictures folder), specifying image coordinates and processing information.

Related Class: [Game_Screen](Game_Screen.md)

### new Game_Picture ()

### Properties

| Identifier           | Type                    | Description                                       |
|----------------------|-------------------------|---------------------------------------------------|
| `_name`              | [String](String.md)     | File name                                         |
| `_origin`            | [Number](Number.md)     | [[Origin]](Game_Picture.md#origin)               |
| `_x`                 | [Number](Number.md)     | x-coordinate (pixels)                             |
| `_y`                 | [Number](Number.md)     | y-coordinate (pixels)                             |
| `_scaleX`           | [Number](Number.md)     | Scale factor [Width]                              |
| `_scaleY`           | [Number](Number.md)     | Scale factor [Height]                             |
| `_opacity`           | [Number](Number.md)     | [Opacity] (0-255)                                |
| `_blendMode`         | [Number](Number.md)     | [[Blend Mode]](Sprite.md#blend-mode)            |
| `_targetX`          | [Number](Number.md)     | Target x-coordinate (pixels)                      |
| `_targetY`          | [Number](Number.md)     | Target y-coordinate (pixels)                      |
| `_targetScaleX`     | [Number](Number.md)     | Target scale factor [Width]                       |
| `_targetScaleY`     | [Number](Number.md)     | Target scale factor [Height]                      |
| `_targetOpacity`     | [Number](Number.md)     | Target [Opacity] (0-255)                         |
| `_duration`          | [Number](Number.md)     | Duration (frames)                                 |
| `_tone`              | [MV.Tone](MV.Tone.md)   | [Tone]                                           |
| `_toneTarget`        | [MV.Tone](MV.Tone.md)   | Tone target                                      |
| `_toneDuration`      | [Number](Number.md)     | Tone duration (frames)                            |
| `_angle`             | [Number](Number.md)     | Rotation angle (degrees)                          |
| `_rotationSpeed`     | [Number](Number.md)     | Rotation speed                                    |
| `_wholeDuration`     | [Number](Number.md)     | **@MZ** Total duration (frames)                   |
| `_easingType`        | [Number](Number.md)     | **@MZ** [Easing Type](#easing-type)              |
| `_easingExponent`    | [Number](Number.md)     | **@MZ** Easing exponent                           |

#### Origin
A number specifying where to display relative to the screen.

| Number | Description       |
|--------|-------------------|
| 0      | Top left          |
| 1      | Center            |

#### Easing Type

| Number | Description                   |
|--------|-------------------------------|
| 0      | Constant speed                |
| 1      | Starts slow                   |
| 2      | Ends slow                     |
| 3      | Starts slow and ends slow     |


### Methods

#### angle () → {[Number](Number.md)}
Returns the rotation angle.


#### applyEasing (current, target) → {[Number](Number.md)}
**@MZ** Applies easing and returns the new value.

##### Arguments

| Name     | Type                   | Description              |
|----------|------------------------|--------------------------|
| `current` | [Number](Number.md)   | Current position         |
| `target`  | [Number](Number.md)   | Target value             |


#### blendMode () → {[Number](Number.md)}
Returns [[Blend Mode]](Sprite.md#blend-mode).


#### calcEasing (t) → {[Number](Number.md)}
**@MZ** Calculates easing and returns the value.

##### Arguments

| Name | Type                   | Description         |
|------|------------------------|---------------------|
| `t`  | [Number](Number.md)    | Progress rate       |


#### easeIn (t, exponent) → {[Number](Number.md)}
**@MZ** Returns the unit progress value for ease-in (starts slow).

##### Arguments

| Name      | Type                   | Description         |
|-----------|------------------------|---------------------|
| `t`       | [Number](Number.md)    | Progress rate       |
| `exponent`| [Number](Number.md)    | Easing exponent     |


#### easeInOut (t, exponent) → {[Number](Number.md)}
**@MZ** Returns the unit progress value for ease-in-out (starts slow and ends slow).

##### Arguments

| Name      | Type                   | Description         |
|-----------|------------------------|---------------------|
| `t`       | [Number](Number.md)    | Progress rate       |
| `exponent`| [Number](Number.md)    | Easing exponent     |


#### easeOut (t, exponent) → {[Number](Number.md)}
**@MZ** Returns the unit progress value for ease-out (ends slow).

##### Arguments

| Name      | Type                   | Description         |
|-----------|------------------------|---------------------|
| `t`       | [Number](Number.md)    | Progress rate       |
| `exponent`| [Number](Number.md)    | Easing exponent     |


#### initBasic ()
Basic initialization.


#### initialize ()
Initialization at object creation.


#### initRotation ()
Initialize rotation.


#### initTarget ()
Initialize target.


#### initTone ()
Initialize [Tone].


#### move (origin, x, y, scaleX, scaleY, opacity, blendMode, duration, easingType)
Moves to the specified position.

##### Arguments

| Name       | Type                   | Description                          |
|------------|------------------------|--------------------------------------|
| `origin`   | [Number](Number.md)    | [[Origin]](Game_Picture.md#origin)  |
| `x`       | [Number](Number.md)    | x-coordinate (pixels)                |
| `y`       | [Number](Number.md)    | y-coordinate (pixels)                |
| `scaleX`   | [Number](Number.md)    | Scale factor [Width]                 |
| `scaleY`   | [Number](Number.md)    | Scale factor [Height]                |
| `opacity`   | [Number](Number.md)    | [Opacity] (0-255)                   |
| `blendMode` | [Number](Number.md)   | [[Blend Mode]](Sprite.md#blend-mode) |
| `duration` | [Number](Number.md)    | Duration (frames)                    |
| `easingType`| [Number](Number.md)   | **@MZ** [Easing Type](#easing-type) |


#### name () → {[String](String.md)}
Returns the file name.


#### opacity () → {[Number](Number.md)}
Returns [Opacity] (0-255).


#### origin () → {[Number](Number.md)}
Returns [[Origin]](Game_Picture.md#origin).


#### rotate (speed)
Rotates at the specified speed.

##### Arguments

| Name   | Type                   | Description     |
|--------|------------------------|------------------|
| `speed` | [Number](Number.md)   | Speed            |


#### scaleX () → {[Number](Number.md)}
Returns the scale factor (width).


#### scaleY () → {[Number](Number.md)}
Returns the scale factor (height).


#### show (name, origin, x, y, scaleX, scaleY, opacity, blendMode)
Displays at the specified position.

##### Arguments

| Name       | Type                   | Description                          |
|------------|------------------------|--------------------------------------|
| `name`     | [String](String.md)    | Name                                 |
| `origin`   | [Number](Number.md)    | [[Origin]](Game_Picture.md#origin)  |
| `x`       | [Number](Number.md)    | x-coordinate (pixels)                |
| `y`       | [Number](Number.md)    | y-coordinate (pixels)                |
| `scaleX`   | [Number](Number.md)    | Scale factor [Width]                 |
| `scaleY`   | [Number](Number.md)    | Scale factor [Height]                |
| `opacity`   | [Number](Number.md)    | [Opacity] (0-255)                   |
| `blendMode` | [Number](Number.md)   | [[Blend Mode]](Sprite.md#blend-mode) |


#### tint (tone, duration)

##### Arguments

| Name      | Type                   | Description         |
|-----------|------------------------|---------------------|
| `tone`    | [MV.Tone](MV.Tone.md)  | Tone                |
| `duration`| [Number](Number.md)    | Duration (frames)   |


#### tone () → {[MV.Tone](MV.Tone.md)}
Returns the tone.


#### update ()
Update every frame.


#### updateMove ()
Update movement.


#### updateRotation ()
Update rotation.


#### updateTone ()
Update [Tone].


#### x () → {[Number](Number.md)}
Returns the x-coordinate (pixels).


#### y () → {[Number](Number.md)}
Returns the y-coordinate (pixels).


### Deprecated MV Methods
erase ()
