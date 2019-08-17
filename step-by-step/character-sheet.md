	ABILITY MODIFIERS

The six ability scores, as handed down by ancient tradition, are Strength, Constitution, Dexterity, Intelligence, Wisdom, and Charisma.
These are traditionally abbreviated Str, Con, Dex, Int, Wis, and Cha, respectively.
In these rules, the full names of abilities refer to the corresponding ability score, while the abbreviated form always refers to the ability modifier.

The ability modifier is a function of the ability score, of the form:

> $modifier = floor ( max ( $score , 0 ) / 2 ) - 5 .

	LIMBS

Your race determines your starting number of legs and arms, though effects may modify these numbers temporarily or permanently.

For every arm you have, you have a weapon slot (see items.md).

Walking, lifting, and running are deeply instinctive behaviors that are difficult to modify later in life.
As such, if your number of legs ever exceeds the number of legs your race has by default, these extra limbs do not grant you any additional benefit.

In effect, $legs = min ( $initialLegs , $currentLegs ) .

	WEIGHT LIMITS

Weight is measured in nameless "units."
These units are an aggregate score approximating bulk, mass, and other factors that make moving an object difficult.
These units are constant in all environments, atmospheric or gravitational changes notwithstanding.

Items in your item slots are considered to be "worn."
Items you wear that are not described in your item slots, like your basic clothing, are considered to be weightless for convenience.

You can wear up to 3 * Strength units without penalty.
Wearing weight beyond this amount inflicts the encumbered condition.

The weight of items you wear also counts towards the total amount of weight you carry.
Carrying over your carry limit also causes encumbrance.
Your carry limit is a function of your strength, number of legs, and unarmed damage, of the form:

> $carry = 10 * $strength * max ( 1 , $damage ) * max ( 1 , min ( $legs , 6 ) )

You can haul items behind you, as on a sledge, or push things forward, as punting a boat.
The maximum weight you can move is 5 * $carry.

	SIZE CATEGORY

Your race determines your initial size category, though effects may modify it temporarily or permanently.

Your size category determines your space, reach, unarmed damage, injury tolerance, and natural evasion.
The values per size category are given as follows:

	SIZE		SPACE	REACH	DAMAGE	INJURY	EVASION
	Tiny		2.5ft		1	0	Min 4
	Small		5ft		1	1	-
	Medium		5ft		1	1	-
	Large		10ft		1	2	-
	Huge		15ft		2	3	Max 2
	Gargantuan	20ft*		2	4	Max 0

	*or more
