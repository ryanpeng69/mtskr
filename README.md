<img width="2109" height="745" alt="MTskR_banner" src="https://github.com/user-attachments/assets/26cfca62-b0df-495b-8bc5-b45b2363196e" />

# MTskR: Minecraft TrainSkript Railway

MTskR is a [Skript](https://modrinth.com/project/xFNYAvMk) work of [Jonathan Ho](https://www.youtube.com/@JonathanHo33)'s [Minecraft Trainsit Railway mod](https://modrinth.com/project/XKPAmI6u).

My goal is to put this mod into a Paper server with [Skript](https://modrinth.com/project/xFNYAvMk) **without any resource packs**.

Join [MTskR Discrd](http://discord.gg/kSSmEyVSRR) for more help!

## Installation:

Grab [mtskr.sk](https://github.com/ryanpeng69/mtskr/blob/main/mtskr.sk) into your scripts folder, reload script, it will automatically generate folder and move.

Required addons: [skbee](https://modrinth.com/plugin/skbee), [skript-gui](https://github.com/APickledWalrus/skript-gui), [skript-reflect](https://github.com/SkriptLang/skript-reflect), [skript-yml](https://github.com/Sashie/skript-yaml)

Tested versions:

* `Paper 1.21.11-130`, `Skbee 3.20.0`, `skript-gui 1.3.1`, `skript-reflect 2.6.3`, `skript-yml 1.7.2`

## Items/Blocks:

##### Blocks:

* [ ] Rail node: stone button (blocks used to connect rails, direction matters)

##### Rail connectors: (use on rail nodes)

* [ ] Normal: iron ingot
* [ ] Platform: redstone
* [ ] Depot: gold ingot

##### Build tools: (use blocks between expression with rail node loc, 1 block left of it, and 1 block right of it)

* [ ] Bridge: stone shovel
* [ ] Tunnel: stone pickaxe
* [ ] Tunnel walls: stone axe

## Data (Yaml) structure:

##### model:

```yml
facing: (south|west|north|east)
%index%:
  loc: %relative loc to base%
  block: %blockdata%
%index%:
  loc: %relative loc to base%
  block: %blockdata%
  door: %facing%%move%
```

##### rail:

```yml
%index%:
  type: (normal|platform|depot)
  loc1: %loc%
  loc2: %loc%
```

## Train function:

* [ ] Model: Display blocks riding on a minecart
* [ ] Spawn: By selecting train in the gui for a depot track, the train will spawn.
* [ ] Stations: Stops for `5` seconds
* [ ] Movement:  Set velocity of train to velocity from loc1 to loc2 (need to set velocity and derailed velocity)
* [ ] Arrival countdown: ? (need a equ)

## GUI:

* [ ] 1st row: tabs (including `items (like creative item tab)`,  `stations (used to modify station (name?))`, `depots (used to modify depots and spawn train)`)
