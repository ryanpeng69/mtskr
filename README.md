<img width="1700" height="600" alt="MTskR Banner" src="https://github.com/user-attachments/assets/d159ed40-3479-4abb-baa7-333b8706d91e" />

# MTskR: Minecraft TrainSkript Railway

  MTskR is a [Skript](https://github.com/SkriptLang/Skript) work of [Jonathan Ho](https://www.youtube.com/@JonathanHo33)'s [Minecraft Transit Railway mod](https://modrinth.com/project/XKPAmI6u) made by [RyanPeng69](https://github.com/ryanpeng69).

  My goal is to put this mod into a Paper Server with [Skript](https://github.com/SkriptLang/Skript) **without any resource packs**.

  Join [MTskR Discrd](http://discord.gg/kSSmEyVSRR) for support or help us translate!

  See [Web](https://mtskr.up.railway.app) or [Wiki](https://github.com/ryanpeng69/mtskr/wiki) for more informations.

## Installation:

<ol>
  <li>Get the required plugins into <code>plugins\</code> folder.</li>
  <li>Grab <a href="https://github.com/ryanpeng69/mtskr/blob/main/mtskr/mtskr.installer.sk" target="_blank">mtskr.installer.sk</a> into <code>plugins\Skript\scripts</code>.</li>
  <li>Run <code>/sk reload scripts</code> to reload the script.</li>
  <li>Run <code>/mtskrinstaller</code>, it will download more files and automatically reload.</li>
  <li>Use <code>/mtskr config</code> to edit config if you want.</li>
  <li>Run <code>/mtskr</code> to get started.</li>
</ol>

  See more installation guide on [wiki](https://github.com/ryanpeng69/mtskr/wiki/Installation)

### Requirements

  Required plugins: [skript](https://github.com/SkriptLang/Skript) [skbee](https://github.com/ShaneBeee/SkBee), [skript-reflect](https://github.com/SkriptLang/skript-reflect), [skript-yml](https://github.com/Sashie/skript-yaml)

  Least requirement: `Paper 1.20.5 (custom_data)`

  Tested versions:

* `Paper 1.21.11-130`, `Skript 2.14.2`, `Skbee 3.20.0`, `skript-reflect 2.6.3`, `skript-yml 1.7.2`

## Data:

### Yaml:

  MTskR use `Yaml` and `Skript variables`:

#### Yaml

  Data Yaml of MTskR are all stored in `plugins\Skript\scripts\.\mtskr\data\`.

  `config.yml` is in `plugins\Skript\scripts\.\mtskr\`

#### Variables

1. `{-MTskR::*}` This is used for loaded things such as trains and routes.

2. `{MTskR::*}` This is only used for storing seat blocks in model builds.
