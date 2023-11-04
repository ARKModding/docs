# CurseForge Cooking
:::danger Login to CurseForge

Before continuing within ADK, visit [CurseForge](https://www.curseforge.com/login)
and login with Twitch, Discord, or Gmail. Failing to do so may require you to
contact CurseForge support to reset/consolidate your accounts.

:::

## Registering ADK with CurseForge
In the application menus, find `UGC` and select `Share Mod`

![UGC Share Mod](/img/docs/cooking/ugc-share-mod-menu.png)

This will pop a dialog which will request your email address.

![CurseForge ADK Registration](/img/docs/cooking/register-curse-forge.png)

Enter your email address and click continue. Check your email and open the link
provided in the email within the same browser you are logged into CurseForge
with. This will link ADK with your logged in CurseForge account.

:::info Reset ADK Registration

If, for some reason, you ever need to reset your ADK registration with CurseForge,
backup and delete the file located at 
`ARKDevKit\Projects\ShooterGame\Modes\.eternal\83374\user_info.json`

:::

## Cooking with CurseForge
### Upload Mod to CurseForge
Once you have registered, the `Share Mod` UGC menu will then present you with
the CurseForge Uploader.

![CurseForge Uploader - First Share](/img/docs/cooking/curse-forge-first-share.png)

1. Select the Platform for which the mod is intended to be used (at the time
of this writing, PC Only is the only available Platform).
2. Select which Mod folder to upload. 
3. Give the Mod a user-friendly name. This name is transformed to kebab casing and used
for the page slug. For example `My Awesome Mod` would be transformed to `my-awesome-mod`.
4. Provide an image of 400px by 400px or larger, while maintaining a 1:1 ratio (square).
5. Select the Mod's primary category (you can select secondaries on CurseForge's Website)
6. Provide a short description for CurseForge and in-game.
7. Provide a detailed description for CurseForge and in-game.
8. If you ever see this screen and this is an already uploaded mod, select this option
to the link of the existing mod.

When you are satisfied with your entries, click the `Continue` button to upload the mod.

:::warning Bad Image

If it fails to upload and provides a 4xx error, you may have provided an invalid image.
Check your image and try again.

:::

When the mod uploads, you should see a success dialog, as well as an Editor success
dialog

![CurseForge Upload Success](/img/docs/cooking/curse-forge-upload-success.png)
![ADK Upload Success](/img/docs/cooking/adk-upload-success.png)

Most importantly, is the Editor dialog success message. Upon success, click the
`Go To Project` button to open the Mod management page on CurseForge.

### Monitoring and Troubleshooting CurseForge Builds
Once you are on the Mod management page, navigate to the `Files` tab, and monitor
the uploaded file's cook status.

![CurseForge Mod Cooking](/img/docs/cooking/curse-forge-cooking.png)

Once the Mod has cooked successfully, you will be presented with a `Ready For Review`
status. Before publishing, you may want to [test the Mod](./testing). 

### Publishing
To publish the build, click the orange button with the file up-arrow icon that has 
`Publish Build` tooltip.

![CurseForge Publish Build](/img/docs/cooking/curse-forge-ready-for-review.png)

With a build published, you can now publish the project. Click the `Publish Project`
button at the top of the page, next to `Manage Project`.

Congratulations! You have now published a Mod!
