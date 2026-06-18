<img width="2109" height="745" alt="MTskR_banner" src="https://github.com/user-attachments/assets/26cfca62-b0df-495b-8bc5-b45b2363196e" />

# MTskR: Minecraft TrainSkript Railway

  MTskR is a [Skript](https://github.com/SkriptLang/Skript) work of [Jonathan Ho](https://www.youtube.com/@JonathanHo33)'s [Minecraft Transit Railway mod](https://modrinth.com/project/XKPAmI6u) made by [RyanPeng69](https://github.com/ryanpeng69).

  My goal is to put this mod into a Paper Server with [Skript](https://github.com/SkriptLang/Skript) **without any resource packs**.

  Join [MTskR Discrd](http://discord.gg/kSSmEyVSRR) for more help!

  See more on [MTskR web](https://mtskr.up.railway.app).

## Installation:

<ol>
  <li>Get the required plugins into <code>plugins\</code> folder.</li>
  <li>Grab <a href="https://github.com/ryanpeng69/mtskr/blob/main/mtskr/mtskr.installer.sk" target="_blank">mtskr.installer.sk</a> into <code>plugins\Skript\scripts</code>.</li>
  <li>Run <code>/mtskrinstaller</code>, it will download more files and automatically reload.</li>
  <li>Edit the config at <code>plugins\Skript\scripts\.\mtskr\config.yml</code> if you want.</li>
  <li>Run <code>/mtskr</code> to get started.</li>
</ol>

##### Requirements

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

  Items of MTskR are stored in [mtskr.items.sk](https://github.com/ryanpeng69/mtskr/blob/main/mtskr/mtskr.items.sk), meaning that you can modify the name, lores, and even custom models.
  Although MTskR is made for resource pack free servers, you can add one if you want. (see [MTskR Wiki](https://github.com/ryanpeng69/mtskr/wiki/Using-resource-packs))

##### Items:

* [X] Tutorial: book
* [X] Brush: brush
* [X] Loc Selector: iron axe
* [X] Route Creator: stick
* [X] Seat
* [ ] Railway Dashboard: map

##### Blocks:

* [X] Rail node: stone button (blocks used to connect rails, direction matters)
* [ ] Platform block

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

## Data:

#### Yaml:

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
  door: %text% # %facing%%move% # optional
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
    siding: # optional
      name: %text = "1"%
      schedule: %int = 0% # seconds
      route: %int% # route id
      train: %text%
```

##### route:

```yml
# data\routes\%world%.yml
%id%:
  name: %text%
  color: %text% # hex
  nodes:
    - %x,y,z%
```

#### Variables:

  MTskR mainly use one variable key: {-MTskR::*}.
  {MTskR::*} is only used for seats for building models.

  **Advantages**:
    {-variable}s will not be saved when server stops, meaning they won't be in variables.csv or your disk.
  **Disadvantages**:
    Every time you restart(reload) the server, it will recalculate routes.

## Train function:

* [X] Model: Display blocks riding on a minecart.
* [X] Spawn: By selecting train in the gui for a siding, the train will spawn.
* [X] Movement: Set velocity of train to vector from loc1 to loc2.
* [ ] Passengers: Must be on a seat.
* [ ] Arrival countdown: ?

## Stations & Depots

  Currently, MTskR does not have stations and depots.
  Their functions are moved to platforms and sidings, allowing stronger railway system.
