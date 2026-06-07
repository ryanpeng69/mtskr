<img width="2109" height="745" alt="MTskR_banner" src="https://github.com/user-attachments/assets/26cfca62-b0df-495b-8bc5-b45b2363196e" />

# MTskR: Minecraft TrainSkript Railway

  MTskR is a [Skript](https://github.com/SkriptLang/Skript) work of [Jonathan Ho](https://www.youtube.com/@JonathanHo33)'s [Minecraft Transit Railway mod](https://modrinth.com/project/XKPAmI6u) made by [RyanPeng69](https://github.com/ryanpeng69).

  My goal is to put this mod into a Paper Server with [Skript](https://github.com/SkriptLang/Skript) **without any resource packs**.

  Join [MTskR Discrd](http://discord.gg/kSSmEyVSRR) for more help!

  See more on [MTskR web](https://mtskr.up.railway.app).

## Installation:

  Grab [mtskr.sk](https://github.com/ryanpeng69/mtskr/blob/main/mtskr.sk) into your scripts folder, reload script, it will automatically generate folder & config and move the script to the folder.

  Required plugins: [skript](https://github.com/SkriptLang/Skript) [skbee](https://github.com/ShaneBeee/SkBee), [skript-gui](https://github.com/APickledWalrus/skript-gui), [skript-reflect](https://github.com/SkriptLang/skript-reflect), [skript-yml](https://github.com/Sashie/skript-yaml)

  Least requirement: `Paper 1.20.5 (custom_data)`

  Tested versions:

* `Paper 1.21.11-130`, `Skript 2.14.2`, `Skbee 3.20.0`, `skript-gui 1.3.1`, `skript-reflect 2.6.3`, `skript-yml 1.7.2`

## Getting Started

  View ingame tutorial with `/mtskr`

##### Models

  To get started, you will need train models.
  You can create one by your self or download one from [models page on web](https://mtskr.up.railway.app/models).

## Items/Blocks:

##### Items:

* [X] Brush: brush
* [X] Loc Selector: iron axe
* [ ] Seat
* [ ] Railway Dashboard: map

##### Blocks:

* [X] Rail node: stone button (blocks used to connect rails, direction matters)
* [ ] Platform block (maybe)

##### Rail connectors: (interact with rail nodes)

* [X] Normal: iron ingot
* [X] Platform: redstone
* [X] Siding: gold ingot
* [X] Turnback: lapis lazuli
* [X] Remove: copper ingot

##### Build tools:

* [X] Bridge: stone shovel
* [X] Tunnel: stone pickaxe
* [X] Tunnel walls: stone axe

## Data (Yaml) structure:

##### model:

```yml
# models\%name%.yml
info:
  facing: (south|west|north|east)
  loc1: %loc%
  loc2: %loc%
  model_version: %int%
  minecraft_version: %minecraft version%
%index%:
  loc: %relative loc to base%
  block: %blockdata%
  door: %facing%%move% # optional
```

##### rail:

```yml
# data\rails\%world%.yml
%loc1%:
  %loc2%:
    type: (normal|platform|siding|turnback)
    platform: # optional
      name: %text = "1"%
      stop_time: %int = 5% # seconds
    depot: # optional
      name: %text = "1"%
      trains:
        - %text% # train model
```

## Train function:

* [X] Model: Display blocks riding on a minecart
* [ ] Spawn: By selecting train in the gui for a depot track, the train will spawn.
* [ ] Movement: Set velocity of train to velocity from loc1 to loc2
* [ ] Passengers: Must be on a seat
* [ ] Arrival countdown: ?

## Stations & Depots

  Use bound from SkBee for area

  Both have `name` and `color`

##### Depots

  These are the extra values of a depot

* [ ] Scedule
* [ ] Routes
