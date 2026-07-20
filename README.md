<img width="1700" height="600" alt="MTskR Banner" src="https://github.com/user-attachments/assets/d159ed40-3479-4abb-baa7-333b8706d91e" />

# MTskR: Minecraft TrainSkript Railway

  MTskR is a [Skript](https://github.com/SkriptLang/Skript) project based on [Jonathan Ho](https://www.youtube.com/@JonathanHo33)'s [Minecraft Transit Railway mod 4.0.0](https://modrinth.com/project/XKPAmI6u), developed by [RyanPeng69](https://github.com/ryanpeng69).

  My goal is to implement this mod into a Paper Server using [Skript](https://github.com/SkriptLang/Skript) **without any resource packs**.

  Join the [MTskR Discord](https://discord.gg/kSSmEyVSRR) for support or to help us translate!

  See the [Web](https://mtskr.up.railway.app) or [Wiki](https://github.com/ryanpeng69/mtskr/wiki) for more information.

## Features:

1. **Display Block Trains**: Trains are made of display blocks, no resource pack required.

2. **Per User Language System**: Each player can use their own language to play MTskR.

3. **Easy Download Installer**: Just one plugin or script can install everything.

4. **Configurable Settings**: Configure the speed and limits to fit your performance.

5. **Node-based Rail System**: You don't need to place rails block by block, trains will go node by node.

6. **Scheduled Departures**: Set the departure interval for your siding, the train will depart regularly.

7. **Routes & Platforms**: Create routes with in-game tools and trains will stop at platforms.

8. **Community Models Sharing**: Build your models in game easily with blocks and share it on [the web](https://mtskr.up.railway.app/models). Everyone can download it with `/mtskr model download`.

9. **Items from GUI**: By running `/mtskr gui`, you can view and get all items without memorizing id.
## Installation:

### 1. Jar Installer (<a href="https://github.com/ryanpeng69/mtskrinstaller">mtskrInstaller.jar</a>)
<ol>
  <li>Download the <a href="https://github.com/ryanpeng69/mtskrinstaller">mtskrInstaller</a> plugin and place it in <code>plugins\</code>.</li>
  <li>Restart the server.</li>
  <li>Run <code>/mtskrinstallerjar requirements</code> to download the required plugins.</li>
  <li>Restart the server again.</li>
  <li>Run <code>/mtskrinstallerjar download</code> to download the scripts.</li>
  <li>Use <code>/mtskr config</code> to edit the configuration if needed.</li>
  <li>Run <code>/mtskr</code> to get started.</li>
</ol>

### 2. Skript Installer (<a href="https://github.com/ryanpeng69/mtskr/blob/main/mtskr/mtskr.installer.sk">mtskr.installer.sk</a>)
<ol>
  <li>Place the <a href="https://github.com/ryanpeng69/mtskr#requirements">required plugins</a> into the <code>plugins\</code> folder.</li>
  <li>Move <a href="https://github.com/ryanpeng69/mtskr/blob/main/mtskr/mtskr.installer.sk">mtskr.installer.sk</a> into <code>plugins\Skript\scripts</code>.</li>
  <li>Run <code>/sk reload scripts</code> to reload the script.</li>
  <li>Run <code>/mtskrinstaller</code>; it will download additional files and automatically reload.</li>
  <li>Use <code>/mtskr config</code> to edit the configuration if needed.</li>
  <li>Run <code>/mtskr</code> to get started.</li>
</ol>

### 3. Manual Installation (<a href="https://github.com/ryanpeng69/mtskr">MTskR GitHub</a>)
<ol>
  <li>Place the <a href="https://github.com/ryanpeng69/mtskr#requirements">required plugins</a> into the <code>plugins\</code> folder.</li>
  <li>Download everything from <a href="https://github.com/ryanpeng69/mtskr">GitHub</a>.</li>
  <li>Place the files in <code>plugins\Skript\scripts\.\mtskr\</code>.</li>
  <li>Run <code>/sk reload scripts</code>.</li>
  <li>Use <code>/mtskr config</code> to edit the configuration if needed.</li>
  <li>Run <code>/mtskr</code> to get started.</li>
</ol>

  See the [Wiki](https://github.com/ryanpeng69/mtskr/wiki/Installation) for a more detailed installation guide.

### Requirements

  Required plugins: [Skript](https://github.com/SkriptLang/Skript), [SkBee](https://github.com/ShaneBeee/SkBee), [skript-reflect](https://github.com/SkriptLang/skript-reflect), [skript-yaml](https://github.com/Sashie/skript-yaml)

  [Paper 1.20.5+](https://papermc.io/downloads/paper) (custom_data)

  Tested versions:

* `Paper 1.21.11-130`, `Skript 2.14.2`, `SkBee 3.20.0`, `skript-reflect 2.6.3`, `skript-yml 1.7.2`
* `Paper 1.21.11-130`, `Skript 2.14.3`, `SkBee 3.20.0`, `skript-reflect 2.6.3`, `skript-yml 1.7.2`
* `Paper 1.21.11-130`, `Skript 2.15.4`, `SkBee 3.25.1`, `skript-reflect 2.6.3`, `skript-yml 1.7.2`

## Getting Started:

After you have installed all the plugins and scripts, you can start creating tracks.

> If you prefer an in-game tutorial or need other languages, type `/mtskr tutorial` in-game.

### Connecting Rails:

MTskR uses `rail nodes` and `rail connectors` to build paths for your trains. Run `/mtskr gui` to get the items.

In this GUI, you will see every block and item included in MTskR. Click on a `rail node` to obtain it.

Now, place 2 `rail nodes` facing the same direction at a distance of 10 blocks.

> The rail length should not be shorter than the train length; a standard train takes up about 10 blocks. See the [Wiki](https://github.com/ryanpeng69/mtskr/wiki/Creating-a-Rail-System) for more information.

Take the `one way rail connector`, `double way rail connector`, `siding rail connector`, and `platform rail connector` from the GUI. We will use them to connect our rails.

Connect the 2 `rail nodes` you just placed using the `siding rail connector`. This is where your trains will spawn.

Go to an open area in your Minecraft world and place 2 `rail nodes` connected with the `platform rail connector`. Your train will stop at this platform.

Place some rail nodes between the siding and the platform, then use a `one way` or `double way` `rail connector` to link them.

> Make sure the rails you connected can route the train from the siding to the platform and back to the siding.

You can use a `brush` on a rail node to view the connected rails.

### Creating Routes:

Once you have connected the rails, you will need to create routes. Take a `route creator` and read below:

Routes are made of 2 bounds: the `out bound` and the `in bound`. Currently, MTskR only supports these 2 bounds.

Click on the end of the platform (the 2nd clicked rail node) you just created. You may add more nodes before it, but make sure you have this one selected.

Sneak-click your `route creator` and it will display a dialog for you to create the route.

Please write a name that ends with `.out` or `||out`. Choose any color you like.

> e.g. `forest.out`

This means that the train will depart from the siding and go through every node you selected. If there isn't a direct rail to a node, it will automatically find the nodes between them.

Now, select any node on the way back to the siding and create a route again.

This time, please set the name to `#<id>.in` or `#<id>||in`. Get the `<id>` by typing `/mtskr route`, which will display the route you just created.

> e.g. `#1||in`

### Modifying Sidings:

Finally, you have your rails set up, but how does the train know when and where to go?

Get a `brush` from the GUI and sneak-click on the start of the siding rail.

In this GUI, you can modify the siding's name, departure interval, train type, route, etc.

Let's click on `select route`, then select the route you just created.

But we still need trains, how do we build one?

You can download one using `/mtskr model download` or create your own.

MTskR provides a user-friendly method to create models in-game; see [Creating Models](#creating-models) below.

When you get the model, click on `select train` and select your model.

If everything is configured correctly, your train will start moving after you press `refresh route`.

Ask for help on [Discord](http://discord.gg/kSSmEyVSRR) if you find it difficult.

### Creating Models:

This is the most unique feature of MTskR: you can build your train models in-game using any blocks you like!

Simply add an oak sign that says `[Model]` to specify the front wheel of your train.

**Important**: Place `Model Seats` inside your train for passengers to sit on.

Get the `loc selector` and select 2 corners like in WorldEdit, then type `/mtskr model create <name>`.

If you think your model looks good, share it on [MTskR Web](https://mtskr.up.railway.app/models)!

## Data:

### Configuration & Variables:

MTskR uses `YAML` files and `Skript variables`:

#### YAML

All MTskR data YAML files are stored in `plugins\Skript\scripts\.\mtskr\data\`.

The `config.yml` file is located in `plugins\Skript\scripts\.\mtskr\`.

#### Variables

1. `{-MTskR::*}`: This is used for loaded data, such as trains and routes.

2. `{MTskR::*}`: This is exclusively used for storing seat blocks in model builds.
