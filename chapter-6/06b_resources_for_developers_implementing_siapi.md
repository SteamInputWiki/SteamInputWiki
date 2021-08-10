# Chapter 06b: Resources for Developers implementing SIAPI

Unfortunately, as a player and not a coder all I can really do is link you to the Valve docs for implementing SIAPI. Those are found here:

https://partner.steamgames.com/doc/features/steam_controller/getting_started_for_devs

However, I would like to offer some perspective as a player on what I believe makes a good SIAPI implementation

## Best Practices

A really good starting point will be to look through the earlier segments of this chapter to see how other SIAPI implementations have been rated, to help inform how you should implement siapi into your game. Though as a brief summary, I have attempted to distill out some key points.

### neutral:

* directly recontextualizing xinput/"the console controls" into siapi with no real changes; not inherently bad, but may as well have not implemented siapi

### bad:

* doesnt have xinput/other native controller support as a fall back option for controller players not opted into steams controller config
* doesnt allow mixing input sources (xinput + siapi + kbm, all at the same time)
* uses auto device detection for determining which glyph set to use for button prompts; this often causes issues with the above. Give the player the option of which set to use and to lock the set
* unnecessarily locks certain inputs in a certain way:
  * Horizon Zero Dawn's hard coding of the steam controllers left touch pad as a dpad
  * if the game uses the triggers, but only as a digital action with no analog component, locking that action to a siapi trigger input style instead of having it be a bindable digital action (think firing a gun, boost in a vehicle, etc)

### good:

* every MAJOR game context has an action set it auto swaps to when in that context (menu, on foot, in car, in flight, etc)
  * In contrast to Valves docs, DONT use action layers. Action layers are a pretty vital tool for power gamers who use siapi when they customize their configs to suit their playstyle. If you automate layers as well as sets, you are removing customization options from the player. Automate ONLY sets.
* in every context, ALL possible actions for that context have a dedicated bindable action
    * a non siapi example of a fail here; Dark Souls has sprint and dodge tied to the same button (B in terms of xinput). While this may be because of a lack of inputs available on a xbox controller, you should assume that when siapi is being used then there are enough inputs to support them being separate due to the wide variety of controllers siapi supports as well as user creativity if they customize the controls
    * If you simply want to replicate Dark Souls' use of the B button for dodging and sprinting while still having them be independent actions, both actions would be bound to the same button HOWEVER dodge would be set to an interruptible regular press activator and sprint would be set to a long press activator. This would accomplish the same thing as hardcoding the B button to do both, but unlike hard coding it would offer the player more freedom when rebinding/customizing the config to their liking.
* including an absolute_mouse input style for touch pad/gyro users
    * if absent, see "bad" section about mixing input sources
* doing unique/novel things that are only possible thanks to siapi
    * siapi can provide the raw gyro quaternions and touch pad data to the game... do something cool with them (as long as there are no conflicts with the above)!
