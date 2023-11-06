---
sidebar_position: 40
title: 4. Initial Setup
---

# Initial setup for Docusaurus

Our ARK Modding Documentation uses a tool called [Docusaurus](https://docusaurus.io/) which allows us to write our documentation in special plain text files called [markdown files](https://www.markdownguide.org/), which is low maintainance and convenient.

Additionally, Docusaurus allows to instantly preview changes locally to see how they will look on the online site before you submit them to the ARK Modding team.

## Installing NodeJS

Docusaurus requires the NodeJS runtime, so you will need to install it on your machine. You can download it from the [official NodeJS website](https://nodejs.org/en/download/) and simply follow the setup instructions.

## Preparing Docusaurus

When running Docusaurus for the first time you need to initialize it, which requires a few simple copy-paste console commands. 

1. Open a terminal / console window on your machine
    
    :::tip
    In Windows 11 and most modern linux distributions you can simply right-click the file explorer in the folder where you cloned the repository and select "Show More Options", then "Open in Terminal". You can then skip step 2.
    :::

    :::tip
    On older Windows systems and some linux distributions you can usually do the same by shift-right-clicking in the folder.
    :::

2. Change your directory to the cloned repository's location on your machine using the command `cd full/path/to/your/cloned/repository`, e.g. `cd C:/repos/arkmodding` or `cd /home/myuser/repos/arkmodding`.

3. Run the following commands one after the other, confirming each with the "Enter" key:
   1. `corepack enable`
   2. `yarn init -2`
   3. `yarn set version stable`
   4. `yarn install`
   
   :::info
   This process can take a few seconds, but usually finishes quickly.
   :::

## Running Docusaurus

After this initial setup you can run Docusaurus with the command `yarn start` in the same terminal window. This will start a local webserver on your machine and open a browser window with the documentation site.

