 
# How to install:

- get the Unity Mod Manager (UMM) from Nexus Mods here: https://www.nexusmods.com/site/mods/21 and install it (simply unpack the zip-file to a location you like).
- now go to the installtion directory of UMM. You need to modify the file UnityModManagerConfigLocal.xml
- open the file with notepad and put the following XML data right before the \</Config> tag.
    ```
    <GameInfo Name="Shop Heroes">
        <Folder>Shop Heroes</Folder>
        <ModsDirectory>Mods</ModsDirectory>
        <ModInfo>Info.json</ModInfo>
        <GameExe>shopheroes.exe</GameExe>
        <EntryPoint>[UnityEngine.UI.dll]UnityEngine.EventSystems.EventSystem.cctor:After</EntryPoint>
        <StartingPoint>[Assembly-CSharp.dll]Bootstrap.Awake:After</StartingPoint>
        <UIStartingPoint>[Assembly-CSharp.dll]Cloudcade.ViewShop.Start:After</UIStartingPoint>
        <GameVersionPoint>[Assembly-CSharp.dll]Version.GetString</GameVersionPoint>
    </GameInfo>
    ```
- now start UMM to install the mod into the game.
- select the "Shop Heroes" entry from the game list 
- select the proper installation folder, e.g. ?:\SteamLibrary\steamapps\common\Shop Heroes
- use **DoorstopProxy** as installation method
- press the **Install** button
    - [optional] start the game to check if the installation has worked as expected. 
      After your character data has been loaded, you should see the mod manager interface. 
      If not, try CTRL+F10 to bring up the interface.
- switch to the Mods-tab 
- use **install mod** and select the included zip-package or use the **drop zip here** area with the included zip file.


If you want to uninstall the mod manager from the game:
- open umm, select Game: Shop Heroes and press Uninstall - the mods will still be in the installation folder but no longer injected to the game.
	
