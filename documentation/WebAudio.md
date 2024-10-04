[Class Tree](index.md)

# Class: WebAudio

Audio data using the Web Audio API.

There are many static methods, making it useful as a utility.

Changes were made in v1.0.2.

Related Classes: [CacheEntry](CacheEntry.md), [SoundManager](SoundManager.md), [Html5Audio](Html5Audio.md), [RPG.AudioFile](RPG.AudioFile.md)

---

### new WebAudio (url)

#### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `url` | [String](String.md) | The URL of the audio file |

---

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_context` | AudioContext | [static] |
| `_masterGainNode` | GainNode | [static] |
| `url` | [String](String.md) | [read-only] URL of the audio file |
| `volume` | [Number](Number.md) | [Volume] |
| `pitch` | [Number](Number.md) | [Pitch] |
| `pan` | [Number](Number.md) | [Pan] |
| `_buffers` | [Array](Array.md) |  |
| `_data` |  |  |
| `_decoder` |  |  |
| `_endTimer` |  |  |
| `_fetchedData` | [Array](Array.md) |  |
| `_fetchedSize` | [Number](Number.md) |  |
| `_gainNode` |  |  |
| `_isError` | Boolean |  |
| `_isLoaded` | Boolean |  |
| `_isPlaying` | Boolean |  |
| `_lastUpdateTime` | [Number](Number.md) |  |
| `_loadListeners` | [Array](Array.md) |  |
| `_loop` | [Number](Number.md) |  |
| `_loopLength` | [Number](Number.md) |  |
| `_loopLengthTime` | [Number](Number.md) |  |
| `_loopStart` | [Number](Number.md) |  |
| `_loopStartTime` | [Number](Number.md) |  |
| `_pan` | [Number](Number.md) |  |
| `_pannerNode` |  |  |
| `_pitch` | [Number](Number.md) |  |
| `_sampleRate` | [Number](Number.md) |  |
| `_sourceNodes` | [Array](Array.md) |  |
| `_startTime` | [Number](Number.md) |  |
| `_stopListeners` | [Array](Array.md) |  |
| `_totalTime` | [Number](Number.md) |  |
| `_url` | [String](String.md) |  |
| `_volume` | [Number](Number.md) |  |

---

### Deprecated MV Properties

`_initialized`, `_unlocked`

---

### Methods

#### (static) _createContext ()
Generates the context.

---

#### (static) _createMasterGainNode ()
Generates the master gain node.

---

#### (static) _currentTime () → {Number}
**@MZ** Returns the current time.

---

#### (static) _fadeIn (duration)
Fade in.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Fade duration (in seconds) |

---

#### (static) _fadeOut (duration)
Fade out.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Fade duration (in seconds) |

---

#### (static) _onHide ()
Handler when the game is hidden.

---

#### (static) _onShow ()
Handler when the game is shown.

---

#### (static) _onUserGesture ()
**@MZ** Handler when user input occurs.

---

#### (static) _onVisibilityChange ()
Handler when the visibility state changes.

---

#### (static) _resetVolume ()
**@MZ** Resets the volume.

---

#### (static) _setupEventHandlers ()
Prepares event handlers.

---

#### (static) _shouldMuteOnHide () → {Boolean}
Should the sound be muted when hidden?

---

#### (static) initialize ()→ {Boolean}
Initializes the audio functionality and returns whether it is ready.

---

#### (static) setMasterVolume (value)
Sets the master volume.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `value` | [Number](Number.md) | Volume (0 to 1) |

---

#### _createEndTimer ()
Generates the end timer.

---

#### _onLoad ()
Handler when the audio file loading is complete.

---

#### _onXhrLoad (xhr)
Handler for XMLHttpRequest.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `xhr` | XMLHttpRequest |  |

---

#### _readFourCharacters (view, index) → {String}
Extracts 4 characters from the specified position in the view.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `view` | Uint8Array |  |
| `index` | [Number](Number.md) | Extraction position |

---

#### _readLoopComments (arrayBuffer)
Reads loop comments.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `arrayBuffer` | Uint8Array |  |

---

#### _readMetaData (view, index, size)
Reads metadata.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `view` | Uint8Array |  |
| `index` | [Number](Number.md) |  |
| `size` | [Number](Number.md) |  |

---

#### _removeEndTimer ()
Removes the end timer.

---

#### _removeNodes ()
Removes nodes.

---

#### _startPlaying (offset)
Starts playback.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `offset` | [Number](Number.md) | Start (in seconds) |

---

#### _updatePanner ()
Updates the pan.

---

#### destroy ()
**@MZ** Disposes of the audio.

---

#### fadeIn (duration)
Fade in.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Fade duration (in seconds) |

---

#### fadeOut (duration)
Fade out.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Fade duration (in seconds) |

---

#### addLoadListener (listener)
Sets the handler when the audio file loading is complete.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `listener` | Function | Callback function |

---

#### addStopListener (listener)
Sets the handler when the audio file stops.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `listener` | Function | Callback function |

---

#### clear ()
Clears the audio data (initialization).

---

#### initialize (url)
Initialization when the object is created.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `url` | [String](String.md) | Path to the audio file |

---

#### isError () → {Boolean}
Whether a loading error occurred.

---

#### isPlaying () → {Boolean}
Whether the audio is currently playing.

---

#### isReady () → {Boolean}
Whether it is ready to play.

---

#### play (loop, offset)
Plays the audio.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `loop` | Boolean | Whether to loop |
| `offset` | [Number](Number.md) | Start position for playback (in seconds) |

---

#### seek () → {Number}
Returns the generation position (in seconds).

---

#### stop ()
Stops the audio.

---

### Deprecated MV Methods

_connectNodes (), _createNodes (), _detectCodecs (), _load (url), _onTouchStart (), _readBigEndian (array, index), _readLittleEndian (array, index), _readMp4 (array), _readOgg (array), canPlayM4a (), canPlayOgg ()
