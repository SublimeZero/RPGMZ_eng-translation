[Class Tree](index.md)

# Class: JsonEx
A wrapper class for the static built-in class [JSON](https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/JSON) that handles JSON files.

Although it includes some private methods (indicated by a leading underscore), the primary methods used are [parse()](JsonEx.md#static-parse-json--object) and [stringify()](JsonEx.md#static-stringify-object--string).<br />
The method [makeDeepCopy()](JsonEx.md#static-makedeepcopy-object--object) is included in this class as it performs a processing task that can convert JSON.

The JSON data is classified under the namespace [RPG](RPG.md).

Related class: [DataManager](DataManager.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `maxDepth` | [Number](Number.md) | [static] The maximum depth of the object (default value: 100) |


### Methods

#### (static) _decode (value, circular, registry) → {Object}
Preprocessing for parse.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `value` | | Object \| [Array](Array.md) | The object to decode |
| `circular` | [Array](Array.md) | Array for circular reference checking |
| `registry` | Object | Registry |


#### (static) _encode (value, circular, depth) → {Object}
Preprocessing for stringify.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `value` | Object \| [Array](Array.md) | The object to encode |
| `circular` | [Array](Array.md) | Array for circular reference checking |
| `depth` | [Number](Number.md) | Depth |


#### (static) makeDeepCopy (object) → {Object}
Returns a deep copy of the specified object (a separate data structure with no reference relationship).

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `object` | Object | The object to copy |


#### (static) parse (json) → {Object}
Converts a JSON string into an object and returns it.<br />
Technically, it can also convert arrays and other structures that are not valid JSON strings.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `json` | [String](String.md) | JSON string |


#### (static) stringify (object) → {[String](String.md)}
Converts an object into a JSON string and returns it.

##### Parameters

| Name | Type | Description |
| --- | --- | --- |
| `object` | Object | The object to convert |


### MV Deprecated Methods
[static]
_cleanMetadata (object), _generateId (), _getConstructorName (value), _linkCircularReference (contents, circular, registry), _restoreCircularReference (circulars)
