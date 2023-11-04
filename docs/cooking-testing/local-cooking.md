# Locally Cooking a Mod
## Cooking in ADK
To cook a Mod locally, click the cooker icon on the top bar (same as Play in PIE). 

![Cooker Icon](/img/docs/cooking/local-cook-icon.png)

This will open the Cooker Dialog window.

![Cooker Dialog](/img/docs/cooking/cook-dialog.png)

(1) Select a Mod to cook and (2/3) determine if you will be testing this on a dedicated 
server. If so, make sure Windows Server is checked. Windows Client will cook all files,
while Windows Server will only cook files required for dedicated server. (4) Set the 
number of cook processes to the amount of RAM you have available divided by five.
```
(Total RAM - Used Ram) / 5 = # Cook Processes
```
(5) Start the cook and (7) monitor the cooker output. If, for any reason, you need to
(6) cancel the cook, do so by clicking the Cancel button.

When the cook finishes, it should open a File Explorer window to the packaged `.zip`
files. If not, check the log output for any errors. If there are no errors, check
`ARKDevkit\ModTools\Output\<ModDirName>` to see if the files were updated. If so, the cook
succeeded. With the cooked zips, you may proceed to testing with locally cooked files.

## Cooking outside ADK
### Interactive Shell
There is a script located at `ARKDevKit\ModTools\Scripts\CookMod.bat`, you can run this
to get an interactive shell that mimics the cooker in ADK.

```
===============================
====== Mod Cook Settings ======
===============================

Cook Platforms:

[1] Windows Client [Enabled]
[2] Windows Server [Enabled]

Mod Information:

[3] Mod Name [None]
[4] # of Cook Workers [3]

[5] Start Cook
[6] Exit

[ERROR]: A valid mod directory has not been entered

Selection:
```

Use the selections, primarily providing a Mod Directory Name, then select `[5] Start Cook`.
Again, the cooker will place the files in `ARKDevKit\ModTools\Output\<ModDirName>`

### Headless (unattended)
Use the following command, filling in the properties appropriately, assuming you have ADK
installed at `C:\ARKDevKit`

```
C:\ARKDevKit\Engine\Build\BatchFiles\RunUAT.bat BuildPlatformUGC -Windows -WindowsServer -Mod=ModDirName -NoCompile -OutputDirectory="C:\ARKDevkit\ModTools\Output\ModDirName\\" -AdditionalCookerOptions="-CookProcessCount=3"
```
Take note of the arguments and their options, filling in the values appropriately. For
example, if the Mod directory name was `MyMod`, replace `ModDirName` with `MyMod` in 
both places (`-Mod`, `-OutputDirectory`).

Again, the cooker will place the files in `C:\ARKDevKit\ModTools\Output\<ModDirName>`
