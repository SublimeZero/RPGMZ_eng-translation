[Class Tree](index.md)

# Class: PIXI.Texture

## Superclass: [PIXI.utils.EventEmitter](http://pixijs.download/v5.3.12/docs/PIXI.utils.EventEmitter.html)
Image data for (WebGL) rendering.

Rather than being added directly to a container for display, it is set to display objects such as [PIXI.Sprite](PIXI.Sprite.md).

When creating with `new`, it is necessary to first create a [PIXI.BaseTexture](http://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html), but you can reuse the settings.
Using `PIXI.Texture.from()`, you can generate a texture by passing the image filename directly, and `PIXI.BaseTexture` is not required.

When specifying in `uniforms` such as in [PIXI.Shader](PIXI.Shader.md), you can pass it as `〇〇: PIXI.Texture instance` and receive it with `uniform sampler2D 〇〇`.

For details, please refer to the official PixiJS site [PIXI.Texture](http://pixijs.download/v5.3.12/docs/PIXI.Texture.html).

Related class: [Bitmap](Bitmap.md)

### new PIXI.Texture (baseTexture, frame opt, orig opt, trim opt, rotate opt, anchor opt)
#### Arguments

| Name         | Type                                               | Required     | Description                                       |
|--------------|----------------------------------------------------|--------------|---------------------------------------------------|
| `baseTexture`| [PIXI.BaseTexture](http://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html) | Yes          | Source of the texture                             |
| `frame`      | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html)   | <Optional>   | Rectangular area to display                       |
| `orig`       | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html)   | <Optional>   | Original rectangular area                          |
| `trim`       | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html)   | <Optional>   | Original trimming rectangular area                 |
| `rotate`     | [Number](Number.md)                               | <optional>   | Rotation angle (radians)                          |
| `anchor`     | [PIXI.IPointData](http://pixijs.download/v5.3.12/docs/PIXI.IPointData.html) | <Optional>   | Anchor point                                      |

### Properties

| Identifier    | Type                                               | Description                                     |
|---------------|----------------------------------------------------|-------------------------------------------------|
| `EMPTY`       | [PIXI.Texture](PIXI.Texture.md)                   | [static] Empty texture                          |
| `WHITE`       | [PIXI.Texture](PIXI.Texture.md)                   | [static] 16×16 size white texture              |
| `_frame`      | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html) | Rectangle area where the texture is displayed   |
| `baseTexture` | [PIXI.BaseTexture](http://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html) | Source of the texture                           |
| `defaultAnchor`| [PIXI.Point](http://pixijs.download/v5.3.12/docs/PIXI.Point.html) | Default anchor point for objects using this texture (default: {0,0}) |
| `frame`       | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html) | Rectangle area where the texture is displayed   |
| `width`       | [Number](Number.md)                               | Width (in pixels)                              |
| `height`      | [Number](Number.md)                               | Height (in pixels)                             |
| `noFrame`     | Boolean                                           | Indicates if there is no frame (default: false) |
| `orig`        | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html) | Original rectangular area                       |
| `resolution`  | [Number](Number.md)                               | [read-only] Resolution                         |
| `rotate`      | [Number](Number.md)                               | Rotation angle                                 |
| `textureCacheIds` | [Array](Array.md).&lt;[String](String.md)&gt; | Array of cache IDs                             |
| `trim`        | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html) | Original trimming rectangular area              |
| `uvMatrix`    | [PIXI.TextureMatrix](http://pixijs.download/v5.3.12/docs/PIXI.TextureMatrix.html) | UV transformation matrix                       |
| `valid`       | Boolean                                           | Indicates whether it is determined to be renderable (default: false) |
| `_updateID`   | [Number](Number.md)                               | [protected] Update ID (default: 0)            |
| `_uvs`        | [PIXI.TextureUvs](http://pixijs.download/v5.3.12/docs/PIXI.TextureUvs.html) | [protected] WebGL UVS data cache               |

### Methods

#### (static) addToCache (texture, id)
Adds to the PIXI shared cache.

##### Arguments

| Name     | Type                                           | Description            |
|----------|------------------------------------------------|------------------------|
| `texture`| [PIXI.Texture](http://pixijs.download/v5.3.12/docs/PIXI.Texture.html) | Texture                |
| `id`     | [String](String.md)                            | Cache ID               |

#### (static) from (source, options opt, strict opt) → {PIXI.Texture}
Generates a texture.

##### Arguments

| Name     | Type                                                                 | Required    | Description                                 |
|----------|----------------------------------------------------------------------|-------------|---------------------------------------------|
| `source` | [String](String.md) \| HTMLImageElement \| HTMLCanvasElement \| HTMLVideoElement \| [PIXI.BaseTexture](http://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html) | Yes         | Source (String is the file path)           |
| `options`| Object                                                               | <optional>  | Properties include only `pixiIdPrefix`     |
| `options.pixiIdPrefix` | [String](String.md)                                        | <optional>  | ID prefix                                   |
| `strict` | Boolean                                                             | <optional>  | [PIXI.settings.STRICT_TEXTURE_CACHE](http://pixijs.download/v5.3.12/docs/PIXI.settings.html#STRICT_TEXTURE_CACHE) |

#### (static) fromBuffer (buffer, width, height, options opt) → {PIXI.Texture}
Generates a texture from buffer data.

| Name     | Type                     | Required   | Description            |
|----------|--------------------------|------------|------------------------|
| `buffer` | Float32Array \| Uint8Array | Yes        | Array of image data    |
| `width`  | [Number](Number.md)     | Yes        | Width (in pixels)      |
| `height` | [Number](Number.md)     | Yes        | Height (in pixels)     |
| `options`| Object                   | <optional> | Same as constructor `options` of [PIXI.BaseTexture](http://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html) |

#### (static) fromLoader (source, imageUrl, name) → {PIXI.Texture}
Generates a texture from the source and adds it to the cache.

##### Arguments

| Name     | Type                                           | Required     | Description                       |
|----------|------------------------------------------------|--------------|-----------------------------------|
| `source` | [String](String.md) \| HTMLImageElement \| HTMLCanvasElement | Yes          | Source (String is the file path)  |
| `imageUrl`| [String](String.md)                          | Yes          | Cache filename                     |
| `name`   | [String](String.md)                          | <optional>   | Alias for `imageUrl` (default: `imageUrl`) |

#### (static) fromURL (url, options) → {PIXI.Texture}
Generates a texture from a URL.

##### Arguments

| Name     | Type          | Required     | Description       |
|----------|---------------|--------------|-------------------|
| `url`    | [String](String.md) | Yes          | URL               |
| `options`| Object        | <optional>   |                   |

#### (static) removeFromCache (texture) → {PIXI.Texture}
Removes the texture from the cache and returns it.

| `texture` | [String](String.md) \| [PIXI.Texture](PIXI.Texture.md) | ID or instance |

#### castToBaseTexture () → {[PIXI.BaseTexture](http://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html)}
Casts to `BaseTexture` and returns it.

#### clone () → {PIXI.Texture}
Creates and returns a clone.

#### destroy (destroyBase opt)
Disposes of the object.

##### Arguments

| Name          | Type    | Required    | Description                                       |
|---------------|---------|-------------|---------------------------------------------------|
| `destroyBase` | Boolean | <optional>  | Whether to dispose of `PIXI.BaseTexture` as well (default: false) |

#### update ()
Updates the rendering. For updating the frame, use `updateUvs()` instead.

#### updateUvs ()
Updates the frame and trim.

#### onBaseTextureUpdated (baseTexture)
Handler for when the base texture is updated.

##### Arguments

| Name          | Type                                               | Description           |
|---------------|----------------------------------------------------|-----------------------|
| `baseTexture` | [PIXI.BaseTexture](http://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html) | Base texture          |
