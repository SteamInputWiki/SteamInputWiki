# Chapter 02c: Mixed input

## What is Mixed Input?

"Mixed input" (the name I use), "simultaneous input", and probably others, this goes by many names but ultimately when people mention it you might wonder what they are talking about.

"Mixed input" is when a player wants to use or is even in the process of using both a gamepad and a keyboard and mouse at the same time (hence "simultaneous" is another name).

Typically speaking, this situation happens most frequently in first person shooters or in other games that have strong aiming components. The idea is that on pc, you'd want the analog control over movement but mouse control over aiming. Playing games this way is really effective, and as such is gaining popularity.

There are tons of examples of mixed input. The most basic are users who hold a xbox controller in their left hand but are moving a mouse with their right. Some people use a sony playstation move controller instead, for improved 1 handed ergonomics.

There are even products that are one handed controllers made specifically for use in this scenario.

Keyboards with analog wasd so the wasd keys can function together as a left analog stick are also starting to pop up, and there are also devices like the Azeron which are 1 handed macro keyboards that have an analog stick for use with the thumb.

These are all examples that are beyond the bounds of steam input, but serve to show that mixed input is something that is gaining popularity.

What is inside the scope of this guide are controllers that are equipped either with touch pads or gyroscopes, or both. This includes the switch pro controller (lacks touch pad but has gyro), dualshock 4 and dualsense (gyro, and an aux touch pad), steam controller (primary touch pads and gyro), and soon to be steam deck (basically everything). Sorry xbox fanbois, your controller of choice simply lacks this feature.

These single controllers can accomplish mixed input entirely on their own, as the touch pads and gyros can be assigned to mouse control while the analog sticks can retain their analog control.

## Unfortunately, not all games actually support mixed input. And its a gradient.

Some games will straight up lock you into the first type of input the game detects.

Some games will bounce back and forth between the input systems, which can cause issues such as slowing down/interrupting either the stick or mouse inputs, or if the render engine is tied to inputs then it may tank performance to unplayable levels.

Other games may technically allow it to happen, but then the button prompts will flicker back and forth between gamepad prompts and keyboard/mouse prompts rapidly enough that its incredibly bothersome.

There are some work-arounds for this compatibility issue, but they are always compromises.

The first work around is to rebind your controller to fully keyboard and mouse binds.

As discussed in the dpad input style chapter, you can set up doad mode with wasd keys and then turn on analog emulation to make it feel sort of like an analog input.

There are 2 downsides of this method; first is that your button prompts will not match your control, and second is that in some games analog emulation will cause animation issues. Its not ideal.

The second work around is to go all gamepad bindings.

As discussed in an earlier segment, mouse-joystick allows you to treat the touch pad or gyro like a mouse, but that input gets converted to joystick movements.

There is one major downside to this work around; mouse-joystick is restricted to how the game handles joystick input, and as such mouse-joystick is incredibly game reliant and will never feel as good as actual mouse input. Everything from jerky grid like movement due to deadzone issues, weird acceleration that somehow means the faster you make inputs the slower the game responds, etc. Its just not that great of an experience.

Do note; not supporting mixed input does not mean the game is not playable with mixed input enabled hardware. Steam Controller users have become pretty familiar with simply going all keyboard and mouse binds - no wasd analog emulation - and putting up with the wrong button prompts. The games are still totally playable. Not supporting mixed input simply means the experience will not be the best it can be.

So with all that in mind…

## A Plea to Developers:

With the increasing popularity of devices that can enable mixed input, please ensure your game supports being played this way.

At a minimum, please test and make sure your games have no outstanding issues when using both a joystick for movement and a mouse for aiming at the same time.

Beyond that though...

Auto device detection has its use, but its time to set that bit of code aside (not fully, it can be an option thats defaulted to as a middle ground) and give the player some choice. The best case here is to allow the player to use any input they want - including mixed - and give them the option to lock in their preferred glyph set for the button prompts.

If you wanted to get really fancy you could natively support the controllers gyro input as a mouse. While that would solve the issue for gyro controller users, remember that this would also leave all the other examples of mixed input behind.

If you are a dev reading this wiki and only take away one thing, that takeaway should absolutely be "mixed input is worth supporting". Especially now. If the Deck winds up as popular as the hype is suggesting, it really will behoove you to ensure your players can get the most out of the controls available to them while playing your game.

One final note; this applies when implementing SIAPI as well. If your siapi implementation does not have an absolute_mouse input style, a player may want to use siapi+mouse which would once again fall under mixed input. Death Stranding does this perfectly; uses siapi, allows mouse at the same time, AND gives the player the option to lock which button prompts they want. Be like Death Stranding.
