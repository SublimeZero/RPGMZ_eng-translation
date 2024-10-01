[Class Tree](index.md)

# Class: ColorFilter

## Superclass: [PIXI.Filter](PIXI.Filter.md)

WebGL color filter object.

Related classes: [Scene_Base](Scene_Base.md), [Sprite](Sprite.md), [Spriteset_Base](Spriteset_Base.md)

### new ColorFilter ()

### Methods Inherited from Superclass

#### [PIXI.Shader](PIXI.Shader.md)

* [destroy ()](PIXI.Shader.md#destroy-)

####  [PIXI.Filter](PIXI.Filter.md) 

* [apply (filterManager, input, output, clearMode, currentState)](PIXI.Filter.md#apply-filtermanager-input-output-clear-currentstate-opt)


### Methods

#### _fragmentSrc () → {String}
Returns the source of the fragment shader as a string.


#### initialize ()
Initializes the object.


#### setBlendColor (color)
Sets the blend color with the specified value.

##### Arguments

| Name   | Type                   | Description                 |
|--------|------------------------|-----------------------------|
| `color`| [MV.Color](MV.Color.md) | Blend color [r, g, b, a]   |


#### setBrightness (brightness)
Sets the brightness with the specified value.

##### Arguments

| Name       | Type              | Description                |
|------------|-------------------|----------------------------|
| `brightness` | [Number](Number.md) | Brightness (0 to 255)     |


#### setColorTone (tone)
Sets the [color tone] with the specified value.

##### Arguments

| Name  | Type                    | Description               |
|-------|-------------------------|---------------------------|
| `tone`| [MV.Tone](MV.Tone.md) | Color tone [r, g, b, gray] |


#### setHue (hue)
Sets the hue with the specified value.

##### Arguments

| Name | Type              | Description                |
|------|-------------------|----------------------------|
| `hue`| [Number](Number.md) | Hue (-360 to 360)         |
