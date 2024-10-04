[Class Tree](index.md)

# Class: TextConverter
**@MZ PluginCommonBase.js** A static class for processing strings.<br />
However, this class is not in the global scope, so it is not used directly.<br />
It is accessed from [PluginManagerEx](PluginManagerEx.md).

*Note: The official plugin PluginCommonBase.js can be treated as core script, so I created a page for the included classes.*

### Methods

#### (static) convertEscapeCharactersBase (text, data) → {[String](String.md)}
Converts control characters within a string and returns them in the appropriate type.<br />
This method performs conversions for V, N, P, and G.

##### Arguments

| Name   | Type          | Traits           | Description      |
|--------|---------------|------------------|------------------|
| `text` | [String](String.md) |                  | The target for conversion |
| `data` | Object        | &lt;optional&gt; | (default: null)  |

---

#### (static) actorName (n) → {[String](String.md)}
Returns the name of the actor with the specified ID.

##### Arguments

| Name | Type          | Description   |
|------|---------------|---------------|
| `n`  | [Number](Number.md) | Actor ID      |

---

#### (static) partyMemberName(n) → {[String](String.md)}
Returns the name of the member with the specified number.

##### Arguments

| Name | Type          | Description   |
|------|---------------|---------------|
| `n`  | [Number](Number.md) | Member number |
