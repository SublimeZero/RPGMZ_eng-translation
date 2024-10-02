[Class Tree](index.md)

# Class: SceneManager
A static class that manages scenes (descendant classes of [Scene_Base](Scene_Base.md)).

It also serves as the base for the overall update.

In MZ, features that overlap with other classes have been deprecated. <br />
Environment checks have been consolidated into [Utils](Utils.md).

Changes have been made in versions 1.4.0 and 1.5.0.

Related classes: [Graphics](Graphics.md), [Bitmap](Bitmap.md), [AudioManager](AudioManager.md), [Input](Input.md), [TouchInput](TouchInput.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_scene` | [Scene_Base](Scene_Base.md) | [static] Current scene (same as `Graphics.app.stage`) |
| `_nextScene` | [Scene_Base](Scene_Base.md) | [static] Next scene |
| `_stack` | [Array](Array.md).&lt;Function&gt; | [static] History of scenes, etc. |
| `_exiting` | Boolean | [static] Whether exiting |
| `_previousScene` | [Scene_Base](Scene_Base.md) | [static] Previous scene |
| `_previousClass` | Function | [static] Previous scene, etc. |
| `_backgroundBitmap` | [Bitmap](Bitmap.md) | [static] Background image |
| `_smoothDeltaTime` | [Number](Number.md) | [static] Adjusted frame interval |
| `_elapsedTime` | [Number](Number.md) | [static] Elapsed time |

### Deprecated MV Properties
Refer to various screen sizes in [RPG.System($dataSystem)](RPG.System.md).

`_deltaTime`, `_currentTime`, `_accumulator`, `_stopped`, `_sceneStarted`, `_screenWidth`, `_screenHeight`, `_boxWidth`, `_boxHeight`

### Methods

#### (static) backgroundBitmap () → {[Bitmap](Bitmap.md)}
Returns a (blurred) snapshot for the generated background.

#### (static) checkBrowser ()
**@MZ** Checks the necessary features in the browser and throws an error if not supported.

#### (static) catchException (e)
Receives an error.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `e` | Event | Error event |

#### (static) catchLoadError (e)
**@MZ** Receives a loading error.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `e` | Event | Error event |

#### (static) catchNormalError (e)
**@MZ** Receives a normal error.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `e` | Event | Error event |

#### (static) catchUnknownError (e)
**@MZ** Receives an unknown error.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `e` | Event | Error event |

#### (static) changeScene ()
Switches the scene.

#### (static) checkPluginErrors ()
Checks for plugin errors.

#### (static) clearStack ()
Clears the history.

#### (static) determineRepeatNumber (deltaTime) → {Number}
**@MZ** Returns the number of loops to run based on the delay time.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `deltaTime` | [Number](Number.md) | Delay time |

#### (static) exit ()
Ends the scene transition.

#### (static) goto (sceneClass)
Transitions to the specified scene.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sceneClass` | [Scene_Base](Scene_Base.md) | Destination scene |

#### (static) initAudio ()
Initializes audio.

#### (static) initGraphics ()
Initializes graphics.

#### (static) initVideo ()
**@MZ** Initializes video.

#### (static) initialize ()
Initialization.

#### (static) initInput ()
Initializes input.

#### (static) isCurrentSceneBusy () → {Boolean}
Checks if the scene is running.

#### (static) isGameActive () → {Boolean}
Checks if the game is active (foreground window).

#### (static) isNextScene (sceneClass) → {Boolean}
Checks if the specified scene is the next scene.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sceneClass` | [Scene_Base](Scene_Base.md) | Scene to compare |

#### (static) isPreviousScene (sceneClass) → {Boolean}
Checks if the specified scene is the previous scene.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sceneClass` | [Scene_Base](Scene_Base.md) | Scene to compare |

#### (static) isSceneChanging () → {Boolean}
Checks if a scene is changing.

#### (static) onBeforeSceneStart ()
**@MZ** Handler before the scene starts.

#### (static) onError (e)
Error handler.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `e` | Event | Error event |

#### (static) onKeyDown (event)
Key down event handler. Controls reload (F5) and debug window (F8) here.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `event` | KeyboardEvent | Keyboard event |

#### (static) onReject ()
**@MZ** Handler when an error occurs.

#### (static) onSceneCreate ()
Handler when a scene is created.

#### (static) onSceneStart ()
Handler when a scene starts.

#### (static) onSceneTerminate ()
**@MZ** Handler when a scene is destroyed.

#### (static) onUnload ()
**@MZ** Handler during unload, such as when the window is closed.

#### (static) pop ()
Transitions by extracting the scene from the history.

#### (static) prepareNextScene (args)
Prepares for the next scene. The argument varies by scene, such as shop items.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `args` | * | Several arguments that differ by scene |

#### (static) push (sceneClass)
Transitions to the specified scene and retains the history.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sceneClass` | [Scene_Base](Scene_Base.md) | Scene to transition to |

#### (static) reloadGame ()
**@MZ** Reloads the game.

#### (static) resume ()
Resumes from a stopped state.

#### (static) run (sceneClass)
Executes the specified scene.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `sceneClass` | [Scene_Base](Scene_Base.md) | Scene to execute |

#### (static) setupEventHandlers()
**@MZ** Prepares various handlers.

#### (static) showDevTools ()
**@MZ** Displays developer tools. For testing only.

#### (static) snap () → {[Bitmap](Bitmap.md)}
Returns a snapshot.

#### (static) snapForBackground ()
Generates a (blurred) snapshot for the background.

#### (static) stop ()
Stops the scene transition.

#### (static) terminate ()
Ends the process.

#### (static) update (deltaTime)
Updates every frame.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `deltaTime` | [Number](Number.md) | Delay time |

#### (static) updateEffekseer ()
**@MZ** Updates Effekseer.

#### (static) updateFrameCount ()
**@MZ** Increases the frame count.

#### (static) updateInputData ()
Updates input data.

#### (static) updateMain ()
Updates the main parts.

#### (static) updateScene ()
Updates the scene.

### Deprecated MV Methods

[static] checkFileAccess (), initNwjs ()

setupErrorHandlers ()
preferableRendererType ()

_getTimeInMsWithoutMobileSafari (), checkWebGL (), isCurrentSceneStarted (), onSceneLoading (), renderScene (), requestUpdate (), shouldUseCanvasRenderer (), tickEnd (), tickStart (), updateManagers ()
