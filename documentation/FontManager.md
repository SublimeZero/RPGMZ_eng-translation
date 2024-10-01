[Class Tree](index.md)

# Class: FontManager
**@MZ** A static class that handles fonts.

This class separates the font loading functionalities that were included in [Graphics](Graphics.md) in MV.

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_urls` | Object.&lt;[String](String.md)&gt; | [static] A list of URLs keyed by family |
| `_states` | Object.&lt;[String](String.md)&gt; | [static] A list of [states](#状態) keyed by family |

#### States

| String | Description |
| --- | --- |
| "loading" | Loading |
| "loaded" | Load complete |
| "error" | Error |

### Methods

#### (static) isReady ()→ {String}
Checks if it is ready.

#### (static) load (family, filename)

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `family` | [String](String.md) | Font family |
| `filename` | [String](String.md) | Font file name |

#### (static) makeUrl (filename)→ {String}
Generates and returns a URL from the specified filename. <br />
Specifically, "fonts/filename"

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `filename` | [String](String.md) | The file name |

#### (static) startLoading (family, url)
Loads the font from the specified URL.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `family` | [String](String.md) | Font family |
| `url` | [String](String.md) | File URL |

#### (static) throwLoadError (url)
Throws a loading error.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `url` | [String](String.md) | File URL |
