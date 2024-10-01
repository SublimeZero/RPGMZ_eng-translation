[Class Tree](index.md)

# Class: EffectManager
**@MZ** A static class that handles effects.

In MZ, the effect system uses [Effekseer](https://effekseer.github.io/jp/), and this class is prepared to handle those files.

Changes were made in v1.1.0 and v1.2.0.

Related classes: [Graphics](Graphics.md), [RPG.Effect](RPG.Effect.md), [Sprite_Animation](Sprite_Animation.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_cache` | Object.&lt;EffekseerEffect&gt; | [static] A list of Effekseer effects keyed by URL |
| `_errorUrls` | [Array](Array.md).&lt;[String](String.md)&gt; | [static] An array of errors |

### Methods

#### (static) checkErrors ()
Throws an error if any errors have occurred.

#### (static) clear ()
Clears the cache.

#### (static) isReady () → {[String](String.md)}
Checks if it is ready.

#### (static) load (filename) → {EffekseerEffect}
Loads effect information from the specified file.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | The filename |

#### (static) makeUrl (filename) → {[String](String.md)}
Generates and returns a URL from the specified filename. <br />
Specifically, "effects/filename.efkefc"

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | The filename |

#### (static) onError (url)
Handler for when a loading error occurs.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `url` | [String](String.md) | The file URL |

#### (static) onLoad (url)
Handler for when loading is complete. <br />
An empty function for extensions.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `url` | [String](String.md) | The file URL |

#### (static) startLoading (url)
Loads effect information from the specified URL.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `url` | [String](String.md) | The file URL |

#### (static) throwLoadError (url)
Throws a loading error.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `url` | [String](String.md) | The file URL |
