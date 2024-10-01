[Class Tree](index.md)

# Class: PIXI.Renderer

## Superclass: [PIXI.AbstractRenderer](http://pixijs.download/v5.3.12/docs/PIXI.AbstractRenderer.html)
A class for rendering with WebGL.

For more details, refer to the official PixiJS site [PIXI.Renderer](http://pixijs.download/v5.3.12/docs/PIXI.Renderer.html).

Related classes: [Sprite_Animation](Sprite_Animation.md), [PIXI.Container](PIXI.Container.md), [PIXI.Application](PIXI.Application.md)

### new PIXI.Renderer (options opt)
#### Arguments
All values are optional.

| Name | Type | Description |
| --- | --- | --- |
| `options` | Object | See details below |
| `options.width` | [Number](Number.md) | Width of the rendering area (default: 800 pixels) |
| `options.height` | [Number](Number.md) | Height of the rendering area (default: 600 pixels) |
| `options.view` | [HTMLCanvasElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement) | Canvas for display |
| `options.useContextAlpha` | Boolean | Use the alpha state of the canvas (default: true) |
| `options.autoDensity` | Boolean | Allow resolutions other than 1 (default: false) |
| `options.antialias` | Boolean | Apply anti-aliasing (default: false) |
| `options.resolution` | [Number](Number.md) | Ratio of resolution / device pixels. Retina resolution is 2 (default: PIXI.settings.RESOLUTION) |
| `options.clearBeforeRender` | Boolean | Clear before rendering. Can only be set to false if preserveDrawingBuffer is true (default: true) |
| `options.preserveDrawingBuffer` | Boolean | Preserve the drawing buffer. Set to true if toDataUrl needs to be called on the WebGL context (default: false) |
| `options.backgroundColor` | [Number](Number.md) | Background color (default: 0x000000) |
| `options.backgroundAlpha` | [Number](Number.md) | Background opacity (default: 1) |
| `options.powerPreference` | [String](String.md) | Parameter passed to the WebGL context. Set to "high-performance" for devices with dual graphics cards |
| `options.context` | Object | Obtain all parameters from the specified WebGL context |

### Properties

| Identifier | Type | Description |
| --- | --- | --- | 
| `plugins` | Object | [static][read-only] Collection of [plugins](#plugins) |
| `batch` | [PIXI.BatchSystem](http://pixijs.download/v5.3.12/docs/PIXI.BatchSystem.html) | [read-only] Instance of the batch system |
| `context` | [PIXI.ContextSystem](http://pixijs.download/v5.3.12/docs/PIXI.ContextSystem.html) | [read-only] Instance of the context system |
| `extract` | [PIXI.Extract](http://pixijs.download/v5.3.12/docs/PIXI.Extract.html) | Deprecated in v6 (use `plugins.extract` instead) |
| `filter` | [PIXI.FilterSystem](http://pixijs.download/v5.3.12/docs/PIXI.FilterSystem.html) | [read-only] Instance of the filter system |
| `framebuffer` | [PIXI.FramebufferSystem](http://pixijs.download/v5.3.12/docs/PIXI.FramebufferSystem.html) | [read-only] Instance of the framebuffer system |
| `geometry` | [PIXI.GeometrySystem](http://pixijs.download/v5.3.12/docs/PIXI.GeometrySystem.html) | [read-only] Instance of the geometry system |
| `gl` | WebGLRenderingContext | [read-only] WebGL context (default: undefined) |
| `globalUniforms` | [PIXI.UniformGroup](http://pixijs.download/v5.3.12/docs/PIXI.UniformGroup.html) | [read-only] Global uniforms |
| `mask` | [PIXI.MaskSystem](http://pixijs.download/v5.3.12/docs/PIXI.MaskSystem.html) | [read-only] Instance of the mask system |
| `projection` | [PIXI.ProjectionSystem](http://pixijs.download/v5.3.12/docs/PIXI.ProjectionSystem.html) | [read-only] Instance of the projection system |
| `renderingToScreen` | Boolean | [read-only] Flag if rendering to the screen vs renderTexture (default: true) |
| `renderTexture` | [PIXI.RenderTextureSystem](http://pixijs.download/v5.3.12/docs/PIXI.RenderTextureSystem.html) | [read-only] Instance of the render texture system |
| `scissor` | [PIXI.ScissorSystem](http://pixijs.download/v5.3.12/docs/PIXI.RenderTextureSystem.html) | [read-only] Instance of the scissor system |
| `shader` | [PIXI.ShaderSystem](http://pixijs.download/v5.3.12/docs/PIXI.ShaderSystem.html) | [read-only] Instance of the shader system |
| `state` | [PIXI.StateSystem](http://pixijs.download/v5.3.12/docs/PIXI.StateSystem.html) | [read-only] Instance of the state system |
| `stencil` | [PIXI.StencilSystem](http://pixijs.download/v5.3.12/docs/PIXI.StencilSystem.html) | [read-only] Instance of the stencil system |
| `texture` | [PIXI.TextureSystem](http://pixijs.download/v5.3.12/docs/PIXI.TextureSystem.html) | [read-only] Instance of the texture system |
| `textureGC` | [PIXI.TextureGCSystem](http://pixijs.download/v5.3.12/docs/PIXI.TextureGCSystem.html) | [read-only] Instance of the texture garbage collection system |

#### Plugins
Not to be confused with RPG Maker MZ plugins, these are extensions of PixiJS functionality.

| Name | Type | Description |
| --- | --- | --- |
| `accessibility` | [PIXI.AccessibilityManager](http://pixijs.download/v5.3.12/docs/PIXI.AccessibilityManager.html) | TAB key focus settings for UI components |
| `batch` | [PIXI.BatchRenderer](#PIXI.BatchRenderer) | Batch processing for Sprites, Graphics, and Meshes |
| `extract` | [PIXI.Extract](http://pixijs.download/v5.3.12/docs/PIXI.Extract.html) | Object for outputting images in other formats |
| `interaction` | [PIXI.InteractionManager](http://pixijs.download/v5.3.12/docs/PIXI.InteractionManager.html) | UI and collision detection |
| `particle` | [PIXI.ParticleRenderer](http://pixijs.download/v5.3.12/docs/PIXI.ParticleRenderer.html) | Renderer for ParticleContainer |
| `prepare` | [PIXI.Prepare](http://pixijs.download/v5.3.12/docs/PIXI.Prepare.html) | Pre-render processing for displayObject |
| `tilingSprite` | [PIXI.TilingSpriteRenderer](http://pixijs.download/v5.3.12/docs/PIXI.TilingSpriteRenderer.html) | Renderer for TilingSprite |

#### PIXI.BatchRenderer
PIXI.BatchRenderer is an object that inherits from [PIXI.AbstractBatchRenderer](http://pixijs.download/v5.3.12/docs/PIXI.AbstractBatchRenderer.html) generated by [PIXI.BatchPluginFactory](http://pixijs.download/v5.3.12/docs/PIXI.BatchPluginFactory.html), but there is no class definition itself.

### Methods Inherited from the Superclass

#### [PIXI.AbstractRenderer](http://pixijs.download/v5.3.12/docs/PIXI.AbstractRenderer.html)

 * [generateTexture (displayObject, scaleMode, resolution, region)](http://pixijs.download/v5.3.12/docs/PIXI.AbstractRenderer.html#generateTexture)
 * [initPlugins (staticMap)](http://pixijs.download/v5.3.12/docs/PIXI.AbstractRenderer.html#initPlugins)

### Methods

#### (static)registerPlugin (pluginName, ctor)
Register a plugin.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `pluginName` | [String](String.md) | Plugin name |
| `ctor` | IRendererPluginConstructor | Constructor |

#### addSystem (ClassRef, name) →  {PIXI.Renderer}
Add a system.

##### Arguments

| Name | Type | Characteristics | Description |
| --- | --- | --- | --- |
| `ClassRef` | Reference to PIXI.Renderer |  | Class reference |
| `name` | [String](String.md) | <optional> | Name |

#### clear ()
Clear the framebuffer.

#### destroy (removeView)
Override: [PIXI.AbstractRenderer](http://pixijs.download/v5.3.12/docs/PIXI.AbstractRenderer.html#destroy)

#### render (displayObject, options opt)
Perform rendering.

##### Arguments

| Name                | Type                                                 | Characteristics | Description                             |
|---------------------|------------------------------------------------------|-----------------|-----------------------------------------|
| `displayObject`     | [PIXI.IRenderableObject](http://pixijs.download/v5.3.12/docs/PIXI.IRenderableObject.html) |                 | The object to be rendered               |
| `options`           | Object                                               | <optional>      | See details below                       |
| `options.renderTexture` | [PIXI.RenderTexture](http://pixijs.download/v5.3.12/docs/PIXI.RenderTexture.html) | <optional>      | The render texture                       |
| `options.clear`     | Boolean                                              | <optional>      | Whether to clear before rendering (default: true) |
| `options.transform`  | [PIXI.Matrix](http://pixijs.download/v5.3.12/docs/PIXI.Matrix.html) | <optional>      | Transformation to apply before rendering |
| `options.skipUpdateTransform` | Boolean                                     | <optional>      | Whether to skip updating the transformation (default: false) |

#### reset () →  {PIXI.Renderer}
Initializes the WebGL state.

#### resize (screenWidth, screenHeight)
Overrides: [PIXI.AbstractRenderer](http://pixijs.download/v5.3.12/docs/PIXI.AbstractRenderer.html#resize) 

### Events

#### context
Event triggered when the WebGL context is called.

##### Arguments

| Name    | Type                    | Description                 |
|---------|-------------------------|-----------------------------|
| `gl`    | WebGLRenderingContext    | The WebGL context           |

#### postrender
Event triggered after rendering is complete.

#### prerender
Event triggered before rendering begins.

#### resize
Event triggered when resizing occurs.

##### Arguments

| Name          | Type                     | Description                     |
|---------------|--------------------------|---------------------------------|
| `screenWidth` | [Number](Number.md)      | Width of the screen (pixels)   |
| `screenHeight`| [Number](Number.md)      | Height of the screen (pixels)  |
