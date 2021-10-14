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

By default this should be under
[Placeholder]

Next within the same directory assuming you do not already have a folder called "info" create one.

Then take your .info file and drop it in.

At this point you should now be able to load up your core successfully from within RetroArch as well as mounting content to it.

## Adding our game to Steam

Now we're going to cover how we can take our ROM or in the case of DOSbox our program that we packaged as a .zip file and add it to Steam.

By using the following steps we can make slight alterations for different emulators as well as different types of files.

Not all emulators will support .zip files or .rar files, however DOSbox Pure specifically does have support for .zip files. I've chosen to package my CDs as .zip files, however optionally you can rip them as .bin and .cue files as well so you will still have the option for CD audio.

Another option supported by DOSBox Pure is to rename our .zip files to .dosz once they've been packaged as zip files. This will give us the added benefit of allowing us to properly mount files using the Disk Control menu yet will still allow them to be properly read within DOSBox Pure.

#### GOG and other distribution platforms

Copies of games from digital online platforms can become fairly murky. Obviously it seems much easier because it's already in a digital format, however in practice there is no way to specifically tell how your game is going to be distributed after purchasing it.

Some games are already packaged with DOSbox seeing as it is an open source emulator, others however may not necessarily be as easy to add. 

### Add an Shortcut for RetroArch to Steam

Next we're going to add a Shortcut for RetroArch, this is not actually going to be used to enter RetroArch, but instead has a basis for the Shortcut that will allow us to use our game.

At the bottom left corner of Steam you're going to see a plus icon.

Click on the icon and select the option to "Add a Non-Steam Game".

This will bring up a list of programs Steam is able to index from your computer.

If you don't see retroarch.exe on this list click on the browse option and make your way to the Steam Library directory where you have installed RetroArch and open it within the dialog box.

### linking the Shortcut to our ROM

Either right click the Shortcut we just made within steam and select Properties or left click on the Options Cog to the right under the Shortcut's page within Steam then select Properties.

Now click on the text box under the name Launch Properties.

Here we are going to be adding a Launch Command that will allow us to tell RetroArch what Core we wish to load as well as what content we want to load with it.

Copy and paste the following Command structure
"path\to\retroarch.exe -L cores\<corename>.dll "path\to\<romname>.zip"
into the text box.

Next copy the directory you see in the Target text box and paste it in place of "path\to\retroarch.exe".

Next for this tutorial replace <corename> with "dosbox_pure_libretro" or optionally we could use the name of any other Core available in RetroArch in order to use said respective emulator.

Finally replace "path\to\<romname>.zip" with the Directory Path to the ROM we wish to use.

Once finished the Command should look something like this
[Placeholder]

From here the Shortcut should be usable and should open up our respective ROM.

#### a brief overview of Shortcut customization
  
Before you close the Launch Properties box you can choose to give the Shortcut a new name that better reflects the game you're adding to Steam.

From here if you'd like you can go one step further and add images to customize this Shortcut within your Steam Library.

I would recommend using
https://www.steamgriddb.com/
to find a Grid Poster, Grid Banner, Hero, Logo, and Icon for your respective game.

## Configuring controls within RetroArch
  
Now that we've got our games hooking directly into Steam it's time to discuss how to best configure for our selected Core.

Some of what we discuss will be applicable to every Emulation Core while other features are only available in DOSBox Pure.

### fiddling with the overlay
  
The first thing we recommend is making sure that once your game has booted you can still notice the Steam Overlay popping up.

If it does not I would recommend trying a different combination of video APIs under RetroArch's settings, however with the complexity of this I can't give you specifics on how to get it working. Under normal circumstances the Overlay should be hooking correctly, however under certain circumstances I've noticed that RetroArch can be finicky.

It's also important to make sure that you're using the Steam Big Picture Overlay if you wish to customize your controls within Steam easier as well as use features that are Steam Overlay dependent.

### default controls behavior within DOSBox Pure
  
The reason I've decided to go with those DOSBox Pure is mostly based around its unique Gamepad mapping system.

By default any games that have been indexed will have pre-applied mappings. These have all been standardized and work great out of the box with most traditional layout controllers.

While it is possible to use these automatic layouts with the Steam Controller they're not always ideal and none of them are pre-configured for analog input due to the complexity of Joystick support at that time.

For those using the Steam Deck you may want to continue following along, but for those using the vast majority of Steam Input supported Controllers you may decide to use these default controls.

### emulated input hardware within RetroArch

RetroArch gives us the ability to use our modern Gamepads as though they were plugged into the virtual ports on our emulated console. We will be exploring the basics on how to configure your Gamepad within the RetroArch settings.

The next section of the tutorial we will be talking specifically about DOSBox and getting Analog Movement working, however this should teach you how you can select different devices for different emulators and make changes to controls.

It is important to know that by default not every emulator is set up properly out of the box. 

For example PCSX ReARMed needs us to change our device type out the gate to one of the supported PlayStation Controllers otherwise Inputs aren't seen.

#### getting analog movement working in DOS games
  
Lets go ahead and open the Steam Shortcut we’ve just made.

Once booted we need to head to the RetroArch Quick Menu. By default "F1" is the menu hotkey and if enabled you can also use "Start + Select" on Gamepad.

From here move down and select the Controls option from the menu.

For the sake of this tutorial we're going to be selecting Port 1 Controls.

From this menu you can do several things but the thing I'd like to teach is how to emulate an analog DOS joystick.

Click left or right on your Gamepad with device type highlighted until you see the joystick option you'd like to use. What you should use will depend entirely on the specific game that you're trying to set controls up for.

Please keep in mind not all DOS games support Joysticks so you will be completely at the mercy of whatever game you'd like to play.

For my game I'm going to select First DOS Joystick (2 Axes, 2 Buttons). It's important to keep in mind that due to the limitations of DirectInput devices, no matter how you bind your controller you will always be missing Axes.

By default we do not need to save a Game or a Core Remap File however it is an option and if you're not sure how RetroArch has been configured The safest option is to save a Game Remap File.

Our next step is to resume the game so that we can begin to configure our Emulated Joystick within our DOS program.

At this point our game most likely does not have a binding for our Joystick so we may need to navigate the menu using Mouse and Keyboard. It's also important to note not all games allow navigation with Joysticks; this is something that you'll have to take into account.

You most likely need to press "Scroll Lock" to enable Game Focus so that we can use our keyboard within the program

Often we should be able to find controls in our Options Menu however some games of the era also required you to enable your controls when making your User Profile.

Often the options menu will consist of a checklist of supported hardware, if your game has an option to enable a joystick click it.

Most games will now ask you to calibrate your Joystick. Follow the on screen prompts.

Assuming everything went correctly you should now have the option to modify your Joystick bindings within the game as well as use it during gameplay.

From here you can modify your controls within Steam safe in the fact that you now have working Analog support for this particular title. The only downside to being the fact that every single DOS game requires individual configuration if you'd like to go the Analog route.

**_!! CAUTION !!_** Not every DOS game will bind without issue. My copy of Descent as an example would rarely accept calibration making it incredibly difficult to get set up. After setup sometimes the Emulated COM Port would fail to be found.

If you find any issues that can't be worked through I recommend trying different flavors of DOSBox or looking for an Open Source Port of your problematic game.
