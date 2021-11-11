# 02b14: Directional Swipe

This Input Style allows you to assign 4 directional bindings much like Directional Pad, but as a more of a gestural based input. These inputs are “one shot”, i.e. they fire once per swipe and are not held.

The most common use case for this Input Style would be to mimic how some Playstation games use the Touchpad on Sony controllers as a swipe pad for inputs.

This Input Style can be applied to:

* Touchpads
* Gyroscopes
* Joysticks
* Directional Pads
* Face Button Clusters

When assigned to Touchpads, swiping in a direction activates that directions binding.

When assigned to Gyroscopes, rotating the controller in a direction activates that directions binding (with respect to the gyro steering axis).

When assigned to Joysticks, Directional Pads, and Face Button Clusters, it acts weirdly. It seems you have to make the input active first (either by partially tilting the Stick or pressing one of the buttons/directions), and then depending on what input you make next kind of determines which binding actually gets activated. However in testing I found the behaviour to be somewhat erratic. I would highly recommend using the Directional Pad Input Style if you desire to have 4 directional bindings on these Input Devices.

## Shared Settings

### Sensitivity

This slider determines how far the input must travel before activating the Swipe. You can think of this kind of like a deadzone for movement. The lower the value, the less movement is needed to activate the Swipe.

### Rotation

This slider allows you to rotate the software grid of the virtual Swipe input to better line up with your individual movements. You want to adjust this slider so a movement you think should be perfectly horizontal is horizontal only. May or may not affect Gyro performance.

### Mode Shifting

This allows you to set a button to Mode Shift the input device into an entirely different Input Style. Mode Shifting is covered in more detail in chapter 4.

### Click Action

While shared between all other Input Devices, this Binding is not available to Gyroscopes.

This is a binding that is activated whenever the Input Devices Click is pressed.

For Joysticks and Touchpads, this means clicking them activates this binding.

For Directional Pads and Face Button Clusters, pressing any of the buttons will activate this Binding.

### Scroll Wheel Mode

When turned on, this gives the swipe a “momentum” much like that of a scroll wheel; the binding will continue to fire multiple times for a short duration after activating.

## Gyro Specific Settings

### Gyro Button Behavior - Turns Gyro

This setting has 3 options:

* On
* Off
* Toggle

When set to On, pressing the Gyro Enable Button turns the Gyro On for as long as the button is held.

When set to Off, the Gyro is on UNTIL the Enable Button is pressed in which case the Gyro is off until the button is released.

When set to Toggle, the Enable Button toggles the Gyro between On and Off with each press.

### Gyro Enable Button

This setting has too many options to list. In effect, you can select which button on your controller enables the Gyro OR you can have the Gyro be Always On.

### Gyro Steering Axis

This setting has 2 options:

* Yaw
* Roll

This sets which type of Gyro rotation controls the horizontal movement of the Mouse.

To better visualize, stick your hand out with your index finger pointing forward and your thumb pointing up. This represents the controller laying flat. Yaw would be sweeping your index finger left and right while your thumb remains pointing up. Roll would be tilting your thumb left and right while your index finger remains pointing forward.

## Notes

### Here is what happens if you try to change Activator settings for the Bindings in this Input Style

* Double Press Activators are exceeding difficult to trigger in this mode, and you may wind up activating other Swipe Directions in the process
* Long Press Activators appear to not work at all.
* Start Press Activators are redundant; this Input Style already fires the Binding a single time upon activating and does not hold it.
* Release Press Activators seem like they might make a change, however if they do it is negligible and redundant for similar reasons to Start Press.
* Chorded Press Activators work like you would expect; the Swipe only activates the Binding if the Chorded Button is held.
* Turbo Mode seems to break the Swipe Direction Binding entirely; if you need the Swipe Binding to have momentum, enable the Scroll Wheel Mode setting discussed earlier.
