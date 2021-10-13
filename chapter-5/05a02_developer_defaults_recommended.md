# 05a02: Developer Defaults/Recommended

Valve encourages developers to create a Default Configuration/Recommended for their game. This configuration would be applied by default. Ideally, this should enable the game to be played with any controller that has been opted into Steams controller support out of the gate. 

Developers can also make several configurations, apply one as a default, and then have the others available to the user to select if they want a different control scheme without going through too much hassle.

You can access the Developer Default/Recommended configuration(s) by clicking on the “Browse Configs” button at the bottom of the Configuration Overview page. This takes you to the “Controller Configurations - Import” page, and “Recommended” is the first category that is selected. This category has the Developer Defaults/Recommended configurations for the game.

NOTE: Having a Developer Default configuration does NOT mean the game has implemented the Steam Input API, though games that do implement the API will have a Developer Default/Recommended configuration as a matter of course.

There are actually two types of Developer Default/Recommended configuration(s)

* The Developer has put effort into creating a configuration to better suit their game depending on what controller you are using. This is by no means an exhaustive list, but here are a few examples:
  * FromSoftware created 4 configurations for Dark Souls 3 the Steam Controller. Each one takes advantage of one of the Steam Controllers unique features, such as dual stage triggers or the common trick of “modeshift clicks” on the right touch pad (which will be fully explained in the tips and tricks section of this chapter).
  * Witch Beam created 2 configurations for Assault Android Cactus for the Steam Controller. One of them uses the Mouse Region Input Style on the Right Touch Pad for better Right Touch Pad controls considering it is a twin stick shooter and the Right Touch Pad is not a Right Joystick.
  * If the developer has implemented the Steam Input API, they will need to create a Default/Recommended configuration.
  * Not only does this make the game much more playable with controllers given the developers have actually taken the time to make controls that should be better than a simple Template, this provides a much better starting point for your configuration than basic Templates.
* If the Developer has not put forth the effort to create a customized configuration for their game, Valve still urges them to at least select one of the Templates. If a developer goes that route, that Template will be applied by default and be listed in the Recommended category as well as the Template category. This is obviously no different than just using Templates, so is not very ideal.

If the Developer has done neither of the above, then one of two things will happen:

* The Gamepad Template will be defaulted to.
* If there are Community configs for the game, the configuration will default to the highest rated Community Configuration. Community Configurations will be explored in the next subsection.
