# Chapter 05f: Accommodating Accessibility in Input as a Developer

The following guide is not meant to shame developers that have not previously considered or have been unable to cater to many different accessibility options. We understand that sometimes these different features may be at odds with either your budget, work capacity, or even your ultimate vision for your project. We simply love gaming and want to share the medium with as many people as possible while fostering a more loving community.

We'd like to take this moment to remind developers optimizing for Steam Input should not be relied on for its accessibility functionality. As will be discussed later in [Chapter 06b01](https://github.com/SteamInputWiki/SteamInputWiki/blob/main/chapter-6/06b01_deciding_if_steam_input_is_right_for_your_project.md#06b01-deciding-if-steam-input-is-right-for-your-project), we should never be making assumptions about how our player will be interacting with our game based on input sources and hardware design characteristics. We should be allowing the player to have the ability to override any of these design decisions.

Also worth mentioning fundamental features such as game remapping, dead zone tweaks, and other accessibility-based changes to input should never be left up to other input remapping software. Although we recommend having these features optimized for remapping software, these features should be built directly into your game to provide ease of access regardless of what software your players have installed or platform purchased from.

### Using Haptics Has an Alternative Feedback Source

Players that have either visual-based or auditory-based disabilities may benefit from having different forms of feedback than what may be included for the general consumer. Although there are many ways of accomplishing this given that our information is based solely on input we are going to be presenting one option for this however we do recommend your team talking about and considering as many accessibility options as possible.

Has a replacement for visual or auditory cues haptics either through traditional Rumble Motors or more modern Haptic Motors in many cases could be used to outright replace these traditional methods of feedback. An FPS game for example might use haptics in the direction the player is being shot at in order to give an alternative to auditory feedback. Another example might be an open world game using haptics pulsing in a specific direction in addition to a visual on-screen direction to help the player locate an objective.

In most scenarios we see these effects potentially being used; they are most likely to be in addition to currently present gameplay and therefore don't necessarily need to be added as a menu option. As always we recommend the ability to turn this functionality off, potentially bundled in with your normal haptics options. If for some reason you feel this feature may not work best for all players and instead want to add it as a substitute we recommend placing it somewhere in your accessibility menu.

### Handling Haptics for Those With Sensory Issues

Haptics can be a very useful form of feedback for users either for accompanying new forms of input or simply giving more when using actions players are already used to. The problem may come in when a small subset of your player base might have issues dealing with the feeling of this new addition to the experience.

Players may experience aversion to other forms of sensory inputs however because this is focused mainly on input we are not going to be covering visual or auditory issues.

Developers that are creating experiences that will utilize native haptics on a hardware level we recommend making these facets optional entirely.

As of writing Steam Input currently has issues regarding certain input sources not allowing the haptics to be completely turned off. As such developers wanting to use Steam Input's current haptic effects yet still provide the option to turn them completely off must do it manually by overriding the haptic motors at a native level.

If a developer decides to account for sensory issues regarding haptics, we suggest giving the player the option to turn them off in your accessibility menu. For developers that want to go beyond, I would suggest including at least one mode with lower haptics and potentially an alternative mode that replaces custom haptics with a more basic rumble-like interpretation.

### Handling Rumble Has an Accessibility Issue

Players with limited motor function or dexterity as well as many other situations may find rumble or even haptic-based effects to impede their ability to play your game. It may make it difficult for players in these situations to physically hold the device or potentially make it difficult for the player to complete inputs.

As stated in the previous point, developers much like with haptic motors I should be providing at the bare minimum a toggle for traditional rumble functionality. Developers wishing to go above and beyond may want to include various levels of rumble. Officially we would recommend placing this setting somewhere in your controller menu or possibly within or near your options for haptic-based controllers.

### Providing Adequate Options for Dexterity-based Inputs

The following suggestion isn't necessarily input related but can be. The best practice when including Quick Time event sequences in your game should be to allow your player to skip them in some manner.

How you should tackle could be entirely up to interpretation; it could be an option to disable it and replace it with an in-game cutscene, you could give the player the option to skip cutscenes at any point in time by pressing a specific button, or you could even include the option after the player has failed a cutscene several times.

Personally I recommend doing two of those three options at the same time. Best practices could be to include this as an option and either your accessibility options menu or your gameplay options menu.

### Ensuring That Players Have Alternate Options for Button Action Behavior

Developers should take into consideration that people with physical disabilities may not necessarily be able to mash buttons within certain periods of time or potentially press buttons requiring a certain level of force on the controller. These types of concessions should be taken into account during the beginning of development.

The popular rule of thumb is that a developer should never be forcing multiple actions at once; the action of for example pushing in a joystick click while holding the joystick forward to run may be very difficult for players. Providing options to change holds into a toggle or varying other options along this line of thought should be included has a best practice.

### Aim Assist Has an Accessibility Feature

For single player games and cooperative games rather than locking aim assist functionality; specifically behind using a controller for several reasons it would be more ideal for a developer to provide them as an additional option regardless of what input device the player is using. Typically in single player and cooperative experiences PVP typically doesn't come into play. By giving  the player the option to use aim assist if it is more helpful to them, you're encouraging the player to further customize their gaming experience to what works for them.

Making these features available regardless of input is very important because (once more) we don't know what the player is going to be using. Your player may choose to use multiple controllers in tandem, play with gyro functionality using a more traditional controller, or even just occasionally use keyboard keys while using a typical controller layout as well as any other conceivable scenario. Making these changes should be considered part of your thought process when making sure that your project is capable of receiving inputs without giving any undesired issues while interacting with unorthodox input methods.

As a best practice this should always be an option, most likely contained within your game's standard controller options settings. Whether or not you should default to this arrangement should really lie behind the type of game and how you feel your players will interact best with the game world. Personally I would recommend a developer make three or more options, automatic switching based on input, off, on, and potentially have either more options for the strength of aim assist or a separate option's menu specifically for adjusting aim assist.

We feel like these changes will be one of the most important physical accessibility settings you can provide simply because although this is an entirely software solution, it is also something that only you as a developer can provide. It simply cannot be provided in any shape from a third-party software. Ideally these solutions should be available for every platform your game is distributed under as well as every console your game releases on.

### Motion Controls Has an Accessibility Feature

Gyro controls can both be an accessibility feature while also being detrimental to accessibility for certain players. Both sides of these coins are true depending on a player's unique strengths and weaknesses. It is recommended to provide the option for gyro support on any platforms that support it by whatever means you see fit based on your project. 

However, Gyro control should always be an optional feature and never a requirement. All game mechanics that are motion based should have some type of alternative mode allowing the player to accomplish the same tasks without ever needing gyro. Although depending on the players proficiency gyro may provide a gameplay advantage, single player games especially should never provide any type of advantage for any source of input that cannot be present or shared by another input source i.e. allowing the player to earn rewards based on a motion-controller only minigame or other forms of exclusive content. While we would never suggest developers stray away from these features, we do ask that you consider how your player will be able to interact with these features and provide other options for experiencing the game.

While Gyroscopic controls could be considered fully an accessibility feature we recommend you place this along with all other input related features in your controller options menu.

### Compatibility With CoPilot and Multi-Controller Setups

Mixed Input does not always refer entirely to using mouse controls while using standard Gamepad controls. Mixed Input can also encompass the concept of using more than one controller; The most current example being Microsoft's Copilot feature for the Xbox family and Windows family of systems.

The Copilot feature is a very good first step however it takes the control out of your hands as a developer and may not necessarily work with every single scenario. It is still recommended to make sure at the very least that your input system allows the option for using multiple controllers at the same time as player one, this way your game will be more equipped to handle a large multitude of different custom input setups that may be necessary for players with disabilities.

It's also important to remember it is impossible to create workarounds for every single disability within your game; giving the player the most control possible is all you can do. We highly recommend making sure that your input system is capable of handling any arbitrary input source including mouse and gamepad in addition to the potential for more than one gamepad, If this is something that you're worried may affect other players negatively simply having these has options either under the accessibility settings menu or controller settings is how we would recommend you to implement.

### How Developers Should Handle Optimizing for Adaptive Technologies

When optimizing for adaptive technologies it is still best to leave these options in your option menu. The knock on effect of having certain features only activate when an adaptive technology is detected is twofold; we don't know whether or not the user wants to use this added functionality and we don't know whether or not our user is going to be using adaptive technologies that are in your database. Users without access to adaptive technologies may still need these additional accessibility features as well.

## Recommended Resources for Other Accessibility Features and Ideas

Unfortunately at this time we can only really cover accessibility specifically pertaining to input related issues, however we encourage developers to think outside the box and try and understand ways that they can modify how they tackle their future projects to better cater to the needs of persons with disabilities. These tweaks go far beyond physical limitations, sight-based limitations, and auditory limitations.

We recommend checking out https://accessible.games for more ideas on how your projects could better cater for accessibility.
