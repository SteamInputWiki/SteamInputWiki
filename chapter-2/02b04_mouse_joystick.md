# 02b04: Mouse Joystick (Mouse-Like Joystick)

Recommended Watching: (find some videos later I suppose)

This Input Style allows you to interact with the Input Device as if it were using the Mouse Input Style, but runs some calculations to transform that Mouse movement into its equivalent Joystick angle and deflection. The goal is that the player makes Mouse-like Inputs, but the game sees a Joystick - specifically a Right Joystick - and responds accordingly. It is intended to be used as a compatibility option for games that do not allow Mixed Input (see chapter 02c) and having gamepad inputs is desirable.

NOTE: Because the game sees a Joystick, sensitivity in this mode is controlled in game ONLY.

This Input Style can be applied to:

* Touchpads
* Gyroscopes (referred from here on as “gyro”)

When applied to Touchpads, you interact with it similarly to if the Touchpad was using the Mouse Input Style (see chapter 02b03).

When applied to Gyro’s, you interact with it similarly to if the Gyro was using the Mouse Input Style (see chapter 02b03).

## Settings

### Click Action

This Binding is only available for touchpads.

It allows you to bind an action to clicking the touchpads button. If playing a game that would traditionally have a right stick for aiming but you are using a touchpad as a mouse for aiming, you could for example assign the right stick click to the touchpad click to retain that functionality.

### Gyro Enable Button

This setting is only available to Gyro.

This setting has too many options to list. In effect, you can select which button on your controller enables the Gyro OR you can have the Gyro be Always On.

### Gyro Button Behavior - Turns Gyro

This setting is only available to Gyro.

This setting has 3 options:

* On
* Off
* Toggle

When set to On, pressing the Gyro Enable Button turns the Gyro On for as long as the button is held.

When set to Off, the Gyro is on UNTIL the Enable Button is pressed in which case the Gyro is off until the button is released.

When set to Toggle, the Enable Button toggles the Gyro between On and Off with each press.

### Sensitivity

This setting is “available” to Touchpads and Gyro.

This setting is greyed out with the following tooltip from Valve:

“Adjust sensitivity in-game.”

[Mennenth’s Notes: As per Valves tip from their main description of this Input Style, you will get the best results by maximizing in-game joystick sensitivity.]

### Rotation

This setting is available to both Touchpads and Gyro… however it does not appear to affect the Gyro at all while it does affect the Touchpad. Perhaps being available to the Gyro is a bug?

This setting takes some set up to explain properly.

A Touchpad is basically a xy/2-axis grid of a whole bunch of tiny sensors. It will have a physical x axis, as well as a physical y axis.

However, due to how you may hold the controller, the size of your hands, the length of your thumbs, and a bunch of other factors, when you swipe your thumb horizontally along the Touchpad your thumb may not be perfectly aligned with the physical x axis of the Touchpad.

With the Steam Controller, Valve designed the ergonomics to account for this to some extent by slightly rotating the Touchpads Y axis towards the centerline of the controller as well as “canting” the Touchpads up at a slight angle towards the users thumbs. However, all those ergonomics decisions can only go so far as everyone’s thumbs will be different and therefore everyone’s “horizontal swipe” will be different.

The Rotation setting further helps solve the issue, by rotating the xy grid in software.

This enables the user to line up the Touchpads x axis with what their thumbs' natural horizontal swipe across the Touchpad is.

Valve did include a visual aid when adjusting this slider. Look at how your thumb moves across the pad, and adjust this setting so the white line is slanted the same. Get in game and test, and make further adjustments if needed. You want what is a natural horizontal swipe for you to be an actual horizontal swipe in game. Do note that there may still be some up and down movement as your thumb moves in arcs and not straight lines. However, as long as the start point and end point of the swipe are on the same horizontal level then you can consider this setting dialed in.

[Mennenth’s Notes: Just like with the Mouse Input Style, Rotation is pretty mandatory for getting a good response out of the Touchpad while using the Mouse-Like Joystick style. See the Mouse Input Style (chapter 02b03) for more details.]

### Sensitivity Vertical Scale

This setting is available to both Touchpad and Gyro.

This slider determines how sensitive the y axis is compared to the x axis. Further to left emphasizes horizontal sensitivity while further to the right emphasizes vertical sensitivity. It is possible to completely remove the y axis by moving the slider all the way to the left, but it is inconsistently not possible to remove the x axis by moving the slider all the way to the right. All the way to the right will result in a still usable x axis but an extremely emphasized y axis.

[Mennenth’s Notes: Unlike with the Mouse Input Style, due to converting the output to a Joystick it is much harder to know the exact ratios for either Touchpad or Gyro. I am not sure if it is safe to assume similar values or not. I will still recommend squashing the vertical at least a little bit on the Touchpad though, but beyond that more experimentation is needed here.]

### Trackball Mode

This setting is only available to the Touchpad.

Trackball Mode gives the Mouse part of Mouse-Joystick virtual “momentum” when you swipe and lift your finger - “flicking” the pad -, causing it to act like a Trackball; it will “spin”, and therefore continue to keep the virtual Joystick deflected for a short duration of time causing camera movement, slowly returning it to center over time (as the virtual ball also slows down in its spin). The user can also preemptively return to center by setting their thumb back down on the Touchpad.

It has two options:

* On
* Off

### Trackball Friction

This setting is only available to the Touchpad.

This setting determines how quickly the virtual trackball portion of Mouse-Joystick will come to a stop, by adding simulated friction to the virtual trackball.

This setting determines how quickly the virtual Joystick will return to center. Or more accurately how much friction is supplied to our emulated Trackball. 

It has 5 options:

* Off - stops immediately
* Low - takes a long time to stop
* Medium - takes some time to stop
* High - takes a short time to stop
* None - will go on forever until the user places their thumb back on the Touchpad

### Friction Vertical Scale

This setting is only available to the Touchpad.

This slider determines how quickly the virtual ball's y axis comes to a stop relative to its x axis..

As Valve mentions in the description, having a higher vertical friction can be beneficial for games where the Joystick controls the camera, so horizontal flicks can rotate mainly the x axis without impacting the y axis very much if at all.

[Mennenth’s Notes: I have come to actively dislike Trackball emulation when using the Mouse-Like Joystick Input Style. There just is not enough control over how it behaves to get consistently good responses across a multitude of games. More on that later, but specific to Trackball emulation games will sometimes have really weird joystick acceleration curves that make Trackball emulation feel incredibly wonky with Mouse-Joystick.]

### Gyro Camera Scale

This setting is only available to Gyro’s.

If you are using Mouse Joystick for both Touchpad and Gyro, this slider determines how important the Gyros input is compared to the Touchpads input when it comes to converting the input to the virtual Joystick.

### Gyro Lean Left/Right Bindings

These Bindings are only available to the Gyro.

These bindings basically treat the Gyro as a giant rocker, with a button activating when you tilt the controller to either side by a certain amount.

### Mode Shifting

This is available to both Touchpad and Gyro.

This allows you to set a button to Mode Shift the input device into an entirely different Input Style. Mode Shifting is covered in more detail in chapter 4.

### Haptics Intensity

This setting is available to both Touchpad and Gyro.

When the haptics are active for Mouse mode, they give slight feedback reminiscent of rumbling whenever the inputs detect movement.

This setting has 4 options that determine how strong that rumbling is:

* Off
* Low
* Medium
* High

[Mennenth’s Notes: Other than with Trackball enabled, I don’t really care for haptics while using the Mouse-Joystick Style.]

### Invert Vertical Axis

This setting is available to both Touchpad and Gyro.

This setting has two options:

* Off
* On

When turned on, this flips any y axis movement; down becomes up, and up becomes down.

!! CAUTION !! As per Valve’s description, be mindful of any in-game settings that also invert the y axis, as they could cancel each other out.

### Minimum Joystick X/Y Output Value (sliders)

These sliders are available to both Touchpads and Gyros.

These sliders determine the smallest amount of virtual Joystick deflection to output to the game possible, on a per axis basis. More to the right makes the smallest possible output larger, more to the left makes it smaller.

!! IMPORTANT !! As Valve's tooltip mentions; adjust the value upward until slow movements are smooth, and down if small movements are too big.

### Enhance Small Movement Precision

This slider is available to both Touchpads and Gyros.

It may be the case that even once the Minimum XY Output Values are dialed in correctly, small movements are still not precise enough. This slider helps fine tune for small movement precision.

[Mennenth’s Notes: The above 3 sliders are absolutely CRUCIAL to getting Mouse-Joystick feeling as good as it can… in games where Mouse-Joystick can work well (more on that last part later). In effect, the Minimum Output Values compensate for any deadzone the game has applied to the Right Joystick so movement can be immediate, and Enhance Small Movement Precision ensures a good response with tiny movements.]

### Invert Horizontal Axis

This setting is available to both Touchpad and Gyro.

This setting has 2 options:

* Off
* On

If set to On, the x axis becomes flipped; left becomes right, right becomes left.

### Custom Response Curve

This slider is available to both Touchpads and Gyros.

This slider allows you to adjust how quickly or slowly Mouse-Joystick ramps up to its maximum output value.

More to the right is a more aggressive response, while more to the left is more relaxed.

### Double Tap Binding

This Binding is only available to Touchpads.

This Binding behaves similarly to the Touch Binding, however you must Double Tap the Touchpad to activate it (similar to the Double Press Activator. More on Activators in Chapter 4).

### Double Tap Duration

This setting is only available to Touchpads.

This slider determines how quickly you must Double Tap the Touchpad to activate the Double Tap Binding. More to the left will require quicker double taps, while more to the right gives you more time to double tap.

### Double Tap Beep

This setting is only available to Touchpads.

This setting has 2 options:

* Off
* On

If set to On, the haptics will audibly beep whenever the Double Tap is activated.

[Mennenth’s Notes: Because Mouse-Joystick unfortunately lacks the Touch Binding, the Double Tap Binding is incredibly useful. I like using the Double Tap Binding for whatever button the game uses as its “Interact” button.]

### Gyro Steering Axis

This setting is only available to Gyro.

This setting has 2 options:

* Yaw
* Roll

This sets which type of Gyro rotation controls the horizontal movement of the Mouse.

To better visualize, stick your hand out with your index finger pointing forward and your thumb pointing up. This represents the controller laying flat. Yaw would be sweeping your index finger left and right while your thumb remains pointing up. Roll would be tilting your thumb left and right while your index finger remains pointing forward.

Remember the Gyro Lean Bindings from earlier? Leaning uses the axis not being used for Steering.

[Mennenth’s Notes: Despite some rather aggressive arguments that have happened online over this, this setting is mostly preference and NOT one being more intuitive than the other. I personally think that on a controller Yaw makes sense as I view it as a laser pointer coming out of the usb port of the controller and pointing at the screen. However a lot of mobile gamers swear by Roll and I can understand the logic there; the screen is kind of like a camera, and in that situation roll makes a lot of sense. So perhaps the context matters?

Nintendo, specifically Splatoon 2, does things a bit differently by mixing and transitioning between Yaw and Roll dynamically depending on the Pitch angle of the controller. JoyShockMapper also recently updated to include a “PlayerSpace” method of handling the Gyro that works similarly to the Splatoon 2 method. 

To any Valve devs reading this, please add PlayerSpace as an option. Have it disable the Lean Bindings if needed, but it would be really nice to experiment with PlayerSpace on my Steam Controller.]

### Gyro Lean Point

This setting is only available to Gyro.

Remember the Gyro Lean Bindings from earlier?

This slider determines how far you have to lean the controller to activate the Lean Bindings.

### Trigger Press Mouse Dampening (drop down menu)

This setting is available to both Touchpads and Gyro.

If a game does not have any ADS mode or sensitivity slow down/sniper button of its own, or if you would like additional buttons to slow down your sensitivity, you can add it with this setting and determine which button enables the pseudo-ads.

There are 7 options for this setting, which determine what button or combinations of buttons cause the slow down:

* Off
* Right Trigger Soft Pull Dampening
* Left Trigger Soft Pull Dampening
* Both Trigger Soft Pull Dampening
* Right Trigger Soft/Full Pull Dampening
* Left Trigger Soft/Full Pull Dampening
* Both Trigger Soft/Full Pull Dampening

### Trigger Press Mouse Dampening (slider)

This setting is available to both Touchpads and Gyro.

This slider determines how slow the mouse movement should become when the Dampening is activated. Further to the right is slower.

### Edge Spin Radius

This setting is available only to Touchpads.

This slider determines the distance from center, the radius, at which Edge Spin happens.

#### What is Edge Spin?

Think of Edge Spin like a Joystick.

Basically, you get Mouse-Like input in the center of the Touchpad and Joystick-like input at the edge.

### Edge Spin Speed

This setting is available only to Touchpads.

This slider determines how far to tilt the Virtual Joystick when Edge Spin has been engaged. Further to the right is more tilt. At all the way to the left, which is default, Edge Spin is disabled.

### Minimum Movement Threshold

This setting is available to both Touchpad and Gyro.

This setting causes input to initially not be sent but rather built up until a threshold is hit and then sent all at once.

As Valve’s description says, its main use is to counter any aggressive filtering a game might have that results in smaller movements being lost. By building up the movement and sending it all at once, it can overcome that filtering. The more to the right the slider is, the larger the threshold is requiring more movement to be built up before being sent. The default of all the way left has no threshold; any movement is sent at all times.

!! CAUTION !! Too much Minimum Movement Threshold can cause the input to feel like it's snapping to places on a grid instead of moving smoothly as the threshold is constantly being overcome and then fallen behind over and over.

[Mennenth’s Notes: I typically have no MMT on gyro, and possibly only a tiny amount on Touchpad if using Mode Shift Clicks to prevent accidental input while clicking the Touchpad.]

## Overall Mennenth’s Notes

So I lifted and modified the descriptions of a lot of settings from the Mouse Input Style (chapter 02b03), because Mouse-Joystick shares a lot of the same settings. I have not put notes on some of the settings though, as I haven’t fully experimented with all of them… and for good reason.

Mouse Joystick is by far the most fiddly Input Style in Steam Input. It takes the most tweaking and experimenting to get feeling as good as it can… but it is also the most game dependent Input Style provided by Steam Input. Depending on how your game handles Joystick input and if the game allows you to customize that response any, Mouse Joystick will be unplayably bad at worst and even at its best it is not going to be as good as the Mouse Style proper. You just lose… “fidelity” we’ll call it, in the translation from Mouse to Joystick.

This is not to say this Style does not have a use.

I have found the games that play the best with Mouse Joystick are typically 3rd person action games such as Dark Souls or 3rd person platformers such as Spyro The Reignited Trilogy. Basically genres of games that could benefit from being able to whip the camera around, but don’t really need the precision of a Mouse and therefore a smoother experience is desired. 

In these types of games, here is the configuration procedure I typically go through to get it feeling as good as it can.

Start by maxing out the in game sensitivity
Then maximize the Minimum Output Value sliders
That will cause the camera to go wild even you are merely resting your thumb on the Touchpad
Slowly decrease the Minimum Output Values until the camera no longer moves, then increase by a tiny amount.
This basically fully compensates for whatever deadzone the game has applied to the Joystick
Increase Enhance Small Movement Precision until the camera slides a bit when holding your thumb on the Touchpad steady, then decrease until that sliding stops.
Do similar steps for Gyro, preferably with Gyro always on and laying the controller on a flat surface.
That is by no means a silver bullet or other magic that makes Mouse Joystick amazing, but rather simply the best it can be given the situation. Some games simply do not play well with this Input Style, for any number of reasons. Joystick Acceleration in particular can really cause things to go sideways with this Style, and is typically why I really rather dislike Trackball mode in Mouse Joystick; sometimes it can feel like the camera speed spikes up then down and back up rapidly prior to steadily slowing.

I think if more developers put more options into their games to customize how the Joystick works in-game, then Mouse-Joystick would stand a better chance… but at that level of effort I’d almost prefer devs focus on Mixed Input (chapter 02c) so this compatibility Style would not even be needed. Obviously both would be ideal though.

[SoraFirestorm’s Notes: I've tested this on some software that I special purpose wrote to fiddle with mouse vs mouse-joystick. Even under what I'd argue is optimal conditions - where the game doesn't do any post-processing on the joystick and is essentially treated as a delta device instead of a angle-velocity device - mouse-joystick is still noticeably worse (but is at least reasonably passable IMO). Granted, this is without me doing any tuning on the Steam Input side because... I'm basically entirely unfamiliar with how to configure this style. So from that perspective... no, I don't think there's really anything a developer can do.

That said, there is still a case for mouse-joystick which may or may not be niche/relevant depending on your gaming lifestyle: there's only one mouse, which means you need to use Mouse-Joystick in some multiplayer contexts

So, depending on the game, there might still be a point.]

Following on from Sora’s note, Portal 2 is a good example of a situation where local multiplayer can be a thing and both players would want Mouse like controls when using controllers that can use such input (has a touchpad or gyro or both). How do you get multiple good mice in local multiplayer? Providing a good SIAPI implementation that has an “absolute_mouse” Input Style for camera control and can differentiate between player 1, 2, etc. More on implementing SIAPI into your games in chapter 06.

In the meantime, if I am playing a game that does not support Mixed Input then I personally bite the bullet of having in-game prompts not match my controller and opt for going with a full keyboard and mouse configuration as that will give the best performance way more reliably.
