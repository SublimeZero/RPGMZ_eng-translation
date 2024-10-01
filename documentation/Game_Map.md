[Class Tree](index.md)

# Class: Game_Map

| Database | JSON Data | Global Variable | Save Data | Sprite Set |
| --- | --- | --- | --- | --- |
| Map | [RPG.Map](RPG.Map.md) | [$gameMap](global.md#gamemap-game_map) | Saved | [Spriteset_Map](Spriteset_Map.md) |

A class responsible for managing maps, including events and tilesets, as well as controlling scrolling and passability.

The numeric values assigned to tiles A through E refer to constants defined in [Tilemap](Tilemap.md).

[Self switches] are managed separately by [Game_SelfSwitches](Game_SelfSwitches.md).

Changes were made in v1.1.0, v1.2.0, and v1.5.0.<br />
Additionally, properties and methods added by the official plugin PluginCommonBase.js are also documented.

Related Classes: [RPG.Tileset](RPG.Tileset.md), [Scene_Map](Scene_Map.md), [Game_Screen](Game_Screen.md), [Tilemap](Tilemap.md), [Game_Player](Game_Player.md)

### new Game_Map ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_interpreter` | [Game_Interpreter](Game_Interpreter.md) | Command interpreter |
| `_mapId` | [Number](Number.md) | ID of the [map] |
| `_tilesetId` | [Number](Number.md) | ID of the [tileset] |
| `_events` | [Array](Array.md).&lt;[Game_Event](Game_Event.md)&gt; | Array of [events] |
| `_commonEvents` | [Array](Array.md).&lt;[Game_CommonEvent](Game_CommonEvent.md)&gt; | Array of [common events] |
| `_vehicles` | [Array](Array.md).&lt;[Game_Vehicle](Game_Vehicle.md)&gt; | Array of [vehicles] |
| `_displayX` | [Number](Number.md) | x-coordinate for map display (in tiles) |
| `_displayY` | [Number](Number.md) | y-coordinate for map display (in tiles) |
| `_nameDisplay` | Boolean | Whether to display the map's [name] |
| `_scrollDirection` | [Number](Number.md) | Scroll direction (supports numpad) |
| `_scrollRest` | [Number](Number.md) | Remaining distance for scrolling |
| `_scrollSpeed` | [Number](Number.md) | Scroll speed (default: 4) |
| `_parallaxName` | [String](String.md) | File name of the [parallax] |
| `_parallaxZero` | Boolean | Whether to set parallax to 0 |
| `_parallaxLoopX` | Boolean | [Loop horizontally] |
| `_parallaxLoopY` | Boolean | [Loop vertically] |
| `_parallaxSx` | [Number](Number.md) | Parallax x [scroll] amount (pixels) |
| `_parallaxSy` | [Number](Number.md) | Parallax y [scroll] amount (pixels) |
| `_parallaxX` | [Number](Number.md) | Parallax x position (in tiles) |
| `_parallaxY` | [Number](Number.md) | Parallax y position (in tiles) |
| `_battleback1Name` | [String](String.md) | File name of battle background image 1 (ground) at the back layer |
| `_battleback2Name` | [String](String.md) | File name of battle background image 2 (wall) at the front layer |
| `_needsRefresh` | Boolean | Whether an update is scheduled by [requestRefresh()](Game_Map.md#requestrefresh-mapid) and others |
| `_dynamicEvents` | [Array](Array.md).&lt;[Game_Interpreter](Game_Interpreter.md)&gt; | **@MZ PluginCommonBase.js** |

### Methods

#### adjustX (x) → {[Number](Number.md)}
Converts and returns the x position in the overall map to the x position from the left of the screen (in tiles).

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |


#### adjustY (y) → {[Number](Number.md)}
Converts and returns the y position in the overall map to the y position from the top of the screen (in tiles).

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `y` | [Number](Number.md) | y position (in tiles) |


#### airship () → {[Game_Vehicle](Game_Vehicle.md)}
Returns the [airship].


#### allTiles (x, y) → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of all [tile IDs](Tilemap.md#タイルID), including any overlapping [events] at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `y` | [Number](Number.md) | y position (in tiles) |


#### autoplay ()
Starts [BGM autoplay][BGS autoplay].


#### autotileType (x, y, z) → {[Number](Number.md)}
Returns the type of autotile at the specified position (returns -1 if not an autotile).

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `y` | [Number](Number.md) | y position (in tiles) |
| `z` | [Number](Number.md) | Overlap (0 to 3) |


#### autorunCommonEvents () → {[Array](Array.md).&lt;[Game_CommonEvent](Game_CommonEvent.md)&gt;}
Returns common events for [autoplay] **@MZ**.


#### battleback1Name () → {[String](String.md)}
Returns the file name of battle background image 1 (ground) at the back layer.


#### battleback2Name () → {[String](String.md)}
Returns the file name of battle background image 2 (wall) at the front layer.


#### boat () → {[Game_Vehicle](Game_Vehicle.md)}
Returns the [small boat].


#### bushDepth () → {[Number](Number.md)}
**@MZ1.5.0** Returns the depth of grass (in pixels).


#### canvasToMapX (x) → {[Number](Number.md)}
Converts and returns the x-coordinate of the canvas to tiles.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x coordinate (in pixels) |


#### canvasToMapY (y) → {[Number](Number.md)}
Converts and returns the y-coordinate of the canvas to tiles.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `y` | [Number](Number.md) | y coordinate (in pixels) |


#### changeBattleback (battleback1Name, battleback2Name)
Changes the [battle backgrounds].

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `battleback1Name` | [String](String.md) | File name of battle background image 1 (ground) at the back layer |
| `battleback2Name` | [String](String.md) | File name of battle background image 2 (wall) at the front layer |


#### changeParallax (name, loopX, loopY, sx, sy)
Changes the [parallax].

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `name` | [String](String.md) | [Image] file name |
| `loopX` | Boolean | [Loop horizontally] |
| `loopY` | Boolean | [Loop vertically] |
| `sx` | [Number](Number.md) | x [scroll] amount (in pixels) |
| `sy` | [Number](Number.md) | y [scroll] amount (in pixels) |


#### changeTileset (tilesetId)
Changes the [tileset].

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `tilesetId` | [Number](Number.md) | ID of the [tileset] |


#### checkLayeredTilesFlags (x, y, bit) → {Boolean}
Checks if there are any tiles at the specified position that have the specified flag set.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `y` | [Number](Number.md) | y position (in tiles) |
| `bit` | [Number](Number.md) | Bit for checking [RPG.Tileset](RPG.Tileset.md) flags |


#### checkPassage (x, y, bit) → {Boolean}
Checks if the specified flag bit is passable at the specified position.<br />
If the first tile that is not [☆] has the specified bit set, returns false.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `y` | [Number](Number.md) | y position (in tiles) |
| `bit` | [Number](Number.md) | Bit for checking [RPG.Tileset](RPG.Tileset.md) flags |


#### createVehicles ()
Generates [vehicles] (boat, ship, airship) on the map.


#### data () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of map data. (See: [RPG.Map.data](RPG.Map.md#マップデータ))


#### deltaX (x1, x2) → {[Number](Number.md)}
Returns the tile distance between two x coordinates (considering loops).

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x1` | [Number](Number.md) | x position (in tiles) |
| `x2` | [Number](Number.md) | x position (in tiles) |


#### deltaY (y1, y2) → {[Number](Number.md)}
Returns the tile distance between two y coordinates (considering loops).

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `y1` | [Number](Number.md) | y position (in tiles) |
| `y2` | [Number](Number.md) | y position (in tiles) |


#### disableNameDisplay ()
Sets the map's [display name] to be hidden.


#### displayName () → {[String](String.md)}
Returns the map's [display name].


#### displayX () → {[Number](Number.md)}
Returns the x-coordinate for map display (in tiles).


#### displayY () → {[Number](Number.md)}
Returns the y-coordinate for map display (in tiles).


#### distance (x1, y1, x2, y2) → {[Number](Number.md)}
Returns the distance between two points.<br />
This is the number of tiles required for movement, not the straight-line distance.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x1` | [Number](Number.md) | X position (in tiles) |
| `y1` | [Number](Number.md) | Y position (in tiles) |
| `x2` | [Number](Number.md) | X position (in tiles) |
| `y2` | [Number](Number.md) | Y position (in tiles) |


#### doScroll (direction, distance)
Scrolls in the specified direction by the specified distance.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `direction` | [Number](Number.md) | Direction (corresponding to the numpad) |
| `distance` | [Number](Number.md) | Distance (in tiles) |


#### enableNameDisplay ()
Sets the map [display name] to be visible.


#### encounterList () → {[Array](Array.md).&lt;[RPG.Map.Encounter](RPG.Map.Encounter.md)&gt;}
Returns an array of [encounters].


#### encounterStep () → {[Number](Number.md)}
Returns the [enemy encounter steps].


#### eraseEvent (eventId)
Deletes the [event] corresponding to the event ID.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `eventId` | [Number](Number.md) | Event ID |


#### event (eventId) → {[Game_Event](Game_Event.md)}
Returns the [event] corresponding to the event ID.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `eventId` | [Number](Number.md) | Event ID |


#### eventIdXy (x, y) → {[Number](Number.md)}
Returns the event ID of the [event] at the specified position. <br />
Returns 0 if there is no event, and the first event ID if there are multiple events.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### events () → {[Array](Array.md).&lt;[Game_Event](Game_Event.md)&gt;}
Returns an array of all [events] currently present on the map.


#### eventsXy (x, y) → {[Array](Array.md).&lt;[Game_Event](Game_Event.md)&gt;}
Returns an array of [events] at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### eventsXyNt (x, y) → {[Array](Array.md).&lt;[Game_Event](Game_Event.md)&gt;}
Returns an array of impassable [events] at the specified position. Nt = No Through.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### height () → {[Number](Number.md)}
Returns the [height] of the map (in tiles).


#### initDynamicEvents ()
**@MZ PluginCommonBase.js** Initializes dynamic events.


#### initialize ()
Initialization during object creation.


#### isAirshipLandOk (x, y) → {Boolean}
Checks if a [airship] can land at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### isAnyEventStarting () → {Boolean}
Checks if any [event] has started execution.


#### isBoatPassable (x, y) → {Boolean}
Checks if a [small boat] can pass at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### isBush (x, y) → {Boolean}
Checks if there is a [bush] flag on the tile at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### isCounter (x, y) → {Boolean}
Checks if there is a [counter] flag on the tile at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### isDamageFloor (x, y) → {Boolean}
Checks if there is a [damage floor] flag on the tile at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### isDashDisabled () → {Boolean}
Checks if [dashing is disabled].


#### isEventRunning () → {Boolean}
Checks if an event is currently running.


#### isInterpreterOf (interpreter) → {Boolean}
**@MZ PluginCommonBase.js** Checks if the specified interpreter is the same as the current map's interpreter.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `interpreter` | [Game_Interpreter](Game_Interpreter.md) | The interpreter to compare with |


#### isLadder (x, y) → {Boolean}
Checks if there is a [ladder] flag on the tile at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### isLoopHorizontal () → {Boolean}
Checks if it [loops horizontally].


#### isLoopVertical () → {Boolean}
Checks if it [loops vertically].


#### isNameDisplayEnabled () → {Boolean}
Checks if the map [display name] is visible.


#### isOverworld () → {Boolean}
Checks if the [tileset] [mode] is [field type].


#### isPassable (x, y, d) → {Boolean}
Checks if it is possible to move from the specified position in the specified direction.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |
| `d` | [Number](Number.md) | Direction (corresponding to the numpad) |


#### isScrolling () → {Boolean}
Checks if scrolling is in progress.


#### isShipPassable (x, y) → {Boolean}
Checks if a [large ship] can pass at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### isValid (x, y) → {Boolean}
Checks if the specified position is within the map range.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### layeredTiles (x, y) → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns an array of overlapping [tile IDs](Tilemap.md#tile-id) at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | X position (in tiles) |
| `y` | [Number](Number.md) | Y position (in tiles) |


#### mapId () → {[Number](Number.md)}
Returns the map ID.


#### parallaxName () → {[String](String.md)}
Returns the filename of the [parallax] image.


#### parallaxOx () → {[Number](Number.md)}
Returns the x position (in pixels) of the [parallax] image, taking parallax into account.


#### parallaxOy () → {[Number](Number.md)}
Returns the y position (in pixels) of the [parallax] image, taking parallax into account.


#### parallelCommonEvents () → {[Array](Array.md).&lt;[RPG.CommonEvent](RPG.CommonEvent.md)&gt;}
Returns an array of [parallel processing] [common events].

#### refereshVehicles ()
Redraws the [vehicles].

#### refresh ()
Updates the [events].

#### refreshIfNeeded ()
Redraws if requested by [Game_Map#requestRefresh](#requestrefresh-mapid).

#### refreshTileEvents ()
Updates the [events] that have tile images set.

#### regionId (x, y) → {[Number](Number.md)}
Returns the region ID of the tile at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `y` | [Number](Number.md) | y position (in tiles) |

#### requestRefresh ()
Requests a redraw of the map.  
*The mapId argument is no longer needed, so it has been removed.*

#### roundX (x) → {[Number](Number.md)}
Converts and returns the x-coordinate (in tiles) without considering the number of loops.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |

#### roundXWithDirection (x, d) → {[Number](Number.md)}
Returns the x-coordinate (in tiles) after moving in the specified direction (without considering the number of loops).

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `d` | [Number](Number.md) | direction (compatible with the numpad) |

#### roundY (y) → {[Number](Number.md)}
Converts and returns the y-coordinate (in tiles) without considering the number of loops.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `y` | [Number](Number.md) | y position (in tiles) |

#### roundYWithDirection (y, d) → {[Number](Number.md)}
Returns the y-coordinate (in tiles) after moving in the specified direction (without considering the number of loops).

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `y` | [Number](Number.md) | y position (in tiles) |
| `d` | [Number](Number.md) | direction (compatible with the numpad) |

#### screenTileX () → {[Number](Number.md)}
Returns the width of the screen (in tiles, including decimals).  
It is rounded to the nearest 1/16 tile.

#### screenTileY () → {[Number](Number.md)}
Returns the height of the screen (in tiles, including decimals).  
It is rounded to the nearest 1/16 tile.

#### scrollDistance () → {[Number](Number.md)}
Returns the scroll distance (in tiles).

#### scrollDown (distance)
Scrolls down by the specified distance.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `distance` | [Number](Number.md) | Distance to move down (in tiles) |

#### scrollLeft (distance)
Scrolls left by the specified distance.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `distance` | [Number](Number.md) | Distance to move left (in tiles) |

#### scrollRight (distance)
Scrolls right by the specified distance.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `distance` | [Number](Number.md) | Distance to move right (in tiles) |

#### scrollUp (distance)
Scrolls up by the specified distance.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `distance` | [Number](Number.md) | Distance to move up (in tiles) |

#### setDisplayPos (x, y)
Displays the map at the specified position (relative to the top-left corner of the screen).  
Also handles whether the scroll stops at the edges of the map or loops.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `y` | [Number](Number.md) | y position (in tiles) |

#### setup (mapId)
Prepares for displaying a new map when moving maps, etc.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `mapId` | [Number](Number.md) | Map ID |

#### setupAutorunCommonEvent () → {Boolean}
Prepares the trigger [auto-execute] common events and returns whether any were prepared.

#### setupBattleback ()
Prepares the battle background.

#### setupDynamicCommon (id)
**@MZ PluginCommonBase.js** Prepares dynamic common events.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `id` | [Number](Number.md) | Common event ID |

#### setupDynamicInterpreter (list)
**@MZ PluginCommonBase.js** Prepares the dynamic interpreter.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `list` | [Array](Array.md).&lt;[RPG.EventCommand](RPG.EventCommand.md)&gt;  | List of commands |

#### setupEvents ()
Prepares the [events].

#### setupParallax ()
Prepares the [parallax].

#### setupScroll ()
Prepares the scrolling.

#### setupStartingEvent () → {Boolean}
Prepares events to be executed at the start, including test events, map events, and common events, and returns whether any were prepared.

#### setupStartingMapEvent () → {Boolean}
Prepares map events to be executed at the start and returns whether any were prepared.

#### setupTestEvent () → {Boolean}
Prepares test events to be executed at the start and returns whether any were prepared.

#### ship () → {[Game_Vehicle](Game_Vehicle.md)}
Returns the [large ship].

#### startScroll (direction, distance, speed)
Starts scrolling.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `direction` | [Number](Number.md) |  |
| `distance` | [Number](Number.md) |  |
| `speed` | [Number](Number.md) |  |

#### terrainTag (x, y) → {[Number](Number.md)}
Returns the first [terrain tag] of the tile at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `y` | [Number](Number.md) | y position (in tiles) |

#### tileEventsXy (x, y) → {[Array](Array.md).&lt;[Game_Event](Game_Event.md)&gt;}
Returns an array of [events] at the specified position that have selected tile set images.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) |  |
| `y` | [Number](Number.md) |  |

#### tileHeight () → {[Number](Number.md)}
Returns the height of the tile (default: 48 pixels).

#### tileId (x, y, z) → {[Number](Number.md)}
Returns the [tile ID](Tilemap.md#タイルID) of the tile at the specified position.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `y` | [Number](Number.md) | y position (in tiles) |
| `z` | [Number](Number.md) | overlap (0 to 3) |

#### tileset () → {[RPG.Tileset](RPG.Tileset.md)}
Returns the [tileset].

#### tilesetFlags () → {[Array](Array.md).&lt;[Number](Number.md)&gt;}
Returns the terrain flags such as [passability] set in the [tileset].  
For details on terrain flags, refer to [RPG.Tileset](RPG.Tileset.md).

#### tilesetId () → {[Number](Number.md)}
Returns the tileset ID.

#### tileWidth () → {[Number](Number.md)}
Returns the width of the tile (default: 48 pixels).

#### unlockEvent (eventId)
Unlocks the [event] with the specified ID. Disables the state of facing the player with the decision button.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `eventId` | [Number](Number.md) |  |

#### update (sceneActive)
Updates every frame.  
However, the interpreter update occurs only if the scene is active.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `sceneActive` | Boolean | Whether the scene is active |

#### updateEvents ()
Updates all [events] on the current map.

#### updateInterpreter ()
Updates the interpreter.

#### updateParallax ()
Updates the [parallax].

#### updateScroll ()
Updates the scroll.

#### updateVehicles ()
Updates all vehicles on the current map.

#### vehicle (type) → {[Game_Vehicle](Game_Vehicle.md)}
Returns a [vehicle] specified by a number (0: small boat, 1: large ship, 2: airship) or a string ('boat', 'ship', 'airship').

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `type` | [Number](Number.md) | [String](String.md) |  |

#### vehicles () → {[Array](Array.md).&lt;[Game_Vehicle](Game_Vehicle.md)&gt;}
Returns an array of generated [vehicles].

#### width () → {[Number](Number.md)}
Returns the [width] of the map (in tiles).

#### xWithDirection (x, d) → {[Number](Number.md)}
Returns the x-coordinate (in tiles) after moving in the specified direction.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `x` | [Number](Number.md) | x position (in tiles) |
| `d` | [Number](Number.md) | direction (compatible with the numpad) |

#### yWithDirection (y, d) → {[Number](Number.md)}
Returns the y-coordinate (in tiles) after moving in the specified direction.

##### Arguments

| Identifier | Type | Description |
| --- | --- | --- |
| `y` | [Number](Number.md) | y position (in tiles) |
| `d` | [Number](Number.md) | direction (compatible with the numpad) |
