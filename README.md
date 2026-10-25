# Better-RA2
WIP

General Changes:
TeamDelays are fixed in all applicable missions so that it isn't reversed. Hard is hard and easy is easy!

Allied 1:
- fixed the shallow pavement bridge
- fixed the incomplete road intersection at 44,38
- reoriented Patriot Missiles
- fixed the cliff ramp near the Statue of Liberty
- fixed some non-homogenous bridge celltags
- added the cut Kirov airship
- switched player-owned lamp posts to Civie1 house
- added a cut low power text warning for the player
- reordered IDs across the map
- re-tiled all water surfaces
- statue of liberty GIs are now LightBlue colored
- implementation fixes

Allied 2:
- Adjusted celltag positions for Tanya's swim hint trigger to minimize chance of it not triggering properly
- Added 5 in-game seconds of delay to the mission loss screen when triggered by Tanya's death so that the EVA voicelines don't get jumbled together
- Changed lightposts owned by the player's house (Americans) to Civilian/Neutral so that Tanya won't die when the player orders her to area-guards on top of the lightposts

Allied 3:
- Fixed TeamDelays.
- Gave Pistola's to CIVSF, CIVSFM, CIVSTM.
- Removed the Lightpost in front of the beacon and instead made the beacon emanate the red light itself. 
- A CAWASH05 left of the Tech Hospital is now damaged, discovering it will fire the building repair hint.
- Added abandoned tanks inbetween the Smithsonian Castle and Smithsonian National History Museum, discovering these vehicles will play the unused "You have salvaged units abandoned after the Soviet invasion." string

Allied 4:
- fixed intro EVA interruption by input unlock
- slight adjustment to team delays (buffed enemy)
- re-add cut V3 EVA warning
- fixed offmap soviet conyard from being visible
- adjusted intro destroyers formation
- re-oriented some defenses
- remapped water tiles
- reordered IDs across the map
- improvements to CIVBFM dummy

Allied 5:
- Replaced Russian Flags with Polish Flags to fit the narrative that this mission takes place at the German-Polish border
- Modified Spy reinforcement loop so that every 4th reinforcement is preceded by Tanya cussing the Player out. (Modified related voiceline timings so that the voiceline doesn't get interrupted)
- Reworked Spy reinforcement loop logic so that the player can now use them to infiltrate War Factories, Barracks and Refineries for their respective bonuses
	- Side effect 1: if the Spies are killed for whatever reason immediately after they get off the Night Hawk (i.e. before they begin flashing), then the trigger loop breaks and no more Spy reinforcements are delivered. However given that this should never happen unless the Player kills their own Spies, this is considered acceptable behaviour.
	- Side effect 2: the Night Hawk has been modified to be Unselectable and provide no vision to accommodate for the trigger. Given that the player never gets them in this mission however, this is considered acceptable.
	- Side effect 3: this complicates the trigger setups related to Battle Lab and Nuke Silos. The corresponding trigger logics have been reworked to accommodate the change with additional QoL. (see below)
		- Changed the Battle Lab objective to allow the player to capture it to progress the mission, unlike in Vanilla where capturing it fails you the mission despite EVA's follow-up voiceline not making any sense.
		- Added 1 in-game second delay to Nuke 1 Destroyed, Nuke 2 Destroyed, Nuke 1 Captured, Nuke 2 Captured, to accommodate reworked Spy setup
		- Modified Nuke Silos to no longer be spyable since doing so was pointless and never affected the mission outcome in any meaningful way.
- Added an extra reveal when the player discovers the crash-landed units to make them easier to spot
	- This repositions and uses waypoint 25, which wasn't used for anything else before this
	
Allied 6:
- Changed defense building orientations so they don't all face the 0° direction.
- Changed the Tech Hospital's colour to grey to reflect other missions.
- Changed Attk_V3_2 AITrig's Comparison Object from AMRADR to GAAIRC, the AI should build it now.
- Made all the Civilian Panic celltags contiguous, you cannot enter the panic zone without triggering the civilian panic sequence now.
- The enemy will now attack the Pentagon, losing the Pentagon will fail the mission. 
- Losing the base around the Pentagon BEFORE completing Objective 1 will fail the mission.

Allied 7:
- removed the exploitable sentry gun and turned it into a basenode
- changed the win condition so that it requires the soviet MCV to deploy before everything else is accounted for
- changed Civie1 house color to Grey
- re-oriented some defenses
- remapped water tiles
- reordered IDs across the map
	
Allied 8:
- Added triggers to properly sell Psychic Beacon when captured by player-built Engineers
- Added Elite abilities to Engineer so that it now benefits from Elite veterancy (faster, self-healing)
- The player can now build the American version of the Air Force Headquarters, as intended. This also fixes AITriggers that depend on the player owning an American Air Force Headquarters
- End-of-game fire sale now also fire sale BadGuy2's buildings, in addition to BadGuy1

Allied 9:
- Made Paratroopers fall down much quicker, making the beginning cutscene drastically shorter.
- Added the unused EVA Seal introduction to the beginning cutscene. 
- Fixed the buggy Flak Track spawning scripts.
- Changed Mayanprism to MayanPrism, the Mayan Prism Cannon thusly gets an 18 range buff.

Allied 10:
- changed the win condition so that it requires the soviet MCVs to deploy before everything else is accounted for
- added a win condition that's enabled after 360s have passed
- readded the polar bear easter egg
- retiled some excessively snowy areas, high altitude areas remain the same
- made some celltags slightly more robust
- fixed a broken cliff and fixed broken road tiles
- remapped water tiles
- reordered IDs across the map

Allied 11:
- Reworked bridge fixer Engineer teams so that it no longer infinitely spawns from Seals blowing up nothing
	- Side effect 1: a 60 in-game seconds delay is added to the enemy Engineer team that spawns in
- Fixed misaligned and nonsensical basenodes for BayGuy2
- Re-oriented facings of defenses to make them appear more natural
- Re-implemented the Spy hint trigger, which now takes place 20 in-game seconds after Romanov's speech finishes

Allied 12:
- Repurposed BadGuy2 as a new Soviet AI, all of BG2's units and tesla coils and power plants at the start of the mission now belong to Other3 which now shares the same colour as BG2. BG2 owns the base to the west, and was given a Radar Tower and a Battle Lab as well as one of the Nuclear Reactors in the east.
- Added more AIT's, all of these use unused Soviet teamtypes.
- Added a "Soviet supply depot detected" string once you approach the only Tech Outpost on the map.
- Players can now build Tesla Tanks if they capture the Soviet bases.
- Added some unused voicelines meant to play after the units teleport.
- Added the unused EVA Kirov introduction speech.
- 700 seconds into the basebuilding part of the mission Soviet reinforcements will arrive and an unused EVA speech will remark on that, 200 seconds after the first wave another will arrive only on medium and hard.
- Fixed the water tiles on the map, now it does not all look uniformly the same.
- Once Tanya enters the Kremlin, an unused "Romanov captured." voiceline will play.
- Implemented LineTrailColorOverride properly, all missiles will now properly render as black in this mission.
- Drastically improved the Chrono countdown timing at the start, units will now appear the moment EVA after says "One."

Soviet 1:
- Added 3 Army Tents near the Pentagon that enemy GIs will garrison
	- This makes the loading screen match the actual mission more closely
- fixed a trigger that was referencing nothing
- made some celltags slightly more robust including the pentagon reinforcements
- removed a tree from the road
- trees from the pentagon parking lot are now standing on grass tiles rather than pavement
- remapped water tiles
- reordered IDs across the map

Soviet 2:
- Added a single Grand Cannon in the Allied base on Hard difficulty; There was leftover ini modifications suggesting that this building would've appeared in this mission.
- Reworked and re-implemented Vladimir's return after his initial escape. He will run away again everytime he is attacked by an enemy. However, if the player supports Vlad and keeps him unharmed, he will help destroy the Pillboxes and the Grand Cannon inside the main Allied base.
	- Re-added related text strings that went unused
- Re-implemented the unused hint trigger to construct a Naval Shipyard

Soviet 3:
- Re-implemented several unused AI Triggers and made them Hard difficulty only.
- The final defense phase has been changed and is now based on several snippets of cut content. After mind-controlling the main enemy force the player will have to fight another wave. Only after destroying this wave will the mission be won.
	- Developer's Note: For some reason we had to set BadGuy2's IQ from 1 to 0 to make the "Destroyed, All..." event condition work properly
- All enemy units in the defense phase will now come from off-map instead of miraculously appearing out of thin air on the map itself.

Soviet 4:
- changed the color of Civilian house to Grey
- changed a player owned lamp post on the map to civilian house
- fixed a broken road
- remapped water tiles
- reordered IDs across the map

Soviet 5:
- Removed the ability to "charge" the Eiffel Tower with the 2 Conscripts from the top-right Flak Track team
	- The Conscripts now simply spawn alongside the Flak Track instead of being inside it
- Re-implemented text trigger for the Ivan CarBomb hint

Soviet 6:
- Properly enables BadGuy1's production after the Korean fleet arrives
- Fixed TeamDelays changes so that enemy production properly scales with difficulty levels
- Re-added secondary text string for the Dreadnought reinforcement
- Re-enabled several AITriggers for base defense and harrier harrass
- Changed the Carrier's CanPassiveAquire ini flag to yes; this allows them to automatically target the player's ground units and buildings
- The Korean Fleet now spawns from multiple off-map waypoints instead of a single on-map waypoint so that their entrance appears more cinematic and less bizarre
- Increased Stray from 2.0 to 4.0 so that GI + transport AITeams won't have a chance to get stuck due to having too large of a taskforce.

Soviet 7:
- reoriented some player defenses
- changed the color of Other3 house to Grey
- fixed a broken road
- remapped water tiles
- reordered IDs across the map
- fixed enemy aircraft crashing on their exit waypoint

Soviet 8:
- Re-implemented the text trigger to hint at the cash bonues from destroying monuments
- Fixed the trigger to free the mind-controlled American soldiers after the Psychic Beacon is destroyed
- Re-implemented the unused harassment trigger which sends a team of flak tracks filled with infantry to attack the player on Hard difficulty
- Added a proper intro to the mission, highlighting Vladimir entering the White House and re-implementing the unused Desolator introduction voiceline by Zofia
- Added a few more groups of mind-controlled Allied soldiers to Vladimir's base to incentivize the destruction of the Psychic Beacon by the player
- Changed facings of defenses on the map to make them appear more natural
- Made the MCV immune to radiation
- Added red lighting to the Psychic Beacon for consistency

Soviet 9:
- Reverted the IFV's attack paradigm changes as it's a legacy change that is no longer necessary
- The Blackhawk's elite weapon damage is raised to 75 to match the increase in its base weapon damage
- The cyan Tech Airport and Allied Power Plant are now properly transferred to the player when captured using a mind-controlled Engineer
- Replaced the Soviet attack dogs with the Allied variant
- Replaced dummy stop sign buildings with the proper terrain object version

Soviet 10:
- reverted the Weather Controller nerf from wood to concrete armor and HP from 200 to 1000
- fixed BadGuy1's basenodes
- reoriented some defenses and units
- fixed a broken road
- remapped water tiles
- reordered IDs across the map
- fix ending softlock
- fix all broken cliffs
- remove duplicate and redundant triggers
- fix softlock lose condition

Soviet 11:
- Changed the tiles near the Kremlin so that it no longer sits awkwardly on paved road
- Adjusted facings of enemy defense structures so they look more natural
- Reworked Nuke Silo Kirov attack teams. Now, they will still continuously respawn if the Nuke Silo persists, but it doesn't happen until the previous wave is completely destroyed. Additionally, selling and rebuilding the Nuke Silo rapidly will no longer trigger repeated Kirov spawns.
	- Delayed Zofia's related Alert and Flak Cannon voicelines by 3 in-game seconds each to account for the faster speed of modern PCs (so that the voiceline doesn't get cut off)
	- Re-implemented related unused text triggers.
- Re-implemented the Yuri taunt movie.
	- A team of 3 PsiCorps Troopers will now be paradroped in front of the Orange AI base 50 in-game seconds after game initialization. When they enter combat, the Yuri taunt movie plays.
- Added an unused TeamType for the Orange enemy AI as an AITrigger. This TeamType rushes down the player with 4 Engineers inside a Flak Track

Soviet 12:
- Fixed triggers so that the repeating chrono reinforcement Prism tanks don't spawn until you reach the third ore field on the mainland
- Added a new trigger that allows the player to still obtain the Kirovs near the Tech Aiport if they build a SpySat before discovering them
- Added a text trigger that indicates when the enemy spots the player and begins AI production (since Zofia says "they will not be expecting us" in the transmission)
- Re-enabled a trigger that recruits 2 additional destroyers to attack the player when they are spotted, but changed it to be only on hard difficulty
- Reworked an obsolete AITeam to instead produce attack teams consisting of 1 or 2 Prism tanks.
	- The original name of the AITrigger was "Solar Tank", which either referred to a cut unit or the Prism tank. It asked the AI to build Tesla tanks despite them not being able to do so
- Added a repeating trigger that reminds the player to destroy the Chronosphere after they capture the Kirovs; This type of repeating reminder is commonly present in most other missions.
- Fixed a bug that caused carrier teams to not actually spawn
	- The (1 Carrier) taskforce had no units in it at all. Fixing this now causes the enemy to properly spawn a carrier when the player spots the initial beach
	- The first enemy base, BadGuy1, will now also produce Carrier AITeams properly
- Added a limited number of basenodes to enemy bases so that they will actually rebuild up to a certain degree

YR Allied 1:
- Removed unused trigger that changes units to the player's house
- Removed obsolete duplicate triggers for Harrier intro sequence, restoring Grand Cannons, and checking if the Partially-Built Psychic Dominator is destroyed
- Removed obsolete trigger that stopped a timer if the player's power goes down
	- Probably leftover from an earlier version of the map design that had the player defend their power at some point
- Reenabled a trigger playing an EVA voiceline introducing the Psychic Dominator when selected
- Reenabled a 3 unused garrison triggers
	- Tweaked actions to spawn Initiates instead of recruiting existing ones
	- Moved 1 garrison that was doubled up on the existing garrison to a building south of the introductory set of Power Plants
	- Added an eviction trigger for the existing garrison, as it was previously using the unused duplicate's eviction trigger
- Removed unused triggers creating a chain pinging different power plants across the map
	- Possibly was part of the introduction before being cut
- Fixed many triggers detecting the ownership and existence of power plants across the map
	- Not currently used for anything but would be a pain to remove from tag chains and annoying to reimplement if you wanted to extend this mission with more mechanics later on
	- Probably leftover from an earlier iteration of the map
- Added a fourth Gattling Cannon to the map linked to an unused reveal trigger
	- Reveal trigger was likely cut for being too close to introductory Power Plants
	- Moved the trigger's tags to a reasonably appropriate nearby location
	- Added triggers to display an arrow pointing to the building, complimenting similar existing triggers for other Gattling Cannons
	
YR Allied 2:
- Restored the original name and voicelines of the three Hollywood stars
- Added a group of rescuable Allied infantry near one of the Grinders
	- Rescuing them plays either an un-used voicelines or a generic GGI select voiceline, depending on whether the player did so BEFORE or AFTER they destroyed all Grinders on the map respectively
- Added a fourth hero unit that uses the modified Texan civilian's stats as an easter egg
	- This unit can be found in the mind-controlled civilian pen in the bottom right corner of the map. Clicking on him will activate the easter egg trigger
	- Added an extra ini change to make the hero immune to mind control
- Extended the intro sequence to add in the un-used Eva voicelines introducing the Slave Miner and Slaves to the player
	- There are two un-used voicelines in the files, one for the Slave Miner and one for the Slaves. Due to overlap, one of them is randomly selected each time you play the mission
	- Slightly increased the amount of ore in the starting patch to compensate for the amount consumed by the Slave Miner intro
- Added several cut voicelines to buildings in Yuri's base when the player clicks on them
- Fixed a bug where a hegdehog barricade was mistakenly assigned under the player's ownership
- Reworked the Flak Cannon method of providing the player with extra funds on Easy difficulty to instead just use CampaignMoneyDeltaEasy
- Made several Yuri units and structures that shouldn't be buildable by the player unbuildable
	- Affected technotypes: Virus, Magnetron, Mastermind, Chaos Drone, Psychic Dominator, Genetic Mutator and Yuri Prime
	- It's a clear oversight that the player is capable of constructing these things at this point of the story, especially since they all get introduced later on
- Added 3 in-game seconds of delay to Return_Control so that Eva's voicelines don't cut each other off

YR Allied 5:
- Restored the Lasher tank's TechLevel to its default value so that both the player and the AI can build it again
- Added triggers that introduce the Tech Hospital and Tech Machine Shop if the player hasn't encountered them up until this point
- Extended the intro sequence to add in the un-used Eva voicelines introducing the Cloning Vat and the Yuri Submarine Pen to the player
	- This extended sequence also spawns additional Initiates at the Cloning Vats, scaling in quantity with the difficulty level, for a better demonstration of the Cloning Vat's abilities
- Added triggers that introduce the Brute to the player using cut voicelines
	- There are two un-used voicelines in the files that both introduce the Brute. Due to overlap, one of them is randomly selected each time you play the mission
	- Added 2 extra starting GIs to compensate for the additional enemy forces spawned as a result of this
- Added 5 extra in-game seconds of guard time to the Dolphin + Destroyer team attacking the initial Boomer Sub to eliminate the rare possibility of them retreating before taking down the Boomer Sub
- Adjusted timing of multiple triggers at the beginning
	- Decreased elapsed time of Eva follow-up speech of initial sidebar movie by 4 seconds to line up the timing better
	- Decreased elapsed time of the camera moving back to the player base by 6 seconds to line up with the input unlock
- Fixed AITriggers that are conditional on the player owning an American Allied Airforce HQ, despite them only being able to build the generic Allied Airforce HQ in this mission
	- Affected triggers: (_A05_Chaos Drone), (_A05_Initiates on Airforce)
- Fixed an AITrigger that is conditional on the player owning a Soviet Barracks, despite them not being able to get one in this mission
	- Affected triggers: (_A05_Brutes (1))
- Added a reinforcement team for the player once they lose a certain amount of units on Easy difficulty
	- This trigger uses an un-used text string
	
YR Allied 7:
- Added a Magnetron introduction sequence after the Allied MCV Chronoshifts into the battlefield
	- This uses an un-used EVA voiceline to introduce the Magnetron
- Added triggers that use cut voicelines to introduce the Genetic Mutator when the player gets close to them
	- The Psychic Dominator voiceline is added in YR Allied 1 already
- Fixed the pathing of a Yuri paradrop team on Tierra Del Fuego
- Re-enabled a trigger that gives the player additional paradrop teams at the start of the mission
- Limited the MCV Chrono reinforcements to happen once at most
	- This cheese is far too overpowered in its original state, changing it brings it more in line with similar triggers in other missions, like in Escape Velocity
- Removed the singular tree on Antarctic ice

YR Soviet 2:
- Added a cut voiceline that introduces the German Tank Destroyers when they move out to attack the player
- Added a cut voiceline that introduces the Battle Bunker once the player deploys their MCV
- Added a cut voiceline that introduces the Spy Plane once the player constructs a Radar Dish
- Added a cut voiceline + sidebar movie for this mission when the player deploys their MCV
- Added "establishing battlefield control" to the start of the mission
- Added an 8 in-game second delay to the Chronosphere Transfer once its first chronoshift finishes
	- This eliminates the visual bug caused by changing the Chronosphere's house right as it fires its superweapon
- Made the Chronosphere unsellable to remove the rare possibility of the AI selling the Chronosphere and hand the player the victory
- Fixed several AITriggers that had erroneous conditions
	- For example, (Amb_MirageBR AITrig) erroneously checks whether BadGuy1 owns Apocalypse tanks instead of checking whether the player owns Apocalypse tanks. Fixing this means AI can now properly create Mirage tank ambush teams
	- Affected triggers: (Amb_MirageBR AITrig), (Amb_MirageBS AITrig), (Amb_MirageBT AITrig), (Amb_MirageBU AITrig), (Amb_MirageBV AITrig), (Amb_MirageBW AITrig)

YR Soviet 4:
- Added a flashing effect on the Tech Airport when the camera pans to it in the intro
- Extended the intro sequence by 19 in-game seconds to add a cut voiceline that introduces the Yuri Clone to the player
- Changed the Kill Light triggers so that the player doesn't see a strange explosion when the invisible light posts are turned off
- Added an un-used text string to the player reinforcements that can occur on Easy and Medium difficulty

YR Soviet 6:
- Changed the Kill Light triggers so that the player doesn't see a strange explosion when the invisible light posts are turned off
- Added a reinforcement team for the player once they lose a certain amount of units on Easy difficulty
	- This trigger uses an un-used text string
