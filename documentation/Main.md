[Class Tree](index.md)

# Class: Main

**@MZ**  
Main class. Defined in `main.js`.

In MV, the initialization process was largely delegated to `SceneManager`'s `run(Scene_Boot)`, but in MZ, some of it has been separated.

Changes made in version v1.4.4.

Related class: [Scene_Boot](Scene_Boot.md)

### new Main ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `xhrSucceeded` | Boolean | Whether XMLHttpRequest was successful |
| `loadCount` | [Number](Number.md) | The number of scripts loaded |
| `error` | Object | Error event |
| `numScripts` | [Number](Number.md) | The number of scripts |

### Methods

#### eraseLoadingSpinner ()
Removes the loading spinner (loading animation).

#### hookNwjsClose ()
**@MZ1.4.4** Sets a hook to ensure NW.js closes properly.

#### initEffekseerRuntime ()
Initializes the Effekseer runtime.

#### isPathRandomized ()
Checks if the gatekeeper is randomizing paths.

#### loadMainScripts ()
Loads the core scripts.

#### makeErrorHtml (name, message) → {[String](String.md)}
Generates and returns an HTML (div element) for error display.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `name` | [String](String.md)  | The name of the error |
| `message` | [String](String.md)  | The error message |

#### onEffekseerError ()
Handler for Effekseer load errors.

#### onEffekseerLoad ()
Handler for when Effekseer finishes loading.

#### onScriptError (e)
Handler for JavaScript load errors.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `e` | Error | The error |

#### onScriptLoad ()
Handler for when JavaScript finishes loading.

#### onWindowError (event)
Handler for window load errors.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `event` | Object | The error event |

#### onWindowLoad ()
Handler for when the window finishes loading.

#### printError (name, message)
Displays the error.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `name` | [String](String.md)  | The name of the error |
| `message` | [String](String.md)  | The error message |

#### run ()
Starts execution.

#### showLoadingSpinner ()
Displays the loading spinner (loading animation).

#### testXhr ()
Tests XMLHttpRequest.
