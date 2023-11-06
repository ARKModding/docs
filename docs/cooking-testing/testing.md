# Testing a Mod
:::info Valid Mod ID Required

Before you can test, you must get a valid Mod ID. Either by using an already published
Mod that you are subscribed to (preferably one that doesn't update often), or by
uploading your Mod to CurseForge at least once, and using the ID from there. 

It is
not uncommon for Modders to use the 
[Identity Helper](https://curseforge.com/ark-survival-ascended/mods/identity-helper) 
Mod, and its ID (`929134`), to test with as it shouldn't update.

:::

:::info Mod Version

The Mod folder installed by the client and server has the following format:

```
modid_buildversion
```

The Mod build version can be seen on the URL for the client or server zip on CurseForge.

:::

## Locally Cooked Mod
### Client Setup
Subscribe to the Mod ID that will be used for testing via the game client and let it
install the mod. Once the Mod has been installed, open the game clients files in
File Explorer (usually 
`C:\Program Files (x86)\Steam\steamapps\common\ARK Survival Ascended`) and navigate to
`ShooterGame\Binaries\Win64\ShooterGame\Mods\83374`. Locate the folder with the Mod ID,
open it and delete the contents from within it. Extract the Mod client files from the 
zip (`MyMod-Windows.zip`) here.

### Server Setup
:::tip Install a Server

If you do not have a server setup already, follow the 
[Dedicated Server Setup](./server-setup.md) guide.

:::

Ensure the Mod is installed by the server by using `-mods=<ModId>` launch option using
the Mod ID. You only have to ensure the server is on the latest version of the Mod
before copying your files in. If this is a Mod ID for a Mod which rarely updates, you 
should only have to start the server to install the Mod once before replacing its files.

With the server in a state that it will not overwrite your locally cooked files on start,
open the location `ShooterGame\Binaries\Win64\ShooterGame\Mods\83374` and open the Mod ID
directory. Clear the contents from within it, and extract the contents of the locally
cooked server files from the server zip (`MyMod-WindowsServer.zip`). Start the server.

## CurseForge Cooked Mod
:::info Non-Uploader Testers

If you have other testers, add them as members on the Project Management dashboard, set
their role to Tester, and ensure `Cross-Platform Tester` permission is checked. They
will then be able to install the Mod when they join the server or via their game client.

:::

### Client Setup
If you are the owner/uploaded of the Mod, you will see the Mod in the game client under
`My Mods` and can install it there. Load up a single player game with the Mod, or setup
a server following the steps provided bellow.

### Server Setup
:::tip Install a Server

If you do not have a server setup already, follow the
[Dedicated Server Setup](./server-setup.md) guide.

:::

Install the Mod by launching the server with `-mods=<ModId>-dev` launch option using the
Mod ID. This will install the latest cooked build for the Mod.
