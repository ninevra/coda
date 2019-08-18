	THE NEW LEVEL

The "new level" or "newlevel" is the currency of character advancement.
New levels are associated with a character and are not transferable.
"You" are the character in possession of the new levels.

You gain new levels at character creation (5 by default).
The GM may award new levels at any time after character creation, usually one at a time.
Traditionally, the receipt of a new level is called "leveling up."

New levels can be "spent" or "forfeited".  New levels are usually
spent to gain feats, though other ways of spending them exist.  More
on this later.

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

At the end of the training period, you may spend a level and then gain a feat of your choice, and then repeat this process any number of times.

At the end of a training period, you may also "retrain" once.
Forfeit a feat of your choice.
Acquire a new feat of your choice.
(You must still satisfy all prerequisites of all of your feats after retraining; see below.)
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

A feat's description may list one or more "prerequisites."
Prerequisites are conditions that must be met in order to gain the feat.
Any time you retrain or spend a level to gain a feat, you must meet all prerequistes of all your feats, both before and after.
// TODO: this prohibits character advancement too often.
For example, to gain a feat with "Prerequisite: Character level 6," your character level must be at least 6.
(Note that, since levels are spent before feats are gained, a level 5 character may train and spend a level to gain such a feat.
They spend a level, bringing their character level to 6, and then gain the feat.)

Some feats belong to one of three organizational structures: the Class, the Specialization, and the Discipline.
A feat's description will note its membership in a class, specialization, or discipline, along with a number, called its "level," that describes its position in the structure.
For example, "Arcane Ward" might be an "Abjurer 3" feat, indicating that it belongs to the Abjurer specialization at level 3.

	CLASSES

Class feats are also called "class levels" for legacy reasons.

A class feat has two implicit prerequisites, not noted in the prerequisites section of the feat:
 * character level of at least the feat's level
 * possession of every lower-level feat in the class

// Example
// If you are level 7 and training, you may take Rogue 8 if you have Rogue 6 (the next lowest Rogue class level).
// If you are level 6 and training, your level is too low to take Rogue 8 even if you have Rogue 6.
// If you are level 6 and spend two new levels while training, remember that these levels are spent one at a time.
// This means that after you spend the first new level, you will be character level 7 and thus eligible to use the second new level acquiring Rogue 8.
// This means that you can acquire Rogue 6 and Rogue 8 in the same training session if you spend multiple new levels.

	SPECIALIZATIONS

Specialization feats are also called "subclass levels," "prestige levels," and "prestige class levels" for legacy reasons.

A specialization feat has three implicit prerequisites, not noted in the prerequisites section of the feat:
 * character level of at least the feat's level
 * you must already have every lower-level feat in the specialization. // TODO fix this, it's just wrong
 * you must not have any other feat from the same specialization with the same level.

// TODO add example

	DISCIPLINES

A discipline feat has two implicit prerequisites, not noted in the prerequisites section of the feat:
 * character level of at least the feat's level
 * acquiring the feat cannot result in you having more feats from this discipline of this level than of any single number less than it. // TODO fix this, it's got holes in
// TODO possibly rename "prerequisite" to "requirement" and then change the second implicit discipline prerequisite to "at least as many lower-indexed feats from this 

// Example
// If you have two Athletics 2 feats and an Athletics 4 feat, you can train to take a new Athletics feat at levels 2, 4, or 6.
// You cannot take two Athletics 4 feats, as this would result in you having three Athletics 4 feats, which is more than your number of Athletics 2 feats.
// If you wanted a third Athletics 4 feat, you would have to take a third Athletics 2 feat first.
