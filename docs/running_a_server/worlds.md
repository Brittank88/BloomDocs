---
id: worlds
title: Managing Worlds
slug: /worlds
hide_title: true
hide_table_of_contents: true
sidebar_label: Managing Worlds
description: Learn how you can upload, export and manage your Minecraft worlds.
image: https://bloom.host/assets/images/logo.png
---

<div class="text--center">
<img src="https://bloom.host/logo-white.svg" alt="logo" height="50%" width="50%"/>
<h1>Managing Worlds</h1>
</div>

:::note
If you'd like to import ALL your files from another hosting company, please follow our [Server Importer](../using_the_panel/server-importer.md) guide instead!
:::

# Importing Worlds
Depending on your specific edition and world, there are a couple of methods of importing worlds.

## From Java Edition Single Player
If you have a single player world in Java Edition, this is what you need to do:

Open the single player menu and select your world. Then, press the 'Edit' button:
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/1.png').default} alt="img"/></div>

Here, press the 'Open World Folder' button:
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/2.png').default} alt="img"/></div>

Then, select all the files within the open directory and right click. Select 'Send To' and 'Compressed (zipped) folder':
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/3.png').default} alt="img"/></div>
You may get a warning about empty folders being skipped but that is okay!

Next, follow [our guide on connecting to your server with an SFTP client](../using_the_panel/sftp.md). In most cases, your world files will be fairly large, so it's best to use a dedicated file transfer protocol, instead of the built-in web file manager.
Once connected via SFTP, right click in SFTP and create a new folder, such as `my-world` and open it.
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/4.png').default} alt="img"/></div>

Drag & drop the ZIP file you created previously and wait until it finishes uploading.
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/5.gif').default} alt="img"/></div>

Once that's done, head over to the 'File Manager' tab of the panel and locate and your folder.
Within, press the '...' button next to your ZIP and click 'Unarchive'. This may also take a few minutes depending on the size of your server.
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/6.png').default} alt="img"/></div>

After unzipping, here is how it should generally look.
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/7.png').default} alt="img"/></div>

Now, if you'd like this to be your main world, open the `server.properties` file in the main directory of your server and ensure the `level-name=` setting matches with the folder that you created before:
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/8.png').default} alt="img"/></div>

Alternatively, if you'd like to use a plugin or mod such as [Multiverse-Core](../plugins_and_modifications/plugins/multiverse.md), you can import it using the folder's name.
In our example, for Multiverse-Core, you'd do `/mvimport my-world NORMAL`

That's it! Make sure to restart your server to apply the changes.

---

## From Java Realms
If you have a Minecraft Realm on Java Edition, this is what you need to do:

Open the Realm menu, select your Realm and press 'Configure':
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/9.png').default} alt="img"/></div>

Switch to the world you'd like to import to your Bloom server by clicking it, if you haven't already.
There press the 'World backups' button:
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/10.png').default} alt="img"/></div>

Lastly, press the 'Download latest' button which will download the very latest backup of your Realm to your single player saves folder: 
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/11.png').default} alt="img"/></div>

That's it! Now you can follow the ['From Java Edition Single Player'](#from-java-edition-single-player) chapter to import your Realm world!

---

## From Bedrock Edition Single Player
If you have a single player world in Bedrock Edition, this is what you need to do:  

Open the worlds list and press the edit button next to your desired world:
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/12.png').default} alt="img"/></div>

Scroll down to the very bottom of the main page and press 'Export World':
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/13.png').default} alt="img"/></div>

Select your desktop, or another easy to access location:
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/14.png').default} alt="img"/></div>

Next, follow [our guide on connecting to your server with an SFTP client](../using_the_panel/sftp.md). In most cases, your world files will be fairly large, so it's best to use a dedicated file transfer protocol, instead of the built-in web file manager.
Once connected via SFTP, open the `worlds` directory and create a new folder, such as `my-world` and open it.
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/15.png').default} alt="img"/></div>

Drag & drop the world file you exported previously and wait until it finishes uploading.
Once it does, rename it, so instead of ending in `.mcworld`, it ends in `.zip`. The rest of the name does not matter.
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/16.gif').default} alt="img"/></div>

Once that's done, head over to the 'File Manager' tab of the panel and locate and your folder in the `worlds` directory.
Then, press the '...' button next to your ZIP and click 'Unarchive'. This may also take a few minutes depending on the size of your server.
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/17.png').default} alt="img"/></div>

After unzipping, here is how it should generally look.
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/18.png').default} alt="img"/></div>

Lastly, open the `server.properties` file in the main directory of your server and ensure the `level-name=` setting matches with the folder that you created before:
<div class="text--center"><img src={require('../../static/imgs/running_a_server/worlds/8.png').default} alt="img"/></div>

That's it! Make sure to restart your server to apply the changes.

---

# Resetting Worlds
You can find our full guide on resetting your world [here](world-reset.md)!

<!--
// Todo:
---

# Exporting Worlds 

## To Java Single Player

## To Bedrock Single Player (`.mcworld`)

-->
