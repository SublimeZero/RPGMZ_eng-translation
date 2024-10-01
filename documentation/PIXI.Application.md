[Class Tree](index.md)

# Class: PIXI.Application
This class holds the essential objects used in PixiJS.

In versions before v4, required objects were created individually.  
Now, this class is responsible for both generating and holding those necessary objects.  
By simply creating an instance of `PIXI.Application`, the environment for using PixiJS is ready.

For more details, refer to the official PixiJS reference: [PIXI.Application](http://pixijs.download/v5.3.12/docs/PIXI.Application.html).

Related Classes: [Graphics](Graphics.md)

### new PIXI.Application (options opt)
#### Arguments
All values are optional.

| Name | Type | Description |
| --- | --- | --- |
| `options` | Object | See details below |
| `options.autoStart` | Boolean | Whether to start rendering after creation (default: true) |
| `options.width` | [Number](Number.md) | Width of the rendering area (default: 800 pixels) |
| `options.height` | [Number](Number.md) | Height of the rendering area (default: 600 pixels) |
| `options.view` | [HTMLCanvasElement](https://developer.mozilla.org/en/docs/Web/API/HTMLCanvasElement) | Canvas for display |
| `options.useContextAlpha` | Boolean | Whether to use the alpha state of the canvas (default: true) |
| `options.autoDensity` | Boolean | Whether to allow resolutions other than 1 (default: false) |
| `options.antialias` | Boolean | Whether to apply antialiasing (default: false) |
| `options.preserveDrawingBuffer` | Boolean | Whether to preserve the drawing buffer, useful if `toDataUrl` is needed in a WebGL context (default: false) |
| `options.resolution` | [Number](Number.md) | Resolution/device pixel ratio. Retina displays are typically set to 2 (default: PIXI.settings.RESOLUTION) |
| `options.forceCanvas` | Boolean | Whether to force canvas rendering (otherwise uses WebGL) (default: false) |
| `options.backgroundColor` | [Number](Number.md) | Background color (default: 0x000000) |
| `options.backgroundAlpha` | [Number](Number.md) | Background opacity (default: 1) |
| `options.clearBeforeRender` | Boolean | Whether to clear before rendering. Can only be false if `preserveDrawingBuffer` is true (default: true) |
| `options.powerPreference` | [String](String.md) | Parameter passed to the WebGL context. On devices with dual graphic cards, set to "high-performance" |
| `options.sharedTicker` | Boolean | Whether to use `PIXI.Ticker.shared` (default: false) |
| `options.sharedLoader` | Boolean | Whether to use `PIXI.Loader.shared` (default: false) |
| `options.resizeTo ` | [Window](https://developer.mozilla.org/en/docs/Web/API/Window) \| [HTMLElement](https://developer.mozilla.org/en/docs/Web/API/HTMLElement) | Browser window or HTML element to resize to |

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| ` loader` | [PIXI.Loader](http://pixijs.download/v5.3.12/docs/PIXI.Loader.md) | [read-only] The loader |
| `renderer` | [PIXI.Renderer](PIXI.Renderer.md) \| [PIXI.CanvasRenderer](http://pixijs.download/v5.3.12/docs/PIXI.CanvasRenderer.html) | [static] The WebGL or Canvas renderer |
| `resizeTo ` | [Window](https://developer.mozilla.org/en/docs/Web/API/Window) \| [HTMLElement](https://developer.mozilla.org/en/docs/Web/API/HTMLElement) | Target window or HTML element for resizing |
| `screen` | [PIXI.Rectangle](http://pixijs.download/v5.3.12/docs/PIXI.Rectangle.html) | [read-only] The size of the screen used for interactions and filters |
| `stage` | [PIXI.Container](PIXI.Container.md) | The root (for **RPG Maker MZ**, it's [Scene_Base](Scene_Base.md)) |
| `ticker` | [PIXI.Ticker](http://pixijs.download/v5.3.12/docs/PIXI.Ticker.html) | Object for frame-by-frame updates (default: `PIXI.Ticker.shared`) |
| `view` | HTMLCanvasElement | [read-only] The canvas element used for rendering |

### Methods

#### (static) registerPlugin (plugin)
Registers a plugin.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `plugin` | [PIXI.IApplicationPlugin](http://pixijs.download/v5.3.12/docs/PIXI.IApplicationPlugin.html) | Plugin to register |


#### destroy (removeView opt, stageOptions opt)
Destroys the application object.

##### Arguments

| Name | Type | Attribute | Description |
| --- | --- | --- | --- |
| `removeView` | Boolean | &lt;optional&gt; | Whether to remove the view |
| `stageOptions` | Boolean \| Object | &lt;optional&gt; | Options for stage destruction |


#### render ()
Renders the current stage.


#### resize ()
Resizes the rendering area to match the target specified in the `resizeTo` property.


#### start ()
Starts rendering.


#### stop ()
Stops rendering.
