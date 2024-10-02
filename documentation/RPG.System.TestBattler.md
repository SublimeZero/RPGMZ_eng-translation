[Class Tree](index.md)

# Class: [RPG](RPG.md).[System](RPG.System.md).TestBattler
JSON data used to pass a battler (party member) for [Battle Testing](#).

This will not be used during actual gameplay.

### Properties

| Identifier                  | Type                                           | Description                             |
|-----------------------------|------------------------------------------------|-----------------------------------------|
| `actorId`                   | [Number](Number.md)                           | Actor ID                                |
| `level`                     | [Number](Number.md)                           | Actor's [Level](#)                     |
| `equips`                    | [Array](Array.md).&lt;[Number](Number.md)&gt; | Array of IDs for the actor's [Equipment](#) (0: Weapon, 1: Shield, 2: Head, 3: Body, 4: Accessory) |
