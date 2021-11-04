# 02b06: Joystick Move

Recommended Watching: (find videos soon)

This Input Style is used when Joystick input is desired. It takes directional input and sends the game virtual Joystick input.

This Input Style can be applied to:

* Joysticks
* Touchpads
* Gyroscopes
* Face Button Sets
* Directional Pads

This Input Style can be considered the “native” Style for Joysticks.

When applied to Touchpads, this Style uses the position of the user's thumb as the Joystick tilt and direction.

When applied to Gyroscopes, this Style makes the entire controller act like a giant Joystick.

When applied to Face Button Sets and Directional Pads, this Style uses the directional button presses as “full Joystick tilt”, meaning those Devices are locked to one speed and eight directions.

## Settings

Other than Gyroscope specific settings, all Input Devices share their settings in this Input Style.

### Output

This setting has 3 options:

* Left Joystick - xinput left Joystick is sent to the game.
* Right Joystick - xinput right Joystick is sent to the game.
* Relative Mouse - the Input Device pushes the Mouse cursor around like a Joystick would.

### Click Action

This setting is not available to Gyroscopes.

This Binding uses the Joystick Click, Touchpad Click, or clicking any of the Face Buttons or Directions on the Directional Pad to activate a binding. A typical use for this Binding is the traditional Joystick Clicks; assigning right stick click to the Right Joystick and left to the left.

!! CAUTION !! As just mentioned, when this Style is being applied to a Face Button Set or D-Pad, any input will activate this Binding as all inputs with those Devices are clicks.

### Mode Shifting

This allows you to set a button to Mode Shift the input device into an entirely different Input Style. Mode Shifting is covered in more detail in chapter 4.

### Haptics Intensity

Haptics in this Style pulse with varying strength depending on how far the virtual Joystick is tilted. So for example with the virtual Joystick barely tilted it provides a very weak “tick” and when the virtual Joystick is fully tilted it provides a very strong “thunk”.

This setting has 4 options that determine how strong that tick/thunk is:

* Off
* Low
* Medium
* High

[Mennenth’s Notes: Haptics might not be needed for any physical input, but when using the Steam Controllers Touchpad (or any controllers Gyroscope) as a Joystick then the Haptics can help you better understand how far your thumb is from the center of the Touchpad. I prefer medium haptics here.]

### Output Axis

This drop down allows you to select which Joystick axis, x and y, cause mouse movement.

It has 3 options:

* Both Horizontal and Vertical - works as normal
* Horizontal Only - only outputs on the x axis
* Vertical Only - only outputs on the y axis

### Outer Ring Binding

This Binding Activates whenever the user has tilted the virtual Joystick past a defined threshold.

!! CAUTION !! When this Style is being applied to a Face Button Set or D-Pad, any input will activate this Binding as all inputs with those Devices will be considered at the maximum value which will always be beyond the defined threshold.

### Stick Response Curve

This setting changes the Response Curve of the Joystick. More relaxed curves allow for more precision with small movements, while more aggressive curves result in reaching the maximum output faster when speed is preferred over precision.

It has 6 options:

* Linear
* Aggressive
* Relaxed
* Wide
* Extra Wide
* Custom

!! CAUTION !! Custom then gives you a slider, details below, but that pushes all the options further down in the UI which can make them hard to see or interact with.

### Custom Response Curve

Only visible if “Custom” is selected in the Stick Response Curve setting.

This slider gives you finer control over the Response Curve.

### Dead Zone Shape

This setting allows you to customize the Dead Zone of your Joystick, specifically the shape.

It has 3 options:

* Circle
* Cross
* Square

A Circle Dead Zone results in an even response across the entire throw range of the virtual Joystick.

A Cross Dead Zone emphasizes the cardinal directions more.

A Square Dead Zone emphasizes the diagonals a bit more.

### Enable Deadzone

This setting is a relatively new addition to Steam Input… and seems to be bugged as the name and description are whack.

In the face of the ever growing “stick drift” issue, Valve has included a way to calibrate the dead zones on your controllers sticks. Details on the Calibration feature can be found in chapter 0e.

The Enable Deadzone setting has 3 functions based on its options.

* None: This mode turns off any form of Deadzones within the Configurator.
* Calibration: the Inner Deadzone will be based on your Controller's Calibrated Settings.
* Configuration: You can fully customize the Inner and Outer Deadzones within the Configurator.

If you are using a joystick and have not run the calibration, it is highly recommended you do so. Once you have, it is highly recommended to set this option to “Calibration” if it is not already on that option.

### Dead Zone Inner

This slider determines how big the Dead Zone in the center of the Input Device is. All the way to the left is no Dead Zone, all the way to the right and the Input Device is basically disabled.

### Dead Zone Outer

Despite its name, this slider does not create a Dead Zone around the edge of the Input Device but rather defines how far away from the center of the Input Device is considered to be the maximum output.

!! NOTE !!

The effective “throw range” or “analog values” get stretched or compressed to be in between the Inner and Outer Dead Zones. To gain the most precision possible, minimize the Inner while maximizing the Outer. To gain the fastest possible “0-100”, have the Outer be basically on top of or lower than the Inner. Steam Input is smart enough to not break when the Outer is less than the Inner.

### Invert Horizontal Axis

This setting has 2 options:

* Off
* On

When on, the horizontal - or x - axis gets reversed; right becomes left, and left becomes right.

### Invert Vertical Axis

This setting has 2 options:

* Off
* On

When on, the vertical - or y - axis gets reversed; up becomes down, and down becomes up.

!! CAUTION !! Be mindful of any in-game settings that also invert the y axis, as they can cancel each other out.

### Mouse Sensitivity

This slider is only visible when “Relative Mouse” has been selected for the output.

This slider sets the maximum sensitivity of the relative Mouse movement. Think of it as a dpi setting for a desktop mouse, only as a slider instead of set values

### Sensitivity Horizontal Scale

This slider determines how sensitive the horizontal - or x axis - is relative to the Mouse Sensitivity slider. All the way to the right, the horizontal axis can reach the maximum sensitivity as set by the Mouse Sensitivity slider. As the slider moves to the left, the horizontal axis’ maximum sensitivity will be decreased until all the way left where it becomes disabled.

### Sensitivity Vertical Scale

This slider determines how sensitive the vertical - or y axis - is relative to the Mouse Sensitivity slider. All the way to the right, the vertical axis can reach the maximum sensitivity as set by the Mouse Sensitivity slider. As the slider moves to the left, the vertical axis’ maximum sensitivity will be decreased until all the way left where it becomes disabled.

### Gyro Lock at Edges

Despite having Gyro in its name, this setting is available to all Input Devices.

It has two options:

* Off
* On

The goal of this setting is to prevent the Gyroscopes output from “flipping” if the controller is rotated far enough. Turn it on if you experience any flipping of the output when rotating the controller too far, or off if you experience issues with the controller locking up over time.

[Mennenth’s Notes: I’m really not sure why this is visible to other Input Devices. Maybe in some cases a physical Joystick may have degraded enough that this could become an issue? I don’t know… I also do not use the Gyroscope as a Joystick, so have never even really experimented with this setting.]

### Outer Ring Binding Radius

This slider sets where the threshold is along the output value. To the right it is nearer to the edge of the Input Device, and to the left it is nearer to the center.

### Outer Ring Binding Invert

This setting has two options:

* Off
* On

When on, the Outer Ring gets inverted and becomes a sort of “center binding”, where the binding is activated whenever the Input Device’s output is on the center side of the radius instead of the edge side.

!! NOTE !!

When this Style is used on a Face Button Set or Directional Pad, the Outer Ring Binding seemingly becomes disabled.

### Output Anti-Deadzone

Sometimes, a game will apply a Dead Zone to camera movement. This slider effectively adds extra movement to your Input in order to counter that Dead Zone. Think of it like a “minimum output value”. You should consider raising this slider if the input feels “mushy” when trying to make small precise movements.

### Output Anti-Deadzone Buffer

If you have applied Anti-Deadzone, you can use the Buffer to re-establish a Dead Zone. To mis-quote Adam Savage of Mythbusters fame “I reject your deadzone and substitute my own!”

[Mennenth’s Notes: Before messing with the Dead Zone Inner slider, double check to see if the game is applying its own Dead Zone. If it is, then the Anti-Deadzone settings should be preferred while Dead Zone Inner should probably be left alone.]

## Gyroscope Specific Settings

### Gyro Enable Button

This setting has too many options to list. In effect, you can select which button on your controller enables the Gyro OR you can have the Gyro be Always On.

### Gyro Button Behavior - Turns Gyro

This setting has 3 options:

* On
* Off
* Toggle

When set to On, pressing the Gyro Enable Button turns the Gyro On for as long as the button is held.

When set to Off, the Gyro is on UNTIL the Enable Button is pressed in which case the Gyro is off until the button is released.

When set to Toggle, the Enable Button toggles the Gyro between On and Off with each press.

### Gyro Pitch Neutral Angle

This slider allows you to set the Pitch angle that is considered within the Dead Zone.

To better help visualize, Pitch refers to the “up and down” orientation of the controller. It is the difference between holding the controller flat in your lap, or up like a steering wheel.

Adjust this slider to fit your play style.

## Overall Mennenth’s Notes

Joystick Move is another “cornerstone” Input Style.

It will be used very frequently especially with traditional dual stick controllers.

For traditional dual stick controllers, it will usually be best to set both Joysticks to Joystick Move, with the left one outputting xinput left joystick and the right one outputting xinput right joystick, and of course their click actions set to the respective joystick clicks. This will be about as “pick up and play” as possible for those controllers, as it's basically the “native” Input Style for Joysticks. As such, these are actually the default settings for dual stick controllers.

Where this Style gets interesting is when considering Touchpads, specifically the Steam Controllers dual primary Touchpads.

Even to this day, 6 years after the Steam Controller launched, there are constant debates over the efficacy of using the Touchpads as Joysticks.

The arguments against using the Touchpads in this way can be distilled into a single point: Touchpads are not Joysticks. To expand on that, Haptics are not a replacement for the physical feedback of the Joystick pushing back against your thumb, and when the user relaxes their thumb there is no physical return to center.

I understand those complaints, though personally I view them as falling under the “feels” category. The “feels” category says nothing about actual performance, and having used at least the Left Touchpad as a Joystick for character movement for 3+ years I have found the Touchpads have some potential performance advantages over Joysticks.

* Precision. You know how people will use stick extenders to gain throw range on their sticks, and extra throw range allows them to be more precise? Having a large surface area is like having a stick extender built in. Push the Dead Zone Outer to near max and enjoy increased precision control over the output! This is important especially when considering the next point.
* The Outer Ring Binding. Increased precision may not matter so much for character movement, but by having that extra precision the Touchpad can sacrifice some of it to the Outer Ring Binding without negatively impacting precision. This enables Touchpads to have increased control over the Outer Ring Binding. A physical Joystick actually has disadvantages here, as the limited throw range means it doesn’t have as much precision it can sacrifice for the Outer Ring, and the whole ordeal of pushing back against your thumb becomes troublesome if you want to have good control over the Outer Ring as holding a “non zero, non max” value on a stick is not as simple as on a Touchpad.
  * What is the Outer Ring Binding even used for? Why does this matter? A very common configuration trick people use is to put the Sprint binding into the Outer Ring. This makes Sprint a natural extension of analog movement. Usually, clicking the Joystick is what causes the character to Sprint. Well, with Sprint in the Outer Ring this frees up the click to be used for something else. Crouch? Jump? Does not really matter, what matters is by then shifting that action to the click, that frees up another button to be used for something else. It becomes a domino-like effect where several small changes in the configuration happen which ultimately lead to a configuration that is more efficient with its inputs, leading to a higher ceiling of game play possible.
  * I would like to reiterate that this is still possible on physical Joysticks, however it works a LOT better on a Touchpad.
* Speed. The Touchpads actually have TWO Dead Zones. The one in the center, and… going into the 3rd dimension and NOT touching the Touchpad by lifting your thumb off of it. This enables you to go from no output to max output in the space of a single frame, without having to go through the entire range first. Among other things.
The more I’ve adapted to how the Touchpad “lacks physical feedback”, the more I’ve come to realize that said physical feedback is actually just a limiter on what I’m capable of. Trying to go back to using a physical Joystick for movement feels restrictive to me at this point. A Joystick forces my thumb to make specific movements, but a Touchpad enables me to be as fast and as precise with my thumb as I can be by letting me do whatever.
* Clicking when off center. To me, clicking Joysticks in when they are tilted/off center has always felt a little weird as the click responds… “differently” I suppose… depending on how much the stick has been tilted. However, that problem does not exist - at least not to the same amount - with Touchpads. Insofar as the problem does exist, it could be solved by replacing the physical click with Force Sensors like Valve is doing with the Deck’s Touchpads.
* Stick Drift. Or rather, lack thereof. Touchpads are quite literally immune to Stick Drift. Even if all those other advantages were removed and even if in terms of performance we just accepted that Touchpads and Joysticks were on par with each other, being immune to Stick Drift makes Touchpads superior on its own merits… at least in my opinion.

At the end of the day, we are talking about character movement so any advantage is ultimately not that impactful. For the most part, preference will likely be valued more than the advantages I have laid out. And this is fine! The reason why so many settings and options exist is precisely to cater to a variety of preferences.

However, all of those advantages no matter how tiny add up and serve to push the Steam Controller “over”, at least in this nerd's opinion.
