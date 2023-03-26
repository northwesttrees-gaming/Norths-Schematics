# Norths Schematics
## Overview
North's Schematics Mod is a survival/creative mode mod that lets players save blocks and block rotation to JSON files using the [File Manager](https://mcreator.net/plugin/64638/file-creator) plugin for [MCreator](https://mcreator.net/https://mcreator.net/plugin/64638/file-creator). Once the file is saved the player can load the structure anywhere in the Minecraft map. In survival mode structures are removed after they are saved. In creative mode they structures are cloned but not removed. Works for both servers and single player as well as LAN. Opped players can control the capped structure size limit. It is possible to save and load structures that are larger than Vanilla Minecraft's structure block size limit.

## Download Sites
- [CurseForge](): All client releases on CurseForge mod page!
- [MCreator](): Latest releases on MCreator mod page!
- [GitHub](): All releases for both development and client on GitHub releases.

## Features
- [x] Supports both survival and creative game modes.
- [x] Servival mode removes the saved structure blocks.
- [x] Chest items are dropped when structures are removed.
- [x] Creative mode clones structures but does not remove them.
- [x] Structure files are saved to profile/server config folder.
- [x] Runs mostly on server-side minus some UI components.
- [x] Designed with servival level in mind.
- [x] Oped players can set structure size caps using game rules.
- [x] When using structure caps you can save/place larger structures than structure blocks.
- [x] Easy to craft in survival mode.
- [x] Easy to get the exact structure size using target blocks on the same structure axis as the save block.
- [x] Support for Forge API

## Planned Features
- [ ] Add support for creative mode for removing structures completly
- [ ] Add support for placement methods such as masking only specifc blocks
- [ ] Trading mechanics for players to trade schematics in some way.
- [ ] Marketplace for schematics allowing players to sell sechematics for diamonds.
- [ ] Support for Fabric API

## Example Structure File
```json
# The display name of the player that saved the file.
  "owner": "Dev",
# When the structure is placed this value is set to true.
# This is later used in script for survival mode player and tested to know if the structure has been placed or not.
  "placed": false,
# When the file is save so is the structure size from the fields
  "size_x": 20.0,
  "size_y": 15.0,
  "size_z": 20.0,
# Each block is saved with its rotation.
  "1_block": "{Name:\"minecraft:grass_block\",Properties:{snowy:\"false\"}}",
  "1_rotation": 2,
  "2_block": "{Name:\"minecraft:grass_block\",Properties:{snowy:\"false\"}}",
  "2_rotation": 2,
  "3_block": "{Name:\"minecraft:grass_block\",Properties:{snowy:\"false\"}}",
  "3_rotation": 2,
  "4_block": "{Name:\"minecraft:grass_block\",Properties:{snowy:\"false\"}}",
  "4_rotation": 2,
  "5_block": "{Name:\"minecraft:cobblestone\"}",
  "5_rotation": 2,
  "6_block": "{Name:\"minecraft:nether_brick_stairs\",Properties:{facing:\"south\",half:\"top\",shape:\"straight\",waterlogged:\"false\"}}",
  "6_rotation": 3,
  "7_block": "{Name:\"minecraft:cobblestone\"}",
  "7_rotation": 2,
  "8_block": "{Name:\"minecraft:cobblestone\"}",
  "8_rotation": 2,
  "9_block": "{Name:\"minecraft:dirt\"}",
  "9_rotation": 2
}
```
## Finding Structure Files
### Single Player & LAN
```
<profile>/config/norths_schematics/players/<player_name>/<file_name>.json
<profile>/config/norths_schematics/players/<player_name>/backups/<file_name>.json
```
### Servers
```
<server_root>/config/norths_schematics/players/<player_name>/<file_name>.json
<server_root>/config/norths_schematics/players/<player_name>/backups/<file_name>.json
```
