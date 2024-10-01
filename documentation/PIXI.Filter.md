[Class Tree](index.md)

# Class: PIXI.Filter

## Superclass: [PIXI.Shader](PIXI.Shader.md)

Filters are a special type of WebGL shader applied to the screen. <br />
They use drawing programs written in a C-like language for OpenGL called [GLSL (OpenGL ES Shading Language)](https://ja.wikipedia.org/wiki/GLSL).

For more details on WebGL and shaders, refer to [WebGL: Web's 2D and 3D Graphics - MDN](https://developer.mozilla.org/ja/docs/Web/API/WebGL_API) and [Basics of WebGL - WebGLFundamentals](https://webglfundamentals.org/webgl/lessons/ja/).

For detailed information on the `Filter` class, refer to the official PixiJS reference [PIXI.Filter](http://pixijs.download/v5.3.12/docs/PIXI.Filter.html) and the documentation on [how to use filters](https://github.com/pixijs/pixi.js/wiki/v5-Creating-filters).

Related classes: [PIXI.DisplayObject](PIXI.DisplayObject.md), [PIXI.Container](PIXI.Container.md)

### new PIXI.Filter (vertexSrc opt, fragmentSrc opt, uniforms opt)
#### Arguments

| Name          | Type                     | Traits        | Description                                               |
|---------------|--------------------------|---------------|-----------------------------------------------------------|
| `vertexSrc`   | [String](String.md)      | <optional>    | Vertex shader (GLSL that transforms polygon vertex positions) |
| `fragmentSrc` | [String](String.md)      | <optional>    | Fragment shader (GLSL that transforms color on a pixel basis) |
| `uniforms`    | Object                   | <optional>    | Variables passed to GLSL                                  |

The `uniforms` can specify any variables in the form of `{variableName: value, ...}`. <br />
The variable names must be defined as `uniform` in the `vertexSrc` or `fragmentSrc` shaders. <br />
Note that `Filter` is normalized with the origin at the top left, allowing usage with JavaScript's coordinate system, but caution is advised when repurposing other GLSL code. <br />
For reference, vertex shaders may also be referred to as "vertex shaders" and fragment shaders as "pixel shaders."

### Subclasses
Additional filters can be downloaded from [PixiJS Filters](https://github.com/pixijs/pixi-filters).

* [PIXI.filters.BlurFilter](http://pixijs.download/v5.3.12/docs/PIXI.filters.BlurFilter.html)
* [PIXI.filters.BlurXFilter](http://pixijs.download/v5.3.12/docs/PIXI.filters.BlurXFilter.html)
* [PIXI.filters.BlurYFilter](http://pixijs.download/v5.3.12/docs/PIXI.filters.BlurYFilter.html)
* [PIXI.filters.ColorMatrixFilter](http://pixijs.download/v5.3.12/docs/PIXI.filters.ColorMatrixFilter.html)
* [PIXI.filters.DisplacementFilter](http://pixijs.download/v5.3.12/docs/PIXI.filters.DisplacementFilter.html)
* [PIXI.filters.FXAAFilter](http://pixijs.download/v5.3.12/docs/PIXI.filters.FXAAFilter.html)
* [PIXI.filters.NoiseFilter](http://pixijs.download/v5.3.12/docs/PIXI.filters.NoiseFilter.html)
* [PIXI.filters.VoidFilter](http://pixijs.download/v5.3.12/docs/PIXI.filters.VoidFilter.html)
* [ColorFilter](ColorFilter.md)

### Properties

| Identifier                | Type                     | Description                                   |
|---------------------------|--------------------------|-----------------------------------------------|
| `defaultVertexSrc`        | [String](String.md)      | [static] Default vertex shader                |
| `defaultFragmentSrc`      | [String](String.md)      | [static] Default fragment shader              |
| `SOURCE_KEY_MAP`          | Object                   | [static][protected]                           |
| `autoFit`                 | Boolean                  | Adjust the filter area to optimal size (default: true) |
| `blendMode`               | [Number](Number.md)      | [Blend mode](Sprite.md#blend-mode) (default: PIXI.BLEND_MODES.NORMAL) |
| `enabled`                 | Boolean                  | Whether to apply the filter (default: true) |
| `legacy`                  | Boolean                  | [read-only] Whether the filter uses attributes like position or uvs |
| `padding`                 | [Number](Number.md)      | Filter padding (if surrounding area is needed) (default: 0) |
| `resolution`              | [Number](Number.md)      | Filter resolution                              |
| `state`                   | [PIXI.State](http://pixijs.download/v5.3.12/docs/PIXI.State.html) | WebGL state                                   |
| `uniforms`                | Object                   | Current variables passed to GLSL             |

### Methods Inherited from Superclass

#### [PIXI.Shader](PIXI.Shader.md)

* [(static) from (vertexSrc, fragmentSrc, uniforms)](PIXI.Shader.md#staticform-vertexsrc-opt-fragmentsrc-opt-uniforms-optpixishader)
* [destroy ()](PIXI.Shader.md#destroy-)

### Methods

#### apply (filterManager, input, output, clearMode, currentState opt)
Applies the filter.

##### Arguments

| Name            | Type                         | Traits        | Description                                       |
|-----------------|------------------------------|---------------|---------------------------------------------------|
| `filterManager` | [PIXI.FilterSystem](http://pixijs.download/v5.3.12/docs/PIXI.FilterSystem.html) |               | The renderer that acquires the filter             |
| `input`         | [PIXI.RenderTexture](http://pixijs.download/v5.3.12/docs/PIXI.RenderTexture.html) |               | Image input target                                |
| `output`        | [PIXI.RenderTexture](http://pixijs.download/v5.3.12/docs/PIXI.RenderTexture.html) |               | Image output target                               |
| `clearMode`     | [PIXI.CLEAR_MODES](#PIXI.CLEAR_MODES) |               | Rendering output destination clear mode           |
| `currentState`  | Object                       | <optional>    | Current state of the filter                       |

`currentState` includes properties such as: <br />
`target`, `filters`, `sourceFrame`, `destinationFrame`, `renderTarget`, `resolution`

#### PIXI.CLEAR_MODES

| Name          | Type   | Description                         |
|---------------|--------|-------------------------------------|
| `AUTO`        | Same as `BLIT` |                                   |
| `BLEND`       | Overlays without clearing |                                |
| `BLIT`        | Matches the settings of FilterSystem |                             |
| `CLEAR`       | Clears                                |                                   |
| `NO`          | Same as `BLEND`, previously `false` |                                   |
| `YES`         | Same as `CLEAR`, previously `true` |                                   |
