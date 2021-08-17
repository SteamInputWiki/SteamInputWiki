# Chapter 04: Changing Things Up

Sometimes, Bindings and Input Styles alone are not enough to either:

* Play the game well
* Fit your playstyle well
* Both of the above

Keyboard and mouse only games that have loads of keybindings often fit into that first category, while anything could fit in the second.

Regardless, when you encounter such a situation you might start wondering how it's possible to do what you want when all the inputs on your controller have already been taken.

In this chapter we’ll be showing you how you can drastically expand what your controller can do by using tools in Steam Input to change things up on the fly.

Steam Input gives you 4 tools to do this. They are:

* Activators
  * These change how your buttons work
* Modeshifts
  * These change how inputs that use Input Styles work
* Action Sets
  * These can be viewed like extra configurations you can swap to for entirely different playstyles, OR like different input “paradigms” for various contexts within the game (menu, on foot, in flight, etc)
* Action Layers
  * These are like Sets, only narrower in scope (if you only need to change a couple of things temporarily, unlike sets which are better for everything more permanently).

The rest of the sections in this Chapter will go over each of those tools in detail, explaining the settings to help you take as much advantage of them as you can.

## Chapter 04a: Activators

What is an Activator?

Press a button, and an action happens. Pressing a button causes an action to happen. It is an activator… but there is actually more to it than that.

Accessing the Activator page (pressing Select on your controller (or clicking on “Show Activators” if using a mouse) when on the Bindings page) gives you a lot of options for customizing both how pressing the button in different ways (yes, there are multiple ways to press a button) affects the outcome, as well as how the outcome itself functions. You can even add multiple activators to the same button, to really push what is possible in your config!

Let’s start with the “Activation Type” drop down found at the top of the left column of the Activator settings. As the hover over description says, this determines how the button actually works.

* Regular Press
  * This Activation Type acts how you think a button would normally act: When you press the button, output is sent for as long as the button is held and stops being sent when you release the button. This is the default Activation Type for all bindings.
* Double Press
  * This Activation Type acts similarly to Regular Press, however you must press the button twice in rapid succession before output is sent. The same “outputs as long as the button is held” rule applies to the second press. How quickly you have to double press the input to activate the output is a setting that can be adjusted.
* Long Press
  * This Activation Type acts similarly to Regular Press, however the button must be held for a duration of time before output is sent. The same “outputs as long as the button is held” rule applies once the duration has elapsed. How long you must hold the input to activate the output is a setting that can be adjusted.
* Start Press
  * This Activation Type acts differently. It sends output when the button is first pressed, but immediately deactivates. Another way to think of it may be as a “One Shot” output that fires when you push the button and is not continuous.
* Release Press
  * This Activation Type acts differently. It sends output when the button is released, and then immediately deactivates. Another way to think of it may be as a “One Shot” output that fires when you release the button and is not continuous.
* Chorded Press
  * This Activation Type acts similarly to Regular Press, however it requires another button be pressed first and held when you press the button that has the Chorded Activator on it. This sounds complicated, so think of it this way; If you want the A button to output A when you press it on its own, but want it to output something else when you are holding the Right Bumper, then the Chorded Activator is for you. The same “outputs as long as the button is held” rule applies, however the output is released if EITHER button is released.

[ Mennenth’s editor notes not to be included in final wiki: I plan on drawing out a table of graphs with button and binding on/off states as the x axis and time as the y axis to better help people visualize how the various activators work. ]

Underneath Activation Type is the Binding. This takes you to the Binding Page to assign the Activator a binding as per normal.

From there, almost all other settings determine how the Binding itself acts once triggered. We’ll go over these top to bottom and left to right.

* Double Tap Time 
  * This slider is only available for the Double Press Activation Type. It determines how fast you must double tap to get output. The more to the left this slider is, the faster you have to tap. The more to the right the slider is, the more time you have.
* Long Press Time
  * This slider is only available for the Long Press Activation Type. It determines how long you have to hold the button to get output. The more to the left this slider is, the shorter the length of time you need to hold the button. The more to the right this slider is, the longer you must hold the button to get output.
* Chorded Button
  * This drop down menu is only available for the Chorded Press Activation Type. This allows you to choose which button you have to hold in order for the Chord to work.
* Toggle
  * This setting is available to all Activation Types. All buttons on controllers are typically “momentary” i.e. when you release the button the output stops. Toggle makes the activator act more like a light switch; even if you release the button, the output will remain until you press the button again which toggles the output back off. 
  * !! CAUTION !! You do have to be mindful of what is being toggled and how the game reacts to receiving multiple of the same button. If you toggle Shift to be on with, say, the Right Bumper but then Shift is also on your Left Grip button and the game reacts to seeing two instances of Shift by canceling them out, then you can run into issues where the Activator is still toggled on but the game isn’t accepting its Shift. Then when you press your Right Bumper again, that simply toggles the Activator back off again so the game doesn’t even see a Shift. You would then need to press Right Bumper *again* to toggle Shift back on in a way the game will see and respond to it. It is a little wonky, but if you keep this in mind then you shouldn’t have too many issues with it.
* Interruptible
  * This setting is ONLY available to the Regular Press, Release Press, and Chorded Press Activation Types. If set to OFF, then this activator will ALWAYS happen if its conditions are met. If set to ON, then if a Double Press or a Long Press activator are on the same button it changes the behaviour of the Activator. Regular Press and Chorded Press Activators will wait to activate until after the Double Tap or Long Press time has elapsed, and will NOT activate if the Double or Long Press does get activated. An example to help demonstrate this would be Dark Souls’ Dodge and Sprint actions, which are both on the B button. Sprint is activated if you hold down B for a certain length of time. Your character only Dodges if you release the B button before your character starts Sprinting. Dodge is therefore like a Regular Press activator with interruptible set to ON, and Sprint is like a Long Press activator assigned to the same button. Release Press Activators set to Interruptible will not activate until after the Double Tap Time has elapsed.
* Fire Start Delay
  * This is available to all Activation Types. It Delays sending the output by a small amount of time, though the total amount of “up time” remains the same. This is useful in multi-activator arrangements to form something similar to macros.
* Fire End Delay
  * This is available to all Activation Types. Once the binding has been deactivated, this delays when it stops sending output by a small amount of time increasing the total amount of “up time”. This is useful in similar multi-activator arrangements to form something similar to macros, when a binding needs to be held while others are happening.
* Haptics Intensity
  * This setting is available to all Activation Types, though currently only works for the Steam Controller. This setting determines if activating the binding should pulse the haptics and how hard the haptics should pulse. It is useful for getting feedback for when a non button binding (ie: outer ring binding on a touchpad or joystick) is activated, as the haptic pulse in those situations takes the place of the more traditional click of a button. If the activator is on a physical button, setting this to OFF is recommended as buttons have their own innate feedback.
* Cycle Binding
  * This setting is available to all Activation Types, though is only useful if a single Activator has multiple bindings assigned to it via the bindings page. If turned OFF, all the bindings assigned get sent at the same time. If turned ON, then only one binding is sent per activation. Each time the Activator triggers, the next binding gets sent. It sends them in the sequence they were assigned when utilizing the multi-binding option, so be mindful of how you are assigning the bindings if you intend to use this setting.
* Hold To Repeat (Turbo)
  * This setting is NOT available to Start Press and Release Press, but IS available to all other Activation Types. When set to OFF, the output will act normally. However, if set to ON then Turbo is enabled for that output. Turbo rapidly pulses the binding off and back on again for the duration the Activator is on.
* Repeat Rate
  * This setting is only available to Activation Types that have Turbo available. It determines how fast the binding is repeated. When to the left the repeat rate is slow, when to the right the repeat rate is fast.

[ Mennenth’s Notes: With the Toggle setting, you can change an action in game that is hard coded as a Hold to a Toggle. But, what if you wanted to change a hard coded Toggle into a Hold? You would actually use 2 separate activators with the same binding; one as a Start Press activator, and one as a Release Press activator. ]

## Chapter 04b Modeshifts

What are Modeshifts?

Let’s say that your Right Joystick is in joystick mode for controlling the camera, but when you hold Left Bumper it becomes a Radial Menu for extra bindings. A lot of modern games do this to bring up a “weapon wheel” while slowing the game down so you can change what weapon you are using. This is where Modeshifts come in.

Each device that can use an Input Style can have a single modeshift associated with it. You can find where to configure the Mode Shifting on the settings page for Input Styles. It will always be the top of the right column of settings.

When you click that box, you are brought to another Input Style settings page that is blank except for two things; Style of Input in the top of the left column of settings, and in the top of the right column of settings “Mode Shifting” has been replaced with “Mode Shift Button”.

Opening up the Style of Input drop down and selecting an Input Style then populates the rest of the page with settings for that style.

Opening up the Mode Shift Button drop down then allows you to choose which button you must hold down for the Mode Shift to happen.

So in the opening example, your Right Joystick would start off as a normal Joystick. Then you would click on Modeshifting, change the Input Style to Radial Menu, select Left Bumper for the Mode Shift Button, and fill out the Radial Menu with all the bindings you want to access with the Right Joystick while you are holding Left Bumper.

### Mennenth’s Notes: 

As mentioned, each input device can only have ONE modeshift associated with it. I would reserve this for things of high priority, such as but not limited to weapon select wheels if the game doesn’t already provide you with one.

I would also recommend going to the Bindings page of the button being used for the modeshift, setting its normal function to be interruptible, and adding a Long Press activator with the EMPTY binding. For the above example, this will allow you to press and release Left Bumper for any normal functions Left Bumper has - say throwing a grenade - but when you hold Left Bumper the only thing that activates is the Mode Shift. No more unintentional grenade throwing when you want to access your weapon wheel!

Finally, the weapon wheel example was specifically chosen because this is a place where the touchpad of the Steam Controller can flex a bit. By assigning the Right Touchpads own click as the Mode Shift Button, the Right Touchpad can be in mouse mode but have the weapon wheel “under” it accessed by clicking the pad itself with no need to involve other buttons. This can also be used in mmo’s to mimic the mmo mice with 12 buttons on the side.

## Chapter 04c Action Sets

What are Action Sets?

Let’s say you want to pack multiple control schemes into a single configuration, whether that be for the purposes of using different Heroes in Hero shooters, or maybe to differentiate your Menu controls from your In Game controls (and as a developer who is implementing SIAPI you want to automate this “context switching” (recommended)), or any of a number of reasons.

Action Sets allow you to do those things.

When you first load a default config, especially from the Templates, there typically will be no Action Sets configured. You can easily add Action Sets by clicking the “Add Action Set” button at the top of the configuration overview screen.

Upon clicking that button, you can name your new Action Set as well as copy over an existing Action Set into the new one if you only want to make a handful of changes.

Once you have created a new Action Set, you will see two new buttons to the left of the Add Action Set button. The one all the way to the left will typically be named “Default”, and to the right of that will be your new Action Set.

Highlighting one of them and pressing Select/Back on your controller (or by clicking on “Manage Action Set'' at the bottom of the screen when using a mouse) brings up options for managing the Action Set.

Those options include:

* Being able to rename the Action Set
* Deleting the Action Set

And 2 other options.

“Action Set to switch to when the cursor is shown/hidden” are options that try to give the player some limited form of automatically swapping between 2 Action Sets. To understand how this works, let’s consider any of a number of modern first person shooters.

When you are in game shooting things, the mouse cursor is often hidden. But if you are in a menu, some games will allow you to navigate that menu and interact with it via mouse, in which case the mouse cursor will be shown.

In those cases, and more importantly if the game uses the hardware cursor instead of a software cursor (devs take note), you can take advantage of those options so your Mouse Input Style mouse sensitivity can be as high as you’d like for in game without negatively impacting your ability to use the mouse to navigate the games menu.

But what if the game does not use the hardware cursor OR you want to use Action Sets for something other than automatically swapping between menu and in game sets?

Then you’ll have to manually swap between the Action Sets. This is done with the “Change Action Set” binding. This binding is found on the Bindings page, as the leftmost option in the top right row of bindings. That row is next to the text entry for naming the binding. The icon for the Change Action Set binding is a stack of 3 circles and two arrows - one that is pointing from the top circle to the bottom circle and the other is opposite. This binding is also only visible if the configuration has more than 1 Action Set (or has more than 0 Action Layers, more on Layers in the next section).

When you first select that icon, a dialog box will appear asking you to “Select Action Option”. Change the drop down to “Change Action Set” if needed, and click OK.

A second dialog box will appear with 3 options.

Change the drop to either the Action Set you want to immediately swap to when activating the binding, or “Next/Previous Action Set”. Next swaps to the next Action Set based on the list of Action Sets at the top of the configuration overview page, and Previous swaps to the last used Action Set.

Then there are two more options

* Display Action Set on Change
  * If the big picture overlay is being used, a notification will pop up on screen whenever you swap to an Action Set, letting you know which Action Set you are currently using.
* Beep on Change
  * This option works regardless of what overlay you are using. It activates the haptics in a way they audibly beep or chirp, to give you feedback on when you have swapped Action Sets

Check or uncheck those options depending on how you want this binding to behave, then click OK. That will take you back to the configuration overview, where you will see “CHANGE TO <Action Set Name>” on the button that you put the binding on.

Mennenth's Notes: not to be placed in actual wiki, this is a note to remind me that I need to test it and report back; I’m pretty sure swapping action sets interrupts several inputs which could theoretically lead to quirky behaviour. Layers have the same issue iirc. This needs to be fully tested and any quirky behaviour documents

## Chapter 04d Action Layers

What are Action Layers?

Action Layers are like a mix between Action Sets and Modeshifts. They can be more permanent than Modeshifts, but are smaller in scope than Sets. You can also kind of think of them like layers in photo editing software such as Photoshop, hence their name.

Layers enable you to change some things within a Set while leaving most things alone. Action Layers are also specific to their Action Set, or put another way each Set can have their own Layers.

You might consider using a Layer if the input you want to change already has a Modeshift due to the “1 Modeshift per Input” restriction, for being able to dynamically invert the y axis of a Joystick if the game pulls a “your controls are inverted now” move, or for any number of other reasons where you’d like to change your inputs but otherwise can’t use modeshifts and sets are a bit too much for the job.

When you first load a default config, especially from the Templates, there typically will be no Action Layers configured. You can create Action Layers using the “Add Action Layer” button towards the top of the configuration overview page. Clicking that button brings up a dialog box where you can name your new Action Layer, and clicking okay again adds a new button to the left of the “Add Action Layer” button that allows you to configure the inputs for that layer.

When you first click that Action Layer, all the inputs will become greyed out. Don’t panic, this is just to show you that the layer is currently not changing anything. If you change something within the layer, that input will then light up again on the configuration overview to let you know something about that input has been changed.

Clicking a Layer and pressing Select/Back on your controller (or by clicking on “Manage Action Set'' at the bottom of the screen when using a mouse) brings up options for managing the Action Layer. This allows you to either rename or delete the Action Layer.

Changing Input Styles and buttons/bindings on the surface level is easy; select the input device you want to change, and make those changes.

Changing Activators gets a little more complicated.

When you first enter the Activators page while in a layer, almost all of it will be greyed out and unselectable. The only thing you can do is click on “Add Activator”, which will bring up a dialog box.

That dialog box allows you to choose if you want to override all Activators that the base Action Set has (by clicking OK) or if you want to bring the activators over to the Layer (by clicking “Copy Activators”). 

Okay so, you’ve configured the Layer to make the changes you want. How do you now access that Layer while in game?

Unlike Sets, Layers have no mechanism for automatically adding or removing them (unless you are a developer implementing SIAPI, but I would personally discourage you from automatically managing Layers as they are a powerful tool for the player to use to customize their configurations). This has to be done manually.

This is done with one of 3 bindings. They are found on the Bindings page, as the leftmost option in the top right row of bindings. That row is next to the text entry for naming the binding. The icon for the binding is a stack of 3 circles and two arrows - one that is pointing from the top circle to the bottom circle and the other is opposite. This binding is also only visible if the configuration has more than 0 Action Layers (or has more than 1 Action Sets, more on Sets in the previous section).

When you first select that binding, it will open a dialog box with a drop down menu. That menu defaults to “Change Action Set” even if there are no other sets. But for Action Layers, there are 3 more options in that drop down.

* Hold Action Layer
  * When set to this, the Layer will be active for as long as the button is being held.
  * !! CAUTION !! If in that Layer you also change what the button does, this could result in the Layer becoming “stuck” as it would no longer see when the Hold ends. Be mindful of what you are doing in the layer. If you want to change what the button does but still have the layer get removed on release of the button, then you’ll likely want to use a combination of the other two options.
* Apply Action Layer
  * This option simply applies the chosen Layer. You will have to manually remove the Layer at a later time.
* Remove Action Layer
  * This option simply removes the chosen Layer.
  * !! Trick !! Going off the previous caution, if you want the functionality of the “Hold Action Layer” option but also intend to do something different with the button, put “Remove Action Layer” on a Release Press activator on that button. That should clear up any “stuck Layer” issues.

Once you have selected an option and clicked “OK”, another dialog box will appear. In this dialog box you can select which Layer you are working with

There will also be 2 other options.

* Display Action Set on Change
  * If the big picture overlay is being used, a notification will pop up on screen whenever you apply or remove an Action Layer, letting you know which Action Layer you are currently using.
* Beep on Change
  * This option works regardless of what overlay you are using. It activates the haptics in a way they audibly beep or chirp, to give you feedback on when you have applied or removed an Action Layer

Check or uncheck those options depending on how you want this binding to behave, then click OK. That will take you back to the configuration overview, where you will see “<HOLD/APPLY/REMOVE> <Action Layer Name>” on the button that you put the binding on.

Mennenth’s Notes: not to be placed in actual wiki, this is a note to remind me that I need to test it and report back; I’m pretty sure swapping action sets interrupts several inputs which could theoretically lead to quirky behaviour. Layers have the same issue iirc. This needs to be fully tested and any quirky behaviour documents
