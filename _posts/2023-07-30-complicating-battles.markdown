---
layout: single
title:  "Complicating battles"
date:   2023-07-30 20:51:00 -0300
categories: jrpgs
---

I've been working on a prologue for the game, which should serve as a demo. 
Battles are still very bare-bones, so improving that is probably next.

Speaking of battles, I've been thinking about how games make turn-based battles 
more exciting. If you think of a turn-based battle where each participant just 
chooses the most damaging option each turn, the outcome of the battle is 
pretty much determined before it starts. So, how can these battles be spiced up?

## Chance

One common option is to add randomness to attacks and effects. This can 
be done in many ways:

- Damage with a (usually) random component, so the same attack on the same 
  target might do slightly different damage each time. 
- Critical hits, where attacks occasionally do increased damage.
- "Reverse" critical hits, where attacks occasionally do less damage or do no 
  damage at all (e.g. missing the target). 
- Attacks that have side effects that only apply occasionally.

Besides making a battle's outcome non-deterministic, this offers the player 
different risk-versus-reward options.

## Non-damaging effects

Another common element is adding attacks that do something other than 
dealing instantaneous damage. This includes:

- Buffs and debuffs, where attacks can modify stats like attack power, 
  defense power, speed, accuracy and others. This will increase or decrease 
  the affected battler's effectiveness in battle.
- Damage-over-time effects, e.g. poison, where smaller damage instances 
  are periodically applied to the affected battler.

This makes the user think about the expected length of the battle: these effects
tend to have a greater impact in longer battles. This, in turn allows for more
elaborate strategies. 

### Resource management

A way to prevent the player from just blasting the enemies with the most effective 
move on every turn is to have a limited resource come into play. For 
example, spells and techniques that require spending magic or skill points: these points 
usually have few or very restricted ways of being replenished mid-battle. 
Health can also be considered a limited resource, one that is usually not spent for 
actions, but one that the user can be allowed to replenish. There are 
some variants for their replenishment:

- While in battle, the resource cannot be replenished.
- While in battle, the resource can only be replenished by using very specific or 
  rare items and skills. Here the first case forces the user to decide whether it's
  worth it to spend these resources; the second usually creates a push and pull 
  where some turns can be spent replenishing resources (e.g. alternating between
  healing and attacking).
- While in battle, the resource automatically replenishes without spending turns
  on it. For example, Limit Breaks and similar systems consist of a bar that
  fills over time or upon some events like characters receiving damage. Once filled,
  a special attack can be used, and the bar is emptied.

Dunno, that's some of the ways I've seen until now. Maybe I'll put some more later!