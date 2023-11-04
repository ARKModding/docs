# Persistent PIE
To enable persistent PIE, a few things must be done.

Open the `ARKDevKit` directory in File Explorer, and copy `RunEditorSDK.bat` so that
the modifications are not lost with DevKit updates. Name the file 
`RunPersistentEditorSDK.bat`. Add `-ForceLoad` and `-ForceSave` to the argument list.

```batch title="RunPersistentEditorSDK.bat"
call "%~dp0Engine\Binaries\Win64\ShooterGameEditor.exe" "%~dp0Projects\ShooterGame\ShooterGame.uproject" -ForceLoad -ForceSave -Installed -AllowPCG -log -DontBuildEditorGrass -NetDriverOverrides=/Script/OnlineSubsystemUtils.IpNetDriver
exit
```

Launch ADK using this new `.bat` file when testing with Persistent PIE. 

With ADK open, open the World Settings (Window -> World Settings) and enable
`Play Persistent Player`.

![Persistent PIE - Play Persistent Player](/img/docs/persistent-pie.png)

Persistence is now enabled in ADK.
