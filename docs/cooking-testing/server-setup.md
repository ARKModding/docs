# Dedicated Server Setup
:::info Windows Only

At the time of this writing, there is only support for Windows.

:::

:::warning Required Resources

At the time of this writing, a Dedicated Server instance requires at least
10GB of free RAM to run without crashing. Monitor RAM usage when running
the server if the machine is close to these limits.

:::
## Directory Setup
You will need two directories to setup a Dedicated Server
1. a directory for SteamCMD
2. a directory for the Dedicated Server (cannot be the same as the Steam CMD directory)

## Install SteamCMD

[Download SteamCMD for Windows](https://steamcdn-a.akamaihd.net/client/installer/steamcmd.zip)
and extract it to a directory (E.g. `C:\steamcmd`). Double click `steamcmd.exe` to
install it into the same directory. When it finishes, close the window.

## Install Dedicated Server
Located the directory you intend to install the Dedicated Server to. While holding shift,
right-click the directory and select `Copy as path` and paste it somewhere for now. 
Now locate the SteamCMD directory. From within the SteamCMD directory, create a new text
file and name it `UpdateServer.bat` (make sure you are not hiding file extensions).
Right-click and edit this file. Inside the file insert the following while replacing 
`<my-dir>` with the path you pasted from the Dedicated Server directory:

```batch title="UpdateServer.bat"
.\steamcmd.exe +force_install_dir "<my-dir>" +login anonymous +app_update 2430930 validate +quit
exit
```

Let this process complete, as it will take some time. Once it has completed, the server
has been installed. You can run this `.bat` file anytime to update the server as well.

## Dedicated Server Setup
### RunServer.bat
From within the directory of the Dedicated Server (where the `Engine` and `ShooterGame`
directories are), create another new text file with the name `RunServer.bat`. 
Right-click and edit this file. Copy the following to the file contents:

```batch title="RunServer.Bat"
set mods=<my-mod-id>,<other-mod-id>
start ShooterGame\Binaries\Win64\ArkAscendedServer.exe TheIsland_WP?listen?Port=7777 -game -server -log -ServerAdminPassword=oppass1 -NoBattlEye -mods=%mods%
exit
```

Take note of the `set mods` part at the top of the file. This is where the mod IDs
for the server will be defined. Insert a comma separated list of mod IDs. If you
are testing an unpublished build ([locally cooked](./local-cooking.md) or 
[CurseForge cooked](./curse-forge-cooking.md)), append `-dev` to the ID (E.g. 
`12345-dev`). If you are using a [locally cooked](./local-cooking.md) Mod, 
[copy the Mod to the Dedicated Server](./testing.md#server-setup).
