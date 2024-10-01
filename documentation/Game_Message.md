[Class Tree](index.md)

# Class: Game_Message

| Global Variables |
| --- |
| [$gameMessage](global.md#gamemessage-game_message) |

This class temporarily stores message and choice strings and settings, which are referenced when the window is displayed.<br />
Game_Message only holds data, and it is referenced from the window when displayed.<br />
The [Game_Interpreter.setWaitMode()](Game_Interpreter.md#setwaitmode-waitmode) method is used to wait for the message to finish.

Related Classes: [Window_Base](Window_Base.md), [Window_Message](Window_Message.md), [Window_ChoiceList](Window_ChoiceList.md), [Window_NumberInput](Window_NumberInput.md), [Window_EventItem](Window_EventItem.md), [Window_ScrollText](Window_ScrollText.md), [RPG.Actor](RPG.Actor.md)

### new Game_Message ()

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| `_texts` | [Array](Array.md).&lt;[String](String.md)&gt; | [Text] |
| `_choices` | [Array](Array.md).&lt;[String](String.md)&gt; | Choices |
| `_speakerName` | [String](String.md) | Content of the [Name] field |
| `_faceName` | [String](String.md) | [Face] file name |
| `_faceIndex` | [Number](Number.md) | [Face] number |
| `_background` | [Number](Number.md) | [[Background]](Game_Message.md#background) |
| `_positionType` | [Number](Number.md) | [[Window Position]](Game_Message.md#window-position) |
| `_choiceDefaultType` | [Number](Number.md) | [Default] for choices |
| `_choiceCancelType` | [Number](Number.md) | [Cancel] for choices |
| `_choiceBackground` | [Number](Number.md) | [[Background]](Game_Message.md#background) for choices |
| `_choicePositionType` | [Number](Number.md) | [[Window Position]](Game_Message.md#window-position) for choices |
| `_numInputVariableId` | [Number](Number.md) | [Variable] ID for numeric assignment |
| `_numInputMaxDigits` | [Number](Number.md) | [Number of Digits] |
| `_itemChoiceVariableId` | [Number](Number.md) | [Variable] ID for choice assignment |
| `_itemChoiceItypeId` | [Number](Number.md) | [Item Type] ID |
| `_scrollMode` | Boolean | Whether to scroll |
| `_scrollSpeed` | [Number](Number.md) | Scroll speed |
| `_scrollNoFast` | Boolean | Whether [No Fast Forward] |
| `_choiceCallback` | function | Callback function for choices |

#### [Background]

| Number | [Background] |
| --- | --- |
| 0 | Window |
| 1 | Darken |
| 2 | Transparent |

#### [Window Position]

| Number | [Window Position] |
| --- | --- |
| 0 | Top |
| 1 | Middle |
| 2 | Bottom |

### Methods

#### add (text)
Adds text.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `text` | [String](String.md) | Text to add |

#### allText () → {[String](String.md)}
Returns all text included in the message.

#### background () → {[Number](Number.md)}
Returns the number for [[Background]](Game_Message.md#background).

#### choiceBackground () → {[Number](Number.md)}
Returns the [[Background]](Game_Message.md#background) for choices.

#### choiceCancelType ()
Returns the type of cancel for choices.

#### choiceDefaultType ()
Returns the type of default for choices.

#### choicePositionType () → {[Number](Number.md)}
Returns the [[Window Position]](Game_Message.md#window-position) for choices.

#### choices () → {[Array](Array.md).&lt;[String](String.md)&gt;}
Returns choices.

#### clear ()
Clears.

#### faceIndex () → {[Number](Number.md)}
Returns the [Face] number.

#### faceName () → {[String](String.md)}
Returns the [Face] file name.

#### hasText () → {Boolean}
Checks if the message has text.

#### initialize ()
Initialization upon object creation.

#### isBusy () → {Boolean}
Checks if currently displaying or processing input/selection.

#### isChoice () → {Boolean}
Checks if [Choice Display] is active.

#### isItemChoice () → {Boolean}
Checks if [Item Selection Process] is active.

#### isNumberInput () → {Boolean}
Checks if [Number Input Process] is active.

#### isRTL () → {Boolean}
**@MZ** Checks if the text contains right-to-left content (e.g., Arabic).

#### itemChoiceItypeId () → {[Number](Number.md)}
Returns the [Item Type].

#### itemChoiceVariableId () → {[Number](Number.md)}
Returns the [Variable] ID for choice assignment.

#### newPage ()
Generates the next page.

#### numInputMaxDigits () → {[Number](Number.md)}
Returns the [Number of Digits].

#### numInputVariableId () → {[Number](Number.md)}
Returns the [Variable] ID for numeric assignment.

#### onChoice (n)
Handler called when a choice is made.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `n` | [Number](Number.md) | Number of the selected item |


#### positionType () → {[Number](Number.md)}
Returns the [[Window Position]](Game_Message.md#window-position) of the message window.


#### scrollMode () → {Boolean}
Whether scrolling is enabled.


#### scrollNoFast () → {Boolean}
Whether [No Fast Forward] is enabled.


#### scrollSpeed () → {[Number](Number.md)}
Returns the scroll speed.


#### setBackground (background)
Sets the [Background] of the message window.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `background` | [Number](Number.md) | [[Background]](Game_Message.md#background) (default: 0) |


#### setChoiceBackground (background)
Sets the [Background] for choices.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `background` | [Number](Number.md) | [[Background]](Game_Message.md#background) |


#### setChoiceCallback (callback)
Sets the callback function for choices.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `callback` | function | Callback function |


#### setChoicePositionType (positionType)
Sets the [Window Position] for choices.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `positionType` | [Number](Number.md) | [[Window Position]](Game_Message.md#window-position) |


#### setChoices (choices, defaultType, cancelType)
Sets the [Choices].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `choices` | [Array](Array.md).&lt;[String](String.md)&gt; | Choices |
| `defaultType` | [Number](Number.md) | Type of [Default] |
| `cancelType` | [Number](Number.md) | Type of [Cancel] |


#### setFaceImage (faceName, faceIndex)
Sets the [Face].

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `faceName` | [String](String.md) | File name |
| `faceIndex` | [Number](Number.md) | Number |


#### setItemChoice (variableId, itemType)
Sets the variable and [Item Type] simultaneously.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `variableId` | [Number](Number.md) | [Variable] ID |
| `itemType` | [Number](Number.md) | [Item Type] |


#### setNumberInput (variableId, maxDigits)
Sets the variable and [Number of Digits] simultaneously.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `variableId` | [Number](Number.md) | [Variable] ID |
| `maxDigits` | [Number](Number.md) | [Number of Digits] |


#### setPositionType (positionType)
Sets the [Window Position] of the message window.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `positionType` | [Number](Number.md) | [[Window Position]](Game_Message.md#window-position) (default: 2) |


#### setScroll (speed, noFast)
Sets the scroll speed and [No Fast Forward] simultaneously.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `speed` | [Number](Number.md) | Scroll speed |
| `noFast` | Boolean | Whether [No Fast Forward] is enabled |


#### setSpeakerName (speakerName)
**@MZ** Sets the [Name] field of the message.

##### Arguments

| Name | Type | Description |
| --- | --- | --- |
| `speakerName` | [String](String.md) | [Name] |


#### speakerName () → {[String](String.md)}
**@MZ** Returns the content of the [Name] field of the message.
