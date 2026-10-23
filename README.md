# Better-RA2
WIP

General Changes:
TeamDelays are fixed in all applicable missions so that it isn't reversed. Hard is hard and easy is easy!

Allied 2:
- Adjusted celltag positions for Tanya's swim hint trigger to minimize chance of it not triggering properly
- Added 5 in-game seconds of delay to the mission loss screen when triggered by Tanya's death so that the EVA voicelines don't get jumbled together
- Changed lightposts owned by the player's house (Americans) to Civilian/Neutral so that Tanya won't die when the player orders her to area-guards on top of the lightposts

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
	
Allied 8:
- Added triggers to properly sell Psychic Beacon when captured by player-built Engineers
- Added Elite abilities to Engineer so that it now benefits from Elite veterancy (faster, self-healing)
- The player can now build the American version of the Air Force Headquarters, as intended. This also fixes AITriggers that depend on the player owning an American Air Force Headquarters
- End-of-game fire sale now also fire sale BadGuy2's buildings, in addition to BadGuy1

Allied 11:
- Reworked bridge fixer Engineer teams so that it no longer infinitely spawns from Seals blowing up nothing
	- Side effect 1: a 60 in-game seconds delay is added to the enemy Engineer team that spawns in
- Fixed misaligned and nonsensical basenodes for BayGuy2
- Re-oriented facings of defenses to make them appear more natural
- Re-implemented the Spy hint trigger, which now takes place 20 in-game seconds after Romanov's speech finishes

Soviet 2:
- Added a single Grand Cannon in the Allied base on Hard difficulty; There was leftover ini modifications suggesting that this building would've appeared in this mission.
- Reworked and re-implemented Vladimir's return after his initial escape. He will run away again everytime he is attacked by an enemy. However, if the player supports Vlad and keeps him unharmed, he will help destroy the Pillboxes and the Grand Cannon inside the main Allied base.
	- Re-added related text strings that went unused
- Re-implemented the unused hint trigger to construct a Naval Shipyard

Soviet 5:
- Removed the ability to "charge" the Eiffel Tower with the 2 Conscripts from the top-right Flak Track team
	- The Conscripts now simply spawn alongside the Flak Track instead of being inside it
- Re-implemented text trigger for the Ivan CarBomb hint

Soviet 6:
- Properly enables BadGuy1's production after the Korean fleet arrives
- Removed TeamDelays changes so that enemy production properly scales with difficulty levels
- Re-added secondary text string for the Dreadnought reinforcement
- Re-enabled several AITriggers for base defense and harrier harrass
- Changed the Carrier's CanPassiveAquire ini flag to yes; this allows them to automatically target the player's ground units and buildings
- The Korean Fleet now spawns from multiple off-map waypoints instead of a single on-map waypoint so that their entrance appears more cinematic and less bizarre
- Increased Stray from 2.0 to 4.0 so that GI + transport AITeams won't have a chance to get stuck due to having too large of a taskforce.

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
	
YR Allied 7:
- Added a Magnetron introduction sequence after the Allied MCV Chronoshifts into the battlefield
	- This uses an un-used EVA voiceline to introduce the Magnetron
- Fixed the pathing of a Yuri paradrop team on Tierra Del Fuego
- Re-enabled a trigger that gives the player additional paradrop teams at the start of the mission
- Limited the MCV Chrono reinforcements to happen once at most
	- This cheese is far too overpowered in its original state, changing it brings it more in line with similar triggers in other missions, like in Escape Velocity

YR Soviet 2:
- Added a 5 in-game second delay to the Chronosphere Transfer once its first chronoshift finishes
	- This eliminates the visual bug caused by changing the Chronosphere's house right as it fires its superweapon
- Made the Chronosphere unsellable to remove the rare possibility of the AI selling the Chronosphere and hand the player the victory
- Fixed several AITriggers that had erroneous conditions
	- For example, (Amb_MirageBR AITrig) erroneously checks whether BadGuy1 owns Apocalypse tanks instead of checking whether the player owns Apocalypse tanks. Fixing this means AI can now properly create Mirage tank ambush teams
	- Affected triggers: Amb_MirageBR AITrig, Amb_MirageBS AITrig, Amb_MirageBT AITrig, Amb_MirageBU AITrig, Amb_MirageBV AITrig, Amb_MirageBW AITrig
- Added a trigger to brief the player on the Battle Bunker once they deploy the Soviet ConYard; uses a related un-used Zofia voiceline

YR Soviet 4:
- Changed the Kill Light triggers so that the player doesn't see a strange explosion when the invisible light posts are turned off
- Added an un-used text string to the player reinforcements that can occur on Easy and Medium difficulty

YR Soviet 6:
- Changed the Kill Light triggers so that the player doesn't see a strange explosion when the invisible light posts are turned off
- Added a reinforcement team for the player once they lose a certain amount of units on Easy difficulty
	- This trigger uses an un-used text string
