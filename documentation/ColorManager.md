[Class Tree](index.md)

# Class: ColorManager
**@MZ** A static class that handles color data for windows.

This class extracts color-related functionality that was part of [Window_Base](Window_Base.md) in MV. <br />
As a result, the methods have been changed to static methods.

### Methods
**@MZ** is used for methods that were not present in [Window_Base](Window_Base.md) in MV.

#### (static) loadWindowskin ()
Loads the window skin.

#### (static) textColor (n) → {[MV.CssColor](MV.CssColor.md)}
Returns the color corresponding to the specified number. <br />
Set with the colors from "img/system/window.png".

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `n` | [Number](Number.md) | Color number (0 to 31) |

#### (static) normalColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the normal color (color number: 0).

#### (static) mpColor (actor) → {[MV.CssColor](MV.CssColor.md)}
Returns the color for [MP]. The `actor` argument is for extension and is unused.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actor` | [Game_Battler](Game_Battler.md)| The target battler |

#### (static) mpCostColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the color for [MP Cost] (color number: 23).

#### (static) mpGaugeColor1 () → {[MV.CssColor](MV.CssColor.md)}
Returns the color 1 for the [MP] gauge (color number: 22).

#### (static) mpGaugeColor2 () → {[MV.CssColor](MV.CssColor.md)}
Returns the color 2 for the [MP] gauge (color number: 23).

#### (static) systemColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the system color (color number: 16).

#### (static) tpColor (actor) → {[MV.CssColor](MV.CssColor.md)}
Returns the color for [TP]. The `actor` argument is for extension and is unused.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actor` | [Game_Battler](Game_Battler.md)| The target battler |

#### (static) tpCostColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the color for [TP Cost] (color number: 29).

#### (static) tpGaugeColor1 () → {[MV.CssColor](MV.CssColor.md)}
Returns the color 1 for the [TP] gauge (color number: 28).

#### (static) tpGaugeColor2 () → {[MV.CssColor](MV.CssColor.md)}
Returns the color 2 for the [TP] gauge (color number: 29).

#### (static) crisisColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the danger color (color number: 17).

#### (static) deathColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the death color (color number: 18).

#### (static) dimColor1 () → {[MV.CssColor](MV.CssColor.md)}
Returns the background color 1 for [Dim] (default: "rgba(0, 0, 0, 0.6)").

#### (static) dimColor2 () → {[MV.CssColor](MV.CssColor.md)}
Returns the background color 2 for [Dim] (default: "rgba(0, 0, 0, 0)").

#### (static) gaugeBackColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the background color for the gauge (color number: 19).

#### (static) hpColor (actor) → {[MV.CssColor](MV.CssColor.md)}
Returns the color for the specified battler's [HP]. <br />
The returned color varies based on the state of the argument.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `actor` | [Game_Battler](Game_Battler.md)| The target battler |

#### (static) hpGaugeColor1 () → {[MV.CssColor](MV.CssColor.md)}
Returns the color 1 for the [HP] gauge (color number: 20).

#### (static) hpGaugeColor2 () → {[MV.CssColor](MV.CssColor.md)}
Returns the color 2 for the [HP] gauge (color number: 21).

#### (static) paramchangeTextColor (change) → {[MV.CssColor](MV.CssColor.md)}
Returns the color corresponding to the specified value. <br />
Used for displaying ability differences when changing equipment.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `change` | [Number](Number.md) | Negative value: powerDownColor, 0: normalColor, Positive value: powerUpColor |

#### (static) pendingColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the undecided color (the color in the center of the selection cursor).

#### (static) powerDownColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the power down color (color number: 25).

#### (static) powerUpColor () → {[MV.CssColor](MV.CssColor.md)}
Returns the power up color (color number: 24).

#### (static) ctGaugeColor1 () → {[MV.CssColor](MV.CssColor.md)}
**@MZ** Returns the timer gauge color 1 (color number: 26).

#### (static) ctGaugeColor2 () → {[MV.CssColor](MV.CssColor.md)}
**@MZ** Returns the timer gauge color 2 (color number: 27).

#### (static) damageColor (colorType) → {[MV.CssColor](MV.CssColor.md)}
**@MZ** Returns the color corresponding to the specified type.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `colorType` | [Number](Number.md) | 0: HP↓, 1: HP↑, 2: MP↓, 3: MP↑|

#### (static) outlineColor () → {[MV.CssColor](MV.CssColor.md)}
**@MZ** Returns the outline color of the text (default: "rgba(0, 0, 0, 0.6)").

#### (static) itemBackColor1 () → {[MV.CssColor](MV.CssColor.md)}
**@MZ** Returns the background color 1 for items (default: "rgba(32, 32, 32, 0.5)"). <br />
Above the gradient of `contentsBack` in [Window](Window.md) and the border.

#### (static) itemBackColor2 () → {[MV.CssColor](MV.CssColor.md)}
**@MZ** Returns the background color 2 for items (default: "rgba(0, 0, 0, 0.5)"). <br />
Below the gradient of `contentsBack` in [Window](Window.md).
