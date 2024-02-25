# Crysis Creative Tools Mod

The mod provides various tools for creativity, creating custom game situations and just for fun.

## Mod description

> *Note: All elements in < > brackets need to be replaced by your values*


Due to the lack of an SDK for Crysis Warhead, the modification exists in 2 versions:

### [Script version] Universal, for Crysis 1, Crysis Warhead

#### Features
- Ability to spawn entities from game (weapons, vehicles, NPS, etc) with DebugGun.
- Customizable entity list of predefined entities for spawn (Just modify array in ```<YOUR_GAME_FOLDER>/Mods/CreativeTools/Game/Scripts/SpawnEntityList.lua```)
- A little changes in suit balancing: Armor x1.5, player health x2, slightly reduced power consuming in cloak and speed modes (You can disable in ```<YOUR_GAME_FOLDER>/Mods/CreativeTools/Game/autoexec.cfg```).


#### How to use

Open console *[~ key]* and give debug gun by command ```i_giveitem DebugGun``` (case sensitive).

**Available actions by debug gun:**
 1. On Fire *[Left mouse click]* - Spawn entity on debug mark, choose by current vale of index from entity list. (On start is 1)
 2. On Zoom *[Right mouse click]* - Increment index and select next entity. (You can check name of selected entity from console by command ```v_debugVehicle```)
 3. On Reload *[R key]* - Try to find entity by name from console variable ```v_debugVehicle``` in entity list. On success select it for spawn. (You can set it from console by type ```v_debugVehicle <YOUR_VALUE>```)
 4. On ChangeMode *[X key]* - Remove last spawned entity.

### [SDK version] Extended, for Crysis 1

> **Warning!** Work only for Crysis 1, currently not support x64.

#### Features & How to use
All features & tools from universal mod version!

Separated entity list in xml format, can find in ```<YOUR_GAME_FOLDER>\Mods\CreativeTools\Game\Scripts\Entities\EntitySpawnList.xml```.

**New console commands:**
- ```spawn <ENTITY_NAME_FROM_LIST>``` => Try find entity by name from list and spawn it!
- ```spawn_entity <ENTITY_NAME>``` => Spawn ANY entity from game by entity name.
- ```spawn_entity_a <ENTITY_ARCHETYPE_NAME>``` => Spawn ANY entity archetype from game by FULL archetype name (include folder names).
- ```extend_power``` => Extend suit characteristics like settings from ```autoexec.cfg```.

*Note:* For more docs type in console ```<COMMAND_NAME> ?``` for in-game documentation.

## Installation

1. Download archive for your game (and choose mod version) for releases on GitHub.
2. Copy all archive content in your game directory.
3. Add run arguments to enable mod
   1. **For Game Launchers (Steam, Origin, etc)**
      1. Open Properties for your game in launcher
      2. Find run arguments and add ```-devmode -mod CreativeTools```
   2. **For other game versions** 
      1. Create (or modify) link of your game executable file for ```<YOUR_GAME_FOLDER>/Bin32/Crysis.exe``` (Recommended) or ```<YOUR_GAME_FOLDER>/Bin64/Crysis64.exe```.
      *Note:* For SDK version use only exe from Bin32 directory.
      2. Add arguments ```-devmode -mod CreativeTools``` in your Target field of link ([Example of adding argument](https://superuser.com/questions/29569/how-to-add-command-line-options-to-shortcut))
4. Run game and enjoy!


## FAQ

- Q: Is this mod support Crysis Remastered?
- A: Currently no, but maybe in future. 

- Q: What versions of Crysis / Crysis Warhead are supported?
- A: Tested on Crysis (v.1.1.1.6156, GOG) and Crysis Warhead (v.1.1.1.711, GOG)


## Links

Fix of start game crash for AMD processors
https://community.pcgamingwiki.com/files/file/1411-crysis-amds-3d-now-fix