[Class Tree](index.md)

# Class: [RPG](RPG.md).Class

## Superclass: [RPG.MetaData](RPG.MetaData.md)

| Database    | JSON File     | Global Variable                         | Object        |
|-------------|----------------|----------------------------------------|---------------|
| [Class]     | Classes.json   | [$dataClasses](global.md#dataclasses-arrayrpgclass)(Array) |               |

Referenced by the _classId property of [Game_Actor](Game_Actor.md).

### Properties

| Identifier   | Type                                     | Description                                                                                                          |
|--------------|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `id`         | [Number](Number.md)                     | Class ID                                                                                                            |
| `name`       | [String](String.md)                     | [Name]                                                                                                             |
| `expParams`  | [Array](Array.md).&lt;[Number](Number.md)&gt; | [Experience Curve]<br />The contents of the array (0: Base Value, 1: Correction Value, 2: Increase Rate A, 3: Increase Rate B) |
| `params`     | [Array](Array.md).&lt;[Array](Array.md).&lt;[Number](Number.md)&gt;&gt; | [Ability Curve] (An array of ability values for each level, in the order of [Ability ID](RPG.Enemy.md#ability-id)) |
| `learnings`  | [Array](Array.md).&lt;[RPG.Class.Learning](RPG.Class.Learning.md)&gt; | An array of conditions required to [Acquire Skills]                                                               |
| `traits`     | [Array](Array.md).&lt;[RPG.Trait](RPG.Trait.md)&gt; | An array of [Traits]                                                                                              |

### Inner Class

* [RPG.Class.Learning](RPG.Class.Learning.md)
