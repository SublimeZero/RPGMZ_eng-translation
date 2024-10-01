# Class: Graphics
A static class for handling image processing.<br />
In addition to regular screens, it also handles loading and error displays.

It has a `PIXI.Application` in the `app` property.<br />
`PIXI.Application` is an important object related to image display that contains the root container, renderer, ticker, and more.<br />
By the way, the root container's `Graphics.app.stage` is the same value as `SceneManager._scene`.

It has an EffekseerContext in the `effekseer` property.<br />
This is also an important object related to effect displays.

The window size is determined by the `package.json` file located directly under the project, and is reconfigured according to the width and height specified there.<br />
Therefore, keeping the values in sync with `package.json` can prevent the window size from changing and causing flickering upon game startup.

Due to the unification of rendering to WebGL, and the migration of functions to classes like [Utils](Utils.md#canUseCssFontLoading) and [Video](Video.md), many properties and methods that existed in MV have been deprecated.

Changes were made in v1.2.0 and v1.6.0.

Related Classes: [Bitmap](Bitmap.md), [ImageManager](ImageManager.md), [SceneManager](SceneManager.md), [Game_Screen](Game_Screen.md), [Window](Window.md), [RPG.System](RPG.System.md), [RPG.System.Advanced](RPG.System.Advanced.md)

### Properties
Properties starting with BLEND_ are constants for specifying image [blending modes](Sprite.md#合成方法) that are the same as PIXI.blendModes.

| Identifier | Type | Description |
| --- | --- | --- |
| `app` | [PIXI.Application](PIXI.Application.md) | **@MZ**[static][read-only] PIXI Application |
| `effekseer` | EffekseerContext  | **@MZ**[static][read-only] Effekseer context |
| `frameCount` | [Number](Number.md) | [static] Frame count |
| `width` | [Number](Number.md) | [static] Width of the game screen (default: 816 pixels) |
| `height` | [Number](Number.md) | [static] Height of the game screen (default: 624 pixels) |
| `boxWidth` | [Number](Number.md) | [static] Width of the UI area (default: 808 pixels) |
| `boxHeight` | [Number](Number.md) | [static] Height of the UI area (default: 616 pixels) |
| `defaultScale` | [Number](Number.md) | [static] Magnification (renamed from scale) |
| `_app` | [PIXI.Application](PIXI.Application.md) | **@MZ**[static] |
| `_width` | [Number](Number.md) | [static] |
| `_height` | [Number](Number.md) | [static] |
| `_defaultScale` | [Number](Number.md) | [static] Magnification (renamed from _scale) |
| `_realScale` | [Number](Number.md) | [static] Actual magnification that fits the window |
| `_errorPrinter` | HTMLElement | [static] Error display p element |
| `_tickHandler` |  | **@MZ** [static]  |
| `_fpsCounter` |  | **@MZ** [static]  |
| `_loadingSpinner` |  | **@MZ** [static]  |
| `_effekseer` |  | **@MZ** [static]  |
| `_wasLoading` |  | **@MZ** [static]  |
| `_canvas` | HTMLCanvasElement | [static] Canvas element |
| `_renderer` | PIXI.SystemRenderer | [static] Renderer |
| `_stretchEnabled` | Boolean | [static] Whether the screen can be stretched |

### Deprecated MV Properties
[static]
`_cssFontLoading`, `_rendererType`, `_boxWidth`, `_boxHeight`, `_errorShowed`, `_video`, `_videoUnlocked`, `_videoLoading`, `_upperCanvas`, `_renderer`, `_fpsMeter`, `_modeBox`, `_skipCount`, `_maxSkip`, `_rendered`, `_loadingImage`, `_loadingCount`, `_fpsMeterToggled`, `_canUseDifferenceBlend`, `_canUseSaturationBlend`, `_hiddenCanvas`, `BLEND_ADD`, `BLEND_NORMAL`, `BLEND_MULTIPLY`, `BLEND_SCREEN`

### Methods

#### (static) _applyCanvasFilter ()
Apply canvas filters.


#### (static) _cancelFullScreen ()
Exit full screen.

#### (static) _canRender ()→ {Boolean}
**@MZ** Whether rendering is possible (stage is ready).

#### (static) _centerElement (element)
Center the specified element.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `element` | HTMLElement | HTML element |


#### (static) _clearCanvasFilter ()
**@MZ** Remove canvas filters.


#### (static) _createFPSCounter ()
**@MZ** Generate the FPS counter.


#### (static) _createLoadingSpinner ()
**@MZ** Generate the loading display.


#### (static) _createPixiApp ()
**@MZ** Generate the _app.


#### (static) _createAllElements ()
Generate all elements.


#### (static) _createCanvas ()
Generate the canvas.


#### (static) _createEffekseerContext ()
**@MZ** Generate the Effekseer context.


#### (static) _createErrorPrinter ()
Generate the error display element.


#### (static) _defaultStretchMode () → {Boolean}
Whether it is the default stretch mode.


#### (static) _disableContextMenu ()
Disable the context menu.


#### (static) _isFullScreen () → {Boolean}
Whether it is in full screen.


#### (static) _makeErrorHtml (name, message) → {[String](String.md)}
Generate and return an error string.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `name` | [String](String.md) | Error name |
| `message` | [String](String.md) | Message |


#### (static) _onKeyDown (event)
Handler called when a key is pressed.<br />
(Handles F2, F3, F4 keys)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `event` | KeyboardEvent | Keyboard event |


#### (static) _onWindowResize ()
Handler called when the window is resized.


#### (static) _onTick (deltaTime)
**@MZ** Handler called when advancing the FPS counter.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `deltaTime` | [Number](Number.md) | Unit time |


#### (static) _requestFullScreen ()
Request full screen.


#### (static) _setupEventHandlers ()
Prepare event handlers.


#### (static) _setupPixi ()
**@MZ** Prepare PIXI.


#### (static) _stretchWidth ()
**@MZ** Expand width.


#### (static) _stretchHeight ()
**@MZ** Expand height.


#### (static) _switchFPSCounter ()
**@MZ** Toggle the FPS counter.


#### (static) _switchFullScreen ()
Switch to full screen.


#### (static) _switchStretchMode ()
Toggle the stretch mode of the screen.


#### (static) _updateAllElements ()
Update all elements.


#### (static) _updateCanvas ()
Update the canvas.


#### (static) _updateErrorPrinter ()
Update the error display.


#### (static) _updateRealScale ()
Update the actual magnification.


#### (static) _updateVideo ()
Update the video.


#### (static) endLoading () → {Boolean}
Remove the "Now Loading" image and return whether the loading image is active.


#### (static) eraseError ()
**@MZ** Remove the display of loading errors.


#### (static) initialize (width opt, height opt, type opt) → {Boolean}
Initialize the image functionality and return `true` when complete.<br />
Typically, the `_screenWidth` and `_screenHeight` from [SceneManager](SceneManager.md) are used as arguments, so x:816 and y:624 are the default values.

##### Arguments

| Name | Type | Attributes | Description |
| --- | --- | --- | --- |
| `width` | [Number](Number.md) | &lt;optional&gt; | Width of the game screen (default: 800 pixels) |
| `height` | [Number](Number.md) | &lt;optional&gt; | Height of the game screen (default: 600 pixels) |
| `type` | [String](String.md) | &lt;optional&gt; | [Renderer type](Graphics.md#renderer-type) (default: auto) |


#### (static) isInsideCanvas (x, y) → {Boolean}
Check if the specified coordinates are inside the canvas.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x-coordinate (pixels) |
| `y` | [Number](Number.md) | y-coordinate (pixels) |


#### (static) pageToCanvasX (x) → {[Number](Number.md)}
Convert and return the x-coordinate within the page to the x-coordinate within the canvas.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x-coordinate within the page (pixels) |


#### (static) pageToCanvasY (y) → {[Number](Number.md)}
Convert and return the y-coordinate within the page to the y-coordinate within the canvas.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `y` | [Number](Number.md) | y-coordinate within the page (pixels) |


#### (static) printError (name, message)
Display an error.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `name` | [String](String.md) | Error name |
| `message` | [String](String.md) | Error message |


#### (static) resize (width, height)
**@MZ** Reset the size of the game screen.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `width` | [Number](Number.md) | Width of the game screen (default: 800 pixels) |
| `height` | [Number](Number.md) | Height of the game screen (default: 600 pixels) |


#### (static) setStage (stage)
**@MZ** Set the stage (root of drawable objects).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `stage` | [PIXI.Container](PIXI.Container.md) | Container to set to `PIXI.application.stage` |


#### (static) setTickHandler (handler)
**@MZ** Set the handler for tick events.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `handler` | Function | Handler to set |


#### (static) showRetryButton (retry)
**@MZ** Show the retry button and set the click handler.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `retry` | Function | Handler executed when the button is clicked |


#### (static) showScreen ()
**@MZ** Display the game screen.


#### (static) startGameLoop ()
**@MZ** Start the application loop.


#### (static) startLoading ()
Begin displaying the loading image.


#### (static) stopGameLoop ()
**@MZ** End the application loop.


### Deprecated MV Methods
[static]
_clearUpperCanvas (), _createFontLoader (name), _createFPSMeter (), _createGameFontLoader (), _createModeBox (), _createRenderer (), 
_createUpperCanvas (), _createVideo (), _disableTextSelection (), _isVideoVisible (), _modifyExistingElements (), _onTouchEnd (event), _onVideoEnd (), _onVideoError (), _onVideoLoad (),
_paintUpperCanvas (), _playVideo (src), _setupCssFontLoading (), _switchFPSMeter (), _testCanvasBlendModes (), _updateRenderer (), _updateUpperCanvas (),_updateVisibility (videoVisible), callGC (), canPlayVideoType (type), canUseCssFontLoading (), canUseDifferenceBlend (), canUseSaturationBlend (), eraseLoadingError (), hasWebGL (), hideFps (), isFontLoaded (name), isVideoPlaying (), isWebGL (), loadFont (name, url), playVideo (src), printLoadingError (url), render (stage), setLoadingImage (src), setVideoVolume (value), showFps (), tickEnd (), tickStart (), updateLoading ()
