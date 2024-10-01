[Class Tree](index.md)

# Class: PluginManager
A static class that manages plugins.<br />
For plugin settings (annotations), refer to [MV.PluginSettings](MV.PluginSettings.md).

The [PluginManagerEx](PluginManagerEx.md) added by the official plugin PluginCommonBase.js is an enhanced version of this class.

Related classes: [Game_Interpreter](Game_Interpreter.md), [RPG.EventCommand](RPG.EventCommand.md)

### Properties

| Name          | Type                                                  | Description                            |
|---------------|-------------------------------------------------------|----------------------------------------|
| `_scripts`    | [Array](Array.md).&lt;[String](String.md)&gt;       | [static] Array of plugin names        |
| `_errorUrls`  | [Array](Array.md).&lt;[String](String.md)&gt;       | [static] Array recording load errors  |
| `_parameters` | Object.&lt;[Parameters](MV.PluginSettings.md#parameters)&gt; | [static] List of parameters keyed by plugin name (in lowercase) |
| `_commands`   | Object.&lt;Function&gt;                              | **@MZ** [static] List of functions keyed by "plugin name: command name" |

### Deprecated MV Property
`_path`

### Methods

#### (static) callCommand (self, pluginName, commandName, args)
**@MZ** Executes a command.

##### Arguments

| Name          | Type                                               | Description                        |
|---------------|----------------------------------------------------|------------------------------------|
| `self`        | Function                                           | The function that sets the scope for `this` |
| `pluginName`  | [String](String.md)                               | Plugin name                        |
| `commandName` | [String](String.md)                               | Command name                       |
| `args`        | Object                                            | Arguments to pass to the command   |

#### (static) checkErrors ()
Checks for errors.

#### (static) makeUrl (filename) → {String}
**@MZ** Generates and returns a URL from the specified filename.<br />
Specifically, "js/plugins/filename.js"<br />
If it's in a folder, the path must include the folder.

##### Arguments

| Name      | Type                       | Description                   |
|-----------|----------------------------|-------------------------------|
| `filename`| [String](String.md)        | Filename (without the .js extension) |

#### (static) loadScript (filename)
Loads a plugin file.

##### Arguments

| Name      | Type                       | Description                   |
|-----------|----------------------------|-------------------------------|
| `filename`| [String](String.md)        | Filename (without the .js extension) |

#### (static) onError (e)
Error handler.

##### Arguments

| Name | Type   | Description        |
|------|--------|--------------------|
| `e`  | Event  | Error event        |

#### (static) parameters (name) → {Object}
Returns parameters corresponding to the specified plugin name as an object.<br />
Refer to the items in [MV.PluginSettings](MV.PluginSettings.md) for the return value contents.

##### Arguments

| Name      | Type                       | Description                    |
|-----------|----------------------------|--------------------------------|
| `name`    | [String](String.md)        | Plugin name (case-insensitive) |

#### (static) registerCommand (pluginName, commandName, func)
**@MZ** Registers a command.

##### Arguments

| Name          | Type                       | Description                      |
|---------------|----------------------------|----------------------------------|
| `pluginName`  | [String](String.md)        | Plugin name                      |
| `commandName` | [String](String.md)        | Command name                     |
| `func`        | Function                   | Command function                 |

#### (static) setParameters (name, parameters)
Sets parameters.

##### Arguments

| Name        | Type                                               | Description                    |
|-------------|----------------------------------------------------|--------------------------------|
| `name`      | [String](String.md)                                | Plugin name (case-insensitive) |
| `parameters`| [Parameters](MV.PluginSettings.md#parameters)      | Combination of parameter [name] and [value] |

#### (static) setup (plugins)
Initializes plugins.

##### Arguments

| Name      | Type                                               | Description                   |
|-----------|----------------------------------------------------|-------------------------------|
| `plugins` | [Array](Array.md).&lt;[MV.PluginSettings](MV.PluginSettings.md)&gt; | Array of plugin settings      |

#### (static) throwLoadError (url)
Throws a load error.

##### Arguments

| Name | Type                       | Description  |
|------|----------------------------|--------------|
| `url`| [String](String.md)        | File URL     |
