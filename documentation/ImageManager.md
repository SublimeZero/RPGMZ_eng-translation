[Class Tree](index.md)

# Class: ImageManager
A static object that loads and holds (caches) image files.

With the transition to MZ, the caching method has changed significantly, so this class has also changed considerably.<br />
It now relies on the browser's caching functionality, making it much simpler.<br />
Methods in the reserveXxxx() family have all been abolished.<br />
Additionally, the specification of hue and smoothing during loading has been removed.

Some properties have been transferred from [Window_Base](Window_Base.md).

Changes made in v1.3.2.

Related classes: [Bitmap](Bitmap.md), [Graphics](Graphics.md), [Game_Screen](Game_Screen.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `iconWidth` | [Number](Number.md) | **@MZ** [static] Icon width (default: 32 pixels) |
| `iconHeight` | [Number](Number.md) | **@MZ** [static] Icon height (default: 32 pixels) |
| `faceWidth` | [Number](Number.md) | **@MZ** [static] Face image width (default: 144 pixels) |
| `faceHeight` | [Number](Number.md) | **@MZ** [static] Face image height (default: 144 pixels) |
| `_cache` | Object.&lt;[Bitmap](Bitmap.md)&gt; | [static] Image cache with URL as the key |
| `_system` | Object.&lt;[Bitmap](Bitmap.md)&gt; | [static] Image cache targeting the system folder with URL as the key<br /> |
| `_emptyBitmap` | [Bitmap](Bitmap.md) | [static] Empty image |

### Deprecated MV Properties
`cache`, `_imageCache`, `_requestQueue`, `_systemReservationId`

### Methods

#### (static) clear ()
Clears the image cache of RPG Maker MZ.<br />
This does not clear the cache held by the browser or others.

#### (static) isBigCharacter (filename) → {Boolean}
Checks if the specified filename has a "$" at the end.<br />
If it has a "$", it is considered as an image for one character of size 3x4, but it is not known if it is actually big.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename |

#### (static) isObjectCharacter (filename) → {Boolean}
Checks if the specified filename has a "!" at the end.<br />
If it has a "!", it is considered as an image that does not shift up during display, but it is not known if it is actually an object image.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename |

#### (static) isReady () → {Boolean}
Checks if the image cache is complete.

#### (static) isZeroParallax (filename) → {Boolean}
Checks if the specified filename has a "!" at the end.<br />
If it has a "!", it is considered as a distant image that does not shift.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename |

#### (static) loadAnimation (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/animations/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadBattleback1 (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/battlebacks1/" folder with smoothing applied.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadBattleback2 (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/battlebacks2/" folder with smoothing applied.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadBitmap (folder, filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified folder and filename from the project folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `folder` | [String](String.md) | Folder name (specify as "img/faces/") |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadBitmapFromUrl (folder, filename) → {[Bitmap](Bitmap.md)}
**@MZ** Loads and returns the image from the specified URL.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `url` | [String](String.md) | File URL |

#### (static) loadCharacter (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/characters/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadEnemy (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/enemies/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadFace (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/faces/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadParallax (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/parallaxes/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadPicture (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/pictures/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadSvActor (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/sv_actors/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadSvEnemy (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/sv_enemies/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadSystem (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/system/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadTileset (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/tilesets/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadTitle1 (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/titles1/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

#### (static) loadTitle2 (filename) → {[Bitmap](Bitmap.md)}
Loads and returns the image with the specified filename from the "img/titles2/" folder.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | Filename (excluding the .png extension) |

### Deprecated MV Methods
[static] _generateCacheKey(path, hue), clearRequest (), loadEmptyBitmap (), update (), releaseReservation, requestAnimation (filename, hue), requestBattleback1 (filename, hue), requestBattleback2 (filename, hue), requestBitmap (folder, filename), requestCharacter (filename, hue), requestEnemy (filename, hue), requestFace (filename, hue), requestNormalBitmap (path, hue), requestParallax (filename, hue), requestPicture (filename, hue), requestSvActor (filename, hue), requestSvEnemy (filename, hue), requestSystem (filename, hue), requestTileset (filename, hue), requestTitle1 (filename, hue), requestTitle2 (filename, hue), reserveAnimation (filename, hue, reservationId), reserveBattleback1 (filename, hue, reservationId), reserveBattleback2 (filename, hue, reservationId), reserveBitmap (folder, filename, hue, smooth, reservationId), reserveCharacter (filename, hue, reservationId), reserveEnemy (filename, hue, reservationId), reserveFace (filename, hue, reservationId), reserveNormalBitmap (path, hue, reservationId), reserveParallax (filename, hue, reservationId), reservePicture (filename, hue, reservationId), reserveSvActor (filename, hue, reservationId), reserveSvEnemy (filename, hue, reservationId), reserveSystem (filename, hue, reservationId), reserveTileset (filename, hue, reservationId), reserveTitle1 (filename, hue, reservationId), reserveTitle2 (filename, hue, reservationId), setDefaultReservationId (reservationId)
