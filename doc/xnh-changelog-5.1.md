## xNetHack 5.1 Changelog

This is a minor version of xNetHack. It is based directly on xNetHack 5.0, and
consists largely of a merge of the upcoming NetHack 3.7 development code onto
xNetHack.  See doc/fixes37.0 for the devteam's changes.

The xNetHack page at the NetHackWiki, https://nethackwiki.com/wiki/XNetHack,
attempts to describe these changes in a way that's better formatted and more
friendly to players. However, the wiki page might be out of date; in case of
conflicting information, this changelog and others in this directory are more
up-to-date than the wiki page, and the commit messages are more up-to-date than
this changelog.

On top of any changes made by the NetHack devteam on 3.7, and any changes
made in previous xNetHack versions, xNetHack 5.1 contains the following
changes:

### Gameplay changes

- Paper golems are instakilled by decay attacks.
- The Gnomish Sewer's wand of cold is now randomly placed (rather than being
  submerged).
- The Ranger home level is now a regular floor instead of all grass.
- Eating invisibility and see invisible rings grants 600+d200 turns of the
  respective intrinsic (the same as a blessed potion).
- If you arrive on Astral with petless conduct intact, your god will no longer
  send any angel.
- Amnesia scrolls are re-introduced, and behave the same as vanilla 3.7, where
  they make you forget spells and skills, not maps and object discoveries.
  However, instead of having 35 probability like in vanilla, they have only 15
  probability. The scroll of water is not removed.
- Monsters' once-per-twenty-turns regeneration of a hit point now depends on
  their monster ID, rather than all monsters simultaneously regenerating a
  point on every 20th turn.
- Figurines can generate as wood, plastic, metal, copper, or gold in addition
  to being stone.

### Interface changes

- Cavemen/women now get a role-specific message for being banished from the
  quest for changing their alignment.
- More hallucinatory monsters, shirts, epitaphs, random engravings, rumors,
  hallucinatory currencies, hallucinatory gods, hallucinatory blasts, and
  taunts.

### Architectural changes

- Added a new function bury_sink_ring to unify codepaths for doing this between
  regular and special level code.
- Remove all rogue level code, and everything that used it, including support
  for the rogue symbol set. Remove extralev.c completely.
