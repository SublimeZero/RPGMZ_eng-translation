[Class Tree](index.md)

# Class: AudioManager
A static class that handles BGM, BGS, ME, and SE.

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `bgmVolume` | [Number](Number.md) | [static] BGM volume |
| `bgsVolume` | [Number](Number.md) | [static] BGS volume |
| `meVolume` | [Number](Number.md) | [static] ME volume |
| `seVolume` | [Number](Number.md) | [static] SE volume |
| `_bgmVolume` | [Number](Number.md) | [static] BGM volume |
| `_bgsVolume` | [Number](Number.md) | [static] BGS volume |
| `_meVolume` | [Number](Number.md) | [static] ME volume |
| `_seVolume` | [Number](Number.md) | [static] SE volume |
| `_currentBgm` | [MV.AudioParameters](MV.AudioParameters.md) | [static] Current BGM |
| `_currentBgs` | [MV.AudioParameters](MV.AudioParameters.md) | [static] Current BGS |
| `_bgmBuffer` | Html5AudioStatic \| [WebAudio](WebAudio.md) | [static] BGM buffer |
| `_bgsBuffer` | Html5AudioStatic \| [WebAudio](WebAudio.md) | [static] BGS buffer |
| `_meBuffer` | Html5AudioStatic \| [WebAudio](WebAudio.md) | [static] ME buffer |
| `_seBuffers` | [Array](Array.md).&lt;Html5AudioStatic \| [WebAudio](WebAudio.md)&gt; | [static] SE buffers |
| `_staticBuffers ` | [Array](Array.md).&lt;Html5AudioStatic \| [WebAudio](WebAudio.md)&gt; | [static] Static buffers |
| `_replayFadeTime` | [Number](Number.md) | [static] Replay fade time |
| `_path` | [String](String.md) | [static] Path to audio folder (default: "audio/") |
| | [String](String.md) | [static] URL |

### Deprecated MV Properties
`masterVolume`, `_blobUrl`

### Methods

#### (static) audioFileExt () → {[String](String.md)}
Audio file extensions (".ogg", ".m4a")

#### (static) checkErrors ()
Error checking.

#### (static) checkWebAudioError (webAudio)
Checks for errors in the specified WebAudio.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `webAudio` | [WebAudio](WebAudio.md) | Web audio |

#### (static) cleanupSe () 
**@MZ** Organizes SE.

#### (static) createBuffer () → {Html5AudioStatic|[WebAudio](WebAudio.md)}
Creates a buffer.

#### (static) fadeInBgm (duration)
Fades in BGM.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Duration of the fade |

#### (static) fadeInBgs (duration)
Fades in BGS.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Duration of the fade |

#### (static) fadeOutBgm (duration)
Fades out BGM.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Duration of the fade |

#### (static) fadeOutBgs (duration)
Fades out BGS.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Duration of the fade |

#### (static) fadeOutMe (duration)
Fades out ME.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `duration` | [Number](Number.md) | Duration of the fade |

#### (static) isCurrentBgm (bgm) → {Boolean}
Checks if the specified BGM is the current BGM.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `bgm` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) isCurrentBgs (bgs) → {Boolean}
Checks if the specified BGS is the current BGS.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `bgs` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) isStaticSe (se) → {Boolean}

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `se` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) loadStaticSe (se)
Loads SE.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `se` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) makeEmptyAudioObject () → {[MV.AudioParameters](MV.AudioParameters.md)}
Generates and returns an empty audio object.

#### (static) playBgm (bgm, pos opt)
Plays BGM.

##### Arguments

| Name | Type | Characteristics | Description |
| --- | --- | --- | --- |
| `bgm` | [MV.AudioParameters](MV.AudioParameters.md) |  | Audio object |
| `pos` | [Number](Number.md) | &lt;optional&gt; | Playback position |

#### (static) playBgs (bgs, pos opt)
Plays BGS.

##### Arguments

| Name | Type | Characteristics | Description |
| --- | --- | --- | --- |
| `bgs` | [MV.AudioParameters](MV.AudioParameters.md) |  | Audio object |
| `pos` | [Number](Number.md) | &lt;optional&gt; | Playback position |

#### (static) playMe (me)
Plays ME.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `me` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) playSe (se)
Plays SE.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `se` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) playStaticSe (se)
Plays static SE.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `se` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) replayBgm (bgm)
Replays BGM.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `bgm` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) replayBgs (bgs)
Replays BGS.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `bgs` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) saveBgm () → {[MV.AudioParameters](MV.AudioParameters.md)}
Saves the state of BGM.

#### (static) saveBgs () → {[MV.AudioParameters](MV.AudioParameters.md)}
Saves the state of BGS.

#### (static) shouldUseHtml5Audio () → {Boolean}
Checks if Html5Audio should be used.

#### (static) stopAll ()
Stops everything.

#### (static) stopBgm ()
Stops BGM.

#### (static) stopBgs ()
Stops BGS.

#### (static) stopMe ()
Stops ME.

#### (static) stopSe ()
Stops SE.

#### (static) updateBgmParameters (bgm)
Updates the parameters of BGM.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `bgm` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) updateBgsParameters (bgs)
Updates the parameters of BGS.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `bgs` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) updateBufferParameters (buffer, configVolume, audio)
Updates the parameters of the buffer.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `buffer` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |
| `configVolume` | [Number](Number.md) |  |
| `audio` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) updateCurrentBgm (bgm, pos)
Updates the current BGM.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `bgm` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |
| `pos` | [Number](Number.md) | Playback position |

#### (static) updateCurrentBgs (bgs, pos)
Updates the current BGS.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `bgs` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |
| `pos` | [Number](Number.md) | Playback position |

#### (static) updateMeParameters (me)
Updates the parameters of ME.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `me` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |

#### (static) updateSeParameters (buffer, se)
Updates the parameters of SE.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `buffer` | [MV.AudioParameters](MV.AudioParameters.md) | Audio object |
| `se` | [MV.AudioParameters](MV.AudioParameters.md) |  |

### Deprecated MV Methods
[static] createDecryptBuffer (url, bgm, pos opt), playEncryptedBgm (bgm, pos opt)
