[Class Tree](index.md)

# Class: ConfigManager
A static class that handles the data for [Options].

Related Class: [Window_Options](Window_Options.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `alwaysDash` | Boolean | [static] [Always Dash] (default: false) |
| `commandRemember` | Boolean | [static] [Command Remember] (default: false) |
| `bgmVolume` | [Number](Number.md) | [static] [BGM Volume] (default: 100) |
| `bgsVolume` | [Number](Number.md) | [static] [BGS Volume] (default: 100) |
| `meVolume` | [Number](Number.md) | [static] [ME Volume] (default: 100) |
| `seVolume` | [Number](Number.md) | [static] [SE Volume] (default: 100) |
| `touchUI` | Boolean | **@MZ** [static] [Touch UI] (default: true) |
| `_isLoaded` | Boolean | **@MZ** [static] Whether it is loaded |

### Methods

#### (static) applyData (config)
Applies the specified options.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `config` | [MV.ConfigData](MV.ConfigData.md) | Option data |

#### (static) load ()
Loads the option data.

#### (static) makeData () → {[MV.ConfigData](MV.ConfigData.md)}
Generates and returns option data.

#### (static) readFlag (config, name) → {Boolean}
Returns the flag for the specified option data.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `config` | [MV.ConfigData](MV.ConfigData.md) | Option data |
| `name` | [String](String.md) | Setting name ('alwaysDash', 'commandRemember') |

#### (static) readVolume (config, name) → {[Number](Number.md)}
Returns the volume for the specified option data.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `config` | [MV.ConfigData](MV.ConfigData.md) | Option data |
| `name` | [String](String.md) | Setting name ('bgmVolume', 'bgsVolume', 'meVolume', 'seVolume') |

#### (static) save ()
Saves the option data.
