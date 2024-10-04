[Class Tree](index.md)

# Class: Utils
A static class that gathers useful methods, mainly for checking the usage environment.

Changes made in v1.3.2.

Related Classes: [Graphics](Graphics.md), [Video](Video.md)

---

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `RPGMAKER_NAME` | [String](String.md) | [static][read-only] The name of RPG Maker (default: "MZ") |
| `RPGMAKER_VERSION` | [String](String.md) | [static][read-only] The version of RPG Maker (e.g., "1.0.0") |

---

### Methods

#### (static) canPlayOgg () → {Boolean}
**@MZ** Checks if Ogg files can be played.

---

#### (static) canPlayWebm () → {Boolean}
**@MZ** Checks if Webm files can be played.

---

#### (static) canReadGameFiles () → {Boolean}
Checks if files in the game folder can be read.

---

#### (static) canUseCssFontLoading () → {Boolean}
**@MZ** Checks if CSS font loading is possible.<br />
Was a method in Graphics in MV.

---

#### (static) canUseIndexedDB () → {Boolean}
**@MZ** Checks if IndexedDB is available.

---

#### (static) canUseWebAudioAPI () → {Boolean}
**@MZ** Checks if WebAudioAPI is available.

---

#### (static) canUseWebGL () → {Boolean}
**@MZ** Checks if WebGL is available.

---

#### (static) checkRMVersion (version) → {Boolean}
**@MZ** Checks if the specified version string is <= the current version.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `version` | [String](String.md) | Version string (e.g., "1.0.0") |

---

#### (static) containsArabic (str) → {Boolean}
**@MZ** Checks if the specified string contains Arabic characters.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `str` | [String](String.md) | String |

---

#### (static) decryptArrayBuffer (source) → {[ArrayBuffer](ArrayBuffer.md)}
**@MZ** Decrypts encrypted data.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `source` | [ArrayBuffer](ArrayBuffer.md) | Data to decrypt |

---

#### (static) encodeURI (str) → {[String](String.md)}
**@MZ** Performs URI encoding (but leaves / unchanged).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `str` | [String](String.md) | String to encode |

---

#### (static) escapeHtml (str) → {[String](String.md)}
**@MZ** Escapes for HTML using character references (e.g., &amp;).

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `str` | [String](String.md) | String to escape |

---

#### (static) extractFileName (filename) → {[String](String.md)}
**@MZ1.3.2** Extracts and returns only the file part from a file path.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | File path |

---

#### (static) generateRuntimeId () → {[Number](Number.md)}
Generates and returns a runtime ID.

---

#### (static) hasEncryptedAudio () → {Boolean}
**@MZ** Checks if the game contains encrypted audio.

---

#### (static) hasEncryptedImages () → {Boolean}
**@MZ** Checks if the game contains encrypted images.

---

#### (static) isAndroidChrome () → {Boolean}
Checks if the browser is Android Chrome.

---

#### (static) isLocal () → {Boolean}
**@MZ** Checks if it is running in a local environment.

---

#### (static) isMobileDevice () → {Boolean}
Checks if it is a mobile device.<br />
Includes "Android", "webOS", "iPhone", "iPad", "iPod", "BlackBerry", "Opera Mini".

---

#### (static) isMobileSafari () → {Boolean}
Checks if the browser is Mobile Safari.

---

#### (static) isNwjs () → {Boolean}
Checks if it is using NW.js as a foundation.

---

#### (static) isOptionValid (name) → {Boolean}
Checks if the specified option (e.g., query after ? in the URL) is included.<br />
Options include "test", "btest", "etest", "onTop", "devToolOff", "showfps", "canvas", "webgl", "noaudio".

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `name` | [String](String.md) | Option string |

---

#### (static) isSupportPassiveEvent () → {Boolean}
Checks if the browser supports passive events.

---

#### (static) rgbToCssColor (r, g, b) → {[MV.CssColor](MV.CssColor.md)}
Generates and returns a CSS color string from the specified RGB color values.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `r` | [Number](Number.md) | Red (0-255) |
| `g` | [Number](Number.md) | Green (0-255) |
| `b` | [Number](Number.md) | Blue (0-255) |

---

#### (static) setEncryptionInfo (hasImages, hasAudio, key)
**@MZ** Sets encryption information.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `hasImages` | Boolean | Whether to encrypt images |
| `hasAudio` | Boolean | Whether to encrypt audio |
| `key` | [String](String.md) | Encryption key |
