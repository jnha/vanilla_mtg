# vanilla_mtg
A solver in rust for a simplified subset of Magic: The Gathering.

Magic: The Gathering is a trading card game that is very complicated.
There are thousands of cards with unique effects,
many of which fundamentally alter the game.
The game as a whole has been shown to be [turing complete, and therefore uncomputable](https://arxiv.org/abs/1904.09828).

The basic gameplay of magic the gathering revolves around creature type cards.
Players play land cards which tap for mana which is used to play creatures.
Creatures are played onto the battlefield, where they can attack the opponent once per turn to deal damage equal to their power.
Creatures also can block the opponents attacking creatures taking the damage instead and dealing their power as damage to the blocked creature.
A creature dies if it is dealt more damage than its toughness, and is then moved from the battlefield to the graveyard.
The game ends when one players life points are reduced to 0 or below, by taking damage.

This solver attempts to solve a game of Magic: The Gathering from a given position with the following assumptions/modifications:
- perfect information: all cards, in hands and in decks are revealed (normally hidden or revealed to one player)
- perfect play: both sides are assumed to play optimally
- basic lands: all lands are basic lands that tap for one mana and have no abilities
- vanilla creatures: all non-land cards are creatures without any abilities
- colorless mana: mana color is ignored

These simplifications allow for a generic computable solver for a important subset of Magic: the Gathering's combat system.
