# 05a01: Templates

Templates are generic configurations that can be applied at any time. 

They are useful for getting a game baseline playable with a controller, but as they are geared more towards being based on genres instead of specific games they may lack things for your specific game. As such, they provide a good starting point towards developing a configuration.

You can access Templates on the Configuration Overview page. At the bottom you will see “Browse Configurations”. Clicking that takes you to the “Controller Configurations - Import” page. You will find Templates as a category in the list on the left hand side of that page.

## Default Templates

While there are some shared Templates, some are also based on which controller you are using.

### Shared between All:

* Gamepad - a “no frills” configuration that sets your controller up like a XBox controller, the most commonly supported controller for games that support controllers, with purely gamepad inputs.
  * For Sony controllers, the Touchpad is in split mode and duplicating start/select
* Keyboard (WASD) and mouse - a “no frills” configuration that sets the controller up with purely keyboard and mouse inputs for games that don’t support controllers. The Template is based on commonly used keybinds in first person shooters, and bound to locations on the controller with respect to their gamepad counterparts ie; Space, often used as Jump, is bound to the A button.
  * The Left Stick on controllers are using the Directional Pad Input Style with WASD bindings instead of dpad bindings.
  * The Right Stick on controllers that have them are using the Joystick Move Input Style, with their outputs set to “Relative Mouse”.
  * For Sony Controllers, the Touchpad is in unified mode with the Mouse Input style.

### Shared between DualShock 4/ Dualsense and Switch Pro:

* Gamepad with Flick Stick - this configuration mostly follows the Gamepad Template, with two exceptions:
  * Right Stick has been set to the Flick Stick Input Style instead of Joystick Move (Right Stick).
  * Gyro has been set to the Mouse Input Style instead of being unbound.
  * This is for games where aiming is critical and “mixed input” is supported.

### Shared between DualShock 4/ Dualsense and Steam Controller:

* Gamepad with high precision camera/aim
  * While available to Sony Controllers, it does not seem to differ from the Gamepad Template. Perhaps being available is an oversight. Recommend using the Gamepad Template to avoid confusion.
  * For Steam Controllers, this Template follows the Gamepad Template with one exception: the Right Touch Pad has been set to the Mouse Input Style instead of the Joystick Move (Right Stick) Input Style. This is for games where aiming is critical and “mixed input” is supported.
* Gamepad with mouse and gyro
  * For Sony Controllers, this Template follows the Gamepad Template with one addition: Gyro has been set to the Mouse Input Style instead of being unbound. This is for games where aiming is critical and “mixed input” is supported.
  * For the Steam Controller, this Template is the same as “Gamepad with High Precision Camera/Aim”, with one addition: Gyro has been set to the Mouse Input Style instead of being unbound. This is for games where aiming is critical and “mixed input” is supported.

### Steam Controller Exclusive:

* Gamepad with Camera Controls - This Template follows the Gamepad Template, with one exception:
  * The Right Touch Pad has been assigned the Mouse-Joystick Input Style instead of the Joystick Move (Right Stick) Input Style. This is for games that do not support mixed input and gamepad inputs are preferred while still desiring mouse-like control over the camera. 

## Personal Templates

It is also possible to create your own Templates if none of these work for you.

For instance, the Keyboard and Mouse Template is pretty first person shooter centric. But there are other genres of games that want Keyboard and Mouse, such as RTS games.

If you make a configuration for such a game and would like to quickly apply it to other games of that genre as a starting point, you can export the configuration to the Templates category.

To do so, start on the Configuration Overview page and click on “Export Config” at the bottom of the screen. This takes you to the “Controller Configurations - Export” page.

From there, navigate to the Templates category on the left side of the page, and select “Save new Template binding”. You will be able to name it and give a quick description of it.

Templates that you have exported now show up in the Templates category when importing a configuration, so you can quickly apply that personalized Template to other games of the same genre (this is how I manage to spend sometimes less than a minute in the configurator).
