You are the attacker.
Choose an attack.

Determine what level of skill, if any, to apply to the attack roll.
The numerical value of that skill level is $skill.

Sum all magical bonuses to the attack roll.
The sum is $atkbuff.
$atkbuff = min(3,$atkbuff).

For each penalty to the attack roll, determine its type.
For each type of penalty, choose one penalty with the greatest absolute value.
Eliminate all penalties that were not chosen. Untyped penalties are always chosen.
Sum the remaining penalties.
The sum is $atkmalus.

The attack may list an "accuracy" ability (in the form "Acc Dex," etc).
If an accuracy ability exists:
	your modifier to that ability is $atkmod;
	determine the target's evasion as follows:

		int $evasion = 10;

		the target's Dexterity modifier is $evamod;

		sum all equipment bonuses to the target's evasion;
		the sum is $evawear;

		sum all magical bonuses to the target's evasion;
		the sum is $evabuff;
		$evabuff = min(3,$evabuff);

		for each penalty to the evasion defense, determine its type;
		for each type of penalty, choose one penalty with the greatest absolute value;
		eliminate all penalties that were not chosen (untyped penalties are always chosen);
		the sum of the remaining penalties is $evamalus;

		$evasion += $evamod + $evawear + $evabuff - $evamalus;

	if 1d20 + $atkmod + $skill + $atkbuff - $atkmalus < $evasion:
		break; // you miss and the attack ends without effect

The attack may list a "damage" ability (in the form "Dag Str," etc).
If a damage ability exists:
	your modifier to that ability is $atkmod;
	determine the target's armor as follows:

		int $armor = 10;

		the target's Constitution modifier is $acmod;

		sum all equipment bonuses to the target's armor;
		the sum is $acwear;

		sum all magical bonuses to the target's armor;
		the sum is $acbuff;
		$acbuff = min(3,$acbuff);

		the number of bruises the target has is $bruise;

		for each penalty to the armor defense, determine its type;
		for each type of penalty, choose one penalty with the greatest absolute value;
		eliminate all penalties that were not chosen (untyped penalties are always chosen);
		the sum of the remaining penalties is $acmalus;

		$armor += $acmod + $acwear + $acbuff - $bruise - $acmalus;

	if 1d20 + $atkmod + $skill + $atkbuff - $atkmalus < $armor:

		determine your size category, then modify that result if you have the Might feature;

	/*

	Might -
If you are smaller than Large and your Strength is 15 or greater, you deal damage as though you were Large.
If you are smaller than Huge and your Strength is 19 or greater, you deal damage as though you were Huge.
If you are smaller than Gargantuan and your Strength is 22 or greater, you deal damage as though you were Gargantuan.

	*/
		consult table Combat by Size Category, finding the row in Column 1 - Size corresponding to your size;
		the entry in Column 5 - Damage corresponding to that row is $damage;
		the attack may provide a "harm" rating $harm;
		$harm += $damage;

		the target gains bruises equal to $harm;
		break; // you miss and the attack ends, inflicting bruises

The attack may list a "power" ability (in the form "Pow Wis," etc).
If a power abiliy exists:
	your modifier to that ability is $atkmod;
	determine the target's focus as follows:

		int $focus = 10;

		the target's Wisdom modifier is $fosmod;

		sum all equipment bonuses to the target's focus;
		the sum is $foswear;

		sum all magical bonuses to the target's focus;
		the sum is $fosbuff;
		$fosbuff = min(3,$fosbuff);

		the number of feedback the target has is $feedback;

		for each penalty to the focus defense, determine its type;
		for each type of penalty, choose one penalty with the greatest absolute value;
		eliminate all penalties that were not chosen (untyped penalties are always chosen);
		the sum of the remaining penalties is $fosmalus;

		$focus += $fosmod + $foswear + $fosbuff - $feedback - $fosmalus;

	if 1d20 + $atkmod + $skill + $atkbuff - $atkmalus < $focus:
		break; // you miss and the attack ends without effect

All three defenses have now either been ignored or beaten on a d20 roll.

Find any text in your special attack or action that says the attack is "lethal."
If you find any, $damage += 1. Apply this only once.

Determine the damage types of the attack (piercing, bludgeoning, etc).
The number of the attack's damage types to which the target has weakness is $weakness.
For each of the attack's damage types to which the target has resistance, $weakness--.

$weakness = min(1,$weakness).
$weakness = max(-1,$weakness).
$damage += $weakness.

Find any text in your special attack or action that says the attack is "nonlethal."
If you find any, $damage = 0.

If damage > 0:
	the target receives $damage injuries;
else:
	if the target is Staggered:
		if the target has at least one injury:
			the target falls unconscious;
		the target receives one injury;
	if the target is Alert:
		the target is Staggered.

Process falling unconscious or dying as necessary.
