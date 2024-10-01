[Class Tree](index.md)

# Class: [Game_Interpreter](Game_Interpreter.md)

## List of Event Command Methods

## Table of Contents

### [1]
*   [Messages](#messages)
*   [Game Progression](#game-progression)
*   [Flow Control](#flow-control)
*   [Party](#party)
*   [Actors](#actors)

### [2]
*   [Movement](#movement)
*   [Characters](#characters)
*   [Pictures](#pictures)
*   [Timing](#timing)
*   [Screen](#screen)
*   [Audio & Video](#audio-video)

### [3]
*   [Scene Control](#scene-control)
*   [System Settings](#system-settings)
*   [Map](#map)
*   [Battle](#battle)
*   [Advanced](#advanced)

### Others
*   [For Editor](#for-editor)
*   [Marks](#marks)

---

## How to Read the Table

All event commands are structured as methods like the following, differing only by the number after "command" and whether there are parameters `params`.

---

### Method
#### command101 (params) → {Boolean}
[1] - [Messages] - [Display Text…]

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `params` | Object | Arguments passed to the command (was [Array](Array.md) in MV) |

---

Thus, for better readability, this is organized into a table.

Below is a table displaying the command numbers and command names in accordance with the tab numbers and groups shown in the RPG Maker MZ editor. <br />
There are also some command numbers that do not exist as commandXxx methods for JSON data. Typically, these are additional command information, represented after ├└.

Note that **bold** and <u>underlined</u> text are personal notes indicating "This is commonly used" and have no particular grammatical significance.

For details on the contents of the arguments, refer to Toriyacan's
[RPG Maker MZ Script Reference](https://docs.google.com/spreadsheets/d/1aqY-xzFqT0vnZE-OkfsMYsP9Ud91vWTrBLU-uDkJ-Ls/edit#gid=2095105278).

---

## [1]
### Messages

| Number | Command |
| --- | --- |
| 101 | <u>**Display Text…**</u> |
| 401 | └ Message for Display Text |
| 102 | **Display Choices…** |
| 402 | ├ When [Choice] |
| 403 | ├ When Canceled |
| 404 | └ End of Choices |
| 103 | Process for Number Input… |
| 104 | Process for Item Selection… |
| 105 | Display Text with Scroll… |
| 405 | └ Message for Display Text with Scroll… |

---

### Game Progression

| Number | Command |
| --- | --- |
| 121 | <u>**Operate Switch…**</u> |
| 122 | **Operate Variable…** |
| 123 | <u>**Operate Self-Switch…**</u> |
| 124 | Operate Timer… |

#### 121: Operate Variable…
* Constants
* Variables
* Random Numbers
* Game Data
    * Item Ownership Count
    * Weapon Ownership Count
    * Armor Ownership Count
    * Actor (Level, Experience Points, HP, MP, Max HP, Max MP, Attack Power, Defense Power, Magic Power, Magic Defense, Agility, Luck, **@MZ** TP)
    * Enemy Characters (same as Actors)
    * Characters (Player, Events) (Map X, Map Y, Direction, Screen X, Screen Y)
    * Party Actor IDs
    * **@MZ** Previous (ID of the last skill used, ID of the last item used, ID of the last acting actor, index of the last acting enemy, ID of the last target actor, index of the last target enemy)
    * Others (Map ID, Party Size, Gold, Steps, Play Time, Timer, Save Count, Battle Count, Victory Count, Escape Count)
* Script


---

### Flow Control

| Number | Command |
| --- | --- |
| 111 | <u>**Conditional Branch…**</u> |
| 411 | ├ Otherwise |
| 412 | └ End of Branch |
| 112 | Loop… |
| 113 | ├ Interrupt Loop |
| 413 | └ Repeat Until |
| 115 | **Interrupt Event Processing** |
| 117 | **Common Event…** |
| 118 | Label… |
| 119 | Jump to Label… |
| 108 | **Annotation…** |
| 408 | └ End of Annotation |


#### 111: Conditional Branch…
* [1]
    * Switch
    * Variable
    * Self-Switch
    * Timer
* [2]
    * Actor (In Party, Name, Class, Skills, Weapons, Armor, States)
* [3]
    * Enemy Characters (Present, States)
    * **Characters (Events)** (Direction)
    * Vehicles
* [4]
    * Money (≤, ≥, <)
    * Items
    * Weapons
    * Armor
    * Buttons (Confirm, Cancel, Shift, Down, Left, Right, Up, Page Up, Page Down) (Pressed, **@MZ** Triggered, **@MZ** Repeated)
    * Script

---

### Party

| Number | Command |
| --- | --- |
| 125 | Increase/Decrease Gold… |
| 126 | **Increase/Decrease Items…** |
| 127 | Increase/Decrease Weapons… |
| 128 | Increase/Decrease Armor… |
| 129 | **Swap Members…** |

---

### Actor

| Number | Command |
| --- | --- |
| 311 | Increase/Decrease HP… |
| 312 | Increase/Decrease MP… |
| 326 | Increase/Decrease TP… |
| 313 | Increase/Decrease States… |
| 314 | **Full Recovery…** |
| 315 | Increase/Decrease Experience Points… |
| 316 | Increase/Decrease Level… |
| 317 | Increase/Decrease Abilities… |
| 318 | Increase/Decrease Skills… |
| 319 | Change Equipment… |
| 320 | Change Name… |
| 321 | Change Class… |
| 324 | Change Nickname… |
| 325 | Change Profile… |

---

## [2]
### Movement

| Number | Command |
| --- | --- |
| 201 | <u>**Move Location…**</u> |
| 202 | Set Vehicle Position… |
| 203 | **Set Event Position…** |
| 204 | Scroll Map… |
| 205 | <u>**Set Movement Route…**</u> (EV Setting: Autonomous Movement [Custom]-[Route]) |
| 206 | Enter/Exit Vehicle |

#### 205: Set Movement Route…
For details, see [RPG.MoveCommand](RPG.MoveCommand.md).

---

### Characters

| Number | Command |
| --- | --- |
| 211 | <u>Change Transparency State…</u> (This Event Only) |
| 216 | Change Formation Walking… |
| 217 | Gather Formation Members |
| 212 | Display Animation… |
| 213 | Display Speech Bubble Icon… |
| 214 | **Temporarily Hide Event** |

---

### Pictures

| Number | Command |
| --- | --- |
| 231 | Show Picture… |
| 232 | Move Picture… |
| 233 | Rotate Picture… |
| 234 | Change Picture Color Tone… |
| 235 | Erase Picture… |

---

### Timing

| Number | Command |
| --- | --- |
| 230 | <u>Wait…</u> |

---

### Screen

| Number | Command |
| --- | --- |
| 221 | <u>**Screen Fade Out**</u> (Move Location) |
| 222 | <u>**Screen Fade In**</u> (Move Location) |
| 223 | Change Screen Color Tone… |
| 224 | Screen Flash… |
| 225 | Screen Shake… |
| 236 | Set Weather… |

---

### Audio & Video

| Number | Command |
| --- | --- |
| 241 | Play BGM… |
| 242 | Fade Out BGM… |
| 243 | Save BGM |
| 244 | Resume BGM |
| 245 | Play BGS… |
| 246 | Fade Out BGS… |
| 249 | Play ME… |
| 250 | <u>**Play SE…**</u> |
| 251 | Stop SE |
| 261 | Play Movie… |

---

### Scene Control

| Number | Command |
| --- | --- |
| 301 | **Battle Processing…** |
| 601 | ├ When Won |
| 602 | ├ When Escaped |
| 603 | └ When Lost |
| 302 | Shop Processing… |
| 303 | Name Input Processing… |
| 351 | Open Menu Screen |
| 352 | Open Save Screen |
| 353 | Game Over |
| 354 | Return to Title Screen |

---

## [3]
### System Settings

| Number | Command |
| --- | --- |
| 132 | Change Battle BGM… |
| 133 | Change Victory ME… |
| 139 | Change Defeat ME… |
| 140 | Change Vehicle BGM… |
| 134 | Change Save Prohibition… |
| 135 | Change Menu Prohibition… |
| 136 | Change Encounter Prohibition… |
| 137 | Change Sorting Prohibition… |
| 138 | Change Window Color… |
| 322 | <u>**Change Actor Image…**</u> |
| 323 | Change Vehicle… |

---

### Map

| Number | Command |
| --- | --- |
| 281 | Change Map Name Display… |
| 282 | Change Tileset… |
| 283 | Change Battle Background… |
| 284 | Change Parallax… |
| 285 | **Get Information at Specified Position…** |

#### 285: Get Information at Specified Position…
* Information Type (Terrain Tag, Event ID, [Tile ID](Tilemap.md#tile-id) (Layer 1), Tile ID (Layer 2), Tile ID (Layer 3), Tile ID (Layer 4), Region ID)
* Location
    * Directly Specified
    * Specified by Variable
    * **@MZ** Specified by Character (Player, Event)

---

### Battle

| Number | Command |
| --- | --- |
| 331 | Increase/Decrease Enemy HP… |
| 332 | Increase/Decrease Enemy MP… |
| 342 | Increase/Decrease Enemy TP… |
| 333 | Change Enemy States… |
| 334 | Full Recovery of Enemy… |
| 335 | Appear Enemy… |
| 336 | Transform Enemy… |
| 337 | Display Battle Animation… |
| 339 | Force Battle Action… |
| 340 | Interrupt Battle |

---

### Advanced

| Number | Command |
| --- | --- |
| 355 | **Script…** |
| 655 | └ Script from Line 2 Onward |
| 356 | Plugin Command… (MV Command) |
| 357 | **@MZ** **Plugin Command…** |
| 657 | **@MZ**└ For Displaying Arguments in Editor |

---

## Others

### For Editor

| Number | Command |
| --- | --- |
| 109 | **@MZ1.5.0** **Skip** |
| 505 | Data for Display in Editor |

---

### Marks

| Number | Command |
| --- | --- |
| 0 | End |
