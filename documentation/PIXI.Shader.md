# Class: PIXI.Shader
Configuration for rendering using GLSL.

When creating with `new`, it is necessary to first create a [PIXI.Program](http://pixijs.download/v5.3.12/docs/PIXI.Program.html). 
Using `PIXI.Shader.form()` allows for direct generation by passing fragment shader code. 
In this case, setting the vertex shader code to `null` will make the vertex shader default (without transformations).

For more details, refer to the official PixiJS documentation [PIXI.Shader](http://pixijs.download/v5.3.12/docs/PIXI.Shader.html).

Related classes: [PIXI.DisplayObject](PIXI.DisplayObject.md), [PIXI.uniformGroup](http://pixijs.download/v5.3.12/docs/PIXI.uniformGroup.html), [PIXI.ShaderSystem](http://pixijs.download/v5.3.12/docs/PIXI.ShaderSystem.html)

### new PIXI.Shader (program opt, uniforms opt)
#### Arguments

| Name      | Type                                                 | Characteristics    | Description                                   |
|-----------|------------------------------------------------------|---------------------|-----------------------------------------------|
| `program` | [PIXI.Program](http://pixijs.download/v5.3.12/docs/PIXI.Program.html) | <optional>          | GLSL program                                  |
| `uniforms`| Object                                               | <optional>          | Values to pass to the GLSL program            |

### Subclass

* [PIXI.Filter](PIXI.Filter.md)

### Properties

| Identifier | Type                                                 | Description                                   |
|------------|------------------------------------------------------|-----------------------------------------------|
| `program`  | [PIXI.Program](http://pixijs.download/v5.3.12/docs/PIXI.Program.html) | GLSL program                                  |
| `uniforms` | Object                                               | [read-only] Values passed to the GLSL program (same as `uniformGroup.uniforms`) |

### Methods

#### (static) form (vertexSrc opt, fragmentSrc opt, uniforms opt) → {[PIXI.Shader](PIXI.Shader.md)}
Generates and returns a shader.

##### Arguments

| Name         | Type                    | Characteristics    | Description                                   |
|--------------|-------------------------|---------------------|-----------------------------------------------|
| `vertexSrc`  | [String](String.md)     | <optional>          | Vertex shader code                            |
| `fragmentSrc`| [String](String.md)     | <optional>          | Fragment shader code                          |
| `uniforms`   | Object                  | <optional>          | Values to pass to the GLSL program            |

#### destroy ()
Disposes of the shader.
