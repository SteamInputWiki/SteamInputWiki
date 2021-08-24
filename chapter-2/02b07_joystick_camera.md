# 02b07: Joystick Camera

Recommended Watching: (find videos later)

This Input Style is used when Joystick input is desired, however unlike Joystick Move (02b06) this Style has a different set of options as well as one stand out feature that will be discussed shortly.

This Input Style, despite being a Joystick Style, can only be applied to:

* Touchpads
* Gyroscopes

The reason why this Joystick Style can only be applied to the above is because of its built-in feature called “Adaptive Centering”.

#### What is Adaptive Centering?

Adaptive Centering dynamically changes the location of the Dead Zone based on where input is first registered.

For Touchpads, this means when your thumb makes contact with the Touchpad the Dead Zone is relocated to be underneath your thumb. When you lift your thumb off the Touchpad and place it back down again, the Dead Zone once more relocates to be underneath your thumb. This is how software Joysticks in mobile games when using a cell phone's touch screen typically work.

For Gyroscopes, this means when the Gyro gets activated its current rotation is considered to be the Dead Zone, and that changes every time the Gyro gets disabled and re-enabled.

Adaptive Centering, in theory, basically makes it impossible to make unintended inputs with the Touchpads and Gyro. 

“Finding the center” is a common complaint when it comes to using the Touchpads as Joysticks, due to how the Touchpads lack a physical return to center and in general do not have strong surface geometry to help you find the center. If you want to put your thumb on the Touchpad but do not want to send input, if you have trouble finding the center then Adaptive Centering could theoretically help.

## Shared Settings

### Output

This setting has 3 options:

* Left Joystick - xinput left Joystick is sent to the game.
* Right Joystick - xinput right Joystick is sent to the game.
* Relative Mouse - the Input Device pushes the Mouse cursor around like a Joystick would.

!! ISSUE !! It seems that as of 24 August 2021, Joystick Camera is not outputting Relative Mouse as it should.

### Stick Response Curve

This setting changes the Response Curve of the Joystick. More relaxed curves allow for more precision with small movements, while more aggressive curves result in reaching the maximum output faster when speed is preferred over precision.

It has 5 options:

* Linear
* Aggressive
* Relaxed
* Wide
* Extra Wide

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

### Smooth Joystick

This setting has 2 options:

* Off
* On

When On, this setting causes the virtual Joystick to have a simulated “return to the center” - much like how a physical Joystick takes a small amount of time to do so - when you lift your thumb off the Touchpad or disable the Gyro.

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

### Sensitivity Vertical Scale

This slider determines how sensitive the y axis is compared to the x axis. Further to left emphasizes horizontal sensitivity while further to the right emphasizes vertical sensitivity.

[Mennenth’s Notes: I have not fully tested how this slider works in this Style. Because this Style outputs Joystick or relative_mouse, I’m not sure how to test to find which values result in what outcome, like with styles that use absolute_mouse instead (Mouse).]

### Output Anti-Deadzone

Sometimes, a game will apply a Dead Zone to camera movement. This slider effectively adds extra movement to your Input in order to counter that Dead Zone. Think of it like a “minimum output value”. You should consider raising this slider if the input feels “mushy” when trying to make small precise movements.

### Output Anti-Deadzone Buffer

If you have applied Anti-Deadzone, you can use the Buffer to re-establish a Dead Zone. To mis-quote Adam Savage of Mythbusters fame “I reject your deadzone and substitute my own!”

### Mouse Sensitivity

This slider sets the maximum sensitivity of the relative Mouse movement. Think of it as a dpi setting for a desktop mouse, only as a slider instead of set values

## Touchpad Specific Settings

### Click Action

This Binding uses the Touchpad Click. A common use would be to assign the Joystick Click (either Left or Right Joystick, depending on the Output) to the Click Action - or the equivalent for keyboard and mouse only games.

### Swipe Duration

If you swipe or “flick” the Touchpad, Joystick Camera can simulate the virtual Joystick being pegged at its maximum output for a duration of time before beginning to virtually recenter (at which point “Smooth Joystick” takes over)

It has 4 options:

* Off - does not stay pegged
* Low - stays pegged for a short duration
* Medium - stays pegged for a medium duration
* High - stays pegged for a long duration

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

### Gyro Steering Axis

This setting is only available to Gyro.

This setting has 2 options:

* Yaw
* Roll

This sets which type of Gyro rotation controls the horizontal movement of the Mouse.

To better visualize, stick your hand out with your index finger pointing forward and your thumb pointing up. This represents the controller laying flat. Yaw would be sweeping your index finger left and right while your thumb remains pointing up. Roll would be tilting your thumb left and right while your index finger remains pointing forward.

### Gyro Pitch Neutral Angle

This slider allows you to set the Pitch angle that is considered within the Dead Zone.

To better help visualize, Pitch refers to the “up and down” orientation of the controller. It is the difference between holding the controller flat in your lap, or up like a steering wheel.

Adjust this slider to fit your play style.

## Overall Mennenth’s Notes

In my opinion, there is an issue with Adaptive Centering that makes it more of a “newb trap”. 

The problem is that unlike the software joysticks in mobile games that dynamically move the Dead Zone, Steam's implementation of Adaptive Centering does not move the entire virtual Joystick preserving the range. 

Steam’s Adaptive Centering relocates the Dead Zone, but then also scales the response range of the virtual Joystick across the entirety of the pad. This shrinks the range in the direction of the closer edge while expanding the range towards the furthest edge. The maximum output of the virtual Joystick is therefore always on the edge of the Touchpad (or extreme rotation values with the Gyro, more on that in a minute). 

The allure of Adaptive Centering is that it should help newcomers get used to the Touchpads, but I really doubt having an inconsistent response range is helpful in that situation*.

Gyro just straight up feels bad here. Joystick Move could maybe work, but due to the Dead Zone constantly shifting and how the output range also gets dynamically scaled, Joystick Camera winds up not really working well on the Gyro because it has to be rotated excessively far to get a response.

That said, there is a use for Joystick Camera. If you know what you are doing, you can take advantage of the Adaptive Centering feature to really load the Touchpad click down with virtual buttons thanks to Mode Shifting, and not have to worry about accidental inputs when clicking. The Dead Zone works better than Minimum Movement Threshold for this purpose.

I’m also wondering if I should experiment more with Joystick Camera as a “fast turn” input with the Touchpad. I don’t really like the Trackball mode of the Mouse Style, but in writing this chapter and thinking about the settings of Joystick Camera… part of me wonders if Joystick Camera set to output relative mouse with the Swipe Duration turned up and Smooth Joystick turned on isn’t perhaps the “real trackball mode”...

*If you are a newcomer to the Touchpads and are wanting some assistance in learning where the center is while reducing the amount of unintended inputs, then I would recommend using Joystick Move. It allows you to create a Dead Zone in the center of the Touchpad. You can start with it being quite large and forgiving, and slowly decrease it over time as you get more comfortable using the Touchpad.
