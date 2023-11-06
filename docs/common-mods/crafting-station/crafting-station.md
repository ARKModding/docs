# Crafting Station

:::danger Initial Mod Folder Creation Required
The assumption is you've already created your mod folder, Primal Game Data and Mod Data Asset before proceeding.
:::

## Intro
The essentials required to create a crafting station are as follows:
- A structure, the building you see in the world.
- A inventory component, to control what is inside(slot count, craftables, etc).
- An item, to place the structure.
- An engram, to learn the item.

## Step 1 - Create The Structure
- RClick in your mod folder and create a new Blueprint Class
- Use the parent class `StructureItemContainerBaseBP`
- Name it something sensible.
- Use the following settings for Class Defaults
    - Static Mesh
    - Auto Activate Container
    - Descriptive Name
    - Use Placement Collision Check

![Structure Defaults](/img/docs/common-mods/crafting-station/StructureDefaults.png)

:::info
I turned Use Placement Collision Check off just to simplify the process. Normally you would leave it on and adjust the placement settings, otherwise this structure can collide with all other building pieces.
:::

## Step 2 - Create Inventory Component
- RClick in your mod folder and create a new Blueprint Class
- Use the parent class `PrimalInventoryComponent`
- Name it something sensible
- Use the following settings for Class Defaults
    - Allow Remote Crafting
    - Use Craft Queue
    - Remote Inventory Description String
    - Default Inventory Items
        - Add any items you want to be craftable in here
    - Inventory Name Override
    - All Default Inventory Is Engrams
    - Force Allow Crafting For Inventory Components
        - Add any `InventoryComponent` classes you want to force allow to be craftable in here

![Inventory Component Defaults](/img/docs/common-mods/crafting-station/InventoryComponentDefaults.png)

:::info
You do not need Force Allow Crafting for Inventory Components to be used, unless you're adding items that normally require being crafted in other inventories. ie. Metal Hatchet and the Smithy
:::

## Step 3 - Create The Primal Item
- RClick in your mod folder and create a new Blueprint Class
- Use the parent class `PrimalItemStructureGeneric`
- Name it something sensible
- Use the following settings for Class Defaults
    - Descriptive Name Base
    - Item Description
    - Item Icon
    - Structure To Build
        - This is the Structure Blueprint created in step 1

![Primal Item Defaults](/img/docs/common-mods/crafting-station/PrimalItemDefaults.png)

:::info
There are likely other settings you will want to play with to get it to your like(crafting requirements, icon, name, etc).
:::

## Step 4 - Create The Engram Entry
- RClick in your mod folder and create a new Blueprint Class
- Use the parent class `PrimalEngramEntry`
- Name it something sensible
- Use the following settings for Class Defaults
    - Required Character Level
    - Required Engram Points
    - Give Blueprint to Player Inventory
    - Can Be Manually Unlocked
    - Blue Print Entry
        - This is the item created in step 3

![Engram Entry Defaults](/img/docs/common-mods/crafting-station/EngramDefaults.png)

:::info
Give Blueprint to Play Inventory allows the item to be crafted in your inventory
:::

## Step 5 - Add Inventory Component to Structure
- Open Structure blueprint.
- Click Add in the Components window.
- Select your newly created inventory component.

![Add Inventory Comp to Structure](/img/docs/common-mods/crafting-station/AddInventoryToStructure.png)

## Step 6 - ModDataAsset Config
- Open your `ModDataAsset(MDA)` blueprint in your root mod folder
- Add the following fields
    - Additional Engram Blueprint Classes
        - The EngramEntry from step 4
    - Additional Structures to Place
        - The Structure from step 1
    - Additional Structure Engrams

![ModDataAsset Settings](/img/docs/common-mods/crafting-station/ModDataAsset.png)

:::info
If you want your item to be crafted in a vanilla container, <ins>Additional Structure Engrams</ins> is the field to add it to. You fill in <ins>For Class</ins> with the Structure you want to add it to(ie: StorageBox_AnvilBench) and the Item you want to add to it(ie: your newly created PrimalItem)
:::

## --- Results ---

## Engrams
![ModDataAsset Settings](/img/docs/common-mods/crafting-station/Engram.png)

## Structure Player Inventory
![ModDataAsset Settings](/img/docs/common-mods/crafting-station/CraftableInInventory.png)

## tructure Vanilla Smithy
![ModDataAsset Settings](/img/docs/common-mods/crafting-station/CraftableInVanillaContainer.png)

## Vanilla Items in Custom Structure
![ModDataAsset Settings](/img/docs/common-mods/crafting-station/AddVanillaItemToCustomStructure.png)