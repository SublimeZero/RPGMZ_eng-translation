[Class Tree](index.md)

# Class: PluginParam

**@MZ PluginCommonBase.js** Holds plugin parameters and parses their types to return them.<br />
However, this class is not in the global scope, so it is not used directly.<br />
It is used as the return value of PluginManagerEx.createParameter().

*Note: The official plugin PluginCommonBase.js can be treated as a core script, so I created pages for the classes it contains.*

Related Class: [PluginManagerEx](PluginManagerEx.md)

### new PluginParam(parameter, needParse opt)
#### Arguments

| Name         | Type                                                      | Characteristics | Default  | Description               |
|--------------|-----------------------------------------------------------|------------------|----------|---------------------------|
| `parameter`  | Object                                                    |                  |          | Plugin parameters          |
| `needParse`  | Boolean                                                   | <optional>       | true     | Whether parsing is needed |


### Properties

| Identifier    | Type                                                      | Description               |
|---------------|-----------------------------------------------------------|---------------------------|
| `_parameter`   | Object                                                    | Plugin parameters         |


### Methods

#### setup (parameter)
Prepares with the specified parameters.

##### Arguments

| Name         | Type                                                      | Description               |
|--------------|-----------------------------------------------------------|---------------------------|
| `parameter`  | Object                                                    | Parameters                |


#### _createAccessor (paramName)
Generates an accessor (property read/write interface).

##### Arguments

| Name        | Type                                                      | Description               |
|-------------|-----------------------------------------------------------|---------------------------|
| `paramName` | [String](String.md)                                      | Parameter name            |


#### _convert(param, paramName) → {*}
Converts the given value to its appropriate type and returns it.<br />
If the suffix of the parameter name is one of text, name, note, desc, or script, it returns it as a string.

##### Arguments

| Name        | Type                                                      | Description               |
|-------------|-----------------------------------------------------------|---------------------------|
| `param`     | *                                                         | Value to convert          |
| `paramName` | [String](String.md)                                      | Parameter name            |


#### _findTextParamSuffixList () → {[Array](Array.md).&lt;RegExp&gt;}
Returns an array of regular expressions to identify suffix strings.


#### _isStructArray (param) → {Boolean}
Checks if it is a Struct array.

##### Arguments

| Name        | Type                                                      | Description               |
|-------------|-----------------------------------------------------------|---------------------------|
| `param`     | *                                                         | Value to check            |


#### _isStruct (param) → {Boolean}
Checks if it is a Struct value.

##### Arguments

| Name        | Type                                                      | Description               |
|-------------|-----------------------------------------------------------|---------------------------|
| `param`     | *                                                         | Value to check            |


#### _param (name) → {*}
Returns the value corresponding to the parameter name.

##### Arguments

| Name        | Type                                                      | Description               |
|-------------|-----------------------------------------------------------|---------------------------|
| `name`      | [String](String.md)                                      | Parameter name            |


#### _paramReplacer (key, value) → {*}
Function passed as the second argument to JSON.stringify.

##### Arguments

| Name        | Type                                                      | Description               |
|-------------|-----------------------------------------------------------|---------------------------|
| `key`       | *                                                         | Value to check            |
| `value`     | *                                                         | Value to check            |
