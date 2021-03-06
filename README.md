# ELS-Plus

See: https://github.com/ejb1123/ELS-Plus/issues to submit an issue. It is important that if you test ELS for FiveM that you submit issues so that we may work to resolve these. Here's some things to consider:

- ELS vehicles are not yet supported.
- Lights are in progress. Currently sync is not working but you are able to use lights.
- Custom cars will require VCF files to be created by following the [How to add custom Vehicles](#how-to-add-els-vehicles-to-els-fivem) section.
- You can spawn a vehicle using /elscar {model}
- You can obtain a list of the vehicles ELS has detected by typing /elslist and pressing F8 to view console.



### Default Controls

|Action Key|Default Key|Default Binding
|---|---|---|
| Vehicle Horn  | E key | Horn control|
| Select Unarmed Weapon | 1 Key | Wail tone |
| Select Melee Weapon | 2 Key | Yelp tone |
| Select Shotgun Weapon | 3 Key | Auxilary tone 1|
| Select Heavy Weapon | 4 Key | Auxilary tone 2|
| Select Special Weapon | 5 Key | Toggles Dual Siren Mode|
| Chat All| Y Key|Goes to next tone or plays tone 1|
| Throw Grenade| G Key|Toggles main siren|
| Radio Wheel | Q Key | Toggles vehicle's Light Stages|
| Multiplayer Info | Z Key | Toggles vehicle's Primary Patterns|
| Drop Projectile | X Key | Toggles vehicle's Secondary Patterns|
| Look Behind | C Key | Toggles vehicle's Warning Patterns|
| Vehicle Next Radio Track | . Key | Toggles vehicle's Takedown Lights (Extra 12)|
| Vehicle Next Radio Track | Alt + . Key | Toggles vehicle's Scene Lights (Extra 11)|
|Replay Show Hot Key | K Key | Toggles vehicle's secondary lights|
|Cinematic Slo Mo | L Key | Toggles vehicle's warning lights|
|| [ Key | Toggles vehicle's Cruise Lights|
|| L Alt + [ | Toggles vehicles Arrowboard if equipped(Not fully working)|
||Ctrl + P|Toggles UI Panel|
|---|---|---|
|Sniper Zoom in secondary|DPad Up|Toggle Auxilary Tone 1|
|Sniper Zoom out secondary|DPad Down|Toggle Main Siren|
|Detonate|DPad Left|Toggle Light Stages|
|Talk|DPad Right|Toggle Takedownlights (Extra 12)|
|Duck|L3(Press left stick)|Horn Control|
|Reload|B(XBox) or O/Circle (PS)|Wail Tone|
|Reload and Duck|L3(Press left stick) + B(XBox) or O/Circle (PS)|Yelp Tone|


### How to install
1. Copy the `ELS-FiveM` folder to `cfx-server\resources\`
2. Add `ELS-FiveM` to `server.cfg`
3. Add `add_ace resource.RESOURCE_NAME command.add_ace allow` to `server.cfg`
   remember to replace `RESOURCE_NAME` with the name of this resource.
4. Add your user to the `group.admin` principle to allow you to use the elscar commmand to spawn a vehicle

### How to add ELS Vehicles to ELS-FiveM
1. Create add-on/replace Vehicle with stream folder and relevant files.
2. In `__resource.lua` add the `VCF` xml file to the `files` list.
3. Add `is_els 'true'` to bottom of `__resource.lua`.
4. Restart Server
5. Profit

#### Important Notes

- When running the rcon command `restart ELS-FiveM` or `start ELS-FiveM`.
Make sure you restart any resources that have ELS vehicles.
- Make sure ELS-FiveM is located below all ELS enabled vehicle stream resources in the `server.cfg` file.

## Contribute
if you are a developer and  would like to contribute any help is welcome!
The contribution guide can be found [here](CONTRIBUTING.md).

### How to Build and Test

1. Add the enviroment variable `FXSERVERDATA` and set its value to the `resources` directory path.

2. `git clone https://github.com/FiveM-Scripts/ELS-FiveM.git`

3. Open `ELS-FiveM\src\ELS-for-FiveM.sln` in Visual Studio

4. Select `Release` and `Any CPU`  next to the Start button

5. In the menu bar under Build click on `Build Solution`

6. Copy all the files from `ELS-FiveM\src\bin\Release` to `cfx-server\resources\ELS-FiveM`

7. Add `ELS-FiveM` to `AutoStartResources` in `cfx-server\citmp-server.yml`
