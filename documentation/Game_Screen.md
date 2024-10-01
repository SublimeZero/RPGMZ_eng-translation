[Class Tree](index.md)

# Class: Game_Screen

| Global Variables | Save Data |
| --- | --- |
| [$gameScreen](global.md#gamescreen-game_screen) | Saved |

Class responsible for event command behaviors related to the [screen].

Related classes: [Game_Map](Game_Map.md), [Game_Picture](Game_Picture.md), [Sprite_Picture](Sprite_Picture.md), [Scene_Map](Scene_Map.md), [Scene_Battle](Scene_Battle.md), [Graphics](Graphics.md), [ImageManager](ImageManager.md)

### new Game_Screen ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_shake` | [Number](Number.md) | Distance shifted by [shake] |
| `_shakePower` | [Number](Number.md) | Strength of [shake] |
| `_shakeSpeed` | [Number](Number.md) | Speed of [shake] |
| `_shakeDuration` | [Number](Number.md) | Duration of [shake] (frames) |
| `_shakeDirection` | [Number](Number.md) | Direction of [shake] |
| `_zoomX` | [Number](Number.md) | x-coordinate of the zoom point (pixels) |
| `_zoomY` | [Number](Number.md) | y-coordinate of the zoom point (pixels) |
| `_zoomScale` | [Number](Number.md) | Zoom rate (1 for 100%) |
| `_zoomScaleTarget` | [Number](Number.md) | Target zoom rate |
| `_zoomDuration` | [Number](Number.md) | Duration of zoom |
| `_weatherType` | [String](String.md) | [Weather] type |
| `_weatherPower` | [Number](Number.md) | [Weather] strength (1~9) |
| `_weatherPowerTarget` | [Number](Number.md) | Target [Weather] strength (1~9) |
| `_weatherDuration` | [Number](Number.md) | Duration of [Weather] (frames) |
| `_brightness` | [Number](Number.md) | Brightness |
| `_fadeOutDuration` | [Number](Number.md) | Duration of fade out (frames) |
| `_fadeInDuration` | [Number](Number.md) | Duration of fade in (frames) |
| `_tone` |  [MV.Tone](MV.Tone.md)  | [Tone] |
| `_toneTarget` |  [MV.Tone](MV.Tone.md)  | Target tone |
| `_toneDuration` | [Number](Number.md) | Duration of tone (frames) |
| `_flashColor` | [Array](Array.md).&lt;[Number](Number.md)&gt; | Color of [flash] (0~0xFFFFFF) |
| `_flashDuration` | [Number](Number.md) | Duration of [flash] (frames) |
| `_pictures` | [Array](Array.md).&lt;[Game_Picture](Game_Picture.md)&gt; | Array of added [pictures] |

### Methods

#### brightness () → {[Number](Number.md)}
Returns the brightness of the screen.

#### changeWeather (type, power, duration)
Changes to the specified [weather].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `type` | [String](String.md) | [Weather] type |
| `power` | [Number](Number.md) | [Weather] strength |
| `duration` | [Number](Number.md) | Duration of [Weather] (frames) |

#### clear ()
Clears.

#### clearFade ()
Clears [fade] processing.

#### clearFlash ()
Clears [flash] processing.

#### clearPictures ()
Clears added [pictures].

#### clearShake ()
Clears [shake] processing.

#### clearTone ()
Clears [tone] processing.

#### clearWeather ()
Clears [weather] processing.

#### clearZoom ()
Clears zoom processing.

#### eraseBattlePictures ()
Clears battle pictures.

#### erasePicture (pictureId)
Clears the specified [picture].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `pictureId` | [Number](Number.md) | Picture ID |

#### flashColor () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns the color of the [flash].

#### initialize ()
Initialization upon object creation.

#### maxPictures () → {[Number](Number.md)}
Returns the maximum number of pictures.

#### movePicture (pictureId, origin, x, y, scaleX, scaleY, opacity, blendMode, duration, easingType)
Moves the specified [picture].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `pictureId` | [Number](Number.md) | Picture ID |
| `origin` | [Number](Number.md) | [[Origin]](Game_Picture.md#origin) |
| `x` | [Number](Number.md) | x-coordinate (pixels) |
| `y` | [Number](Number.md) | y-coordinate (pixels) |
| `scaleX` | [Number](Number.md) | Zoom rate [width] |
| `scaleY` | [Number](Number.md) | Zoom rate [height] |
| `opacity` | [Number](Number.md) | [Opacity] |
| `blendMode` | [Number](Number.md) | [[Blend Mode]](Sprite.md#blend-mode) |
| `duration` | [Number](Number.md) | Duration |
| `easingType` | [Number](Number.md) | **@MZ** [Easing Type](Game_Picture.md#easing-type) |

#### onBattleStart ()
Handler called at the start of the battle scene.

#### picture (pictureId) → {[Game_Picture](Game_Picture.md)}
Returns the specified picture.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `pictureId` | [Number](Number.md) | Picture ID |

#### realPictureId (pictureId) → {[Number](Number.md)}
Returns the common picture ID for normal scenes and battle scenes.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `pictureId` | [Number](Number.md) | Picture ID |

#### rotatePicture (pictureId, speed)
Rotates the specified [picture].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `pictureId` | [Number](Number.md) | Picture ID |
| `speed` | [Number](Number.md) | Speed |


#### setZoom (x, y, scale)
Sets the specified zoom.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X-coordinate of the zoom point (pixels) |
| `y` | [Number](Number.md) | Y-coordinate of the zoom point (pixels) |
| `scale` | [Number](Number.md) | Zoom scale (1 for 100%) |


#### shake () → {[Number](Number.md)}
Returns the distance shifted by the [shake].


#### showPicture (pictureId, name, origin, x, y, scaleX, scaleY, opacity, blendMode)
Displays the specified [picture].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `pictureId` | [Number](Number.md) | Picture ID |
| `name` | [String](String.md) | Name |
| `origin` | [Number](Number.md) | [[Origin]](Game_Picture.md#origin) |
| `x` | [Number](Number.md) | X-coordinate (pixels) |
| `y` | [Number](Number.md) | Y-coordinate (pixels) |
| `scaleX` | [Number](Number.md) | Zoom scale [width] |
| `scaleY` | [Number](Number.md) | Zoom scale [height] |
| `opacity` | [Number](Number.md) | [Opacity] |
| `blendMode` | [Number](Number.md) | [[Blend Mode]](Sprite.md#blend-mode) |


#### startFadeIn (duration)
Starts the specified [fade-in].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Duration (frames) |


#### startFadeOut (duration)
Starts the specified [fade-out].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Duration (frames) |


#### startFlash (color, duration)
Starts the specified [flash].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `color` | [Array](Array.md).&lt;[Number](Number.md)&gt; |  |
| `duration` | [Number](Number.md) | Duration (frames) |


#### startFlashForDamage ()
Starts the damage flash.


#### startShake (power, speed, duration)
Starts the specified [shake].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `power` | [Number](Number.md) | [Shake] strength |
| `speed` | [Number](Number.md) | [Shake] speed |
| `duration` | [Number](Number.md) | Duration (frames) |


#### startTint (tone, duration)
Starts the specified [tone] effect.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `tone` | [MV.Tone](MV.Tone.md) | [Tone] |
| `duration` | [Number](Number.md) | Duration (frames) |


#### startZoom (x, y, scale, duration)
Starts the specified zoom.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X-coordinate of the zoom point (pixels) |
| `y` | [Number](Number.md) | Y-coordinate of the zoom point (pixels) |
| `scale` | [Number](Number.md) | Zoom scale (1 for 100%) |
| `duration` | [Number](Number.md) | Duration (frames) |


#### tintPicture (pictureId, tone, duration)
Adds a [tone] effect to the specified picture.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `pictureId` | [Number](Number.md) | Picture ID |
| `tone` | [MV.Tone](MV.Tone.md) | [Tone] |
| `duration` | [Number](Number.md) | Duration (frames) |


#### tone () → {[MV.Tone](MV.Tone.md)}
Returns the [tone].


#### update ()
Updates every frame.


#### updateFadeIn ()
Updates the [fade-in].


#### updateFadeOut ()
Updates the [fade-out].


#### updateFlash ()
Updates the [flash].


#### updatePictures ()
Updates the [pictures].


#### updateShake ()
Updates the [shake].


#### updateTone ()
Updates the [tone].


#### updateWeather ()
Updates the [weather].


#### updateZoom ()
Updates the zoom.


#### weatherPower () → {[Number](Number.md)}
Returns the [weather] strength.


#### weatherType () → {[String](String.md)}
Returns the [weather] type.


#### zoomScale () → {[Number](Number.md)}
Returns the zoom scale.


#### zoomX () → {[Number](Number.md)}
Returns the X-coordinate of the zoom point (pixels).


#### zoomY () → {[Number](Number.md)}
Returns the Y-coordinate of the zoom point (pixels).
