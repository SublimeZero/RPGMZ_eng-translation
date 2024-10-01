[Class Tree](index.md)

# Class: Bitmap

The basic object representing an image.

Uses `baseTexture` for image data storage ([PIXI.BaseTexture](https://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html))<br />
Uses `image` for loading images ([Image(HTMLImageElement)](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement))<br />
Uses `canvas` for drawing images ([HTMLCanvasElement](https://developer.mozilla.org/ja/docs/Web/API/HTMLCanvasElement)). This class integrates these functionalities.

If created with `new Bitmap(0, 0)`, the `canvas` will not be generated. Therefore, to use drawing-related methods, at a minimum, you need to create it with `new Bitmap(1, 1)`.

It also has the functionality to decrypt encrypted image files.

Changes were made in v1.1.1, v1.2.0, v1.4.0, and v1.5.0.

Related Classes: [Graphics](Graphics.md), [ImageManager](ImageManager.md), [Game_Screen](Game_Screen.md), [Sprite](Sprite.md), [Game_Picture](Game_Picture.md)

### new Bitmap (width, height)
#### Arguments

| Name   | Type          | Description             |
| ------ | ------------- | ----------------------- |
| `width` | [Number](Number.md) | Width of the image (pixels) |
| `height` | [Number](Number.md) | Height of the image (pixels) |


### Properties

| Identifier      | Type                       | Description                                     |
| --------------- | -------------------------- | ----------------------------------------------- |
| `fontFace`     | [String](String.md)       | Font name (default: "sans-serif")              |
| `fontSize`     | [Number](Number.md)       | Font size (default: 16 pixels)                 |
| `fontItalic`   | Boolean                   | Is italic (default: false)                      |
| `fontBold`     | Boolean                   | Is bold (default: false)                        |
| `textColor`    | [MV.CssColor](MV.CssColor.md) | Text color (default: "#ffffff")                |
| `outlineColor` | [MV.CssColor](MV.CssColor.md) | Outline color (default: "rgba(0, 0, 0, 0.5)") |
| `outlineWidth` | [Number](Number.md)       | Outline width (default: 3)                      |
| `url`          | [String](String.md)       | [read-only] URL of the image file              |
| `baseTexture`  | [PIXI.BaseTexture](https://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html) | [read-only] Base texture for image data storage |
| `canvas`       | [HTMLCanvasElement](https://developer.mozilla.org/ja/docs/Web/API/HTMLCanvasElement) | [read-only] `<canvas>` element for image manipulation |
| `context`      | [CanvasRenderingContext2D](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D) | [read-only] 2D rendering context                 |
| `image`        | [Image(HTMLImageElement)](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement) | **@MZ** [read-only] `<img>` element for file loading management |
| `width`        | [Number](Number.md)       | [read-only] Width of the image (pixels)       |
| `height`       | [Number](Number.md)       | [read-only] Height of the image (pixels)      |
| `rect`         | [Rectangle](Rectangle.md)  | [read-only] Rectangular area of the image     |
| `smooth`       | Boolean                   | Apply smooth scaling (blurring) (default: true) |
| `paintOpacity` | [Number](Number.md)       | Opacity during drawing (0 to 255) (default: 255) |
| `_loadingState` | [String](String.md)      | [Loading State](#loading-state)                |
| `_loadListeners` | [Array](Array.md).&lt;Function&gt; | Array of load listeners                        |
| `_smooth`      | Boolean                   |                                               |
| `_paintOpacity` | [Number](Number.md)      |                                               |
| `_url`         | [String](String.md)       |                                               |
| `_baseTexture` | [PIXI.BaseTexture](https://pixijs.download/v5.3.12/docs/PIXI.BaseTexture.html) |                                               |
| `_context`     | [CanvasRenderingContext2D](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D) |                                               |
| `_canvas`      | [HTMLCanvasElement](https://developer.mozilla.org/ja/docs/Web/API/HTMLCanvasElement)  |                                               |
| `_image`       | **@MZ** [Image(HTMLImageElement)](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement) |                                               |

#### Loading State

| String   | Description                  |
| -------- | ---------------------------- |
| "none"   | No image                    |
| "loading" | **@MZ** Loading image       |
| "loaded" | Image is ready for use      |
| "error"  | Error occurred              |

The states "pending", "purged", "requesting", "requestCompleted", "decrypting", and "decryptCompleted" have been deprecated and consolidated into "loading".

### Deprecated MV Properties
`cacheEntry`


### Methods

#### (static) load (url) → {[Bitmap](Bitmap.md)}
Loads an image file and returns a Bitmap object.<br />
In this case, the `canvas` will not be generated until it is needed.

##### Arguments

| Name | Type          | Description                      |
| ---- | ------------- | -------------------------------- |
| `url` | [String](String.md) | URL of the image file          |


#### (static) snap (stage) → {[Bitmap](Bitmap.md)}
Returns a Bitmap object that contains a snapshot of the specified Stage's game screen.

##### Arguments

| Name   | Type      | Description          |
| ------ | --------- | -------------------- |
| `stage` | [Stage](Stage.md) | Stage object      |


#### _drawTextBody (text, tx, ty, maxWidth)
Draws the main body of the text.

##### Arguments

| Name   | Type          | Description                |
| ------ | ------------- | -------------------------- |
| `text` | [String](String.md) | String                    |
| `tx`   | [Number](Number.md) | X coordinate (pixels)     |
| `ty`   | [Number](Number.md) | Y coordinate (pixels)     |
| `maxWidth` | [Number](Number.md) | Maximum width (pixels)   |


#### _drawTextOutline (text, tx, ty, maxWidth)
Draws the outline of the text.

##### Arguments

| Name   | Type          | Description                |
| ------ | ------------- | -------------------------- |
| `text` | [String](String.md) | String                    |
| `tx`   | [Number](Number.md) | X coordinate (pixels)     |
| `ty`   | [Number](Number.md) | Y coordinate (pixels)     |
| `maxWidth` | [Number](Number.md) | Maximum width (pixels)   |


#### _makeFontNameText () → {[String](String.md)}
Returns the font name as a string.


#### _onError ()
Handler called on error.


#### _callLoadListeners ()
Calls all load listeners.


#### _createBaseTexture (source)
**@MZ** Generates the base texture from a canvas or image element.

##### Arguments

| Name   | Type  | Description                       |
| ------ | ----- | --------------------------------- |
| `source` | [HTMLCanvasElement](https://developer.mozilla.org/ja/docs/Web/API/HTMLCanvasElement) \| [Image(HTMLImageElement)](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement) | Data that will be the texture source |


#### _createCanvas (width, height)
**@MZ** Creates a canvas.

##### Arguments

| Name   | Type          | Description             |
| ------ | ------------- | ----------------------- |
| `width` | [Number](Number.md) | Width (pixels)        |
| `height` | [Number](Number.md) | Height (pixels)      |


#### _destroyCanvas ()
**@MZ** Disposes of the canvas.


#### _ensureCanvas ()
**@MZ** Secures the canvas.


#### _onLoad ()
Handler called at the end of loading.


#### _onXhrLoad (xhr)
**@MZ** Handler called when the XMLHttpRequest loading ends.

##### Arguments

| Name | Type  | Description                |
| ---- | ----- | -------------------------- |
| `xhr` | [XMLHttpRequest](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest) | XML HTTP request       |


#### _startLoading ()
**@MZ** Starts the loading process.


#### _startDecrypting ()
**@MZ** Starts the decryption process.


#### _updateScaleMode ()
**@MZ** Updates the scaling mode (smoothing).


#### addLoadListener (listener)
Adds a listener function that will be called when the image is loaded.

##### Arguments

| Name      | Type     | Description         |
|-----------|----------|---------------------|
| `listener`| Function | Callback function    |


#### adjustTone (r, g, b)
Changes the color tone of the image to the specified RGB.

##### Arguments

| Name | Type          | Description               |
|------|---------------|---------------------------|
| `r`  | [Number](Number.md) | Red (-255 to 255)       |
| `g`  | [Number](Number.md) | Green (-255 to 255)     |
| `b`  | [Number](Number.md) | Blue (-255 to 255)      |


#### blt (source, sx, sy, sw, sh, dx, dy, dw opt, dh opt)
Transfers an image block from the specified source image.

##### Arguments

| Identifier | Type          | Characteristics | Description                     |
|------------|---------------|-----------------|---------------------------------|
| `source`   | [Bitmap](Bitmap.md) |                 | Source image                   |
| `sx`       | [Number](Number.md) |                 | Source x-coordinate (pixels)   |
| `sy`       | [Number](Number.md) |                 | Source y-coordinate (pixels)   |
| `sw`       | [Number](Number.md) |                 | Source image width (pixels)    |
| `sh`       | [Number](Number.md) |                 | Source image height (pixels)   |
| `dx`       | [Number](Number.md) |                 | Destination x-coordinate (pixels) |
| `dy`       | [Number](Number.md) |                 | Destination y-coordinate (pixels) |
| `dw`       | [Number](Number.md) | <optional>     | Destination image width (default: sw) |
| `dh`       | [Number](Number.md) | <optional>     | Destination image height (default: sh) |


#### bltImage (source, sx, sy, sw, sh, dx, dy, dw opt, dh opt)
Transfers an image block from the specified source image, but does not draw it on the canvas.

##### Arguments

| Identifier | Type          | Characteristics | Description                     |
|------------|---------------|-----------------|---------------------------------|
| `source`   | [Bitmap](Bitmap.md) |                 | Source image                   |
| `sx`       | [Number](Number.md) |                 | Source x-coordinate (pixels)   |
| `sy`       | [Number](Number.md) |                 | Source y-coordinate (pixels)   |
| `sw`       | [Number](Number.md) |                 | Source image width (pixels)    |
| `sh`       | [Number](Number.md) |                 | Source image height (pixels)   |
| `dx`       | [Number](Number.md) |                 | Destination x-coordinate (pixels) |
| `dy`       | [Number](Number.md) |                 | Destination y-coordinate (pixels) |
| `dw`       | [Number](Number.md) | <optional>     | Destination image width (default: sw) |
| `dh`       | [Number](Number.md) | <optional>     | Destination image height (default: sh) |


#### blur ()
Applies a blur effect.


#### checkDirty ()
Checks if the texture is dirty.


#### clear ()
Deletes the image.  
If a `Bitmap` is already set in the `bitmap` property of [Sprite](Sprite.md) and assigning a new `Bitmap` could be memory inefficient, it's advisable to check if the `bitmap` property has a value and then delete it with this method.

##### Example
```js
if( sprite.bitmap ) {
    sprite.bitmap.clear();
}else{
    sprite.bitmap = new Bitmap(1, 1);
}
```

#### clearRect (x, y, width, height)
Deletes the specified rectangular area.

##### Arguments

| Name    | Type          | Description                    |
|---------|---------------|--------------------------------|
| `x`     | [Number](Number.md) | Left x-coordinate (pixels)     |
| `y`     | [Number](Number.md) | Top y-coordinate (pixels)      |
| `width` | [Number](Number.md) | Rectangle width (pixels)       |
| `height`| [Number](Number.md) | Rectangle height (pixels)      |


#### decode ()
Decodes the image.


#### destroy ()
Destroys the object.


#### drawCircle (x, y, radius, color)
Draws a circle.

##### Arguments

| Name     | Type          | Description                    |
|----------|---------------|--------------------------------|
| `x`      | [Number](Number.md) | Center x-coordinate (pixels)   |
| `y`      | [Number](Number.md) | Center y-coordinate (pixels)   |
| `radius` | [Number](Number.md) | Radius (pixels)                |
| `color`  | [MV.CssColor](MV.CssColor.md) | Color                         |


#### drawText (text, x, y, maxWidth, lineHeight, align)
Draws text.

##### Arguments

| Name      | Type          | Description                       |
|-----------|---------------|-----------------------------------|
| `text`    | [String](String.md) | Text to draw                   |
| `x`       | [Number](Number.md) | Left x-coordinate (pixels)     |
| `y`       | [Number](Number.md) | Top y-coordinate (pixels)      |
| `maxWidth`| [Number](Number.md) | Maximum allowable width (pixels)|
| `lineHeight`| [Number](Number.md) | Line height (pixels)          |
| `align`   | [String](String.md) | Text alignment (left, center, right) |


#### fillAll (color)
Fills the entire area with the specified color.

##### Arguments

| Name   | Type                     | Description               |
|--------|--------------------------|---------------------------|
| `color`| [MV.CssColor](MV.CssColor.md) | Color (CSS string)      |


#### fillRect (x, y, width, height, color)
Fills the rectangular area with the specified color.

##### Arguments

| Name    | Type          | Description                    |
|---------|---------------|--------------------------------|
| `x`     | [Number](Number.md) | Left x-coordinate (pixels)     |
| `y`     | [Number](Number.md) | Top y-coordinate (pixels)      |
| `width` | [Number](Number.md) | Rectangle width (pixels)       |
| `height`| [Number](Number.md) | Rectangle height (pixels)      |
| `color` | [MV.CssColor](MV.CssColor.md) | Color (CSS string)       |


#### getAlphaPixel (x, y) → {[Number](Number.md)}
Returns the opacity (0-255) at the specified position.

##### Arguments

| Name | Type          | Description                    |
|------|---------------|--------------------------------|
| `x`  | [Number](Number.md) | x-coordinate (pixels)        |
| `y`  | [Number](Number.md) | y-coordinate (pixels)        |


#### getPixel (x, y) → {[MV.CssColor](MV.CssColor.md)}
Returns the color of the pixel at the specified position (in #rrggbb format).

##### Arguments

| Name | Type          | Description                    |
|------|---------------|--------------------------------|
| `x`  | [Number](Number.md) | x-coordinate (pixels)        |
| `y`  | [Number](Number.md) | y-coordinate (pixels)        |


#### gradientFillRect (x, y, width, height, color1, color2, vertical)
Draws a rectangle with a gradient.

##### Arguments

| Name     | Type                     | Description                |
|----------|--------------------------|----------------------------|
| `x`      | [Number](Number.md) | Left x-coordinate (pixels)   |
| `y`      | [Number](Number.md) | Top y-coordinate (pixels)    |
| `width`  | [Number](Number.md) | Rectangle width (pixels)     |
| `height` | [Number](Number.md) | Rectangle height (pixels)    |
| `color1` | [MV.CssColor](MV.CssColor.md) | Start color           |
| `color2` | [MV.CssColor](MV.CssColor.md) | End color             |
| `vertical` | Boolean             | Whether to apply the gradient vertically |


#### initialize (width, height)
Initialization when creating the object.

##### Arguments

| Name    | Type          | Description                    |
|---------|---------------|--------------------------------|
| `width` | [Number](Number.md) | Width (pixels)               |
| `height`| [Number](Number.md) | Height (pixels)              |


#### isError () → {Boolean}
Checks if an error occurred during loading.


#### isReady () → {Boolean}
Checks if the image is ready to be drawn.


#### isRequestOnly () → {Boolean}
Checks if it's just a request.


#### isRequestReady () → {Boolean}
Checks if the request is complete.


#### measureTextWidth (text) → {[Number](Number.md)}
Returns the width of the specified string.  
**(v1.1.1)** The return value is passed through ceil() to make it an integer (to reduce text blurriness).

##### Arguments

| Name | Type          | Description                     |
|------|---------------|---------------------------------|
| `text`| [String](String.md) | String to measure width       |


#### retry ()
**@MZ** Retries image loading.


#### resize (width, height)
Resizes the image to the specified size.  
Make sure to allocate the drawing area before various drawing methods like [blt()](#blt-source-sx-sy-sw-sh-dx-dy-dw-opt-dh-opt).

##### Arguments

| Name    | Type          | Description                    |
|---------|---------------|--------------------------------|
| `width` | [Number](Number.md) | Width (pixels)               |
| `height`| [Number](Number.md) | Height (pixels)              |


#### rotateHue (offset)
Changes the hue by the specified amount.

##### Arguments

| Name    | Type          | Description                    |
|---------|---------------|--------------------------------|
| `offset`| [Number](Number.md) | Hue change amount (360 degrees) |


#### strokeRect (x, y, width, height, color) 
**@MZ** Draws a rectangle outline.

##### Arguments

| Name    | Type          | Description                    |
|---------|---------------|--------------------------------|
| `x`     | [Number](Number.md) | x-coordinate (pixels)         |
| `y`     | [Number](Number.md) | y-coordinate (pixels)         |
| `width` | [Number](Number.md) | Rectangle width (pixels)      |
| `height`| [Number](Number.md) | Rectangle height (pixels)     |
| `color` | [MV.CssColor](MV.CssColor.md) | Color                      |


### Deprecated MV Methods
[static] request (url)  
_setDirty (), startRequest (), touch ()
