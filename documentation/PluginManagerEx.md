[Class Tree](index.md)

# Class: PluginManagerEx
A static class that handles command registration for plugins from **@MZ PluginCommonBase.js**.<br />
An enhanced version of [PluginManager](PluginManager.md).<br />
In addition to [PluginParam](PluginParam.md) and [TextConverter](TextConverter.md) classes in PluginCommonBase.js, these are utilized from PluginManagerEx, so there is no need to focus on them.<br />
New methods have also been added to [Game_Event](Game_Event.md) and [Game_Map](Game_Map.md).

* The official plugin PluginCommonBase.js can be considered almost as core script, so I created pages for the included classes.<br />
Note that PluginCommonBase.js has been updated from the version included in the sample game, so please use the files located in "/dlc/BasicResources/plugins/official/".

Related classes: [Game_Switches](Game_Switches.md), [Game_Switches](Game_Switches.md), [Game_Variables](Game_Variables.md)

### Properties

| Identifier      | Type                                     | Description                                   |
|------------------|------------------------------------------|-----------------------------------------------|
| `_selfSwitchKey `| [Array](Array.md).&lt;*&gt;            | [static] Self-switch key [map ID, event ID, type] |

### Methods

#### (static) convertVariables (text, data opt) → {*}
Converts control characters in the string and returns the appropriate type.

##### Arguments

| Name      | Type                       | Attributes   | Description                      |
|-----------|----------------------------|---------------|----------------------------------|
| `text`    | [String](String.md)        |               | Target for conversion (returns as is if not a string) |
| `data`    | Object                     | &lt;optional&gt; | (default: null)                  |

#### (static) convertEscapeCharacters (text, data opt) → {[String](String.md)}
Converts control characters in the string and returns them.<br />
This method performs conversions for V×2, N, P, G, and subsequently S, SS.

##### Arguments

| Name      | Type                       | Attributes   | Description                      |
|-----------|----------------------------|---------------|----------------------------------|
| `text`    | [String](String.md)        |               | Target for conversion (returns as is if not a string) |
| `data`    | Object                     | &lt;optional&gt; | (default: null)                  |

#### (static) convertEscapeCharactersEx (text, data opt) → {[String](String.md)}
Converts control characters in the string and returns them.<br />
This method performs conversions for S and SS.

##### Arguments

| Name      | Type                       | Attributes   | Description                      |
|-----------|----------------------------|---------------|----------------------------------|
| `text`    | [String](String.md)        |               | Target for conversion (returns as is if not a string) |
| `data`    | Object                     | &lt;optional&gt; | (default: null)                  |

#### (static) createParameter (currentScript) → {[PluginParam](PluginParam.md)}
Returns the parameters of the target plugin after type parsing.

##### Arguments

| Name              | Type   | Description                               |
|-------------------|--------|-------------------------------------------|
| `currentScript`   | Object | Target plugin (document.currentScript)    |

#### (static) createCommandArgs (args) → {Object}
Returns the command arguments after type parsing.<br />
If the arguments include an object, it returns [PluginParam](PluginParam.md).

##### Arguments

| Name      | Type   | Description                     |
|-----------|--------|---------------------------------|
| `args`    | Object | Arguments                       |

#### (static) findMetaValue (object, nameList) → {*}
Returns the value of the metadata in the memo field of the specified database.<br />
`nameList` can specify multiple tag names for multilingual support, but if there is only one tag, a single string is sufficient.<br />
It searches from the first tag and returns the value of the first found tag.

##### Example
```js
const metaValue = PluginManagerEx.findMetaValue( $dataActors[1], [ "englishTag", "JapaneseTag"] );
```

##### Arguments

| Name        | Type                                                      | Description                        |
|-------------|-----------------------------------------------------------|------------------------------------|
| `object`    | [MetaData](RPG.MetaData.md)                              | Database with a memo field        |
| `nameList`  | [Array](Array.md).&lt;[String](String.md)&gt; \| [String](String.md) | Array of tag names                |


#### (static) findMetaObject (object, nameList) → {[PluginParam](PluginParam.md)}
Parses and returns the JSON string written in the memo field of the specified database.

##### Arguments

| Name        | Type                                                      | Description                        |
|-------------|-----------------------------------------------------------|------------------------------------|
| `object`    | [MetaData](RPG.MetaData.md)                              | Database with a memo field        |
| `nameList`  | [Array](Array.md).&lt;[String](String.md)&gt; \| [String](String.md) | Array of tag names                |


#### (static) findMetaProperty (object) → {Object}
Returns the meta object of the specified object. Throws an error if it doesn't exist.

##### Arguments

| Name        | Type                                                      | Description                        |
|-------------|-----------------------------------------------------------|------------------------------------|
| `object`    | [MetaData](RPG.MetaData.md)                              | Database with a memo field        |


#### (static) findPluginName (currentScript) → {[String](String.md)}
Returns the name of the target plugin.

##### Arguments

| Name           | Type                                                      | Description                        |
|----------------|-----------------------------------------------------------|------------------------------------|
| `currentScript`| Object                                                    | Target plugin (document.currentScript) |


#### (static) registerCommand (currentScript, commandName, funcName) → {[PluginParam](PluginParam.md)}
Registers a plugin command.<br />
Enhanced version of [PluginManager.registerCommand()](PluginManager.md#static-registercommand-pluginname-commandname-func).

##### Arguments

| Name           | Type                                                      | Description                        |
|----------------|-----------------------------------------------------------|------------------------------------|
| `currentScript`| Object                                                    | Target plugin (document.currentScript) |
| `commandName`  | [String](String.md)                                      | Command name                      |
| `funcName`     | Function \| [String](String.md)                          | Command execution function (if string, method in [Game_Interpreter](Game_Interpreter.md)) |


#### (static) isExistPlugin (pluginName) → {Boolean}
Checks if the specified plugin exists.

##### Arguments

| Name           | Type                                                      | Description                        |
|----------------|-----------------------------------------------------------|------------------------------------|
| `pluginName`   | [String](String.md)                                      | Plugin name                       |


#### (static) generateSelfSwitchKey (eventId)
Generates a key for the self-switch.<br />
Stored in the `_selfSwitchKey` property.

##### Arguments

| Name        | Type                                                      | Description                        |
|-------------|-----------------------------------------------------------|------------------------------------|
| `eventId`   | [Number](Number.md)                                      | Event ID                          |


#### (static) findClassName (object) → {[String](String.md)}
Returns the class name of the specified object.

##### Arguments

| Name        | Type                                                      | Description                        |
|-------------|-----------------------------------------------------------|------------------------------------|
| `object`    | Object                                                    | Object                             |


#### (static) throwError (message, currentScript)
Throws an error.

##### Arguments

| Name           | Type                                                      | Description                        |
|----------------|-----------------------------------------------------------|------------------------------------|
| `message`      | [String](String.md)                                      | Error message                     |
| `currentScript`| Object                                                    | Target plugin (document.currentScript) |


#### (static) escapeXmlTag (text) → {[String](String.md)}
Replaces `&amp;lt;` with `<` and `&amp;gt;` with `>` in the string and returns it.

##### Arguments

| Name        | Type                                                      | Description                        |
|-------------|-----------------------------------------------------------|------------------------------------|
| `text`      | [String](String.md)                                      | String                             |
