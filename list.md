# Introduction

Before we begin, a few notes:

First, my gaming machine runs Windows 7. I don't use Windows 10, because fuck Microsoft. (Yes, I'm aware that Github is owned by Microsoft.) But if you're unfortunate enough to have to use it, just about everything I say here should be applicable to Windows 10. The utilities I recommend should work under Windows 10 just as well as Windows 7. A couple procedures might be a bit different, but you should be able to figure it out.

Second, this mod list is for the original game engine, not [OpenMW](https://github.com/OpenMW/openmw/releases). OpenMW has several advantages and several disadvantages compared to the original engine. The biggest advantage of OpenMW in my opinion is that it runs natively under Linux. Anything that helps us move away from Macroshit Wangblows is a good thing. Probably the biggest disadvantage is that MWSE-lua mods don't work with OpenMW. If you want to use OpenMW, feel free. Most of the mods on this list will work with it, but many won't. I'll be assuming you're using the original game engine.

Third, I have the GOTY CD version of Morrowind. For the most part, which version of the game you have doesn't matter. If you're using the original (non-GOTY) retail CD version, you'll need to install the [last official patch](https://cdn.bethsoft.com/elderscrolls/morrowind/patches/Bloodmoon_v1.6.1820.exe) after installing Bloodmoon. If you have a downloadable version of the game, your procedure for (re)installing the game will be different than mine. But generally everything here is applicable to all versions.

Fourth, you'll need a couple basic utilities before we get started. You probably already have an archive manager that can work with .7z and .rar files, as well as .zip files. If not, there are plenty of good ones out there, so I'll leave it to you to find one you like.

I also recommend using an image viewer that will open .dds files (most texture files for Morrowind are in .dds format). This will help you preview and compare textures. Microshit's default image viewer naturally will not open .dds files. Again, I'll leave it to you to find an image viewer you like; there are plenty of good ones out there.

Also, make sure you have Windows Explorer set to *not* hide extensions for known file types. (To find this setting, in Windows Explorer, go to Tools -> Folder Options -> View.) Microsoft stupidly makes hiding extensions for known file types the default (seriously, *fuck* Microsoft). Not only is this a security risk - you could double click on a file that you think is a .jpg file, but is actually a malicious .exe file - it's also a problem when you have to rename files (which you will on occasion with this list).

For example, when you install the crosshair replacer on this list, you'll need to rename a file target.dds. If .dds is a known file type, but you have extensions hidden, when you type in target.dds the new file name will really be target.dds.dds, which is not what the game is expecting, so the mod won't work. So, set Windows Explorer to always show extensions, and keep that setting permanently.

I should also point out here that everything on this list is optional. Hell, playing Morrowind at all is optional. This list represents my personal vision for the game, and reflects my preferences. If you disagree with me about something, then you're free to not use a mod I suggest, or to use a substitute, or to use additional mods that I don't recommend here (though you'll have to determine if there are any conflicts and deal with them yourself).

There aren't very many "added content" type mods on this list. In particular, [Tamriel Rebuilt](https://www.nexusmods.com/morrowind/mods/42145) is not recommended with this list, because TR's new stuff is designed with vanilla game balance in mind, which this list tries its best to move away from.

And one more thing. Read the readmes/descriptions for these mods/utilities before installing them. They often have important instructions and information about the mod, or sometimes additional steps you need to perform. I'll try to point out the important things to give you a heads up, but I can't cover everything exhaustively. Read the readmes!

All that said, let's get started.

# Clean Installation and Other Preliminaries

I strongly recommend beginning this process with a clean install of Morrowind. This will clean out any shit you have left over from a previous install that can cause conflicts and confusion. So uninstall Morrowind and everything related to it, delete any Morrowind-related files left over from your old install, and reinstall. If you have a downloadable version of the game you can still uninstall and reinstall from within the program. (I'm trying to avoid saying "Steam," because fuck Steam.)

## Installation

When you install Morrowind, be sure to install to a location other than Program Files. Installing in the default Program Files location can result in problems with file permissions. I install in C:\Games\Morrowind, but you can install wherever you want.

Also install the Construction Set when prompted to do so. Every Morrowind player should have the Construction Set installed.

When you're asked to install DirectX 8.1, do so unless you're sure you already have it installed. There's no harm in reinstalling it, nor is there any harm in installing 8.1 if you already have a newer version of DirectX installed; it won't overwrite the newer version.

## Backup

Now, before you start the game, or install anything else, the very first thing you should do is copy your vanilla install files (the entire contents of your install directory, e.g. C:\Games\Morrowind) to another location. You want this backup of the vanilla install files in case anything goes wrong. (You can also have multiple working installs of Morrowind on your system if you want.)

## Start Game and Create Test Save

Now you can actually start the game for the first time. Set the game settings to whatever you want. In particular, you should set the view distance to as far as possible (you'll enable distant land in MGE XE later, but the game's view distance setting determines where game engine rendering ends and MGE XE's distant land begins, and you want that distance to be as far as possible). I also recommend disabling real-time shadows, since they look like shit and are very inefficient in terms of performance (you'll get some more performance friendly and better looking shadow effects with MGE XE later).

Proceed in the game through chargen until you exit the Census and Excise office and see the last tutorial popup, and can save your game. This will be your initial test save. After every few mods installed, or after a major change, load up this save and make sure everything works and looks as expected.

# Utilities

We'll now install a number of important utilities that will enhance your game or be very useful for other purposes.

## Morrowind Code Patch ([stable](https://www.nexusmods.com/morrowind/mods/19510), [beta](https://www.nexusmods.com/morrowind/mods/26348))

This is the big one. MCP patches the game's executable (Morrowind.exe) to fix a number of bugs that couldn't be fixed by regular plugins. It also makes (or offers to make) a number of other gameplay and balance changes to the game, most of which are real improvements. It gives you a choice of exactly which patches it will apply and which it won't.

At the time of writing, the beta version is more up to date than the stable version. I recommend installing the beta. Don't let "beta" scare you; the beta version of MCP is quite stable. If you want it, download and install the stable version first, and then install the beta version on top of it (the beta download does not include the .exe file). MCP needs to be installed in your main Morrowind directory.

Also, the main download page has a regular download and a python version download. Don't bother with the python version.

When you run the MCP executable, you'll be presented with a window with a list of patch categories on the left. Clicking on a category will pull up a list of specific patches in the middle of the window, and clicking on a patch will show a description of the patch on the right. All patches that are checked will be applied, and all patches that are unchecked will not be applied. (If you've already patched your .exe, any patches that you uncheck will be removed when you apply patches.) Once you've checked the patches you want, and unchecked any you don't want, click the Apply Chosen Patches button at the bottom to patch your .exe.

I won't list every patch here. Instead, I'll list each category, mention whether patches in that category should generally be applied or not applied, and then list any patches in that category that are exceptions or that I have specific notes about. I suggest reading MCP's description of each patch to get an idea of what it does, but many patches I don't need to say anything specific about and you can just enable.

So, here we go.

### Beta

This patch category exists only in the beta version, obviously. If you're not using the beta, you won't see the patches in this category. At this time, all of the patches in this category should be turned **on**, except for the "Doppler audio fix" patch, which, as you can tell from the description, should be **off**.

### Game Mechanics

This category contains patches that are not so much bugfixes as gameplay changes and balance improvements. For the most part, patches in this category should generally be turned **on**, unless I say otherwise, although some of them are a matter of personal preference and can be turned off if you don't want them. Specific patches of note are:

- Pickpocket Overhaul

My recommendation: **on**

This is a great gameplay improvement. In vanilla Morrowind, pickpocketing is absurdly difficult, and the difficulty is based on the value of the item. This patch makes pickpocketing difficulty vary based on weight instead of value, and makes pickpocketing generally easier, especially for experienced thieves. Highly recommended.

- Slowfall Overhaul

My recommendation: **on**

The Slowfall mechanic in vanilla Morrowind is broken. Even a 1-point magnitude Slowfall spell will totally prevent all falling damage. This patch changes that, and makes damage reduction depend on spell magnitude. The version of BTB's Game Improvements, our major game balance overhaul, on this list assumes the use of this patch; definitely enable it.

- Healthy Appetite

My recommendation: **on**

In the vanilla game, eating ingredients raw can actually fail to have any effect, with the odds of success depending on your Alchemy skill. At low skill, eating ingredients will usually have no effect. This is a totally unrealistic mechanic.

This patch makes it so that eating ingredients always succeeds (the first effect of the ingredient will always be applied). This is much more realistic, as even if you're very unskilled at mixing potions, eating a poisonous ingredient should still poison you.

This patch does potentially have game balance implications, because, in vanilla Morrowind, successfully eating ingredients is one of the things that advances your Alchemy skill (along with successfully mixing potions). Therefore, this patch makes it easier to train your Alchemy skill.

However, BTBGI makes a number of changes to skill progression rates, and in particular eliminates the Alchemy skill gain from eating ingredients, thus removing this issue. In addition, another mod on this list, Controlled Consumption, prevents you from scarfing down ingredients one after another.

I highly recommend this patch, as a realism improvement and as an antifrustration feature when eating ingredients.

- Two-Handed Weapon Removes Shield

My recommendation: **on**

In vanilla Morrowind, you could have a two-handed weapon and a shield equipped at the same time. You couldn't actually block with the shield in this case, but the armor rating of the shield still contributed to your overall armor rating, and you could still benefit from any constant effect enchantment on the shield.

This patch fixes this oversight. Now, if you want to benefit from a shield's armor rating or enchantment, you can't have a two-handed weapon equipped.

- Alchemy Potion Weight Rebalance

My recommendation: **on**

This is a pretty significant balance patch that should definitely be **on**. It fixes a bug that allowed you to create extremely lightweight potions. Now the weight of homemade potions will be based on the quality of your alembic and the total weight of the ingredients used to make the potion.

- Enchanted Item Cooldown

My recommendation: **on**

This patch implements a cooldown period of three seconds between uses of enchanted items. Compare this with vanilla, where there is no cooldown period at all and offensive enchanted items can be fired off at enemies as fast as you can click the mouse button, resulting in insane DPS. This is a huge improvement for game balance.

- Enchanted Item Rebalance

My recommendation: **on**

This is the second part of the enchant skill rebalance. This patch makes increasing Enchant skill have less of an effect on the number of uses enchanted items have, in particular significantly reducing the number of uses for enchanted items at high Enchant skill. See the description for specifics. This patch should definitely be enabled.

- Item Recharging Rebalance

My recommendation: **on**

This patch makes it significantly easier to recharge magic items (including cast-on-strike weapons) with soulgems. Definitely an improvement, as enchanted item recharging was too difficult in vanilla.

This patch is especially important when using BTB's Game Improvements, which eliminates the ability of enchanted items to gradually recharge over time, rendering soulgems the only way of recharging magic items.

- Soulgem Value Rebalance

My recommendation: **on**

Makes the value of filled soulgems depend solely on the size of the soul trapped in them, unlike in vanilla where filled soulgem value also depended on the value of the soulgem when empty, and resulted in some ridiculously overvalued items.

- Arrow Enchanting

My recommendation: **on**

Does what it says on the tin: allows you to enchant arrows and other projectiles. MCP's description of this patch says that it's not considered balanced, but the version of BTBGI on this list rebalances equipment enchant capacities, including for projectiles. I think this patch is a useful improvement, and we could always use another incentive to play a marksman character.

- Enchanting Increases Item Value

My recommendation: **on**

In vanilla, enchanting an item has no effect on its value. With this patch, the value of an enchanted item will be increased, depending on the item and the enchantment. This is a balanced feature (especially since BTBGI removes the ability for you to create enchanted items yourself without paying for them), so is recommended.

- On-Use Ring Extra Slot

My recommendation: **personal preference**

Allows you to equip an on-use ring and two constant effect rings at the same time (unlike vanilla, where you can only equip two rings at once no matter what). I don't care for this one personally.

- Allow Gloves With Bracers

My recommendation: **off**

Does exactly what you'd think, and results in clipping, which is why I don't like it.

- Permanent Barter Disposition Changes

My recommendation: **on**

In vanilla Morrowind, a successful barter causes a merchant's disposition toward you to increase by one, while a failed barter (you tried to haggle too much and the merchant rejects your offer) causes their disposition to decrease by one. But these changes in disposition (both increases and decreases) are wiped out as soon as you end the conversation with the merchant.

This patch simply makes the disposition changes for successful and failed barters permanent, even after closing the conversation window.

This is particularly significant for us, as one of the mods on this list completely removes the disposition increase for successful barters, while leaving the decrease for failed barters intact. This means you can permanently lower a merchant's disposition with failed barters, but can't raise it back again (outside of persuasion and magic).

This makes interacting with merchants more realistic and more difficult, which is why I recommend this patch. There is a potential downside, in that it can tend to encourage save-scumming (save before haggling, and reload if the offer is rejected). But one of the optional mods on this list eliminates this downside by preventing us from save-scumming, forcing us to live with the consequences of our actions.

This patch is highly recommended as a realism improvement and a difficulty enhancement.

- Allow Stealing from KOed NPCs

My recommendation: **on**

This patch allows you to pickpocket from knocked out NPCs. In older versions of MCP, this patch introduced a bug where you could speak to hostile NPCs if you sneak up on them. But that bug has been fixed, and so I recommend this patch. (It provides another potential use for the Hand-to-Hand skill if nothing else.)

- Exhaust NPCs with Damage Fatigue

My recommendation: **on**

This makes the Damage Fatigue magic effect more useful, as it can now knock out NPCs, whereas before it could not (Drain Fatigue and Hand-to-Hand attacks always could).

- Strength-Based Hand-to-Hand Damage

My recommendation: **on**

This makes the Hand-to-Hand skill significantly more useful by varying its damage based on the player's Strength attribute. At 100 Strength, Hand-to-Hand attacks will do 2.5 times vanilla damage. With Hand-to-Hand being by far the weakest weapon skill, enhancing it in this way is definitely a good thing.

- Spellmaking Max Magnitude Increase

My recommendation: **off**

Increases the maximum magnitude of spell effects in the spellmaking and enchanting menus from 100 to 500, as some spell effects require magnitudes of over 100 to be very effective. This allows you to make more effective use of certain effects like Feather.

It also allows you to make godlike custom spells, far more powerful than anything the designers intended. This is partially balanced by the fact that such spells would have a particularly high magicka cost and require very high skill to cast, but the potential to be imbalanced outweighs the potential usefulness, in my opinion.

- Spellmaker Area Effect Cost

My recommendation: **on**

This increases the cost of spells with large area effects, which is a good game balance improvement (in vanilla, large area-effect spells are too cheap).

- Spellmaking Matches Editor

My recommendation: **on**

In vanilla Morrowind, spells created in the spellmaking menu are different from pre-made spells (those created in the Construction Set) in a number of ways. This patch changes spellmaking to make such spells the same as those made in the Construction Set. See MCP's description for more details.

The most significant change here is that this patch makes casting short-duration (especially one-second) spells created in the spellmaking menu considerably easier. Normally this might be unbalancing, but BTB's Game Improvements makes many of the exploits involving short-duration spells no longer possible (for example, you can no longer create a custom one- or two-second Charm spell), so I can recommend this patch.

- Hidden Traps

My recommendation: **on**

In vanilla Morrowind, you can always see when a container or door is trapped, no matter how low your security skill. This is completely unrealistic and, as the MCP description says, trivializes the idea of traps.

With this patch, you can now never see when a container or door is trapped, no matter how high your security skill. This is also totally unrealistic, and only severely increases the frustration associated with traps, turning it into a guessing game.

Normally I would recommend against this patch, but there is now a mod called Locks and Traps Detection that makes detecting traps depend on your security skill (among other things). This elegantly solves the dilemma regarding traps, making this mechanic much more realistic and well-balanced. Also, another mod on this list implements the ability to detect traps with magic.

Since Locks and Traps Detection requires that this patch be on, I definitely recommend this patch.

- Hidden Locks

My recommendation: **on**

In vanilla, you can always see when a container or door is locked, and the exact lock level of the lock, regardless of your security skill. With this patch, you can never see an object's lock status or level, regardless of your security skill - all you have to go on is the sound made when you try and fail to open the container or door.

Since you don't know what the lock level is, you'll have no idea how hard it will be to unlock until you try. It also makes trying to unlock things using the Open spell effect a guessing game.

The Locks and Traps Detection mod also fixes this mechanic, making whether or not you can detect a lock, and your certainty regarding its lock level, depend on your security skill. That mod requires that this patch be on, so enable this patch.

- Detect Life Spell Variant

My recommendation: **on**

Causes the Detect Animal spell effect to detect NPCs, whereas in vanilla it could only detect creatures. This is a good improvement, and BTB's Game Improvements assumes you're using this patch (BTB renames the Detect Creature spell).

- Attribute Uncap

My recommendation: **on / doesn't matter**

This patch removes the cap of 100 for attributes.

With the vanilla leveling system, this is a pretty radical change, allowing you to much more heavily customize a character than before. You could, for example, create a character very highly focused on strength, increasing strength well past 100, but this would be to the detriment of other attributes, as before you would have to start boosting those other attributes once your strength reaches 100.

This allows quite a bit more flexibility in character builds, allowing for characters with much more pronounced strengths and weaknesses at high levels, if that's the way you choose to develop your character.

This patch also eliminates the dilemma associated with attribute-raising birthsigns, and other attribute-boosting effects such as vampirism. Without this patch, the attribute-boosting birthsigns are wasted at high levels (at least without a special script that removes them when you level), and the cap creates a strong incentive to wait until you're already very powerful before becoming a vampire, to avoid the attribute gains ultimately being wasted. With this patch, that dilemma goes away, as in both cases the gains are no longer wasted, since there's no longer a cap.

I would generally recommend this patch. However, one of the mods on this list, Class-Conscious Character Progression, radically transforms the game's leveling system. If you're using CCCP, it doesn't matter whether this patch is enabled or not, since attributes will be able to exceed 100 regardless.

- Skill Uncap

My recommendation: **on**

This patch does the same thing as Attribute Uncap, but for skills.

Increasing skills significantly beyond 100 is considerably more difficult than it is for attributes. For one thing, even master trainers can only train your skills up to 100, so any increases beyond that must come the old-fashioned way, through practice (or from skill books or scripted quest rewards). And skill progression rates are very slow at such high skill levels.

This also, like the Attribute Uncap patch, eliminates the dilemma surrounding skill-boosting effects like vampirism and certain quest rewards. There's no longer a need to min-max by waiting until your skills are already at 100 before claiming a skill-increasing quest reward, reading skill books, or becoming a vampire.

### Visuals

This category contains graphics-related patches. The ones that I don't discuss below are related to third-person camera view, which I never use, so I can't say much about them.

- Rain/Snow Collision

My recommendation: **on**

This makes rain and snow no longer pass through objects, so you can, for example, stand under an overhang and not get rained on. This is definitely more realistic. It normally doesn't make much of a practical difference, but one of the mods on this list uses this patch to very good effect, so definitely enable it (otherwise you'd get rained on in the Vivec plazas).

Be sure to make the .ini edits listed in the MCP description.

- Bump/Reflect Map Local Lighting

My recommendation: **on**

This makes the light coming from reflective objects (those with bump or reflection maps) depend on the local light level, as opposed to being the same brightness all the time. This is an improvement, especially if you're using mods that include bump and reflect mapped objects.

This also applies to glowing enchanted items, but one of the mods on this list removes this glow effect.

### Mod Specific

This category includes patches that improve the ability of mods to mod the game. While most of these are optional, I have most of them turned **on**, except for where I say otherwise below. Patches of note are:

- Scripted Music Uninterruptible

My recommendation: **on**

Makes it so that music being played by a mod will not be interrupted by Morrowind's default "explore" and "battle" music.

One of the mods on this list is nothing but scripted music, so definitely enable this.

- Separate Axe Inventory Sounds

My recommendation: **on**

MCP's description says most of what needs to be said about this. Upon enabling this patch, no sound will play when picking up or putting down an axe, until you install a mod that adds those sounds. Patch for Purists, our major bugfix mod which we'll install in a bit, includes this fix. So, go ahead and enable this patch.

- Weapon Resistance Change

My recommendation: **on**

This patch allows mods to cause enchanted weapons to no longer ignore normal weapon resistance (whereas before, any enchanted weapon automatically ignored resistance, regardless of the state of the "ignores resist" flag for that weapon). One of the mods on this list removes this flag from low-quality enchanted weapons, assuming the use of this patch.

- Allow Scroll Enchant Price Modifier

My recommendation: **on**

This patch allows the cost of enchanting scrolls, which can only be used once, to be different from the cost of enchanting items that can be used over and over again. This is obviously a great change, but only when used in conjunction with a mod that edits one of the game's GMSTs to actually enable the price difference.

BTB's Game Improvements edits this GMST under the assumption that players will enable this patch. So enable it.

- Hi-Def Cutscene Support

My recommendation: **on**

All of vanilla Morrowind's included videos are low resolution, and vanilla Morrowind won't play videos with a resolution above 640x480. This patch significantly increases the maximum video resolution.

There are a couple mods on this list that replace vanilla videos with higher resolution versions, and these mods require this patch to be enabled.

- 'Talked to PC' Extension

My recommendation: **on**

There is a flag called "Talked to PC" that represents whether or not you've talked with an NPC before. 1 for yes, 0 for no. Dialogue responses can filter for this flag, which means that NPCs can have different dialogue the first time you talk to them than they do in subsequent conversations. A few responses for the "little advice" topic do this.

However, in the vanilla game, the "Talked to PC" flag is set to 1 immediately after the initial greeting, so no dialogue responses other than greetings will ever see this flag as being 0. This means you'll never see those dialogue responses that filter for the flag being 0.

This patch delays setting the "Talked to PC" flag to 1 until after you've said goodbye to them for the first time, which means that dialogue during that first conversation can include the filtered responses.

As MCP's description says, this causes a problem with mods that use multiple greetings to run scripts, such as Economy Adjuster Merchant Skills. None of the mods on this list do this, however, so this patch can be enabled. (While Economy Adjuster Merchant Skills is a great mod, we'll be using a different one to balance trading.)

- NPC AI Casts Zero Cost Powers

My recommendation: **off**

This allows NPCs to use their racial powers against you in battle. This results in a very large increase in difficulty when fighting against NPCs, even with the vanilla game's racial powers. BTB's Game Improvements significantly boosts the racial powers, making them even more dangerous, and making the game *too* difficult with this patch enabled. So leave it OFF.

- Container Respawn Timescale

My recommendation: **off**

In vanilla, respawning containers (such as plants) respawn every three months, and this time period can be edited by changing a GMST that determines the number of months until respawn (default 3). This patch makes the GMST represent the number of *days* until respawn, instead of the number of months, but it doesn't change the GMST itself, which means that plants and other respawning containers would respawn every three days unless you're using a mod that edits this GMST with this patch in mind. Since we're not, leave this patch **off**.

### Interface Changes

This category includes patches that change the user interface in some way, many of which are convenience improvements. Patches in this category should generally be **on**, unless I say otherwise, though some are just matters of personal preference and can be disabled if you prefer. Notable patches are:

- Map Expansion (for Tamriel Rebuilt)

My recommendation: **off**

This expands the in-game world map, so it will show the new lands added by Tamriel Rebuilt. If you're not using TR (and we're not with this list), this patch should remain OFF.

- UI Display Quality Fix

My recommendation: **on**

Makes the UI more clear and less blurry. Obviously a great improvement. This works very well with the Better Dialogue Font mod, further down in this list.

- Convenient Defaults

My recommendation: **off (but it's a matter of preference)**

In vanilla, every time you load the game, your movement speed will be set to walk rather than run (requiring you to hit the toggle run key to start running), and the map will display the local map. This patch reverses this; movement speed will be set to run and the map will display the world map when you load the game.

If you find these new defaults more convenient, then enable this patch. If you want running to be the default movement speed, but want the local map instead of the world map to display by default, as the MCP description says you can leave this patch **off** and make a small edit to your Morrowind.ini instead. That's what I do.

- Spell Select by Name

My recommendation: **doesn't matter**

This is a nifty UI improvement that allows selecting spells in the spell list when your menu is open by pressing the first letter of the spell name. However this patch is obsoleted by one of the mods on this list, UI Expansion, which, among other things, allows filtering and searching for spells. It doesn't matter whether this patch is enabled or not; UI Expansion will work either way.

- See All Standard Potion Effects

My recommendation: **personal preference**

This one is arguably a gameplay change instead of a UI change. It enables you to see all effects of most standard (pre-made) potions, whereas in vanilla you can only see a certain number of effects depending on your Alchemy skill, like with ingredients. This does not affect player-mixed potions.

The effects of most stock potions that you can buy from merchants are pretty obvious from the name, though the magnitude and duration might not be. Perhaps the most important effect of this patch is allowing you to see all the effects of alcoholic beverages.

This is really a convenience patch, but there is an argument to be made that characters with low Alchemy skill should not be able to see these effects. Whether to enable this patch is a matter of preference. I personally enable it.

- Better Typography

My recommendation: **on**

This significantly improves the text display of books, scrolls and the journal. As MCP's description says: "Book pages have more words per line, and lines per page. The quest and topic list is wider, and wraps less. Scrolls have their text area increased to fill the available space as much as possible."

Many scroll texture replacers are incompatible with this patch, because the area of the texture intended for text is now smaller than the text area. However, the scroll replacer on this list does not have this problem, and Better Typography is too good to pass up regardless.

- Journal Text Colour Configuration

My recommendation: **personal preference**

Allows you to change the color of journal text. Note that if you enable this patch (and make a change to a line in Morrowind.ini that's required for it to have any effect), it will change the text color of scrolls as well as the journal.

- Improved Inventory Filters

My recommendation: **doesn't matter**

Another good patch that's obsoleted by the UI Expansion mod, which implements its own inventory filters. Like with the Spell Select by Name patch, it doesn't matter whether this patch is enabled or not; UI Expansion will work either way.

- Ownership Tooltip

My recommendation: **on**

Adds a line to the item tooltip to indicate when the item is owned (taking an owned item is a crime, and can earn you a bounty if you're caught doing so). This is a pretty significant convenience improvement, and can help you avoid accidentally taking something owned in front of witnesses.

Vanilla Morrowind has a lot of stuff that really should be owned but isn't, which means you can take it with impunity if you know it's unowned. But one of the mods on this list, Ownership Overhaul, addresses this issue by making all that stuff that reasonably should be owned actually owned, which means this patch will mostly just confirm common sense (shit that's lying around in public, in town, is owned by somebody and can't just be taken for free).

However, in the case of items owned by a faction, this patch can provide a bit too much information. The tooltip will display not only that the item is owned, but the name of the faction that owns it, and the rank you need to be in that faction to take it.

Another of the mods on this list, Essential Indicators, changes the color of the crosshair when focusing on an item that's owned, which could duplicate the core functionality of this patch without providing so much information for faction-owned stuff. But the fancy red crosshair from Essential Indicators can be hidden by the item tooltip in some cases, so I still recommend this patch be enabled regardless.

- Display More Accurate Item Weight

My recommendation: **on**

Causes item tooltips to display the item's weight to two decimal places rather than one. This is a good change, as some items have weights that are not a multiple of 0.1.

### International

This category contains patches related to international (non-English) localizations of Morrowind. These patches should all be **off**, unless you're playing a non-English localization, in which case read MCP's descriptions to see if these patches apply to you (but then much of this list would be inapplicable to you anyway).

### Bug Fixes

This category contains the main bugfix patches of MCP. All of these patches should be turned **on** (except for one, which is pure preference). Most of these patches I won't specifically list here, as MCP's description is self-explanatory, and they should all be **on** anyway. But particularly notable patches include:

- Resolution Options Fix

My recommendation: **on**

Allows you to set resolutions for aspect ratios other than 4:3, including 1920x1080 (16:9). MGE XE (which we'll install in a bit) also allows you to set such resolutions, but this patch allows you to set them natively within Morrowind.

- Mercantile Fix

My recommendation: **on**

This patch fixes the so-called "mercantile bug."

The "mercantile bug" refers to an intentional stopgap that the developers programmed into the game in an attempt to prevent the player from exploiting merchants too badly. In vanilla Morrowind (without this patch), the sell price of an item is capped at its buy price. As your mercantile skill (and merchant disposition) increases, the buy price of items (what merchants will charge you for them) decreases, while the sell price (what merchants will pay for them) increases. At high enough mercantile and/or merchant disposition, the sell price will reach the buy price. At this point, as the buy price continues to decrease, the sell price decreases too, because it's capped at the buy price.

This patch removes this cap. MCP's description also states that it adjusts differences from base price by half, but after testing it appears to do more than what it says in the description. Having the patch enabled will increase the player mercantile and/or merchant disposition value at which the sell price meets the buy price, which has the effect of making it significantly more difficult to exploit merchants.

The conclusion is obvious: for better realism and to minimize the possibility of exploiting merchants for unlimited money, enable this patch.

One of the mods on this list is Economy Adjuster Adjustments, which contains versions of two of the modules of Economy Adjuster, modified to address a few issues. We won't actually be using the Merchant Skills module of EcoAdj, but see the readme for that mod for more details about this issue, including details of tests conducted to determine the effects of this patch.

Also note that another of the mods on this list, HardTrade, will completely obviate the need for this patch, but leave it **on** anyway.

- Calm Spells Fix

My recommendation: **on**

This patch has a game balance effect, and so is particularly important for this list. In vanilla, Calm spells of any magnitude always forced the target to stop trying to kill you. With this patch, combat will end only if the Calm spell is of a high enough magnitude.

- Reflected Spells Fix

My recommendation: **on**

I think this is more of a gameplay change than a bugfix, but it increases difficulty by adding more risk to using Absorb spells, and so I definitely recommend it.

In vanilla Morrowind, if you cast an Absorb spell (say, Absorb Health) at an enemy that reflects the spell, you would just absorb from yourself and there would be no effect. With this patch, when an Absorb spell is reflected, the enemy absorbs from you instead.

- Dispel Fix

My recommendation: **on**

The magnitude of a Dispel effect is the percentage chance of the effect succeeding. Without this patch, Dispel effects would stack with themselves, meaning 100% chance of effectiveness could be achieved with much less than 100 magnitude. This patch fixes that.

Technically this patch is not necessary with BTB's Game Improvements, which ensures that all Dispel effects will always be at 100 magnitude, but it should be enabled anyway.

- Save File Limit Warning

My recommendation: **personal preference**

This patch isn't really a bugfix, but more of a convenience patch. If you have too many savegames in your saves directory, bad things can happen. This patch reminds you to clean out your saves directory when the number of saves starts getting too high. It's not really necessary as long as you remember to clean your saves directory frequently.

- Game Formula Restoration

My recommendation: **on**

Fixes a number of calculations that the developers flubbed. This is particularly important with a plugin on this list called "More Meaningful Encumbrance", which, among other things, implements fatigue cost for spellcasting, which will not work as intended without this patch.

## .ini Changes

There's a file in your main Morrowind directory called Morrowind.ini. This .ini file contains many game settings, many of which can be tweaked for convenience, better performance or improved appearance.

Following is a list of changes I generally recommend. Settings that can easily be changed in MGE XE (which we'll install in a bit) are omitted from this list. Also, don't bother changing the settings for the individual weather conditions, except for the ones listed below. The weather settings will mostly be controlled by the Weather Adjuster mod we'll install later.

### [General]

- `AllowMultipleEditors=1`

This can be useful if you do a lot of work in the Construction Set.

- `Always Run=1`

Causes the default movement speed to be running, instead of walking, when loading the game. This doesn't prevent you from changing it to walk in-game.

- `SkipProgramFlows=1`

Causes the game to skip displaying certain minor errors that don't need to be reported anyway.

- `ThreadPriority=0`

This defaults to -1. If you have a multicore system, which most people do now, it's better set to 0.

- `Interior Cell Buffer=10`
- `Exterior Cell Buffer=32`

How many cells Morrowind will keep in memory. The above values are the defaults. Keeping more cells in memory is convenient because Morrowind will more quickly load cells you've been to before. However, I don't recommend increasing these numbers above the defaults because keeping more cells in memory can contribute to an eventual crash when Morrowind reaches the 4 GB memory limit.

Instead, I suggest leaving them at the default values for now. One of the mods we'll be installing later allows you to monitor the game's memory usage. If you start approaching the memory limit, you can come back here and reduce these values, which will help. In fact, you can reduce them both to 0, though if you do you might experience problems with delays on loading cells.

### [Weather Rain]

- `Rain Diameter=1200`
- `Max Raindrops=1500`

### [Weather Thunderstorm]

- `Rain Diameter=1200`
- `Max Raindrops=3000`

### [Weather Snow]

- `Snow Diameter=1600`
- `Max Snowflakes=1500`

The above weather changes are needed if you're using the "Rain/Snow Collision" feature of MCP, which you really should be.

## [Wrye Mash](https://www.nexusmods.com/morrowind/mods/45439)

Wrye Mash is a mod manager, an extremely useful utility that lets you manage almost all aspects of your Morrowind install. Among other things, Wrye Mash allows you to:

- Install, uninstall and change the installation order of mods on the Installers tab. Wrye Mash remembers which mods have which files, so if you uninstall mods or change their order, Wrye Mash will make sure the correct files from the correct mods are installed.

- View and change the load order of your plugins on the Mods tab. You can also update or change a plugin's master files here, along with many other functions.

- View your savegames on the Saves tab. You can update your savegame's masters when you add, remove, or change the load order of mods, as well as clean savegames.

- Clean plugins with tes3cmd (a utility we'll be installing shortly), directly within Wrye Mash, as well as use tes3cmd to create a multipatch, which, among other things, merges changes to leveled lists.

- You can launch Morrowind itself from within Wrye Mash, as well as utilities like MGE XE, which we'll be installing in a bit.

I suggest grabbing the x64 manual archive under main files at the top. I also suggest getting the most recent x64 beta under update files. The beta is quite stable, and I haven't experienced any crashes or other problems. Wrye Mash must be installed in your main Morrowind directory. Install the main archive, then the beta update archive on top of it.

In the Mopy directory you'll find a file called Wrye Mash.dat (open it in your web browser). This is the Wrye Mash readme. **Read it!** Read the whole thing, from beginning to end (except maybe the changelog at the end). Read it slowly, thoroughly, and carefully, and make sure you understand it. It might take 45 minutes to an hour or so to read and understand it, but it's time well spent. Once you become familiar with Wrye Mash, you'll never play Morrowind without it again.

There are two terms that will be used throughout this list that I'll go ahead and define here: install order and load order. The install order is the order of your mods as shown in the Installers tab in Wrye Mash. This determines which mod takes precedence when two mods both contain different versions of the same file. This is particularly important with mods like texture replacers, where multiple mods will be replacing the same files.

Load order is the order in which Morrowind will load your plugins. Morrowind always loads all .esm files (master files) first, then all .esp files (plugin files). Within each category, .esms and .esps, the files will be loaded in order of their last modified date, earliest to latest. You can adjust load order in the Mods tab in Wrye Mash. There's also a utility called [mlox](https://github.com/mlox/mlox/releases) that you can use to adjust load order; however, mlox isn't necessary with this list as I've already done the work of determining a good load order.

There are a few other things about Wrye Mash that are important to understand:

When a package has multiple sub-packages (in other words, it's a "complex" installer as described in the readme), the sub-packages will be listed in alphabetical order, and this is the order in which they'll be installed if more than one is selected. This means the alphabetical order of sub-packages is important if multiple sub-packages in the same installer have different versions of the same file.

Some (okay, many) of the mods on this list come in archives that are not packaged properly for Wrye Mash, and will need to be fixed first. (Either Wrye Mash will simply not recognize the directory structure of the archive and will refuse to install it, or it will skip important files because they're not in the expected directories.) Fixing these archives to make them compatible with Wrye Mash can involve things like deleting extraneous directories, getting rid of an unnecessary layer in the directory structure, putting loose textures in a Textures directory, creating separate properly-structured sub-packages for different parts of the mod, and so on.

I generally recommend to only install .esm and .esp files that you'll actually be enabling on the Mods tab (with one exception) - in other words, uncheck any .esm/.esp files you don't intend to use in the Esp/m Filter window. This is to avoid confusion about which plugins should be enabled and which shouldn't be. It also avoids confusion about which plugins to select in applications like MGE XE (for distant land generation), tes3view, and the Construction Set.

Throughout this list I'll generally assume that you understand the above, along with the rest of the information in the Wrye Mash readme. In particular, I will generally not mention when a mod's archive needs to be fixed in some way for Wrye Mash installation, except in egregious or unusual cases (such as when files need to be renamed). I'm assuming you're smart enough to figure out when and how to fix such poorly-packaged archives. Be sure to carefully examine each mod's directory structure for problems before trying to install it.

And one more thing. I recommend Wrye Mash in this list, but there's another mod management tool called [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194) which is excellent and would make a good alternative. If you're already familiar with MO2 and want to keep using it, or just prefer it to Wrye Mash, feel free to use it. However, if you use MO2, you'll need to install Wrye Mash anyway for some of its features, such as cleaning savegames, updating plugin masters, and creating a multipatch. This, along with the increased complexity of MO2, argues pretty strongly for just using Wrye Mash, in my opinion. But it's up to you.

## Original Data Files Archive

Since you've read the Wrye Mash readme (you have read the Wrye Mash readme, right?), you understand that Wrye Mash keeps track of which files it's installed and which mods include which files.

But Wrye Mash only knows about files that it installs. It doesn't know about any files in Data Files that were not installed via Wrye Mash - for example, files that are part of the vanilla Morrowind install, such as the vanilla sound files. This means that if you install a mod that overwrites such vanilla files, and then uninstall that mod, the vanilla version of the files will not be restored, because Wrye Mash doesn't know about them. The files will be outright deleted instead.

So, for example, if you install a mod that includes new versions of the vanilla sound files, then uninstall that mod, those sound files will be gone, which will result in errors in-game because files the game is expecting are missing. (Note that this does not apply to things like mesh and texture replacers, since in those cases the vanilla files are actually in the .bsas, and are not being overwritten.)

Therefore, it's a good idea to actually install the vanilla files in Wrye Mash, to avoid errors in case you uninstall a mod that replaces them (and a few mods on this list do overwrite vanilla files). To do this, we'll be creating a Wrye Mash installer that contains the vanilla files.

Create an archive with the following directories in it: Fonts, Music, Sound, Splash, Textures, and Video (just copy them over from the backup of your vanilla install that you made earlier). Not all of these directories contain files that will be overwritten by mods on this list, but go ahead and include all six of them anyway to be thorough, and so you'll be covered in case you decide to experiment later. (You can ignore the BookArt, Icons, and Meshes directories, because they're empty, as well as the Bethesda .esm and .bsa files.)

Put each of these six directories in a separate sub-package so that you can install or uninstall them independently in Wrye Mash if needed. Also, there should be separate sub-packages for each of the three Music subdirectories (Battle, Explore and Special).

So the directory structure of the archive should be something like this:

```
Original Fonts
    Fonts
        (files)
Original Music - Battle
    Music
        Battle
            (files)
Original Music - Explore
    Music
        Explore
            (files)
Original Music - Special
    Music
        Special
            (files)
Original Sound
    Sound
        (files)
Original Splash
    Splash
        (files)
Original Textures
    Textures
        (files)
Original Video
    Video
        (files)
```

Now go ahead and install this archive (all sub-packages) in Wrye Mash. This will not result in any changes in-game (it's just replacing the vanilla files with identical versions of them from the archive). But Wrye Mash now knows about these files, so if you later install then uninstall a mod that replaces them, the vanilla files will be restored.

Another reason to do this is to allow you to easily *uninstall* some of these vanilla files if needed. For example, if you wanted to uninstall the vanilla splash screens because they clash with new ones you've installed, you'd be able to easily do so in Wrye Mash. Installing this archive in Wrye Mash will allow us to just uninstall the relevant sub-packages (and reinstall them later if we want to) without having to mess with manually moving files back and forth.

If you're exactly following this list, and never uninstall anything, then this procedure is not strictly speaking necessary. But if you decide to play around with mods, or uninstall mods, there's a decent chance you'll eventually uninstall a mod that replaces vanilla files, and it can be quite a pain determining exactly which files are now missing and tracking down those vanilla files so you can copy them over again. And if you don't have a backup of your vanilla files either, you might not be able to fix the problem without a reinstall. I learned this the hard way.

## tes3cmd ([0.37v](https://sourceforge.net/projects/mlox/files/tes3cmd/), [0.40 alpha2](https://github.com/john-moonsugar/tes3cmd/releases/))

This is a command line utility that can perform all sorts of functions on Morrowind plugins. Don't let that intimidate you though if you're not comfortable with the command line; for our purposes tes3cmd can be invoked exclusively from within the Wrye Mash GUI.

There are two versions available. Each has advantages and disadvantages compared to the other; however, the only important metric for the purposes of this list is how they handle leveled list merging.

0.37v seems to handle very complex installs, with many plugins that make conflicting changes to leveled lists, better than 0.40. However, with the mods on this list, I haven't had any problems with 0.40. In addition, 0.40 handles one specific situation much better than 0.37v: when plugins *remove* items from leveled lists, which one mod in particular on this list does.

The verdict: For this list, I recommend using 0.40 alpha2.

tes3cmd must be installed in your Data Files directory to work as intended for our purposes; just dump the tes3cmd.exe file in Morrowind\Data Files.

It might also be necessary to add your Data Files directory (where tes3cmd.exe is located) to your system's path for Wrye Mash to be able to use it (only do this if you get an error when trying to invoke tes3cmd from within Wrye Mash). To do this, in Windows 7, go to Control Panel -> System -> Advanced System Settings -> Advanced tab -> Environment Variables. Find the Path variable at the bottom, click Edit, and add your Data Files directory at the end. If you're using Windows 10, you poor schmuck, you should be able to figure it out on your own, or just DuckDuckGo that shit. (Seriously, use DuckDuckGo, because fuck Google.)

There are lots of things you can do with tes3cmd (type "tes3cmd help" on the command line for more info), but there are only two functions that are of particular interest to us, both invoked from Wrye Mash. (Don't do these yet; we'll get to that later.)

- You can right click on a plugin (or .esm master file for that matter, as long as it's not one of the Bethesda masters) on the Mods tab and select "Clean with tes3cmd". This will use tes3cmd's clean function to clean the plugin of dirty references (references that are identical to the plugin's master files) and some other things that shouldn't be there. It will show you exactly what it changed, if anything, and allow you to save a log. You can also clean multiple plugins at once by selecting them while holding down the shift or control keys.

- From the Mods tab, go to Misc -> tes3cmd -> Create multipatch. This creates a plugin called multipatch.esp, which merges changes to your leveled lists, plus fixes a few additional issues.

We'll use these functions later to make sure our plugins are clean (quite a few mods aren't), and create our multipatch.

## [tes3merge](https://www.nexusmods.com/morrowind/mods/46870)

tes3merge is a utility that can fix many conflicts between mods in your load order. In many cases, two or more plugins in your load order will edit different aspects of the same object. For example, one plugin might change an NPC's name, a second plugin might edit some of that NPC's skills, and a third plugin might add items to the NPC's inventory. Generally, only the changes made by the last of these plugins in your load order will be seen in-game, while the changes made by the first two plugins will be lost.

tes3merge fixes this by scanning the plugins in your load order, and creating a plugin called Merged Objects.esp that incorporates the multiple changes made by different mods to the same object. So for the NPC in the example above, Merged Objects.esp will include the name change, the skills changes and the new inventory items, so you'll see all three changes in-game.

Only where two or more plugins edit the same specific aspects of the same object is a "winner" of the conflict chosen. So, to continue the example, if the third plugin also changed the NPC's name (to something different than what the first plugin changes it to), the third plugin's name change will be the one that wins, because it's later in the load order (but all the other changes to the NPC made by these plugins will still be present in Merged Objects.esp).

Merged Objects can fix many, many conflicts between mods. It should be installed somewhere in your Morrowind directory so it can detect your Morrowind install; create a directory called "tes3merge" in your main Morrowind directory, and put it there.

tes3merge is a command line utility, but it can be run by simply double clicking on the executable. Don't do it now; we'll run tes3merge toward the end of this process.

## tes3view ([Github](https://github.com/TES5Edit/TES5Edit/releases), [Discord](https://cdn.discordapp.com/attachments/518048160526893057/907953273363898368/xEdit_4.1.4_EXTREMELY_EXPERIMENTAL.7z))

tes3view is actually a program called xedit. You might know it as tes4edit, tes5edit, etc. It works for Morrowind too, though some of the functionality present with the other games is absent for Morrowind, because of differences in how Morrowind mods work. Its primary purposes for Morrowind are to see exactly what changes a plugin makes and to diagnose conflicts between mods.

I strongly recommend installing tes3view; it's invaluable as a conflict diagnosis tool. It also helps clue you in to issues with your load order, as some conflicts can be addressed just by changing your load order.

At time of writing, the most recent version has been released on Github as well as Discord. If you see more recent versions on Github (or if you check the xedit Discord for newer releases, as Github tends to be updated with new binaries infrequently), be sure to grab one of the 4.1.x versions; the 4.0.x versions don't work as tes3view.

tes3view does not need to be installed in your Morrowind directory; install it anywhere you want. Now you need to *rename* the executable file xTESEdit.exe to tes3view.exe. This is a required step. (Ignore the file xTESEdit64.exe.)

To use it, select all the plugins in your load order in the "module selection" screen; you'll need to manually select them, or right click and "select all." Once the list loads, you'll be able to view all the records for each plugin (and see any conflicts with that record) by expanding the plugin on the left.

To filter this view so that it only shows records that conflict with other mods, right click somewhere in the plugin list on the left, and select "Apply Filter to show Conflicts". It might take a while to process this command, but when it's done you'll be able to easily inspect your plugins for conflicts.

There's no point in using tes3view right now, but after you've installed most of your mods, you should use it to diagnose conflicts.

## [Enchanted Editor](http://mw.modhistory.com/download-95-1662) ([Instruction Manual](http://mw.modhistory.com/download-95-5259))

Enchanted Editor is an "advanced" Morrowind mod editor. It's very useful for modders, but can also be useful to players who just occasionally want to fix something with a plugin. Many small changes to plugins can be made much more easily in EE than in the Construction Set, and there are a couple points on this list where it's useful to edit a plugin with EE.

You can install EE anywhere; it doesn't need to be installed in your Morrowind directory. The first directory the installer will ask you for is just a location for it to dump temp files; then it will ask you for the actual install location. You can delete the temp files after installation.

There's one more step you can do after installation to improve EE. In the EE install directory, there will be a file called ESTemplate.ini. This file tells EE what some of the values in plugin files (and save files) are for, so that EE can display more meaningful information to you. But the ESTemplate.ini file that comes with the EE download is pretty out of date, and there's a slightly less out of date version of the file that comes with Wrye Mash. Since you've already installed Wrye Mash, you'll find it in your Morrowind\Mopy\Extras directory. Just replace the file in your EE install directory with the newer one from Mopy\Extras.

You can do a lot of advanced stuff with Enchanted Editor, but the simple changes we might need to make, like tweaking values or deleting references, are very easy.

## [Morrowind Graphics Extender XE](https://www.nexusmods.com/morrowind/mods/41102) ([Distant Statics Overrides](https://www.dropbox.com/s/j25igx3p0m5bejs/Abot%20Distant%20Statics%20Override%20-%20Necro%20Edit%202.0.7z?dl=1))

MGE XE is a utility that can drastically improve the appearance of Morrowind. It has antisotropic filtering and anti-aliasing options, advanced lighting options, shaders, and more. One of its biggest graphical improvements is its distant land feature, which can significantly extend the default Morrowind view distance and render distant terrain and objects in the background (depending on how powerful your system is).

MGE XE also includes its own version of Morrowind Script Extender (MWSE), which provides greatly expanded scripting functionality for modders to create cool stuff for Morrowind. Quite a few mods on this list require MWSE.

There are two options on the download page linked above, an executable installer and a manual archive. I recommend downloading the manual archive (why will be clear in a bit). There's also an optional "HUD mods" download that can be safely ignored.

The MGE XE archive includes some files that need to go in your Morrowind\Data Files directory. These files should be installed via Wrye Mash. The reason for this is the same as the reason we installed that archive containing the vanilla Data Files earlier: we want Wrye Mash to "know" about these files. Otherwise, if we later install a mod that includes updated versions of any of these files (and a couple mods on this list do), and then uninstall that mod, the files in question would be deleted outright instead of reverted to MGE XE's version of them, which would result in errors.

So, compress the contents of the MGE XE archive's Data Files directory into an archive and install that archive in Wrye Mash. You can skip the included plugin. Then dump all the rest of the MGE XE files directly into your main Morrowind directory.

After installing MGE XE itself, you'll need to run MWSE-Update.exe (which is now in your main Morrowind directory) to download and install the latest version of MWSE. This is required because quite a few of the mods on this list require an up-to-date version of MWSE to function properly, and can cause unexpected behavior and crashes with old MWSE versions.

I suggest you run MWSE-Update.exe occasionally to update your MWSE version, whenever you install a new MWSE mod or update one to a newer version. MWSE is under active development, so new versions can be released frequently.

MGE XE can be launched directly from Wrye Mash, though you might have to open up the Wrye Mash settings window and tell it where MGE XE is first. Below I'll go through (some of) the various MGE XE settings. You can hover the mouse over most settings to see a brief explanation as well.

Finally, before we get into the nuts and bolts of the MGE XE settings, there's also the distant statics overrides files linked above that I recommend installing. This is my personal edit of Abot's original overrides file, which replaces the woefully inadequate one that ships with MGE XE.

We'll use these files to improve how MGE XE handles distant statics when generating distant land. For now, just dump the necro_distant_statics_override directory into your Morrowind\mge3 directory.

### Graphics tab

- Resolution

With MGE XE you can set whatever resolution you want, including resolutions that might not be available in Morrowind's settings (though to set an arbitrary resolution you must use windowed mode). Click the "select screen resolution" button and pick your resolution. You'll probably want to select whatever your monitor's native resolution is (1920x1080 in my case).

- Windowed mode

This is likely to reduce performance, so generally is not recommended, though you might be able to more easily alt-tab in and out of Morrowind this way.

- Antialiasing

Reduces jagged lines on edges (particularly noticeable on foliage). Set this as high as your graphics card allows (you can determine this on the Config tab; for me it's 8x).

- Anisotropic filtering

Improves texture clarity. Set as high as your graphics card allows (again, you can determine this on the Config tab; for me it's 16x).

- VSync

Syncs the game's rendering of frames to your monitor's refresh rate. This can cause a performance hit, but it solves tearing issues. Turn this on if you experience tearing (which I always do without vsync).

- Shaders

The "Enable shaders" checkbox controls whether or not shaders will be used at all. The "Shader setup" button opens a window where you can enable or disable particular shaders, and determine the order they're applied in.

In this window, click the "Modding" button to show more of the window, where you can fine-tune which specific shaders are present and their order. My recommended shader order for now is:

```
SSAO HQ (or Fast, depending on your performance needs)
Underwater Interior Effects
Underwater Effects
Sunshafts
Bloom Soft (I think Fine puts too much of a light halo/aura around objects)
```

I don't like the "Eye Adaptation (HDR)" shader. It basically simulates the need for your eyes to adapt to varying levels of light, but over a much shorter period of time. When you transition from a dark interior to a bright exterior, you'll be blinded by light for a couple seconds before it drops down to normal levels, and the reverse will happen when going from a bright exterior to a dark interior. I find it annoying, not realistic.

I'm also not a fan of Depth of Field shaders, which make either near or far objects blurry depending on what the focus appears to be.

Some of these shaders will be replaced with superior versions by one of the mods on this list.

- Display FPS

Shows current FPS in the corner of the screen. This can be useful while you're setting up your mods, to monitor performance and make adjustments in MGE XE as needed. I disable this when I'm actually playing.

- FOV

Adjusts the field of view. This is particularly useful for those with widescreen monitors. I suggest just selecting "Auto FOV" so MGE XE can set your FOV automatically based on your aspect ratio (91.3 FOV for 16:9 aspect ratio).

- FPS limiter

This depends on your equipment, but if your monitor has a refresh rate of 60 Hz, there's no point in having FPS above 60 anyway, and limiting it can improve stability and performance. I recommend setting this equal to your monitor's refresh rate (60 in my case).

- Fog mode

Just leave this at range vertex, which is the highest quality option.

- Mipmap LOD bias

This allows you to set a negative LOD (level of detail) bias, which can increase texture detail on distant textures, but comes with a performance hit. I think it's not worth it.

- Screenshots

You can change the format of screenshots, the filename format, and where they're saved.

### In-Game tab

- Disable MGE/MWSE

There's no reason to select these except for troubleshooting purposes.

- Skip opening movie

Skips the Bethesda logo and the menu intro movies, so you don't have to press Escape to skip them every time. A definite improvement.

- Responsive menu caching

Improves performance when the menu is open. Leave this enabled unless you have problems with it.

- Macro editor

Allows you to assign keyboard and mouse button presses to any of a long list of functions, to any combination of keystrokes, or to any console command. I suggest assigning F12 to the "take screenshot" function. Any other keys assigned are a matter of preference.

- Key remapper

You can remap any key to any other key.

- Dynamic lighting coefficients

These are the same values as in Morrowind.ini for quadratic, linear and constant lighting, and editing these values will change Morrowind.ini. When using per pixel lighting (see the Distant Land tab), I recommend values of 2.619, 0.0, and 0.382 respectively. Without PPL, I use basically the same values but change linear from 0.0 to 1.0.

- Allow yes to all load errors

Causes a "yes to all" button to appear on error messages, both in Morrowind and the Construction Set. This should definitely be checked.

- High detail actor shadows

This should definitely *not* be checked. High detail shadows results in extremely poor performance, for very little benefit, since Morrowind's shadows suck so badly anyway (badly enough that I recommend just turning Morrowind's vanilla shadows off in the game's settings).

- Thread loading

This should remain checked.

### Distant Land generation

This is the first step in the process of setting up distant land. You won't be able to set most of the options on the Distant Land tab until you generate distant land first. Click the "distant land generator wizard" button to get started. You'll be led through a series of screens that will ultimately generate your distant land.

Right now, since we haven't installed any actual mods yet, distant land will be generated for vanilla Morrowind, with no mods and no texture replacers. After you're done installing your mods, before you actually start playing the game, you'll definitely need to re-generate distant land again, and after that you'll want to do so every time you add, remove, or change mods that affect the land, textures or distant statics.

- Plugins

First is the plugins screen, where you'll select the plugins you're using (the plugins MGE XE will parse for distant land data). Click "use current load order" on the right to automatically select all plugins in your current load order.

If you have plugins for any grass mods installed, you'll then need to select them manually on the list, as they shouldn't actually be in your Morrowind load order, but they must be selected here so MGE XE will create the grass.

After you click continue, if you've generated distant land before, another window will pop up asking if you want to setup distant land automatically using saved/default settings. I suggest not doing this and instead clicking the "distant land configuration setup" button at the bottom to set the distant land settings manually each time, so you can be sure of what the distant land generator is doing.

- Land Textures

On each screen, MGE XE will complete processing for the previous step, and you won't be able to initiate the current step until this processing is complete (there's a progress bar at the bottom of the window).

On this screen you'll see two dropdown menus for world texture resolution and normalmap resolution. These control the quality of the textures for the land itself. Unless you have a relatively low-end system, I recommend selecting the highest setting the dropdown allows, 8192, for both options. If you need performance you might try lowering normalmap resolution to 4096, but for me it doesn't make much difference.

Click "create land textures" to proceed.

- Land Meshes

Here you'll see a single dropdown controlling the quality of the landscape mesh (i.e. the shape of the landscape). I suggest "ultra high," the highest quality option. Any lower, even "very high," and you'll see artifacts and jagged edges in distant land.

- Statics

This page includes a number of options for distant statics (objects like rocks and buildings).

**Minimum static size**: Objects smaller than this size will never appear in distant land (they'll only appear once they come within Morrowind's standard view distance range). The smaller this is, the more performance demanding near distant statics will be. I personally set this to 50, which is pretty small, but minimizes the problem of objects not being visible in distant land only to suddenly pop in once I get within standard Morrowind view distance. Set this higher if you have performance or memory usage issues, at the cost of more of the aforementioned problem (an NPC's height is about 128).

**% grass density**: How much of the grass in your grass plugins MGE XE will include. I set it to 100%, but lower values can increase performance.

**Mesh detail level**: Level of detail for the shape of distant statics. Distant statics don't use very detailed meshes anyway because they don't need them, so just leave this on "full."

**Distant texture reduction**: Determines how much the quality of textures for distant statics is reduced. By default this is set to 1/2. Changing it to "none" will make distant textures noticeably sharper, even with vanilla textures. It doesn't have that much impact in terms of performance, plus distant statics generation is much faster when MGE XE doesn't have to reduce all those textures.

**Include large interiors**: This includes distant objects in large interior cells.

**Include interiors behaving like exteriors**: This lets you see distant objects in Mournhold, and should be checked (one mod on this list uses this to good effect).

**Include reflective water in interiors**: This one isn't really needed, and you can leave it unchecked for performance reasons, but I like it myself.

**Include activators**: Checking this has a performance impact, but not including activators can result in weird anomalies like doors suddenly appearing when you get close enough. Check this one.

**Include misc objects**: This one should also be checked unless you have a low-end system.

**Static override lists**: Here you can specify text files that contain lists of statics for which MGE XE should override the behavior dictated by the other options on this page. In other words, these lists tell MGE XE to make exceptions for certain objects. MGE XE comes with one such list, which is in the Morrowind\mge3 directory.

However, if you followed my advice you put a directory full of additional override files in the same directory, and these are the files we'll be using. Check the "use lists of statics overriding parameters set above" checkbox and click "edit lists." Remove MGE XE's default file if present, then click "add". Select the file "00_main.ovr" (at the beginning of the game, this is the only file that should be enabled), and save the list.

When you're done, click "create statics" to proceed. If you've already created distant statics before, you'll see a window asking if you're sure you want to proceed. Just click yes.

- Finished

This last screen is just where you'll have to wait for the (maybe significant) length of time it takes for MGE XE to generate distant statics. When it's done, click the "finish" button.

### Distant Land tab

Now that you've generated distant land, you can now access the options on this tab.

- Use Distant Land

If this box is unchecked, you won't see distant land at all.

- Draw Distance

Determines how far away MGE XE will draw distant land. The fog end distance (see below) should be equal to this.

Distant land itself isn't actually very performance demanding; it's distant statics that can kill your FPS. That said, I don't like to see raw landscape with no statics stretching out into the distance.

You might need to test out different values for this and the other distant land settings in-game, until you find ones you're happy with and that result in acceptable performance. Keep in mind that many of the mods we'll be installing later are more demanding in terms of performance than the vanilla assets, so you might have to come back here later and lower these values if performance degrades too much.

I personally set this to 12.0.

- Reflections

These checkboxes determine what you'll see reflected in water (MGE XE comes with its own water shader, which is superior to vanilla Morrowind's water). Unless you have a low-end system, everything should be checked. (Interiors won't work unless you selected "include reflective water in interiors" when you generated distant land.)

- Dynamic ripples

Controls the height of water waves. A value of 40 here works well.

- Caustics

The default value of 50 is just fine.

- Dynamic solar shadows

Causes the sun to cast shadows of trees, buildings and other objects. I think they look pretty good.

- Per-pixel lighting shader

MGE XE's per-pixel lighting looks great, and I strongly recommend it as long as you can afford the performance hit. (Read the tooltip in MGE XE to learn more.) You can also choose whether per-pixel lighting is always on, or on only in interiors. I leave it always on.

On some systems, PPL can result in a brief "stuttering" when you first load a game; you'll see what I mean if you experience it. I think PPL is worth it, but if you experience this and it annoys you, you can always disable PPL.

- Light Settings

Clicking this button opens a window where you can select multipliers for ambient light and sunlight for various weather conditions. I suggest not messing with this. The mod Weather Adjuster, further down on this list, allows you to adjust the lighting/color values for weather conditions.

- Auto set other distances

With this checked, MGE XE will automatically set the values below. I suggest unchecking this so you can manually set the below values.

- Distant statics

Okay, this is probably the most important part of your distant land setup, so pay attention.

First, there's a checkbox that determines whether or not MGE XE will show distant statics at all. (However, in my experience, unchecking this box has no effect.)

Then there are six boxes for the minimum size and the end distance of near, far and very far statics. This allows you to create three categories of distant statics, defined by their size, with different viewing ranges for each.

Out to the standard Morrowind view distance, Morrowind itself will render everything (MGE XE hasn't taken over yet). Between the standard Morrowind view distance and the near end distance (near range), you'll see all distant statics larger than the near minimum size. Between the near and far end distances (far range), distant statics larger than the far minimum size will appear. Between the far and very far end distances (very far range), only distant statics larger than the very far minimum size will be shown. And beyond the very far end distance, no distant statics will be visible at all.

The very far end distance should be the same as the fog end distance, while end distance for far and near statics should obviously be progressively closer. MGE XE will not allow you to set a near statics end distance less than 2.0.

Minimum size for near statics can't be changed here; it's equal to the minimum distant static size you set when you generated distant statics. The minimum size for far and very far statics can be set to whatever you like, but you don't want to set them so small, and to appear so far away, that you can't see them - that just degrades performance for no benefit.

After a substantial amount of playing around in MGE XE, I've discovered settings that work well for me. These settings allow me to see quite some distance, and see distant statics in reasonable detail, while maintaining reasonable performance on my system (30+ FPS for the most part, though it can dip down to 25-30 in busy areas).

You can use these settings as a starting point, but they're heavily dependent on your system and your preferences; you can push near statics out farther and decrease minimum sizes so you'll see even smaller objects in the distance, and pull back the draw/fog and very far statics distances for performance.

With a draw distance of 12.0, my distant statics settings are:

```
Near: 50 / 2.0
Far: 200 / 7.0
Very Far: 1000 / 12.0
```

- Above Water Fog

The start distance is the distance that you'll start seeing light fog, in clear weather, and the end distance is the distance beyond which you'll see nothing, because of the fog.

The fog end distance should be equal to your overall draw distance. I set both to 12.0. This will obviously depend on your system's performance and your personal preferences.

Fog start distance is mostly a matter of personal preference. If you were to have MGE XE auto-set distances, with a fog end distance of 12.0, it would set fog start to 3.3. I set it to 4.0 personally (or 1/3 of the fog end distance). If you prefer a more distant fog start, you can set this higher, maybe something like 9.0, but in that case you'll probably also want to tweak the "weather settings" (see below) to make certain weathers, especially foggy weather, look foggy enough.

- Below Water Fog

Sets the start and end distance for fog underwater. This is the mechanism for reducing visibility underwater, and these distances should be drastically lower than the above water fog distances.

The default values are -0.5 and 0.3, and I recommend leaving them as they are. The negative value for start fog distance means that you're "in the fog" underwater, which is desireable.

- Distant Interiors Fog

Sets the start and end distance for fog in interior cells that show distant objects. I set these to 2.0 and 6.0 respectively.

- Use high quality (exponential) fog

This improves the quality and realism of the fog. I highly recommend keeping this enabled, because the fog looks terrible otherwise.

- High quality atmosphere & distance colouring

I keep this checked, as it improves visuals, but you can uncheck it if you're having performance issues.

- Weather Settings

Allows you to set values for wind speed and fog for the different weather conditions. I do not suggest modifying these settings.

-----

Here's a summary of my important distant land settings:

```
Draw distance: 12.0
Near statics: 50/2.0
Far statics: 200/7.0
Very far statics: 1000/12.0
Above ground fog: 4.0-12.0
Exponential fog: checked
```

This strongly depends on your system and preferences. However, exponential fog should definitely be enabled, and fog end distance and very far statics distance should both be equal to draw distance.

If your draw/fog distance is significantly different from mine, you'll obviously need to tweak statics settings. I recommend a near statics distance of 2.0 and a far distance halfway between the near and very far distances. You'll need to experiment with far and very far statics sizes until you find a combination you're happy with.

### Distant statics overrides

Finally, before we move on, I'll briefly discuss the distant statics override files we installed earlier.

There are a number of items that benefit from special handling for viewing as distant statics. Some items shouldn't be shown at all because they're disabled (like the chargen boat and the stuff on it) or because they're not supposed to actually be visible. Some need to be hidden or have their mesh detail reduced for performance reasons, while some should appear at a greater distance even when they normally wouldn't. These files handle all that.

There are also a number of circumstances in which you would want to change what gets rendered in distant land, depending on where you are in the game, and these files allow for that too. For example, the ghostfence (the actual forcefield, not the pylons) should appear in distant land before the main quest is complete, but it should not appear afterward. The great house strongholds should normally not appear in distant land (they would just disappear when you got close enough). Instead, they should only be rendered once they've actually been constructed in-game.

The way to handle this is to enable one or more additional, supplemental files that override the main one. For example, when the main quest is complete, go to regenerate distant statics again in MGE XE. Click on edit lists, then add the file "01_main_quest_complete.ovr" after the main file. Then regenerate distant statics, and say goodbye to the ghostfence forcefield in distant land.

The readme included in the archive with the distant statics overrides contains more information, and instructions on when to enable each file. The milestones at which you'll need to change which files are enabled and regenerate distant statics are:

- After completing the main quest
- After completing the Bloodmoon main quest
- At each stage of great house stronghold construction
- At each stage of Raven Rock construction
- While Boethiah's quest is in progress
- After completing Boethiah's quest
- After completing the Firemoth quest if you're using that official plugin

# Bugfixes

Now we come to the "regular" mods, which we'll be installing in Wrye Mash. First up is the bugfix mods, which are needed to fix the astounding number of bugs that plague vanilla Morrowind.

## [Patch for Purists](https://www.nexusmods.com/morrowind/mods/45096)

This is the big patch mod. If you could only install one Morrowind mod, you'd want it to be this one.

PFP fixes an enormous number of Morrowind's bugs, ranging from minor annoyances to serious bugs that render quests impossible to complete. A brief summary like this can't do justice to the improvement that PFP will bring to your game. The documentation for the mod lists the fixes that it implements.

The fixes made by PFP are split into three files. The main file is an .esm, Patch for Purists.esm, which contains the lion's share of the patch's fixes. There are also two .esp files, Book Typos and Semi-Purist Fixes. The readme describes these .esps as optional, and they are, but there's no good reason not to include them.

In terms of load order, Patch for Purists.esm should be the first .esm to load after Bethesda's master files. The two PFP .esp files should also be relatively early in your load order; this way they can be overridden by other mods as needed.

By the way, Patch for Purists.esm should not be cleaned with tes3cmd. It contains one technically "dirty" reference that's supposed to be there. Morrowind.esm contains an error in the Steel Cuirass. Tribunal fixes this mistake, but Bloodmoon reverts the fix. PFP reverts it back to the Tribunal version, but since the record is identical to the one in Tribunal.esm, tes3cmd thinks it's dirty and removes it. This is the only "dirty" record in the file anyway, so don't clean it.

## [Texture Fix](http://mw.modhistory.com/download-56-10353)

You wouldn't know from the name of this mod, but the fixes it contains are related to Morrowind's land surface. In vanilla Morrowind, where different landscape textures meet, they're supposed to smoothly blend into each other so you can't detect exactly where one ends and the other begins. But there are many (many) places where this smooth blending does not take place and there is a very abrupt transition from one landscape texture to another. With Morrowind's vanilla textures, this isn't very noticeable, but with high quality texture replacers like ones we'll be installing later, these "landscape seams" start to really stick out.

Texture Fix eliminates these landscape seams by making the landscape textures seamlessly blend into each other, like they were supposed to in the first place. Texture Fix is an .esm file, so its changes can be overridden by mods (as opposed to the other way around, which would break mods). I put it after PFP in my load order, before any other .esms.

There is one minor problem with Texture Fix that you can resolve now. The .esm file in the archive contains a number of references to landscape textures. The presence of two of these references causes a minor problem with distant land generation in MGE XE.

If you generate distant land with Texture Fix in your load order, the distant land generator will present errors related to the textures tx_lavacrust00 and tx_ma_sandstone02. These errors do not actually prevent distant land generation, but they are annoying.

To fix it, open up Texture Fix 2.0.esm in Enchanted Editor, and click on the "Land Textures" category to expand it. Scroll down to the entry "LTEX tx_lavacrust00.tga", right click on it and delete it. Do the same for MA_sandstone02, then save the file. (Deleting these references does not impact the functionality of Texture Fix in any way.)

## [Texture Fix - Bloodmoon](http://mw.modhistory.com/download-56-10388)

This mod does the same thing as Texture Fix above, but for Solstheim, causing landscape textures to seamlessly blend into one another as they were intended. Like Texture Fix, these changes are implemented in an .esm file, and I put it right after Texture Fix 2.0.esm in my load order.

## [Cinia](https://www.nexusmods.com/morrowind/mods/47153)

The Morrowind developers failed to place the medium armor master trainer, Cinia Urtius, in the game, and Patch for Purists does not fix this oversight. Thus the need for this mod, which places Cinia at the docks at Tel Fyr. She offers training (including master training in medium armor) and one-way travel to Sadrith Mora.

## [Dubdilla Location Fix](https://www.nexusmods.com/morrowind/mods/46720)

This mod fixes an inconsistency related to the dungeon Dubdilla, the destination for the quest A Cure for Vampirism. Molag Bal says in spoken dialogue that it's beneath Mount Assarnibibi, but the dungeon's actual location is in the Grazelands.

Since the spoken dialogue can't be easily changed, this mod simply changes the location of the dungeon (and the text of the journal entry pointing you there).

There's one error in the plugin that can be fixed in the Construction Set. Edit the script VampireMolag and look toward the bottom of the script. See all those "endif"s? There's one too many. Delete one of them, save the script and the plugin, then clean in Wrye Mash.

## Bloated Morrowind Magnified ([Nexus](https://www.nexusmods.com/morrowind/mods/47504), [Moddinghall](https://mw.moddinghall.com/file/26-bloated-morrowind-magnified))

Bethesda created a plant called bloatspore, but for some reason neglected to actually place any in the game. This mod addresses that oversight by placing bloatspore plants at various locations throughout the Bitter Coast, and in some caverns and grottos.

I consider this a bugfix mod, as there's no good reason why this plant that Bethesda went to all the trouble to create was not placed in the game. It also provides an additional source of ingredients for alchemy buffs.

## Under Construction ([Nexus](https://www.nexusmods.com/morrowind/mods/50285), [Moddinghall](https://mw.moddinghall.com/file/159-under-construction))

The Great House strongholds have three main stages of construction, but there are actually construction-in-progress phases that, for stages 2 and 3, are unimplemented in vanilla Morrowind. This mod implements them.

Now you'll see scaffolding and other construction materials at the Hlaalu and Redoran strongholds while the second and third stages are under construction; at the Telvanni stronghold you'll see intermediate stages of the tower's development.

This content had all been placed by Bethesda - it had just never been enabled in the scripts. This might technically be more of a "cut content" type mod, but I'm considering it a bugfix here, as the omission in the scripts seems like an oversight to me.

The mod also fixes a couple errors in the Raven Rock scripts, in particular a flub that caused certain trees and rocks at the SE factor's estate location to be disabled when they shouldn't be.

# Official Plugins and Related Mods

I recommend adding a couple (but not all) of Bethesda's official plugins to your load order - the ones that I feel add something worthwhile to the game. We won't be downloading the original versions of these plugins, because they have some bugs and other problems. This section consists of alternate versions of a few official plugins, plus a couple related mods and fixes.

## Unofficial Morrowind Official Plugins Patched ([Nexus](https://www.nexusmods.com/morrowind/mods/43931), [Moddinghall](https://mw.moddinghall.com/file/78-unofficial-morrowind-official-plugins-patched))

This mod, the name of which can thankfully be shortened to UMOPP, is actually a compilation of all of Bethesda's official plugins, with their bugs and other issues fixed. In particular, those official plugins that include journal entries now have official journal quests (the original versions of the official plugins were released before the journal quest system was introduced in the expansions).

The download page for UMOPP includes a couple of optional files, including a download with "merged and compatibility" versions, but there's no need to bother with these. (The compatibility versions would generally be recommended, but the plugins I suggest using don't have compatibility versions.) Just download the main file.

I recommend enabling the following plugins from this package:

- Master Index: Vanilla Morrowind contains ten "propylon indices" that can be used for fast travel between the Dunmer strongholds scattered over Vvardenfell, but almost no clues to their locations. This plugin adds a quest that clues you in, plus a "master index," that can be used for more convenient fast travel between the strongholds, as a quest reward for finding them all.

- Helm of Tohan (EBQ_Artifact): Adds a small quest, and a unique adamantium helm as a reward.

We'll be installing an alternative version of Area Effect Arrows in a bit, and one of the mods on this list basically incorporates an alternative version of Adamantium Armor. The other official plugins aren't worth our time.

I put the official plugins, and other related plugins, early in the load order.

## [Better Propylon Teleport Script](https://www.nexusmods.com/morrowind/mods/46364)

The page linked to above is actually a collection of small mods by PikachunoTM, the author (or rather editor) of UMOPP. Most, but not all, of these mods are related to the official plugins in some way. The only file we need on this page is Better Propylon Teleport Script.

This mod improves the teleportation system between strongholds to ask you for confirmation before teleporting, and to allow you to choose a destination if you have the Master Index. There are two plugins in the archive; use only the Master Index version, not both.

## [Particle Arrow Replacer](https://www.nexusmods.com/morrowind/mods/47749)

This is not an official plugin, but it's required by the derivative of Area Effect Arrows that we'll install in a bit, so I'm including it here.

Particle Arrow Replacer replaces the lame vanilla particle effects on enchanted arrows with much cooler-looking effects, depending on what spell they're enchanted with.

You don't actually need either of the plugins in this archive, as the next mod we'll be installing includes all of PAR's edits. All you need from this archive are the meshes.

## Area Effect Projectiles Integrated ([Nexus](https://www.nexusmods.com/morrowind/mods/47745), [Moddinghall](https://mw.moddinghall.com/file/125-area-effect-arrows-integrated))

The official plugin Area Effect Arrows adds a new merchant in Vivec who, as you can probably infer, sells arrows (and other projectiles like bolts and throwing weapons) with cool area effect enchantments.

BTB created a modified version called Area Effect Projectiles, which adjusts the weapons and enchantments with an eye toward game balance (in line with his game balance mod BTB's Game Improvements), and makes a lot of additional fixes. He also created a "PAR Edit" version, which additionally includes the new particle effects from Particle Arrow Replacer.

The "integrated" version linked above does not add the new merchant in Vivec at all. Rather, it distributes the new projectiles between several merchants, and adds them to a few appropriate marksman-related leveled lists. It includes "integrated" versions of the original AEA and BTB's AEP, and a "PAR Edit" version of the latter.

Use only the AEP PAR Edit version, not the other versions, and not either of the plugins in the PAR archive. (But do make sure you've installed the meshes from PAR above, or else the PAR Edit version won't work.)

# Convenience Mods

This section contains a number of mostly small mods that make various aspects of Morrowind more convenient or less frustrating. I would recommend these mods for any playthrough.

## [Expeditious Exit](https://www.nexusmods.com/morrowind/mods/45634)

Expeditious Exit is an MWSE mod that force-quits Morrowind when you exit the game, rather than letting Morrowind shut down in its normal way. I have problems with the game hanging upon exit, which this mod eliminates. Quitting the game is noticeably faster with this mod installed, and you can configure it in the Mod Config Menu to skip the confirmation dialogue to save even more time. (I don't recommend enabling the "use taskkill" option unless you have trouble with the mod's default method of shutting down the game.)

MWSE mods like this one can be fussy if you're using an outdated version of MWSE. Make sure you're using an up-to-date version of MWSE, and update it whenever you install new MWSE mods or newer versions of existing mods.

## Memory Monitor ([Nexus](https://www.nexusmods.com/morrowind/mods/45696), [Moddinghall](https://mw.moddinghall.com/file/95-memory-monitor))

Vanilla Morrowind can only access up to 2 GB of memory (it's an old game, after all). Morrowind Code Patch thankfully increases that limit up to 4 GB, but it's not hard to reach that limit with a heavily modded game. Once you reach the 4 GB memory limit, Morrowind will crash.

Memory Monitor is a utility mod that keeps track of how much memory the game is using. It adds a small bar in the HUD above the minimap that shows you how much memory Morrowind is using. The bar is very unobtrusive, and it will only show up once memory usage reaches a configurable threshold (50% of the 4 GB limit by default).

Once you reach a configurable critical threshold (90% of the limit by default), a messagebox will pop up allowing you to save your game and quit Morrowind to avoid a crash. You can also save without quitting or just continue the game if you prefer.

The mod can be configured by opening the file MWSE\config\Memory Monitor.json in a text editor. I suggest leaving the critical threshold at the default 0.9, but the visible threshold (below which the memory bar will not be displayed) can be adjusted to your preference.

If, after you've finished installing all your mods and setting up Morrowind the way you want it, you find that your memory usage never approaches the limit, you might choose to uninstall this mod, but it's a good idea to install it in the meantime.

## Quick Char ([Nexus](https://www.nexusmods.com/morrowind/mods/47706), [Moddinghall](https://mw.moddinghall.com/file/122-quick-char-necro-edit))

Quick Char significantly shortens the character creation process by giving you the option as soon as you appear on the boat with Jiub to skip the chargen tutorial. If you say yes, all of the character generation screens will appear in order, and you'll be dumped in front of Sellus Gravius with your papers in your inventory.

You're not forced to do this; you can proceed through the chargen tutorial like normal. But you can only listen to the esteemed Mr. Ergalla say "Ah yes, we've been expecting you..." so many times without going crazy.

The version of this mod linked above includes two versions of the plugin. One includes only the basic functionality of the mod, while the other also sets the timescale global variable to 6, from the default 30. I recommend just using the regular (Necro Edit) version of the plugin, not the Timescale6 Edit version, because another mod on this list will manage the timescale and is highly configurable.

## [Continue](https://www.nexusmods.com/morrowind/mods/45952)

This MWSE mod adds a "Continue" button to the game's main menu, which will automatically load your most recent save. Granted, this only saves you a couple seconds each time, but I think it's very convenient.

It can also optionally be configured to hide the "Credits" button in the main menu, and the "New" button once you're in-game, to de-clutter the menu.

## [New Game Confirmation](https://www.nexusmods.com/morrowind/mods/47693)

Have you ever accidentally clicked the "New" button in the main menu, and found yourself staring Jiub in the face, when all you wanted to do was load your savegame? This mod will prevent that by adding a confirmation dialog box when you click "New" from the main menu. Just another mod that'll save you a few seconds here and there.

## Sophisticated Save System ([Nexus](https://www.nexusmods.com/morrowind/mods/45608), [Github](https://github.com/NullCascade/morrowind-mods))

This mod changes the save system in a number of ways to make it more convenient. The most important enhancement for our purposes is an increase in the number of available quicksaves/autosaves. Vanilla Morrowind allows only one quicksave and one autosave; SSS implements a system of rotating quicksave/autosave slots, with ten slots available by default.

This is particularly important if you choose to use Restrictive Saving, one of the optional mods further down on this list, which prevents us from saving unless we're resting in a bed. Especially with Restrictive Saving, it's important to have more than one quick/autosave slot (in case of savegame corruption, or to be able to go back to a previous save).

Additional changes implemented by SSS include the ability to autosave under different circumstances (entering or leaving combat, cell change, automatically after a certain amount of time has passed). It also causes quickload to load your most recent save of whatever type, not just a quicksave.

I suggest grabbing the mod from Github, which might be more up to date than the version on the Nexus. In Github, just click the "code" button, then click "download zip." You'll then need to create an archive with just SSS to install in Wrye Mash. (We'll also be installing UI Expansion and Consistent Enchanting later, so go ahead and create installers for those mods as well.)

There are a few changes that I suggest making in the Mod Config Menu. These changes are necessary if you plan to use Restrictive Saving, but I recommend them even if you don't. First, disable all four "create autosave" options. We don't want the game autosaving all the time. Not only is that immersion-breaking, but it would conflict with Restrictive Saving, which would cause those autosaves to fail.

Also, change the "minimum time between autosaves" value from 1 to 0. We want to disable this feature because a failed autosave will still count and will reset the timer, and there will be a failed autosave with Restrictive Saving every time you wait.

## [Right Click Menu Exit](https://www.nexusmods.com/morrowind/mods/48458)

This mod makes one aspect of the game much more convenient: you can now close almost any menu in the game by right clicking (or whatever button you've set in the game options for menu mode). This includes dialogue, barter and other service windows, options menu, save/load, container menu, alchemy menu, and many more.

This is much faster and more convenient than having to click the close/cancel button every time, and while MCP already gives shortcuts to close a few of these menus, this mod is a definite convenience improvement.

## UI Expansion ([Nexus](https://www.nexusmods.com/morrowind/mods/46071), [Github](https://github.com/NullCascade/morrowind-mods))

UI Expansion is an MWSE mod that improves Morrowind's UI in numerous ways. This includes, among many other things:

- Improved inventory filtering, and filtering in the magic menu.
- Search bars in the inventory, magic and additional menus.
- Filtering in the barter menu by whether the merchant will buy the item.
- Dialogue topics highlighted if unique, and gray if you've heard it before.
- Savegame list filtering by character.

I consider this a major convenience mod, and I wouldn't want to play Morrowind without it anymore. I strongly suggest grabbing the Github version, which tends to be more up-to-date than the version on the Nexus (which is rarely updated).

### MCM Settings

Most of the mod's features are configurable in the Mod Config Menu. You can generally enable or disable any of these features at your convenience, though I have a few specific recommendations.

1. I suggest disabling the "map mode switch on cell change" feature. This feature causes the in-game map to automatically switch from the local map to the world map on every exterior cell change. This might be okay if you never use the local map outside, but for me it's very annoying.

2. If you plan to use Map and Compass, another mod on this list, you should disable the "map" component entirely. The map component does two things. The first is the feature that we just disabled that automatically switches the map mode. The second is a new hotkey (the right Alt key by default) for switching between the world and local maps. This is generally pretty useful, but causes a problem with Map and Compass (which totally changes how the map works). So, if you plan to install Map and Compass, just disable the map component of UI Expansion to avoid any problems.

3. I suggest enabling the "display value/weight ratio" option. This is very helpful when you're trying to decide what loot to haul out of a dungeon and what to leave behind.

4. Leave the "transfer stacks between inventories without pressing alt" feature **off**. I've experienced problems and the occasional crash with this feature enabled.

### Tooltip Tweaks

I also make two minor tweaks to the code in tooltip.lua. These tweaks are not at all necessary, so skip them if you don't feel like bothering with them. First, find this line:

```
if not e.object.id:find("Gold_") and not e.object.isKey then
```

and change it to:

```
if ( not e.object.id:find("Gold_") ) and ( ( not e.object.isKey ) or e.object.id:lower() == "bm_bearheart_unique" or e.object.id:lower() == "bm_seeds_unique" ) then
```

Those two objects are technically keys, which means UI Expansion's icon bar would not display for them. But they're not really keys, and they should have the icon bar.

Second, find this line:

```
if objectValue and e.object.weight then
```

and change it to:

```
if objectValue and e.object.weight and ( objectValue > 0 or e.object.weight > 0 ) then
```

This causes the icon bar to not display when the weight and value of an object are both 0.

## [Smart Journal](https://www.nexusmods.com/morrowind/mods/47492)

This mod implements a number of convenience improvements to the journal. In particular the journal no longer displays the date header for every entry, only when the date changes or at the top of each page. It also no longer displays links that are not whole words, but only inside of longer words. These behaviors and more are configurable in the MCM.

By default the mod also changes your quest list to add a prefix to each quest name (which by default is the ID number of the mod the quest is from). It also displays a "hint" whenever you mouse over each quest name, which can show the quest ID and the name of the mod it's from. Plus it changes the messagebox that appears when your journal is updated to include the name of the associated quest.

I find the above behavior immersion-breaking; it can also cause a short delay when loading the quest list. Fortunately this behavior can be disabled in the MCM. The top three options in the MCM - clear topics with no entries, collapse dates, skip links inside words - should be on, and everything else should be disabled, including the quest prefix dropdown. (It might be useful to enable some of the other features when troubleshooting quests.)

## [Hot Quests](https://www.nexusmods.com/morrowind/mods/48976)

Another journal convenience mod. This one implements hotkeys to bring up the quest list (and the topics list), so you no longer have to bring up the journal then click one or two buttons to see your list of quests.

The hotkeys default to U (quest list) and I (topic list), but they can be modified if desired in the MCM.

## [Book Worm](https://www.nexusmods.com/morrowind/mods/46851)

This small but great MWSE mod adds an indicator to the names of all books that you've already read. For example, once you've read Lives of the Saints, the name of all copies of that book in the future will display as "Lives of the Saints (Read)" to let you know you've already read it. I consider this a must-have convenience mod.

## [Shrine Tooltips](https://www.nexusmods.com/morrowind/mods/48275)

Another small MWSE convenience mod, this one for Tribunal shrines. When you activate a shrine, you'll see a list of blessings to choose from. Some of these, like "cure disease" or "restore attributes," are self-explanatory, but for many blessings it's not at all obvious what the effects are until you choose it. This mod adds a tooltip that will display these blessings' effects when you hover over their button, so you'll no longer be surprised when a blessing gives you a useless "resist corprus disease" effect.

## No Thank You ([Nexus](https://www.nexusmods.com/morrowind/mods/49681), [Moddinghall](https://mw.moddinghall.com/file/151-no-thank-you))

While we're on the subject of shrines, this mod adds a "cancel" button to them so you can easily back out and keep your greedy paws on your gold. That's it. Both Temple and Imperial shrines are included. Just a small quality of life improvement.

## [Essential Indicators](https://www.nexusmods.com/morrowind/mods/48267)

Essential Indicators makes a number of convenience improvements to indicate when NPCs and items are important.

First, it turns the crosshair red when you're targeting an owned item (or an NPC in sneak mode), indicating you'll be committing a crime if you take it. This makes a good supplement to MCP's ownership tooltip.

Second, it turns the crosshair blue when you're targeting an essential NPC, one whose death would prevent you from completing the Main Quest in the normal manner. This includes NPCs marked with the vanilla "essential" flag (e.g. Caius Cosades, Nibani Maesa), and NPCs without that flag but whose deaths would nonetheless interfere with the Main Quest (e.g. various Ashlanders, whose deaths would prevent you from speaking to their leaders).

Also, once an NPC is no longer required for the Main Quest, they're no longer considered essential, and you'll no longer get the blue crosshair when targeting them.

Third, when targeting an item that's required for a quest, the crosshair also turns blue, and you'll see a tooltip indicating it's an essential item (you'll also see this tooltip when hovering over such an item in the inventory). This clues you in that you shouldn't sell it or drop it in a random dungeon.

In addition, you'll see a different-colored crosshair when you target an NPC that's required for a side-quest, or that's a quest giver in a guild. The mod also includes an option to display an Oblivion-like sneak indicator, and provides a few different custom crosshair options.

Just about every aspect of the mod is configurable in the MCM. The sneak indicator is a matter of personal preference, though it does mean you no longer have to keep checking the lower left corner of the screen while sneaking. However I don't recommend hiding the vanilla sneak icon; another mod further down on this list (called Stealth Improved) depends on the vanilla icon being visible.

On the Crosshair Settings page, I would disable the new default crosshair, which is similar to the big, honking vanilla crosshair, just not quite as big and not quite as honking. We'll be replacing the vanilla crosshair with a smaller, subtle dot crosshair later. (Essential Indicators does include a dot crosshair, but it's way too small, and if you increase its size in the MCM it's fuzzy and indistinct.)

## [Security Enhanced](https://www.nexusmods.com/morrowind/mods/47038)

This is another MWSE convenience mod. It allows you to do a few things:

- Set hotkeys (outside of the standard 1-9 keys set in the F1 menu) to equip lockpicks and probes.

- Cycle through all the picks/probes you have when the hotkey is pressed (the order of cycling is configurable).

- Automatically equip picks/probes whenever you activate a locked or trapped object (also configurable).

All of its options are configurable in the MCM. I recommend that you disable automatic equipping of probes, though, as that in part would defeat the purpose of another mod further down on this list, Locks and Traps Detection.

## [Torch Hotkey](https://www.nexusmods.com/morrowind/mods/45747)

An MWSE mod that basically does what it says on the tin: adds a hotkey to equip a torch.

The hotkey can actually equip any light source, not just a torch. It will automatically unequip any shield or two-handed weapon you had equipped to make way for the light source. And when you press the key again, it will unequip your light source and re-equip whatever shield or two-handed weapon you had equipped before.

There are a couple issues to be discussed. First, the hotkey will equip the *first* light source in your inventory, whatever that is, which means if you have candles in your inventory, it might equip them instead of a superior light source. Therefore it's a good idea to not carry around shitty light sources and only keep the good ones in your inventory.

It does, at least, give priority to light sources that have already been used, so if you have five identical torches stacked in your inventory, it will use one of them until it burns out before switching to the next one.

Second, by default the key bound to this function is the C key. This is convenient for me (it's the key I would have chosen anyway), but if you want to change this keybinding, the process is not made easy.

To do so, you'll need to manually edit the file MWSE\mods\Torch Hotkey\main.lua in a text editor. There's a line that says in part `filter = 46`. Change `46` to `tes3.scanCode.<key>`, with `<key>` being the key you want. For example, to change the hotkey to the x key, you would change `filter = 46` to `filter = tes3.scanCode.x`. A list of available keys and their numeric codes can be found in the file MWSE\core\tes3\scanCode.lua (do *not* modify this file).

## MWSE Hide the Skooma ([Nexus](https://www.nexusmods.com/morrowind/mods/48454), [Moddinghall](https://mw.moddinghall.com/file/144-mwse-hide-the-skooma))

How many times has this happened to you: You pop into a trader's shop to sell your haul from the last dungeon you cleared out, but when you go to barter with him he refuses to provide services because you have some Moon Sugar in your inventory. You think "oh yeah, I forgot," open your inventory and dump your Moon Sugar on the floor so the merchant will just buy your junk already. You go on your way, and several hours later, when you go to sell your Moon Sugar to one of the few merchants who'll buy it from you, you notice that you don't have any. "Where's my Moon Sugar?" you ask yourself. "Oh yeah, I dropped it on the floor at some trader's shop." But you forget exactly which trader's shop it was, or which city it was in, so you have to backtrack everywhere you think you might have traded in the past few hours looking for your 35 units of Moon Sugar.

If you're like me, this has happened to you more times than you'd care to admit. Hide the Skooma eliminates this problem. It temporarily removes Moon Sugar and Skooma from your inventory whenever you're trading with a merchant who won't buy them from you, and re-adds them afterward. Basically it lets you "hide the skooma" from the merchant so you can trade like normal without having to drop your shit on the floor and remember to pick it back up again.

This mod uses MWSE, so no plugin is required and there are no compatibility issues. It also won't hide your contraband from merchants who are willing to buy it from you.

This is my favorite Morrowind mod, and I could never play Morrowind without it again.

## Rational Names ([Nexus](https://www.nexusmods.com/morrowind/mods/50000), [Moddinghall](https://mw.moddinghall.com/file/157-rational-names))

There are many (many) annoying things about how items sort in the inventory in vanilla Morrowind. Within each type of item (weapons, armor, etc.), items sort purely alphabetically, which leads to all sorts of problems.

Weapons of different types (blunt weapons, bows, and so on) are all mixed together rather than separate. Potions are all over the place because Morrowind's naming scheme for potions is so inconsistent. Keys (and propylon indexes) are scattered throughout the misc items area, and gold is annoyingly toward the beginning of the misc items.

This mod fixes these problems by renaming items so that they'll sort more conveniently in the inventory. Weapons sort by type and then by attack. Armor sorts (by default) by weight class, then armor slot, then armor rating. Clothing sorts by slot. Potions sort by effect and then quality (with drinks and other special potions sorting separately), while tools sort by quality. Notes and magic scrolls each sort separately from regular books. Lights sort by radius and then by time. Keys, propylon indexes and soulgems all sort separately from other misc items (with soulgems additionally sorting by soul capacity), and gold sorts at the end of the misc items.

Rational Names also bypasses Morrowind's limit of 31 characters for item names, allowing longer names to display in the UI. This allows for lengthening the names of certain objects whose names were abbreviated in vanilla because of the limit.

The readme goes into more detail about exactly what the mod does for each object type. The MCM contains a number of options to configure the mod to your liking, though I mostly prefer the default settings.

This mod is highly configurable, but if you don't like it for whatever reason, there are a few smaller mods that do something similar for specific types of items: Consistent Keys ([Nexus](https://www.nexusmods.com/morrowind/mods/47954), [Moddinghall](https://mw.moddinghall.com/file/131-consistent-keys)), Potion Renamer ([Nexus](https://www.nexusmods.com/morrowind/mods/49853), [Moddinghall](https://mw.moddinghall.com/file/154-potion-renamer)), Soulgem Renamer ([Nexus](https://www.nexusmods.com/morrowind/mods/49861), [Moddinghall](https://mw.moddinghall.com/file/155-soulgem-renamer)), and Propylon Index Renamer ([Nexus](https://www.nexusmods.com/morrowind/mods/49941), [Moddinghall](https://mw.moddinghall.com/file/156-propylon-index-renamer)). You can use them instead, but, as its readme says, you won't want to use Potion Renamer alongside BTB's Game Improvements.

## [Clock Block](https://www.nexusmods.com/morrowind/mods/46292)

A simple MWSE mod that adds a small clock display to the lower right of the screen, near the mini-map. The mod can be configured to display real time or in-game time; in-game time is much more immersive. Now you can know what time it is in the game world without having to press the wait key to check.

## [HUD Weapon Charge](https://www.nexusmods.com/morrowind/mods/47962)

HUD Weapon Charge adds a bar showing the remaining charge on your weapon's enchantment; the charge bar appears directly underneath the weapon health bar (itself beneath the weapon icon), but only when your equipped weapon has a cast on strike enchantment. Now you can see how much charge your weapon has left without having to open the menu.

The MCM has a number of configurable options, but I suggest leaving them alone. There's no point displaying a new charge bar for cast on use or constant effect enchantments, and the bar's thickness and color are fine as they are.

In fact, there's a minor tweak to Morrowind.ini related to charge bar colors you can make that works well with this mod. The new weapon charge bar is blue (with default settings), but the magic charge bar (which also shows the charge for cast on use enchantments) is red, like the weapon health bar. It would be more consistent if the magic charge bar were also blue, like the weapon charge bar, and only the weapon health bar were red.

To make this change, find the line in Morrowind.ini that says:

```
color_magic_fill=200,60,30
```

and change it to:

```
color_magic_fill=53,69,159
```

## [Controlled Weapon Enchants](https://www.nexusmods.com/morrowind/mods/50142)

Weapons with cast on strike enchantments can be pretty powerful, but they have one big downside: the enchantment will fire on every weapon strike as long as it has enough charge (i.e. the enchantment can't be disabled). This means that, in some cases, many or most casts of the enchantment are at best unneeded and at worst wasted.

BTB's Game Improvements makes this even worse, as it prevents enchanted items from recharging over time (requiring using soulgems to recharge them). This means charges are even more precious, and makes it more painful to waste a charge on a weak opponent or one who resists the enchantment.

This mod allows you to toggle cast on strike weapon enchantments on and off. By default the key to toggle the enchantment is the G key, though this is configurable in the MCM. When on strike enchantments are disabled, you'll see a relatively unobtrusive X icon overlaid on the weapon icon in the HUD. The mod affects only on strike enchantments, not on use enchantments.

This represents a major convenience improvement, and makes cast on strike weapons considerably more attractive. Now you can reserve your weapon charge for when you need it, and avoid wasting charges when you don't.

## No Auto Vanity Camera ([Nexus](https://www.nexusmods.com/morrowind/mods/48933), [Moddinghall](https://mw.moddinghall.com/file/150-no-auto-vanity-camera))

This tiny mod simply prevents the game from automatically switching to vanity camera mode (where the camera circles around the player in third person) due to inactivity. You no longer have to keep moving the mouse every 30 seconds when you're trying to just watch something. You can still manually enable the vanity cam if you want.

The archive includes an MWSE version and a plugin version. I'm sure you can guess which one I recommend using. The MWSE version also allows you to customize the timeout value, if for some reason you want to.

## [Assetless No Glow](https://www.nexusmods.com/morrowind/mods/47925)

This mod simply makes it so that magic items no longer have that super-annoying, plastic shiny/reflective appearance. Not only does it remove a visual annoyance, it's also a difficulty enhancement, as you can no longer tell that an NPC has an enchanted weapon by the fact that his sword is glowing. Use that Detect Enchantment spell!

This version of No Glow requires MWSE, and is an improvement over the standard No Glow that just replaced the effect textures with blank ones. This one causes the visual effect to not be rendered at all, thus improving performance.

## [No Shield Sparkle](https://www.nexusmods.com/morrowind/mods/45989)

Another visual annoyance-fixing mod. In vanilla Morrowind, whenever you have a shield-type magic effect (Shield, Fire Shield, Frost Shield or Lightning Shield) on yourself, you'll see super-distracting little colored sparkles floating around yourself in first-person view. Any piece of equipment that provides one of these spells as a constant effect is, at least for me, pretty much unusable because of how distracting the sparkle effect is.

This mod fixes this annoyance by removing the sparkle visual effect from these spell effects. Notably, unlike a couple other mods that also address this problem, this mod does not remove the "shield bubble" (which you'll still see on yourself in third person), so that you can still tell when an NPC has a shield effect; all it removes is the sparkles.

This mod just consists of meshes. It does not require a plugin.

## [Just Drop It](https://www.nexusmods.com/morrowind/mods/49557)

Normally, when you drop an item on the ground, it will be oriented flat, even if the surface it's dropped on is not, which looks really funny and can be immersion-breaking.

This mod just causes dropped objects to orient with the ground or whatever surface they're lying on, which is a lot more realistic. It also applies to corpses when things die.

## [Character Creation Name Generator](https://www.nexusmods.com/morrowind/mods/46189)

This is just a small MWSE mod that allows you to randomly generate a lore-friendly name for your character during chargen based on race and sex. If you don't like what it picks for you, you can reroll until you do, and you can always override it and type in a custom name like normal. This is a convenience mod for those who like their characters to have lore-friendly names.

## [What Are My Attributes?](https://www.nexusmods.com/morrowind/mods/49912)

When you're choosing your race during character generation, the game doesn't tell you what the base attributes are for the selected race and sex, which means trying to remember "okay, do Dunmer start with 30 strength or 40?" for the fifth time.

This mod adds a list of base attributes to the race menu, updated when you change which race or sex is selected. Now you won't have to try to remember or look it up. It also adds the game's race descriptions to this menu, for just a little bit of immersion.

There are two tiny issues that can be fixed by tweaking the code. This mod is awesome enough to be worth it.

1. Label color

The "Attributes", "Description" and "Specials" labels are a brighter white than the other labels. To fix this, in the code you'll find three instances of this text:

```
{1,1,1,1}
```

Change them all to:

```
{0.875,0.788,0.624,1.000}
```

2. Text spacing

In the attribute tooltips, there could stand to be a bit more space between the icon and the text around it. After this line:

```
tooltipIcon.justifyText = "left"
```

add the following:

```
tooltipIcon.borderAllSides = 8
tooltipIcon.borderLeft = 1
```

And after this line:

```
tooltipTitleLabel.justifyText = "left"
```

add this:

```
tooltipTitleLabel.borderTop = 5
```

## [Class Description Tooltip](https://www.nexusmods.com/morrowind/mods/47527)

This small MWSE mod just adds tooltips containing class descriptions to the class selection menu during character generation. A nifty immersion mod.

# Graphics - User Interface

Before we start upgrading Morrowind's graphics generally, let's go ahead and improve the user interface. I don't include any complete UI overhauls on this list, but below you'll find replacements for various graphical components (with a pretty broad definition of "user interface").

## [Better Dialogue Font](https://www.nexusmods.com/morrowind/mods/36873)

The user interface in vanilla Morrowind is, for some unfathomable reason, intentionally made blurry. One of the patches in the Morrowind Code Patch fixes this, but the font the game uses to display most text is also, again for some reason, unacceptably blurry.

Better Dialogue Font is a replacement font for Morrowind, that looks just like the vanilla font, except it's sharp instead of blurry. Download, install and stop squinting.

By the way, this mod is actually one of the reasons I walked you through the whole process of creating an archive with your vanilla Data Files and installing it in Wrye Mash earlier, since it contains a new version of one of those vanilla files, and if you were to uninstall this mod for some reason the font file would be removed entirely. (Actually this mod contains a "backup" directory with a copy of the vanilla font, just in case.)

## [Better Daedric Font](https://www.nexusmods.com/morrowind/mods/44540)

This mod is similar to Better Dialogue Font, but for the daedric font (which is mainly found in scrolls). It makes the daedric font much sharper and nicer-looking.

Unfortunately, the archive is structured horribly, and will have to be adjusted manually before installing in Wrye Mash.

The mod actually includes four different versions of the daedric font. There's a "standard" version, in which the letters are different sizes and not perfectly lined up, as in vanilla Morrowind, and there's an "aligned" version, in which all the letters are the same size and aligned uniformly. Each of these is missing the letters X and Y, like in vanilla, but also included is a "+XY" variant of each version that includes these letters.

The files are all just loose in the archive, and three of them need to be renamed if you want to use them. Read the readme carefully for more information.

I prefer the "Aligned+XY" version of the font, but which one to install is really a matter of personal taste. You'll need to create an installer with the file "daedric_font_obw.tex" in it (in a Fonts directory obviously), along with the font file for the version you want. (And if that's not the standard one, you'll need to rename the font file to "daedric_font.fnt" as well.)

## [Title Screen and Logo Reworked](https://www.nexusmods.com/morrowind/mods/43657)

This mod is a higher-quality version of the main menu texture (the screen that appears with the main menu when you first load the game); it's basically the vanilla Morrowind main menu screen, only better.

There are four downloads for this mod. There are standard (4:3) and widescreen (16:9) versions of the title screen, and there are also standard and widescreen versions of the logo video that fades into the title screen (this is distinct from the "Bethesda logo" video that shows earlier than that).

The logo video is unnecessary, assuming you enabled the option in MGE XE to skip it, so just grab the title screen download (and only one version of it, depending on your monitor's aspect ratio).

## [Widescreen Splash Replacer](https://www.dropbox.com/s/kn5808h9pv7vptn/Widescreen%20Splash%20Replacer%202.0.7z?dl=1) ([Additions](https://www.nexusmods.com/morrowind/mods/48001))

Now that you've installed a superior main menu texture, you'll probably notice that it now looks better than Morrowind's vanilla splash screens. The vanilla splash screens are well designed, but they're pretty low-quality, and if you have a widescreen monitor they'll be stretched and distorted to fit (they were designed for a standard 4:3 aspect ratio).

These splash screens are basically higher-quality, widescreen versions of the vanilla ones, plus three new splash screens done in the vanilla style. It obviously only makes sense to install these splash screens if you have a widescreen monitor; if you don't, the vanilla splash screens are actually okay, or you can find a 4:3 splash replacer.

The "additions" download linked above provides yet three more splash screens, higher quality versions of three cut vanilla splash screens done in the same style. They fit in very well.

Alternative: If you prefer a more "pure vanilla" look, there's a mod called [Unstretched Splash Screens](https://www.nexusmods.com/morrowind/mods/45800), which is just the vanilla splash screens (plus a few cut ones) with black bars on the side so they won't be stretched on a widescreen monitor. It also includes an unstretched version of the vanilla main menu texture.

## [Crosshair Pack II](http://mw.modhistory.com/download-56-1312)

This mod is a collection of a (very) large number of alternative crosshairs. There are several different styles, and for each style several different colors. You can install whichever one you want, but honestly: just pick the simple "gray dot" crosshair.

However, this archive is structured just as terribly as Better Daedric Font is. You'll need to create an installer with the texture you want in it (in a Textures directory obviously), renamed to "target.dds".

## [Alternate Enchanted Item Icons](http://mw.modhistory.com/download-90-10395)

"Enchanted item icons" refers to the bright blue swirl graphic in your inventory for enchanted items. The vanilla texture is a bit too garish, but this mod fixes that.

There are actually two alternate versions in the archive. Set 1 is a subtle, soft blue glow, while set 2 is more similar to the vanilla bright blue swirl. Set 1 is clearly the better choice.

## [Ultimate Icons Replacer](http://mw.modhistory.com/download-56-6673)

As you can probably glean from the name, this mod replaces all of the game's icons with bigger, better versions. They're not actually bigger (icons are limited to 32x32), but they appear bigger in-game because the visible part of the icon takes up more of the available space. They've also been generally touched up. It's a bigger improvement than you'd think.

Some of these icons will be overwritten by later mods on this list that also include new icons, but that's okay.

# Graphics - Videos

Morrowind's vanilla cutscene videos look like garbage, especially compared to the sharp, hi-res textures we'll be installing later. The following mods will replace these videos with updated versions that are less unpleasant to watch.

Note that these mods require the "hi-def cutscene support" feature of Morrowind Code Patch; otherwise the game will crash when trying to play them.

## [HD Intro Cinematic](https://www.nexusmods.com/morrowind/mods/39329)

This mod replaces the Morrowind intro video (the one that plays when you start a new game, where Azura tells you that you've been chosen) with a higher quality, much better looking version.

There are three files on the download page, and you only need one. Nab the one that corresponds to your monitor's aspect ratio. (If you have a 1920x1080 monitor like I do, get the 16:9 version).

You'll also need to rename the video file to "mw_intro.bik" before installation.

## [Cutscenes Revamped - Cavern of the Incarnate](https://www.nexusmods.com/morrowind/mods/49126)

This is a high-quality upgrade for the Cavern of the Incarnate video (which plays in the middle of the main quest). Be sure to grab the 720p version of the mod, the one under main files. The 1080p version only works on OpenMW.

Also you'll need to adjust the archive to put the video file in a Video directory before installing in Wrye Mash.

## [Prince of Moonshadow](https://www.nexusmods.com/morrowind/mods/44492) ([Fix](https://www.nexusmods.com/morrowind/mods/45379))

This is a very cool mod that (1) replaces the in-game model of Azura with one that looks a whole lot better, and (2) replaces the cinematic video that plays when you finish the Main Quest with a better, high-resolution one.

Unfortunately, this mod also has a few vexing issues that require discussion.

First, there are three versions of the ending video, each for a different aspect ratio (4:3, 16:9, 16:10), and the archive includes all three videos instead of splitting them up into separate downloads, so you have to download them all. What's worse, the videos for 4:3 and 16:10 aspect ratios are absurdly humongous in terms of file size, far larger than the 16:9 video (the reason for this is ambiguous). Therefore, you must download this entire 1.3 GB (!) file, the overwhelming majority of which is useless if you have a 16:9 monitor like I do.

Second, the videos are not named properly. You'll need to delete the two that you don't need, and rename the one for your aspect ratio to "mw_end.bik".

Third, the included mesh is in the wrong place. It's in the main Meshes directory, when it should be in Meshes\r.

Fourth, the main version of the mod above requires Robert's Bodies, a body replacer further down on this list, to work. Specifically, it doesn't require that you actually be using Robert's Bodies, but it does require a number of the textures from Robert's Bodies be present in your Data Files directory, as the new Azura mesh uses them.

Fortunately, you don't have to actually install Robert's Bodies first to use this mod. This is where the "Fix" download above comes in. This is a fixed version of the mod (sans videos) that contains the specific Robert's Bodies textures required (and also has the mesh in the correct location, and fixes another error with the main mod). As the fix download does not include the videos, you'll still need to download the 1.3 GB main file regardless.

So, the procedure is: (1) download the enormous 1.3 GB main file, (2) make the required changes to the archive listed above and install it, and (3) download and install the "fix" archive on top.

# Graphics - Mesh Replacers

Before we get to the main texture replacers, we need to replace many of vanilla Morrowind's meshes. A mesh basically represents the shape of an object, while textures are the images painted onto that shape. Many of the vanilla meshes have various problems: some are inefficient in terms of performance, some have issues related to the mapping of textures to certain parts of the mesh, and some have too few polys and look too segmented, rather than smooth.

There are a lot of mesh replacement mods for Morrowind, and the install order here is important. Install these mods in the order listed.

## [Creature VFX Restoration](https://www.nexusmods.com/morrowind/mods/46194)

A number of creatures were supposed to have animated special effects (death effects, particle effects and so on) but, due to errors in the meshes, they were never displayed or were buggy in the vanilla game. This mod replaces the meshes for these creatures with fixed versions that will display the special effects properly.

Note that a couple of these meshes (Dagoth Ur and Ancestor Ghosts) will be replaced by other mods further on, but that's okay.

## [Correct UV Rocks](http://mw.modhistory.com/download-45-13485)

A mesh replacer for rocks. Fixes seams and other sorts of ugliness in the thousands and thousands of rocks in Morrowind.

Note that the above link is to version 1.0 of the mod, while there is a [version 1.5](https://www.nexusmods.com/morrowind/mods/46104) available on the Nexus. Version 1.5 adds bottoms to many rocks, to fix floaters. But the bottoms reduce performance and they're unnecessary with PFP, which just lowers the rocks that are too high, which is why version 1.0 is on this list instead.

There's one problematic file that needs to be deleted from the archive prior to installation: meshes\f\Terrain_rock_WG_17.nif. This file causes this particular rock to partially block the entrance to the cave Assarnud.

## [Morrowind Optimization Patch](https://www.nexusmods.com/morrowind/mods/45384)

This is the biggest and by far the most important of the mesh replacers on this list. MOP replaces an enormous number of the game's meshes, with improvements aimed at increasing performance without harming visuals. See the description on the Nexus for more information.

Optional sub-packages include a few textures that work well with the MOP meshes, "Lake Fjalding Anti-Suck" (which improves performance around Lake Fjalding on Solstheim by consolidating many of the meshes in that area), and a couple patches that can be ignored.

In addition to the core sub-package, install the Better Vanilla Textures and Lake Fjalding Anti-Suck sub-packages. (Most of the textures in Better Vanilla Textures will be overwritten by our texture replacers later on, but not all of them will be, so go ahead and install it.)

The remaining mesh replacers in this section are here primarily to provide smoother, less segmented and generally better-looking objects. They generally don't radically change the appearance of those objects, but those looking for a more vanilla-like visual experinence (or those with a lower-end machine) might choose to skip them and move on to the next section.

## [Moar Meshes](https://www.nexusmods.com/morrowind/mods/44057) ([Bugfix](https://www.dropbox.com/s/n9slolvwp8gohgz/Moar%20Meshes%201.05%20Extra%20Bugfix.7z?dl=1), [Patches](https://www.nexusmods.com/morrowind/mods/48753))

Improves and fixes issues with quite a few meshes.

There are a few bugs and errors in the main Moar Meshes archive, thus the need for the bugfix (called Moar Meshes Extra) by abot linked above. But one issue with the main archive is not addressed by the bugfix. Delete the file D\Ex_common_door_01.nif from the main archive before installation (this mesh will be replaced by another mod later on anyway). This version of the mesh causes the keyhole to look way too bright and shiny, which is why we're deleting it.

Install the main Moar Meshes archive after deleting that file, then install the bugfix archive.

The GHerb meshes are actually not needed (they're for an older version of Graphic Herbalism than the one we'll be installing), and you can delete them before installation if you'd like, but it's not necessary. The actual plant meshes will be overwritten by those in Graphic Herbalism.

Finally, there's the "patches" download, which fixes a few additional issues with Moar Meshes, mostly with doors. It comes with a "core" sub-package and several optional ones for popular texture replacers. Go ahead and install the core sub-package and those for Shacks Docks and Ships Arkitektora and Vivec and Velothi Arkitektora (we'll be installing both of those replacers later).

We'll also need to install the Project Atlas patch, but not yet. It will need to go in a different place in the install order, so create an archive with just the Project Atlas patch and save it for later.

We'll be installing Imperial Ordo Arkitektora, but the one fixed mesh for it in this archive would be overwritten by another mod later that also fixes it, so there's no need to install the patch. We'll also be installing Hlaalu Arkitektora, though it won't be our primary Hlaalu retexture; we'll really just install it for its door textures. But the included mesh for it would be overwritten by our main Hlaalu retexture mod, so there's no point in installing that one now either.

## [RR - Better Meshes](https://www.nexusmods.com/morrowind/mods/43266)

This one replaces meshes for quite a lot of the small, miscellaneous objects in the game.

There are actually several files on the downloads page, but Better Meshes is the only one we need.

Unfortunately, the "main files" sub-package includes a number of meshes that use non-vanilla texture paths, which means they won't be affected by texture replacers. Since the included textures for them suck, we'll need to remove the offending files.

First, in the Meshes\i subdirectory, delete the files in_velothismall_fresco_01 and 02. In Meshes\m, do the same with all 43 of the meshes that start with "text". Finally, delete the Textures directory.

With that done, go ahead and install the archive. Just install the "Main Files" sub-package (now that you've removed the offending book and fresco meshes from it). The "Optimized Melchior Dunmer Lanterns" sub-package is not needed; it's based on an earlier version of Melchior's mod, and we'll be installing the most recent version later. None of the other optional sub-packages is anything I'd recommend.

## [Glowing Flames](https://www.nexusmods.com/morrowind/mods/46124)

This mod fixes a few issues with light sources, especially candles, in Morrowind. Candles are now properly glowmapped, so the tip of the candle where the flame is will appear to glow (more) realistically. Also, you'll no longer see lit candles with invisible flames, or unlit candles with visible flames.

The mod comes with two plugins, but we won't actually need either. We don't need the "True Lights and Darkness tweaks" plugin, and the functionality of the "no more lightless flames" plugin is replicated by an MWSE mod we'll be installing later (the "TLAD Lights" MWSE mod that comes along with True Lights and Darkness - Necro Edit). So you can skip both plugins.

Or you could go ahead and install the "no more lightless flames" plugin if you want to see its effects in-game now. If you do, you'll need to update the plugin's masters in Wrye Mash - click on the plugin in the list on the Mods tab, right click on the header of the masters list on the right, select update, then click save at the bottom.

## [Properly Smoothed Meshes](https://www.nexusmods.com/morrowind/mods/46747) ([Flask Fix](https://www.nexusmods.com/morrowind/mods/46026))

Replaces meshes for many miscellaneous objects, plus a few other things. Improves upon some of the meshes in previous replacers as well.

The archive has several optional sub-packages: glowing candles, a few misc objects, and optional textures. Beyond the core sub-package, I only recommend the glowing candles and the barrels, but the others are mostly a matter of personal taste.

You'll also need to install the "flask fix" linked above, to fix an issue where a particular flask is too low and thus buried in the table or whatever surface it's on. The link is to "Various Retextures and Replacers," another small mod compilation. We'll also eventually need the blood replacer from this page, so you might want to go ahead and grab it now.

## [Dwemer Mesh Improvement](https://www.nexusmods.com/morrowind/mods/43101)

Now it's time to replace the meshes for Dwemer ruins with smoother, optimized models. This covers Dwemer architecture and various objects, inside and out.

## [Telvanni Mesh Improvement](https://www.nexusmods.com/morrowind/mods/42343)

Same as the above, except for Telvanni towns. This is a great improvement for those areas.

## [Overlooked Meshes Replacer](https://www.nexusmods.com/morrowind/mods/46855)

Don't worry, we're almost done with the mesh replacers. This one covers quite a few things that haven't been replaced so far.

The optional sub-package includes a more realistic looking version of repair prongs. I think it's worth installing.

## [Ingredients Mesh Replacer](https://www.nexusmods.com/morrowind/mods/44067)

This mod upgrades the appearance of a number of the game's ingredients with improved, more detailed and realistic meshes. And that's it. Super simple.

## [Dunmer Lanterns Replacer](https://www.nexusmods.com/morrowind/mods/43219)

This mod replaces a number of the game's lanterns with smoother, better-looking ones. It's quite an improvement.

There are several optional sub-packages, but we don't need any of them. We'll be installing better textures later, and I don't care for the "glow effect" myself. Just install the core sub-package.

# Graphics - Bodies

The next step in our quest to replace things that look like shit (and there's a lot of it) with things that look better is bodies. The vanilla Bethesda bodies look ugly and blocky. So let's fix that.

## [Expanded Robert's Bodies](https://www.nexusmods.com/morrowind/mods/46068)

Robert's Bodies replaces the blocky lumps of clay that Bethesda calls bodies with smooth, realistic-looking bodies. It replaces both the meshes (the shape) and the textures (the image painted over that shape) of bodies.

The download page includes several files. The one we're looking for is "Robert's Bodies - Pluginless". This file contains a version of the body replacer that does not require a plugin.

The archive contains quite a few sub-packages. The "humanoids" sub-package is the core of the mod, and replaces the non-beast races (all except Khajiit and Argonians). The meshes in this sub-package include underwear on the models to cover up genitals and breasts, like vanilla Morrowind. You'll need to install this sub-package even if you want nude humanoids (the nude sub-packages are just patches for this one).

There are two sub-packages for Khajiit: nude and peanut gallery. Only install one. Nude should be self-explanatory; the peanut gallery version has nude females but underwear on the males. The peanut gallery version is for "straight" guys who really aren't, but pretend because "mama didn't raise no fag," who are so insecure about their sexuality that the sight of an anthropomorphized cat's penis brings those conflicted feelings to the surface again and makes them uncomfortable. The nude version is for everybody else.

Next up are three sub-packages for nude bodies, removing the underwear from the humanoid races. One sub-package replaces both sexes with nude versions, one replaces only females and one only males. I install the one for both sexes myself. Underwear on Morrowind bodies is primarily for teenagers still living under the oppressive yoke of their parents, who are afraid they'll get in trouble if their prudish mom happens to walk by and sees a pair of Bosmer boobies on their screen. And we already know what kind of person needs female-only nudity.

There's also a sub-package that removes only the bra from females, plus three sub-packages that replace Robert's underwear from the core sub-package with more vanilla-friendly underwear. If you've installed the nude version, these vanilla underwear sub-packages aren't needed.

In summary, I install three sub-packages: Humanoids, Khajiit (nude), and Nude both sexes.

Note that there are actually two body replacers for Morrowind that are any good: Robert's Bodies and Better Bodies. Robert's Bodies looks vastly better than Better Bodies, especially for males, while Better Bodies is more compatible because more mods were made for it. However, there's a patch we can use for Better Clothes (see below) to avoid clipping issues with Robert's Bodies, and I haven't seen any obvious problems with the robe replacer I recommend either.

But if you prefer Better Bodies, feel free to install it. For BB, I prefer the [pluginless version](https://www.nexusmods.com/morrowind/mods/48005) with Westly's Heads, plus separate downloads for [hand fixes](https://www.nexusmods.com/morrowind/mods/47521), [textures](http://mw.modhistory.com/download-4-11353) for use with Westly's heads, and [high-resolution textures](http://mw.modhistory.com/download-10-14637) for the females (unfortunately there's no similar mod for males).

And if you don't install any body replacer at all, you'll want to install the "Chuzei fix" from Morrowind Optimization Patch (which fixes an issue with a particular helm, but isn't needed with a body replacer).

## [New Beast Bodies Pluginless](https://www.nexusmods.com/morrowind/mods/49529)

New Beast Bodies replaces the beast race bodies (Khajiit and Argonians) with ones that are not distractingly ugly. The above link is to the pluginless version of the mod, based on version 3.3 of LizTail's original.

The version of Robert's Bodies we just installed includes a Khajiit body replacement, so we only need the Argonians from this mod. However, the files for both races are all mixed in together, so you'll need to delete the Khajiit files before installing in Wrye Mash (which files to delete is obvious, and you really only need to delete the Khajiit meshes).

Also, this pluginless version of the mod only includes the "mature" (i.e. nude) version of NBB, though keep in mind that Argonians are reptiles, not mammals, so nudity doesn't mean tits and dongs.

# Graphics - Heads

While their bodies look much better now, it's still difficult to distinguish most NPCs' heads from their asses. Rectifying this situation requires chopping off their heads and replacing them with better ones.

## [Westly's Pluginless Head and Hair Replacer](https://www.nexusmods.com/morrowind/mods/50152)

Like with bodies, there are a number of options for head replacers, but I think Westly's is the top dog. Westly's heads look much better than Better Heads (an earlier and generally inferior head replacer), and, while they don't look *bad* per se, I'm not a fan of the style of MacKom's heads.

The link above is to the pluginless version of Westly's head replacer. There's also a plugin-required version (called [Master Head Pack](https://www.nexusmods.com/morrowind/mods/47605)), but I prefer to avoid unnecessary plugins.

For those who prefer a more vanilla-like aesthetic, I can recommend [Familiar Faces](https://www.nexusmods.com/morrowind/mods/50093) and [Facelift](https://www.nexusmods.com/morrowind/mods/47617) as alternatives to the mods in this section. These mods fix a number of issues with the vanilla heads, and Facelift includes upscaled textures for them. Install Familiar Faces first, then Facelift on top. The Facelift meshes are required, but the textures are optional.

## [Westly's Head and Hair Replacer - Various Fixes](https://www.nexusmods.com/morrowind/mods/47547)

There are a number of problems with Westly's Heads that this download fixes. In particular, there's a problem where Dunmer females' jaws didn't move when they spoke, and an issue where the fangs on female Orc heads didn't move properly. There's also some problem involving hair that I don't really understand.

Just install this file and forget about it.

## [Pluginless Khajiit Head Pack](https://www.nexusmods.com/morrowind/mods/43110) ([Vampires](https://www.nexusmods.com/morrowind/mods/43795))

Westly's Heads doesn't include Khajiit and Argonians, so we'll need to address them separately. This mod takes care of the Khajiit. There's actually a plugin version of this mod as well, but I wouldn't bother with it.

The first link above is to the main download page for this mod. There are two versions on the download page, one with whiskers and one without. You only need one of these, not both. You can ignore the optional file here.

The main mod for some reason does not include vampire heads, so we'll need the file called "Pluginless Khajiit Head Pack - Vampires" from the second link above. This leads to a mod page called "Various Tweaks and Fixes," which is a collection of small mods, mostly fixes for other mods. We only need the Khajiit vampire heads right now, but we'll eventually also need "Tyddy's Telvanni Fixes" and "Blank Glowmaps for Robe Overhaul," so you might want to go ahead and grab those too.

The Vampires archive contains three sub-packages. Install the textures, and either the vanilla or whiskers sub-package, depending on which version of the main mod you chose.

Don't worry about Argonians for now; Intelligent Textures, a general texture replacer further down on this list, includes upscaled versions of the vanilla Argonian heads that look just fine.

# Graphics - Shaders and Weather

There are a couple areas left in which we can enhance the visuals of Morrowind before we start on our mountain of texture replacers, and one of these areas is the shaders used. MGE XE comes with a number of default shaders, and I gave you some advice earlier, when we were installing MGE XE, about which ones to use and which ones not to. However, there are better versions of some of these shaders that we can install to further improve Morrowind's appearance.

There's also the issue of the game's weather. You've probably noticed that the nights are awfully bright, and the coloring and lighting levels for the various weather conditions are pretty bland. Clearly something must be done about this.

## [Weather Adjuster](https://www.nexusmods.com/morrowind/mods/46816)

In vanilla Morrowind, the colors and lighting levels under various weather conditions and at various times of day are determined by long lists of values in Morrowind.ini, and these values can be tweaked manually. Weather Adjuster is an MWSE mod that includes an interface that allows you to tweak these values in a different, but equally confusing and non-intuitive, way. However, at least you can see the effects immediately without leaving the game.

It comes with reasonable preset values that look better than Morrowind's defaults, and also has the advantage of allowing clouds to actually be dark at night (before the clouds were eerily bright at night). You can also have different weathers depending on region, where before any given weather condition looked the same no matter where you are.

By default, the key combination to open the Weather Adjuster interface is Shift+F4, though it can be modified in the MCM.

Feel free to play around with Weather Adjuster's values as much as you want. You can always revert back to the preset values. However, one of the mods we'll be installing soon includes a customized Weather Adjuster config file that will override any changes you make right now.

## [Morrowind Graphics Guide Shaders](https://www.nexusmods.com/morrowind/mods/46158)

This mod includes several improved shaders for use with MGE XE.

There are actually two relevant files on the downloads page, vanilla-style and Skyrim-style. The actual MGE XE shaders in the two files are identical, and the shaders are the only thing we need to install here (we've already installed Weather Adjuster, and the next mod on this list includes a custom config file for that mod). For simplicity, just download the Skyrim-style archive, because it contains less stuff we don't need.

Once you've downloaded the archive, it needs to be modified before installation. First, it contains an extraneous top-level directory that Wrye Mash doesn't know how to handle, so get rid of that.

Second, delete the mge3 directory (Wrye Mash can't install that directory anyway because it's outside of Data Files). This directory contains an .ini file for MGE XE, and if you install it, it will change your MGE XE settings in ways that you don't want. The only reason the mod creator included it is so people don't need to manually adjust their shaders list in MGE XE, but you (should) know how to do this, and if you don't, I'll walk you through it.

Finally, you can also delete the MWSE directory containing the Weather Adjuster config file, because we'll be installing a different one in a bit. All we need to install from this archive are the shaders.

## [MGE XE Shader Pack Rev2](https://drive.google.com/file/d/15gyqU9u45wniksi6prMQdMty1OYWNsQH/view?usp=sharing)

This is another shader pack, like the above. Install only the core sub-package.

Now that we've installed the shaders from these two mods in Wrye Mash, open up MGE XE, make sure the "enable shaders" checkbox is checked, and click "shader setup" to open a new window. Click the "modding" button to expand the window to show a pane where you can adjust your active shaders. From here adjusting your shader list should be straightforward.

You'll see the new shaders on the list of available shaders. Here is the shader list I recommend (and their order is important):

```
MGG SSAO
Underwater Interior Effects
Underwater Effects
Sunshafts
Bloom Soft
deband_fogawarev2
```

SSAO provides a nice shadowing effect on objects, and the sunshafts are pretty. I like the soft bloom effect, but I think fine bloom is too much. The deband_fogawarev2 shader helps reduce the phenomenon of striped "bands" low in the sky in some weather conditions. I think HDR and depth of field suck, but it's a matter of personal taste. I haven't noticed a difference using the film shader, and it can safely be ignored.

There's also the MGG darker interiors shader, which, as you might have guessed, provides the effect of making interiors darker. This is useful if you're not using an overall lighting overhaul, but we'll be installing a lighting mod later that makes interiors darker, so the MGG darker interiors shader is not needed.

Finally, there's the EdgeAA and Special Process shaders. EdgeAA can reduce sharp lines on the edge of foliage, but it tends to make everything blurry, and I don't care for it. Special Process does a lot, and I think it's really not needed.

The Nexus description for MGG Shaders recommends changing the lighting settings in MGE XE to specific values. You might have already modified these earlier when installing MGE XE, in which case just leave them alone. If not, we'll deal with these values later on in this list.

One last thing. While shaders can help make Morrowind a more beautiful game environment, they're also somewhat demanding in terms of performance. If your system is really struggling, you might want to turn off (some) shaders. I'd start with SSAO and bloom.

## MGG Weathers Darker Nights ([Nexus](https://www.nexusmods.com/morrowind/mods/47141), [Moddinghall](https://mw.moddinghall.com/file/120-mgg-weathers-darker-nights))

Weather Adjuster's default values are pretty sensible, but still kind of bland, and by default there's just one preset applied to all regions.

The MGG Shaders mod we just installed includes a Weather Adjuster config file that enhances the coloring/lighting of the weathers without going overboard, and also has region-based presets. It also includes Weather Adjuster's original default preset, in case you wanted to switch back to it.

The problem with the MGG Shaders presets is that the nights are still very bright. The "Darker Nights" download is a modified version of the config file included in MGG Shaders Skyrim-Style, which contains new presets with darker nights (it also includes the presets in the original MGG Shaders version, plus Weather Adjuster's unmodified default preset). Other than darkening the nighttime colors, the new presets are mostly identical to the original MGG Shaders presets (the few other tweaks made are described in the readme).

If for some reason you don't like the darker nights, you can always switch to the included original presets.

And if something is still not to your liking, you can tweak any of the values in Weather Adjuster and save your own presets (if you do, I recommend creating new presets so you can always switch back to the Darker Nights or original presets later).

## [Enhanced Water Shader](https://www.nexusmods.com/morrowind/mods/49964)

This is a heavily tweaked and improved water shader for use with MGE XE distant land. It looks absolutely gorgeous; it makes MGE XE's default water look drab and gray by comparison. It also (mostly) fixes the issue where you could put your eye level right at the water's surface and see super-clearly underwater.

There are three different color options available. I like the green-blue water best, but it's really a matter of taste.

The readme suggests enabling exponential fog and dynamic ripples in MGE XE distant land tab, and setting wave height to 40. This should already be the case if you're following this list.

For those who liked vanilla Morrowind's water, an alternative is [Pixel Shader Style Water](https://www.nexusmods.com/morrowind/mods/50044), which replicates the feel of the vanilla water. I like it, though it doesn't fix the see-far-underwater bug like Enhanced Water Shader does.

# Graphics - Lighting

Now it's time to transform Morrowind's lighting system. While we've installed Weather Adjuster and a tweaked config file to address exterior lighting, especially at night, and enabled a couple MGE XE options that improve lighting generally, interiors are still unrealistically bright and drab. In this section we'll fix that.

## [Let There Be Darkness](https://www.nexusmods.com/morrowind/mods/47912)

In vanilla Morrowind, interior areas, even deep caves and other dungeons, are usually unrealistically bright, and torches and other light sources (especially with the default lighting settings) are so feeble as to be useless. Not like you'd ever need a light source anyway; in vanilla Morrowind, you can basically go through the entire game without ever needing a torch or a Night-Eye spell.

The next few mods will go a long way towards improving the appearance and realism of lighting in Morrowind. First up is Let There Be Darkness, an MWSE-lua mod that, among other things, can be used to significantly darken the game's interior cells.

There are quite a few options in the MCM, and in this case I'll describe each of them.

### General and Cell Settings

- Ambient, fog and sun color adjustment

There are nine sliders here that allow you to adjust the red, blue and green components of the ambient, fog and sun color values of interior cells. These sliders represent a percentage value that the interior lighting values will be set to, but only if overrides are *not* used (see below about overrides). By default the ambient sliders are set to 50%, fog to 80% and sun to 40%, which means that, with overrides being off, the ambi/fog/sun values for interior cells will be adjusted by these percentages compared to the vanilla values (or compared to the values set by any plugin you're using which modifies them).

We'll definitely be using overrides, so for the most part the values for these sliders won't be used. However, they would still be used in interior cells added by mods, which don't have override values. I suggest leaving them at the default values.

- Apply lighting changes only to whitelisted cells

This controls whether the mod's lighting changes (including changes to ambient light values and potentially the disabling of unnatural light sources) apply to *all* cells, or only to cells on a whitelist. By default, this feature is **off** (i.e. changes are applied to all cells). There is a "Whitelist cells" page that allows you to whitelist specific cells so lighting changes will be applied in them.

I suggest leaving this feature **off**, so the mod's lighting changes will be applied to all cells.

- Cell lighting value overrides

This is a dropdown with three options: NONE, True Lights and Darkness, and di.Still.ed Lights. If set to NONE, ambient light values of interior cells will be changed consistent with the nine sliders at the top. If set to one of the other two options, the ambient light values will be determined by the mod's override list (one of the .lua files), and the ambient/fog/sun sliders will only be used if the cell has no override specified (which almost all vanilla cells do). There are two options for override values, with ambient light values from two popular lighting overhauls: True Lights and Darkness (TLAD), and di.Still.ed Lights (DL).

By default this feature is set to use the TLAD overrides, which are pulled from the ambient light values of TLAD, a version of which we'll be installing next. I recommend keeping the default setting, so we'll get TLAD's ambient light values for interior cells. However, if you think this results in some interiors being too dark, you might try the DL overrides instead.

- Use debug mode

If turned on, information about lighting values will be displayed on screen and be printed in the MWSE log. By default it's **off**, and it should stay that way.

### Light Settings

- Light radius scaling

This is a percentage value that the radius of all light sources will be set to. By default it's set to 100%, which means that the radius of lights will not be changed from the vanilla values (or, again, from the values set by any plugin that changes the radius of lights).

Normally, it would definitely be necessary to significantly boost the radius of lights, since the vanilla lights are so feeble. But the next mod we'll be installing significantly increases the radius of most light sources, and this setting would not play well with it. I highly recommend leaving this setting at the default value of 100% (i.e. the radius of lights will be unchanged by this mod).

- Light radius scaling cutoff

This is the cutoff value for the radius scaling option above. The radius of any light with a radius at or above this value will not be modified. The default is 1024. Since we're leaving the radius at 100% (unchanged) anyway, the cutoff doesn't matter. Just leave it at the default.

- Disable lights without a mesh

This disables all "unnatural" light sources in the game, i.e. all lights without a visible source. There are lots and lots of such lights in the game. By default this feature is off. Normally this feature will disable *all* lights without a mesh, but the next setting allows us to pick and choose which lights are disabled.

Whether or not to use this feature is a matter of personal preference, but I suggest turning it **on**. A lot of the unnatural lights in the game are pretty obnoxious (like the ubiquitous bright glow often seen in exteriors around the coasts), and are not really needed, especially with the changes to light sources that we'll be installing in a bit.

- Disable only blacklisted lights without a mesh

This setting modifies the previous feature by allowing you to use a blacklist (on the Blacklist lights page) to control exactly which lights are disabled. By default it's off. I recommend turning it **on** so we can have control over which unnatural lights are disabled. (Though if you don't want to disable any lights without a mesh, obviously leave both of these settings off.) We'll cover the lights blacklist in a bit.

- Disable dark (negative) lights

Morrowind sometimes uses "negative lights" to simulate darkness or shadow. Unfortunately, these negative lights look like ass with MGE XE's per pixel lighting enabled. To see what I mean, go to the Census and Excise office in Seyda Neen (the room with Socucius Ergalla) and look in the corner near the fireplace.

This feature terminates these negative lights from your game with extreme prejudice. By default it's **on**, and I recommend leaving it that way. However, if you're not using per pixel lighting for some reason (say, for performance reasons), this feature isn't as necessary, because negative lights don't look as bad without PPL.

- Disable light flickering

In vanilla Morrowind, most lights have a flicker effect. This makes the level of illumination provided by the light fluctuate noticeably, and at least to me very annoyingly. This feature disables the flicker effect from *some* lights. (It does not apply to lights that have the "fire" flag set in the Construction Set, and lots of lights do.)

By default this feature is turned on, but I recommend turning it **off**. This is primarily because the next mod we'll be installing, which drastically improves many of the game's light sources, also disables flickering for the lights it needs to be disabled for, including many that this feature doesn't touch, so it's not necessary to use this feature. Also, this feature tends to result in an increase in the perceived brightness of lights, which is really not needed with TLAD's light values which we'll be installing soon.

- Apply flicker removal to fire

This makes the previous setting apply to *all* lights, including those the game flags as fire. If we were using LTBD's flicker removal feature, I would also recommend that it be applied to fire as well. But since I recommend letting another mod handle flickering, this setting should be left **off**, as it is by default.

- Use TLAD overrides for radius and color of light sources

This is another override feature, this time for light sources rather than ambient lighting values. By default this feature is on, which means the color and radius of Morrowind's vanilla light sources (or any plugin you're using that modifies them) will be replaced by the override values taken from True Lights and Darkness. (Actually, the overrides come from the "Necro Edit" version of TLAD, which does not include some of the more radical color changes made by the original TLAD. See the next mod on this list for more on this.)

This is actually a pretty nifty feature, but there's one issue with it that prevents me from recommending it. In addition to changing the radius, time and color values of light sources, TLAD (including the Necro Edit version) also adjusts a few other light attributes, including the weight and value of many carryable light sources, in ways that make a lot of sense. LTBD's light source override list unfortunately omits these changes.

I think some of these adjustments are pretty important, so I recommend turning this feature **off** and instead using the next mod on this list to adjust light color and radius. (It can also remove the flicker effect from many lights, and we'll need to use a plugin for interior daylight - see the next mod on this list for discussion about that.)

- Use True Skyrimized Torches overrides for lights that can be carried

This is an additional light source override feature, this time with the color and radius values pulled from a mod called True Skyrimized Torches. The TST overrides only affect carryable light sources, and will override the TLAD overrides if you have both enabled.

This feature is on by default, and again I recommend turning it **off** so the version of TLAD we'll be installing next can handle light sources.

### Whitelist Cells

This page contains the whitelist of specific cells that LTBD's lighting changes will be applied to, *if* you're using the "apply lighting changes only to whitelisted cells" feature. By default, the whitelist contains all vanilla interior cells in the game except for test cells, but you can remove any of these cells from the whitelist, and can add any other interior cells (such as mod-added cells). Exterior cells cannot be whitelisted.

If you're not using the "apply lighting changes only to whitelisted cells" feature (and I recommend not using it), there's no point in making any changes to the whitelist.

### Blacklist Lights

If you're using both the "disable lights without a mesh" and "disable only blacklisted lights without a mesh" features, the blacklist determining which lights are disabled can be modified from this page. I recommend using both of those features and adjusting the blacklist as needed to suit your preferences.

By default, the blacklist contains only two lights that are ubiquitous in exteriors around Vvardenfell's coasts. I blacklist most unnatural lights (everything not mentioned below), but there are certain lights or categories of lights that you might not want to blacklist:

**Mod-added lights**: A few mods on this list, such as Glowing Atronachs and TLAD's interior daylight plugin, add meshless lights, and these lights will appear on the list of available lights after you install those mods. You probably won't want to blacklist any of the mod-added lights.

**Anything starting with "bc mushroom"**: These lights are responsible for the glow surrounding the mushrooms in the Bitter Coast (and other locations where these plants are). I very much like the glow-in-the-dark mushrooms (in fact later we'll install a whole mod, Graphic Herbalism Lighting, relating to them), so I don't blacklist these lights.

**Anything with "lava" in it**: The eerie red glow of lava comes from these lights. I don't blacklist them because I like the lava glow. Note that most of these lights start with "lava", but one of them is "light_lava".

**"ghostgate glow"**: Responsible for the glow around the Ghostfence. I think this glow is very appropriate and atmospheric and I wouldn't want to get rid of it, so I don't blacklist this light.

**"blade light"**: This light is responsible for the glow of the sword Trueflame that you'll receive as part of the Tribunal main quest. It's supposed to glow in the dark, so leave this light alone.

**"eggsack_glow_256"**: Responsible for the glow around kwama eggsacs found in egg mines. Maybe the eggsacs are bioluminescent.

**Anything starting with "bm"**: These lights are used to provide illumination in the ice caves on Solstheim. Unfortunately, the devs were particularly lazy with these caves; they have very few visible light sources like torches and instead in many cases rely almost entirely on these meshless light sources for illumination.

If you disable them, many of the Solstheim ice caves will be pitch black, including ones that obviously have NPCs living in them. It can be pretty disconcerting for a hostile NPC to suddenly jump out at you from the inky blackness, and while that would normally be a good thing, it's not exactly realistic for people to be living in total darkness.

So you might want to consider keeping these lights around, though it's a matter of personal taste.

**"z"**: This is one of the lights added by Bloodmoon and used in a few of the ice caves. The same considerations apply as above.

-----

Finally, there's one more thing about this mod you might want to change. LTBD uses the L key to bring up a menu that allows you to temporarily edit the ambient lighting values in an interior cell, just to experiment with different values and see what they look like. This is nifty, but I prefer to use the L key as my hotkey to equip a lockpick with Security Enhanced. If you do too, you can edit MWSE\mods\RFD\LetThereBeDarkness\main.lua, find the line toward the end that starts with `event.register("keyDown"`, and either change the scan code at the end of the line to a different key, or just disable this menu by commenting out this line (put two hyphens at the beginning).

## True Lights and Darkness - Necro Edit ([Nexus](https://www.nexusmods.com/morrowind/mods/47133), [Moddinghall](https://mw.moddinghall.com/file/119-true-lights-and-darkness-necro-edit))

Let There Be Darkness, which we just installed, is in many respects a replacement for this older lighting overhaul (as we've seen, it includes options to use this mod's ambient light values for interior cells and its light source values). However, LTBD lacks a couple features of TLAD which we want.

In particular, while it includes overrides for TLAD's radius/time/color values of light sources (without which interiors would be very bland and *too* dark), the overrides lack TLAD's changes to several other attributes of many lights, including weight and value. Many of these changes make a lot of sense and I want to keep them. LTBD also lacks TLAD's gorgeous interior daylight, which I can't do without. Therefore, it's necessary to install a version of TLAD.

True Lights and Darkness is a lighting overhaul that does a number of things to improve Morrowind's lighting. It significantly lowers the ambient light values of almost all interior cells (ambient light in dungeons such as caves is lowered to zero), which makes dark areas genuinely dark. It increases the radius of most light sources, increases the time that many lights last before burning out, and makes a few other tweaks. And it adjusts the color values of some light sources for (in some cases) improved appearance.

With the right lighting settings in MGE XE (see below), especially per-pixel lighting, this makes lighting in Morrowind generally much more immersive and realistic.

The "Necro Edit" archive linked above contains three sub-packages. One contains two different modified "full" versions of the TLAD plugin. These include TLAD's ambient light edits, which aren't necessary because that's handled by LTBD. Another sub-package contains several modular plugins, two for interior daylight and four more that are different versions of TLAD's light source edits. The third sub-package contains an MWSE mod that does basically the same thing as the "TLAD Lights" modular plugins, but with no plugin required and in a much more customizable way.

First, definitely install the MWSE TLAD Lights sub-package. This MWSE mod is basically a more complete and customizable version of LTBD's TLAD light source overrides. In the MCM, there are several dropdowns, one for each of the affected light attributes (radius, time, color, name, weight, value, and so on). You can choose between vanilla and TLAD values for these attributes, and in some cases can also choose "Necro edit" or "logical flicker" values. The descriptions in the MCM tell you basically what you need to know, but I'll comment briefly on light colors, flicker settings and meshes here.

TLAD makes a number of changes to the colors of lights, and some of these changes are quite radical. The original TLAD takes a lot of light sources like candles and changes their color from normal candlelight color to colors like an eerie purple, deep blue or ominous red. These changes can substantially alter the mood of many areas. They're also rather unrealistic and not to my tastes. The "Necro edit" colors revert TLAD's more radical color changes, while leaving more minor color tweaks and "lightness" changes intact.

The "flicker" effect has already been discussed under LTBD above. The "Necro edit" option will remove flicker from many lights, mainly as an anti-annoyance feature. The "logical flicker" option attempts to make the effect apply in a more consistent and realistic manner.

The "mesh" option in the MCM can be used to replicate the functionality of the "no more lightless flames" plugin from Glowing Flames (we installed Glowing Flames earlier). Assuming you have the Glowing Flames assets installed, select the Glowing Flames mesh option and you won't need to use the plugin from that mod (be sure to deactivate the "no more lightless flames" plugin if you're using it).

My recommendation is to choose "Necro edit" settings for names, colors and flicker settings, "Glowing Flames" for meshes, and "TLAD" for everything else (though if you plan to use The Midnight Oil, you might want to choose vanilla time values, to allow one of the features of that mod to be more useful). However, one of the main purposes of this mod is to be customizable, so configure the mod however you prefer (though if you don't at least enable TLAD's light radius changes, you're likely to find light sources inadequate with LTBD's TLAD ambient lighting overrides).

That leaves TLAD's interior daylight, which is not implemented in MWSE and which requires one of the "TLAD Daylight" plugins in the modular plugins subpackage. TLAD's interior daylight allows sunlight to shine through windows in appropriate interiors, depending on weather and time of day. It's very beautiful and immersive, and I highly recommend it.

If for some reason you don't want the interior daylight, you should (1) have your head examined, and (2) not bother with the modular plugins sub-package.

There are two versions of the TLAD Daylight plugin, and you should only use one. The "No Vivec Plazas" version omits the interior daylight in the Vivec plaza cells, and is intended for use with a mod called Glass Domes of Vivec, which will substantially increase lighting levels in the plazas. I recommend Glass Domes of Vivec further down on this list, so go ahead and use the No Vivec Plazas plugin. Only use the regular daylight plugin if you don't intend to use Glass Domes of Vivec.

The original TLAD readme lists some recommended changes to the lighting settings in Morrowind.ini. If you're following this list, your settings should already be similar, except that linear lights are disabled, because they're useless with per pixel lighting. If you haven't done this already, with PPL enabled, I recommend lighting coefficients of 2.619, 0.0 and 0.382 for quadratic, linear and constant, respectively (set these in MGE XE's in-game tab). If you're not using PPL, I suggest basically the same settings but with linear at 1.0 (the same as TLAD recommends).

## Waterfall Lights Remover ([Nexus](https://www.nexusmods.com/morrowind/mods/50437), [Moddinghall](https://mw.moddinghall.com/file/160-waterfall-lights-remover))

For some reason, the developers gave waterfalls in Vivec and Molag Mar an eerie blue glow, which is pretty unrealistic, not to mention off-putting - you'd normally consider glowing water a sign that something is very wrong.

This mod removes these inexplicable glowing lights, so the waterfalls just look like regular water. That's it.

## [Light Decay](https://www.nexusmods.com/morrowind/mods/46671)

This small but neat MWSE mod makes it so that torches and other light sources will burn out gradually, instead of going from full on to full off when their time expires, like a light switch was flipped off. Just a nifty realism mod.

## [The Midnight Oil](https://www.nexusmods.com/morrowind/mods/48293)

This is more of a gameplay mod than a lighting mod, but it exclusively affects how you interact with the game's lighting system, so I'm putting it here.

The Midnight Oil is an MWSE mod that makes a number of improvements to Morrowind's lights, the most important of which are:

- Lights are no longer destroyed when taken underwater, though they'll be automatically unequipped, and (except for torches) no longer cease to exist when their time runs out.

- Lights (other than torches) whose time has expired can be refilled with purchaseable refill candles or oil flasks.

- Lights placed in the world, including carryable and non-carryable lights, can be manually toggled on and off by holding down a configurable hotkey while activating them.

- Lights in the world (only non-carryable lights in settlements by default) will automatically toggle off during the day and on and night, though you can override this by toggling them manually.

This mod makes lights more useful due to the ability to recharge them, and it's a convenience mod in that you no longer have to remember to unequip your light before taking a swim. It's also a realism improvement in that streetlights and such are no longer on during the day (which improves performance in cities as well).

The MCM allows you to configure the manual toggle hotkey, and contains several options related to the automatic toggling of lights based on time of day - I think the default settings are just fine.

There's one improvement you can make to this mod by editing the code. By default, the automatic toggling of lights only happens in exterior cells, which excludes the "exterior" Mournhold cells, which are technically interiors. To make the lights in Mournhold automatically toggle as well, open the file MWSE\mods\mer\midnightOil\nightDay.lua in a text editor, find the following line:

```
if tes3.player.cell.isInterior ~= true then
```

and change it to this:

```
local playerCell = tes3.player.cell
if playerCell.isInterior ~= true or playerCell.behavesAsExterior then
```

Now the Mournhold lights will turn off during the day like in any other city.

# Graphics - General

Now that we've installed the major mesh replacers and tweaked a few other aspects of Morrowind's appearance, the next area of focus will be general graphics mods, those that change the way the game looks in one way or another and don't fit into the other categories. This will range from a massive, gamewide texture replacer, to a mod that improves the appearance of quill pens, and lots of things in between.

This is the largest section of this list in terms of number of mods. Also, like with the mesh replacers, install order is important here. While not everything has conflicts with everything else, you should install these mods in the order presented here to ensure everything looks as intended. (If a mod should be installed in a particular place in the install order in Wrye Mash, rather than at the bottom, I'll say so.)

## [Intelligent Textures](https://www.nexusmods.com/morrowind/mods/47469)

Intelligent Textures is one of the largest of the mods on this list, in terms of file size. IT includes upgraded versions of nearly every texture in vanilla Morrowind. It does this by taking the vanilla textures and upscaling them using various software tools, resulting in larger, sharper, more detailed versions of the vanilla textures.

We're installing this first so it can act as a base on which other texture replacers are applied. Even with all of the additional texture replacers on this list, IT replaces over 1300 textures that aren't covered elsewhere. IT also serves as our Argonian head replacer; the IT Argonian heads are highly detailed and I think they look great in-game.

Only install the core sub-package for now, not the atlas textures, but you'll want to create a separate archive with just IT's atlas textures for later, since it will need to be installed in a different spot in the install order. We'll deal with atlas textures later.

By the way, many of the remaining mods in this section will diverge from the vanilla aesthetic in one way or another. Those who prefer a vanilla-like appearance might choose to skip most of the rest of this section, though I strongly suggest installing Graphic Herbalism and Glow in the Dahrk regardless.

## [Papill6n Various Graphics Things](http://mw.modhistory.com/download-56-6750)

This mod is a collection of small replacers for a wide variety of things in Morrowind, from awnings, to ropes, to hammocks, to spinwheels. Given how awful hammocks still look, I'm sure you'll agree we need something like this.

The download page has a couple of optional files, but ignore them. Just grab the main download.

The archive contains many separate directories containing each individual replacer. I suggest installing the following sub-packages:

- Awning woven
- Bridge rope brown
- Corkbulb
- Kneeling stool
- Loom
- Ropes woven + hammock's pillow (bedrolls and hammocks)
- Rusted metal
- Spinningwheel + spool

The others would be overwritten by better replacers later on or are just not worth installing.

## [Seamless Papill6n Bedrolls](https://www.nexusmods.com/morrowind/mods/47266)

Part of "Ellie's Mystic Minimods," another of those small mod compilations, this tiny mod is just an update to the bedroll texture from Papill6n Various Graphics Things that removes unsightly seams.

There are a few other mods at the above link we'll eventually need, so you might want to go ahead and download Touched Up Ringmail, Vanilla Land Crackedearth Fix, and Imperial Door Fixes while you're there.

## [Soulgem Ingredient Retexture](https://www.nexusmods.com/morrowind/mods/19467)

Includes upgraded and much-improved textures for many (though not all) of the game's ingredients. Also includes new meshes for several ingredients.

Some of these ingredients will be overwritten by better replacers later, and that's okay. As the name would indicate, this mod also retextures soulgems, but those will be overwritten by better ones. We're installing this for the ingredients.

## [Improved Bread Mesh and Texture](https://www.nexusmods.com/morrowind/mods/44321)

A small mod that does a small thing very well: makes the bread ingredient look like an actual loaf of bread, rather than a vaguely ellipsoidal mass of something brown that you probably don't want to put in your mouth. Now it looks like something you might actually eat.

This mod is part of another mod compilation, "Pherim's Small and WIP Mods." There are a few other files on this page we'll eventually need, so you might want to go ahead and pick them up: New Guar Cart Mesh and Textures, Vanilla Friendly Scum Texture, and Smoothed Marshmerrow for Graphic Herbalism MWSE.

## [Throbbing Meat](https://www.nexusmods.com/morrowind/mods/45339)

Another small mod that replaces the once boring corprusmeat ingredients with animated, squirming chunks of corprus flesh, with disturbing things like eyes and mouths growing in them. It's deliciously disgusting, and makes those Sixth House bases even creepier.

For some reason that I cannot fathom, this mod includes a version of the texture tx_colony_rope, but it will be replaced by a later mod on this list.

## [Daedric Intervention - Ingredients](https://www.nexusmods.com/morrowind/mods/46044)

The link above is to a collection of replacers for various daedric-related parts of the game. There are five files available: ruins, ingredients, creatures, weapons and armor. Right now we're only looking for the ingredients replacer, but you might want to go ahead and pick up the ruins replacer as well, since we'll be installing it later.

DI Ingredients is a small replacer, only covering a few ingredients, but highly recommended.

## [Darknut's Weapons Complete](https://www.nexusmods.com/morrowind/mods/43418)

Replaces nearly every weapon in the game with an improved texture. Darknut's weapons remain very faithful to the vanilla design, while being generally sharper and more detailed than IT, with a bit "rougher" and less smooth appearance.

The archive looks like it's packaged properly for Wrye Mash, but it's not. The Textures directory contains subdirectories called 512 and 1024; 512 contains the lower quality version of the textures (for very old and slow computers), and 1024 contains the higher quality version. You'll need to move the textures out of the 1024 subdirectory into the main Textures directory, and delete the 512 directory.

## [Darknut's Armor Textures](https://www.nexusmods.com/morrowind/mods/43416)

This mod basically takes what Darknut's Weapons does for weapon textures, and does it for armor. Almost every piece of armor in the game is affected, though quite a few sets will be overwritten by the next few mods on this list.

Darknut's armor textures are done in the vanilla style; they're not necessarily higher quality than IT, but they have a darker, rougher, grittier style that I prefer. However, if you like IT's armor textures better, you might skip this one.

The link above is to the 1024 (higher quality) version of the mod, though there is also a 512 version out there for very old and slow computers. Be sure to nab the version 1.2 download, not the old 1.1 download that for some reason is above it. There are a number of issues in 1.1 that are fixed in 1.2.

It doesn't matter whether you use the "alternate" Imperial Chain Cuirass texture, since it will be overwritten anyway.

## [Touched Up Ringmail](https://www.nexusmods.com/morrowind/mods/47266)

This is part of "Ellie's Mystic Minimods," and you might have already picked up this file earlier.

Darknut's Armor Textures skips over the Nordic Ringmail Cuirass. This small mod addresses that oversight. This version is somewhat darker than the Intelligent Textures version. I like it.

## [Dark Brotherhood Armor Replacer](https://www.nexusmods.com/morrowind/mods/1610)

The vanilla Dark Brotherhood Armor looks pretty ridiculous. DBAR replaces the silly-looking DB armor with much cooler-looking ninja outfits with masks.

Also included are several alternate color schemes for the new armor. I think the pure black looks better and is more in keeping with the Dark Brotherhood's sinister vibe, though you can swap out the colors if you really want to.

There's another, and probably more popular, version of this mod called [Dark Brotherhood Armor Replacer Expanded (DBARE)](https://www.nexusmods.com/morrowind/mods/2678). DBARE adds a number of new weapons to the various DB assassins, plus a new suit of armor, in addition to replacing the vanilla DB armor. I don't recommend DBARE primarily because the new stuff is really not well balanced with BTB's Game Improvements in mind, and I don't want to bother with BTB's compatibility plugin. The original DBAR is just fine.

## [Hirez Armors Native Styles V2 Fixed and Optimized](https://www.nexusmods.com/morrowind/mods/47919)

Hirez Armors Native Styles is a great armor replacer mod for the native Dunmer armor styles. Bonemold, Ebony, Glass, Indoril and more look amazing. The version of the mod linked above has been "fixed and optimized" (thus the name) from the original version, which had tons of problems with it and required no fewer than four different downloads to install (and deleting a file in one of them first) if you wanted it to work at all without crashing the game.

This version is problem-free, and requires only a single download. Just install it and you're done.

## [Armors Retexture Outlander Styles](https://www.nexusmods.com/morrowind/mods/44210)

This mod is yet another part of our upgrade from Darknut's Armor Textures. It replaces quite a few complete sets of armor with beautiful, high quality textures. Your iron armor has never looked so good.

## Darknut's Creature Textures ([Morrowind](https://www.nexusmods.com/morrowind/mods/43420), [Tribunal](https://www.nexusmods.com/morrowind/mods/43421), [Bloodmoon](https://www.nexusmods.com/morrowind/mods/43422), [Addendum](https://www.nexusmods.com/morrowind/mods/43441))

If you can't figure out what this one does from the name, there's no help for you. It retextures nearly every creature in the game, in a vanilla-friendly style. However, I don't actually recommend installing all of them.

First, you might want to skip the Tribunal and Bloodmoon replacers. For the most part, I think IT's textures for these creatures are much higher quality.

Second, I also much prefer IT's atronachs to Darknut's. I suggest deleting the atronach textures (which ones to delete should be obvious) from the main ("Morrowind") archive before installation.

Third, the main archive has an issue that needs fixing before installation. Find the file tx_kwama_foragerspit.dds and delete it from the archive. This file is borked and will cause errors in-game.

So, if you're following my advice: (1) download the main and addendum archives, (2) delete the foragerspit texture and the atronachs from the main archive, and (3) install both archives, the main one first.

## [Glowing Atronachs](https://www.nexusmods.com/morrowind/mods/46473)

While we're on the subject of creatures, this mod is a plugin that causes all atronachs (including summoned ones) to glow, which I think is very appropriate for atronachs.

## [Divine Dagoths](https://www.nexusmods.com/morrowind/mods/45536)

Replaces Dagoth Ur and the Ash Vampires. This mod makes them look genuinely scary.

You only need the main Data Files sub-package. The other sub-packages can be safely ignored.

You don't need any of the plugins either. Without them, the mod acts as a pluginless replacer for the Ash Vampires and Dagoth Ur. The plugins give the Ash Vampires unique appearances, but can also cause conflicts with other mods on this list (and there will be enough conflicts as it is to fix later, trust me). I prefer using this mod as a pluginless replacer.

## [Better Clothes Complete](https://www.nexusmods.com/morrowind/mods/47549)

Better Clothes replaces much of the old, ugly, segmented vanilla clothing with smooth, better looking versions. Now you won't be ashamed to wear that Common Shirt around town.

Better Clothes used to be separated into several downloads (the original Better Clothes, More Better Clothes, versions for Tribunal and Bloodmoon, plus a few fixes), but now all of that is conveniently combined into a single archive for easy installation, so just download and install.

The archive also includes a high-quality texture replacer by Darknut for many of the BC clothes, replacing them with sharper, more detailed textures. I definitely recommend it. Now you'll be downright proud of that Common Shirt.

Note that Better Clothes was designed for Better Bodies, but it works pretty well with Robert's Bodies, and there's a patch we'll install shortly to address any clipping issues.

## [Better Clothes Retextured](https://www.nexusmods.com/morrowind/mods/47851)

This is a retexture for Better Clothes Complete that greatly improves the appearance of the items it covers. This mod and the Darknut retexture subpackage of Better Clothes Complete both cover items that the other doesn't, so both should be installed, but install this one second, because it's better.

## [Better Clothes Robert's Bodies Patch](https://www.nexusmods.com/morrowind/mods/47068)

The link above is to "Half11's Misc Mods," a collection of small mods. The file we're looking for is a patch for Better Clothes that eliminates clipping issues when using BC with Robert's Bodies. Just install after the other BC-related mods.

## [Better Robes](https://www.nexusmods.com/morrowind/mods/42773)

Better Clothes does not cover Morrowind's robes; it's time to fill this gap. This mod includes smoother meshes for the game's robes along with separate female versions, plus a required plugin. We're only installing this because it's required by the next mod on this list. We don't need either of the patches included in the archive.

The included .esp needs to have its masters updated in Wrye Mash (you'll notice the checkbox for it is yellow). To do this, right click on the column headers in the masters section of the Mods tab, click update, then save.

## [Robe Overhaul](https://www.nexusmods.com/morrowind/mods/43748)

Robe Overhaul is a full replacement for the game's robes with crisp, high-resolution textures. The robes look great in my opinion; this mod makes me want to actually wear them. Robe Overhaul requires Better Robes, because it makes use of some of the meshes from that mod.

There is a "basic" version of Robe Overhaul available on the download page, which is just a pure texture replacer that does not require Better Robes, but I definitely recommend the full mod.

Note that an alternative to this mod and Better Robes is [CanadianIce Robe Replacer](http://www.wolflore.net/uploads/keening/modlibrary/[CANADIAN%20ICE]%20Robe%20Replacer/), specifically the NioLiv version, which gives a unique appearance to each robe in the game (with Robe Overhaul, as in vanilla Morrowind, some unique robes have the same appearance as standard robes). I prefer Robe Overhaul because CanadianIce's replacer has relatively minor display issues with Robert's Bodies for some robes, but the CanadianIce replacer is a viable option. If you prefer it, also skip Better Robes above, as well as the blank glowmaps below.

## [Blank Glowmaps for Robe Overhaul](https://www.nexusmods.com/morrowind/mods/43795)

This is one of the files available on the "Various Tweaks and Fixes" page, and you might have already picked it up.

Robe Overhaul is great, but there's one big annoyance: some of the robes have glowmapping, which makes portions of the robes glow. Take a look at Trebonius Artorius in Vivec to see what I mean.

If you're like me and can't stand this, install this patch, which just replaces the glow textures with blanks to remove the glow effect. Problem solved.

## [Vivec God Replacement](http://mw.modhistory.com/download-56-10946)

This mod makes Vivec look a little more worthy of the title of living god, so it's at least less of a disappointment meeting him after doing all the work required to get that invitation.

There are actually two versions of this mod. The link above is to the "Creature Edition," in which Vivec is a creature as he is in the vanilla game. There's also an "[NPC Edition](http://mw.modhistory.com/download-56-10911)" that changes him to an NPC, but I don't recommend it.

There are a number of "extras":

**Armour**: An optional plugin that makes it possible to take Vivec's armor off his corpse after you kill him. The armor sucks and looks like shit, so don't bother.

**Body Textures**: Alternate textures for Vivec's body that look good with the concept head. Only use these if you use the concept head.

**Concept**: An alternate look for Vivec's head. I like it.

**Concept+Particle**: The concept head with a glowing particle effect around it. I'm not really a fan of the particle effect, but to each their own.

**Normal**: This just contains the normal head from the main portion of the mod, in case you want to go back to it, so with Wrye Mash installation this directory isn't needed at all.

**Normal+Particle**: The normal head with the particle effect.

**Older**: Alternate face textures to make Vivec look older, though they only work with the Normal or Normal+Particle heads.

I personally use the Body Textures and Concept extras, but not the others.

## [Better Almalexia](http://mw.modhistory.com/download-70-13339)

We've already replaced Azura (with Prince of Moonshadow earlier), Dagoth Ur and Vivec. This mod completes our quadfecta of god replacers by giving Almalexia a much-needed makeover. Alma's ugly Bethesda body and unsightly vanilla mug are transformed into something much more fitting for a powerful and terrible living goddess.

The archive includes a few extras that we don't want though. First, you should delete the Splash directory. It contains a new Tribunal-themed splash screen that looks very jarring alongside our upgraded vanilla-style splash screens. The alternate eye texture is also not something I recommend.

Finally, the mod includes an optional plugin that gives you the ability to loot Almalexia's armor at the end of the Tribunal main quest, but I suggest skipping the plugin. It's nothing we need. (BTB actually created an edited version of the plugin that rebalances the armor, but I still wouldn't bother with it.)

Now we've finally upgraded all of the game's gods (well, except for Sotha Sil, but nobody cares about him).

## [Skies .IV](https://www.nexusmods.com/morrowind/mods/43311)

Skies .IV includes sky meshes that stretch across the entire sky, instead of tiling across the sky as in vanilla, as well as great-looking sky textures that are vastly superior to the vanilla skies. It also includes several directories worth of extras.

As to which of the sub-packages to install:

**Skies - .IV**: This is the main sub-package, including the required sky meshes and the main sky textures. The other "skies" sub-packages are alternate skies based on other mods, and I certainly don't recommend any of them.

**Moons**: Excellent replacement textures for Morrowind's moons. The two alternate versions are clearly inferior.

**Particles**: Replaces the particle textures for things like raindrops and ash storm flakes.

There's one issue with the particles sub-package to discuss, though. In general the new particles (and ash and blight clouds) are an improvement over the vanilla ones, but I'm not a fan of the snowflakes. Skies IV's snowflakes are much thicker and heavier than vanilla, so much so as to drastically reduce visibility, especially at night. In fact, with Skies IV's particles I can see better at night in a blizzard than I can in snowy weather.

My solution to this is to delete the texture tx_bm_snowflakes_01.dds from the particles sub-package before installation. This will leave us with IT's snow (which I think looks okay), while letting us enjoy all the other pretty particles.

One more thing. As the readme states (I hope you're reading these readmes, like I said at the beginning), you need to edit Morrowind.ini and divide all the "cloud speed" lines by 5 (so, for example, `Cloud Speed=1.25` becomes `Cloud Speed=0.25`), or the clouds will be moving five times faster than normal.

## [Arukinn's Better Books and Scrolls](https://www.nexusmods.com/morrowind/mods/43100)

This mod replaces the covers and insides of books as they appear in the game world, as well as some in-game scrolls and notes textures. (Note that it doesn't replace the "menubook" texture that you see when you read a book, or the scroll texture when you have a scroll open; we'll cover those later.)

You'll actually only see these book textures for books added by mods, because another mod on this list will give each book a unique appearance. Nothing on this list adds new books, but you'll still see the scroll/note textures, so you should definitely still install this mod.

## MWSE Daleth's Book Jackets ([Nexus](https://www.nexusmods.com/morrowind/mods/48449), [Moddinghall](https://mw.moddinghall.com/file/143-mwse-daleths-book-jackets))

Daleth's Book Jackets gives each book in the vanilla game, plus expansions, its own unique cover (and unique insides, for books that appear open in-game). It's an enormous undertaking, since there are so many books, and it's very well done.

But we're not going to be using this mod as-is. We're only installing it because our real book cover replacer, Enchanted Library (see below), requires some of the assets from Daleth's Book Jackets. The version of Book Jackets linked above includes all the needed assets in a single file, which is why we're installing it instead of the original.

Install only the Core Assets sub-package from this mod. Do not install the MWSE Component sub-package, because Enchanted Library will handle actually replacing the book meshes/icons, and using the MWSE components of both mods would have undesired effects. You also don't need the other sub-packages, since the books they modify are also covered by Enchanted Library.

## [Melchior's Magnificent Manuscripts](https://www.nexusmods.com/morrowind/mods/45626)

The main portion of this mod is mostly a mesh replacer for the vanilla books, with smoother, optimized meshes. The main reason we're downloading this mod, though, is for the optional sub-package, a patch for Daleth's Book Jackets which replaces Daleth's book meshes with better-looking and more optimized versions (though this will only be visible in-game for those meshes which the next mod on this list uses).

## [Enchanted Library](https://www.nexusmods.com/morrowind/mods/48776)

This mod is our actual book covers replacer. Enchanted Library gives every book in the game a unique cover. It's a port of a similar mod for Skyrim (that added Morrowind books to that game), and the included book covers are considerably higher quality than the ones in Book Jackets.

Since the Skyrim mod didn't add every single Morrowind book, this mod relies on the Book Jackets assets to cover the books the Skyrim mod didn't include, which is why we installed the core assets from Book Jackets earlier. This mod has its own MWSE component which will replace the icons and meshes for each book.

I put this in the graphics category, but in my view this is as much of a convenience mod as it is a graphics mod. In vanilla Morrowind, with all the books using generic covers, you can't tell what a book is until you actually hover the crosshair over it. This means when you find a library with shelves full of books, you have to hover the crosshair over each book one at a time to determine what all of them are, only to discover that most of them are multiple copies of Lives of the Saints and The Anticipations, and the others are books you've already read.

But Enchanted Library gives each book a unique cover and a unique spine (most of which have the book's title printed on them), so you can tell with a quick glance what books are on the shelf, without having to hover the crosshair over each one individually. This, together with the Book Worm mod we've already installed, makes browsing through a library for new books much faster and less frustrating.

Grab the main version of the mod (2.0), along with the 2.0.1 hotfix that's needed to correct a filename flub in the main archive (or you could just rename one file before installation). Don't bother with the "lite" version of the mod in the optional files section.

The "core" sub-package is obviously required, as it contains all of the new high-quality assets. One of the two "main" sub-packages is also required; definitely install the MWSE sub-package.

Most of the rest are patches for two mods we're not using, but you might want to install the "Alt Vonwolfe Covers" sub-package, which contains alternate versions of quite a few books. I generally prefer these alternate covers, but it's really a matter of taste.

## [Vurt's Hi-Res Menubook and Scroll Pack](https://www.nexusmods.com/morrowind/mods/28562)

This mod replaces the "menubook" texture, which is the book page texture you see in the journal and when you're reading a book. It also provides four options for the scroll texture shown when reading scrolls.

There are a couple of issues with this mod, however, that require further discussion. First, while Vurt's menubook texture looks amazing, the bookmark texture (seen when viewing the journal) included in this mod sucks. Unfortunately, this texture cannot be higher resolution than vanilla, so there are limited options for replacing it. I prefer the vanilla bookmark texture, so it's necessary to delete the texture tx_menubook_bookmark.dds from the archive before installation.

Second, none of these scrolls will work for us. Scroll #1 is clearly the best. But if you install it, you'll notice in-game that scroll text is very noticeably overflowing the portion of the scroll texture intended for text. This is because the texture for scroll #1 doesn't take up enough of the available space to be compatible with the "Better Typography" feature of Morrowind Code Patch (which, you might remember, in part expands the text area of books and scrolls). This is an issue plaguing many scroll texture replacers.

Scroll #3 is the only option in this mod that takes up enough space for Better Typography, but it's radically different from the vanilla scroll texture, and I don't care for it. So, don't install any of the new scroll textures either. Just install the main menubook texture, tx_menubook.dds.

## [Pete's Scroll](https://www.nexusmods.com/morrowind/mods/47863)

Speak of the devil: This is a high quality menu scroll retexture compatible with MCP's Better Typography. It's rare among menu scroll textures in that it both (1) works with Better Typography and (2) doesn't look like shit.

Grab the file with just the scroll texture, not the one that also includes the journal (menubook) texture, which doesn't look as good as the one we just installed. Also, just use the 4k texture, which looks noticeably better than the 2k one even on a 1080p monitor. And only insane people will use the "daedric alphabet" scroll.

## [Old Dwemer Books](https://www.nexusmods.com/morrowind/mods/43339)

In Tribunal, there are a number of "old Dwemer books" that contain a single line of text describing what they appear to be. This mod changes these books to add Dwemer-looking bookart, so now you can *see* what they appear to be. Just a small immersion mod.

There are two .esps in the archive, one for use with MCP's "better typography" patch and one without. Only use one (and you really should be using better typography).

## [Bookart Replacer](https://www.nexusmods.com/morrowind/mods/48896)

More bookart here - this mod replaces the bookart in the base game with crisper, higher resolution drawings that are very faithful to the originals.

The included plugin is optional, but there's no reason not to use it, as long as you're using MCP's "better typography" patch, which you should be. The plugin modifies a handful of books so the bookart will display as intended with better typography active.

## [New Guar Cart Mesh and Textures](https://www.nexusmods.com/morrowind/mods/44321)

Part of "Pherim's Small and WIP Mods." You might have already downloaded this file earlier.

This mod replaces the common guar cart (there's one in Ald-ruhn, for example) with a smoother mesh and much better-looking textures. You'll need to install the main ("vanilla style") sub-package for the mod to work. If you want your guar carts to have rails, also install the sub-package for that, which only includes the mesh. (The rails are a matter of personal taste.)

## [Ashlanders Textures](https://www.nexusmods.com/morrowind/mods/45162)

This replacer covers one of the more neglected areas of the game: the Ashlander camps. It replaces textures for the tents, inside and out, banners, lanterns, dead silt striders and other Ashlander-related objects.

The textures in the "core" sub-package are somewhat of a mixed bag - some of them are great, but others are worse than IT. These are the textures I recommend installing from this sub-package:

- tx_ashl_lantern_01-07
- tx_ashl_screen
- tx_ashl_tent_04
- tx_guar_tarp
- tx_rope_heavy_01

Delete the others from the archive before installation. I do recommend installing the guar skin and silt strider sub-packages.

## [HQ Bug Shells](https://www.nexusmods.com/morrowind/mods/45449)

A high quality replacer for the bug shells that appear frequently in Ashlander camps. The mod includes fixed and smoothed meshes as well as high quality textures. These objects are actually also covered by the Ashlanders Textures mod we just installed (among the textures I recommended deleting from that mod), but the HQ Bug Shells versions look a lot better.

The "Extra" directory in the main archive can be deleted; there's nothing in there worth using. I definitely recommend also picking up and installing the "Vanilla Colors Tweak" download, which is basically the same textures as in the main mod, but with the colors tweaked to be more subdued and like vanilla.

## [HD Forge](https://www.nexusmods.com/morrowind/mods/46738)

This is a mesh and texture replacer for the blacksmiths' forges. It also replaces the anvils, bellows and spear holders. All of it looks good, and the forge in particular (especially the inside) looks much better than what we've been using.

The archive includes a few optional extras, but the only one I recommend is the distant land mesh. This mesh is optimized for MGE XE's distant land to improve performance, since you can't see the detail in the distance anyway. You don't need the glowing ash texture, since it would just be overwritten by another mod, and I can't recommend the animated bellows.

There's also a second download on the files page for the Bloodmoon forge, which you should go ahead and install too. Like with the regular forge, you should also install the distant land mesh, but, again like the regular forge, don't bother with the optional coals texture, since it would be overwritten anyway.

## [Articus 6th House Dagoth](https://www.nexusmods.com/morrowind/mods/48319)

This excellent replacer retextures various Sixth House items that appear in their bases, enhancing the creepy vibe of these locations. It also includes a better texture for the squirming corprusmeat from Throbbing Meat. Highly recommended.

## [Vanilla Land](https://www.nexusmods.com/morrowind/mods/45953)

Vanilla Land is our primary landscape retexture, covering basically all land textures in the game (only a tiny number of which will be overwritten by future mods on this list). All land textures are very high quality, done in 2K resolution, and faithful to the vanilla style.

There's an "optional" _land_default texture that I also recommend installing. (It's only "optional" because it causes problems if you're not using Morrowind Code Patch, but why anybody would play Morrowind without MCP is beyond me.) You'll need to move this file into the main textures directory before installation.

Oh, and if your first thought on seeing the new scum texture (in the stagnant pools in the Bitter Coast) is "this looks like absolute shit," you're not alone. Don't worry, we'll replace that specific texture with a better one in the near future.

## [Vanilla Land Crackedearth Fix](https://www.nexusmods.com/morrowind/mods/47266)

You might have already downloaded this file; this mod is part of "Ellie's Mystic Minimods."

One of the textures included in Vanilla Land is unnecessarily pixellated. This tiny mod fixes that issue. To see the difference, look at the ground in the Erabenimsun Camp.

## [Bitter Coast Scum Replacer](https://www.nexusmods.com/morrowind/mods/48291)

Now it's time to replace that godawful scum texture from Vanilla Land. This mod includes improved meshes for the scum - the texture will come in a bit.

The link above is to "Anumaril's Minor Mods," another compilation of small mods. We only need the Bitter Coast Scum Replacer download right now, but you might want to grab Vivec Palace Water Replacer while you're here.

The archive includes a number of sub-packages. The "core" sub-package is not needed, since its files are only for the animated version of the scum, which I don't care for. Instead, just install the "Standalone - Lougian's Meshes Fixed" sub-package, which contains improved scum meshes. These are actually fixed versions of the scum meshes from another mod, and the issue they fix is an annoying one: Previously you couldn't pick up an object that had been dropped in the scum. Now you can.

## [Vanilla Friendly Scum Texture](https://www.nexusmods.com/morrowind/mods/44321)

This is part of "Pherim's Small and WIP Mods," which we've already visited, so you might already have this file.

This scum texture requires the scum meshes from Lougian's Scum Retexture, or the fixed version of the same, which is why we downloaded the above mod first. This texture is faithful to the vanilla feel, while looking vastly better than the Vanilla Land scum texture.

## [Swamp Rocks](https://www.nexusmods.com/morrowind/mods/45673)

This mod replaces only one texture, the ubiquitous tx_bc_rock_03.dds, used for the rocks that are *everywhere* in the Bitter Coast. For example, all the rocks near the Seyda Neen silt strider platform use this texture. The texture we're currently using for these rocks is the one in Vanilla Land, which itself is quite high quality, so if you really like the Vanilla Land version, feel free to keep it. But I prefer the Swamp Rocks version myself.

There are actually three files available, each in a different color: swamp green, vanilla, and muddy brown. I much prefer the brown version, but feel free to check them all out and use the one you like best.

In each file are several sub-packages for different texture resolutions. I can only recommend the 2048x2048 version, which is the same size and quality (though different appearance) as the Vanilla Land texture.

## [Dangerous Lava and Oil](https://www.nexusmods.com/morrowind/mods/46140)

Despite the name, this doesn't actually make lava and hot oil more dangerous. It just makes it look a whole lot cooler (actually, a whole lot hotter). Just grab the main file for this one; I don't recommend the "visual damage" optional downloads.

A closer-to-vanilla alternative, if you can get past the groan-inducing name, is I Lava Good Mesh Replacer ([Nexus](https://www.nexusmods.com/morrowind/mods/49605), [Moddinghall](https://mw.moddinghall.com/file/65-i-lava-good-mesh-replacer)).

## [Ultimate Dunmer Strongholds](https://www.nexusmods.com/morrowind/mods/45830)

This is our texture replacer for the Dunmer strongholds.

Unfortunately, this archive is particularly poorly packaged, and will need considerable adjustment. Create sub-packages for the main part of the mod and any of the extras and alternatives you want in the "Alternative Textures" and "May Conflict" directories; you can delete the ones you don't want. Obviously in any sub-packages put the textures in a Textures directory.

First up, in the Alternative Textures directory are two alternate textures for a wall and door. I say yea to both.

There are also two different alternate versions of two trim textures. They have "plain" or "wood" in the filenames, and if you want to use one of these two options, the files will have to be renamed first before putting them in a subpackage. I like the "plain" alternative the best (and oddly one of the "wood" textures is identical to the one in the main part of the mod, which appears to be an oversight on the creator's part).

In the "May Conflict" directory are two extra textures that aren't covered in the main part of the mod; the mod creator put them here instead because they might stand out compared with other texture replacers you're using. The "ashlands" texture is for the sandpits, and the "natural cave beam" texture is for a wood pillar often found in the strongholds. I'm not a fan of the sandpit texture, and while the new wood pillar texture looks nice, it would be overwritten by the next mod on this list anyway, so don't bother with it.

## [Articus Old Stucco 2k Retexture](https://www.nexusmods.com/morrowind/mods/45880)

Texture replacer for the old, fallen-down ruins of dwellings you'll occasionally stumble across. This is pretty minor as far as architecture replacers go, but I like it.

## [Ministry of Truth Bump Mapped](https://www.nexusmods.com/morrowind/mods/42921)

A retexture with bump map for the Ministry of Truth (what is this, Oceania?), the floating moon above the Temple in Vivec. Another minor texture replacer, one of not very many for the Ministry of Truth.

However, I generally don't care for bump mapping, and I prefer to use just the regular texture from this mod, without the bump maps. If you agree with me, then create an archive with just the tx_moon_base_01.dds texture from the mod, without the other textures and without the mesh.

## [Sewers Arkitektora](https://www.nexusmods.com/morrowind/mods/43144)

This replacer covers the sewers underneath Vivec and a couple other places (it does not touch the Mournhold sewers; that comes later).

The download page contains four files, a regular version and a "dirty" version (which unfortunately just means the walls are dirtier), with an HQ and MQ (high and medium quality) version of each. The dirty files are for some reason under miscellaneous files. Just get the dirty HQ version.

## [Articus Clockwork City 2k Retexture](https://www.nexusmods.com/morrowind/mods/46149)

A high quality retexture for Sotha Sil's Clockwork City. I think this is the best of the Clockwork City retextures, and nothing on this list has touched this area since Intelligent Textures, so this is a huge improvement.

## [Daedric Intervention - Ruins](https://www.nexusmods.com/morrowind/mods/46044)

Another component of Daedric Intervention, this one covering daedric ruins. Highly recommended. The new ruins textures are a big improvement, and they also cover the daedric statue textures, which many other daedric ruins retextures don't.

## [Set in Stone](https://www.nexusmods.com/morrowind/mods/21377)

Retextures a number of the game's statues. This doesn't cover the daedric statues (which were redone by Daedric Intervention - Ruins above), and the Dwemer statues will be overwritten by better ones soon, but this will improve the statues in Vivec. It's a pretty subtle change from Intelligent Textures, but enough of an improvement that I recommend it.

## [Better Head Statues](https://www.nexusmods.com/morrowind/mods/47701)

Building upon Set in Stone which we just installed, this is a replacer for the St. Delyn and St. Olms statues on top of their respective cantons in Vivec (which are otherwise pretty neglected in terms of replacers).

The textures are based on the Set in Stone textures; the main difference is the statues' heads, which now look less like Bethesda's ugly deformed heads and a bit more like real heads.

The "optional vibrant textures" are certainly nothing I recommend.

## [Full Dwemer Retexture](https://www.nexusmods.com/morrowind/mods/44264)

A high quality retexture for Dwemer ruins (including Bamz-Amschend), creatures, weapons and armor, much superior to what's already in the game.

There are lots of files on the download page, but just get the main HQ file. There's also an MQ version, modular downloads just for certain parts of the mod, and an alternative version of the Dwemer observatory sky, but you don't need any of them.

## [Hlaalu Arkitektora Vol 2](https://www.nexusmods.com/morrowind/mods/46246)

This isn't our main Hlaalu retexture; most of the textures in this mod will be overwritten by the next mod on the list. The reason we're installing it is to update some of the Hlaalu interior loading doors; the IT ones don't look great alongside Hlaalu Retexture.

Just grab the regular HQ download and install it. Don't bother with the atlas downloads.

This is actually a very high quality retexture for the Hlaalu areas. The only reason I'm not thrilled about it is that it's too smooth and light-colored for my tastes. Thus, we're installing:

## [Hlaalu Retexture](https://www.nexusmods.com/morrowind/mods/42396)

Covers the Hlaalu areas (e.g. Balmora), exteriors and interiors. Provides a highly detailed, gritty texture that I prefer over other Hlaalu replacers.

Just nab the main 2k file on the downloads page; don't bother with any of the optional files.

## [Imperial Houses and Forts Ordo Arkitektora](https://www.nexusmods.com/morrowind/mods/43940)

Next up is the Imperial areas (e.g. Pelagiad). This mod covers both forts and other buildings, inside and out, and is the best of the Imperial replacers.

Like the last couple mods, you only need the main HQ file from the downloads page; skip the optional files.

## [Imperial Door Fixes](https://www.nexusmods.com/morrowind/mods/47266)

Yet another small mod that's part of "Ellie's Mystic Minimods" and which you might have picked up earlier.

This mod includes a few fixes for the Imperial door meshes. Also install the sub-package "Arkitektora Fix," which includes an improved texture for Imperial Ordo Arkitektora's keyhole.

## [Articus Old Mournhold and Sewers Retexture 2k](https://www.nexusmods.com/morrowind/mods/45769)

This updates the Mournhold sewers and Old Mournhold areas (the above-ground areas of Mournhold will come later). A big improvement from Intelligent Textures. Don't let the beauty of the environment distract you when you're fighting those assassins.

## [Raven Rock HD](https://www.nexusmods.com/morrowind/mods/45545)

This is by far the best texture replacer for Raven Rock that I've found. Now you'll no longer be ashamed to go home to your Factor's residence.

There are two files available on the downloads page, one with icicles, and one without. Choose whichever you prefer (you only need one, not both), but I think the icicles look fine. You might notice the version number is different between the two files (2.1 for the one with icicles, 2.2 for the one without), but the only difference between the two seems to be the icicles or lack thereof, so it doesn't matter which one you use.

## [Shacks Docks and Ships Arkitektora](https://www.nexusmods.com/morrowind/mods/43520)

Replaces the old and busted textures for - can you guess? - wooden shacks, docks and boats with some new hotness in the form of high resolution textures that might make you want to actually live in one of those shacks in Hla Oad.

As usual, just grab the HQ download and ignore the MQ one. Also, the Extras directory just contains a patch for Windows Glow that you don't need.

## [Cavern of the Incarnate Retexture](https://www.nexusmods.com/morrowind/mods/46101)

This retexture gives the Cavern of the Incarnate, where you go to meet Azura in the middle of the main quest, a major overhaul, with very high-quality textures. IT's textures for the CoI don't look bad, but these look amazing. Very fitting for a major milestone in your quest to rid Morrowind of an ancient and powerful evil.

## [Glowing Bitter Coast](http://mw.modhistory.com/download-56-14321)

Glowing Bitter Coast makes Luminous Russula and Violet Coprinus, the mushrooms found everywhere in the Bitter Coast, glow. (This does not refer to the actual light sources that illuminate nearby objects, but to the glowy spots on the plants themselves.) It also adds glowmapping to the Draggle-Tail plant, and the ingredients from these three plants. Makes me enjoy wandering through the Bitter Coast at night.

## [Comberry Bush and Ingredient Replacer](https://www.nexusmods.com/morrowind/mods/42586)

If you've ever spent any significant amount of time in the Ascadian Isles, you've noticed how hideous the comberry plant looks. This mod replaces those dull splotches of color with something that actually looks like a plant.

The archive's Data Files directory contains the main portion of the mod. I also recommend installing the Vanilla Style Textures (which, worry not, are vastly superior to the actual vanilla textures).

The Extras directory contains a patch for Graphic Herbalism; don't install it. (It's for a different version of Graphic Herbalism than the one we'll be installing later.)

## [Pherim's Fire Fern](https://www.nexusmods.com/morrowind/mods/43568)

Replaces the fire fern plant and ingredient with much sharper, better-looking versions. We're removing the suck from Morrowind one mod at a time.

Like with the comberry replacer, don't install the Graphic Herbalism patch; it's for the wrong version of GH. This time I don't care for the alternative textures, but it's a matter of taste.

## [Hackle-lo Fixed](https://www.nexusmods.com/morrowind/mods/42784)

Another ugly, borked vanilla plant, another mod that replaces that plant with a version that will no longer make you avert your eyes. It also fixes a few issues with the original mesh.

Like with the last two mods, the Graphic Herbalism patch is for an older version of that mod, so don't install it.

## [Improved Kwama Eggs and Egg Sacs](https://www.nexusmods.com/morrowind/mods/43555)

I think this is the best of the individual "plant" and ingredient replacers we'll be installing. The new egg sacs in particular look great. There are a few optional extras:

**Bump maps**: I don't care for bump maps, and I generally avoid them on this list, but they're not too bad here. Install them if you want them.

**Pulsing animation**: Makes the egg sacs pulse and writhe in a gross way, but it's the cool kind of gross, and I definitely recommend it. Install either the regular or bump mapped version (depending on whether you installed the bump maps), but not both. (Technically you could refrain from installing this subpackage, since its only file will be overwritten when we install Graphic Herbalism anyway - GH contains a patch for the pulsing animation.)

**Graphic Herbalism**: Another patch for an old version of GH to ignore.

## [Lichen Retexture](https://www.nexusmods.com/morrowind/mods/48850)

A small texture replacer for the black/green/red lichen plants. They look quite good (maybe not good enough to eat), and are a definite improvement over IT.

## [Underwater Static Replacer](http://mw.modhistory.com/download-56-11998)

This mod is a replacer for three (mostly) underwater objects: barnacles, kelp and oyster shells. It's an improvement from Intelligent Textures.

## [Vurt's Tree Textures Overhaul](https://www.nexusmods.com/morrowind/mods/28744)

Replaces the game's various tree textures (e.g. bark and leaves) with better ones than the ones in Intelligent Textures.

We're really only installing this for the Solstheim trees and the leaves of some other trees. The other textures will be overwritten by better ones soon.

Note that this mod, the earliest of Vurt's trees mods, is a texture-only replacer that leaves the tree models themselves alone. You might be wondering why I'm not including any major tree replacers, like Vurt's big tree mods, on this list.

I actually think Vurt's major tree mods are excellent for the most part. The trees they add are beautiful and significantly change and enhance the atmosphere of the game. That's part of the problem: I prefer a more vanilla feel for the game's regions.

In addition, some of the major tree replacer mods are performance killers, and the new trees of Vurt's tree mods can look very odd in the few interior cells they're used in.

For these reasons, I prefer to go with the vanilla trees with upgraded textures. But if you really want to use tree overhaul mods, go ahead. For the most part I recommend Vurt's tree mods (with the few fixes and optimizations that are out there for some of them) over others.

## [Bark Again](https://www.nexusmods.com/morrowind/mods/46134)

This is a texture replacer only for the game's various tree bark textures. It looks better than Vurt's bark, which is why we're installing it after.

The archive includes two different versions of the Bitter Coast bark, "clear" (meaning light) and dark, but we don't actually need either one, as the very next mod on this list includes superior Bitter Coast bark.

## [Bitter Coast Redux Trees](https://www.nexusmods.com/morrowind/mods/45762)

This mod replaces the Bitter Coast tree textures with versions much better than those included in the previous mods. Like Vurt's Tree Textures Overhaul, this is just a texture replacer.

There are a number of files available to download. The one we're looking for is the vanilla trees replacer, not Vurt's trees replacer (and get the HD version). While you're at it though, go ahead and download and install the HD Bitter Coast Flora archive. It only replaces the lilypads, but they're a lot better than IT's lilypads.

## [Dunmeri Urns](https://www.nexusmods.com/morrowind/mods/43541) ([Fix](https://drive.google.com/file/d/1RguLehdkOS79ArPANTrh72uZDPIo8_SY/view))

This mod includes new meshes and textures for both urns and planters (for potted plants). The textures are very crisp and high-quality; they definitely look better than IT's urns. However, as the existence of a "fix" link probably clued you in, there's a problem that needs to be addressed.

There are actually four downloads available on the Nexus page. There are HQ and MQ downloads for the regular version of the mod, and there are also HQ and MQ downloads with bump maps. I don't care for the bump maps (I generally avoid them on this list), so just grab the main HQ download.

The problem is that one of the meshes in this archive erroneously calls for a bump map texture that doesn't exist in the regular version, which will lead to errors in-game. Fortunately there's a fixed version of this mesh available, linked above, so download and install it too.

Alternatively, you could just delete the meshes from the main archive and only install the textures. You don't really need the meshes anyway, and the urn meshes (though not the planter meshes) will be overwritten by Project Atlas later.

## [Apel Sacks](https://www.nexusmods.com/morrowind/mods/42558)

A mesh and texture replacer for the various sacks in the game. This mod upgrades our sacks from medium quality to very high quality. You only need one version from the downloads page, and I prefer the version without bump maps.

## [Better Crates](https://www.nexusmods.com/morrowind/mods/45299)

As you can probably glean from the name, this mod includes improved crate textures. They're not quite as high quality as the sacks we just installed, but they're quite a bit better than IT's crates.

## [Glow in the Dahrk](https://www.nexusmods.com/morrowind/mods/45886)

Glow in the Dahrk makes many of the game's windows glow at night, as though lanterns are lit inside. It's the successor to various other mods like Windows Glow and Illuminated Windows that do basically the same thing.

The older mods implement their changes by editing cells and placing light sources around windows, and so any mod that changes the buildings can conflict. GITD works its magic with a combination of MWSE-lua scripts and special meshes that include an alternate version for nighttime. Therefore GITD accomplishes its objective in a much cleaner way than the old mods, with much lower overhead in terms of performance.

Install order is important here. Some of the mods we've already installed include different versions of the same meshes, and we want GITD to take precedence. A couple mods later in this list also replace some of these meshes, but those mods have GITD patches, so that's okay.

The archive includes a number of sub-packages. The Core sub-package is obviously required for the mod to function. Of the optional sub-packages, I recommend only the Hi Res Window Texture Replacer and Interior Sunrays (the sunrays are a matter of personal taste, but I think they look very nice).

GITD can be configured in various ways in the MCM, but the default settings are just fine, and I see no reason to change them.

## [Graphic Herbalism](https://www.nexusmods.com/morrowind/mods/46599)

Okay, this is an important one, and it's somewhat complicated, so pay attention.

In vanilla Morrowind, whenever you activate a plant to harvest it, the container menu appears, just as if you were opening a chest, and you have to manually take the ingredients, or click "take all." This is obviously a pain in the ass when you have a group of 60 identical plants to harvest. There's also no visual indication that a particular plant has been harvested, so no way to tell which ones you've harvested and which ones you haven't.

Graphic Herbalism changes all that. With GH, when you activate a plant, that plant is immediately harvested, with no container menu, and you'll see a message indicating whether or not harvesting was successful and what you got. It also changes the appearance of the plant in some way (exactly how it changes depends on the plant) to provide a visual indicator that you've harvested it.

This is obviously an enormous improvement. GH is really as much of a convenience mod as a graphics mod. It's also highly configurable in the MCM, but I don't see a need to mess with the default settings.

There are actually two versions of Graphic Herbalism. The one I link to is the MWSE version (which also works with OpenMW, if you happen to be using that), which works its magic with lua scripts and special plant meshes. There's also an [older version](https://www.nexusmods.com/morrowind/mods/43140) of GH that uses conventional Morrowind scripting instead, and is therefore messier and more performance impacting. Use the MWSE version.

Like with Glow in the Dahrk, install order is important here. Some mods earlier in this list, which we've already installed, have meshes that will be overwritten by the GH meshes. This is okay. (If we had installed GH earlier, its meshes would have been overwritten by those other mods, which is bad.) GH should be immediately after GITD in the install order.

There are several files available on the mod's download page. The only ones we need are the main Graphic Herbalism file, and the "GH Patches and Replacers" file.

The main file has two sub-packages. The "core + vanilla meshes" sub-package is required for GH to work. The "smoothed meshes" sub-package is optional, but recommended.

The Patches and Replacers file (which should obviously be installed after the main one) is pretty complicated, and includes a large number of sub-packages. Read the readme to ensure you understand what you're doing. If you're following this list, these are the sub-packages you should install:

**Correct UV Ore**: Replaces the ore rocks (ebony, glass, diamond, adamantium) with ones that blend into their environment. Contains two .esp files, but you should only use one of them. If you use the "fixed" (non-respawning) version, ore rocks will never respawn - once you've harvested them once, the ore in them is gone forever. The "respawning" version makes the ore respawn just like other "plants" do, after three months by default. The non-respawning version is more realistic, and consistent with vanilla. The respawning version would eventually allow you to harvest more adamantium, which is otherwise a finite resource. I suggest using the non-respawning version.

**Pherim's Replacers**: These are GH-compatible versions of the plant meshes from Pherim's plant replacer mods (for comberry, fire fern, hackle-lo and kwama eggs) that we installed earlier. Install the main Pherim's Replacers subpackage. The "Pherim Reflection Mapped" sub-package can be ignored, unless you really like reflection maps (I don't), in which case you should have installed the reflection maps in Pherim's comberry replacer as well.

**Pherim Pulsing Kwama**: This is highly recommended, unless you're some kind of weirdo who doesn't like the pulsing animation portion of Pherim's kwama egg replacer. (It doesn't matter whether or not you actually installed the pulsing animation portion of Pherim's mod, since its only file would be overwritten by this sub-package.) The "Pulsing Kwama Reflect" sub-package can again be ignored.

**Less Epic Plants**: The name is a reference to the mod Epic Plants (not on this list), which replaces some plant meshes with very high quality, very performance-demanding versions. This sub-package just includes improved meshes for two plants that are less performance-hungry than the Epic Plants meshes. I don't recommend the "Slightly Less Epic Plants" sub-package; I think it imposes too much of a performance penalty for not enough benefit.

**Glowing Bitter Coast Smoothed**: The next two sub-packages are patches for Glowing Bitter Coast, so the mushrooms will still have glowmapping. Install either the regular or smoothed sub-package, but not both, depending on whether you want smoothed meshes (which I definitely recommend).

And that's it for the moment. Do *not* install any of the atlas sub-packages for now; we'll come back to them in the atlas mods section of this list. The other sub-packages are patches for replacers and other mods we're not using, so they should be ignored.

## [Graphic Herbalism Lighting](https://www.nexusmods.com/morrowind/mods/47864)

This mod fixes a minor annoying issue with Graphic Herbalism. Morrowind places glowing lights around certain plants, such as the Bitter Coast mushrooms and ore rocks (which are technically plant containers). With Graphic Herbalism, these plants disappear or are altered after being picked, but the light remains. This mod causes the glowing light to disappear when the plant is harvested, a definite realism improvement.

It also corrects a few issues with the positioning of the lights. When you start harvesting mushrooms in a cluster, you'll see the light intensity decrease accordingly until finally disappearing entirely once they're all picked. It's very well done.

## [Smoothed Marshmerrow for Graphic Herbalism MWSE](https://www.nexusmods.com/morrowind/mods/44321)

This is another small mod in the "Pherim's Small and WIP Mods" compilation, so you might have already picked it up.

One plant that could still really stand to be replaced is the marshmerrow plant. The ones in the game now look like shit in my opinion. This mod gives marshmerrow an improved appearance, while being fully compatible with GH.

There are three options in the archive. The "pure replacer" sub-package is for those who aren't using the MWSE version of Graphic Herbalism. One of the other versions leaves stubs of the marshmerrow plants in the ground after you pick them, and one of them doesn't. Install whichever you prefer.

## [Graphic Herbalism Ash Yam Collision Switch](https://www.nexusmods.com/morrowind/mods/49154)

Another minor but annoying issue with Graphic Herbalism, another mod to fix it.
With GH, some plants will disappear entirely when harvested - ash yams are one of these plants. However, the "picked" version of the GH ash yam mesh still has collision, even though there's no longer a visible plant, which means you'll be stopped by an invisible object when you try to walk through the space the ash yam used to occupy. This mod simply removes the collision from picked ash yams so you'll no longer be blocked by non-existent plants.

## [Vanilla-Based Ash Grasses](https://www.nexusmods.com/morrowind/mods/43836)

This is not a "grass mod" like Remiros' Groundcover (which we'll be installing later) that adds new grass to the game. It's just a simple retexture of the various tufts of grass that appear in vanilla Morrowind.

In addition to the ash grasses (replacing the tufts of grass in the Ashlands), there's also a replacer for the Bitter Coast and Ascadian Isles grasses, which you should pick up as well.

There are actually two different versions of each replacer available for download, a regular and "brighter" version. I prefer the regular version, but it's a matter of taste.

## [Articus Mournhold 2k Retexture](https://www.nexusmods.com/morrowind/mods/46011)

Now back to our architecture replacers. This one covers the above ground Mournhold areas - not the sewers or Old Mournhold (which we've already replaced). The textures are very high quality and close to the vanilla style, unlike some other Mournhold replacers.

Of the optional sub-packages, I recommend installing the alternate cart and statues - I like them. Almalexia is covered by Better Almalexia above, and the "Flora Redux" textures do nothing in-game (the trees in the core sub-package look great anyway).

## [Redoran Arkitektora Vol 2](https://www.nexusmods.com/morrowind/mods/46235)

High quality texture replacer for the Redoran areas (e.g. Ald-ruhn), inside and out. We're quickly running out of areas to give a makeover.

This mod is separated into two components, one for regular buildings and one for Ald Skar. There are HQ and MQ downloads for the buildings on the downloads page, and HQ and UHQ (ultra high quality) downloads for Ald Skar, and you only need one of each. Get the HQ buildings file. For Ald Skar, I recommend the UHQ version (that crab shell is so big, after all) unless you're really struggling in terms of performance.

We don't need the atlas download right now, but you might as well go ahead and pick up the HQ atlas file while you're here. Don't install it yet though; we'll deal with this in the atlas mods section later.

## [Silverware Repolished](https://www.nexusmods.com/morrowind/mods/46385)

Replaces the silver plates, bowls, cups, pitchers, candles and utensils with better-looking and better-performing versions. This mod actually replaces many of the silverware meshes with atlased versions (see the atlas mods section further below for more discussion of atlases) for improved performance.

Go ahead and pick up the main file and the HD Clutter atlas texture.

In the main file, I recommend installing only the core sub-package that's required for the mod to work. The bump mapped meshes options give bump maps to the silverware, making them somewhat reflective. I generally don't care for bump maps, and the HD Clutter atlas texture doesn't work with them anyway, so I don't recommend them. All the other sub-packages would just be overwritten by other mods later anyway, so there's no need to install them.

You might as well also go ahead and install the HD Clutter atlas texture archive. This archive contains a much higher quality version of the silverware atlas texture we just installed, based on the silverware textures in a mod called HD Clutter (which we'll be installing in a bit). Now your silverware will look vastly improved in addition to being more performant.

## [Telvanni Arkitektora](https://www.nexusmods.com/morrowind/mods/43530) ([Fixes](https://www.nexusmods.com/morrowind/mods/43795))

Retextures the Telvanni areas (e.g. Sadrith Mora) with high quality textures. Also includes most of the emperor parasols.

There are several files available on the mod's download page, but you only need the main HQ download. The "missing texture" update file isn't needed because it's included in the main download, and you can also ignore the bump map downloads.

The other page ("fixes") linked above is for "Various Tweaks and Fixes," a collection of small mods, mostly small fixes for other mods. We were already here before for a head-related download, and you might have picked up the file we need then. If not, grab the file "Tyddy's Telvanni Fixes" now. (You can ignore the file related to bump maps.)

The "fixes" archive contains a few sub-packages. We need the fixed meshes and the 2k fixed textures, and you should also install the compatibility patch for Telvanni Mesh Improvements, which we installed earlier.

## [Vivec and Velothi Arkitektora Vol 2](https://www.nexusmods.com/morrowind/mods/46266)

Finally, this is the last of the major architecture texture replacers. This one covers Vivec and other Velothi buildings, such as temples.

For now we only need the main HQ file from the downloads page. You might want to go ahead and pick up one of the atlas downloads, as we'll need it later, but don't install it yet. (Ideally the UHQ atlas download is best, but it gives me problems in-game due to being too large for my graphics card, so I actually use the HQ atlas file.)

## [Better Rugs](https://www.nexusmods.com/morrowind/mods/46339)

A replacer for the various floor rugs in the game. This mod's rugs both look good and fit in well with the game environment.

There are two downloads available, a regular version and a "worn" version, containing more worn down, less colorful textures which I recommend.

## [Glory to the Empire](https://www.dropbox.com/s/oucph8b6hy46g9y/Glory%20to%20the%20Empire%202.01.7z?dl=1)

A very small mod that replaces only two textures, for imperial banners. One of these is actually identical to the one already being used in-game (from Articus Mournhold), but the other one is a dramatic improvement over the "imperial flag" texture from IT. To see the difference, look on the fort walls in Ebonheart.

## [Dunmer City Banners](http://mw.modhistory.com/download-56-6938)

Replaces the banners for things like shops and temples with new, high-quality ones. This mod is the best of the replacers I've found for these items.

Just pick up the main download from the mod page. I don't recommend either of the "alternative" textures.

## [SWG's Signs](https://www.nexusmods.com/morrowind/mods/21418)

This mod updates the wooden signs outside establishments like taverns and the Fighters and Mages Guilds. Don't worry about the note in the description calling the mod "outdated" - I think the signs look quite good.

## [Septim Gold and Dwemer Dumacs](https://www.nexusmods.com/morrowind/mods/1634)

Replaces the gold coins in the game with much better looking, high resolution textures. Also covers the Dwemer coins ("Dumacs").

Be sure you're picking up version 7.5 from the download page, not 7.0 which for some reason is above it. Also ignore the "name changes" optional file.

Don't bother with the .esp version, and I don't like the white or lavender Dumacs either, but I definitely like the "rough septims" option. It makes the coins look less shiny and new, and more rough and weathered.

## [Swappable Texture Signposts](https://www.nexusmods.com/morrowind/mods/46804)

This mod replaces the unreadable signposts in the game (the ones that point the direction to various destinations) with real, readable signposts. There are several other mods that do basically the same thing, but ST Signposts is the best-looking one I've found, and it's more customizable.

The installer includes several sub-packages with different options. The only one that's required is either Simple Signs or Environmental Signs (only use one, not both). With Simple Signs, the signposts all look the same everywhere (except for the text of course). Environmental Signs features unique-looking signposts depending on the region.

The next two sub-packages are optional; pick only one, or none, but not both. The core mod has the signs in Imperial areas in English, and the signs in Dunmer areas in Daedric (which is really just English with a different alphabet, but whatever). All Daedric Text makes all the signposts be in Daedric, while All English Text, surprisingly, makes them all be in English.

Tyddy Style Simple Signs is an alternative (and I think better) look for the Simple Signs (does not work with Environmental Signs).

I recommend using Environmental Signs (for better realism and variety), and All English Text (for better utility). However, if you're using Intelligent Textures but not other higher-quality texture replacers, you might choose Simple Signs, which I think fits in well with IT.

Alternatively, if you're playing with vanilla textures, there's [Near Vanilla Road Sign Replacer](https://www.nexusmods.com/morrowind/mods/44957), which includes vanilla resolution readable road signs.

## [Articus Immersive Crystals](https://www.nexusmods.com/morrowind/mods/46014)

Replaces the crystals found in certain caves and Telvanni buildings. The ones they're replacing (from Telvanni Arkitektora) already look quite good, so this is really more a matter of taste than anything, but I really like these.

There are two extras in the Optional directory, both of which can safely be ignored/deleted.

## [Illy's Bedspreads](https://web.archive.org/web/20161103151732/http://download.fliggerty.com/file.php?id=1108)

IT's beds actually don't look bad, but these beds look much more inviting. Don't be too tempted though; you're supposed to be exploring and adventuring!

The archive contains a couple optional "alternative" textures. I prefer the alternative purple bed texture myself, but not the alternative grey one.

## [Improved Better Skulls](https://www.nexusmods.com/morrowind/mods/46012)

If having skulls that are only improved or merely better isn't enough for you, but you insist on skulls that are both improved *and* better, then this is the mod for you. (Actually, it's an improvement on an earlier mod called Better Skulls, thus the name.) This mod optimizes the meshes for skulls and makes them look more like real skulls. There's also an optional atlas download which you should definitely grab.

The main download for the mod has three sub-packages. The one just called "Data Files" is the main version of the mod, including new textures and a required plugin. The sub-package called "Vanilla Textures" is an alternative to the main one, that just includes the improved meshes that use vanilla texture paths (despite the name, this doesn't mean they'll use actual vanilla textures, since we're using texture replacers). You should install either the main ("Data Files") or pluginless ("Vanilla Textures") sub-package, but not both. I recommend the pluginless one.

The Fixed Skeletons sub-package fixes various issues with skeletal corpses, but it's not needed because all its files would just be overwritten by Skeletons Atlased.

The optional Skeletons Atlased file improves performance by replacing the skeleton creature and skeletal corpse containers with atlased versions that only call a single large texture file. There are several sub-packages to choose from, and you only need one. Since we're using Darknut's Creature Textures (1024 version), install the Darknut Textures 1024 sub-package.

## [One True Faith - Saints and Frescoes Retexture](https://www.nexusmods.com/morrowind/mods/43810)

This is a very high quality retexture of the images on Temple shrines and several of the Temple frescoes.

There are three versions available on the download page: MQ, HQ and UHQ. The UHQ version looks noticeably better than the HQ version, even with a 1080p monitor, so unless you're having performance issues just grab the UHQ download.

## [Articus Various Retextures](https://www.nexusmods.com/morrowind/mods/46379)

Includes retextures of two things (which might not qualify it as "various"): soulgems and water pools. These are split into two separate files on the downloads page, and you should install both. The soulgems download contains an "Extras" directory that can safely be deleted, as there's nothing worth our time in there.

## [Various Retextures and Replacers - Blood](https://www.nexusmods.com/morrowind/mods/46026)

This is a completely different "Various Retextures" than the last mod, and it's a bit more worthy of the name, as this one covers *11* things (but only two of them are of interest to us).

The "various" retextures are split up into 11 separate files on the downloads page. Go ahead and nab the Blood download if you haven't already. It's a high quality blood retexture, without being over the top. You might have already picked this up earlier - you should have already installed the "flask fix."

## [Skeleton and Metal Sparks Blood Retexture](https://www.nexusmods.com/morrowind/mods/43359)

A retexture for the "blood" that comes from skeletons and Dwemer centurions when you hit them. This is pretty much the only option for these textures, but they look pretty good, certainly better than the vanilla blobs.

The "optional" gold blood texture has fewer, larger sparks, more like vanilla, but I prefer the one in the main Data Files directory myself.

## [Better Waterfalls](https://www.nexusmods.com/morrowind/mods/45424)

A retexture of waterfalls, such as the ones pouring out of the Vivec cantons. While the water that the waterfalls are flowing into is rendered by MGE XE, the waterfalls themselves are just textures rendered by Morrowind. This is in my opinion the best of the very few mods that cover waterfalls. We only need the core sub-package from this mod.

## [Vivec Palace Water Replacer](https://www.nexusmods.com/morrowind/mods/48291)

The link is to "Anumaril's Minor Mods," and you might have already picked up this file when you were here earlier.

This is a replacer for the flowing water on the four exterior levels of the Palace of Vivec. The vanilla water here looks like garbage, but this mod's animated water looks reasonably nice.

Install the core sub-package which contains the textures, and either one of the other two sub-packages, which contain differently colored versions of the water mesh. I prefer the blue color myself.

## [Subtle Smoke](https://www.nexusmods.com/morrowind/mods/47341)

The various smoke effects in the game (from chimneys, the large hanging censers in daedric ruins, and so on) are very thick and obtrusive, and in my opinion distracting. This mod tones most of these effects down. The smoke coming from chimneys will now be very subtle, and that in daedric ruins won't be so garish. A small but worthwhile improvement.

## [Dwemer Plans and Schematics](https://www.dropbox.com/s/aguk37w0004jpyw/Dwemer%20Plans%20and%20Schematics%201.0.7z?dl=1)

Texture replacer for the various "Dwemer schematics" items, like Dwemer Airship Plans and Dwemer Scarab Schematics. This is quite an improvement for these items over Intelligent Textures. They diverge from the vanilla look a bit, but not radically so.

## [HD Clutter](https://www.nexusmods.com/morrowind/mods/45972)

Contains very high quality textures for a number of "clutter" items, like bottles, pots and redware. Also retextures baskets, which haven't been touched since Intelligent Textures. We've actually already installed an atlased version of this mod's silverware textures along with Silverware Repolished above; this mod includes loose versions of those textures, for the meshes that still use them.

Pick up the main 1k download (not the "modular" version). For now, install only the main ("full") sub-package. I can't recommend Diverse Cloth, and the atlas textures will need to come later in the install order, after we've installed the required atlas meshes.

## [Long Live the Plates](https://www.nexusmods.com/morrowind/mods/43935)

The HD Clutter mod above didn't cover a number of plates, an oversight which this mod rectifies. This is a huge improvement over the IT textures the game was previously using for these plates. Clutter might be useless, but it doesn't have to be ugly.

## [Skiff Boat Texture Replacer](https://www.nexusmods.com/morrowind/mods/46479)

The small skiff boat in vanilla Morrowind uses one of the Ashlander tent textures, which doesn't look quite right for a boat. This mod replaces the skiff boat mesh with one that uses its own unique, higher quality texture.

## [Lightning Ghostfence Hi Res](https://www.nexusmods.com/morrowind/mods/43799)

This is a texture replacer for the Ghostfence (not the solid architecture, but the actual forcefield barrier). It gives the forcefield a lightning motif, and also allows you to see through it more easily. It looks very nice.

## [Fire Retexture](https://www.nexusmods.com/morrowind/mods/42554) ([Clipping Fix](https://www.dropbox.com/s/m0szfr5rqofq214/Fire%20Retexture%202.0%20Clipping%20Fix.7z?dl=1))

This is actually both a mesh and texture replacer for the fires in Morrowind. The appearance of fires, from handheld torches to the fire on top of Seyda Neen's lighthouse, is dramatically improved. Fires now actually look like a real fire, rather than a bad animation of a fire.

There is one annoyance though: the fire texture is too large (takes up too much of the texture space), and therefore clips through torches, which can be very visually distracting. The Clipping Fix linked above contains a version of the fire texture (and, for consistency, the smoke textures) resized to 75% of the original size in order to fix this issue. (The textures themselves are actually the same size, but the fire/smoke is smaller, taking up less space.)

## [R-Zero's Quill](https://www.nexusmods.com/morrowind/mods/44025)

The link is to "R-Zero's Random Retextures," another of those small mod compilations. The quill is the only file we need from this page.

This is possibly the smallest and most minor texture replacer on this list, but it's an improvement, so it makes the cut. All this does is replace the texture for the quill pen with a sharper one. The one in Intelligent Textures sucks, so just about anything would be an improvement.

## [Distant Mournhold](https://www.nexusmods.com/morrowind/mods/43255)

Distant Mournhold makes it so that you can see the Mournhold Temple over the walls from the other "exterior" Mournhold cells. A small but immersive change. In order to make the Temple visible from beyond Morrowind's in-game view distance, you'll need to regenerate distant land in MGE XE with this plugin enabled.

This is another plugin that needs its masters updated in Wrye Mash.

## [The Dream Is the Door](https://www.nexusmods.com/morrowind/mods/47423)

This is another one of those nifty little immersion mods. When trying to find the Cavern of the Incarnate as part of the main quest, you'll be told that the entrance is only seen during the hours of dawn and dusk. And yet, when you make your way to the cavern, the entrance door is perfectly visible at any time (though you won't be able to actually enter if it's not the correct time).

This mod changes that by hiding the door until you approach it at one of the correct times, at which point a new animation will reveal the door. Neat.

## [Remiros' Groundcover](https://www.nexusmods.com/morrowind/mods/46733)

Adds grass to the game, which is a sorely needed realism improvement over just flat land textures. Grass is only added in appropriate locations, and the type and appearance of grass varies widely depending on region. It even adds little rocks to the ground in rocky areas.

There are quite a few grass mods out there, but I like this one the best.

You only need the main file from the downloads page. The relevant sub-packages have an MGE XE version and an OpenMW version; obviously, install the MGE XE version of any sub-packages.

Install the "Core" sub-package, including all the .esp files in it. I also suggest installing the No Mushrooms sub-package, which gets rid of those little non-harvestable white mushrooms everywhere. If you don't mind the mushrooms, you can install the Thicker Grass sub-package instead, but I think the mushrooms look like crap. (Note that No Mushrooms itself includes Thicker Grass, so you're not missing out on anything.) The other sub-packages are either related to other mods or have optional low-quality textures that anybody using this list would want to stay far away from.

This mod works a bit differently than other mods we've installed. You should install all seven of the .esp files (one for each region with grass) in the Installers tab in Wrye Mash, but do *not* activate these .esps in the Mods tab!

Instead, regenerate distant land in MGE XE, and when you do, make sure that the seven Remiros' Groundcover .esps are selected in the plugin list. This will allow MGE XE to generate the grass. These .esps should only ever be selected in MGE XE when regenerating distant land; they should never be selected in the Mods tab of Wrye Mash to be used in-game.

As beautiful and immersive as the grass is, it does have a performance impact. In general I recommend keeping the grass density (which is set during MGE XE distant statics generation) at 100%, but if performance is hurting, try lowering it - 50% should be fine. If your system is *really* straining, this might be a mod to skip.

# Graphics - Atlas Mods

In vanilla Morrowind, most meshes contain a number of separate shapes, and each of these shapes references its own separate texture. This can be very demanding in terms of performance, as each of these shapes must call its own texture individually.

An atlas mesh is a mesh with all of its shapes combined into a single shape, which calls only one megatexture, an atlas texture, which is a single large texture containing what used to be several individual texture files. This can significantly improve performance by streamlining the process of drawing textures on all these shapes.

Only a few areas of the game have been atlased so far, but these tend to be the more demanding areas (e.g. Balmora), and these areas will see real performance improvements once we install our atlas meshes and textures. The mods in this section will ultimately have no impact on the game's visuals, but will significantly improve the game's performance in certain areas.

## [Project Atlas](https://www.nexusmods.com/morrowind/mods/45399)

Project Atlas is a collection of atlased meshes for areas and objects (e.g. Hlaalu and Redoran architecture, the Imperial dragon statue) that are particularly demanding in terms of resources. The archive also contains a number of large megatextures, or atlas textures, which are used by the atlased meshes.

Install order is particularly important here. Project Atlas should be *after* the main Graphic Herbalism archive (which itself should be after Glow in the Dahrk), but *before* the GH Patches and Replacers archive on the Installers tab in Wrye Mash. The reason for this is that GH Patches and Replacers includes atlas patches for the Bitter Coast mushrooms which must overwrite the Project Atlas meshes in order for Graphic Herbalism to work with them.

In other words, the install order is: GITD, GH, Project Atlas, GH Patches and Replacers.

One of the atlas meshes in the core sub-package is borked and needs to be deleted before installation: meshes\x\ex_imp_plat_01.nif. If this mesh is present, you'll end up stuck underwater when fast traveling from Raven Rock to Fort Frostmoth.

The "core" sub-package is obviously required. Install only one of the GITD patch sub-packages, depending on whether or not you're using GITD's interior sunrays.

If you installed the smoothed BC mushroom meshes from Graphic Herbalism (which you should have if you have any sense), then install both the BC Mushrooms Smoothed sub-package and the Smoothed Glowing BC patch sub-package. (If for some reason you didn't install smoothed mushrooms, then just install the Normal Glowing BC patch sub-package.) I also suggest the smoothed redware and urns sub-packages.

Do not install the Wood Poles Hi-Res Texture sub-package. It includes an atlas texture that's higher-quality than the vanilla-based atlas texture in the core sub-package, but we'll be installing an even more high-quality atlas texture later. What's more, this optional sub-package also includes some loose textures that would overwrite superior textures from other mods. So, don't install it.

If you start up the game again after you've installed Project Atlas, you'll notice that (parts of) the areas it covers have reverted to vanilla appearance. This is temporary. The new atlas meshes don't use the high-quality regular textures we've spent so much time installing, but instead use their own special atlas textures, and the atlas textures included in this archive are low quality ones based on the vanilla textures. Soon we'll install high-quality atlas textures for these, based on the texture replacers we've already installed.

The Project Atlas archive also includes a number of batch files (with a .bat extension) that can be used to generate your own atlas textures from higher-quality regular textures, like those in a texture replacer. Doing so requires installing Image Magick, and in some cases resizing textures with a program like Gimp. Don't worry, you won't have to do this, because some of the downloads later on include generated atlas textures.

## Graphic Herbalism Atlas Patch

Now that you've installed Project Atlas (which again should be *after* the Graphic Herbalism main file but *before* GH Patches and Replacers in the install order), go back to your GH Patches and Replacers installer in Wrye Mash and install the atlas-related sub-packages. There are four atlas sub-packages here. Install only one of the first two (for normal or smoothed meshes), and install only one of the last two (Glowing Bitter Coast atlas patches, for either normal or smoothed).

## Moar Meshes Patches - Atlas Patch

We installed "Moar Meshes Patches" earlier, which includes a patch for Project Atlas, but the atlas patch needs to come after Project Atlas in the install order. So go ahead and install the archive with just the atlas patch that you created earlier (or create one now).

## Intelligent Textures Atlas Textures

Now that we've installed our atlas meshes, it's time to start installing high-quality atlas textures, to restore our beautiful visuals along with the performance improvement of atlases.

First up is the atlas textures that come with Intelligent Textures. Remember when I said to create a separate archive with just the IT atlas textures? Now's the time to install it. Install only the atlas textures here so they'll overwrite the vanilla ones from Project Atlas; IT's regular textures should already be installed earlier in your install order.

We need this for the BC mushrooms and Imperial dragon statue, both of which are using IT textures. Technically we don't need the other atlas textures from IT, but there's no harm in just installing the whole thing.

## [Vivec and Velothi Arkitektora Atlas Texture](https://www.nexusmods.com/morrowind/mods/46266)

The file we're looking for is the Atlas download, either HQ or UHQ. (You might have already downloaded it when you were here earlier.) The UHQ file is higher resolution, but it doesn't work for everybody. For me it's borked, because it's too large for my system to handle. If you have trouble with the UHQ archive, grab the HQ one instead.

This atlas texture is based on the regular textures from Vivec and Velothi Arkitektora Vol 2 that we've already installed, so they'll be completely consistent with any objects that don't use atlases, plus interiors.

## [Redoran Arkitektora Vol 2 Atlas Texture](https://www.nexusmods.com/morrowind/mods/46235)

Like with the Vivec and Velothi Arkitektora atlas texture above, you might have already downloaded this when you were here earlier. If not, go ahead and grab the HQ atlas download. This will restore Redoran areas (such as Ald-ruhn) to the high-quality appearance to which we've grown accustomed.

## HD Clutter Atlas Textures

When we installed HD Clutter a while back, we held off on installing the included atlas textures. Now that we have the required atlas meshes, go ahead and install the atlas textures from HD Clutter. You'll need to create a separate installer for them, as they need to come after Project Atlas and the IT atlas textures in the install order.

## Atlas Texture Collection ([Nexus](https://www.nexusmods.com/morrowind/mods/47123), [Moddinghall](https://mw.moddinghall.com/file/116-atlas-texture-collection))

Normally, to generate high-quality atlas textures from the loose textures in a texture replacer, you would need to install Image Magick, and then run the atlas generator batch files included with the atlas meshes. In some cases, textures would need to be resized with a program like Gimp (since the textures being used to generate the atlas texture must have the same aspect ratio as the vanilla textures). Atlas Texture Collection saves you the trouble of doing all that.

This archive is a collection of high-quality atlas textures, generated from the texture replacers we've already installed (and therefore the atlased objects will look the same as they would without atlases, and will be visually consistent with non-atlased surfaces such as interiors).

Specifically, if you're following this list, the following atlas textures should be installed:

**Emperor Parasols**: Generated from the emperor parasol textures in Telvanni Arkitektora.

**Hlaalu**: Generated from the textures in Hlaalu Retexture.

**Imperial**: Generated from the textures in Imperial Ordo Arkitektora.

**Urns**: Generated from the textures in Dunmeri Urns.

**Wood Poles**: Generated from textures in Imperial Ordo Arkitektora and Shacks Docks and Ships Arkitektora.

**Nord**: Generated from the textures in Imperial Ordo Arkitektora.

**Nord Common**: Generated mostly from the textures in Imperial Ordo Arkitektora (the one that isn't is from Glow in the Dahrk).

If you're following this list, these are the only textures that should be installed from this archive. BC mushrooms and the Imperial dragon statue are using IT textures (and thus the IT atlas textures), and we've already taken care of Velothi and Redoran. (The Redoran sub-package in this mod contains a special Redoran atlas texture for use with the mod [RR Better Redoran Architecture](https://www.nexusmods.com/morrowind/mods/43266), which we're not using.)

Be sure to install the correct redware and urns textures, as there are multiple options for each. Also included are "half size" options for Imperial and Nord Common atlas textures. Only use these if the full size textures cause problems in-game.

The game will now look exactly the same as it did before we started installing atlases, but should perform much better in certain areas.

## [Glass Domes of Vivec](https://www.nexusmods.com/morrowind/mods/48935) ([Moonrain Edition](https://www.nexusmods.com/morrowind/mods/48946))

This is not actually an atlas mod, but I'm putting it here in the atlas mods section because it requires a Vivec/Velothi atlas texture be installed to work properly (the new canton meshes are atlas meshes).

This mod replaces the stone roofs of the Vivec plazas with glass domes. The domes are quite beautiful, and let the light in, depending on the weather. In vanilla, the Vivec plazas are very stuffy places - this mod completely changes that. It greatly enhances the atmosphere (and the light levels) in the plazas. You can see the sun through the dome overhead, hear the rain fall on the glass above you, and the plazas are bathed in sunlight during the day (at least in good weather).

Technically, the mod checks the "behaves as exterior" flag for the plazas (similar to the "exterior" Mournhold cells), so you'll experience exterior-like lighting and weather effects while in the plazas. Don't worry, you won't get rained on, as long as you've enabled the "rain/snow collision" feature of Morrowind Code Patch (which you should have earlier), and made the .ini changes that MCP feature requires.

The installation process is somewhat complicated, so pay attention. First, this mod requires the presence of a Vivec/Velothi atlas texture, because its meshes depend on it. This is why we saved this until after we installed our atlas mods.

Second, you should be using the "No Vivec Plazas" version of the TLAD interior daylight plugin, not the regular version of that plugin. With this mod, there's no need for TLAD's interior daylight in the plazas, and using it could cause problems.

Third, the Moonrain Edition fixes quite a few issues with the original, but it requires the original to be installed. So, install the original version of the mod first. You only need the assets from the original; don't use the plugin.

Next, install Moonrain Edition. The archive includes quite a few sub-packages. The "core" sub-package is required - it overwrites some, but not all, of the assets of the original mod.

Next up are two GITD patches, and you only need one of them. The GITD patches cause the exterior domes to glow at night like other windows. The "flickering" version includes a very subtle flicker effect. I use the flickering version of the patch, but it really doesn't matter which you choose.

The "optional green glow" sub-package causes the GITD light from the exterior domes to glow green. I don't prefer this one myself.

Then there's the "new weather mechanics" sub-package, which you should definitely install. This sub-package includes an MWSE component that significantly improves the way the mod handles interior weather, and also makes it compatible with Creeping Blight (a mod we'll be installing later which, among other things, allows the possibility of ashstorms or blight storms in the Ascadian Isles). It also includes a plugin to replace the one in the original mod, but you don't need this plugin either because the next sub-package includes an alternate one.

The next sub-package is "Atmospheric Arena Addition." The main mod does not include the Arena Pit in its changes. This sub-package will also cause the Arena Pit to be an "interior behaving as exterior," with enhanced lighting and interior weather, like the other plazas. Unlike the other plazas, the Arena Pit retains its stone vault; light simply shines through the slit-like windows around it. The plugin in this sub-package is the one you should use. (Only use one Glass Domes of Vivec plugin.)

The next two sub-packages are patches for mods we're not using. After that are several optional sub-packages that make the domes more transparent on the outside and inside; use them if you want, though I much prefer the darker green glass in the main mod.

Once you get the mod installed, you'll want to regenerate distant statics so the domes will appear properly in distant land.

The mod also has an MCM (assuming you're using the "new weather mechanics" sub-package, which you should be). The only interesting thing you can do in the MCM is enable a green tint to the interior sunlight in the plazas, but I don't care for it (plus it significantly increases the complexity of what the MWSE component has to do on cell change).

# Sound and Music

Before we get to our gameplay mods, there's still one more area of the game we need to transform: the sounds and music of Morrowind. The mods of this section are overhauls for sound and music, that combine to make the game much more immersive.

## [Atmospheric Sound Effects Expanded](https://www.nexusmods.com/morrowind/mods/49371)

Atmospheric Sound Effects is one of the most immersive mods on this list; it's a huge improvement. Vanilla Morrowind is extremely quiet. If you turn the music all the way down, you'll generally hear no sound effects at all, with a few exceptions (footsteps, combat, torches, water).

This mod fixes that by adding an enormous number of new sounds to the game. Cities will actually sound like they have people living in them. Wilderness areas have their own appropriate sound effects, and sounds vary depending on the weather. Weather conditions themselves now also have ambient sound effects, and you'll hear weather sounds like thunder in (certain) interiors.

The link above is to a version of ASE which merges the original mod with another sound mod called [Expanded Sounds](https://www.nexusmods.com/morrowind/mods/44787). The merged version also cleans up many of the sound files, and includes quite a few different plugins to choose from depending on your preferences (whether you want Expanded Sounds included, whether you want tavern music, and so on). The readme for ASE Expanded (ASE-EXPANDED-\<version\>-README.TXT) goes into considerable detail about the mod and the different options, and you should read it.

I recommend installing the following sub-packages: ASE Core, ExpSnds Core, ASE Expanded 3.5 (not any of the other sub-packages with alternate ESPs). In that last sub-package I recommend using the "NoMusic" plugin, which removes ASE's shitty tavern music system so that a better mod's tavern music can take over (for which, see below).

Note that a number of ASE's changes require editing Morrowind.ini. The readme contains a list of the required changes (which applies only to the "expanded" version), but that list is missing a couple of additional .ini entries included in the original ASE readme that should also be changed. Assuming you're using one of the "Expanded 3.5" plugins, the full list of .ini changes is as follows:

```
[Water]
NearWaterIndoorID=_ase_water layer
NearWaterOutdoorID=_ase_water layer

[Weather]
Minimum Time Between Environmental Sounds=5.0
Maximum Time Between Environmental Sounds=15.0

[Weather Clear]
Ambient Loop Sound ID=plx_WA_clear

[Weather Cloudy]
Ambient Loop Sound ID=plx_WA_cloudy

[Weather Foggy]
Ambient Loop Sound ID=plx_WA_foggy

[Weather Overcast]
Ambient Loop Sound ID=plx_WA_overcast

[Weather Rain]
Rain Loop Sound ID=_ase_rain
Ambient Loop Sound ID=plx_WA_rain

[Weather Thunderstorm]
Thunder Sound ID 0=plx_WE_thunder0
Thunder Sound ID 1=plx_WE_thunder1
Thunder Sound ID 2=plx_WE_thunder2
Thunder Sound ID 3=plx_WE_thunder3
Rain Loop Sound ID=plx_WE_heavyrain
Ambient Loop Sound ID=plx_WA_thunder

[Weather Ashstorm]
Ambient Loop Sound ID=plx_WA_ashstorm

[Weather Blight]
Ambient Loop Sound ID=plx_WA_blightstorm

[Weather Snow]
Ambient Loop Sound ID=plx_WA_overcast
```

(The original ASE readme does not include the line NearWaterIndoorID in its list of changes, because vanilla Morrowind ignores that line. But Morrowind Code Patch fixes that issue, so go ahead and update this line as well.)

A more modern sound mod is [AURA](https://www.nexusmods.com/morrowind/mods/48255), but I've experienced a few problems with AURA that I don't have with ASE, which is why I recommend ASE.

However, if you don't want to install a large sound mod at all, I would at least recommend [Interior Weather](http://mw.modhistory.com/download-37-10356), which makes certain weather sounds like rain and thunder audible when inside (ASE also includes this functionality). There's also a "[replacement sounds](http://mw.modhistory.com/download-37-11448)" mod with alternate versions of the interior weather sounds.

## [Morrowind Music System Extended (MUSE)](https://www.nexusmods.com/morrowind/mods/46200) ([Necro Edit](https://www.dropbox.com/s/0z4lcgpq9moopyo/MUSE%202.02%20Necro%20Edit.7z?dl=1))

Vanilla Morrowind's music is extremely limited, with a few tracks that play in battle, and a few tracks that play out of battle. The vanilla music is actually quite good, but using the same few tracks for towns, wilderness, forts and Sixth House bases means that it rarely fits the environment in which it's used.

MUSE represents the first step along the path to fixing Morrowind's music system. MUSE by itself actually won't do much of anything; it's a supremely customizable framework that allows you to implement your own custom music by creating config files managing music for different regions, cells and dungeon types, as well as custom battle music for different enemies.

Creating a workable custom music setup can be very complicated. Fortunately, all the work has already been done for you, so all you really have to do is install a few archives in Wrye Mash and you're done.

There are a few things to be addressed with MUSE before we install our MUSE-compatible music pack. First, I suggest deleting the default config files in MWSE\config\MS, along with all the empty directories in music\MS, before installation. This isn't strictly necessary, but it can avoid confusion later after you install the custom config files and music directories.

Second, there are a few bugs in MUSE that desperately need fixing, plus a few ways in which the MUSE code can be tweaked to make it work better with the music pack we'll be installing.

The "Necro Edit" download above contains fixed versions of several of MUSE's files. It doesn't contain all the required files, so you'll still need to download and install MUSE from the Nexus first.

The Necro Edit file contains two sub-packages, and you should only install one. The "bugfix" sub-package just fixes the outright bugs to make MUSE function basically as its creator intended. The "Necro Edit" sub-package also makes a few additional tweaks that work well with Better Music System (the pack of music and custom config files we'll be installing next). The readme contains a more detailed description of these changes, and the Nexus description of the next mod on this list has even more details.

For this list, I definitely recommend installing the Necro Edit sub-package. However, if you want to use the air or underwater music functions of MUSE, or particularly like the way MUSE handles the combat music threshold, or are using different music tracks than BMS uses and don't want to disable combat music in the Mortrag Glacier maze cells, then install the bugfix sub-package instead.

Finally, MUSE has a few adjustable options in its MCM. If you installed the Necro Edit sub-package in the fixed code archive, it doesn't matter what you set the combat threshold to, since it won't be used anyway. Otherwise, set it how you like it, but I wouldn't set it higher than the default unless you don't want to hear battle music very much.

There's also a region music queueing option, which is on by default. This means that when you enter a new region, the currently playing track will finish before the new region's music starts playing. Disabling this option will cause the new region's music to start playing right away as soon as you enter the region.

I prefer to disable this option, but it's really a matter of personal taste. (Sometimes having this option disabled can cause the music to switch back and forth when you're traveling right along the boundary of a town cell, but I think that's better than the wrong music playing when you enter a region.)

## Better Music System - MUSE Version ([Nexus](https://www.nexusmods.com/morrowind/mods/48665), [Moddinghall](https://mw.moddinghall.com/file/147-better-music-system-muse-version), [with music](https://www.dropbox.com/s/ckhveds0r366dqv/BMS%20MUSE%20Version%201.0%20with%20music.7z?dl=1))

This is our last step in overhauling the music system.

The [original](http://mw.modhistory.com/download-58-13678) Better Music System was created by Xiran, and used a plugin with a lot of complicated and performance-demanding mwscript to make different music play in different situations. Then BTB [came along](https://web.archive.org/web/20150423044052/http://btb2.free.fr/files/morrowind_bms.zip) and [improved](http://mw.modhistory.com/download-58-15318) BMS, simplifying it in the process. This MUSE version consists of a collection of custom MUSE config files that closely replicate the functionality of BTB's version of BMS, with a few adjustments (and with much better performance, since we're using MUSE, which uses MWSE).

With Better Music System, different tracks will play in different circumstances. There are tracks that play in different towns, in wilderness areas, on Red Mountain, on Solstheim, in various types of dungeons, and in battle depending on how strong the enemies you're fighting are.

Since we're using MUSE, all of this is highly configurable. You could grab the version of the mod with config files only (and no music tracks), from the Nexus or Moddinghall links above, and then use your own music to create a highly customized soundtrack. (You would need to manually transfer music tracks to all the mod's empty music directories.)

However, I recommend just getting the version of the mod that includes music tracks (the "with music" link above) and save yourself the hassle. The included tracks are all from BTB's soundtrack for his version of BMS, and the custom music that will play in various circumstances in this mod is basically the same as with BTB's plugin.

The tracks from BTB's soundtrack are highly appropriate to the surroundings and circumstances, with memorable tracks that you'll come to associate with Morrowind (even if you happen to recognize some of the tracks from elsewhere).

Just download the "with music" file, install it, and you're done. You can always tweak or change which tracks play in which circumstances if you feel the need; it's as simple as dragging music files between directories.

The Nexus description for this mod contains quite a bit of information about how MUSE works, and will be useful to anybody who wants to dive into MUSE configuration and customize the config files or create their own.

# Gameplay Mods

This section consists of mods that make some gameplay change, but that don't have a significant impact on game balance or difficulty (though some of these mods could probably also be put in the balance mods section). Basically, if it doesn't fit into one of the other categories, it goes here.

## [Magicka Expanded](https://www.nexusmods.com/morrowind/mods/47111)

Fundamentally, this mod is a framework that allows other mods to do funky and cool things with the game's magic system. The only reason we're installing it is because the version of Enhanced Detection (the next mod on this list) that I recommend requires it. (If you intend to install the "lite" version of ED, or don't intend to install ED at all, then skip this mod.)

There are several sub-packages in the archive; we only need the main "framework" sub-package. The framework by itself will make no changes to the game, but Enhanced Detection needs it to work its magic.

The other sub-packages of this mod add "spell tomes" of various new magic effects to the game, and I don't recommend any of them.

## [Enhanced Detection](https://www.nexusmods.com/morrowind/mods/47480) Lite/Less Lite ([Nexus](https://www.nexusmods.com/morrowind/mods/48471), [Moddinghall](https://mw.moddinghall.com/file/145-enhanced-detection-lite))

Enhanced Detection makes a number of changes to the magical detection effects (Detect Animal, Detect Enchantment and Detect Key). First among these, and the main reason we're installing this mod, is that it adds sweet new visual effects to these spells. In vanilla, detected items are only shown as lame little dots on the local map and minimap. With ED, there are really nifty effects shown when looking at a detected object, so you don't need to rely on the local map.

This is particularly important with another mod on this list, Map and Compass, which, at least when used properly, disables the local map. This would otherwise render the detect effects useless, but Enhanced Detection allows them to remain useful (and you'll want to use them just for the cool VFX).

The full version of ED makes several other changes. It adds new magic effects for different types of objects (such as daedra, doors, corpses and traps). It creates new spells with these effects, modifies some vanilla spells to add the new effects, and adds the new spells to NPCs.

It also makes a few changes to the functionality of the vanilla detect effects. It causes Detect Animal to only detect "normal" creatures, excluding daedra, undead and humanoid creatures, and also excluding "automatons" like Dwemer centurions. It also does not detect NPCs, even if you're using the "detect life spell variant" MCP patch that normally causes Detect Animal to detect NPCs. The full version also causes Detect Enchantment to detect soulgems, which it doesn't in vanilla.

The "lite" version linked above actually contains two modified versions of the mod: lite and less lite. The lite version omits all of the additional changes in the full version of ED; it just adds the sweet new visual effects without any of the non-vanilla additions and changes. The "less lite" version additionally includes the Detect Trap and Detect Door effects from the full mod, and is the version I recommend.

The reason I recommend the less lite version over the lite version is because the two new effects are particularly useful combined with other mods on this list. As I said above, one of these other mods, Map and Compass, disables the local map, which will allow Detect Door to sometimes be genuinely useful. Also, Detect Trap is quite handy with another mod I recommend, Locks and Traps Detection, to provide a magical means of detecting a trap.

Note that the lite and less lite versions themselves require the full version (because the lite versions do not contain all the required assets like meshes and textures), so download and install the full version first (from the main Enhanced Detection link above). The "core" subpackage of the full version is required. The other sub-packages contain further modifications to the visual effects, and are optional.

Cast VFX is a pretty radical change to the visual effects upon casting the spells. I find these casting effects distracting, so I can't recommend them, but feel free to try them out.

Alternate VFX contains a more minimal set of VFX for the detect effects. Unfortunately, the "alternate" effects are all the same size and color, preventing them from being distinguished when the same object detects in more than one category (for example an NPC with a key and an enchanted item could have as many as three shown VFX with three detect effects active). So I can't recommend this sub-package either.

Nvidia VFX contains an older version of the visual effects, that was designed specifically for Nvidia graphics cards. If you don't have an Nvidia card, don't use it. If you do, then it's a matter of personal taste, though I personally don't like it as much as the "core" effects.

Anyway, the full version of ED requires Magicka Expanded. The lite version does not require ME, but the "less lite" version does. If you plan to use the less lite version (or the full version), install ME if you haven't already done so.

Once you've installed the full version of ED along with Magicka Expanded, go ahead and install the less lite version on top of it, which will overwrite the MWSE-lua files of the full version.

The less lite version includes an MCM in which each new effect (Detect Trap and Detect Door) can be disabled individually, though I don't recommend doing so. There's also a "BTBGI mode" option for compatibility with BTB's Game Improvements, which we'll be installing later. You might as well go ahead and enable this option.

## [Map and Compass](https://www.nexusmods.com/morrowind/mods/48455)

In Morrowind, there are two maps: the world map and the local map (there's also the minimap in the lower right, which is just your immediate surroundings in the local map), and both of them are cheap beyond measure.

The world map is unrealistic because it contains a cheap "YOU ARE HERE" marker which continually pinpoints your position in the world. Nevertheless, it still manages to be not very useful. You can see roughly where you are in relation to cities or major landmarks, but it's just not detailed enough to actually use it for navigation.

And the local map is outright broken. All characters, even the least magically inclined, have some sort of magical ability or extrasensory perception that allows them to divine not only exactly where they are in the current dungeon or town, but also where all the doors are, exactly where they lead, and the layout of the area at least in their immediate vicinity, including the presence of hidden side-passages and tunnels.

Map and Compass is the mod that will fix this brokenness. This MWSE mod does a number of neat things that greatly improve immersion:

1. It allows you to disable the vanilla world map and local map, which you should definitely do.

2. It allows you to replace them with one or more static maps which basically act as paper maps that your character brings with them to navigate by. There are two map packs in the mod; I recommend enabling all three of the maps in the Wagner pack and not bothering with the other pack.

    The "Wagner" maps are electronic versions of the drawn, stylized paper maps of Vvardenfell, Mournhold and Solstheim that Bethesda shipped with the CD versions of Morrowind. So you can, for example, pull up the Vvardenfell map and use it just like your character would to figure out where they are. It's detailed enough to be genuinely useful for navigation, while not containing that cheap player position marker, so you do have to actually use it realistically and remember where you are.

    You can enable any of the maps the mod comes with in the MCM, and you can switch back and forth between any of the maps you've enabled in the map menu. You can also create notes on the map just like you can on the vanilla map.

3. It allows you to disable the display of the current cell name at the top of the map menu, which I also highly recommend. This greatly increases immersion and allows you to become genuinely lost if you don't use your map and compass to keep track of your location. You can also hide the text that appears in the lower right corner when you move from one exterior cell to another.

4. Speaking of the compass, this mod includes an option to disable the display of the minimap in the lower right of the screen. Instead it will display a static compass background. Your player marker still spins to show which direction you're facing, so this can be used as a realistic compass (that doesn't also magically show you area layout and doors).

5. The map can be zoomed in and out with the mouse wheel. The max magnification is configurable in the MCM. With the Wagner maps, I like to set the max zoom level to 1x, since it doesn't really help to zoom them in beyond the default magnification. It's zooming *out* with them that's useful.

This mod renders the vanilla detect effects (Detect Animal, Detect Enchantment and Detect Key) less than useful, because those little circles are only displayed on the local map and minimap. But that's why we installed Enhanced Detection earlier.

Install this mod, and enjoy getting lost in the wilderness.

## [Map Replacements](https://www.nexusmods.com/morrowind/mods/48460)

This is a set of alternate versions of the Wagner maps for Map and Compass. They're the same maps, but with a more worn, weathered feel, looking more like something an adventurer might actually be carrying around with them.

There are two main options here: the "colored" maps or the "yellowed" maps. I suggest the yellowed maps for maximum realism and immersion, but use whichever you prefer. (Don't bother with the "lighter sea" map.)

Note that this is not a proper map pack for Map and Compass. Each of the subdirectories of the archive just contains the loose map files to replace the ones in the Wagner pack. To install these files with Wrye Mash (which you should do in case you decide to uninstall them later), you'll need to fix the directory structure of the archive so the map files are in MWSE\mods\Map and Compass\mapsWagner\\.

## Fortify MAX ([Nexus](https://www.nexusmods.com/morrowind/mods/49825), [Moddinghall](https://mw.moddinghall.com/file/152-fortify-max))

The Fortify Magicka and Fortify Fatigue effects are broken. They add a one-time use pool of magicka/fatigue to your current total, which will be gone after a few spellcasts or weapon swings, and everything you gained will be lost once the effect wears off, possibly resulting in collapsing on the ground in exhaustion. These effects are more useful for exploits than for their intended use - fortify your fatigue above max and you'll get better prices from merchants and be better at persuasion.

This mod fixes these effects by making them affect max as well as current magicka/fatigue. It basically does for these effects what MCP's "Fortify Maximum Health" feature does for Fortify Health.

These effects are now substantially more useful for their intended purpose - providing an extra pool of magicka/fatigue for normal use, which can be restored like normal (hopefully avoiding an untimely exhaustion). Constant effect enchantments with these effects are now actually useful. And certain broken (and potentially game-breaking) exploits are rendered impossible.

This mod breathes new life into these two effects. In vanilla Morrowind, these effects hardly ever saw any real use except for exploits. I'll bet that will change now.

## Class-Conscious Character Progression ([Nexus](https://www.nexusmods.com/morrowind/mods/48110), [Moddinghall](https://mw.moddinghall.com/file/134-class-conscious-character-progression-cccp))

As great of a game as Morrowind is, its leveling system sucks ass. Your attribute gains on levelup are determined by multipliers that are themselves determined by the number of skills you've increased since your last level that are governed by those attributes.

With the vanilla leveling system, there's a strong incentive to minmax, choosing major/minor skills you'll normally never use so you can control your levelups and carefully controlling skill gains to ensure you always get those coveted x5 multipliers, making developing your character an exercise in tedium rather than fun and rewarding.

CCCP changes that by radically transforming the leveling system. Skill gains now earn you attribute gains directly (and levelups from those), with each skill influencing multiple attributes to varying degrees. Both your race and your class have an influence on your starting attributes and how fast your attributes will increase.

Different characters (and in particular different classes) will now be a lot more diverse. You now have an incentive to make your character generation choices based on the type of character you'd like to play, and then you're allowed to have fun and play to your character's unique strengths rather than intricately planning each levelup.

Health and max magicka are also affected by your character's class and skills, and magicka will regenerate over time (albeit rather slowly for characters who aren't advanced spellcasters). With default settings, dedicated spellcasters will have much lower health than in vanilla, and be considerably more vulnerable, but this is compensated for by greatly increased max magicka and a decent rate of magicka regen, especially with a more developed character. Skill progression will also slow down over time once each skill reaches a specific threshold.

CCCP is basically an MWSE implementation of [Galsiah's Character Development](http://www.wolflore.net/download/file.php?id=1357), an earlier leveling mod. It implements most features of GCD in a simpler and more performance-friendly way than GCD itself, and it's highly customizable in the MCM.

The mod looks complicated, but don't let the large number of MCM options intimidate you. The default settings are reasonable (they're the same as GCD's defaults), and you can always tweak the settings once you gain some experience playing with the mod. The readme contains a more detailed summary of how CCCP works.

Note that, while this mod changes how max magicka is calculated, it is compatible with Fortify MAX.

With all that said, CCCP is a pretty radical overhaul of Morrowind's leveling system, and some players just won't prefer it. If you're one of them, there are a few mods I'd recommend using instead.

The first is MWSE State-Based Health ([Nexus](https://www.nexusmods.com/morrowind/mods/48133), [Moddinghall](https://mw.moddinghall.com/file/135-mwse-state-based-health)). CCCP implements its own health system; without it, you'll need another health mod to move away from the awful vanilla mechanic where you have to focus on endurance early or you'll permanently gimp yourself when it comes to health. MWSE State-Based Health basically uses the vanilla health formula, but health will change based on your current endurance and strength, so you don't have to raise endurance early to get "full" health.

I also recommend those averse to CCCP use another mod to address the leveling system in some way, if only to remove the vanilla system's incentive to minmax for perfect attribute multipliers. BTB's Game Improvements, further down on this list, makes all attribute multipliers x3. But if you don't plan on playing with BTBGI either, there's [Fixed Level Multipliers](https://www.nexusmods.com/morrowind/mods/45064), which has a x3 option (the x5 version is too overpowered).

Finally, CCCP basically incorporates a mod called [Inspirational Messages Expanded](https://www.nexusmods.com/morrowind/mods/49851), which includes vanilla-friendly levelup messages beyond level 20. If you don't use CCCP, you might want to download that mod and follow the instructions to add its messages to your Morrowind.ini so you'll see them on levelup.

## [Quest Skill Reward Fix](https://www.nexusmods.com/morrowind/mods/48269)

This fixes a relatively minor but frustrating issue involving skill progression and its affect on attribute and level progression.

Whenever you increase any of your skills by any of the "normal" means (through use, paid training or reading a skill book), this will trigger a skillup event (called `skillRaised` in MWSE-lua), which results in progress towards attribute and level progression. CCCP also detects this event and works its magic so that the skill increase contributes directly to attribute progress rather than level.

But scripted skill increases, such as those you receive as rewards for several quests (e.g. The Angry Trader, Widowmaker) don't trigger this event, which means in vanilla Morrowind they don't result in progress toward level or attributes. It also means that CCCP won't detect it, which means the skill increase will not contribute toward attribute gains under CCCP.

Quest Skill Reward Fix resolves this problem by detecting these scripted skill increases, incrementing level and attribute progress as appropriate and triggering the `skillRaised` event so CCCP can detect it. Now these increases will contribute towards attribute gains with CCCP just like any other skillups.

By default the mod only triggers the event for skill gains rewarded by the four vanilla quests that grant them. There's an option in the MCM to turn on "generic detection" so the mod will detect any scripted skill increase from dialogue and work its magic. This list doesn't include any mods that add such skill increases, so it doesn't really matter whether you enable this option, but there's no harm in it.

## [Magicka Based Skill Progression](https://www.nexusmods.com/morrowind/mods/48330)

MBSP addresses another unbalanced, exploitable vanilla mechanic that needs fixing. In vanilla Morrowind, whenever you cast a spell, you always gain a set amount of skill experience for that spell's magicka school, regardless of the amount of magicka the spell cost. This incentivizes casting custom-made spells that only cost 1 magicka over and over again to cheese up your magic skills. CCCP's magicka regen would only reinforce this incentive.

Magicka Based Skill Progression solves this problem by making the amount of skill experience you receive per spell cast depend on the magicka cost of the spell. The higher the magicka cost, the more skill progress you'll receive, while casting a 1-magicka spell will give you very little skill experience. Now you'll be incentivized to make progress in your magic skills through normal use rather than ridiculous cheese.

This works perfectly with CCCP's skill slowdown system too; the amount of experience gained (determined by magicka cost) will be affected by slowdown just like any other skill progress.

MBSP allows you to configure the amount of skill experience awarded per magicka point in the MCM. By default this value is 0.2, which gives the vanilla amount of skill progress for each 5 magicka expended. I think this is much too high, especially with CCCP's expanded magicka pool for mages, plus magicka regen. I personally set this value to 0.067, which will give the vanilla experience amount for each 15 magicka expended. If you find that results in too slow progress, you might try 0.1, which gives the vanilla experience amount for each 10 magicka expended.

I also suggest turning off logging in the MCM, to avoid cluttering up the console with the mod's messages.

## [Nimble Armor](https://www.nexusmods.com/morrowind/mods/48251)

The unarmored skill in vanilla Morrowind works basically just like any other armor skill: it reduces the damage you take upon being hit. The author of this mod thought that was stupid and set about fixing it, and this is the result.

Nimble Armor adds an evasion mechanic to Morrowind. Unarmored skill will no longer contribute to your armor rating. Instead it will contribute to your "evasion" rating, which allows you to evade attacks completely. When you evade an attack, you'll gain experience toward your unarmored skill (being hit no longer grants unarmored experience).

Armor contributes to your evasion rating as well, though often negatively, depending on the armor type and your skill in it. Light armor is the most evasive type, and you can gain light armor experience by evading attacks while wearing it, as well as by taking blows in it. You have to be highly skilled in medium armor to evade attacks in it (and you'll gain no skill experience when doing so), and you can't evade attacks in heavy armor at all (unless your heavy armor skill exceeds 100) with default settings.

Note that the stat that this mod calls "evasion" exists in vanilla Morrowind; in vanilla, it's basically just whatever magnitude of the Sanctuary magic effect you're affected by. Any Sanctuary magnitude you're under will combine with your armor-based evasion to determine the evasion stat you'll see in the menu.

The mod has an MCM that allows you to adjust a couple of its settings, but I don't recommend touching them. It's quite well-balanced as it is.

## [Expansion Delay](https://www.nexusmods.com/morrowind/mods/47588)

This mod was created by Half11, the main editor/compiler of Patch for Purists. In fact, the predecessor of this plugin used to be packaged along with PFP, but it was split off because it isn't exactly "purist."

Expansion Delay makes a number of improvements to the way Bethesda implemented the new content in the Tribunal and Bloodmoon expansions. Among other things, Dark Brotherhood assassins will no longer try to kill you as soon as you step off the boat in Seyda Neen, and you'll no longer hear rumors about Solstheim from nearly every NPC in the game. See the readme to learn more.

## Early Transport to Mournhold ([Nexus](https://www.nexusmods.com/morrowind/mods/47985), [Moddinghall](https://mw.moddinghall.com/file/132-early-transport-to-mournhold))

In vanilla Morrowind, you can't travel to Mournhold until you've been attacked by the Dark Brotherhood. Normally this wouldn't be a big deal, except that we're using Expansion Delay, which delays the DB attacks until we've made significant progress in the main quest. This means we can't set foot in Mournhold until pretty late in the game. This sucks.

Fortunately this mod is here to solve that problem by allowing us to travel to Mournhold early, before the DB attacks begin. You'll eventually hear a rumor about a means of transport to Mournhold which will lead you where you need to go.

You can't start the Tribunal main quest early this way (you still have to be attacked for that), but you can travel to Mournhold, explore, and complete Tribunal miscellaneous quests. A whole area of the game, once blocked off, is now available to you practically from the get-go.

## [Hospitality Papers Expanded](https://www.nexusmods.com/morrowind/mods/46107)

The original mod [Hospitality Papers](http://mw.modhistory.com/download-90-6206) enforces a gameplay mechanic that was hinted at in vanilla Morrowind but never actually implemented. In the vanilla game, you'll be told that you must purchase Hospitality Papers in order to receive services in Sadrith Mora, but this is never actually enforced. The mod causes service providers in the city to refuse service to you unless you have your papers in your inventory.

The "expanded" version linked above builds upon and expands the original in a few ways, including by adding new related dialogue so players will know where to buy the papers, increasing the price to buy them and further increasing the price if you need a replacement. Amazingly, the mod even includes new voice greetings recorded by original Morrowind voice actor Jeff Baker.

## Expansions Integrated ([Nexus](https://www.nexusmods.com/morrowind/mods/47861), [Moddinghall](https://mw.moddinghall.com/file/129-expansions-integrated))

In vanilla Morrowind, you can travel all over Vvardenfell and basically never know that Mournhold and Solstheim exist. You'll never find any items from the expansions anywhere in Vvardenfell, and the expansions' many new creatures are absolutely nowhere to be seen.

Expansions Integrated changes that by adding much of the content (items and creatures) from Tribunal and Bloodmoon to Vvardenfell. Much of this is done via leveled lists, but some items are also handplaced.

One copy of each adamantium armor piece and each adamantium weapon have been handplaced on Vvardenfell. This helps make up for the rarity of adamantium armor in particular; now you should be able to put together a complete set without resorting to murdering friendly NPCs. (Though if murdering friendly NPCs is totally your bag, baby, then I won't judge.)

Dark Brotherhood armor has been added to a few Brotherhood members on Vvardenfell. In addition, many Tribunal and Bloodmoon weapons and armor, clothing, ingredients and other items have been added to leveled lists, so you'll come across them throughout Vvardenfell.

Quite a few creatures from the expansions have also been added to leveled creature lists; you'll find them everywhere, depending on your level. A couple of them have been added at lower levels than when they can be found in the expansions themselves, so beware. (At least you won't have ten wolves swarming all over you like you will on Solstheim.)

Overall this isn't as huge of a difference as it sounds like. The biggest difference is the increase in difficulty because of the more powerful creatures, but you won't run into them all the time; they'll be mixed in with Morrowind's normal creatures.

But this mod brings us closer to having one integrated game world, rather than three completely separate realms that have very little in common. It's definitely an improvement.

The mod includes two alternate versions that omit some or all of the Bloodmoon integration, but I recommend the full version.

Alternatively, if you don't want to integrate most of the expansion content, there's Adamantium Armor Integrated ([Nexus](https://www.nexusmods.com/morrowind/mods/47731), [Moddinghall](https://mw.moddinghall.com/file/124-adamantium-armor-integrated)), which just places the adamantium armor on Vvardenfell without any of the other content.

## Creeping Blight - MWSE Version ([Nexus](https://www.nexusmods.com/morrowind/mods/47904), [Moddinghall](https://mw.moddinghall.com/file/130-creeping-blight))

Creeping Blight tweaks the weather chances for the game's various regions. In particular, it implements the possibility of blight outside of Red Mountain before the main quest is complete. The chance of blight increases as you make progress in the main quest, and it also increases with the passage of time until the main quest is complete.

This is actually not an extreme change; in most regions, with default settings, the chances of blight are pretty low even at their highest. But it's a concrete manifestation of the escalating threat from Dagoth Ur.

It also works well with Blighted Blight, a mod further down on this list, which reimplements the possibility of actually catching blight disease in blight storms.

Definitely get the MWSE version, not the plugin version. This version is more compatible, and also allows you to configure the base weather chances in all of the game's regions if you want, though I recommend sticking with the default settings. See the readme for a detailed explanation of the mod's changes.

## Dynamic Timescale ([Nexus](https://www.nexusmods.com/morrowind/mods/48287), [Moddinghall](https://mw.moddinghall.com/file/138-dynamic-timescale))

This MWSE mod makes the timescale (how quickly time passes in the game) vary depending on where you are and what you're doing. There are different timescales for dungeons, town interiors, town exteriors, other named exterior locations and wilderness areas. Traveling through the wilderness will now take an appropriately long amount of in-game time, since Vvardenfell is supposed to be a lot bigger than it's depicted, while time will slow down in towns and dungeons.

In addition, time will also slow down when you're in combat, sneaking, standing still, or take a number of other actions that require paying close attention.

Finally, there are two speedup modes that allow you to drastically speed up the passage of time as long as a configurable hotkey is pressed down, providing a more natural way to wait than using the vanilla wait menu. Press the hotkey to enter Fast Forward mode, and press control at the same time to enter Turbo mode.

Every aspect of the mod is configurable in the MCM. You can change each location-based and action-based timescale, disable the action-based timescales individually, and set other options related to them, such as how long time will remain slowed down after the action.

You can also set a multiplier to the timescale at night, and there's an option to adjust fast travel time proportionally with the wilderness timescale, so taking a boat from Ebonheart to Sadrith Mora will take as long as it should.

In general, I recommend leaving the mod's settings alone, but there are a couple you might want to change. I do suggest enabling the option to adjust the fast travel time. Also, you might want to lower the wilderness timescale.

By default, the timescale in the wilderness (when none of the other timescales apply) is 120, which is quite fast; if it's too fast for you, you might lower it to 60. 120 is more "realistic" given the distances that are supposed to be involved, but you might not like seeing the sun move across the sky so quickly.

While I quite enjoy this mod, if you don't like the timescale changing, there are alternatives. The first is a mod called Pass the Time ([Nexus](https://www.nexusmods.com/morrowind/mods/48217), [Moddinghall](https://mw.moddinghall.com/file/136-pass-the-time)), which allows you to set the normal timescale, implements Fast Forward / Turbo modes, and allows changing fast travel time, without the rest of Dynamic Timescale's features.

If you don't want to use Dynamic Timescale or Pass the Time, then I would suggest using the "Timescale6 Edit" version of Quick Char rather than the "Necro Edit" version. The Timescale6 version just sets the timescale to 6, so time will pass more slowly.

## [Lua Lockbashing](https://www.nexusmods.com/morrowind/mods/48544)

In order to open a locked container in vanilla Morrowind, you have basically three options: pick the lock (requires Security skill), use Open magic (requires Alteration skill, or buying/finding scrolls or enchanted items), or find a key (which many locked containers don't have). Obviously, stealth or magic oriented characters have a distinct advantage here, and pure fighters will often have to forego the contents of containers that a different skill set would allow them to open.

This mod changes that by adding a lock bashing mechanic to the game. The new mechanic is very simple: just swing your weapon at a locked door or container to attempt to bash the lock.

It's also quite well balanced. Lockpicking or magic will always be preferable if possible; lock bashing will wear out your weapon very quickly, and the cost of repair will be greater than the cost of new lockpicks. Weapon skill, strength and fatigue are taken into account. And you're much better off trying to bash locks with a two-handed battle axe than with a dagger. Also, bashing open an owned container or door is a crime just like picking the lock is.

There are several configurable settings in the MCM, and I suggest leaving most of them alone. The only one you might want to change is the top setting, which determines how the mod handles its one minor annoyance: refreshing the tooltip (that displays the lock level) when you bash a lock. There are three options, but basically only two for us, and neither is perfect.

The default setting is option 1, "pause menu flicker." With this option, the mod will very briefly open then close the game (escape) menu each time you bash a lock, so you'll see the game menu appear for a fraction of a second. This is necessary in order to immediately refresh the tooltip and update the lock level display.

If you don't like this, you can select option 0, "do it yourself." With this option, the game menu will not flicker, and the tooltip will not automatically refresh when you bash the lock, meaning you'll need to briefly look away from the door or container in order to update the lock level display.

There's also a third option (option 2) to force the immediate display of the exact lock level (the mod overrides the tooltip text), but this works poorly with Locks and Traps Detection, a mod we'll be installing later which generally hides the exact lock level and displays a possible range depending on your security skill. So don't select this option.

Keep in mind that, due to Locks and Traps Detection, you probably won't be able to see the exact lock level in the tooltip anyway, so I think option 0 is a reasonable choice. However, if you're not bothered by the game menu flickering, you might choose to keep the default setting (option 1). If you don't intend to use Locks and Traps Detection at all, select option 2.

In addition to the above, there's also an optional feature of the mod that will cause weapons and armor to be degraded, and other items to be destroyed outright, when you bash a container's lock open. This feature is disabled by default, and I leave it that way, but you can play around with it if permanently destroying loot sounds fun to you.

Overall, despite the minor tooltip issue above, this is a very worthwhile addition to Morrowind gameplay. I know I've hesitated to create purely combat-oriented characters in the past because of the problem of opening locked containers. This mod provides a balanced option for such characters.

## Hold Your Breath ([Nexus](https://www.nexusmods.com/morrowind/mods/48872), [Moddinghall](https://mw.moddinghall.com/file/82-hold-your-breath))

In vanilla Morrowind, you can hold your breath underwater for 20 seconds before you start taking drowning damage, and this length of time never changes. This MWSE mod makes the length of time you can hold your breath vary depending on your endurance.

Using the default settings, with an endurance of 0, you can hold your breath for 10 seconds. With an endurance of 50, the time is up to 20 seconds, as in vanilla, and with an endurance of 100, you can hold your breath for 30 seconds.

The base value (10 seconds) and endurance multiplier can be adjusted in the MCM if you feel the need, but I think the default values are reasonable.

## [Immersive Run Fix](https://www.nexusmods.com/morrowind/mods/45947)

Now we come to a series of five mods that affect movement speed. This one fixes a minor but bothersome inconsistency. In vanilla Morrowind, if you run forward and also strafe left or right at the same time, you'll move faster than you would if you were just running forward, because your full forward speed and left/right speeds are combined. This actually applies whenever you combine forward/back movement with left/right movement, whether running, walking, sneaking, swimming or flying. This mod just slows you down while moving diagonally, so you'll no longer get there faster than by just running straight ahead.

There's one issue to fix in the archive before installation. Unlike other MWSE mods, this mod's main.lua file is just dumped in MWSE\mods rather than being put in a subdirectory. This is confusing, and would conflict with any other mod that does the same thing (since the file path would be the same). So go ahead and put the file in its own subdirectory before installing - the file should be MWSE\mods\Immersive Run Fix\main.lua.

## [Wading in Water](https://www.nexusmods.com/morrowind/mods/48783)

This mod lowers your speed when running or walking in water that's not deep enough for you to actually be swimming. In vanilla Morrowind, you can wade into the water and maintain your normal running speed right up until the water gets deep enough for you to have to swim. With this mod, your speed while wading will gradually slow down as the water gets deeper, until eventually reaching your normal swimming speed (modified by any Swift Swim magnitude you're under) once you start swimming.

## [Realistic Movement Speeds](https://www.nexusmods.com/morrowind/mods/46248)

We still need to address movement speed while moving backward or strafing. Without this mod, your speed when moving backward is the same as when moving forward, and your strafing (sideways movement) speed is 75% of your forward speed.

With this mod, your backward and strafing speeds will be modified by a configurable multiplier. These multipliers by default are 60% for backward movement and 80% for strafing (80% of 75% is 60%, so your backward and strafing speeds will end up being the same with default settings). Your forward movement speed is not affected, though diagonal movement will be slower because you're strafing.

This is much more realistic. Now, if you start running backward while slinging spells or arrows at your opponents, expect them to be able to catch up with you. You can adjust the speed modifiers in the MCM, though I recommend leaving them as they are.

## [Reduced Forward Jump](https://www.nexusmods.com/morrowind/mods/45426)

Reduced Forward Jump is a tiny mod that's needed to address an issue that really bugs me.

You've probably noticed that jumping greatly boosts your forward speed; you can move forward much faster by jumping than by running. This encourages bunny hopping everywhere to get there faster.

This mod makes forward speed while jumping much more reasonable. In most circumstances, jumping forward speed should be pretty close to running forward speed. Not exactly - it depends on your acrobatics skill compared to your speed/athletics, while encumbrance and fatigue play a role as well - but it's much closer than before.

## [Wings of Will](https://www.nexusmods.com/morrowind/mods/46626)

This last of our movement speed mods addresses your speed while levitating. In vanilla Morrowind, your levitation speed is based on your speed attribute. This mod simply makes it based on your willpower attribute instead, while keeping the calculation otherwise identical. This makes a lot more sense, and provides a sorely-needed additional use for willpower.

There's one minor issue we can address by editing the code. When you're levitating underwater, you're still levitating, in addition to swimming, and this mod will still affect your speed. This means that if your willpower and speed are very different, you can greatly increase (or decrease) your swimming speed by casting levitate.

To address this, find the line that says:

```
if e.mobile.actorType ~= 0 then
```

and add the following immediately below it:

```
if e.mobile.isSwimming then return end
```

Now your "levitation" speed will be based on your speed attribute while swimming, and casting levitate should no longer make a big difference to your swim speed.

## [A Sinking Feeling](https://www.nexusmods.com/morrowind/mods/50113)

There's one more highly unrealistic movement mechanic to address: in vanilla Morrowind, you can equip full plate heavy armor and load up your pack with as much as you can carry, and then skillfully swim, wearing heavy armor and lugging all that stuff around, without sinking.

This mod implements a "pull down" mechanic, where gravity will pull you down beneath the waves. Of course you can resist this and try to keep yourself surfaced, but this becomes more difficult (and can easily become impossible) depending on various factors.

There are several modes you can choose from in the MCM, which use different means to determine how strong the pull is (and therefore how hard it is to keep yourself from being dragged under). The various modes are based on the weight class of your armor, the total weight of your equipment, or your total encumbrance.

I recommend setting the down-pull formula to "worst case scenario", which is basically a combination of all the other modes - whichever is worst is the one that applies. (All that stuff you're carrying around with you will drag you down whether you're wearing it or not, while wearing heavier armor will impede your mobility, which will make it harder to keep surfaced even if you're really strong.)

I also recommend leaving the "Worst or Best Case Scenario All Equipment variety" dropdown at "Necro Edit". This means that, when using the "worst case scenario" mode, the "all equipment" mode won't be considered, in favor of the "all equipment (Necro edit)" mode, which is a bit less punishing with very heavy equipment.

This mod adds a new consideration to Morrowind gameplay. You'll have to pay close attention to how much you're carrying and what you're wearing when you venture into the water, and might need to (gasp!) drop some of your heavy shit before going for a swim. It also gives you another reason to use those Feather effects - and Feather can be superior to Fortify Strength in this context. Or you can use Levitate effects, which let you fly underwater just as easily as on the surface.

You might want to enable the option in the MCM to affect only the player, as NPCs are exceedingly stupid and will happily drown themselves.

## [Alchemical Knowledge](https://www.nexusmods.com/morrowind/mods/49036)

This mod makes a number of improvements to the game's alchemy system in order to make alchemy more realistic and more convenient.

To start with, the alchemy menu (where you brew potions) is greatly improved. You can no longer see all common effects for any ingredient combination. Instead, you can see the effects of the most recent potion you created. This allows for genuine experimentation in potion creation, since you'll no longer be able to see what effects a combination will have if you don't already know them.

The alchemy menu now also includes an effect filter, which allows you to filter ingredients by effect, but only when you already know that effect for the ingredient in question. This makes creating potions with specific effects vastly more convenient, as long as you have enough alchemy knowledge to know the effects (if you don't, you'll need to experiment).

The mod also provides an additional way to learn ingredient effects beyond just increasing your alchemy skill. Once you create a potion with an effect, you now know that effect on each of the potion's ingredients that has it. You'll now be able to see that particular effect for those particular ingredients in the item tooltip, even if your alchemy skill would normally not be high enough to see that effect, and the alchemy menu's effect filter will remember that you know the effect, so the affected ingredients will show up when you filter by that effect in the future.

There are a couple of additional alchemy-related features as well. In particular, there are now "inedible" ingredients which you can no longer consume directly; these include ore samples, other metals and precious stones (this list is configurable in the MCM).

Overall, this mod represents a drastic improvement to Morrowind's alchemy system.

## [The Publicans](https://www.nexusmods.com/morrowind/mods/45410)

There are a number of places in vanilla Morrowind that for all the world look like inns, but for some reason don't actually function as inns - you can't actually rent a room there, even though it looks like you should be able to. For example, does anybody care to tell me why it is that you can't rent a room at "End of the World Renter Rooms" in Dagon Fel?

This mod enables the ability to rent a room in these places, via the "beds" topic like in any other inn. It doesn't go overboard adding new content or new gameplay mechanics; it blends in very well with the rest of the game, and really feels more like a bugfix than a gameplay mod.

This mod works very well with No Rest Without Beds, which we'll install later and which will give you a good reason to seek out a bed.

## [Great Service](https://www.nexusmods.com/morrowind/mods/47767)

Morrowind shipped with a great number of voice dialogue lines from service providers of different races and both sexes that were never actually heard in-game. This includes lines from pawnbrokers, alchemists, spell merchants and more, offering services, promoting their wares and so on. This mod simply enables these Bethesda dialogue lines to be heard in-game, providing much greater diversity of spoken dialogue, at least for service providers.

## [Religions Elaborated](https://www.nexusmods.com/morrowind/mods/47843)

Religions Elaborated improves upon a few game mechanics related to the Imperial Cult and Tribunal Temple factions.

First, it prevents you from being a member of both factions. It makes no sense that you can join two mutually opposed religious factions, do quests and rise in the ranks of both, especially given how hostile the Temple is to the Cult and everything else Imperial. Now if you're a member of one faction, the other will refuse to admit you.

Second, it adds Almsivi Intervention markers to the temples that were missing them (Suran, Maar Gan, Vos and Ghostgate). Now you can use AI to teleport to these locations.

Additionally, healers in the temples will now actually provide healing services for a fee, rather than just standing there uselessly and maybe selling potions. Cult and Temple locations also now have supply chests for members of these factions, like the Fighters and Mages Guildhalls do.

Finally, the mod makes a few changes regarding a few Temple and Cult quests. The biggest change here is that the Cult quests are no longer all based out of Ebonheart. Two of the quest types now have different quest givers in different locations. There are also a few minor tweaks and additional options for some quests, but no additional major changes.

There are two versions of the mod available for download. The "no quest changes" version omits the changes described in the above paragraph (decentralizing the Cult quests out of Ebonheart and the additional tweaks), but still implements the other changes. I recommend the regular version, but use the alternate version if you want.

## [Improved Temple Experience](https://www.nexusmods.com/morrowind/mods/49373)

The main reason we're installing this mod is because it adds actual Temple shrines to a number of Temple locations that were missing them. Now you won't be disappointed when you take refuge in the Suran Temple hoping to cure your blight disease, only to find there's no shrine.

The mod also adds the same missing temple markers that Religions Elaborated does, and I recommend tweaking the plugin to remove them. It's not strictly speaking necessary - if you don't, there will just be two temple markers at those locations, which doesn't really hurt anything - but I'm not a fan of unnecessary edits. (Of course, if you're not using Religions Elaborated, you won't want to do this.)

To remove those markers from the plugin, open it up in Enchanted Editor and delete the references to the four *exterior* cells. Don't delete the interior cell edits, as those contain the added shrines.

## [Divayth Fyr Puzzle Fixed](https://www.nexusmods.com/morrowind/mods/45155)

Tel Fyr includes a nifty little puzzle. There are a number of chests scattered throughout the four zones of Tel Fyr (including the Corprusarium) with keys in them. Each key unlocks the next chest in the sequence, and there are a number of powerful artifacts inside locked containers.

This is all well and good, but the problem is that the aforementioned powerful artifacts can all be acquired without even bothering with the key-finding puzzle; just unlock the relevant chests with picks or spells (or bash them open with Lua Lockbashing). This mod makes all the chests involved in the puzzle well and truly locked until you find the required key to open them, preventing you from completely bypassing the puzzle and giving you a strong incentive to run around tracking down all those keys.

## Consistent Enchanting ([Nexus](https://www.nexusmods.com/morrowind/mods/50029), [Github](https://github.com/NullCascade/morrowind-mods))

When you enchant a weapon or a piece of armor, the item's condition is not carried over to the enchanted version. In other words, if the item you're enchanting is damaged, enchanting it will repair it to full. This mod fixes that; enchanted items will retain the condition of their base items.

This mod also carries over any script that was attached to the base item, and any data that was attached to them by other MWSE-lua mods, though that's unlikely to be important when using this list. There's an MCM where you can disable carrying over certain things, but there's no need to mess with it.

This is another mod with a (usually) more up-to-date version on NullCascade's Github, so I suggest grabbing it from there.

## [Randomized Chargen](https://www.nexusmods.com/morrowind/mods/46915)

Randomized Chargen is an MWSE mod that allows you to randomly roll the following characteristics when you create your character: race, sex, face, hair, (non-custom) class, and birthsign. This, combined with the Name Generator mod above, allows you to almost completely randomize your character. It's also fully compatible with Quick Char.

Randomization is also optional, so you can still manually select any or all of your characteristics like normal. The only shortcoming is that it doesn't allow you to randomize a custom class; if you want a custom class, you'll have to manually select its characteristics.

# Game Balance and Difficulty

This is the most important group of mods we'll be installing with this list in terms of game balance. The mods in this section rebalance certain portions of the game, prevent you from exploiting flawed game mechanics, increase the difficulty of aspects of the game in realistic ways, or make various options (such as development paths for your character, or equipment categories) genuinely useful where in vanilla some are overpowered and others are useless.

The mods in this category, taken together, transform the game from a way too easy one filled with highly exploitable mechanics into one where you have to really think about the decisions you make, where every choice matters and every option is generally useful in some way.

## Economy Adjuster Adjustments ([Nexus](https://www.nexusmods.com/morrowind/mods/47130), [Moddinghall](https://mw.moddinghall.com/file/118-economy-adjuster-adjustments))

Here we come to the first of the major game balance overhauls on this list. The economy in vanilla Morrowind is, as HotFusion says in his readme, "out of control." It's way too easy to make enormous sums of money, and there's really nothing worth spending all that money on (as loot quickly becomes far more useful than store-bought equipment).

Economy Adjuster is a collection of five modules that together aim to reform Morrowind's economy, making it more difficult to earn large sums of money and preventing you from exploiting broken game mechanics (such as taking advantage of Morrowind's hapless merchants for unlimited gold).

The original Economy Adjuster includes the following modules: Merchant Skills, Crime, Ingredients, Daedric Drops, and Misc. Of these five, only the Crime module is of interest to us. (As to why we won't be using the Merchant Skills module, see below.) See HotFusion's readmes for details about the other modules, though many of the changes made by those modules are incorporated into BTB's Game Improvements further down on this list.

The links above are for EcoAdj Adjustments, which contains versions of the Merchant Skills and Crime modules, based on BTB's edited versions, with a few additional improvements. See below for a brief description of the Crime module, and see the EcoAdj Adjustments readme for a more thorough explanation of these changes.

The Crime module addresses an important balance issue in vanilla Morrowind: crime is ridiculously under-punished. You'd generally get a slap on the wrist for the most serious crimes, including murder, and crime is generally way too profitable even if you get caught. For example, you can murder a merchant in plain view of a guard, pay the small fine, then take all the merchant's stuff and sell it for a handsome profit.

This module changes all that, primarily by significantly increasing the bounty you'll earn for various crimes to the point where crime generally doesn't pay (unless you don't get caught, of course). HotFusion's original version of the plugin missed the bounty for "trespassing" (unlocking an owned container or door), so BTB's edited version increases the bounty for this crime consistent with those of other crimes.

The EcoAdj Adjustments version of the module addresses a few issues in the original and BTB versions. First, it raises the penalty for theft (which was missed by both prior versions). Second, it adjusts the death sentence threshold (the point where guards will simply attack you instead of trying to arrest you) to be a bit less harsh than in the earlier versions. And third, it adjusts the amount of time you must spend in jail if you can't pay, so that it's still a real deterrent against serious crimes like murder, without being so debilitating as to be unacceptable to any player. See the EcoAdj Adjustments readme for more thorough explanations.

So, why aren't we using the Merchant Skills module?

Merchant Skills addresses another important balance issue in vanilla Morrowind: it is easy (and I mean *really* easy) to exploit the game's merchants and walk away with huge amounts of cash, and this can be done right from the beginning of the game. The Merchant Skills module addresses this brokenness by raising the absurdly low mercantile and speechcraft skills of merchants, so that a player with even a moderate mercantile skill can no longer completely take advantage of them.

This is all well and good, but the next mod on this list fixes this imbalance in a much more comprehensive way via MWSE-lua. In fact, it makes exploiting the game's merchants practically impossible, unlike EcoAdj's Merchant Skills module, and makes them drive much tougher bargains.

So in short, just download the EcoAdj Adjustments version of Economy Adjuster, and use only the Crime module.

## [HardTrade](https://www.nexusmods.com/morrowind/mods/47368)

As we discussed under Economy Adjuster above, exploiting Morrowind's merchants to rake in unlimited amounts of cash is absurdly easy, even for players with a modest mercantile skill. Just buy a 300-gold item for 250, sell it right back for 350, and repeat, with higher mercantile skill and disposition allowing you to clean merchants' barter gold out faster. HardTrade will definitely put a complete stop to all that nonsense.

It does this using an MWSE-lua script that determines the buy and sell price of an item using a formula that takes into account the item's base value; the player's mercantile, speechcraft, personality and luck; the merchant's values for the same skills and attributes; the merchant's disposition towards the player; and the player's rank in the merchant's faction. The player's and merchant's mercantile skill, the merchant's disposition and the player's faction rank are the most important factors.

The buy price (before haggling) will never be less than 1.5 times the base value of the item, and the pre-haggle sell price will never be more than two-thirds the base value, even with player stats above 100 and max disposition, and with low stats prices will be much worse. This makes exploiting merchants for free cash practically impossible.

To see how this works in practice, here are the pre-haggle buy price and sell price of a 100-gold bottle of Flin, with Arrille, with varying player stats and disposition:

Merc | Spch | Pers | Luck | Disp | Buy | Sell
-- | -- | -- | -- | -- | -- | --
5 | 5 | 40 | 40 | 40 | **271** | **37**
30 | 30 | 50 | 50 | 80 | **234** | **43**
70 | 70 | 70 | 70 | 80 | **207** | **48**
90 | 90 | 90 | 90 | 90 | **187** | **53**
100 | 100 | 100 | 100 | 100 | **175** | **57**
134 | 134 | 134 | 134 | 100 | **150** | **67**

That 150/67 buy/sell price is the best pre-haggle price for a 100-gold item you'll ever see with HardTrade.

In theory, it would be possible to use HardTrade alongside the Merchant Skills module of Economy Adjuster, but this would be overkill; it would make trading *too* difficult and prices too unfavorable. HardTrade was clearly designed with the vanilla merchant stats in mind. Trust me, it's hardcore enough by itself.

HardTrade also affects the prices of other services, such as spells and fast travel, though the effect is less severe.

There are two issues with HardTrade that need to be addressed. First, by default the mod caps your effective attributes and skills (e.g. personality, mercantile) at 100 when trading. I think this is unnecessary, as the coefficient that determines the change to buy/sell price can't go below 1.5 anyway (thus the floor of 150-gold buy price for a 100-gold item). This limiting feature can be disabled in the Mod Config Menu.

Second, and more importantly, HardTrade also does a couple other unnecessary things that can't be disabled in the MCM, so we'll need to edit the mod's .lua file and comment out a few lines. (To comment out a line, put two hyphens at the beginning of the line, so it changes from `<code>` to `--<code>`.)

In addition to the core price formula, HardTrade also changes six of the game's GMSTs related to haggling and bribing to make both more difficult (it makes these changes via the lua script rather than with a plugin). This might sound like a good change, but we don't need it; HardTrade makes getting a good deal from a merchant extraordinarily difficult even without these GMST changes. Also, implementing these changes via the lua script will override any plugin that also changes any of these values, and one of the mods on this list does.

To disable these GMST changes, open up the file MWSE\mods\HardTrade\main.lua in a text editor and comment out the lines toward the end of the file that begin with `tes3.findGMST`.

HardTrade also implements a shop investment feature that I don't care for. By bribing merchants 1000 gold, you can permanently increase their amount of barter gold (depending on your mercantile skill). If you agree with me that this feature is unnecessary bloat, you can disable it by commenting out the line that begins `event.register("uiActivated", onPersuationMenu` toward the bottom of the main.lua file.

## Ownership Overhaul ([Nexus](https://www.nexusmods.com/morrowind/mods/48051), [Moddinghall](https://mw.moddinghall.com/file/133-ownership-overhaul))

Item ownership in Morrowind is a complete mess. Buttloads of stuff that should be owned isn't, meaning it's free for the taking. This includes lots and lots of containers in many cities and towns, many of which have gold, ingredients, and even weapons and other items which you can nab for free fresh off the boat. It also includes piles of lanterns and torches, keys and gold, and gobs of other stuff. And as soon as you join a faction you can clear out its guildhalls of all that faction owned stuff.

This mod puts a stop to that by making all that stuff that should be owned actually owned. Now you'll have to go dungeon delving for your loot instead of clearing out half of Balmora for free. Of course, you can always steal stuff, but you'll no longer be up to your ass in freebies within 100 feet of fast travel locations. This is a real balance and difficulty improvement.

There's an .esm version and an .esp version of the mod, and you should only use one. The .esm version is safer from a compatibility standpoint (to ensure that other mods that touch the affected objects take priority), so just use the .esm. It should load immediately after Patch for Purists.esm, before your other .esms.

## BTB's Game Improvements - Necro Edit ([Nexus](https://www.nexusmods.com/morrowind/mods/47129), [Moddinghall](https://mw.moddinghall.com/file/117-btbs-game-improvements-necro-edit))

BTB's Game Improvements is really the core mod of this list, as it makes the bulk of the game balance changes that transform Morrowind into a more rewarding and demanding experience.

Many of BTBGI's changes revolve around making once-useless options genuinely useful, so that players will actually choose them once in a while, or nerfing previously overpowered and godlike items and abilities. Many exploits are removed and cheap tactics rendered impossible or irrelevant. The game is made more rewarding by forcing you to make real decisions about things like how to develop your character, what skills to develop, what equipment to use, and having those decisions actually matter throughout the game.

The version of the mod linked above is my personal edit of BTBGI, with most of BTBGI's modules combined into one plugin, BTB's edits to Morrowind Advanced and Service Requirements included, plus a number of changes and additions.

Below is a brief summary of the changes made by BTBGI. See the documentation for a more in-depth discussion. I suggest reading BTB's original readme in addition to the readme for the Necro Edit version. (BTB's readme is quite lengthy, but well worth reading. Indeed, it's one of the more important readmes on which to follow my earlier advice about reading the readmes, so you'll have an understanding of the many changes BTBGI makes to the game.)

The summary below is separated by module, even though the modules are mostly no longer separate plugins.

### Character

BTB describes this as the "flagship module" of BTBGI (which would make it the core of the core of this list, as it were, even though I actually use a different mod that's based on it, for which see below).

Primarily this module implements a very thorough and exacting rebalance of all the game's birthsigns and races. Previously useless (or even worse than useless) options have been given new life so they can compete with the others. A few overpowered options have been toned down a bit. Attribute bonuses for birthsigns have been expanded and rebalanced, and skill boosts for races have been rebalanced as well. See BTB's readme for more details.

### Spells

This module thoroughly rebalances the game's spells. The pre-made spells are made generally more useful, and cheaper than custom-built spells to encourage their use. Additional useful spells for the player are added to spell merchants. NPCs now have more dangerous spells that they can use against you (depending on their magicka and magic skills). The starting spells have been rebalanced so new players get two useful beginner spells per magic skill on their major list.

In addition, a number of spell effect costs have been tweaked to balance their usefulness, both as spells and as potions. And some spell effects have been outright disabled for spellmaking and enchanting, mostly to eliminate several of the game's more broken exploits. BTB's readme lists all these effects with an explanation of the reason for the change, in addition to going into great detail about the other changes made by this module.

### Alchemy

The Alchemy module reworks several aspects of the alchemy system. Ingredients have their values balanced to reflect their rarity or the difficulty in acquiring them. The distribution of effects among the various ingredients has been completely overhauled - you'll particularly notice that negative effects in self-made potions are now much more common, as well as more relevant to what you're trying to do.

Several spell effects have been removed from alchemy entirely, again in significant part to eliminate exploits. And the pre-made potions and alchemy apparatus have been rebalanced as well in various ways. See the readme for lengthy explanations.

### Equipment

This module gives the same exactingly thorough treatment to the game's equipment as the previous ones do for spells and potions. The values of high-end equipment have been greatly reduced, to prevent you from becoming richer than Scrooge McDuck after selling a few pieces. Armor ratings have been rebalanced, both between and across armor classes (light armor is no longer the overwhelming top choice), and the durability of glass equipment has been nerfed.

On the other hand, the mountains of shitty, useless equipment the game was previously overflowing with have generally been diversified and made more useful. There's now more of a progression from low-end to better and better equipment throughout the game. Also, you can no longer sell your shit to Creeper and the Talking Mudcrab, forcing you to deal with regular merchants (who, with HardTrade, become merciless traders). Like with the other modules, BTB's readme goes into much more detail about these changes.

### Settings

This is the catch-all, miscellaneous module of the bunch, making various tweaks and adjustments that didn't fit in elsewhere. These changes include (but are definitely not limited to):

- A number of game settings have been tweaked for better balance or to enhance game difficulty.

- Skill progression rates for specific skills have been adjusted, with the aim of encouraging training skills through normal use rather than through grinding.

- Enchanted items will no longer regain charges over time; it is now necessary to use soulgems to recharge items.

- Restocking supplies of empty soulgems and Soul Trap scrolls have been added to a few merchants.

- It is no longer possible to enchant items on your own; you must pay an enchanter for this service.

- Enchanting a scroll (with the cast once enchantment type) is now vastly cheaper than other enchantments, and paper has a higher enchant value. This makes creating scrolls a viable option.

- No more creating custom constant effect enchantments, to prevent abuse of the cheap effects.

- The amount of time until a merchant's gold resets has been reduced from 24 hours to one hour, to minimize how long you need to stand in front of a merchant and wait in order to sell all your shit.

- The distance at which NPCs will play their voice greetings has been substantially reduced, minimizing the desire to murder NPCs just to shut them up.

- A few new guards have been added at appropriate locations, to make it more difficult to steal valuable items.

In addition to the above, one of the changes BTB makes in this module is to the skill progression rates of major, minor and miscellaneous skills. In particular, misc skills now have zero skill progression rate, meaning they will no longer increase naturally at all (outside of training, skill books and quest rewards).

BTB's readme goes into great detail about why this is a good thing. I agree with BTB on this one. This change forces you to play to your character type, and prevents you from creating a generalist character who's highly skilled at everything (or at least makes it much more difficult to do so). It also ensures that major and minor skills will be chosen on the basis of how you intend to play the game, rather than on the basis of how easy it is to cheese three 5x attribute multipliers (CCCP also greatly helps with this).

### Diseases and Daedric Drops

BTB's edits related to diseases and daedric drops from his [modified version](https://web.archive.org/web/20150423044046/http://btb2.free.fr/files/morrowind_advanced.zip) of [Morrowind Advanced](https://www.nexusmods.com/morrowind/mods/30205) have been incorporated into this version of BTBGI. Diseases have been rebalanced, with mild diseases being somewhat worse and the acute diseases being not quite so severe, so they won't be worse than blight diseases. Disease-related dialogue has also been updated to reflect these changes.

Certain creatures (here's looking at you, Golden Saints and Dremora) will no longer drop daedric equipment, so you'll no longer be up to your eyeballs in the stuff. Daedric equipment is supposed to be rare! Instead, these creatures now have constant effect bound item abilities, so they can use high-end weapons against you, but you can't take those weapons after you kill them.

### Factions

BTB's faction-related edits from his [modified version](https://web.archive.org/web/20150421154605/http://btb2.free.fr/files/morrowind_service.zip) of Service Requirements have also been included. Attribute and skill requirements (especially attribute requirements) for promotion in factions have been significantly increased. You're not going to advance to the pinnacle of any of the game's factions without significantly developing your character.

The favored attributes and skills for many factions have also been tweaked for better balance between the factions and among attributes and skills.

-----

The archive contains two sub-packages: "Core" and "Rational Names Addendum". Install the core sub-package, and, if you're using Rational Names, also install the related sub-package (otherwise the names that Rational Names assigns to certain potions would no longer be accurate with BTBGI).

The core sub-package contains the main plugin, and a Races and Birthsigns addon with the race- and birthsign-related edits from the Character module. If you intend to use Balanced Passive Races and Birthsigns (see below), then skip the Races and Birthsigns add-on; otherwise, install the add-on as well.

The "PFP Patch" plugin addresses an issue with Patch for Purists, and should definitely also be enabled.

There's also a "Creature Buffs" plugin, which buffs many vanilla creatures in line with changes made by Morrowind Advanced. This add-on makes creatures tougher, stronger and faster, gives them more health and fatigue, and makes them hit harder. I personally don't use it, because I think the creature buffs are a bit much with BTBGI, but if you want to use it, use it alongside (and have it load after) the main BTBGI plugin.

-----

I highly recommend BTBGI if you want a balanced game. However, there will always be players who don't want to play such a massive overhaul, or who object to some of BTBGI's changes. If you don't want to install BTBGI for whatever reason, there are a number of other mods you might want to consider.

- [Fixed Level Multipliers](https://www.nexusmods.com/morrowind/mods/45064) (if also not using CCCP)

BTBGI incorporates the x3 version of this mod, which makes all attribute multipliers on levelup x3 (in order to remove the vanilla leveling system's incentive to minmax and allow players to develop their characters naturally). With CCCP this doesn't matter, because CCCP radically overhauls the leveling system. But if you're not using CCCP either, I recommend Fixed Level Multipliers. (Make sure you use the x3 version; the x5 version is too overpowered.)

- Magas Volar Anti-Cheat ([Nexus](https://www.nexusmods.com/morrowind/mods/47714), [Moddinghall](https://mw.moddinghall.com/file/123-magas-volar-anti-cheat)) (if also not using There Can Be Only One)

This mod just removes the script from the daedric lord of Magas Volar that in vanilla automatically teleports you after you kill him. This way you have to loot the Daedric Crescent from his corpse, and are prevented from using Mark/Recall to get a duplicate Crescent.

BTBGI incorporates this mod, as does There Can Be Only One, further down on this list. You only need this mod if you'll be using neither BTBGI nor TCBOO.

- [Merchant Gold Reset](https://www.nexusmods.com/morrowind/mods/43764)

BTBGI incorporates the one-hour version of this mod, which causes merchants' gold to reset after one hour instead of having to wait 24 hours. It's a small convenience mod to minimize use of the wait key.

- [Reduced Commentary](http://mw.modhistory.com/download-90-12831)

This mod causes NPCs to greet you with their spoken hello lines less frequently, in order to minimize the desire to murder them just to shut them up. BTBGI makes a similar change.

- [Tooltips Complete](https://www.nexusmods.com/morrowind/mods/46842)

Implements lore-friendly descriptive tooltips for pretty much every item in the game. The only reason this mod isn't on this list is because BTBGI changes a number of items such that Tooltips Complete's description would no longer be accurate.

- Potion Renamer ([Nexus](https://www.nexusmods.com/morrowind/mods/49853), [Moddinghall](https://mw.moddinghall.com/file/154-potion-renamer)) (if also not using Rational Names)

Earlier on this list I recommend Rational Names, which, among other things, renames many items for improved inventory sorting. I also list a number of smaller alternatives in case you don't want to use Rational Names, among them Potion Renamer, which just renames potions using BTBGI's naming scheme so they'll sort in a way that makes sense.

However, Potion Renamer conflicts with BTBGI, because it assumes the potions have vanilla effects (BTBGI changes the effects of many potions). Rational Names doesn't have this problem, because BTBGI includes an MWSE addendum for Rational Names. If you're not using BTBGI or Rational Names, then it's safe to use Potion Renamer instead.

## Balanced Passive Races and Birthsigns ([Nexus](https://www.nexusmods.com/morrowind/mods/47782), [Moddinghall](https://mw.moddinghall.com/file/127-balanced-passive-races-and-birthsigns))

This mod is a modified version of the race- and birthsign-related edits from BTBGI, described above. It makes two significant changes from BTBGI:

- All once-a-day powers have been removed from races and birthsigns. Instead, new permanent (constant effect) abilities have been added, or new effects added to existing abilities, to make races and birthsigns more unique and useful.

- Racial skill bonuses have been tweaked as needed to ensure that no race has more than one weapon skill (not including marksman or hand-to-hand) or more than one armor skill (not including unarmored). Races, at least those that have weapon or armor skill bonuses at all, now specialize in one primary weapon type and one primary armor type, which makes them more unique and avoids skill bonuses going to waste when you end up only using one primary weapon and armor type anyway.

The readme includes detailed comparisons between vanilla, BTBGI and this mod, and discussions of many of the changes made. You should read it, and then install this mod if you like what you read (if you don't, then use BTBGI's Races and Birthsigns addon in addition to the main BTBGI plugin).

## [Morrowind Anti-Cheese](https://www.nexusmods.com/morrowind/mods/50308)

This mod makes a number of changes to the game in order to prevent exploits or make it more difficult to get really nice stuff. It makes some enemies guarding aforementioned nice stuff tougher, plus adds some new guards and other enemies, replaces some of that nice stuff with less nice stuff, and makes a few other changes. See the readme for a complete list.

The link above is actually to "BTBGI Necro Edit Tweaked and Patches", which is a modified version of BTBGI Necro Edit, plus a number of patches. The archive contains a number of sub-packages, but we only need Anti-Cheese. (The Enhanced Detection patch is for the full version of ED; it's not needed with the Less Lite version.)

This version of Morrowind Anti-Cheese has been modified from [the original](https://www.nexusmods.com/morrowind/mods/47305) for compatibility with BTBGI, and should come immediately after BTBGI and its patches in your load order. (If you're not using BTBGI for some reason, then you should use a [different alternate version](https://www.nexusmods.com/morrowind/mods/49232) of Anti-Cheese instead.)

There is one more consideration with Anti-Cheese. One of the mods further down on this list is More Deadly Morrowind Denizens, which, among other things, modifies a bunch of NPCs to make them tougher. Anti-Cheese edits some of the same NPCs, and since this version of Anti-Cheese needs to come after BTBGI in the load order, while MDMD should load before BTBGI, Anti-Cheese will override MDMD's better edits to those NPCs.

Therefore, if you plan to use MDMD, you'll need to remove the offending NPC edits from the Anti-Cheese plugin. To do this, open up Anti-Cheese with Enchanted Editor, and delete the following NPC records:

- Draramu Hloran
- Dreveni Hlaren
- Elante
- Furius Acilius
- Galmis Dren
- Koffutto Gilgar
- Raxle Berne
- Sorkvild the Raven
- Vindamea Drethan
- Volrina Quarra

## [Better Character Classes](https://www.nexusmods.com/morrowind/mods/47078)

One thing BTBGI doesnt touch is the vanilla pre-made character classes, and they're a complete mess. Classes specializing in multiple armor types or multiple weapon types (or both) are extremely common. No matter which class you select, you're almost certain to end up with multiple major and minor skills that you'll never use, making it difficult to play to your character type. The pre-made classes are so unbalanced and by-and-large useless that anybody in their right mind is just going to create a custom class.

This mod provides a balancing touch to the pre-made classes, and it's an excellent companion to BTBGI (and CCCP). Multiple armor and weapon types for a single class have been minimized (though not completely eliminated), skill distribution among the classes is more balanced, and a few other tweaks have been made. The result is a list of default classes that a sane player might actually choose, which makes picking a default class (or taking the personality quiz) a viable option.

Of course, many players are likely to still create custom classes in order to be able to exercise maximum control over all aspects of their characters, but it's nice to have a list of more or less reasonable default options to choose from as well.

Normally, using this mod would have an unfortunate side effect: it would cause some NPCs who are supposed to be wearing armor to wear their birthday suits instead, because their armor skills have changed and the game correctly determines they're now better off without armor. BTBGI would exacerbate this problem, because it increases the effectiveness of the unarmored skill. But Nimble Armor, which we installed above, causes unarmored skill to not contribute to armor rating at all (it contributes to the evasion stat instead), which means this won't be a problem for us.

## [No Rest Without Beds](https://www.nexusmods.com/morrowind/mods/46724)

Does what it says on the tin: requires you to find a bed in order to rest. It does so in a very clean, straightforward way with an MWSE-lua script, without requiring a plugin or any cell edits. (In other words it does what BTB was aiming to do in the Settings module of BTBGI, but in a much better way than BTB was able to do with a conventional plugin, which is why the Necro Edit version of BTBGI omits all those cell edits.)

The default rule with this mod is very straightforward - you can only rest in a bed, and pressing the wait key only allows you to wait, never rest. There are a couple of optional tweaks that you can make in the Mod Config Menu though, one to disallow resting in exterior areas (even with a bed), and one to allow resting without a bed in interior cells where the game considers resting to be legal (such as caves and other dungeons).

Changing that second setting would bring the mod more in line with what BTB intended with his anti-camping edits in BTBGI, but I suggest just sticking with the default settings. You're not going to lie down on the cold, hard ground in a haunted tomb to catch some shut-eye. Find a bed.

## [No Beds for the Diseased](https://www.nexusmods.com/morrowind/mods/49232)

The mod we just installed prevents you from resting unless you find a bed. This mod prevents you from renting a bed from a publican if you have a disease. The two mods together provide a stronger incentive to get your diseases cured.

With this mod, you'll feel a bit more like an outcast from society as long as you're diseased, which I think is a good thing. The consequences of not getting yourself cured are worsened, making disease a bit more of a big deal.

The above link is to "Sigourn's Misc Mods and Patches", which is mostly a collection of patches for various mods, including several on this list. For right now we only need No Beds for the Diseased, but there are a number of other files we'll need soon from the download page, so you might as well go ahead and pick them up now:

- Ownership Overhaul Patches
- MDMD - More Deadly Morrowind Denizens Patches
- Controlled Consumption (MMC Edit)

## [No Disease Labels](https://www.nexusmods.com/morrowind/mods/48295)

A very small MWSE mod that just changes the names of certain creatures to remove any indication that the creature is diseased. So "Diseased Rat" is now just labeled "Rat", and "Blighted Cliff Racer" is just a "Cliff Racer". They're still diseased; it just won't be immediately obvious anymore. This eliminates the advantage of knowing what you're getting into ahead of time.

## [Enchanted Weapon Resistance](https://www.nexusmods.com/morrowind/mods/50194)

Some creatures resist "normal" weapons. Try swinging an Iron Shortsword at an Ancestor Ghost and see how far that gets you.

There's a flag for weapons in the Construction Set called "ignore normal weapons resistance"; if this flag is set, the weapon will damage such resistant creatures normally. Weapons made of higher-quality materials (silver or better) generally have this flag set, while weapons made of lower-quality materials (like iron or steel) generally have it unset.

In vanilla Morrowind, there's a bug that causes any enchanted weapon to automatically ignore normal weapon resistance, regardless of the ignores resist flag. The "weapon resistance change" feature of MCP fixes this bug so that even enchanted weapons will respect the state of this flag.

However, in vanilla Morrowind, almost all enchanted weapons have this flag set, even the low-end ones like an Iron Sparksword. This means that such shit-tier enchanted weapons will still damage ghosts and the like.

This mod addresses this issue by setting the ignore resist flag for enchanted weapons the same as that of the "normal", unenchanted version of the weapon. So, silver or better enchanted weapons will damage fully resistant enemies, while the lower-end stuff will not. This applies to ammunition items (arrows and bolts) as well.

The mod also has an additional feature. Normally, when you attack an enemy that's immune to normal weapons with a cast-on-strike enchanted weapon without the flag set, the enchantment will be effective, even though the weapon swing itself will not be. However, this mod by default renders the enchantment also ineffective if the enemy fully resists the weapon it's attached to. This feature can be disabled in the MCM if you prefer, but I like it.

## [Service Requirements Lore](https://www.nexusmods.com/morrowind/mods/45567) ([Sigourn Edit](https://cdn.discordapp.com/attachments/218457935846703104/796555612372467712/Service_Requirements_Lore_v1.4_Sigourn_Edit.zip))

The primary purpose of Service Requirements is to implement faction rank requirements in order to obtain services from members of a faction. In general, you will now have to be the same rank as the service provider in their faction to obtain services from them; otherwise they will refuse to provide services. There are a few exceptions where it makes sense.

This mod has a significant effect on difficulty. It can make it much harder to find NPCs who will provide you essential services, and it does a lot to change the atmosphere of the game to make you feel like more of an outsider. It also gives you a strong incentive to join and try to advance in at least one or two factions, so you're not left out in the cold when it comes to services.

Definitely grab the "Sigourn Edit" version linked above, which fixes a few bugs and inconsistencies in the version on the Nexus.

It's not necessary or desirable to use BTB's edited version of Service Requirements 1.4.3, because BTB's faction-related edits to that mod have been incorporated into the Necro Edit version of BTBGI above. Just use Service Requirements Lore (Sigourn Edit).

## [Tribunal Rebalance](https://www.nexusmods.com/morrowind/mods/45713)

Morrowind has a fundamental balance problem beyond what BTBGI fixes. The game was originally released without the Mournhold and Solstheim content, with the Tribunal and Bloodmoon expansions adding that new content later. The expansions were designed to be played through by characters who had already done everything they could do on Vvardenfell and thus were super-powerful.

Being designed for godlike level 40+ characters, creatures and NPCs (friendly and hostile) in the expansions are crazy strong, more powerful than some high-level, endgame bosses on Vvardenfell. The result is that low- or even mid-level characters have no hope of completing much of the content of the expanions.

This mod and the next two mods on this list fix this issue by rebalancing the expansion content (and making Sixth House enemies much stronger). This mod starts us off with the Tribunal content. The intent was to rebalance Tribunal as though it had been designed along with the vanilla game and they had shipped together.

Goblins (and their equipment) are drastically weaker, so that relatively low-level characters can beat them without too much difficulty. Most NPCs are no longer insanely high level, and the Dark Brotherhood equipment has been gimped. The Tribunal main quest is still very difficult to complete, and the endgame bosses have not been touched.

This mod and the next two have a "full" plugin and a handful of modular plugins for those who don't want all of the mod's changes. I recommend using the full mod for all three. They should all come after BTBGI in your load order.

## [Bloodmoon Rebalance](https://www.nexusmods.com/morrowind/mods/45714)

This mod does for the Bloodmoon expansion content what the above mod does for Tribunal. The Bloodmoon content is rebalanced as though it had been designed alongside vanilla Morrowind.

Enemies like wolves, bears, rieklings and so on are weaker, and most NPCs are no longer crazy high level. The Bloodmoon endgame is still very challenging, however.

## [Beware the Sixth House](https://www.nexusmods.com/morrowind/mods/46036)

This finishes the job of the previous two mods by making Sixth House enemies much more powerful. The endgame Sixth House bosses are now the most powerful enemies in the game. You can also no longer easily swipe Keening without dealing with an Ash Vampire.

## [More Deadly Morrowind Denizens](https://www.nexusmods.com/morrowind/mods/48745) ([Necro Edit](https://www.dropbox.com/s/x251dgzcfxkv0k5/MDMD%201.05%20Necro%20Edit.7z?dl=1))

All of the rebalances we've installed so far don't change the fact that most of Morrowind's enemies are predictable and easy. They all pretty much have the same boring leveled equipment, cast the same shit-tier auto-assigned spells (though BTBGI at least helps on this score), offer no surprises whatsoever, and require no strategy beyond swinging your weapon at them until they die.

No longer. MDMD takes the sea of mind-numbing pointlessness that is Morrowind enemy NPCs and transforms it into a turbulent ocean of engaging challenges. Many, many enemies have seen stat buffs, "boss" enemies in particular. The shitty, useless spells that so many enemies cast have been replaced with dangerous, genuinely useful spells like custom spells a clever player might have come up with. Some NPCs' weak, generic equipment has been replaced by more interesting stuff that presents more of a threat to you, while not being overpowered. See the readme for a detailed explanation of the mod's changes.

There's also a "creatures add-on" that makes a few changes to creatures and is worth using.

The "Necro Edit" linked above fixes a few issues in the original plugins. Most importantly, the gold values of some of the high-valued weapons have been brought back down to the lower, less exploitable values in previous versions. The other fixes are minor, and are outlined in the Necro Edit readme.

Enable both plugins from the Necro Edit archive. The creatures add-on must load after the main plugin, and both should load after Expansions Integrated but before BTBGI.

## There Can Be Only One ([Nexus](https://www.nexusmods.com/morrowind/mods/47766), [Moddinghall](https://mw.moddinghall.com/file/126-there-can-be-only-one))

Daedric equipment is supposed to be super-rare, but there's actually quite a lot of it in the game. Most pieces have multiple locations, you can get almost all the armor in one go from Divayth Fyr, and you'll be up to your eyeballs in daedric weapons and shields from Dremora and Golden Saints.

This mod makes daedric weapons and armor the legendary equipment they were meant to be by ensuring that there's only one of each in the game (ammunition and thrown weapons excluded). Daedric items will no longer appear on leveled lists. You'll no longer get a piece from almost every Golden Saint you see. Stumbling upon a piece of daedric equipment is now a thrilling experience instead of ho-hum, another daedric weapon to sell.

And while Dremora and Golden Saints no longer drop daedric stuff, they now have constant effect Bound Item abilities, so they still get to use it against you but it disappears when they die, so no daedric loot for you. (The edits related to daedric drops in this mod are the same as those made by the Necro Edit version of BTBGI, so there's no confict there.)

The main version of the plugin replaces Divayth Fyr's daedric equipment with Dwemer, and increases his heavy armor skill to compensate. Some people might not like that change, so there are two alternate versions that handle Fyr differently - one makes his daedric armor disappear when he dies, and one gives him a cool, unique daedric robe. See the documentation for details. Which plugin you use is up to you; I personally prefer the "Alt Fyr 2" version.

This mod removes stuff from leveled lists, and will conflict with any mod that edits the relevant lists. In particular, it conflicts with Expansions Integrated, which also edits one of these lists. Fortunately, in this particular case there's a patch (see Sigourn's Misc Mods and Patches below).

This plugin should load after MDMD but before BTBGI.

If for whatever reason you don't want to use this mod, and you're also not using BTBGI, then I recommend installing Magas Volar Anti-Cheat ([Nexus](https://www.nexusmods.com/morrowind/mods/47714), [Moddinghall](https://mw.moddinghall.com/file/123-magas-volar-anti-cheat)), which both TCBOO and BTBGI incorporate. Magas Volar Anti-Cheat just prevents you from grabbing yourself a duplicate Daedric Crescent by recalling back to Magas Volar after killing the daedra there.

## Helm of Tohan BTBGI Patch ([Nexus](https://www.nexusmods.com/morrowind/mods/47152), [Moddinghall](https://mw.moddinghall.com/file/121-helm-of-tohan-btbgi-patch))

This is a very small mod that adjusts the stats of the Helm of Tohan from the official plugin to be in line with the changes BTB's Game Improvements makes to the regular Adamantium Helm. That's all it does.

The archive contains a plugin version and an MWSE version of the patch. Use the MWSE version.

## [TCBOO Expansions Integrated Patch](https://www.dropbox.com/s/r4zhl6fwox3xble/TCBOO%20Expansions%20Integrated%20Patch%201.0.7z?dl=1)

This patch includes conflicting edits There Can Be Only One and Expansions Integrated make to a leveled list. Put it right after TCBOO in your load order.

## [Sigourn's Misc Mods and Patches](https://www.nexusmods.com/morrowind/mods/49232)

The link above is to a collection of patches and edited versions for several mods, many of which are on this list. We've already installed No Beds for the Diseased earlier, but there are more files here that we need, so download them if you haven't already.

### Ownership Overhaul Patches

This download contains alternate versions of the two Glass Domes of Vivec plugins that incorporate Ownership Overhaul's changes to object ownership (Glass Domes of Vivec has to move the entire contents of many of the plaza cells, which is why the two mods conflict without the patch).

Install only one of the two Glass Domes patches (the Atmospheric Arena version, if you're following this list). Note that this plugin needs to be installed in addition to the plugin in the Glass Domes Moonrain Edition archive; it's a patch, not a replacement. The plugin obviously needs to load after the main Glass Domes plugin.

### MDMD Patches

This file contains patches for MDMD with several mods. You'll want to install the following:

1. Expansions Integrated Patch

Expansions Integrated and MDMD make conflicting edits to a number of NPCs, and this patch fixes it. It should come immediately after the MDMD plugins in your load order (which should themselves be after Expansions Integrated).

2. There Can Be Only One (Alt Fyr 2) Patch

The archive contains six subpackages related to TCBOO. There are patches for the three versions of TCBOO (standard, Alt Fyr 1, and Alt Fyr 2). There's also an alternate version of Alt Fyr 2 (giving an alternate robe to Divayth Fyr) with a patch for it, and an additional modified version of TCBOO that Sigourn calls "Alt Fyr 3", with a patch for it as well. Finally, there's a patch for MDMD's creatures addon and TCBOO.

Install the patch for whichever version of TCBOO you're using; I use Alt Fyr 2 myself. (You can use Sigourn's alternate Alt Fyr 2 if you prefer it, though I wouldn't recommend using Alt Fyr 3.) The patch should go right after the TCBOO Expansions Integrated patch in your load order.

We don't need to install the TCBOO MDMD Creatures patch, because the BTBGI MDMD Creatures patch includes all of its edits and more.

3. BTBGI Patch

BTBGI and MDMD's creatures add-on make conflicting edits to quite a few creatures, which this patch fixes. Put this patch after BTBGI in your load order.

There are actually two versions of this patch. Use the regular version, unless you're using the "creature buffs" plugin from BTBGI, in which case use the creature buffs patch instead.

## [Alvazir's Various Patches](https://www.nexusmods.com/morrowind/mods/48955)

This page is a collection of many (many) patches and tweaks. The file we're mainly looking for on this page is "BTBGI Necro Edit Modular Patch", which is itself a collection of many (many) patches for BTBGI and other mods, plus a few tweaks intended for use with BTBGI. However, also pick up the Bloodmoon Rebalance PFP Patch.

There are only a few plugins we're interested in here. The others either are patches for mods not on this list, or I can't recommend them for other reasons. All of these plugins except the last are in the BTBGI Patch archive.

### Better Clothes Complete and Better Robes Patches

These two patches are in the "Various - Modular" sub-package. Both patches should load after both BTBGI and Better Clothes/Robes.

### Tribunal Rebalance Patch

This one is also in the "Various - Modular" sub-package. However, we'll want to remove a few things from the plugin first. Open up the patch in Enchanted Editor, and *delete* the following from the plugin:

- All the armor records. The patch makes balance decisions here that I don't agree with. Just let tes3merge take care of it.

- The NPC record. King Helseth is also affected by a couple other mods, and tes3merge will be needed for him regardless.

Only the two weapon records (Goblin Club and Goblin Sword) should remain in the plugin.

The patch must load after Tribunal Rebalance (which should load after BTBGI).

### Bloodmoon Rebalance and Beware the Sixth House Patches

These are in "Various - Modular" as well. There are no problems with either of them - indeed the Beware the Sixth House patch fixes a couple of mistakes in that mod.

Both patches should load after their respective mods (which themselves should load after BTBGI).

### More Meaningful Encumbrance

This plugin is in the "Game Settings - Modular" sub-package. It's not a patch; rather, it's a set of tweaks that cause encumbrance to have a greater effect on fatigue costs and jumping height. It also causes spellcasting to cost fatigue, which is also dependent on encumbrance. See "Game Settings.txt" for more details.

This tweak is optional, although I think it's a good change - it gives you an additional reason to watch what you're carrying and avoid loading yourself up unnecessarily. Note that you should be using the "Game Formula Restoration" MCP patch for the spellcasting fatigue cost to work as intended.

More Meaningful Encumbrance needs to come after BTBGI in your load order.

### Suggested Tweaks

Also in the "Game Settings - Modular" sub-package, this plugin makes several tweaks to game settings. However, I only actually like a couple of its changes:

- Lowering the perspective while sneaking in first person, to make it more visually obvious that you're sneaking.

- Increasing the too-sluggish rate of travel of projectiles and thrown weapons.

I don't care for the other changes made by this plugin. So, if you want to use it (like More Meaningful Encumbrance, this one is optional), I suggest opening it up in Enchanted Editor and removing a few records. These are the GMSTs in this plugin that we want to *keep*:

- fprojectilemaxspeed
- fprojectileminspeed
- fthrownweaponmaxspeed
- fthrownweaponminspeed
- i1stpersonsneakdelta

Delete all of the plugin's *other* GMSTs in EE.

### Bloodmoon Rebalance PFP Patch

This patch has its own separate download on the linked page; it's not in the BTBGI Patch archive.

This one patches a number of creatures edited by Bloodmoon Rebalance, incorporating fixes from PFP. Put it somewhere after Bloodmoon Rebalance in your load order.

-----

There's also a file called "Miscellaneous Patches". If you're following this list, this file isn't needed. But if you're not using a body replacer (like Robert's Bodies, the one on this list), you'll want to pick this up and enable the Chuzei BTBGI patch, which combines the fix to a particular helm in MOP's Chuzei fix with the change that BTBGI makes to that helm. (You don't need MOP's Chuzei fix plugin with this patch; just make sure the patch loads after BTBGI.)

## Blighted Blight ([Nexus](https://www.nexusmods.com/morrowind/mods/48631), [Moddinghall](https://mw.moddinghall.com/file/146-blighted-blight))

Originally, it appears that it was supposed to be possible for the player to actually catch blight diseases while outside in a blight storm, but for some reason the Morrowind developers took this mechanic out. This mod adds it back.

Now, there will be a 10% chance (by default) that you'll catch a random blight disease upon each exterior cell change in a blight storm. Any Resist Blight Disease effect you have is taken into account, and you won't be able to catch blight if you have 100% Resist Blight.

This mod works well with Creeping Blight, which we've already installed, which implements the possibility of blight outside Red Mountain before the main quest is complete.

You can adjust the base chance of catching blight on cell change in the MCM. I think the default of 10% is reasonable.

## Equipment Requirements - Necro Edit ([Nexus](https://www.nexusmods.com/morrowind/mods/47813), [Moddinghall](https://mw.moddinghall.com/file/128-clothing-requirements))

In games like Morrowind, character development is supposed to be a long, gradual process. Through experience, you increase your skills and abilities, allowing you to take on more dangerous tasks with greater rewards, enabling you to find and buy progressively better equipment, which allows you to handle even more dangerous areas and thus further develop your character, and so on.

However, this long process can be partially bypassed if you're familiar with the game and where stuff is. You can hop off the boat and immediately seek out high-end equipment and unique artifacts, thus substantially boosting your power right at the beginning of the game, as long as you know where to look. This mod should put an end to that kind of douchebaggery.

Equipment Requirements implements minimum skill thresholds for equipment. The better the equipment is, the greater the relevant skill must be in order for you to equip it. For example, you can equip steel armor with a heavy armor skill of 20, but you won't be able to equip daedric pieces until your heavy armor skill has reached a more respectable 80. This enforces a gradual character progression, where you move on to better and better equipment as you gain the skill to use it.

The requirements are implemented via MWSE-lua. The code contains tables listing the vanilla game's equipment (meaning armor and weapons) and specifying a skill requirement for each piece. Equipment in the official plugins is also covered, along with the equipment from a few other mods, including More Deadly Morrowind Denizens, a mod on this list that adds quite a bit of new equipment. Any piece of equipment without a requirement specified in the code will have a requirement based on a generic formula instead, so if you're using any mods not covered, the equipment added by those mods will still have requirements.

The mod includes an "alternate mode," selectable in the Mod Config Menu. With alternate mode off, you are unable to equip anything you don't meet the skill requirement for. With alternate mode on, the game will allow you to equip anything, but if you don't meet the requirement a penalty will be imposed (like greater fatigue loss, slower movement speed, and a cast chance penalty).

I personally prefer hardcore mode (i.e. alternate mode off), but if you can't stand the thought of not being able to equip ebony armor at level 1, then I guess there's no stopping you.

The links above are to the "Necro Edit" version, which fixes a few issues with the original. This version is packaged along with a mod called Clothing Requirements, which basically does for clothing what Equipment Requirements does for armor and weapons. I don't recommend actually using Clothing Requirements, but do use the version of Equipment Requirements in the archive.

## [Armor Rating](https://www.nexusmods.com/morrowind/mods/49715)

Each piece of armor in Morrowind has an armor rating, which represents how much protection it provides against attacks. When you equip a piece of armor, its armor rating is modified by your relevant armor skill to determine the actual AR it gives you. So far so good.

But the vanilla formula results in an extremely broad range of armor values for a given piece of equipment, depending on skill. With an armor skill of 30, you'll receive exactly the armor's base AR value. With a skill of 5, it will provide only 1/6 the base amount of protection, and at an armor skill of 100 you'll have 3 1/3 times the base AR. In other words, armor is *20 times* more effective with a skill of 100 than with a skill of 5. This is insane, and results in armor being nearly useless at very low skill levels while providing too much protection at high skill.

This mod changes the armor rating formula to be more reasonable. With this mod, you'll start out with the base AR value for equipment at very low skill (instead of having to wait until a skill level of 30 to get that armor rating as in vanilla), while at a skill of 100 you'll see twice the base level of protection (instead of 3 1/3 times, as in vanilla). In other words, armor ratings will be higher than vanilla at low skill levels and lower than vanilla at high skill.

The mod also has another effect: it makes bound armor actually useful, even at high skill levels. In vanilla Morrowind, bound armor is an exception to the armor rating formula - it just grants the base AR value regardless of armor skill (in other words, it grants protection as though your armor skill were 30, no matter how low or high it actually is). Bound armor actually has quite high base AR, but even at moderately high armor skill you're better off using weaker armor that provides a benefit that scales with your armor skill.

With this mod, the effectiveness of bound armor will scale with your (light) armor skill just like any other armor, except that it's also modified by your conjuration skill. You'll need 100 conjuration skill to receive full benefit from bound armor; you can receive as little as half protection (though again still modified by your light armor skill) with very low conjuration.

And there's one other change made by this mod. In vanilla Morrowind, the maximum damage reduction provided by armor is 75%. Any attack will do at least 25% of its full damage, no matter how high your armor rating. This mod changes the maximum reduction to 90%, so high AR can reduce incoming damage to as little as 10% of the full value. This can potentially help to compensate for reduced effectiveness of armor generally at high skill levels. This setting can be adjusted in the MCM, if you feel the need.

Armor Rating makes a good companion to Equipment Requirements. This mod makes armor more effective than vanilla at low skill levels, while Equipment Requirements limits you to low- or medium-tier armor until you're more skilled, at which point the AR for high-tier armor will be somewhat lower than in vanilla. This prevents you from exploiting the effects of this mod by grabbing a few pieces of ebony or daedric armor right off the boat and enjoying their full base AR values, while at higher skill levels, the reduced effectiveness of armor gives you more of an incentive to seek out the more powerful equipment sets which are newly opened up to you.

As discussed above, this mod will make the early game somewhat easier and the late game somewhat harder. If you don't want that for whatever reason, then I suggest installing Useful Bound Armor ([Nexus](https://www.nexusmods.com/morrowind/mods/49829), [Moddinghall](https://mw.moddinghall.com/file/153-useful-bound-armor)) instead, which just causes the AR of bound armor to scale with light armor skill, without the other armor rating changes.

## [Sneaky Strike](https://www.nexusmods.com/morrowind/mods/48317)

Morrowind, like many similar games, has a "sneak attack" multiplier. If you manage to attack an enemy without that enemy being aware of your presence, the damage from the attack (weapon damage only, not any enchantment damage) is multiplied by this value, which is 4.0 in vanilla Morrowind and 2.5 with BTBGI.

Whether you're using a light, fast dagger or a massive, cumbersome warhammer, the damage multiplier is the same for a sneak attack, which makes sneak attacks with heavy, powerful weapons insanely damaging (though somewhat less so with BTBGI).

This mod changes the sneak attack multiplier depending on the type of weapon you have equipped, in particular depending on the speed stat of that weapon. With vanilla Morrowind's sneak attack multiplier GMST of 4.0, and with default settings in the MCM, sneak attack damage multiplier will range from 1.0 for very slow, heavy weapons to 7.0 for very fast weapons like daggers. In other words, if you plan on doing sneak attacks, use light, fast weapons; there's no point in even trying it with heavy warhammers and the like.

Another useful feature of Sneaky Strike is that it allows you to achieve critical damage on sneak attacks with ranged weapons like bows (in vanilla, this was not possible).

The MCM contains a setting that you can adjust to tweak the sneak attack damage (lower values for the setting result in higher sneak attack multipliers). If you're using BTBGI (which lowers the base multiplier from 4.0 to 2.5), you'll need to change this setting in order to ensure a reasonable multiplier range.

In particular, I recommend changing it from the default 3 to 1.5. This, together with BTBGI, will result in the sneak attack multiplier ranging from 1.0 for very slow weapons to 4.75 for very fast weapons. (If you're not using BTBGI, then you shouldn't make this change; the value of 1.5 for this setting assumes a base multiplier of 2.5.)

Unfortunately, the MCM does not allow you to change this setting to a non-integer value, so you'll need to open the config file (MWSE\config\sneakyStrike.json) and set `coefShift` to 1.5 there. If you subsequently check the MCM, it will say the value is 2, but it will actually remain 1.5 as you set it in the config file, as long as you don't mess with it.

## [Locks and Traps Detection](https://www.nexusmods.com/morrowind/mods/48528)

In vanilla Morrowind, you can always tell when an object is trapped, regardless of your skill level, which is absurdly unrealistic and makes traps meaningless. You can also always determine the exact lock level of a lock, again regardless of your skill level. Morrowind Code Patch has the "Hidden Traps" and "Hidden Locks" patches, which make it so that you can never tell when something is trapped or locked, again regardless of your skill level. This is no less unrealistic, and vastly more frustrating.

This nifty MWSE mod finds a middle ground, making whether or not you're able to detect a trap depend on your security skill, amongst other things. The trap mechanic is now much more realistic and gives you an additional incentive to improve (or fortify) your security skill. Your security skill also determines whether or not you can tell that something is locked, and your degree of confidence regarding its lock level.

Traps can still be a frustrating aspect of the game for non-thiefly characters who are less likely to be able to detect them, but at least it's realistically frustrating, and there are a couple ways around it (Telekinesis, for example). Also, the version of Enhanced Detection I recommend above adds the Detect Trap magic effect which allows magically inclined characters to detect traps.

A couple terms in the formula the mod uses can be customized in the MCM, but I see no reason to change them. Also, this mod requires that MCP's Hidden Locks and Hidden Traps patches be enabled, which they should be if you're following this list (without those patches, the game would always show when an object is trapped or locked regardless of this mod).

Also, the MWSE mod Security Enhanced, which we installed earlier in this list, includes an option in its MCM to automatically equip a probe whenever you activate a trapped object. This option doesn't know you're using Locks and Traps Detection, so will equip a probe even if you don't detect the trap, which would obviously defeat the purpose of this mod. Therefore, automatic equipping of probes should be disabled in the Security Enhanced MCM.

## [Stealth Improved](https://www.nexusmods.com/morrowind/mods/49614)

This mod introduces a number of refinements to Morrowind's stealth system, including a few tweaks to the calculations determining when you're detected. These are mostly minor but important tweaks to improve stealth over vanilla; this is mostly not a radical transformation of the stealth system.

With default settings, the important differences for our purposes are:

- How close you are to a light source is taken into account.

- Stealth checks happen every one second instead of every five.

- Chameleon and Invisibility provide less of a bonus to stealth. In vanilla, being invisible guarantees that no one can possibly detect you, and chameleon is very overpowered. Now both effects provide significant bonuses but are no longer guarantees.

- NPCs get a +20 bonus to their effective sneak skill when it comes to their chance of detecting you. NPCs tend to have very low sneak skills and are pretty easy to hide from in vanilla.

- It's twice as hard to avoid being detected by an NPC who's facing you.

- Sneak attacks from behind always hit.

- You're no longer guaranteed to not get caught when taking an item while invisible and sneaking. In vanilla Morrowind, taking an item while invisible dispels your invisibility, but no new stealth check is conducted, which means, if you're sneaking, you're guaranteed to remain undetected for some length of time. Now a new stealth check is conducted immediately, before taking the item, so you're just as likely to be seen as you would have been without invisibility.

Overall this mod represents a significant improvement to the vanilla stealth system, making it now reasonably (but not overly) difficult to sneak around without being seen.

Just about every aspect of the mod is configurable in the MCM, and I recommend making a few changes. First, I turn off the "enable light-based stealth" and "show light bar" options. The light-based stealth feature isn't actually based on how much light is illuminating you, but on how close you are to any light source, including those that aren't actually emitting any light.

Second, I change "percentage effectiveness of chameleon" from 50 to 25. This means only 1/4 (instead of 1/2) of your chameleon magnitude will be added as a bonus on your stealth check. It also means invisibility will provide a slightly higher bonus than 100% chameleon, with the downside of going away as soon as you do anything except move.

Finally, there's a few additional tweaks I like to make to this mod, but doing so requires editing the code to change three things that I think are less than ideal:

1. Chameleon magnitude beyond 100 contributes to your sneak bonus, so you can still stack on chameleon above normal magnitudes to get a really high bonus. I think chameleon magnitude should be capped at 100 for the purpose of calculating sneak bonus.

2. If you have chameleon and invisibility at the same time, you get both bonuses. I think you should get only whichever bonus is higher.

If you agree with me about the above two points, open up MWSE\mods\stealth\main.lua in a text editor. Find this part:

```
-- Add on chameleon modifier.
playerScore = playerScore + (config.chameleonMultiplier/100 * macp.chameleon) --chameleon only counts for half

-- Invisibility bonus, defaults to 0 but can be manually restored
if (macp.invisibility > 0) then
    playerScore = playerScore + config.invisibilityBonus
end
```

Delete the above and replace it with the following:

```
local effectiveChameleonMagnitude = math.min(macp.chameleon, 100)
local chameleonBonus = ( config.chameleonMultiplier / 100 ) * effectiveChameleonMagnitude
local invisBonus = 0

if macp.invisibility > 0 then
    invisBonus = config.invisibilityBonus
end

local finalBonus = math.max(chameleonBonus, invisBonus)
playerScore = playerScore + finalBonus
```

3. In addition to the above, there's one minor error in the code that causes the "NPC sneak bonus" slider in the MCM to not function. To fix it, in mcm.lua (not main.lua), find this line:

```
id = "npcSneakMultiplier",
```

and replace it with:

```
id = "npcSneakBonus",
```

## [MAB0's Foundations](https://www.nexusmods.com/morrowind/mods/47244)

MAB0's Foundations doesn't actually do anything by itself. Rather, it's a framework required for the next mod on this list. So just install it and move on.

## [MAB0's Manipulated](https://www.nexusmods.com/morrowind/mods/47222)

In Morrowind, assaulting and killing a friendly NPC is a crime (and now, thanks to the Crime module of Economy Adjuster Adjustments we installed earlier, it's a very serious crime). But if you cast a Frenzy Humanoid spell on that same friendly NPC first to magically compel them to attack you before ripping them a new one, no crime is committed, no matter how many witnesses were watching. That kind of nonsense ends now.

This mod makes casting "mental manipulation" effects on friendly NPCs a crime. Specifically, by default the mod criminalizes the following effects: Frenzy Humanoid, Calm Humanoid, Rally Humanoid, Demoralize Humanoid, Command Humanoid and Charm.

The implementation is very well done. Casting one of these effects on an NPC counts as assault, and will give you the same bounty as any other assault (which, with EcoAdj Crime, is now sizeable). If there are no witnesses around, no crime is reported, just as with any other assault. You can still use magic to force people to attack you, but be prepared for the consequences.

The mod has an MCM that can be used to disable the criminalization of any of the six affected spell effects, and I suggest doing so for three of them: Calm Humanoid, Rally Humanoid and Charm. Calm Humanoid is an attempt to *stop* a fight, and shouldn't be a crime. Rally Humanoid is likely to be used "legitimately," for example on followers to prevent them from running away in a fight. And criminalizing Charm would pretty much eliminate its usefulness (and making somebody temporarily like you so they'll give you information or sell their stuff more cheaply is a far cry from magically compelling them to attack you so you can mercilessly tear them apart).

But there's no excuse for Frenzy Humanoid being legal. Command Humanoid is also highly exploitable and can easily be used to lure an NPC to their death (though BTBGI takes steps to limit its use to low-level NPCs). And I guess Demoralize Humanoid is more "hostile" of an effect than Calm, Rally and Charm, so it can be criminalized too.

Finally, I've received reports that this mod no longer works for everybody, though it still works properly for me. Check mwse.log. If you see an error related to this mod, you might need to just skip it. I'm not sure what causes the error, or why it happens for some people but not others. Unfortunately, if this mod doesn't work for you, I'm not aware of a good alternative.

## [Controlled Consumption](https://www.nexusmods.com/morrowind/mods/49232)

This is an anti-exploit mod that restricts how often you can drink a potion or consume an ingredient, or how many potions/ingredients you can have affecting you at one time. If not enough time has passed, or you're already under the effect of too many potions/ingredients, and you try to consume another one, you'll see a messagebox informing you that you must wait until the required amount of time has passed or until one of your potions/ingredients expires before you can consume the next one.

This obviously prevents a number of potential exploits, such as stacking lots of restore health potions until you can survive anything, or fortify strength potions until you can kill Vivec with one blow. You can still swill a fortification potion before a fight, or a healing potion to heal up after one, and you can still eat an ingredient raw to give yourself an effect that you lack a potion for, but you can no longer use alchemy to make yourself a god.

The link above is to "Sigourn's Misc Mods and Patches," from which you should have already picked up this mod. The version of Controlled Consumption on Sigourn's page is the "MMC Edit" version, which also affects ingredient consumption (the [original version](https://www.nexusmods.com/morrowind/mods/45624) of the mod only affects potions).

In the MCM, there are three "modules" you can choose from which determine how the mod works (in addition to a fourth module that just disables the mod). "Vanilla NPC Style" implements a five-second cooldown time between potions or ingredients (i.e. after you consume a potion/ingredient, you must wait at least five seconds, not counting time with the menu open, before consuming the next one). "Oblivion Style" does not have a universal cooldown time, but prevents you from being under the effect of more than four potions or ingredients at once. "Vanilla NPC Style (Necro Edit)" is identical to Vanilla NPC Style, except that it fixes an issue that can arise when the timescale changes (which it will if you're using Dynamic Timescale), and is the module I recommend.

## [Silver Tongue](https://www.nexusmods.com/morrowind/mods/49086)

This mod enhances the game's speechcraft/persuasion system in a number of ways. It basically does for speechcraft what Alchemical Knowledge does for alchemy.

A number of new features and abilities are added to the persuasion system, and most options now have speechcraft skill requirements to be able to use. With default settings, increasingly powerful features become available depending on your speechcraft skill:

- 0-24: You cannot see NPCs' disposition, nor can you use the admire, intimidate or taunt persuasion options. The only persuasion option available is bribe. This adds a new difficulty to getting information from people, since your only clue to how they feel about you is what they say. It also makes increasing your speechcraft skill at low levels more expensive, since your only option besides paid training is bribes.

- 25-49: You can now see NPCs' disposition. (You can't actually see the exact number, unlike in vanilla, but the blue bar will clue you in to approximately how they feel about you.) You can also now admire NPCs to increase their disposition further.

- 50-74: In addition to disposition, you can now see a bar indicating NPCs' fight rating, or their inclination to attack you. You can also now manipulate that fight rating through the intimidate and taunt options.

- 75-99: You can now see a bar indicating NPCs' alarm rating, or how inclined they are to report your crimes. In addition, when you successfully bribe an NPC, their alarm rating will decrease.

- 100+: You can now start conversations with hostile NPCs, as long as they're not actually attacking you. This allows you to potentially make them non-hostile by intimidating them.

In addition to the above, paupers are now easier to bribe, while guards are now less likely to accept your bribes - and a failed attempt to bribe a guard will lead to your arrest. This is balanced by the possibility of using bribes to lower guards' alarm ratings so they'll look the other way when you commit a crime, if your speechcraft skill is high enough.

All of the mod's features, including the skill thresholds for various abilities, can be configured in the MCM. In general I suggest sticking with the default settings, but there's one change I highly recommend making: increase the skill requirement for taunting to 200, as high as it will go (and if you think you might actually reach 200 speechcraft skill, you can edit MWSE\config\Silver Tongue.json and change `allowTaunt` to something like 1000). This will essentially disable taunting entirely.

Why disable taunting? Because it's just too powerful. In Morrowind, it's technically a crime to walk up to a friendly NPC and stab them through the heart, but the taunt option basically makes the law against murder a dead letter.

By using taunt, you can force any NPC to attack you, no matter who they are, and no matter how low your speechcraft skill. Even with a skill of 5 and a disposition of 0, your taunts will still occasionally succeed, so all you have to do to make any NPC attack you is just mash the left mouse button. And once they take the bait you can slaughter them with impunity, in front of witnesses, with no legal consequences.

You can walk up to the King of Morrowind himself, in his throne room surrounded by his guards, and say a few unkind words about his mother until he personally attacks you (rather than ordering his guards to do it). And once he does so, you can bash his skull in with your +5 Mace of Godly Strength, strip his corpse naked, take his Royal Signet Ring and slip it on your own finger, then casually walk out of the room humming a tune, while his elite guards just stand there dumbly as though nothing had happened.

This should not be possible no matter how skilled you are at smooth talking.

By disabling taunting, you can no longer kill anyone you want with no bounty. This works very well with MAB0's Manipulated, which criminalizes the use of Frenzy Humanoid. You can still go around killing friendly NPCs, but if there are witnesses expect your crime to be reported.

In addition to disabling taunting, there are two tweaks I suggest making to the mod's code (edit the mod's main.lua file in a text editor):

1. Topic pane width

This mod increases the width of the dialogue menu's topic pane, which can sometimes cause a portion of a long greeting to be cut off. There's no need to widen the topic pane anyway; the vanilla width is quite wide enough for the mod's new fillbars.

To fix this, change all five instances of the number `192` in the function `updateDialogFillBars` to `166`. This will revert the topic pane to its vanilla width.

2. Log errors

The mod will sometimes cause errors in mwse.log related to trying to index a nil value. To fix this, find this line:

```
if e.target.object.baseObject.objectType ~= tes3.objectType.npc then return end
```

Immediately *before* that line, add:

```
if not e.target.object.baseObject then return end
```

## [Putting Power in Willpower](https://www.nexusmods.com/morrowind/mods/45742)

In vanilla Morrowind, the willpower attribute is useful for very little. It contributes to your max fatigue, and it helps you resist certain magic effects that have no magnitude, such as paralysis, and that's pretty much it. A couple mods we've already installed implement additional uses for willpower: with CCCP, willpower influences your rate of magicka regen, and with Wings of Will, it affects your speed while levitating. This mod will finish the job of making willpower a full-fledged attribute.

Putting Power in Willpower allows the willpower attribute to contribute to resistance against just about all resistable magic, not just those very few effects with no magnitude. Players (and NPCs) with high willpower will find themselves taking less damage from enemy spells, enchantments and traps, and doing more damage to enemies with their magic. Conversely, those with low willpower will find themselves taking more magic damage, and their own offensive spells less effective.

The primary determining factor is the difference between the caster's and target's willpower. When the caster has a lower willpower than the target, the spell will do less damage than normal, while, depending on how the mod is configured in its MCM, it will do more than normal damage when the caster's willpower is higher than the target's. The target's luck and fatigue are also taken into account.

There are a few important considerations with this mod:

1. Ignore the plugin. It's intended to be used with a feature of the mod that we'll be disabling.

2. There's a minor oversight in the code that can cause a target's high fatigue to make things worse instead of better when the target's willpower is lower than the caster's. To fix this, open up MWSE\mods\r0\will\main.lua in a text editor. Find the line that says:

    ```
    local resistBonus = config.resistMultiplier / 10 * ( ( targetFatigueTerm * ( ( targetWillpower - casterWillpower ) + 0.1 * targetLuck ) ) )
    ```

    Immediately before this line, insert the following:

    ```
    if casterWillpower > targetWillpower then
        targetFatigueTerm = 1 - ( targetFatigueTerm - 1 )
    end
    ```

3. There's another mistake in the code that prevents resisting effects without a magnitude, like Paralysis. To fix it, find this line:

    ```
    if ( resistChance > roll ) then
    ```

    and change it to this:

    ```
    if ( e.resistedPercent > roll ) then
    ```

4. In the MCM, change the resist multiplier from 10 to 5. This will have the effect of halving the resist bonus (or penalty) granted by the mod. With the default multiplier, the resist bonus/penalty can become pretty overpowered when the difference in willpower is large. It's even possible to achieve outright immunity to most magic with high enough willpower, and a high-willpower mage can steamroll many enemies with offensive magic. A multiplier of 5 results in more modest, but still significant, resistance bonuses.

5. Turn on the option to allow negative resistance bonuses. This will allow spells and enchantments to do greater than normal damage against targets with low willpower (and the multiplier change above will prevent this from becoming overpowered).

6. Turn off the option allowing magic absorption for high resistances. This is totally unnecessary, and resistance is unlikely to get that high anyway.

I suggest leaving the other MCM options alone.

## [DragonDoor](https://www.nexusmods.com/morrowind/mods/47169)

Have you ever noticed how you can have every guard in town chasing you, hot on your tail, but all you have to do to evade pursuit is step into the nearest house? Or how those hostile bandits will never follow you outside their cave? The fact that NPCs can't pass through loading doors is a highly exploitable gameplay mechanic.

This MWSE mod fixes this mechanic. You can now no longer escape hostile NPCs just by passing through a loading door into another cell. This is both a difficulty and a realism improvement. Now you'll have to be more careful not to piss off people you can't handle, especially if you have no means of escape and can't outrun them.

Hostile NPCs won't follow you forever. You can make them lose sight of you, or give up the chase if you run far enough, and teleporting away is a guaranteed escape. Hostiles who abandon the pursuit will return to their original locations.

There are a number of options in the MCM; most of these can be left alone, but there are two options you might want to change. First, turn off the option allowing vampires to chase you. Vampires aren't terribly smart, and if you leave this option enabled they'll chase you right into the sunlight.

Second, you might also want to disable the option allowing NPCs to call for help in battle. This option can have a radical effect on combat in dungeons. NPC enemies will call for help unless you kill them (or otherwise disable them, such as with paralysis) very quickly, which will bring every other hostile NPC within a configurable distance running.

In theory, this is a substantial realism improvement. Enemies will hear the commotion of combat and come running to assist, rather than allowing you to take them on one at a time while their colleagues in the next room stand by and do nothing. However, in practice, often every enemy in the current cell will swamp you all at once, which can easily become overwhelming. Feel free to try out this mechanic if it sounds fun, but you might end up disabling it just to protect your sanity.

There's one additional feature of this mod that I don't care for, and it can't be disabled in the MCM, so we'll need to tweak the mod's code. When a pursuing enemy gives up the chase and returns to their original position, the mod will award you experience toward your sneak skill. I think this is silly.

If you agree with me, open up the file MWSE\mods\DragonDoor\main.lua in a text editor. Unfortunately, the code formatting for this author's mods is horrible. You'll find two instances of the following text:

```
mp:exerciseSkill(19, 1 + r.object.level/10)
```

Delete them both. Don't delete the entire lines; just delete the above text.

## [Dungeons Rest](https://www.nexusmods.com/morrowind/mods/49699)

Like DragonDoor above, this mod eliminates an exploit that comes from attacking enemies in dungeons and then running away. In vanilla Morrowind, you can fight an enemy, wear down their health, and run away when you're overwhelmed; when you return after resting and recuperating, you'll find your opponent in the exact same state you left them.

With Dungeons Rest, when you leave a dungeon with hostiles, any enemies you've damaged but not killed will be fully rested and restored by the time you return. Only health, magicka and fatigue are affected - damaged gear remains damaged, and dead opponents stay dead.

This mod works well with DragonDoor. Hostiles who are chasing you will not be affected by this mod, but if you give them the slip and then return later, you'll find them rested and at full strength.

## [Limited Leaping](https://www.nexusmods.com/morrowind/mods/46299)

In vanilla Morrowind, besides the fatigue loss, there are no restrictions on jumping - you can jump as many times in a row as you want, even with no fatigue at all. This leads to some silliness, like players "bunny hopping" everywhere they go, both to get there faster (though Reduced Forward Jump, which we installed earlier, addresses this) and to train the acrobatics skill.

BTBGI helps a little by increasing the fatigue cost of jumping from 5 to 20, but this is really just a bandaid. The cost of constant jumping has been increased, but players who are willing to jump through the wilderness with zero fatigue are still able to do so.

Limited Leaping is an MWSE mod that introduces the ability to set restrictions on when you can jump. It has the potential to have a pretty radical effect on the game, but my recommended settings result in a more modest change.

The mod has an MCM with two configurable settings: the cooldown time required between jumps, from zero to ten seconds, and the minimum fatigue required to jump, from zero to 100. (You can actually set these higher than these maximums by editing the config file, but I wouldn't recommend it.)

I recommend setting the cooldown time to one second, minimizing it without disabling it entirely. A mandatory cooldown between jumps doesn't make much sense; after all, in real life you're generally able to jump over and over again with no rest time in between, as long as you don't get too tired. But without any cooldown at all, the game allows you to rapid-fire jump up a steep incline (like the ramps in Vivec exteriors) to quickly train your acrobatics skill. Setting the cooldown to one second prevents that cheese without being too limiting.

I set the minimum fatigue to jump to the amount that jumping lowers your fatigue. This way, if you don't have the full amount of fatigue that jumping costs you, you can't jump. This will at least put an end to unlimited bunny hopping, requiring you to rest and regain some fatigue before jumping again. This is just a bit more realistic.

Jumping lowers your fatigue by 5 points in vanilla Morrowind, and by 20 with BTBGI. If you're using the "More Meaningful Encumbrance" tweak mod, the fatigue cost of jumping will vary from 15-35, depending on encumbrance; in this case, I suggest setting the minimum fatigue to jump to 35.

# Optional/Hardcore Mods

Everything on this list is optional; this list reflects my personal vision for Morrowind, and it's definitely not for everybody. However, the mods in this section are more optional than most.

These mods will tend to present a more radical change to the game and/or a more extreme increase in difficulty than other mods on this list, and there are definitely good reasons to not use them. Only install these mods if you're the kind of person who will enjoy the experience they provide.

## [Limited Intervention](https://www.nexusmods.com/morrowind/mods/46687)

The first few mods in this section will restrict the use of teleportation magic in one way or another; this one limits the number of times you can cast Almsivi or Divine Intervention spells. This is needed to balance these spells and prevent them from being abused.

Most players end up using AI/DI as a method of routine fast travel, or a way to haul lots of loot back to town, rather than the purpose for which they were intended: escape from a dire situation in an emergency. But the gods no longer have infinite patience, and will only intervene to save you so many times.

First, if you're not a member of the Tribunal Temple or Imperial Cult, the respective intervention spell will no longer work at all. The gods don't intervene to save the lives of people who don't serve them. This also means that only one or the other spell will be usable in any given playthrough, since we've also installed Religions Elaborated which prevents you from joining both factions.

Second, there's a limit, configurable in the MCM, to how many times the spell will work. The limit is the maximum number of times the spell can be cast per rank in the associated faction. This means that if the limit is set to two, and you're at the fifth rank, you'll be able to cast the spell ten times. The default limit is two castings per rank for both AI and DI; this is reasonable, but you might set it to one casting per rank if you want to be super hardcore.

Third, this limit applies not per in-game day, but to the *total* number of times you can *ever* cast the spells. This enforces the intended use of the spells: for emergency escape. With a limit of two castings per rank, you'll only be able to cast the spell a maximum of 20 times (since there are ten ranks), so you certainly won't want to waste it just to save yourself a trip from Vivec to Ebonheart.

Finally, the restriction only applies to casting the actual spells. It does not apply to AI/DI effects in scrolls and other enchanted items, or potions. So you can still use those AI/DI scrolls if you really need to. However, another optional mod we'll get to in a bit will cause you to think twice about that too.

## Limited Recall ([Nexus](https://www.nexusmods.com/morrowind/mods/48438), [Moddinghall](https://mw.moddinghall.com/file/141-limited-recall))

Similar to Limited Intervention above, this mod limits how often you can cast Recall by imposing a per-day limit.

By default the limit only applies to spells, but you can configure the mod in the MCM to apply to other sources as well (scrolls, potions, enchanted items), and I recommend doing so. This closes off the most obvious way of getting around the limit.

You can also make the limit apply per real-life day instead of per in-game day as default, and I suggest enabling this setting as well. This will prevent you from just abusing the wait key so you can Recall again.

Finally, the MCM includes an option to enable a lifetime limit to the number of times your character can *ever* use Recall, in addition to the daily limit. This is similar to how Limited Intervention applies to AI/DI spells, and is definitely recommended.

The daily and lifetime limits themselves are also configurable in the MCM. The defaults are one Recall per day, and 10 lifetime if the lifetime limit is enabled. You might want to increase the lifetime limit to something like 20, both to match the default AI/DI limit in Limited Intervention and because it also can apply to enchantments and potions. Increasing the daily limit to two is also reasonable.

## [Naked and Alone](https://www.nexusmods.com/morrowind/mods/47910)

This is the last of the mods on this list changing teleportation spell mechanics, and it's a big change. This mod causes (or can cause, depending on how you configure it in its MCM) AI/DI to only teleport *you* to the nearest Temple or Cult shrine, not your belongings. In other words, you appear at the shrine completely naked.

The gods might be convinced to save you from disaster a few times (and only a few times, with Limited Intervention installed), but there's a big drawback. They won't transport all of your equipment and loot with you. Instead, it will all be dumped on the ground at the point you teleported from. You can get it all back later, but it requires venturing into danger again once you've recovered and restocked.

The core functionality of the mod is implemented via MWSE, but there's also an optional plugin that makes a few minor changes to the Temple/Cult shrine areas. There are now donations of mostly clothing items left behind by the faithful for those in need (which now includes you), so you can at least walk out with dignity wearing a Common Robe. A new NPC is also added in the Gnisis Temple who partially explains the new mechanic, and a few supporting dialogue changes are made. I definitely recommend using the plugin in addition to the required MWSE component.

The mod can be configured in a couple of ways in the MCM. First, you can choose whether *everything* is left behind when you cast AI/DI, or whether you get to keep your worn equipment. By default, everything is left behind, and I recommend keeping it that way.

Second, you can also set a percent chance of your stuff being left behind. By default this chance is 100%, but you can set it lower so it ends up being a roll of the dice. I suggest leaving it at 100%.

Overall, this mod combined with Limited Intervention will ensure that you only use AI/DI effects in genuine emergencies, rather than abusing them to carry back lots of loot or just for routine travel. Note that this mod also applies when you cast AI/DI from an enchanted item or potion.

There are a couple considerations here. First, despite the fact that you're now naked, Morrowind will place you *outside* the temple or fort, exposed for the world to see, when you use intervention. If you're not much of an exhibitionist, you might want to use [Intervention Improved](https://www.nexusmods.com/morrowind/mods/43267) instead of Improved Temple Experience. Intervention Improved adds teleport markers and shrines just like Improved Temple Experience does, but the main plugin of Intervention Improved also causes you to end up *inside* next to the shrine, instead of outside subject to public scorn. There's also a "Ghostgate Pull" version which is pretty nifty; see the readme to learn more (I definitely can't recommend the version that adds the Mages Guild teleportation spell though).

Second, keep in mind that gold is an item that gets left behind like anything else, so you can't just buy new equipment right off the bat. You'll have to gather ingredients or easy loot, or steal stuff, or find some other way to make a bit of money to buy basic equipment and other essentials, then venture back into the lion's den that caused you so much trouble in the first place so you can finally retrieve your stuff. If you've taken over a house for storage, you might want to stash some gold away there for a rainy day.

And speaking of gold...

## [Worth Its Weight](https://www.nexusmods.com/morrowind/mods/48070)

In vanilla Morrowind, gold is weightless. You can run around carrying hundreds of thousands, or even millions, of gold pieces and not be encumbered by it in the slightest. This mod will change that.

Worth Its Weight is a gold weight mod. It uses MWSE-lua to add weight to gold pieces. Now gold will weigh you down just like any other object you have to carry, and you can only lug around so much of the stuff without becoming overencumbered.

There are two versions of the mod available for download. The newest version is labeled "experimental," but it works quite well, with no performance issues. Just get the newest version.

The weight per gold piece is configurable in the MCM. The default value is 0.02 pounds per gold piece, or 50 gold to a pound. This is reasonable, but you can adjust this value if you feel a need.

This mod creates quite a substantial change to how you play the game, which is why it's in this "optional" section. With default values, you're simply not going to carry more than a few thousand gold around with you. This means you need to either spend your money as you get it or find a house or somewhere else to store stuff so you can offload excess coin. You'll also need to figure out a way to manage any large purchases.

In short, this mod makes dealing with gold more realistic but less convenient.

## [Skills Module](https://www.nexusmods.com/morrowind/mods/46034)

This mod does nothing on its own. It's required by Ashfall (see below). So, if you plan on using Ashfall, also install Skills Module. If you don't, then don't.

## [Ashfall](https://www.nexusmods.com/morrowind/mods/49057)

Ashfall can be described as a needs mod, but that's not really doing it justice. Ashfall is an extremely well done, full-featured survival mod implemented in MWSE.

To give a very brief summary of Ashfall's mechanics: Ashfall has hunger, thirst and tiredness mechanics - you need to eat, drink and sleep periodically, or you'll gradually get weaker. It has temperature mechanics - dress for the weather or you'll suffer the effects of heat or cold. It has survival mechanics - cut firewood, build a fire, boil water, cook food, pitch a tent.

The Nexus page contains a link to a wiki with a more thorough run-down of Ashfall's many features, and is strongly recommended reading if you plan on playing with the mod.

Ashfall is in the optional section because it, like other needs mods (indeed more so), has a radical effect on how you play the game. This kind of mod isn't everybody's cup of tea, but if you enjoy needs mods generally, Ashfall is far and away the best choice.

There are a few special considerations for those following this list if you choose to use Ashfall:

1. You won't want to use Blighted Blight. Ashfall includes its own mechanic for catching blight diseases when out in blight storms, and Blighted Blight would conflict. (You can, and should, still use Creeping Blight, which allows the blight to spread outside Red Mountain.)

2. You also probably won't want to use Dynamic Timescale. Playing with a timescale higher than 20 is not recommended with Ashfall, as the mod's needs mechanics depend on the passage of in-game time. If time passes too quickly, you'll find yourself needing to eat/drink/sleep too frequently in real-time.

    I recommend using Pass the Time ([Nexus](https://www.nexusmods.com/morrowind/mods/48217), [Moddinghall](https://mw.moddinghall.com/file/136-pass-the-time)) instead and setting the normal timescale to 20. (Also be careful with fast-forward/turbo mode.) You can lower the timescale below 20 if you want an easier time of things. You can also continue using Dynamic Timescale if you really want to, but at the very least you should drastically lower the default wilderness timescale of 120.

3. A beta version of Ashfall had a conflict with CCCP, where max magicka could get out of whack under certain circumstances (possibly among other things). With the release version of Ashfall, there appears to no longer be a serious conflict.

    I think the two mods should work fine together, but if you experience any problems playing with both, please let me know.

## [No Combat Menu](https://www.nexusmods.com/morrowind/mods/46732)

This mod, as I'm sure you can imagine just by looking at the name, prevents you from opening the menu while you're in combat. Specifically, it prevents you from opening the inventory / right-click menu or opening containers (including corpses), but does not prevent you from opening the game menu with the Escape key.

Obviously, this represents a significant, even radical, difficulty increase. You can no longer open up your inventory in the middle of combat to swap equipment or spells (though you can still pause the game if needed with Escape). Instead, you must plan encounters in advance, anticipate what you're going to need and ready it ahead of time. Make good use of your hotkeys.

This mod creates a sense of tension and nervousness when exploring the game, and isn't that a nice feeling? The world feels more dangerous now.

The mod has an MCM in which you can customize the distance you must be from anything that wants to rip your head off before you can open the inventory again. I suggest cranking it up to max (4000). This prevents you from just running a short distance away so you can open your inventory.

## No Console ([Nexus](https://www.nexusmods.com/morrowind/mods/48448), [Moddinghall](https://mw.moddinghall.com/file/142-no-console))

Does exactly what it says on the tin: disables the console.

Sometimes, the temptation to cheat using the console is just too much to overcome. This mod eliminates that temptation, forcing you to play it straight.

There are very few situations in which you legitimately *need* the console. If you do run into a situation in which using the console is legitimate (say, to bypass a bug that prevents you from progressing in a quest, or if you get stuck in an object), you can always save and quit, uninstall this mod, reload, fix the situation with the console, then save, quit and reinstall the mod. But that's enough of a pain in the ass that you won't do it just to `coc` to some distant location or to kill a tough opponent. (And Restrictive Saving below will make this even more of a pain.)

## One Life to Live ([Nexus](https://www.nexusmods.com/morrowind/mods/48316), [Moddinghall](https://mw.moddinghall.com/file/139-one-life-to-live))

This is a permadeath mod. You have a configurable number of lives, and when you run out of lives, you will no longer be able to load any saves for that character. Your number of lives remaining is displayed in the stat menu along with your level and class information.

As you would expect, this represents a radical change to the game. Your heart will beat a bit faster knowing that around any corner lurks the real danger of death, meaning not just reloading your last save but starting all over again. If you enjoy that kind of experience, then install this mod.

## [Deleveler](https://www.nexusmods.com/morrowind/mods/47897)

This mod creates a more radical change, and a steeper difficulty increase, than just about anything else on this list. So, if that's not your bag, then skip this one.

Deleveler is an MWSE mod that, on the fly and with no need of a plugin, "delevels" all of your leveled lists. This means that all creatures and items in their respective leveled list types now appear at level 1. This applies to vanilla leveled lists and those added or changed by mods.

If you know anything about Morrowind and leveled lists, you know how extreme of a change this is. All leveled creatures have the potential to appear at level 1. Wandering the countryside, you can encounter anything from a Kwama Forager to a Blighted Kagouti (and worse). In a tomb infested with daedra, you can run into anything from Scamps to Golden Saints, all at level 1. You never know what you'll encounter until you step out into the unknown.

Deleveler affects leveled items as well as leveled creatures. You'll now be able to find high-powered weapons, top-tier armor and more starting at level 1. You'll also find more shit-tier garbage at high levels, rather than being inundated with more high-level stuff than you know what to do with.

In short, Morrowind becomes more random, and you won't feel safe anymore wandering away from town at low levels. This, combined with the inability to save on demand due to Restrictive Saving, the next mod on this list, creates a high level of tension (the good kind) in Morrowind. You'll now feel properly nervous venturing out into the world. Morrowind has suddenly become a much more dangerous place for the unprepared.

I like Deleveler because it's more realistic and random, but it does have the consequence that the world no longer levels up with you. The game starts out terrifying, with each foray into the wilderness potentially leading to your demise at the hands of a high-level monstrosity. But as you get stronger, the enemies you face do not, which means the game will gradually become easier as you level. As I said, this is a radical change, and not necessarily to everyone's tastes, so if you don't like it, skip it.

The mod has an MCM where you can disable the deleveling of each type of leveled list (creatures and items) separately, so you could, for example, have only creatures deleveled but not items. However, if you're going to use this mod at all, I recommend having both types deleveled.

## [Restrictive Saving](https://www.nexusmods.com/morrowind/mods/47584)

So far we've made the game more difficult in a number of ways, installing mods that disable exploitable game mechanics or prevent you from cheesing them too easily. But one highly exploitable mechanic remains: save-scumming.

If you want to steal an item, but people are nearby, what do you do? You quicksave, then enter sneak mode and take the item, and if you're caught, you quickload and try again, repeating as needed until you successfully take the item without being seen. If you know there's a strong enemy in the next room, you save right before entering the room so if the battle fares poorly you can load your save and try again.

This mod puts an end to that sort of cheese. Restrictive Saving prevents you from saving the game under a number of conditions, with each option being configurable in the MCM. There are a multitude of options: you can disable saving in combat, or in bad weather, or when you're overencumbered, for example, or any combination of these options and more. You can even disable saving entirely, though I certainly wouldn't recommend it.

The option we're installing this mod for is "restrict saving unless resting." This option prevents autosaves unless you're resting in a bed. You won't be able to autosave if you're just waiting, or if you're resting without using a bed (though No Rest Without Beds prevents you from doing the latter anyway).

You'll also want to turn on the options to disable hardsaving and quicksaving, so you can no longer manually save (in fact, the Save option won't even appear in the options menu). With both options turned on, plus the "restrict saving unless resting" option, you'll have to find a bed in order to save.

This obviously will have a huge impact on how you play the game. It forces you to accept the consequences of your decisions (unless you're willing to go back to the last time you were able to rest). It adds a certain tension to the playing experience when you know that one wrong move can cause you to lose 20 minutes of play; Morrowind suddenly feels like a more foreboding, dangerous place. It also gives you another sorely-needed reason to rent a room in town once in a while.

And thanks to Sophisticated Save System, which we installed earlier, we now have multiple autosave slots (default 10) to cycle through, allowing us to return to a previous save in case something goes wrong.

Of course, you'll need to enable the autosave on rest option in Morrowind in-game options, as otherwise you wouldn't be able to save at all. And make sure the option to disable autosaves is turned off in the MCM as well, or, again, no saving at all. I recommend all the other save-restricting options (no saving in inclement weather, or unless grounded, and so on) be turned off.

You might also want to go ahead and disable the "Enable Messages" option as well. Otherwise, you'll be told "you cannot save" every time you wait, which I find distracting.

There's definitely one good reason not to use this mod: if you have problems with the game crashing. This mod itself won't cause crashes, but if the game sometimes crashes on you, this mod will prevent you from saving frequently to compensate. If you experience crashes more than very rarely, then don't use this mod.

# Fixing Conflicts

After all that work, we're finally done installing mods. However, there are still quite a few conflicts remaining to be resolved, that otherwise would result in undesired behavior.

The overwhelming majority of these conflicts will be fixed by creating our Multipatch and Merged Objects plugins, but there are likely to be a few more that will require more directed intervention.

## Install Order

The first step is to check our final install order (on the Installers tab in Wrye Mash), to make sure there are no problems. Not everything conflicts with everything else obviously, but where two or more mods each contain different versions of the same file, install order is important. For example, we wouldn't want one mod's shitty textures to overwrite the much better textures of an earlier mod.

Below is my final install order, after having installed all the mods on this list, including optional mods (click the "Install Order" label to expand):

<details>
<summary>Install Order</summary>

```
Original Data Files
MGE XE Data Files
Patch for Purists
Texture Fix
Texture Fix - Bloodmoon
Cinia
Dubdilla Location Fix
Bloated Morrowind Magnified
Under Construction
Unofficial Morrowind Official Plugins Patched
Better Propylon Teleport Script
Particle Arrow Replacer
Area Effect Projectiles Integrated
Expeditious Exit
Memory Monitor
Quick Char
Continue
New Game Confirmation
Sophisticated Save System
Right Click Menu Exit
UI Expansion
Smart Journal
Hot Quests
Book Worm
Shrine Tooltips
No Thank You
Essential Indicators
Security Enhanced
Torch Hotkey
MWSE Hide the Skooma
Rational Names
Clock Block
HUD Weapon Charge
Controlled Weapon Enchants
No Auto Vanity Camera
Assetless No Glow
No Shield Sparkle
Just Drop It
Character Creation Name Generator
What Are My Attributes?
Class Description Tooltip
Better Dialogue Font
Better Daedric Font
Title Screen Reworked
Widescreen Splash Replacer
Widescreen Splash Additions
Crosshair Pack II
Alternate Enchanted Item Icons
Ultimate Icons Replacer
HD Intro Cinematic
Cutscenes Revamped - Cavern of the Incarnate
Prince of Moonshadow
Prince of Moonshadow Fix
Creature VFX Restoration
Correct UV Rocks
Morrowind Optimization Patch
Moar Meshes
Moar Meshes - Extra
Moar Meshes - Patches
RR - Better Meshes
Glowing Flames
Properly Smoothed Meshes
Properly Smoothed Meshes - Flask Fix
Dwemer Mesh Improvement
Telvanni Mesh Improvement
Overlooked Meshes Replacer
Ingredients Mesh Replacer
Dunmer Lanterns Replacer
Robert's Bodies Pluginless
New Beast Bodies Pluginless
Westly's Pluginless Head and Hair Replacer
Westly's Head and Hair Replacer - Various Fixes
Pluginless Khajiit Head Pack
Pluginless Khajiit Head Pack - Vampires
Weather Adjuster
MGG Shaders Skyrim-Style
MGE XE Shader Pack Rev2
MGG Weathers Darker Nights
Enhanced Water Shader
Let There Be Darkness
True Lights and Darkness - Necro Edit
Waterfall Lights Remover
Light Decay
The Midnight Oil
Intelligent Textures
Papill6n Various Graphics Things
Seamless Papill6n Bedrolls
Soulgem Ingredient Retexture
Improved Bread Mesh and Texture
Throbbing Meat
Daedric Intervention - Ingredients
Darknut's Weapons Complete
Darknut's Armor Textures
Touched Up Ringmail
Dark Brotherhood Armor Replacer
Hirez Armors Native Styles v2 Fixed and Optimized
Armors Retexture Outlander Styles
Darknut's Creature Textures
Darknut's Creature Textures - Addendum
Glowing Atronachs
Divine Dagoths
Better Clothes Complete
Better Clothes Retextured
Better Clothes Robert's Bodies Patch
Better Robes
Robe Overhaul
Blank Glowmaps for Robe Overhaul
Vivec God Replacement
Better Almalexia
Skies .IV
Arukinn's Better Books and Scrolls
MWSE Daleth's Book Jackets (Core Assets only)
Melchior's Magnificent Manuscripts
Enchanted Library 2.0
Enchanted Library 2.0.1 Hotfix
Vurt's Hi-Res Menubook
Pete's Scroll
Old Dwemer Books
Bookart Replacer
New Guar Cart Mesh and Textures
Ashlanders Textures
HQ Bug Shells
HQ Bug Shells Vanilla Color Tweak
HD Forge
HD Bloodmoon Forge
Articus 6th House Dagoth
Vanilla Land
Vanilla Land Crackedearth Fix
Bitter Coast Scum Replacer
Vanilla Friendly Scum Texture
Swamp Rocks Brown
Dangerous Lava and Oil
Ultimate Dunmer Strongholds
Articus Old Stucco 2k Retexture
Ministry of Truth (not) Bump Mapped
Sewers Arkitektora - Dirty HQ
Articus Clockwork City 2k Retexture
Daedric Intervention - Ruins
Set in Stone
Better Head Statues
Full Dwemer Retexture
Hlaalu Arkitektora Vol 2
Hlaalu Retexture
Imperial Ordo Arkitektora
Imperial Door Fixes
Articus Old Mournhold and Sewers Retexture 2k
Raven Rock HD
Shacks Docks and Ships Arkitektora
Cavern of the Incarnate Retexture
Glowing Bitter Coast
Comberry Bush and Ingredient Replacer
Fire Fern Replacer
Hackle-lo Fixed
Kwama Eggs and Sacs Replacer
Lichen Retexture
Underwater Static Replacer
Vurt's Tree Textures Overhaul
Bark Again
Bitter Coast Redux - Vanilla Trees HD
Bitter Coast Redux - Flora HD
Dunmeri Urns
Dunmeri Urns Non-Bump Mapped Fix
Apel Sacks
Better Crates
Glow in the Dahrk
Graphic Herbalism
Project Atlas
Graphic Herbalism Patches and Replacers
Graphic Herbalism Lighting
Smoothed Marshmerrow for Graphic Herbalism MWSE
Graphic Herbalism Ash Yam Collision Switch
Vanilla-Based Ash Grasses
Vanilla-Based AI and BC Grasses
Articus Mournhold 2k Retexture
Redoran Arkitektora Vol 2 - Buildings
Redoran Arkitektora Vol 2 - Ald Skar
Silverware Repolished
Silverware Repolished - HD Clutter Atlas Texture
Telvanni Arkitektora
Tyddy's Telvanni Fixes
Vivec and Velothi Arkitektora Vol 2
Better Rugs - Worn
Glory to the Empire
Dunmer City Banners
SWG's Signs
Septim Gold and Dwemer Dumacs
Swappable Texture Signposts
Articus Immersive Crystals
Illy's Bedspreads
Improved Better Skulls
Skeletons Atlased
One True Faith
Articus Various Retextures - Soulgems
Articus Various Retextures - Water Pools
Various Retextures and Replacers - Blood
Skeleton and Metal Sparks Blood Retexture
Better Waterfalls
Vivec Palace Water Replacer
Subtle Smoke
Dwemer Plans and Schematics
HD Clutter
Long Live the Plates
Skiff Boat Texture Replacer
Lightning Ghostfence Hi Res
Fire Retexture
Fire Retexture Clipping Fix
R-Zero's Quill
Distant Mournhold
The Dream Is the Door
Remiros' Groundcover
Moar Meshes Patches - Atlas Patch
Intelligent Textures Atlas Textures
Vivec and Velothi Arkitektora Atlas Texture
Redoran Arkitektora Vol 2 Atlas Texture
HD Clutter Atlas Textures
Atlas Texture Collection
Glass Domes of Vivec
Glass Domes of Vivec Moonrain Edition
Atmospheric Sound Effects Expanded
MUSE
MUSE - Necro Edit
Better Music System - MUSE Version (with music)
Magicka Expanded (Framework)
Enhanced Detection
Enhanced Detection (Less) Lite
Map and Compass
Map Replacements
Fortify MAX
Class-Conscious Character Progression
Quest Skill Reward Fix
Magicka Based Skill Progression
Nimble Armor
Expansion Delay
Early Transport to Mournhold
Hospitality Papers Expanded
Expansions Integrated
Creeping Blight - MWSE Version
Dynamic Timescale
Lua Lockbashing
Hold Your Breath
Immersive Run Fix
Wading in Water
Realistic Movement Speeds
Reduced Forward Jump
Wings of Will
A Sinking Feeling
Alchemical Knowledge
The Publicans
Great Service
Religions Elaborated
Improved Temple Experience
Divayth Fyr Puzzle Fixed
Consistent Enchanting
Randomized Chargen
Economy Adjuster Adjustments
HardTrade
Ownership Overhaul
BTB's Game Improvements - Necro Edit
Balanced Passive Races and Birthsigns
Morrowind Anti-Cheese - BTBGI Compatibility
Better Character Classes
No Rest Without Beds
No Beds for the Diseased
No Disease Labels
Enchanted Weapon Resistance
Service Requirements Lore
Tribunal Rebalance
Bloodmoon Rebalance
Beware the Sixth House
More Deadly Morrowind Denizens
There Can Be Only One
Helm of Tohan BTBGI Patch
TCBOO Expansions Integrated Patch
Sigourn - Ownership Overhaul Patches
Sigourn - MDMD Patches
BTBGI Necro Edit Modular Patch
Bloodmoon Rebalance PFP Patch
Blighted Blight
Equipment Requirements - Necro Edit
Armor Rating
Sneaky Strike
Locks and Traps Detection
Stealth Improved
MAB0's Foundations
MAB0's Manipulated
Controlled Consumption MMC Edit
Silver Tongue
Putting Power in Willpower
DragonDoor
Dungeons Rest
Limited Leaping
Limited Intervention
Limited Recall
Naked and Alone
Worth Its Weight
Skills Module
Ashfall
No Combat Menu
No Console
One Life to Live
Deleveler
Restrictive Saving
```
</details>

If you've followed this list exactly, installing all of these mods in the order presented (except when specifically instructed to place a mod elsewhere in the installers list), your install order should be the same as mine. If not, check for any undesired conflicts, and adjust install order as needed (and anneal in Wrye Mash afterward of course).

## Load Order

Load order of plugins (on the Mods tab in Wrye Mash) is even more important than install order, as in the case of conflict between plugins, the last one in the load order will take precedence.

Merged Objects will fix most conflicts, but setting the load order correctly can itself resolve some conflicts or at least ensure that the desired mod ends up the winner. For example, BTB's Game Improvements and Tribunal Rebalance both edit the Dark Brotherhood armor. I think it's better for the edits in Tribunal Rebalance to take precedence, which means Tribunal Rebalance should come after BTBGI in the load order to ensure it wins the conflict.

We've already installed all our plugins, except for the final patches we'll be creating. Here is a good load order for the mods on this list, including optional plugins (click the Load Order label to expand):

<details>
<summary>Load Order</summary>

```
Morrowind.esm
Tribunal.esm
Bloodmoon.esm
Patch for Purists.esm
Ownership Overhaul.esm
Texture Fix 2.0.esm
Texture Fix - Bloodmoon 1.1.esm
Patch for Purists - Book Typos.ESP
Patch for Purists - Semi-Purist Fixes.ESP
Lake Fjalding Anti-Suck.ESP
master_index.esp
EBQ_Artifact.esp
Better Propylon Teleport Warp-Master Index.esp
Area Effect Projectiles Integrated (PAR Edit).esp
AtmosphericSnd+ExpandedSnd-3.5-NoMusic.esp
Dubdilla Location Fix.ESP
Under Construction.esp
Cinia.esp
Expansion Delay.ESP
Early Transport to Mournhold.esp
Quick Char (Necro Edit).esp
Glowing Atronachs.esp
Better Clothes Complete.ESP
Better Robes.ESP
DM_DB Armor Replacer.esp
Better_Typography_Bookarts_Fix.ESP
Old_dwemer_books_Better_typography.esp
correctUV Ore Replacer_fixed.esp
ST_Signposts_Environs.esp
Hospitality_Papers_Expanded_v2.7.esp
No Thank You.esp
Religions Elaborated.ESP
Improved Temple Experience.ESP
The Publicans.ESP
No Beds for the Diseased.ESP
Great Service.ESP
Mournhold LOD.ESP
Divayth Fyr Puzzle Fixed.ESP
The Dream is the Door.ESP
Bloated Morrowind Magnified.esp
Reduced_Forward_Jump.ESP
Service Requirements Lore.esp
Naked and Alone.esp
Better Character Classes.esp
Glass Domes of Vivec_atmospheric arena.esp
Glass Domes of Vivec_atmospheric arena Ownership Overhaul Patch.ESP
Expansions Integrated.esp
MDMD - More Deadly Morrowind Denizens.ESP
MDMD - Creatures Add-On.ESP
MDMD Expansions Integrated Patch.ESP
There Can Be Only One (Alt Fyr 2).esp
There Can Be Only One Expansions Integrated Patch.ESP
There Can Be Only One (Alt Fyr 2) MDMD Patch.esp
BTB's Game Improvements (Necro Edit).esp
Balanced Passive Races and Birthsigns.esp
BTBGI PFP Patch.esp
BTBGI MDMD - Creatures Patch.ESP
Morrowind Anti-Cheese Tweaked.ESP
tribunal rebalance.ESP
Bloodmoon Rebalance.esp
Beware the Sixth House.ESP
avp BTBGI-NE - Better Clothes Complete.esp
avp BTBGI-NE - Better Robes.esp
avp BTBGI-NE - tribunal rebalance.esp
avp BTBGI-NE - Bloodmoon Rebalance.esp
avp BTBGI-NE - Beware the Sixth House.esp
avp BTBGI-NE - Game Settings - More Meaningful Encumbrance.esp
avp BTBGI-NE - Game Settings - Suggested Tweaks.esp
Bloodmoon Rebalance - PFP.esp
EcoAdjCrime (Necro Edit).esp
TheMidnightOil.ESP
Ashfall.esp
Waterfall Lights Remover.esp
TLAD Daylight - No Vivec Plazas.esp
```
</details>

Of course, not every plugin conflicts with every other, so there are many variations of the above that are just as good, but just to be safe you might as well go ahead and adjust your load order in Wrye Mash to match mine. (I've already done the work of checking out conflicts in tes3view to determine the proper load order.)

Also, if you have plugins listed on the Mods tab in Wrye Mash that you're not using, you might want to get rid of them now (just uncheck any plugins you're not using in the Installers tab for each package and anneal). This minimizes confusion and the possibility of selecting the wrong plugins in MGE XE distant land generation, for example, or tes3view, or the Construction Set. The only plugins we're not actually using in-game that should still be installed are the seven grass plugins of Remiros' Groundcover (we need those for distant land generation).

## tes3cmd and the Multipatch

The first major step we'll be taking here is to use tes3cmd to clean our plugins and create our multipatch. (Don't worry, we don't need to use the command line for this; I'm assuming you followed the instructions earlier to install tes3cmd and ensure it can be invoked from within Wrye Mash.)

First things first: cleaning our plugins. tes3cmd can clean any plugin file, including .esm files, except for the Bethesda masters. *Many* plugins are unclean in one way or another, meaning they have references that are identical to those in their master files, and therefore unneeded. Dirty plugins can result in conflicts or unintended behavior.

There are some mods that have plugins that intentionally include references identical to those in their masters (for example, to ensure that other mods don't modify the masters' references because doing so would break the mod), and should therefore not be cleaned. There's only one such mod on this list: Patch for Purists.esm, which intentionally contains one "dirty" reference. Be sure not to clean this file (though if you do accidentally clean it, you can always reinstall PFP from the Installers tab in Wrye Mash to get the original file back).

Any plugins cleaned will be different than the version that's in the installers, which means the installer's checkbox will display in orange on the Installers tab. This is fine, but if you ever for some reason reinstall one of these mods, the original, dirty version of the plugin will be installed, and you'll need to clean it again.

To clean your plugins, select every plugin on the Mods tab (except for the three Bethesda masters and Patch for Purists.esm). You can hold down the shift key while clicking to easily select them all at once. With all the plugins selected, right click on one of them and select "clean with tes3cmd". tes3cmd will now examine and clean all of your plugins, which will take quite some time to complete. (Most plugins will not be modified by this process because they're already clean, but you might as well clean them all just to be sure.)

The second major thing we need to do with tes3cmd is to create a plugin called multipatch.esp. The multipatch does a number of things, the most obviously beneficial of which is to merge changes to leveled lists contained in your plugins. For example, if plugin1 adds items A and B to a certain leveled list, and plugin2 later in the load order adds items C and D to that same leveled list, only items C and D will actually be added in-game, because the last plugin in the load order overrides the earlier one. The multipatch merges these changes, in this case adding all four items to the leveled list.

The multipatch also solves a few additional issues, such as fixing any cells subject to the "fog bug" (which can cause a completely black display under certain circumstances).

You should be using the latest version of tes3cmd, 0.40 alpha2, as I advised much earlier in this list. The alpha version handles items being *removed* from leveled lists better than the older version does, and there is a mod on this list that removes items from leveled lists.

To create the multipatch, make sure all plugins you'll be using are enabled in Wrye Mash's Mods tab, then select Misc -> tes3cmd -> create multipatch. After it's done, enable "multipatch.esp" on the Mods tab, which should be at the end of your load order.

For more details regarding what tes3cmd is doing here, run the following commands on the command line:

```
tes3cmd help clean
tes3cmd help multipatch
```

## tes3view and Checking the Multipatch

With the old version of tes3cmd (0.37v), the multipatch did not handle leveled list merging in the best way when items were removed from lists, and it was necessary to manually edit the multipatch to fix a few lists. With the newer tes3cmd version (0.40 alpha2), this step should not be necessary if you're following this list, since this version of tes3cmd handles this situation much better.

However, I still recommend checking out the multipatch and making sure everything looks okay, just in case. Our task now is to pull up our load order in tes3view (which we installed way back at the beginning of this process) and examine the edits in multipatch.esp to make sure everything's kosher.

When you start the program, on the plugin select screen, right click and "select all," then uncheck any you're not using (which ideally should be just the Remiros' Groundcover plugins). It'll take a minute (not very long really) to load your plugin list.

From here, you can expand the plugins on the left to view their records. You can also narrow down the list by right clicking somewhere on the plugin list and selecting "filter to show conflicts." The filtering process might take a few minutes, but when it's done only plugins and records that have conflicts with others will be shown.

Don't bother with the filtering though, since the multipatch won't have too many records in it, and we want to examine them all anyway. Go through all the records in multipatch.esp, one at a time, and examine them to make sure everything looks as expected.

Following this list, and using the latest tes3cmd to generate the multipatch, I discovered no problems, but if you see anything that doesn't look right, you'll need to manually edit multipatch.esp in either the CS or Enchanted Editor to fix it.

## tes3merge and Merged Objects

This is the most important step we can take to resolve conflicts; Merged Objects will fix the great majority of them.

Most of the mods on this list are compatible with each other, but there are still quite a lot of conflicts - mostly small, but some not - between them. The importance of these conflicts varies, but you can use tes3view to check them out.

tes3merge will scan all of your active plugins and create a new plugin called Merged Objects.esp, which contains references to all objects (such as NPCs or equipment) of which two or more mods make conflicting edits. These references contain all of the edits of the various plugins which modify these objects.

To run tes3merge, make sure all plugins you'll be using are enabled in Wrye Mash's Mods tab (including multipatch.esp), then either double click tes3merge.exe in your tes3merge directory, or run the command on the command line. In addition to creating Merged Objects.esp, it will also generate a log in your tes3merge directory which you can check to make sure everything looks right.

Don't forget to activate Merged Objects.esp on the Mods tab in Wrye Mash. It should be at the end of your load order, after multipatch.esp.

## Merged Objects Fixes

We're almost done. Merged Objects, like the multipatch, is essential, but it doesn't handle everything perfectly, and there are likely to be additional problems that we haven't fixed yet.

Pull up your load order in tes3view again and examine the edits in Merged Objects.esp for any problems. You can also filter to show conflicts and examine the conflicts in your other plugins to find records that Merged Objects doesn't address but should (and I found something to fix this way).

Using the load order from this list, I encountered three additional problems that require fixing. If you're using different mods, different versions of mods, or a different version of tes3merge, you might notice more, fewer or different problems than I do. That's why you should check for yourself.

The three problems that I encountered in Merged Objects, and how to fix them, are as follows:

### Sjoring Hard-Heart

Merged Objects makes a couple of unusual edits to Sjoring, and there's no conflict with him to fix anyway. The only plugin on this list that touches him is MDMD, and its edits are perfectly fine.

The edits Merged Objects makes to Sjoring are problematic, and this issue is somewhat important.

Fortunately, it's easy to fix. To do so, open up Merged Objects.esp in Enchanted Editor and just delete the reference to Sjoring. Easy peasy.

### Ash Feast

There's a spell called "Ash Feast" used by some Sixth House enemies. BTBGI changes the spell's effects and removes the autocalc flag. Beware the Sixth House changes the effects again and halves the magicka cost from 18 to 9, while keeping the autocalc flag. Alvazir's patch for the two mods restores the spell to the BTBGI version (which I think is best), but Merged Objects pulls in the lower magicka cost from Beware the Sixth House, which would mean the spell is only half as expensive as BTB intended.

To fix this, delete the reference to this spell from Merged Objects in EE.

### Dark Brotherhood Masks

Dark Brotherhood Armor Replacer adds the "Dark Brotherhood Mask" (which is a clothing item, not a piece of armor) to the DB assassins, but Merged Objects omits it from a couple of them.

This issue is not particularly important. But I can be pretty anal about some things (okay, maybe a lot), and, like Goldilocks, I want everything in my Morrowind to be "just right."

Unfortunately, this issue is not as easy to fix as the last one. The easiest way to fix this one is to use the Construction Set. In the CS, select all of Merged Objects' masters in the plugin list (Merged Objects' masters include every plugin in your load order with records that it modifies), along with Merged Objects itself. Do not select an active plugin - we'll be creating a patch for Merged Objects.

Once Merged Objects and all of its masters are loaded, add the clothing item "Dark Brotherhood Mask" (quantity 1) to the following NPCs:

- db_assassin3
- db_assassin3a

Note that one of these was not even edited by my Merged Objects at all; I wouldn't have even noticed this error (until seeing it in-game) if I hadn't manually checked all my conflicts in tes3view.

Now save your plugin (I call it Merged Objects Patch). This patch plugin should load *after* Merged Objects (don't forget to clean it).

# Wrapping Up

Whew, this sure has been a long process. There's actually one last thing we can (maybe) do to possibly improve appearance and/or performance, but otherwise we're done.

## Nvidia Graphics Settings

If you have an Nvidia graphics card, there are a number of settings that can be tweaked in the Nvidia Control Panel (NVCP) which can improve the appearance and performance of games generally. Only a few of these have the potential to improve the Morrowind experience, but it's worth experimenting with them to see.

However, this is completely optional. Morrowind looks fine with our MGE XE settings without bothering with tweaking Nvidia settings, and if you don't feel like messing with this, feel free to skip it.

This discussion is based on the [Nvidia Tweak Guide](https://web.archive.org/web/20191028152332/https://www.tweakguides.com/NVFORCE_1.html). The full guide is well worth reading, though we'll only cover a few specific settings here. This discussion is specifically for Nvidia graphics cards, but if you have an AMD card you should be able to find similar settings in your AMD software.

To test out these settings, you'll need to load the game without the setting activated, then load it again with the setting activated and compare them. Taking before and after screenshots (from the same position) can help. Turning on MGE XE's FPS display can also be useful here.

Before we begin, you should make sure you have the latest Nvidia drivers installed. The tweak guide linked above has very detailed instructions for upgrading your drivers.

On the Nvidia Control Panel's "Manage 3D Settings" page, which is where all the important settings are, there are two tabs. The Global Settings tab controls settings that apply universally, to all applications, while the Program Settings tab allows you to change settings for individual applications. I suggest leaving the Global Settings alone, and only changing settings for Morrowind specifically on the Program Settings tab.

The specific settings that might have an impact on Morrowind's appearance or performance include:

### Anisotropic filtering

This is the same as the AF setting in MGE XE, and you should currently have this set in MGE XE to 16x, or as high as your graphics card allows. AF improves the clarity of the game's textures, making them appear sharper and more detailed.

The only choice to be made here is whether we want AF to be controlled by MGE XE, or by NVCP. To enable it in NVCP, set it to 16x (or as high as you can) here, and then turn AF *off* in MGE XE (having it enabled in both places can cause unspecified Bad Things to happen).

A good place to test this change is somewhere where you can see the ground texture or some other structure such as a dock stretching out away from you, where you're looking at the textures at an angle.

Enabling 16x AF in NVCP as opposed to 16x AF in MGE XE is likely to either very slightly improve appearance, or make no difference at all. It should make no difference in terms of performance (AF is not very performance demanding anyway).

### Antialiasing - Transparency

This does not replace the AA setting in MGE XE, but has the potential to enhance it. AA reduces the phenomenon of jagged lines that you might see at the edges of objects, and you should have AA set in MGE XE as high as your graphics card will allow (which for me is 8x).

The transparency setting in NVCP enhances AA with respect to textures with transparency effects, particularly foliage. To enable it, the NVCP setting should be set to the same level as you have AA set in MGE XE. So, for example, if AA is set to 8x in MGE XE, you should enable 8x (supersample) transparency AA in NVCP. Leave the AA setting in MGE XE alone; you want it enabled in both places, as the NVCP setting merely enhances the MGE XE setting.

The best place to test this change is near trees or other foliage.

For me, enabling 8x (supersample) transparency AA here on top of the 8x AA already enabled in MGE XE had a relatively small but noticeable impact on appearance, with less jagged edges around foliage. Note that this setting does impact performance, so if your system is struggling you might want to only enable the more basic "multisample" transparency AA here, or just skip this one entirely.

### Multi-Frame Sampled AA (MFAA)

Like the previous setting, this one also enhances (does not replace) the AA setting in MGE XE. As the Nvidia Tweak Guide says, this setting basically increases your AA by one level (say, from 4x to 8x, or from 8x to 16x), improving visuals at no cost to performance.

This should definitely be enabled in NVCP (in addition to your AA setting in MGE XE, and possibly the transparency AA setting above). For me this also resulted in noticeable improvement in appearance.

### Power management mode

This setting determines whether your graphics card will lower its performance output when it's not being stressed in-game, or whether it will always churn out maximum performance regardless of load.

Setting this to "prefer maximum performance" might possibly improve performance and reduce stutter in-game, but will probably have no effect.

### Texture filtering - Anisotropic sample optimization and Trilinear optimization

These two settings can be used to optimize the game's texture filtering in ways that might provide small performance improvements, but probably won't. Both NVCP and the tweak guide say that turning these settings on might result in a small loss of visual quality, but on my system I actually see a small improvement in visual quality with both of these options turned on. Experiment with it though.

### Vertical sync

This is the same as the vsync setting in MGE XE. It synchronizes the game's frame rendering to your monitor's refresh rate, which has an impact on performance but eliminates tearing. The Nvidia Tweak Guide has much more information about vsync (with links to even more information).

I have zero tolerance for tearing, so I always enable vsync. The choice here is whether to enable vsync in MGE XE, or in NVCP (you could also try "adaptive vsync" in NVCP, but I didn't have much luck with it, and still experienced tearing). If you want to enable vsync in NVCP, set it to on here, and then you can turn it off in MGE XE.

Having vsync turned on in NVCP, as opposed to having it turned on in MGE XE, will have no impact on appearance, and should have no impact on performance either, though it could conceivably result in a very small performance improvement.

-----

Mucking around with the other settings is unlikely to have any good effect in Morrowind, but I do recommend reading the whole tweak guide; there's some good stuff in there.

## Last Words

And that's it. We're done. (Well, almost done. Don't forget to regenerate distant land in MGE XE one more time before you start playing.)

The process we've just been through to *prepare* to play Morrowind is almost as much of an epic journey as the game itself. (And writing this list certainly has been.)

Feel free to contact me on Discord (Necrolesian#9692) or [the Nexus](https://www.nexusmods.com/morrowind/users/70336838) with any feedback, questions, suggestions or insults.

In the meantime, say hi to that old sugar-tooth Caius for me.

-----

The ending of the words is ALMSIVI.
