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

