


               ~ Final Fantasy 4: Stasis ~



 Version 0.90
 El Forko
 theForkMan@protonmail.com


Contents:  (search for the tag with the @ symbol to jump to a section)

@PATCHING  - Instructions on how to patch the rom
@OVERVIEW  - Short description of what this mod is
@CHANGES   - Full list of changes
@DAMAGE    - A breakdown of how damage is now calculated
@BETA      - What's left to do before version 1.0
@FAQ       - Frequently Asked Questions
@THANKS    - Folks who's work made this possible



  @PATCHING


This mod requires the 1.1 US version of the Final Fantasy 2/4j SNES ROM.

You have two options for patching: 
1) Patch it with the included FF4_Stasis.ips file
    (If you don't already have a patcher, you can find an online one here: https://www.romhacking.net/patch/ )
2) Go to https://theforkman.github.io/ and use the patching tool
    (this is probably easier, since it'll automatically troubleshoot any potential issues)

If patched successfully, you should have a playable FF4_Stasis.smc file,
 the title screen should say "STASIS" at the bottom when you start the game,
 and it should have a SHA-1 hash of 9770E92203D2797F1A10344DD03C8087B16AB2D6
 (you can check the MD5 sum here: https://www.romhacking.net/hash/ )

You should also have an ArmorGuide.pdf file, which contains a full list of armor in the game.






  @OVERVIEW



This mod provides a fairly substantial overhaul to the game's mechanics, while leaving the world and story intact. My goal was to preserve the general feel of the original game, while having the battles and resource management challenge my adult brain the way they challenged my kid brain when I first played vanilla.


Here's a bird's eye view of what this mod does (for a complete list, see the CHANGES section)

 - Character stats have undergone major changes: Defense and Vitality have been vastly improved and a single Evade stat has replaced the other defensive stats.  Magic Defense is now a single stat that mitigates a percentage of magic damage.  Will now determines how strong Summons are in addition to White Magic

 - Levels and XP are gone: your characters now have the same base stats throughout the game

 - All weapons and armor have been redesigned.  Equipment is now the only way to boost your character's stats, and choosing your armor provides more flexibility in how you prioritize and build your characters

 - All enemy stats have been adjusted, and some enemy behavior has been changed

 - The physical damage algorithm has been rewritten; see the DAMAGEALGO section for details

 - The power and cost of all spells has been adjusted, cast times have been removed, and some spells have been altered in other ways.  Certain spells are now learned from NPCs

 - The end-game experience has been changed to be a bit more open-world: the Sylph and Summons cave are now about as difficult as the Lunar Subterrane is, and the optional bosses have been redesigned


This mod was designed to be a bit harder than vanilla, but not like a crazy hardcore level of difficulty.

The training room has been updated with info about this mod, make sure to visit it!






  @CHANGES



Here's a full list of changes this mod makes:


 Character Growth and Stats

 - XP and Levels have been removed

 - Characters have the same base stats throughout the game.  HP and MP will never change, but Str Vit Wis and Wil can be increased by equipment

 - The damage equation has been reworked, so that damage is less random and the damage mitigation of armor is more consistent (for more information about this, see the DAMAGE section)

 - Vitality has been changed so that it is now as important for physical defense as strength is for physical offense

 - The ATB system was pretty broken in vanilla; it's been fixed so Agility actually does what it should

 - In vanilla there were three "Defence"(sp) values and three "Mag Def" values; these have been replaced with just Defense, Evasion, and MBlock.  Evasion and MBlock work like you'd expect from later Final Fantasy games: Evasion is the probability that the enemy will 'Miss!' your character, and MBlock is a percentage reduction in magic damage

  (For a detailed breakdown of how damage is now calculated and what stats do, see the DAMAGE section below)



 Equipment

 - All equipment stats have been modified.  A few new items have been added, and many have been removed

 - All spears are now 2-handed, and many of Cecil's swords are too (2H swords now use what was the holy sword icon in vanilla)

 - The "arm" equipment slot is now only for rings, which act more like accessories from FF7 than armor

 - Rings are now the only equipment that provide elemental protection (and they no longer make you weak against the opposing element).  These rings also follow the naming convention of later FF games (i.e. the Flame ring protects you against Fire, unlike the Flame Shield in vanilla which protects you against Ice)

  (See the ArmorGuide.pdf file for a full list of armor stats)



 Magic

 - The power and MP costs of all spells have been adjusted

 - Cast times have been removed

 - Magic Defense (MBlock) is now a percentage reduction (in vanilla, it was subtracted from spell power)

 - Lower level spells are now more MP efficient than higher level ones (i.e. Fire3 is 3 times as powerful as Fire1, but costs 5 times the MP).

 - Cure spells aren't as MP efficient as in vanilla

 - A number of spells have been removed

 - Certain spells are now learned from NPCs, with the aid of reagent items

 - "Virus" is now "Bio".  It inflicts Poison instead of Sap, and is Dark elemental (most humans are now weak against Dark)

 - "Blink" now only creates 1 image instead of two, but it's very cheap MP-wise.  A "Blnk2" spell has been added, which creates 2 images but costs more MP.  Edge's "Image" spell still creates two images and retains a low MP cost

 - If a character with a Blink image is attacked, an evasion check is done, and if successful the character doesn't lose an image from the miss



 Abilities

 - Fight does 50% damage from the back row (and also does half damage against back row enemies)

 - Defend halves incoming physical damage (in vanilla Defend doubled Defense)

 - Jump now get's a 25% damage penalty from the back row

 - Most Summon spells are now effected by Will instead of Wisdom

 - Cover no longer works from the back row, and has a chance to fail when covering critical allies (though it does now work with Defend, which, oddly, caused Cover to not work in Vanilla)

 - Dart only works with shurikens and knives now, but does extra damage to flying enemies

 - Sing and Sneak have been removed

 - J abilities have NOT been added back in

  (See the FAQ section below if you're wondering why I made these choices)



 Items

 - Potions are self-cast only now (i.e. the character has to stop and drink it)

 - The "Life" potion is no longer a potion, and can be used on others (I should probably rename it to PhxDown or something)

 - Ether2 and Elixirs have been removed.

 (These changes are also discussed in the FAQ section below)



 Gold

 - GP is sort of a proxy for XP now, since your net worth roughly determines how good your characters stats will be

 - Equipment can now be sold for 90% of the purchase price

 - Consumables only sell for 10% of their buy price (so Ethers and Lifes from chests can't be sold off for easy GP gains).  Arrows and Shurikens sell for 50%



 Random Encounters

 - The scaling of GP dropped from battles is significantly less than in vanilla: early game battles will net you around 100 GP, end game battles around 500gp (though some will occasionally yield valuable items too)

 - If you run from battle, you will always lose half the GP you would have gained from that fight

 - Exit and Smoke cost a decent amount of MP

 - Encounter rates have been significantly reduced



 Saving and Tents

 - You can now save anywhere in dungeons or towns, not just the overworld.

 - You can still only use a Tent at a Sleep point (that's what the 'S' stands for now, "Sleep"!)

 - Cabins have been removed, and Tents fully restore HP/MP/Status



 End-game

 - Cave of Summons and Sylvan Cave are harder than in vanilla  

 - During your first time in the Cave of Summons you won't have Float.  Damage floors do more damage, and Arachne still cast Quake (and it can hurt)

 - Sylvan Cave is now magnetized, and is filled with enemies with high magic defense

 - Dragon enemies are now exclusively found on the moon, and are MUCH more difficult than in vanilla

 - Many chests in these two caves and on the moon are trapped, and some contain enemies that are difficult.  You might want to save before opening chests in these areas

 - A few magical gates have been added to allow for easier transportation around end-game areas.  Gates have to be unsealed before they can be used (don't forget to check upstairs in the house of the Sylphes)

 - You may come across rare gems, like sapphires or emeralds; these currently serve no purpose other than to be sold for GP (though this will change in a future update).  Pearls DO serve a purpose; don't sell them until you've figured out what that is!



 Miscellaneous

 - Any item that has no effect will have a "no effect" message appear, so it's more explicit.

 - Unique items are now unsellable, but can still be given to the Big Chocobo (who no longer requires carrots)

 - Equipment is returned to your inventory when characters leave (note: if your bag is full, equipment will be lost; practically, this shouldn't be an issue, unless you're in the habit of buying potions 1 at a time and not sorting them)

 - NPCs in inns give mod-specific hints






  @DAMAGE



The new damage equation looks like this (offensive stats belong to the attacker, defensive stats to the defender)

     Without bonuses: damage = str*(Random(1.0...1.5)*(attack-0.75*defense)-0.25*defense)/vit

75% of the defender's Armor is subtracted from attacker's Attack power before the 1.0-1.5 randomization happens (and then the remaining 25% is applied afterwards, so there's still some randomness to mitigation).

     With bonuses: damage = BerserkOrJumpBonus*str*(Random(1.0...1.5)*(CritBonus*(RaceBonus+EleBonus)*attack-0.75*defense)-0.25*defense)/vit * HalfIfDefending * HalfIfBackRow

 - The damage bonuses from Berserk and Jump are applied after the 75% armor mitigation happens.  The Critical Hit damage bonus is not (i.e. critical hits have a more noticable damage boost against armored enemies than Berserk and Jump)

 - Elemental and Racial modifiers are still applied to attack power before defense is subtracted, so their attack bonus is still an effective way to circumvent enemy defense.  However, Racial weakness now only provides a 2x boost, Strong Elemental weakness only 3x, and weaknesses now stack via addition instead of multiplication (i.e ele weakness & racial weakness yeilds 3x AP instead of 4x ap, and for strong-ele & racial it's 4x instead of 8x AP).

 - The ratio between your characters armor and average enemy attack power has been raised, and enemy attack power is relatively higher than in vanilla on average, so that your armor's defense has become a lot more important

 - Defense modifiers (i.e. back row and Defend) now halve final damage, instead of doubling defense

 - Monster attacks aren't penalized if from the back row.  Attacks against them are however

 - Curse has been tweaked in that it now halves final damage instead of attack power (otherwise it would make enemies do virtually no damage).  It still halves defense though; this makes curse more dangerous for your characters  

 - Evasion now works more similarly to later FF games: a single roll against evasion determines if your character evades the entire attack.  Accuracy still works per attack multiplier (i.e. low accuracy still means more random damage)

 - Vitality no longer provides a boost to defense; instead, physical damage is divided by it.  For example; if Kain has 14 Vitality and Rydia has 10 and they're wearing the same armor, Rydia will take 140% of the damage Kain would take from the same attack

 - The three magic defense stats ("Mag Def", "Mag Def%" and the Mag Def multiplier) have been replaced with a single "MBlock" stat, which (on average) blocks a percentage of magic damage.



In effect, this all means the following:

 - The damage mitigation from Defense is now much more consistent than it was in vanilla.

 - Increasing Vitality provides more noticeable damage mitigation to characters with low Vitality.  If Cecil has 16 Vitality and puts on a ring with 4+ vitality, his physical damage will be divided by 20 instead of 16, meaning the ring will reduce his physical damage taken by 20%.  If Rydia has 10 Vitality and is given that same ring, her damage will be divided by 14 instead of 10, reducing her damage by 28% (a good deal higher than Cecil's 20%).

 - Increasing Defense provides more noticeable damage mitigation to characters that already have a lot of it.  If Kain has 50 defense and gets attacked by a monster with 70 attack power, he'll get hit for 20x(str&etc) damage.  If his defense is increased by 5 to a total of 55, then that same attack will only do 15x(str&etc) damage; a 25% reduction.  If Rosa has 30 defense and gets hit by that same monster with 70 attack power, she'll take 40x(str&etc) damage (though hopefully she's in the back row, so this will get halved).  Giving her the same 5 defense increase will net her 35 defense, meaning the monster will now hit for 35x(str&etc), only a 12.5% reduction in damage compared to Kain's 25% reduction.

 - Similar to Defense, increasing MBlock provides a more noticeable reduction in magic damage to characters that already have a lot of it.  If Rosa has 50 MBlock and puts on a ring with 5 Mblock, she'll now take 45% magic damage instead of 50%, meaning she'll take 90% of the damage she'd take without the ring (sorry if this is confusing, since we're now talking about multiple percentages...).  If Rydia has 75 MBlock and then puts on that same ring, she'll now take 20% magic damage instead of 25%, meaning she'll take 80% of the damage she'd take without the ring.






  @BETA



 The mod is playable through the end of the game, and complete except for the following points:


 - The four fiends fight has been temporarily removed for the beta.  I'm going to make the fight more challenging, and put it in the Lunar Subterrane (so if you can't beat them, you're not stuck in the Giant of Babil)

 - The Sylph summon is currently removed, but will be put back in after I fix the MP glitch, and tweak how it works

 - A few minor NPCs in towns say the wrong lines

 - The text and visual effects for trade-ins is very basic at the moment.  Going to play with those more.

 - Sylvera is going to be modified and will serve a new function in the game.  For now it's a bit empty...

 - Back attacks are temporarily removed (since they're devastating for back row characters with the algo changes), but I'm going to put them back in in a way that doesn't cause instant caster death.

 - My changes to the ATB system still have some flaws, going to tinker with that some more.

  If you find anything else that seems wrong, please let me know!



Here's a list of things I want to do before releasing version 1.0:


 - Generally improve enemy AI and make fights more interesting

 - Add Protect Shell Haste and Slow back in as statuses like in later FF games (in FF4, they simply modify character defense/speed values)

 - Have Edge start all fights with full ATB, like an inherent "initial strike" 

 - Cap the GP loss at 1k when selling armor (currently you'll lose 2.5k selling a 25k item, which is painful)

 - Going to add a lot more weapons and rings, and a couple new pieces of armor

 - Have the Cover ability be greyed out in Cecil's ability menu when he's in the back row, so it's more obvious that it's disabled in the back row

 - Balance out how Cecil and Kain are a bit underpowered at the moment, and Edge is a little too strong

 - Fix Magic Defense and Evade, they don't work exactly as I like at the moment

 - Make it so if you don't have enough GP to run from monsters, you can't run away (since, the way I see it, you're dropping GP so the monsters stop to pick it up)

 - Have charmed characters only Fight (instead of using MP instensive spells, argh)

 - Have berserked characters only attack front row enemies (so they're not being penalized 50% when attacking bow row enemies)

 - When using a self-berserk spell from certain items, have it refill your ATB gauge so you attack immediately

 - Add boomerangs back in as a re-usable Dart weapon, and add another shuriken or two






  @FAQ



 I haven't actually been asked any of these questions, but these are answers to questions I'm guessing players might have:


- Why remove levels from a Final Fantasy game?

I've personally never liked the idea of levels in fantasy games, going back to D&D.  I mean, I like the dynamic of a character getting more effective in battle from experience if it's done right, but the whole "level" system often results in silly situations, like if mid-level character returns to an early game area where there are wolves or imps or whatever about, and character is buck naked and asleep or paralyed and get's attacked, the wolf biting into that character will do a miniscule amount of damage.  I don't care how strong or experienced a person is: if they're in a situation where a wolf is biting into their uncovered flesh, it's going to do some goddamn damage!  Personally, I'm a huge fan of how Ultima Online handled character progression (that game did a lot of things well... until fucking EA bought it, ugh), and I wish more games took inspiration from the system it used.


- Why are there no whips/harps/etc?

Those weapons rarely if ever had a practical use.  I could have left them in as novelty/RP items (I did enjoy messing with them when I played FF2 as a kid), maybe if enough people want them in this mod I'll put them back in in some form, but for the moment I decided to just cut them.  Although to say more on harps: I just never liked the idea of using a harp as a weapon... I mean maybe to magically effect the psychology of an enemy, but having a harp cause physical damage always felt wrong to me, even if the damage wasn't that much.


- Why are there no J abilities/spells? And why remove Sing?

Those abilities are similar to the weapons I described in my last answer; most of them are kinda useless IMO, except for Palom's Bluff (which is overpowered if spammed), and Cecil's Dark Wave, which is the only one I debated keeping.

As for Sing... maybe I just have a thing against bards in general, but the idea of someone running around and singing in the middle of an intense battle always seemed kinda lame to me.  Also, why do the songs only effect the bad guys, and not everyone that can hear it?  Anyway, I might put it back in to some capacity, maybe a harpless version that always casts lullaby or charm and is more effective, but for now it's just out (and honestly, Edward is probably still more useful in this mod than he is in vanilla)


- Why were so many of Cecil and Kains elemental and racial weapons removed, like the Fire and Ice Swords/Spears, the Ogre Axe, etc?  

Because then practically everyone has a large array of elemental exploiting weapons at their disposal, and it becomes one of those things where when everyone can do it, it's no longer special.  Rydia and Edge can already exploit (non-holy) weaknesses, and Rosa too (if equipped to do so); so I decided to leave Cecil as a beefy healing tank (who can destroy undead enemies) and Kain as a non-elemental heavy hitter (with one or two powerful exploitative weapons at end-game)


- Why is Edge so overpowered?  And why was Dart nerfed?

I went a little overboard and I'm going to correct this in the future.  However, I've often seen people in FF4 forums saying that Edge sucks up until you can have him Dart-spam at the end of the game, and this completely ignores the fact that he can wear claws.  Even in vanilla, if you give him a katana and a claw, he's a goddamn beast against nearly any enemy with a racial or elemental weakness.  I always enjoyed playing him this way, so I decided to give him some decent end-game claws, and nerfed Dart to balance it out.

As for Dart: the way it worked in vanilla didn't make sense to me: Edge did more damage throwing a sword at someone than directly attacking them with it.  And I decided to limit Dart to only shurikens and knives because otherwise... well, I just have this mental image of Edge running around with a bunch of greatswords strapped to his back and belt, tossing them at enemies, which always seemed weird to me.


- Why is there no QOL sprint hack?

Personal preference: In FF6 you move painfully slow without Sprint Shoes, but I always found the move speed in FF4 to be "just right" personally.  If this isn't you and you find the walking speed too slow, feel free to apply the speed QOL hack onto this.


- Why no QOL disable random battles hack?

Random battles are meant to be part of the game IMO.  That being said, I do think the devs totally dropped the ball in vanilla, making the random battles too frequent and too easy, so they ended up being feeling like tedious busywork instead of being interesting or challenging.  My hope is that I've fixed that (or at least made it a bit better).  You still have the options to skip battles, but it now comes at a cost of GP or MP.


- Why isn't there [insert something else common to many other overhaul mods here]

Overall, I wanted to keep the feel of the original SNES game, since it's the game I played so much as a kid and was my first experience with an RPG.  That's another reason why there are no J Abilities, why I left most of the original Spell names, and nearly all of the sloppy translation (though I'm debating maybe changing some of the text that's just flat-out wrong or confusing).  My goal with this mod was to change the way the gameplay felt and make it more satisfying, while leaving the feeling of inhabitting the world of FF2 US pretty much intact.


- Why are potions self-cast/drink only?

I initially wanted to try it just because it made more sense (having to stop for a moment to drink a potion, instead of having your ally crabwalking next to you and bottle-feeding you mid-battle).  Then after I tried it I really liked how it changes the way healing works.  For one thing, it makes White casters instantly more valuable, since they're now the only characters capable of healing other characters.  Also it adds value to the defensive stats of DPS characters and makes having glass-cannons more of a gamble, since they can now only be healed by the one or two characters in the party with White magic (or they have to forfeit a turn themselves to drink a potion).


- Why are Cure spells so weak?!

This gives more value to defensive stats and gear, and rewards good healer MP management and using Cover.


- Why no Ether2 or Elixir?

IMO, high MP restore items screw with the healer MP management dynamic of boss fights.  Either a boss is designed with the expectation that the player won't grind for GP to be able to spam those items for rapid MP regain (which makes the boss easy in exchange for tedious grinding), or the boss is designed to require such items (which then requires tedious grinding).

Sometimes in games I found the presence of such consumables interesting (e.i. I'm in some boss fight and an Elixir would be a huge help, but I'm hesitant to use it since it's rare), but usually I just end up hording them for the final boss.  Since with this mod I've nerfed heals so much and decreased the MP efficiency of high level heal spells, I'm hoping that those interesting "should I use it or not?" choices that came with Elixirs in vanilla will now come from the choice of which healing spells to use and how much MP to burn.


- Cover is broken, sometimes it doesn't work!

Cover no longer works if Cecil is in the back row, and has a small chance of failing on critical characters (this is so that intentionally getting a character's HP down to critical is no longer a fail-safe strategy to protect them against enemies that don't cast)


- Why is armor so expensive, while weapons and rings are so cheap?

Armor is now the main way to boost character stats, so expensive armor makes GP act a bit like XP did in vanilla (i.e. more GP = better stats).  I initially made weapons expensive too, but this incentivized players to sell any weapons they didn't have equipped, and I wanted to keep the feeling from the original game of having multiple tools in your bag to deal with any situation (i.e. enemies with different elemental or racial weaknesses).

Funny thing is, after I made this decision, I googled around and found out that this is actually kind of accurate to how things were in medieval times: a suit of armor back then would cost a fortune, and a high quality sword cost only a fraction of what a full suit of armor would cost.  Sure, you could argue that a magical ring or a magical sword would fetch a good amount of money too... and I guess I don't have a good counter argument for that... but uhm, let's just say that most shop keepers aren't equipped to recognize and appraise magical artifacts, and that's why they don't offer good money for them.


- Why change it so you can save anywhere?

Being limited to saving at save points usually means you have to waste a bunch of time getting back to a boss fight.  It's one thing in a Mario game or a platfomer where it takes skill to get back to the end of a level, but in Final Fantasy it's more just an investment of time (and a test of one's patience).  While that invested time does potentially make the player more emotionally invested in the outcome of a boss fight, the trade-off isn't worth it IMO.  So, now you can save right before a boss fight, and if you die you can jump right back to the beginning of the fight.






  @THANKS



This mod wouldn't have been possible without the following people:


Aexoden, chillifeez, Crow! for answering my nooby questions and helping me learn the basics of general romhacking, how to hack FF4 specifically, and helping me take my first steps into assembly hacking (like figuring out where the physical damage code is and how it works, where the sell-back price code is, and how to do the GP flee code).

Pinkpuff for making FF4kster open source, which was a massive help in figuring out how to modify practically everything in the game.

Everything8215 for making FF6tools and his public Final Fantasy IV Dissassembly, which was a huge help in figuring out how to do certain assembly hacks.

Thanks again to Crow! for making the TLS Equipment Screen Mod, Grimoire LD and chillifeez for the Critical Hit Fix patch, and Dragoon ZERO for the Long Range Fix patch.

Bond617 for hosting his site rb.thundaga.com after slick productions went down (though sadly it's down now too), along with the docs he wrote.

Thanks by extension to everyone who made their work possible (especially whoever it was that wrote the Tower of Babil docs).

BTB, Synchysi, and everyone else involved in making the FF6 Brave New World mod, which inspired me to get into romhacking in the first place.


