---
layout: single
title:  "Menus, Inventories and Items"
date:   2021-02-27 21:16:00 -0300
categories: jrpgs
---

Phew! Been working on a few things. Having chosen a general scene structure
and  a graphical style, I started laying the foundations for
[Kadath](https://github.com/jbahamon/kadath). At the present time, I'm working
a bit on menus and I started looking at other games.


## Menus

I will mainly talk (write?) about the menus used during world exploration
(i.e. local and/or world scenes). Apart from these, we can find other menus
such as the main menu and the battle menu. The former is usually quite simple,
and the latter is better analyzed when talking about battle systems.

In-game menus usually have a few submenus/categories. I will use similar words
whenever possible instead of in-game terms, to simplify a bit:

- **Final Fantasy 6** has Equip, Item, Skills, Relic, Status, Config, Save.

- **Chrono Trigger** has Equip, Item, Skills, Party, Config, Save.

- **Golden Sun** has two menus. The first has Save, Pause, Config; the second
has Psynergy, Djinn, Item, Status.

- **Pokémon** games have some variation, but they usually have Pokédex, Party,
Item, Status, Save, Config.

- **Radiant Historia** has Item, Skill, Stats, Equip, Party.

We can see some of these menu options are present throughout most of all of
these games, so it's relevant to talk a bit about them.

### Equip

Many RPG games offer a degree of customization by letting the player [choose
their characters' weapons, armor and other equippable
items](https://tvtropes.org/pmwiki/pmwiki.php/Main/EquipmentBasedProgression).
This system is usually also used in connection with economy systems (letting
the player sell and/or buy better equipment as they progress through the game)
and quest rewards (e.g. optional side stories that reward the player with
unique or special equipment).

This submenu lets the player choose the equipment that is actually assigned to
each party member. It should clearly display the differences between each
piece of equipment: for example, showing what stats are increased or decreased
if a different armor piece is equipped. Additional effects beyond the strictly
numerical should be mentioned in this screen, too.

Some games have specific equipment split into a different submenu, especially
if it's related to a distinctive game mechanic. Final Fantasy 6 has the
_Relic_ submenu, which is essentially special equipment that can drastically
alter a character's behavior in battle; Golden Sun has the _Djinn_ submenu,
where magical creatures can be assigned to party members in order to
drastically change their abilities and stats. Similar to these is Final
Fantasy 7's _Materia_ submenu, where special items callled _Materia_ can be
assigned to characters to customize their skillset.

The Pokémon games are a special case: the equipment system is greatly
simplified. Each Pokémon can only equip one item, so the Equip submenu is
absent, and equipping items is done through either the Party or Item submenu

### Item

Similar to the equipment system, most games allow the player to keep an
inventory with them at all times. This submenu usually allows the player to
check the items they currently have, dispose of those they don't want, reorder
them and check their in-game description. Some of these items can be used on
the spot, and this submenu should offer that option. 

### Party and Status

These submenus are mostly about displaying information. Some games put the
stuff in this section in the "Party" submenu, while others put it in the
"Status" one. Some dispose of one of these, showing some data in the main menu
screen.

Nevertheless, this includes:

- Checking the party's status such as health, status afflictions, remaining
energy and statistics such as attack, defense, etc. 

- Changing the party's order, if it's relevant.

- Minor statistics such as total play time, in-game money and story progression.

As said before, some games put some of these stuff elsewhere. Final Fantasy 6
has the main menu screen handle general stats and party reordering, while the
Status screen shows detailed stats. Chrono Trigger shows party stats in the
Equip submenu, and the Party submenu only handles party reordering. Pokémon
games have the first two items in the Party submenu, and the last in the
Status submenu. All in all, it depends on the amount of information that has
to be shown to the player. 

### Skill

Some games allow party members to use skills outside of battle. Some games
allow [healing
techniques](https://tvtropes.org/pmwiki/pmwiki.php/Main/TheMedic) to be used
in this fashion, offering an alternative to consumable items for restoring the
party's health (Final Fantasy 6, Chrono Trigger, Golden Sun, Radiant
Historia...). Other skills might affect the environment, such as [removing
obstacles, solving puzzles and help with
movement](https://tvtropes.org/pmwiki/pmwiki.php/Main/AbilityRequiredToProceed)
(Golden Sun, Pokémon). This submenu allows the player to use these skills.

If the game has [progression or learning system for
skills](https://tvtropes.org/pmwiki/pmwiki.php/Main/SkillScoresAndPerks)
(Final Fantasy 6, Chrono Trigger...), this submenu also lets the player check
their progress, what skills can be learned and such. Information about
these skills is also displayed.


### Save

Simple enough, this allows the player to save their progress. Some games allow
the player to save at any time outside of battle (Pokémon). Others allow
saving only at specific [save
points](https://tvtropes.org/pmwiki/pmwiki.php/Main/SavePoint) (Radiant
Historia): this submenu would be disabled at other times. Some take a mixed
approach, letting the player save anytime while in the World Scene, but only
at specific points while in the Local Scene (Final Fantasy 6, Chrono Trigger).


### Config

User preferences. Settings such as text speed, font size, UI styling and input
mapping should be available to edit here. Additional settings usually include
some related to game mechanics, such as limiting battle animations or altering
some of the battle system's aspect.

## Inventories and Items

Some of the previous submenus are related to items the player can obtain
throughout the game. Some games [don't really
limit](https://tvtropes.org/pmwiki/pmwiki.php/Main/HyperspaceArsenal) the
player's inventory. Others [limit the player's
inventory](https://tvtropes.org/pmwiki/pmwiki.php/Main/InventoryManagementPuzzle)
by [establishing a maximum
amount](https://tvtropes.org/pmwiki/pmwiki.php/Main/LimitedLoadout) of
different items that can be carried at a time and/or limiting the maximum
"stacking" of identical items in the player inventory. Some games have more
elaborate limitations, such as assigning a weight value to each existing item,
and [limiting the maximum
weight](https://tvtropes.org/pmwiki/pmwiki.php/Main/CriticalEncumbranceFailure)
that can be carried; other games might use
[grids](https://tvtropes.org/pmwiki/pmwiki.php/Main/GridInventory) to simulate
something closer to a backpack's limitations. At the moment, I'm not really
considering limiting the player's inventory, though.


Instead of trying to organize items in separate classes, I think it's better
to think of them as having [mixins](https://en.wikipedia.org/wiki/Mixin), i.e.
having a combination of capabilities. These are some interesting ones:

### Equipable

Items that are equipable can be assigned to characters to activate their
effect. This usually brings limitations into play: a character, for example,
can only equip one armor set at a time, even if the player has dozens of them
in their inventory; additionally, equipment cannot usually be swapped
once in battle. However, their effect is usually automatic once equipped. Some
equipables have out-of-battle effects, such as faster movement or reduced
random ecounters.

### Usable in-battle

Items that can be directly activated while in battle. For example, items that
temporarily raise the party's defenses, or items that heal status ailments.

### Usable out-of-battle

Items that can be directly activated outside of battle. For example, items
that fully restore the party but can only be used at save points, and items
that let the player escape a dungeon without having to manually backtrack.

### Consumable

Items that disappear from the inventory after directly activating its effects:
for example, [healing
potions](https://tvtropes.org/pmwiki/pmwiki.php/Main/HealingPotion).

### Stackable

The player can have multiple copies of the item. Usually 
plot-important items, whose only relevance is where they're on the player's
inventory or not, can't be stacked.

### Sellable

The item can be exchanged for in-game currency. Plot-important items usually
can't be sold. Sometimes one-of-a-kind equipment can't be sold either, to
prevent player frustration. Some items have this characteristic as their only
[selling (hehe)
point](https://tvtropes.org/pmwiki/pmwiki.php/Main/VendorTrash).

The idea that these are characteristics that can be combined is applied in
many games:

- Some items that can be used outside of battle might not necessarily be
consumed, such as maps, tools involved in solving puzzles and items used for
fast travel.

- Some items can be used both in and outside of battle (e.g. healing potions).

- Most consumables are also stackable, in order to allow using multiple copies of
the item in a short period of time. Most are also sellable.

- **Final Fantasy 6** has items that can be both equipped and used in-battle:
there are Rods that, when used during battle, unleash a strong spell. They are
also consumable, as this usage consumes the item. They can also be equipped as
weapons, in which case they have the usual weapon behavior and are not
consumed. However, Rods that are currently equipped cannot be directly used.

In my implementation, this will probably involve [duck
typing](https://en.wikipedia.org/wiki/Duck_typing), as Godot seems to encourage it.