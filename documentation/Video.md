[Class Tree](index.md)

# Class: Video
**@MZ** A static class for processing videos.

The video functionality that was included in [Graphics](Graphics.md) in MV has been made independent.

Related Classes: [Bitmap](Bitmap.md), [ImageManager](ImageManager.md), [SceneManager](SceneManager.md), [Game_Screen](Game_Screen.md), [Window](Window.md)

---

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_element` | HTMLElement | [static] HTMLVideoElement |
| `_loading` | Boolean | [static] Whether it is loading |
| `_volume` | [Number](Number.md) | [static] Volume (default: 1) |

---

### Methods

#### (static) _createElement ()
Generates an HTMLVideoElement.

---

#### (static) _isVisible () → {Boolean}
Checks if the video is visible.

---

#### (static) _onError ()
Handler for when playback ends.

---

#### (static) _onError ()
Handler for when an error occurs.

---

#### (static) _onLoad ()
Handler for when loading is complete.

---

#### (static) _onUserGesture ()
Handler for when user input (keydown, mousedown, touchend) occurs.

---

#### (static) _setupEventHandlers ()
Prepares the event handlers.

---

#### (static) _updateVisibility (videoVisible)
Changes to the specified visibility state.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `videoVisible` | Boolean | Whether to display it |

---

#### (static) initialize (width, height) → {Boolean}
Initializes the video.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `width` | [Number](Number.md) | Width of the video (in pixels) |
| `height` | [Number](Number.md) | Height of the video (in pixels) |

---

#### (static) isPlaying () → {Boolean}
Checks if the video is playing.

---

#### (static) play ()
Plays the video.

---

#### (static) resize (width, height)
Resizes the video.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `width` | [Number](Number.md) | Width of the video (in pixels) |
| `height` | [Number](Number.md) | Height of the video (in pixels) |

---

#### (static) setVolume (volume)
Sets to the specified volume.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `volume` | [Number](Number.md) | Volume (0-1) |
