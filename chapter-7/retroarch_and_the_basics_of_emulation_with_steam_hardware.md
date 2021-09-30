# 7f Retroarch and the Basics of Emulation with Steam Hardware

## Expectations of This Guide

Before we begin I'd like to take the moment to set your expectations for this guide, this is meant to be as brief as possible and we will not be going very in-depth at all with how to set up individual emulators.

We will only be covering the very basics of getting RetroArch started and hooking properly to Steam Input with multiple different emulation cores. RetroArch was chosen specifically because it is a very versatile program and can cover a vast amount of generations without the need of going in depth of multiple different emulation programs.

As an example we will be going over emulation for Microsoft DOS for both its historical value to PC gaming as well as its slight extra complexity in terms of getting games running and mapped correctly within Steam Input.

**Because this guide is written well in advance of the Steam Deck's launch, as of now it will not be covering installation on Steam OS.**

# Disclaimer

In regards to files necessary for emulation such as BIOS copies and ROM files, please make sure that emulation does not violate the standards or law practices within your local region. **The Steam Input Wiki team does not advocate for software piracy.**

This guide will be written and maintained with the expectation that any files procured with the intention of emulating software were ripped and obtained legally through whatever means your local government provides you to do so.

## What Is RetroArch?

The first step for our emulation guide is to install RetroArch, a free open source front-end for Libretro, which is a modular emulation system that allows for cores that interconnect; each one designed and based on specific hardware systems.

For the simplicity of this guide we'll be using the Steam version I've RetroArch, which as of writing has just officially gone Gold.

### Install RetroArch

First we will go to Steam and search for RetroArch from the Steam catalogue.

Once we’ve found it, we will go ahead and click on install and it will be added to our library then begin downloading.

Before we leave the store page if you would like you can go ahead and install different cores from the DLC page. This is different from the normal open source variant of RetroArch in order to meet Valve's guidelines for having the emulation front-end on the store. But don't worry for any system cores that are not available; we will be covering how to get them.

Once RetroArch has finished installing we recommend you go ahead and try running it in order to make sure any software redistributables are installed and functioning before moving on.

**_!! CAUTION !!_** If you were attempting to install on Steam when running a 32-bit Operating System, Steam allows you to attempt to download it through Steam despite there not being support for 32-bit systems with the Steam release of RetroArch.

This can cause a myriad of problems The biggest of which being the program will download without an executable making it entirely inoperable.

If you are running a 32-bit system you will need to download it manually from either

https://www.libretro.com/

or the LibRetro repository on GitHub at

https://github.com/libretro/RetroArch

### Download and insert DOSBox Pure

For the sake of this example we're going to be downloading a fork of the popular emulator DOSBox called DOSBox Pure.

The latest pre-release can be found at

https://github.com/schellingb/dosbox-pure/releases

To find cores for other emulators you can find them at

https://buildbot.libretro.com/stable/

For the Steam version of RetroArch we will need to manually download it. This is because as stated earlier the Steam iteration of RetroArch only allows for specific cores to be downloaded as Steam DLC and currently DOSBox Pure is not available.

For those using this tutorial with the standalone release of RetroArch, you can download this within the program by going to Online Updater, selecting Core Downloader, and then finding and selecting DOS "DOSBox-Pure".

#### Manually Installing DOSBox Pure

Once we've downloaded our core we should receive a .zip file containing both a .info and a .dll file.

First take the .dll file and drop it in the and drop it into the cores directory within your RetroArch folder.

