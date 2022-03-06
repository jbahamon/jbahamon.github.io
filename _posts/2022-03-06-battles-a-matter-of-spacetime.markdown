---
layout: single
title:  "Battles: A matter of spacetime"
date:   2022-03-06 16:33:00 -0300
categories: jrpgs
---

Progress is slow but steady on Kadath! I'm developing the battle system at 
the moment, and wanted to write a bit about my observations.


## The Games

I will try to limit myself to the games from Kotaku's 
[20 JRPGs You Must Play](https://kotaku.com/the-20-jrpgs-you-must-play-1222229344). 
They are:

- Chrono Trigger
- Dragon Quest VIII
- Earthbound
- Final Fantasy VI
- Final Fantasy VII
- Final Fantasy IX
- Illusion of Gaia
- Kingdom Hearts II
- Lost Odyssey
- Lufia 2
- Lunar 2: Eternal Blue Complete
- Ni no Kuni
- Persona 5
- Phantasy Star IV
- Radiant Historia
- Suikoden II
- Super Mario RPG
- The Legend of Heroes: Trails in the Sky
- Xenogears

I might include other examples if I find them interesting enough. I'll
also skip Final Fantasy Tactics since I kinda consider Tactical RPGS
their own genre.

## About Time

How does a game interleave the player party's actions and the enemies'
actions? This is solved in various ways by games, some of which I'll
try to describe now. We'll go from the most abstract ones to the more 
real-like systems.

### Round-based

In a game with round-based combat, battle is divided in rounds where
the player inputs actions for each of their characters, and then each
combatant takes a single action depending on their speed. This means
that speed only determines if a characters acts earlier in a given
round: the only thing that matters is whether their speed is higher
or not. For example, in a battle between two characters, it doesn't
matter if the fastest character has two times or ten times the
other's speed: the action order will be the same.

Some examples:

- Dragon Quest VIII
- Earthbound
- Lufia 2
- Lunar 2: Eternal Blue Complete
- Phantasy Star IV
- Suikoden II
- Super Mario RPG

- Lost Odyssey

In addition to the acting character's Speed stat, turn order is also
affected by character's Casting Time and the action's Casting Speed.
Some actions might take multiple rounds to execute, and they can be
delayed if the character is hit by attacks under certain conditions.

- Persona 5

Persona 5 doesn't have rounds, but instead strictly interleaves
actions between the player and the enemy sides. Roughly, the fastest
entity from either side goes first; the highest-agility entity from
the opposite side goes next and so on. The system has slightly
different behavior for bosses, ambushes, preemptive attacks and
battles with an uneven number of fighters on each side, but that's
the general gist of it.

### Queue-based

This type of battle system takes into account the relative difference
in speed between characters. The battle system has an internal,
global, non-real time clock; each character's speed determines how
many clock ticks must pass before they can take another action. In
this way, a character that has ten times the speed of another might
need wait for a tenth of the ticks, so it can act ten times before
the other makes a move. The clock is fast-forwarded programatically
to the next action each time, so there's no waiting actually
involved.

Used in:

- Radiant Historia
- The Legend of Heroes: Trails in the Sky

### Active-time battle

ATB stands for Active Time Battle. The system adds action gauges for
each character and enemy; these gauges refill in real time. Once a
character's gauge is filled, they can perform an action, which
depletes their gauge. This, in effect, combines aspects of turn-based
combat and real-time combat. Usually, only the player's party
members' gauges are visible.

A problem with this system concerns menus. If the action gauges keep
on refilling while selecting actions or items(usually called 'active'
ATB), battles can be decided by how quickly the player can navigate
menus, since enemies will perform attacks while the player is busy
with the UI. This means the UI becomes an extra 'enemy' for the
player. On the other hand, if action gauges don't refill while
navigating menus (usually called 'wait' ATB), it's easy for the
player to resort to opening a menu and planning their next action
from there, thereby eliminating the active aspect of the system.
Another problem is that sometimes the player can be just waiting for
ATB gauges to fill: while it might create moments of tension, it can
also get boring.

Used in:

- Chrono Trigger
- Final Fantasy VI
- Final Fantasy VII
- Final Fantasy IX
- Xenogears

In Xenogears, once a character's ATB gauge fills up, they receive an
amount of Action Points which they can then spend. Each action has
its own AP cost, and the player can keep inputting commands as long
as they have APs left.

### Pausable real-time

These games feature real-time combat, but some UI interactions or
actions either slow down time or completely pause the action,
allowing the player to make more strategic choices.

Used in:

- Ni no Kuni:

The battle pauses while you choose a party member to
control and enemies to target, but you can freely move around and
perform actions in real time as attacks are performed. Special
actions act as as cutscenes that pauses battle.

- Final Fantasy VII Remake

### Strict real-time

These battle systems are pretty much stepping into hack-and-slash
territory. Since actions and decisions are made in real time, actions
tend to be bound to button combinations or simple inputs, to avoid
forcing the player to navigate multiple menus.

Used in:

- Illusion of Gaia
- Kingdom Hearts II


## About Space

Does the distance between characters affect what they can do? Can they
move in the battlefield? Does it matter? Again, games answer these
question in different ways. These are some of those, going from the
more restricted/abstract to the more free/realistic.

### None or very limited

Some games don't consider spatial positioning at all as a factor. The
party is usually rendered in a row facing the enemies, usually also
in a row. Attacks target one or multiple characters, but their
relative position is not taken into account.

Used in:

- Dragon Quest VIII
- Earthbound
- Persona 5
- Phantasy Star IV
- Super Mario RPG
- Xenogears

- Pokémon

While Pokémon games normally don't consider spatial positioning, the
fifth generation of Pokémon games (Black/White/Black 2/White 2)
introduced Triple Battles, where three Pokémon on one side fight
against three on the other. In these battles, some moves take into
account whether a Pokémon is adjacent to another: for example,
Selfdestruct will damage all adjacent Pokémon. If the Pokémon using
Selfdestruct is in the left or right spots, it will hit two of the
opposing Pokémon and one of its allies, while if it's on the center
it will hit all three opponents and both of its allies.


### Row system

Some games use the concept of a front row and a back row, where
characters placed in the front row deal more damage, receive more
damage, or both; characters in the back row deal more damage, receive
less damage, or both. There are usually some ways to circumvent the
attack reduction for back row characters: using ranged weapons or
spells, for example.

Used in:

- Final Fantasy VI, Final Fantasy VII

Only the party has a front and a back row. A back attack from an enemy
starts a battle where the front and back row assignments start out
reversed. Additionally, some battles can be a 'pincer attack', where
the party is attacked by a group of enemies to its left and one to
its right. Attacks that usually affect all enemies will only affect
one of the groups at a time.

- Lost Odyssey

Both the enemies and the party have front and back rows. The total
amount of HP of characters in the front row determines the bonuses
characters in the back row get.

- Lufia 2

Only the party has front and back rows, each of them able to hold 2
characters. The second character in the front row also gets damage
reduction, but to a lesser extent than those in the back row.

- Suikoden II

Both the enemies and the party have front and back rows. In addition,
depending on the weapon wielded by a character, they're classified as
short, medium or long range. Short range characters can only hit the
enemies in the front row, and only from the front row; medium range
characters can attack the front row enemies from both the front and
back row; finally, long range characters can attack both the front
and back row of enemies from both the front and back row.

### Grids

These games feature a grid where characters are positioned. Usually,
this means both party characters and enemies can perform actions that
change their position in the grid. Attacks can affect
variously-shaped grid areas (lines, crosses, etc) allowing characters
to take advantage of their enemies' formations. This means formations
can become very relevant for battle. In fact, a whole genre spawned
from this: the Tactical RPG genre.

- Lunar 2: Eternal Blue Complete
- The Legend of Heroes: Trails in the Sky

- Radiant Historia

Curiously, Radiant Historia uses a very small (3x3) grid for enemies,
which work like rows. The player characters do not have any sort of
spatial positioning, but they do have spatial-related actions that
can reposition enemies, damage certain grid patterns, etc.

### Free 2D

These games allow players and enemies to be freely positioned in a 2D
arena; relative positioning affects attacks. Concepts like range back
attacks can become very relevant. Usually used in real-time battles,
where the user can reposition freely as they choose their actions.

Used by:

- Illusion of Gaia
- Ni no Kuni

- Chrono Trigger

In Chrono Trigger's battles, both enemies and the player's party are
freely positioned in the screen. Notably, while most enemies
constantly move over the battlefield, and some enemy attacks can move
the party characters around, the player has no way of repositioning.
Some attacks and techniques take into account spatial positioning:
some hit all enemies in a line that passes through the attacker;
others hit the vicinity of an ally or an enemy. 


### Free 3D

In addition to free 2D movement, some games include jumps and other
acrobatics that make use of vertical space in order to evade attacks,
reposition and attack. This, again, is close to hack-and-slash and
action-adventure games.

Used by:

- Kingdom Hearts II



----

That's it! I think I'm going with a Queue system similar to Radiant
Historia for time management, and a Free 2D system for spatial
positioning similar to Chrono Trigger (but with some way to let the
player reposition). We'll see how that goes!