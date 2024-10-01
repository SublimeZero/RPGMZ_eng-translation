[Class Tree](index.md)

# Class: [RPG](RPG.md).UsableItem

## Superclass: [RPG.BaseItem](RPG.BaseItem.md)
Basic information about items and skills.

### Subclasses

* [RPG.Skill](RPG.Skill.md)
* [RPG.Item](RPG.Item.md)

### Properties

| Identifier | Type | Description |
| --- | --- | --- |
| scope | [Number](Number.md) | [Range](#範囲) |
| occasion | [Number](Number.md) | [Usable Occasion](#使用可能時)  |
| speed | [Number](Number.md) | [Speed Modifier] |
| successRate | [Number](Number.md) | [Success Rate] % (0–100) |
| repeats | [Number](Number.md) | [Repeat Count] (1–9) |
| tpGain | [Number](Number.md) | [TP Gain] (0–100) |
| hitType | [Number](Number.md) | [Hit Type](#命中タイプ) |
| animationId | [Number](Number.md) | [Animation ID](#アニメーションid) |
| damage | [RPG.Damage](RPG.Damage.md) | [Damage] |
| effects | [Array](Array.md).&lt;[RPG.Effect](RPG.Effect.md)&gt; | Array of [Effects] |

#### Range
Combination of faction (none, enemy, ally, enemy & ally, user)<br />
Number (single, all, random)<br />
Condition (alive, incapacitated, unconditional)<br />
can specify the following patterns.

| Number | [Range] |
| --- | --- |
|  0 | None |
|  1 | Single Enemy |
|  2 | All Enemies |
|  3 | Random 1 Enemy |
|  4 | Random 2 Enemies |
|  5 | Random 3 Enemies |
|  6 | Random 4 Enemies |
|  7 | Single Ally (Alive) |
|  8 | All Allies (Alive) |
|  9 | Single Ally (Incapacitated) |
|  10 | All Allies (Incapacitated) |
|  11 | User |
|  12 | **@MZ** Single Ally (Unconditional) |
|  13 | **@MZ** All Allies (Unconditional) |
|  14 | **@MZ** All Enemies and Allies |

#### Usable Occasion

| Number | [Usable Occasion] |
| --- | --- |
| 0 | Anytime |
| 1 | Battle Screen |
| 2 | Menu Screen |
| 3 | Unusable |

#### Hit Type
hitType is defined as a constant in [Game_Action](Game_Action.md). It is used in forms like <code>Game_Action.HITTYPE_CERTAIN</code>.

| Number | Constant | [Hit Type] |
| --- | --- | --- |
| 0 | HITTYPE_CERTAIN | Guaranteed Hit |
| 1 | HITTYPE_PHYSICAL | Physical Attack |
| 2 | HITTYPE_MAGICAL | Magical Attack |

#### Animation ID
The ID set in [Database]-[[Animation](RPG.Animation.md)].

| ID | [Animation] | Description |
| --- | --- | --- |
| -1 | Normal Attack | The animationId of the equipped [RPG.Weapon](RPG.Weapon.md) is used |
| 0 | None |
| 1+ | Any | Content set in [Animation] |

If no weapon is equipped for [Normal Attack], the ID from [Game_Actor.bareHandsAnimationId()](Game_Actor.md#barehandsanimationid---number) (default: 1) is used.
