---
id: spark
title: Taking a Spark Profile
slug: /spark
hide_title: true
hide_table_of_contents: true
sidebar_label: Taking a Spark Profile
description: How to run a Spark profile to identify causes of lag on your server.
keywords:
  - Spark
  - Performance
  - Spigot
  - Paper
  - Bloom.host
  - Bloom.host
  - Pterodactyl Panel
  - Minecraft
image: https://bloom.host/assets/images/logo.png
---

<div class="text--center">
<img src="https://bloom.host/logo-white.svg" alt="logo" height="50%" width="50%"/>
<h1>Spark</h1>
</div>

### What does the plugin do?
Spark is a performance profiling plugin (with limited availability for Forge and Fabric) that can display server information, such as TPS, memory, tick durations, CPU usage, and disk usage. But more importantly it can create a performance profile that can be viewed on a fully feature web interface.
It does not require any configuration and is incredibly easy to install.

### Setup
:::note
You can ignore this step if you are running Purpur 1.19.1 or above.
:::
Download the latest build from [Spark](https://spark.lucko.me/download) and drop it into your plugins (or mod folder if you are running Forge/Fabric) folder. Turn on or restart the server, and you're done! If you need help installing plugins, check [How to install plugins](https://docs.bloom.host/installing-plugins).

## Using The Profiler
The most useful tool in terms of diagnostics is the profiler feature which can be run with `/spark profile start`.

Usually you'll want to run the profile during a time of stress for your server, to get the most out of the report you should try to leave it running for 10 minutes or more. You can also add additional parameters to the report, for more information check the [Spark Documentation](https://spark.lucko.me/docs/Command-Usage)

Once you are ready to check the results of the profiler you should run `/spark profile stop` and copy the link produeced.

When you open the link you'll find a useful web interface that displays all the data collected.

<div class="text--center">
<img src={require('../../static/imgs/running_a_server/spark/1.png').default} alt="img"/></div>

## Other Useful Commands

Running `/tps` will display an output that looks like this:

<div class="text--center">
<img src={require('../../static/imgs/running_a_server/spark/2.png').default} alt="img"/></div>

Running `/spark healthreport` will display an output that looks like this:

<div class="text--center">
<img src={require('../../static/imgs/running_a_server/spark/3.png').default} alt="img"/></div>

The values will depend on your server, newer versions of Spark will contain more useful information, as the utility is in active development.

For more parameters to use, and other useful commands you can check the [Official Spark Documentation](https://spark.lucko.me/docs/Command-Usage)

## Need Help Reading the Profile?

If you require help with reading your Spark profile, create a ticket in [Bloom.host Discord!](https://discord.gg/bloom).

## Info

[Spark's Official Website](https://spark.lucko.me/)
[Github](https://github.com/lucko/spark)
