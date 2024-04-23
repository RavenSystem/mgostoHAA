# Shelly convert to HAA (old models)

[![Donate](https://img.shields.io/badge/donate-PayPal-blue.svg)](https://paypal.me/ravensystem)

[![Twitter](https://img.shields.io/twitter/follow/RavenSystem.svg?style=social)](https://twitter.com/RavenSystem)

[![Chat](https://img.shields.io/discord/594630635696553994?style=social)](https://discord.com/servers/esp-homekit-devices-594630635696553994)

<p align="center"><img width="300" src="https://raw.githubusercontent.com/RavenSystem/ravensystem-media/master/works-with-apple-home.svg"></p>

A minimal firmware for OTA (over the air) flashing HAA target firmware starting from Mongoose OS for old Shelly devices (gen1).

For newer Shelly devices (Plus, Pro and Mini), use this instead: [mgos32 to HAA](https://github.com/RavenSystem/mgos32toHAA)

:warning: **This is a third-party experimental project, without any relation with Shelly or Alterco. If you decide to try it, all is under your responsability :warning:**

Original repository at https://github.com/yaourdt/mgos-to-tasmota. This repository
is tailored to use HAA Latest Release Version only.

## Overview

This is an intermediate firmware that can be used to install [HAA HomeKit firmware](https://github.com/RavenSystem/esp-homekit-devices)
on various Shelly models. It will install the latest `fullhaaboot.bin` released version.

## Install

**Warning:** _This application should generally be safe to use for all supported
devices. Still, overwriting a device's bootloader via OTA update is a risky
operation. If something unexpected fails, your device may be bricked, unless you
know how to flash a new firmware over a wired connection._

**Warning:** _You can go back to Mongoose OS via OTA as well, using [this firmware](https://github.com/yaourdt/tasmota-to-mgos),
but be aware the application is still at an early stage. If something fails,
your device may be bricked, if you don't know how to flash a new firmware over
a wired connection._

Before flashing this firmware, connect your device to a WiFi network with
Internet access. From your browser, open the update URL for your device from the
table below. Replace `shellyip` with the IP address of your Shelly. The device
will restart one or two times and attempt to download. If this download
succeeds, the device will restart again, and you will see a new WiFi network
labeled `HAA-??????`. This process should take no longer than 4 - 5 minutes,
depending on your network connection.

If the download fails, or your internet connection is disrupted, simply turn the
device off and on again, the intermediate firmware will retry until it succeeds.

In the unlikely event that the WiFi credentials are wrong, the device will try
to connect to a backup WIFI with SSID _mgos-recover_ and password _RJoPuKC3u5_,
which you can use for recovery.

Device | Update URL
------ | ----------
Shelly 1        | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-Shelly1.zip`
Shelly 1PM      | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-Shelly1PM.zip`
Shelly 1L       | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-Shelly1L.zip`
Shelly Plug S   | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyPlugS.zip`
Shelly 2        | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-Shelly2.zip` 
Shelly 2.5      | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-Shelly25.zip`
Shelly RGBW2    | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyRGBW2.zip`
Shelly Dimmer 1 | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyDimmer1.zip`
Shelly Dimmer 2 | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyDimmer2.zip`
Shelly EM       | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyEM.zip`
Shelly Bulb     | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyBulb.zip`
Shelly Vintage  | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyVintage.zip`
Shelly Plug US  | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyPlugUS.zip`
Shelly Duo      | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyBulbDuo.zip`
Shelly H&T      | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyHT.zip`
Shelly i3       | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyI3.zip`
Shelly Plug 2   | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyPlug2.zip`
Shelly Uni      | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyUni.zip`
Shelly Duo RGBW | `http://shellyip/ota?url=http://mgostohaa.ravensystem.es/HAA-ShellyDuoRGBW.zip`

You must setup the MELPHAA script as your needs. [HAA Wiki](https://github.com/RavenSystem/esp-homekit-devices/wiki)

In addition to this firmware, you can obtain [**HAA Home Manager App**](https://github.com/RavenSystem/esp-homekit-devices/wiki/haa-home-manager), the perfect App companion
to manage your HAA devices, with batch updates, enable setup mode, and other extra features: 

<p align="center"><a href="https://apps.apple.com/app/id1556105121"><img src="https://raw.githubusercontent.com/RavenSystem/ravensystem-media/master/haamanager_app.png"></a></p>

If you want to measure the performance of your Apple Home, you can get [**Home Bench App**](https://github.com/RavenSystem/esp-homekit-devices/wiki/home-bench), the only App that performs speed tests directly over accessories using Apple HomeKit API: 

<p align="center"><a href="https://apps.apple.com/app/id6473729247"><img src="https://raw.githubusercontent.com/RavenSystem/ravensystem-media/master/homebench_app.png"></a></p>

And don't forget to subscribe to YouTube Channel:

<p align="center"><a href="https://www.youtube.com/channel/UCRumJzAoAnQ7dUpSnSUuuJw"><img width="40%" src="https://raw.githubusercontent.com/RavenSystem/ravensystem-media/master/YouTube_logo.png"></a></p>
