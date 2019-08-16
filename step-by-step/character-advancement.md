	THE NEW LEVEL

The "new level" or "newlevel" is the currency of character advancement.
New levels are associated with a character and are not transferable.
"You" are the character in possession of the new levels.

You gain new levels at character creation (5 by default).
The GM may award new levels at any time after character creation, usually one at a time.
Traditionally, the receipt of a new level is called "leveling up."

New levels can be "spent" or "forfeited".  The most common way to spend new levels is to gain feats, though other ways exist.  More on this later.

	THE CHARACTER LEVEL

Each character has an integer value called "character level" or simply "level."
"Your" level is your character's level.

A character's level is equal to the number of new levels they have ever spent, or the level cap, whichever is lower.  The "level cap" is 24.  If your character level would increase beyond the level cap, it instead does not.  You may continue to spend new levels when your character level is 24, but you cannot acquire feats except through retraining.

If new levels would be spent simultaneously (such as when choosing a high-level race during character creation), instead they are spent one at a time. // Like drawing cards in Magic: the Gathering.

	TRAINING

Rules may tell you to spend new levels to complete a task, most likely during character creation.
Outside of these special events, you may only voluntarily spend new levels through "training."

Your character must spend an amount of narrative time practicing a set of abilities they wish to acquire.
This amount of time may be just minutes of reading a user's manual or even a single flash of inspiration, or it may be years at a remote monastery, depending on the needs of the narrative.
It should not be an amount of time that disrupts the progress of gameplay; characters should be ready to resume their adventure when needed.

At the end of the training period, you spend any number of new levels and acquire the same number of feats of your choice.
Feats may list prerequisites. You must meet all prerequisites for any feat in order to acquire it.

At the end of a training period, you may also "retrain" once.
Forfeit a feat of your choice, provided that no other feat you have requires you to have it.
Acquire a new feat of your choice.
Training periods for retraining may take significantly more narrative time than ordinary training periods.

	FEATS AND FEATURES

A "feature" is a block of rules text, from a single sentence up to multiple paragraphs.
Some features have names. Some do not.
Characters are said to "have features." These features' rules apply to the character.
Writing your features, or at least their names, on your character sheet is common practice.

Additional copies of named features in a character's rules text are redundant and do not stack.

A "feat" is a named set of feats and features. These names are not unique. // TODO: Pick a hashing algorithm to generate unique IDs for feats.
Feats which are granted by other feats will indicate this fact in their description.
These feats cannot be acquired through training.

Some feats belong to one of three organizational structures: the Class, the Specialization, and the Discipline.
Names of feats contain an Arabic numeral if and only if they belong to one of these three feat families.

	CLASSES

A feat belongs to a class if and only if its name includes a dash ( - ) before the number.
The class contains all feats whose names have the same text before the dash (e.g. "Ranger").
Class feats are also called "class levels" for legacy reasons.

A class feat has two implicit prerequisites, not noted in the prerequisites section of the feat:
	spending a new level to acquire the feat must make your character level equal to or greater than the feat's number;
	you must already have every feat in the class that has a lower number.

// Example
// If you are level 7 and training, you may take Rogue - 8 if you have Rogue - 6 (the next lowest Rogue level).
// If you are level 6 and training, your level is too low to take Rogue - 8 even if you have Rogue - 6.
// If you are level 6 and spend two new levels while training, remember that these levels are spent one at a time.
// This means that after you spend the first new level, you will be character level 7 and thus eligible to use the second new level acquiring Rogue - 8.
// This means that you can acquire Rogue - 6 and Rogue - 8 in the same training session if you spend multiple new levels.

	SPECIALIZATIONS

A feat belongs to a specialization if and only if its name includes a closing angle bracket ( > ) before the number.
The specialization contains all feats whose names have the same text before the dash (e.g. "Abjurer").
Specialization feats are also called "subclass levels," "prestige levels," and "prestige class levels" for legacy reasons.

A specialization feat has two implicit prerequisites, not noted in the prerequisites section of the feat:
	spending a new level to acquire the feat must make your character level equal to or greater than the feat's number;
	you must already have every feat in the specialization that has a lower number.

You cannot take a specialization feat with a name that is the same as any specialization feat you have.

	DISCIPLINES

A feat belongs to a discipline if and only if its name puts parentheses ( () ) around the number.
The discipline contains all feats whose names have the same text before the parentheses (e.g. "Athletics").

A discipline feat has two implicit prerequisites, not noted in the prerequisites section of the feat:
	spending a new level to acquire the feat must make your character level equal to or greater than the feat's number;
	acquiring the feat cannot result in you having more feats from this discipline of this number than of any single number less than it.

// Example
// If you have Athletics (2), Athletics (2), and Athletics (4), you can take Athletics (2), (4), or (6).
// You cannot take (4) twice, as this would result in you having three Athletics (4) feats, which is more than your number of Athletics (2) feats.
// If you wanted a third Athletics (4) feat, you would have to take a third Athletics (2) feat first.
