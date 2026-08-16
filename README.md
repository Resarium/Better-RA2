# Better-RA2
WIP

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
	- Side effect 3: this complicates the trigger setups related to Battle Lab and Nuke Silos. The corresponding trigger logics have been reworked to accomodate the change with additional QoL. (see below)
		- Changed the Battle Lab objective to allow the player to capture it to progress the mission, unlike in Vanilla where capturing it fails you the mission despite EVA's follow-up voiceline not making any sense.
		- Added 1 in-game second delay to Nuke 1 Destroyed, Nuke 2 Destroyed, Nuke 1 Captured, Nuke 2 Captured, to accommodate reworked Spy setup
		- Modified Nuke Silos to no longer be spyable since doing so was pointless and never affected the mission outcome in any meaningful way.
- Added an extra reveal when the player discovers the crash-landed units to make them easier to spot
	- This repositions and uses waypoint 25, which wasn't used for anything else before this