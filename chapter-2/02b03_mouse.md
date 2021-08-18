# 02b03: Mouse

Recommended Watching: (uhhh… find some videos later I suppose, prior to moving to the full wiki?)

This Input Style converts the Input Device into a 1-to-1 Mouse input, more technically called “absolute_mouse” in software. It moves the cursor on screen, the camera in fps’, etc. Think of what your desktop mouse does, and that is precisely what this Input Style does.

This Input Style can be applied to:

Touchpads
Gyroscopes (referred from here on as “gyro”)

When applied to a touchpad, you can think of it like a laptop touchpad.

[Mennenth’s Notes: While this is the most accurate comparison, it carries some unfortunate stigma as laptop touchpads are often not regarded as good gaming input devices for a variety of reasons. However, I would like to challenge you to set aside any preconceptions here. The Steam Controllers touchpads are higher resolution than typical laptop touchpads, include haptics, and most importantly are actually ergonomically set up to be used for gaming where laptop touchpads typically aren’t.]

When applied to a gyro, you can think of the entire controller as being either an air mouse or a laser pointer. Gyro’s use the rotation of the controller to accomplish their task, so in a way you can view a Gyro in Mouse mode as being a Mouse that is controlled through rotating the controller in the air as opposed to translating/moving a mouse across a desk surface

[Mennenth’s Notes: Gyro is a form of motion control. Motion controls are another thing that has a lot of stigma surrounding it due to waggle commands from a bygone era, often leading to people calling motion controls a gimmick. But “waggle commands” and “gyro aimings” only similarity is that they are both forms of motion control; gyro aiming is way better and more intuitive than stick only aiming, as it's basically a mouse. And yes, I did just imply that mice are a form of motion control too. You move the entire device to accomplish the task. Calling “gyro aiming” a gimmick is equivalent to calling “mouse aiming” a gimmick. Check mate.]

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

On
Off
Toggle

When set to On, pressing the Gyro Enable Button turns the Gyro On for as long as the button is held.

When set to Off, the Gyro is on UNTIL the Enable Button is pressed in which case the Gyro is off until the button is released.

When set to Toggle, the Enable Button toggles the Gyro between On and Off with each press.

### Sensitivity

This setting is available to both Touchpad and Gyro.

This determines how sensitive the input is. Think of it as a dpi setting for a desktop mouse, only as a slider instead of set values. As such, Valve recommends lowering in-game sensitivity while increasing this slider to achieve the smoothest result as the game will have more to work with.

[Mennenth’s Notes: I will be covering this much more in depth later, however I would actually advise against maximizing Steam’s sensitivity while minimizing in-game sensitivity. At least when using this Input Style on Gyro. I’ve noticed that Gyro becomes prone to building up errors at extreme sensitivity values, which can negatively impact your aiming performance in game. Valve is totally correct that maximizing sensitivity in Steam while minimizing in-game will result in a smooth experience, but by keeping sensitivity values more reasonable the Gyro feels a lot more “locked in”.]

### Rotation

This setting is available to both Touchpads and Gyro… however it does not appear to affect the Gyro at all while it does affect the Touchpad. Perhaps being available to the Gyro is a bug?

This setting takes some set up to explain properly.

A Touchpad is basically a xy/2-axis grid of a whole bunch of tiny sensors. It will have a physical x axis, as well as a physical y axis.

However, due to how you may hold the controller, the size of your hands, the length of your thumbs, and a bunch of other factors, when you swipe your thumb horizontally along the Touchpad your thumb may not be perfectly aligned with the physical x axis of the Touchpad.

With the Steam Controller, Valve designed the ergonomics to account for this to some extent by slightly rotating the Touchpads Y axis towards the centerline of the controller as well as “canting” the Touchpads up at a slight angle towards the users thumbs. However, all those ergonomics decisions can only go so far as everyone’s thumbs will be different and therefore everyone’s “horizontal swipe” will be different.

The Rotation setting further helps solve the issue, by rotating the xy grid in software.

This enables the user to line up the Touchpads x axis with what their thumbs' natural horizontal swipe across the Touchpad is.

Valve did include a visual aid when adjusting this slider. Look at how your thumb moves across the pad, and adjust this setting so the white line is slanted the same. Get in game and test, and make further adjustments if needed. You want what is a natural horizontal swipe for you to be an actual horizontal swipe in game. Do note that there may still be some up and down movement as your thumb moves in arcs and not straight lines. However, as long as the start point and end point of the swipe are on the same horizontal level then you can consider this setting dialed in.

[Mennenth’s Notes: This is one of the big “sleeper settings” when it comes to getting the Touchpad to feel good as a Mouse. There were loads of people at launch who complained about the Touchpad being inaccurate, but given how many reviewers - especially mainstream reviewers - never really bothered with any settings at all I imagine this was the culprit. If the xy grid is not lined up with your thumbs' natural movements, then what is happening on screen has far less of a chance to match up with what you intended to happen on screen; you swipe horizontally left, but the game's camera goes left and down so you miss your target. Clearly that means the Touchpad is inaccurate, right? Well, if that has happened to you then I strongly urge you to play around with this setting. For me, the Touchpads xy grid is lined up with my thumbs’ natural horizontal swipe when the slider is approximately 3 ticks from maximum.]

### Acceleration

This setting is available to both Touchpads and Gyro.

Acceleration causes sensitivity to become dynamic, based on how fast or slow the user makes inputs. This can allow the user to have both precise movements when making slow inputs and broad movements when making faster inputs, overcoming the issues associated with limited ranges of motion.

This setting has 4 options, which determine the strength of the Acceleration:

Off
Low
Medium
High

### Trackball Mode

This setting is only available to the Touchpad.

Trackball Mode gives the Mouse virtual “momentum” when you swipe and lift your finger - “flicking” the pad -, causing it to act like a Trackball; it will continue to move the cursor for a short duration of time, slowing down as time goes on. The user can also preemptively stop this motion by setting their thumb back down on the Touchpad.

It has two options:

On
Off

### Trackball Friction

This setting is only available to the Touchpad.

This setting determines how quickly the virtual trackball will come to a stop.

It has 5 options:

Off - stops immediately
Low - takes a long time to stop
Medium - takes some time to stop
High - takes a short time to stop
None - will go on forever until the user places their thumb back on the Touchpad

### Friction Vertical Scale

This setting is only available to the Touchpad.

This slider determines how quickly the virtual ball's y axis comes to a stop relative to its x axis.

As Valve mentions in the description, having a higher vertical friction can be beneficial for games where the mouse controls the camera, so horizontal flicks can rotate mainly the x axis without impacting the y axis very much if at all.

[Mennenth’s Notes: I really love Trackball Mode for desktop navigation, but in games I usually leave it disabled.]

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

Off
Low
Medium
High

[Mennenth’s Notes: Other than Trackball Mode being enabled, I really don’t like haptics for Mouse on either Touchpad or Gyro. It could just be the implementation, but to me the haptic rumbling simply is not consistent enough. If you move slowly, the haptics have long pauses in between pulses which feels more like detents on a knob instead of Mouse movement. For Trackball it is fine because a good flick will cause the haptics to work well enough to sell the illusion of a ball rolling, but for everything else Mouse related I’d rather turn the haptics off.]

### Invert Vertical Axis

This setting is available to both Touchpad and Gyro.

This setting has two options:

Off
On

When turned on, this flips any y axis movement; down becomes up, and up becomes down.

!! CAUTION !! As per Valve’s description, be mindful of any in-game settings that also invert the y axis, as they could cancel each other out.

### Sensitivity Vertical Scale

This setting is available to both Touchpad and Gyro.

This slider determines how sensitive the y axis is compared to the x axis. Further to left emphasizes horizontal sensitivity while further to the right emphasizes vertical sensitivity. It is possible to completely remove the y axis by moving the slider all the way to the left, but it is inconsistently not possible to remove the x axis by moving the slider all the way to the right. All the way to the right will result in a still usable x axis but an extremely emphasized y axis.

For Touchpads, the default value results in a 1:1 ratio for sensitivity.

For Gyro, the default value results in a 16:9 ratio. That ratio is the same as the typical desktop monitor, which is great for desktop navigation. However, if you would like a 1:1 ratio with the Gyro for camera control in game you will need to use an actual mouse to set this slider to 0.890. Unfortunately, that is still not true 1:1. Steam Input simply snaps to the nearest 0.XX5 or 0.XX0, and as a result 0.890 is the closest to 1:1 that is possible in Steam.

[Mennenth’s Notes: This is the second “sleeper setting” for getting a good response from the Touchpad as a mouse. Remember how with Rotation it is possible to line up the xy grid with the natural horizontal movement your thumb makes, but there is still a bit of up and down movement as thumbs move in arcs instead of straight lines? When the slider is pushed left, it clamps down on that up and down movement flattening the curve into more of a straight line. I would not recommend removing the y axis all together, but setting the slider halfway between default and all the way left has yielded great results for me.

As an aside to any Valve devs reading this; it's a small thing but please add a check box or a drop down setting that overrides this slider and forces true 1:1 for Gyro. 1:1 is how JoyShockMapper handles Gyro input, and is preferred for fps’.]

### Touch Binding

This Binding is only available to Touchpads.

This Binding activates whenever you touch the Touchpad.

### Trigger Press Mouse Dampening (drop down menu)

This setting is available to both Touchpads and Gyro.

If a game does not have any ADS mode or sensitivity slow down/sniper button of its own, or if you would like additional buttons to slow down your sensitivity, you can add it with this setting and determine which button enables the pseudo-ads.

There are 7 options for this setting, which determine what button or combinations of buttons cause the slow down:

Off
Right Trigger Soft Pull Dampening
Left Trigger Soft Pull Dampening
Both Trigger Soft Pull Dampening
Right Trigger Soft/Full Pull Dampening
Left Trigger Soft/Full Pull Dampening
Both Trigger Soft/Full Pull Dampening

### Trigger Press Mouse Dampening (slider)

This setting is available to both Touchpads and Gyro.

This slider determines how slow the mouse movement should become when the Dampening is activated. Further to the right is slower.

### Smoothing

This setting is available to both Touchpads and Gyro.

This setting filters the input to remove any noise or jitter to provide a smoother experience. The slider controls how much filtering is applied; to the left is less smoothing, to the right is more smoothing.

!! CAUTION !! Too much smoothing can result in increased input latency, which can cause the game's camera to feel like you are trying to pull it through mud/molasses/other thick liquid.

### Double Tap Binding

This Binding is only available to Touchpads.

This Binding behaves similarly to the Touch Binding, however you must Double Tap the Touchpad to activate it (similar to the Double Press Activator. More on Activators in Chapter 4).

### Double Tap Duration

This setting is only available to Touchpads.

This slider determines how quickly you must Double Tap the Touchpad to activate the Double Tap Binding. More to the left will require quicker double taps, while more to the right gives you more time to double tap.

### Double Tap Beep

This setting is only available to Touchpads.

This setting has 2 options:

Off
On

If set to On, the haptics will audibly beep whenever the Double Tap is activated.

[Mennenth’s Notes: Despite the existence of the Touch Binding with a Double Press Activator, the Double Tap Binding is actually surprisingly useful. You can use Activators with the Double Tap Activator too, which gives it more flexibility than the Double Press Activator. I like using the Double Tap Binding for whatever button the game uses as its “Interact” button.]

### Gyro Steering Axis

This setting is only available to Gyro.

This setting has 2 options:

Yaw
Roll

This sets which type of Gyro rotation controls the horizontal movement of the Mouse.

To better visualize, stick your hand out with your index finger pointing forward and your thumb pointing up. This represents the controller laying flat. Yaw would be sweeping your index finger left and right while your thumb remains pointing up. Roll would be tilting your thumb left and right while your index finger remains pointing forward.

Remember the Gyro Lean Bindings from earlier? Leaning uses the axis not being used for Steering.

[Mennenth’s Notes: Despite some rather aggressive arguments that have happened online over this, this setting is mostly preference and NOT one being more intuitive than the other. I personally think that on a controller Yaw makes sense as I view it as a laser pointer coming out of the usb port of the controller and pointing at the screen. However a lot of mobile gamers swear by Roll and I can understand the logic there; the screen is kind of like a camera, and in that situation roll makes a lot of sense. So perhaps the context matters?

Nintendo, specifically Splatoon 2, does things a bit differently by mixing and transitioning between Yaw and Roll dynamically depending on the Pitch angle of the controller. JoyShockMapper also recently updated to include a “PlayerSpace” method of handling the Gyro that works similarly to the Splatoon 2 method. 

To any Valve devs reading this, please add PlayerSpace as an option. Have it disable the Lean Bindings if needed, but it would be really nice to experiment with PlayerSpace on my Steam Controller.]

### Gyro Lean Point

This setting is only available to Gyro.

Remember the Gyro Lean Bindings from earlier?

This slider determines how far you have lean the controller to activate the Lean Bindings.

### Edge Spin Radius

This setting is available only to Touchpads.

This slider determines the distance from center, the radius, at which Edge Spin happens.

#### What is Edge Spin?

Think of Edge Spin like a Joystick. If tilted in a direction, the Mouse will continue to move in that direction at a constant rate.

With Edge Spin, you basically get “absolute_mouse” in the center of the Touchpad and “relative_mouse” at the Edge of the Touchpad. This can help alleviate the issue of limited range of motion. By providing a way to constantly move the mouse, using Edge Spin drastically reduces the amount of swiping the user needs to make on the Touchpad in order to make large camera movements.

### Edge Spin Speed

This setting is available only to Touchpads.

This slider determines how fast the Mouse will continue to move when Edge Spin has been engaged. Further to the right is faster. At all the way to the left, which is default, Edge Spin is disabled.

[Mennenth’s Notes: Edge Spin is really wonky. You can’t simply tap the edge of the Touchpad to engage Edge Spin, you have to swipe to the Edge and then hold it there… which then also impacts Edge Spin Speed as it carries the momentum - or lack thereof - from the swipe. It has potential when it comes to tracking a moving target over long distances of moving the same direction, but it functions so weirdly that I personally have never bothered to get used to it.]

### Minimum Movement Threshold

This setting is available to both Touchpad and Gyro.

This setting causes input to initially not be sent but rather built up until a threshold is hit and then sent all at once.

As Valve’s description says, its main use is to counter any aggressive filtering a game might have that results in smaller movements being lost. By building up the movement and sending it all at once, it can overcome that filtering. The more to the right the slider is, the larger the threshold is requiring more movement to be built up before being sent. The default of all the way left has no threshold; any movement is sent at all times.

!! CAUTION !! Too much Minimum Movement Threshold can cause the Mouse to feel like it's snapping to places on a grid instead of moving smoothly as the threshold is constantly being overcome and then fallen behind over and over.

[Mennenth’s Notes: I typically have no MMT on gyro, and possibly only a tiny amount on Touchpad if using Mode Shift Clicks to prevent accidental Mouse movement while clicking the Touchpad.]

### Invert Horizontal Axis

This setting is available to both Touchpad and Gyro.

This setting has 2 options:

Off
On

If set to On, the x axis becomes flipped; left becomes right, right becomes left.

[Mennenth’s Notes: It's natural to think it odd to invert the x axis, but for Gyro this actually has a brain bender of an application; reducing the amount of “ratcheting” needed to make broad camera movements with Gyro. Instead of setting a Gyro Enable Button, consider having the Gyro set to Always On and then set up a Mode Shift (more on those in Chapter 04) to give the Gyro the exact same settings just with Invert Horizontal Axis set to On. Turn right to the point of hitting your wrists range of motion but still need to turn right? Activate the Mode Shift which inverts the x axis. Now when you physically turn the controller left to recenter the Gyro will still be turning right!]

## Overall Mennenth’s Notes

Once again, Mouse is a cornerstone Input Style especially for first person shooters or other cursor driven games.

The Mouse being integral to pc gaming is a big reason why Valve went with Touchpads for the Steam Controller. As a pc gaming controller first and foremost, it simply has different requirements to fill compared to a more traditional modern console controller.

However, while the Touchpad is a great input device the Gyro is the real star of the show here.

Compared to moving your thumb within a 40mm circle, the Gyro gets both arms involved in the aiming process. It can be very fast and accurate as a result. Indeed, the broader Gyro Gaming community has done things such as Aimlab challenges and using only the Gyro people who have participated in those challenges have posted really amazing scores. The current record for Aimlab Gridshot with a Gyro as far as I’m aware is held by a Steam Controller user [insert link to megaphones 92k run]. Gyro users are basically performing on the same level as desktop mouse users.

That isn’t to say Gyro is a panacea for aiming on a controller. It has a pretty significant weakness; the range of motion is limited by your wrists, and even with a way to dynamically enable or disable the Gyro to recenter when that limit is reached that then introduces “ratcheting”.

But that weakness can be overcome!

The Touchpad, despite its more restricted range of motion and reliance on the thumb which is NOT good at precision, can easily cover for that weakness.

By setting the Touchpad up with a higher sensitivity, the Touchpad can then take care of all the broad camera movements, referred to as “fast turn” from here on out, while the Gyro handles all the “precision aiming” work. This is an incredibly effective way to play first person shooters on the Steam Controller.

To prevent this section from going too long, I’ll not repeat what I mentioned in all my earlier notes. I already covered pretty much everything in them… except for how I set my Sensitivities.

Because the Sensitivity Slider is basically an abstracted dpi setting and because Touchpads and Gyros are not mice, myself and many others have recontextualized how to go about tuning sensitivity for them.

For the Touchpad, that recontextualization comes in the form of leaning into the idea of the Touchpad being a “fast turn” input to cover for the Gyro’s limited range of motion. The idea is to choose a “degrees per swipe” amount. 

For instance, I prefer 270 degrees per swipe. What that means is that when I make a full horizontal swipe on the Touchpad, the camera will go through 270 degrees of x axis rotation. Some prefer lower numbers like 180 degrees per swipe, some even lower or some even a full 360 degrees! Regardless, choose an amount you feel comfortable with and tune Touchpad sensitivity from there.

For the Gyro, I have taken a page out of the Gyro Gaming communities book and tuned for what they call a “Real World Sensitivity”. In a nutshell, if you rotate the controller on the x axis through a full 360 degrees, how many times does the in-game camera do a full 360? If only once, that is a Real World Sensitivity of 1. 1 means that the in-game camera does exactly what you are doing with the gyro.

I play with a Gyro Real World Sensitivity of 3, meaning the in-game camera does a full 360 degree x axis rotation for every one 360 my controller does. That may seem high, but some play at a Real World of 4 or higher.

If you are just starting out with Touchpad and Gyro Mouse aiming, I would recommend starting with lower sensitivity values for both. That is what I have done, and I have slowly increased them to their current values over time as I have become more comfortable using the Steam Controller.

If you are using a different controller that has Gyro and a right Joystick, so not the Steam Controller, you can still benefit from the Real World Sensitivity for the Gyro and can still use your Joystick as a “fast turn” input. In fact, there is an Input Style specifically for using a Joystick in combination with a Gyro that way, but that is for another chapter.
